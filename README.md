<html>
<head>
  <meta charset="UTF-8">
  <title>서면나눔5일장</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link href="https://unpkg.com/tailwindcss@^2/dist/tailwind.min.css" rel="stylesheet">
  <style>
    .hero-bg {background: linear-gradient(180deg, rgba(255,99,71,0.08), rgba(255,160,122,0.02));}
    .search-item {min-width: 300px;}
  </style>
</head>
<body class="font-sans text-gray-800 bg-gray-50">

<!-- Header -->
<header class="bg-white shadow-sm">
  <div class="max-w-6xl mx-auto px-4 py-4 flex items-center justify-between">
    <div class="flex items-center space-x-3">
      <div class="w-12 h-12 bg-red-500 rounded-md flex items-center justify-center text-white font-bold">5일</div>
      <div>
        <h1 class="text-lg font-semibold">서면나눔5일장</h1>
        <p class="text-xs text-gray-500">양양군 서면 구룡령로 1906-89</p>
      </div>
    </div>
    <div class="flex items-center space-x-2">
      <input id="search-input" type="text" placeholder="검색..." class="border p-2 rounded w-64">
      <nav class="space-x-4 text-sm">
        <a href="#schedule" class="hover:underline">장터 일정</a>
        <a href="#donation" class="hover:underline">기부금 사용내역</a>
        <a href="#posts" class="hover:underline">게시글</a>
        <a href="#products" class="hover:underline">상품</a>
        <button id="login-btn" class="px-2 py-1 bg-blue-600 text-white rounded">관리자 로그인</button>
      </nav>
    </div>
  </div>
</header>

<!-- Hero -->
<section class="hero-bg py-12">
  <div class="max-w-6xl mx-auto px-4 grid md:grid-cols-2 gap-6 items-center">
    <div>
      <h2 class="text-3xl font-extrabold mb-2">맛있는 고추를 저희 장터에서 사세요!🌶</h2>
      <div class="flex space-x-3">
        <a href="#schedule" class="px-4 py-2 bg-red-500 text-white rounded shadow-sm">장터 일정 보기</a>
        <a href="https://forms.gle/h7DNUtKJ9b5EeR3CA" target="_blank" class="px-4 py-2 border border-gray-300 rounded hover:bg-gray-100">문의 작성하기</a>
        <a href="tel:01026946608" class="px-4 py-2 border border-gray-300 rounded hover:bg-gray-100">전화 문의</a>
      </div>
    </div>
    <div class="bg-white rounded-lg shadow-inner p-4 text-center">
      <img src="홍고추.jpg" alt="홍고추 상품 이미지" class="mx-auto w-48 h-auto mb-2 rounded">
      <p class="font-semibold">홍고추</p>
      <p class="text-red-500 font-bold">0원</p>
      <p class="text-sm text-gray-600">무료배송 (CJ ONE)</p>
    </div>
  </div>
</section>

