<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <title>서면나눔5일장</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link href="https://unpkg.com/tailwindcss@^2/dist/tailwind.min.css" rel="stylesheet">
</head>
<body class="font-sans text-gray-800 bg-gray-50">

<!-- Header -->
<header class="bg-white shadow-sm">
  <div class="max-w-6xl mx-auto px-4 py-4 flex items-center justify-between">
    <h1 class="text-lg font-bold">서면나눔5일장</h1>
    <button id="login-btn" class="px-3 py-1 bg-blue-600 text-white rounded">관리자 로그인</button>
  </div>
</header>

<!-- 게시판 -->
<section id="posts" class="bg-white py-10">
  <div class="max-w-6xl mx-auto px-4">
    <h3 class="text-2xl font-bold mb-4">게시글</h3>

    <!-- 글쓰기 영역 (관리자 전용) -->
    <div id="write-section" class="mb-6 hidden">
      <input id="post-title" type="text" placeholder="제목" class="border p-2 w-full mb-2 rounded">
      <textarea id="post-content" placeholder="내용" class="border p-2 w-full mb-2 rounded"></textarea>
      <input id="post-image" type="file" accept="image/*" class="mb-2">
      <input id="post-video" type="file" accept="video/*" class="mb-2">
      <button id="post-submit" class="px-4 py-2 bg-green-600 text-white rounded">게시</button>
    </div>

    <!-- 글 목록 -->
    <div id="post-list" class="flex overflow-x-auto space-x-4"></div>
  </div>
</section>

<!-- 관리자 로그인 모달 -->
<div id="login-modal" class="fixed inset-0 bg-black bg-opacity-50 flex justify-center items-center hidden">
  <div class="bg-white p-6 rounded shadow-md w-80">
    <h3 class="text-lg font-bold mb-4">관리자 로그인</h3>
    <input id="admin-id" type="text" placeholder="ID" class="border p-2 w-full mb-2 rounded">
    <input id="admin-pw" type="password" placeholder="비밀번호" class="border p-2 w-full mb-4 rounded">
    <div class="flex justify-end space-x-2">
      <button id="login-cancel" class="px-3 py-1 bg-gray-400 text-white rounded">취소</button>
      <button id="login-confirm" class="px-3 py-1 bg-blue-600 text-white rounded">로그인</button>
    </div>
  </div>
</div>

<script>
let posts = [];   // 글 저장
let isAdmin = false;

// 글 렌더링
function renderPosts() {
  const list = document.getElementById('post-list');
  list.innerHTML = "";
  posts.forEach((post, index) => {
    const div = document.createElement('div');
    div.className = "border p-4 w-96 flex-shrink-0 search-item";
    div.innerHTML = `
      <h4 class="font-semibold mb-1">${post.title}</h4>
      <p class="mb-2 whitespace-pre-line">${post.content}</p>
      ${post.image ? `<img src="${post.image}" class="mb-2 rounded">` : ""}
      ${post.video ? `<video controls class="mb-2 rounded"><source src="${post.video}"></video>` : ""}
      ${isAdmin ? `
        <div class="flex space-x-2">
          <button onclick="editPost(${index})" class="px-2 py-1 bg-yellow-500 text-white rounded">수정</button>
          <button onclick="deletePost(${index})" class="px-2 py-1 bg-red-600 text-white rounded">삭제</button>
        </div>
      ` : ""}
    `;
    list.appendChild(div);
  });
}

// 글쓰기
document.getElementById('post-submit').addEventListener('click', () => {
  const title = document.getElementById('post-title').value.trim();
  const content = document.getElementById('post-content').value.trim();
  const imageFile = document.getElementById('post-image').files[0];
  const videoFile = document.getElementById('post-video').files[0];

  if (!title || !content) {
    alert("제목과 내용을 입력하세요");
    return;
  }

  let newPost = { title, content, image: null, video: null };

  if (imageFile) {
    const reader = new FileReader();
    reader.onload = e => {
      newPost.image = e.target.result;
      if (videoFile) {
        const vReader = new FileReader();
        vReader.onload = ev => {
          newPost.video = ev.target.result;
          posts.push(newPost);
          renderPosts();
        };
        vReader.readAsDataURL(videoFile);
      } else {
        posts.push(newPost);
        renderPosts();
      }
    };
    reader.readAsDataURL(imageFile);
  } else if (videoFile) {
    const vReader = new FileReader();
    vReader.onload = ev => {
      newPost.video = ev.target.result;
      posts.push(newPost);
      renderPosts();
    };
    vReader.readAsDataURL(videoFile);
  } else {
    posts.push(newPost);
    renderPosts();
  }

  document.getElementById('post-title').value = "";
  document.getElementById('post-content').value = "";
  document.getElementById('post-image').value = "";
  document.getElementById('post-video').value = "";
});

// 글 수정
function editPost(index) {
  const post = posts[index];
  document.getElementById('post-title').value = post.title;
  document.getElementById('post-content').value = post.content;
  posts.splice(index, 1);
  renderPosts();
}

// 글 삭제
function deletePost(index) {
  if (confirm("정말 삭제하시겠습니까?")) {
    posts.splice(index, 1);
    renderPosts();
  }
}

// 로그인 기능
const loginBtn = document.getElementById('login-btn');
const loginModal = document.getElementById('login-modal');
const writeSection = document.getElementById('write-section');

loginBtn.addEventListener('click', () => loginModal.classList.remove('hidden'));
document.getElementById('login-cancel').addEventListener('click', () => loginModal.classList.add('hidden'));
document.getElementById('login-confirm').addEventListener('click', () => {
  const id = document.getElementById('admin-id').value;
  const pw = document.getElementById('admin-pw').value;
  if (id === "eonju23" && pw === "200301") {
    isAdmin = true;
    alert("관리자 로그인 성공");
    writeSection.classList.remove('hidden');
    loginModal.classList.add('hidden');
    renderPosts();
  } else {
    alert("로그인 실패");
  }
});
</script>
</body>
</html>
