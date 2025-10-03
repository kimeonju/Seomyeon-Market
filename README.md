<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <title>서면나눔5일장</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link href="https://unpkg.com/tailwindcss@^2/dist/tailwind.min.css" rel="stylesheet">
</head>
<body class="font-sans text-gray-800 bg-gray-50">

<header class="bg-white shadow-sm">
  <div class="max-w-6xl mx-auto px-4 py-4 flex items-center justify-between">
    <h1 class="text-xl font-bold">서면나눔5일장</h1>
    <div class="flex items-center space-x-2">
      <input id="search-input" type="text" placeholder="검색..." class="border p-2 rounded w-64">
      <button id="login-btn" class="px-2 py-1 bg-blue-600 text-white rounded">관리자 로그인</button>
    </div>
  </div>
</header>

<main class="max-w-6xl mx-auto p-4">
  <!-- 상품 -->
  <section id="products" class="py-10">
    <h2 class="text-2xl font-bold mb-4">상품</h2>
    <div id="product-form" class="hidden mb-6">
      <input id="product-name" type="text" placeholder="상품명" class="border p-2 w-full mb-2 rounded">
      <input id="product-price" type="text" placeholder="가격" class="border p-2 w-full mb-2 rounded">
      <button id="add-product" class="px-4 py-2 bg-green-600 text-white rounded">상품 추가</button>
    </div>
    <div id="product-list" class="flex overflow-x-auto space-x-4"></div>
  </section>

  <!-- 게시글 -->
  <section id="posts" class="py-10">
    <h2 class="text-2xl font-bold mb-4">게시글</h2>
    <div id="write-section" class="hidden mb-6">
      <input id="post-title" type="text" placeholder="제목" class="border p-2 w-full mb-2 rounded">
      <textarea id="post-content" placeholder="내용" class="border p-2 w-full mb-2 rounded"></textarea>
      <button id="post-submit" class="px-4 py-2 bg-green-600 text-white rounded">게시</button>
    </div>
    <div id="post-list" class="flex overflow-x-auto space-x-4"></div>
  </section>
</main>

<!-- 로그인 모달 -->
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
// ================== GitHub 연동 설정 ==================
const GITHUB_USER = "사용자명";     
const GITHUB_REPO = "레포명";      
const DATA_PATH   = "data.json";   
const BRANCH      = "main";        
const TOKEN       = "ghp_토큰";     

let posts = [];
let products = [];

// 데이터 불러오기
async function loadData() {
  try {
    const res = await fetch(`https://raw.githubusercontent.com/${GITHUB_USER}/${GITHUB_REPO}/${BRANCH}/${DATA_PATH}?t=${Date.now()}`);
    const data = await res.json();
    posts = data.posts || [];
    products = data.products || [];
    renderPosts();
    renderProducts();
  } catch (err) {
    console.error("데이터 로드 실패:", err);
  }
}

// 데이터 저장하기
async function saveData() {
  const url = `https://api.github.com/repos/${GITHUB_USER}/${GITHUB_REPO}/contents/${DATA_PATH}`;
  const content = btoa(unescape(encodeURIComponent(JSON.stringify({posts, products}, null, 2))));
  const getRes = await fetch(url, { headers: { Authorization: `token ${TOKEN}` } });
  const getData = await getRes.json();
  const sha = getData.sha;

  await fetch(url, {
    method: "PUT",
    headers: { "Authorization": `token ${TOKEN}`, "Content-Type": "application/json" },
    body: JSON.stringify({
      message: "자동 업데이트",
      content: content,
      sha: sha,
      branch: BRANCH
    })
  });
}

// 렌더링
function renderPosts(filter="") {
  const list = document.getElementById("post-list");
  list.innerHTML = "";
  posts.filter(p => p.title.includes(filter) || p.content.includes(filter))
       .forEach(p => {
    const div = document.createElement("div");
    div.className = "border p-4 w-96 flex-shrink-0 bg-gray-50 rounded";
    div.innerHTML = `<h4 class="font-semibold">${p.title}</h4><p>${p.content}</p>`;
    list.appendChild(div);
  });
}

function renderProducts(filter="") {
  const list = document.getElementById("product-list");
  list.innerHTML = "";
  products.filter(p => p.name.includes(filter))
          .forEach(p => {
    const div = document.createElement("div");
    div.className = "border p-4 w-60 flex-shrink-0 bg-gray-50 rounded text-center";
    div.innerHTML = `<p class="font-semibold">${p.name}</p><p class="text-red-500 font-bold">${p.price}원</p>`;
    list.appendChild(div);
  });
}

// 게시글 추가
document.getElementById("post-submit").addEventListener("click", async ()=>{
  const title = document.getElementById("post-title").value.trim();
  const content = document.getElementById("post-content").value.trim();
  if (!title || !content) return alert("제목과 내용을 입력하세요.");
  posts.push({title, content});
  renderPosts();
  await saveData();
});

// 상품 추가
document.getElementById("add-product").addEventListener("click", async ()=>{
  const name = document.getElementById("product-name").value.trim();
  const price = document.getElementById("product-price").value.trim();
  if (!name || !price) return alert("상품명과 가격을 입력하세요.");
  products.push({name, price});
  renderProducts();
  await saveData();
});

// 관리자 로그인
document.getElementById("login-btn").addEventListener("click", ()=> modal.classList.remove("hidden"));
document.getElementById("login-cancel").addEventListener("click", ()=> modal.classList.add("hidden"));
document.getElementById("login-confirm").addEventListener("click", ()=>{
  const id = document.getElementById("admin-id").value;
  const pw = document.getElementById("admin-pw").value;
  if(id==="eonju23" && pw==="200301"){
    writeSection.classList.remove("hidden");
    productForm.classList.remove("hidden");
    modal.classList.add("hidden");
  } else {
    alert("로그인 실패");
  }
});

// 검색 기능
document.getElementById("search-input").addEventListener("input", e=>{
  const filter = e.target.value;
  renderPosts(filter);
  renderProducts(filter);
});

loadData();
</script>
</body>
</html>