<!-- Sections Wrapper -->
<div id="sections">

  <!-- Products -->
  <section id="products" class="bg-white py-10">
    <div class="max-w-6xl mx-auto px-4">
      <h3 class="text-2xl font-bold mb-4">상품</h3>
      <div id="product-form" class="hidden mb-6">
        <input id="product-name" type="text" placeholder="상품명" class="border p-2 w-full mb-2 rounded">
        <input id="product-price" type="text" placeholder="가격" class="border p-2 w-full mb-2 rounded">
        <input id="product-img" type="file" accept="image/*" class="mb-2">
        <button id="add-product" class="px-4 py-2 bg-green-600 text-white rounded">상품 추가</button>
      </div>
      <div id="product-list" class="flex overflow-x-auto space-x-4"></div>
      <p class="mt-4 text-sm text-gray-500">※ 고추 1kg 기준: 100g당 300원, 건고추 가격은 별도 문의.</p>
    </div>
  </section>

  <!-- Posts -->
  <section id="posts" class="bg-white py-10">
    <div class="max-w-6xl mx-auto px-4">
      <h3 class="text-2xl font-bold mb-4">게시글</h3>
      <div id="write-section" class="hidden mb-6">
        <input id="post-title" type="text" placeholder="제목" class="border p-2 w-full mb-2 rounded">
        <textarea id="post-content" placeholder="내용" class="border p-2 w-full mb-2 rounded"></textarea>
        <input id="post-media" type="file" accept="image/*,video/*" class="mb-2">
        <button id="post-submit" class="px-4 py-2 bg-green-600 text-white rounded">게시</button>
      </div>
      <div id="post-list" class="flex overflow-x-auto space-x-4"></div>
    </div>
  </section>

  <!-- Schedule -->
  <section id="schedule" class="bg-white py-8">
    <div class="max-w-6xl mx-auto px-4">
      <h3 class="text-2xl font-bold mb-4">장터 일정</h3>
      <div class="overflow-auto bg-gray-50 p-4 rounded">
        <table class="min-w-full text-sm text-left">
          <thead><tr><th class="p-2">날짜</th><th class="p-2">판매 품목</th></tr></thead>
          <tbody>
            <tr class="border-t"><td class="p-2">매달 4일, 9일</td><td class="p-2">생고추, 건고추, 풋고추</td></tr>
            <tr class="border-t"><td class="p-2">매달 14일, 19일</td><td class="p-2">생고추, 건고추, 풋고추</td></tr>
            <tr class="border-t"><td class="p-2">매달 24일, 29일</td><td class="p-2">생고추, 건고추, 풋고추</td></tr>
          </tbody>
        </table>
      </div>
    </div>
  </section>

  <!-- Inquiry -->
  <section id="inquiry" class="bg-white py-10">
    <div class="max-w-6xl mx-auto px-4">
      <h3 class="text-2xl font-bold mb-4">문의</h3>
      <p>문의사항은 <a href="https://forms.gle/h7DNUtKJ9b5EeR3CA" target="_blank" class="text-blue-600 underline">구글 폼</a>을 이용해주세요.</p>
    </div>
  </section>

  <!-- Donation -->
  <section id="donation" class="bg-white py-10">
    <div class="max-w-6xl mx-auto px-4">
      <h3 class="text-2xl font-bold mb-4">기부금 사용내역</h3>
      <div class="overflow-auto bg-gray-50 p-4 rounded">
        <table class="min-w-full text-sm text-left">
          <thead><tr><th class="p-2">날짜</th><th class="p-2">항목</th><th class="p-2">금액</th><th class="p-2">비고</th></tr></thead>
          <tbody id="donation-body"></tbody>
        </table>
      </div>
    </div>
  </section>

</div>

<!-- Footer -->
<footer class="bg-gray-800 text-gray-200 py-6 mt-8">
  <div class="max-w-6xl mx-auto px-4 text-sm flex flex-col md:flex-row justify-between">
    <div>
      <p class="font-semibold">서면나눔5일장</p>
      <p class="text-xs">주소: 양양군 서면 구룡령로 1906-89</p>
    </div>
    <div class="text-xs text-gray-400">
      <p>© 2025 서면나눔5일장. All rights reserved.</p>
    </div>
  </div>
</footer>

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
// 기부금 불러오기
async function loadDonations() {
  const sheetId = "1BonKPabCsJpnpmatmyoabENRZjgxpOmN7q73cgQdFD8";
  const sheetName = "Sheet1";
  const url = `https://opensheet.elk.sh/${sheetId}/${sheetName}`;
  try {
    const res = await fetch(url);
    const data = await res.json();
    const tbody = document.getElementById("donation-body");
    tbody.innerHTML = "";
    data.forEach(row => {
      const tr = document.createElement("tr");
      tr.innerHTML = `
        <td class="p-2 border-t">${row.날짜 || ""}</td>
        <td class="p-2 border-t">${row.항목 || ""}</td>
        <td class="p-2 border-t">${row.금액 || ""}</td>
        <td class="p-2 border-t">${row.비고 || ""}</td>
      `;
      tbody.appendChild(tr);
    });
  } catch(err) { console.error("기부금 로드 실패:", err); }
}
loadDonations();

// 관리자 로그인
const loginBtn = document.getElementById('login-btn');
const modal = document.getElementById('login-modal');
const writeSection = document.getElementById('write-section');
const productForm = document.getElementById('product-form');

loginBtn.addEventListener('click', ()=> modal.classList.remove('hidden'));
document.getElementById('login-cancel').addEventListener('click', ()=> modal.classList.add('hidden'));
document.getElementById('login-confirm').addEventListener('click', ()=> {
  const id = document.getElementById('admin-id').value;
  const pw = document.getElementById('admin-pw').value;
  if(id==='eonju23' && pw==='200301'){
    alert("관리자 로그인 성공");
    writeSection.classList.remove('hidden');
    productForm.classList.remove('hidden');
    modal.classList.add('hidden');
  } else alert("로그인 실패");
});

// 게시글 작성
document.getElementById('post-submit').addEventListener('click', ()=>{
  const title = document.getElementById('post-title').value.trim();
  const content = document.getElementById('post-content').value.trim();
  const media = document.getElementById('post-media').files[0];
  if(!title || !content){ alert("제목과 내용을 입력하세요"); return; }
  const div = document.createElement('div');
  div.className = 'border p-4 w-96 flex-shrink-0 search-item bg-gray-50 rounded relative';
  let mediaHTML = "";
  if(media){
    const url = URL.createObjectURL(media);
    if(media.type.startsWith("image")) mediaHTML = `<img src="${url}" class="mt-2 rounded">`;
    if(media.type.startsWith("video")) mediaHTML = `<video src="${url}" controls class="mt-2 rounded"></video>`;
  }
  div.innerHTML = `
    <h4 class="font-semibold">${title}</h4>
    <p>${content}</p>
    ${mediaHTML}
    <div class="mt-2 flex space-x-2">
      <button class="edit-post px-2 py-1 text-xs bg-yellow-500 text-white rounded">수정</button>
      <button class="delete-post px-2 py-1 text-xs bg-red-600 text-white rounded">삭제</button>
    </div>
  `;
  document.getElementById('post-list').appendChild(div);
  document.getElementById('post-title').value = "";
  document.getElementById('post-content').value = "";
  document.getElementById('post-media').value = "";
});

// 게시글 수정/삭제
document.getElementById('post-list').addEventListener('click', (e)=>{
  if(e.target.classList.contains('delete-post')) e.target.closest('div').remove();
  if(e.target.classList.contains('edit-post')){
    const box = e.target.closest('div');
    const title = prompt("제목 수정", box.querySelector('h4').innerText);
    const content = prompt("내용 수정", box.querySelector('p').innerText);
    if(title) box.querySelector('h4').innerText = title;
    if(content) box.querySelector('p').innerText = content;
  }
});

// 상품 추가
document.getElementById('add-product').addEventListener('click', ()=>{
  const name = document.getElementById('product-name').value.trim();
  const price = document.getElementById('product-price').value.trim();
  const img = document.getElementById('product-img').files[0];
  if(!name || !price || !img){ alert("상품명, 가격, 이미지를 입력하세요"); return; }
  const url = URL.createObjectURL(img);
  const div = document.createElement('div');
  div.className = 'border p-4 w-60 flex-shrink-0 search-item text-center bg-gray-50 rounded relative';
  div.innerHTML = `
    <img src="${url}" class="mx-auto w-32 h-auto mb-2 rounded">
    <p class="font-semibold">${name}</p>
    <p class="text-red-500 font-bold">${price}원</p>
    <button class="delete-product px-2 py-1 text-xs bg-red-600 text-white rounded mt-2">삭제</button>
  `;
  document.getElementById('product-list').appendChild(div);
  document.getElementById('product-name').value = "";
  document.getElementById('product-price').value = "";
  document.getElementById('product-img').value = "";
});

// 상품 삭제
document.getElementById('product-list').addEventListener('click', (e)=>{
  if(e.target.classList.contains('delete-product')) e.target.closest('div').remove();
});

// 검색 기능
const searchInput = document.getElementById('search-input');
const sections = document.getElementById('sections');

searchInput.addEventListener('input', ()=>{
  const term = searchInput.value.trim().toLowerCase();
  ['products','posts','schedule','inquiry','donation'].forEach(id=>{
    const sec = document.getElementById(id);
    sec.style.display = sec.innerText.toLowerCase().includes(term) ? 'block' : 'none';
  });
});
</script>

</body>
</html>
