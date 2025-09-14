<html>
<head>
  <meta charset="UTF-8">
  <title>서면나눔5일장</title>
  <meta name="description" content="양양군 서면의 장터, 서면나눔5일장 농산물 직거래 페이지입니다.">
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
    <div class="flex items-center space-x-4">
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

<!-- Hero Section -->
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

<!-- Schedule Section (항상 보임) -->
<section id="schedule" class="bg-white py-8">
  <div class="max-w-6xl mx-auto px-4">
    <h3 class="text-2xl font-bold mb-4">장터 일정</h3>
    <p class="text-gray-600 mb-4">본 장터는 5일 간격으로 운영됩니다.</p>
    <div class="overflow-auto bg-gray-50 p-4 rounded">
      <table class="min-w-full text-sm text-left">
        <thead>
          <tr class="text-gray-600">
            <th class="p-2">날짜</th>
            <th class="p-2">판매 품목</th>
          </tr>
        </thead>
        <tbody>
          <tr class="border-t">
            <td class="p-2">매달 4일, 9일</td>
            <td class="p-2">생고추, 건고추, 풋고추</td>
          </tr>
          <tr class="border-t bg-white">
            <td class="p-2">매달 14일, 19일</td>
            <td class="p-2">생고추, 건고추, 풋고추</td>
          </tr>
          <tr class="border-t bg-white">
            <td class="p-2">매달 24일, 29일</td>
            <td class="p-2">생고추, 건고추, 풋고추</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</section>

<!-- Donation Section -->
<section id="donation" class="bg-white py-10">
  <div class="max-w-6xl mx-auto px-4">
    <h3 class="text-2xl font-bold mb-4">기부금 사용내역</h3>
    <p class="text-gray-600 mb-4">서면나눔5일장은 기부금을 투명하게 운영하며, 매달 사용 내역을 공개합니다.</p>
    <div class="overflow-auto bg-gray-50 p-4 rounded">
      <table class="min-w-full text-sm text-left">
        <thead>
          <tr class="text-gray-600">
            <th class="p-2">날짜</th>
            <th class="p-2">항목</th>
            <th class="p-2">금액</th>
            <th class="p-2">비고</th>
          </tr>
        </thead>
        <tbody id="donation-body"></tbody>
      </table>
    </div>
    <p class="mt-4 text-sm text-gray-500">※ 개인 비용으로 구매한 농산물은 투자 비율만큼 가져간 후 일부 기부, 일부 소유합니다.</p>
  </div>
</section>

<!-- Posts Section -->
<section id="posts" class="bg-white py-10">
  <div class="max-w-6xl mx-auto px-4">
    <h3 class="text-2xl font-bold mb-4">게시글</h3>
    <div id="write-section" class="mb-6 hidden">
      <input id="post-title" type="text" placeholder="제목" class="border p-2 w-full mb-2 rounded">
      <textarea id="post-content" placeholder="내용" class="border p-2 w-full mb-2 rounded"></textarea>
      <button id="post-submit" class="px-4 py-2 bg-green-600 text-white rounded">게시</button>
    </div>
    <div id="post-list" class="flex overflow-x-auto space-x-4">
      <div class="border-b py-2 px-4 w-96 flex-shrink-0 search-item">
        <h4 class="font-semibold">2025년 9월 20일 장터 준비 안내</h4>
        <p>이번 주 장터는 홍고추와 풋고추를 중심으로 진행됩니다.</p>
      </div>
    </div>
  </div>
</section>

<!-- Products Section -->
<section id="products" class="bg-white py-10">
  <div class="max-w-6xl mx-auto px-4">
    <h3 class="text-2xl font-bold mb-4">상품</h3>
    <div id="product-list" class="flex overflow-x-auto space-x-4">
      <div class="border p-4 w-60 flex-shrink-0 search-item text-center">
        <img src="홍고추.jpg" class="mx-auto w-32 h-auto mb-2 rounded">
        <p class="font-semibold">홍고추</p>
        <p class="text-red-500 font-bold">0원</p>
      </div>
      <div class="border p-4 w-60 flex-shrink-0 search-item text-center">
        <img src="풋고추.jpg" class="mx-auto w-32 h-auto mb-2 rounded">
        <p class="font-semibold">풋고추</p>
        <p class="text-red-500 font-bold">0원</p>
      </div>
    </div>
    <p class="mt-4 text-sm text-gray-500">※ 고추 1kg 기준: 100g당 300원, 건고추 가격은 별도 문의.</p>
  </div>
</section>

<!-- Footer -->
<footer class="bg-gray-800 text-gray-200 py-6 mt-8">
  <div class="max-w-6xl mx-auto px-4 text-sm flex flex-col md:flex-row justify-between">
    <div>
      <p class="font-semibold">서면나눔5일장</p>
      <p class="text-xs">주소: 양양군 서면 구룡령로 1906-89</p>
      <p class="text-xs mt-2">※ 고추 1kg 기준: 100g당 300원, 건고추 가격은 별도 문의.</p>
    </div>
    <div class="text-xs text-gray-400">
      <p>© 2025 서면나눔5일장. All rights reserved.</p>
    </div>
  </div>
</footer>

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

<!-- JS -->
<script>
// 구글 시트 기부금 불러오기
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
  } catch(err) { console.error("기부금 데이터 로드 실패:", err); }
}
loadDonations();

// 검색 기능 (장터 일정은 항상 보임)
const searchInput = document.getElementById('search-input');
searchInput.addEventListener('input', function() {
  const query = this.value.toLowerCase();
  document.querySelectorAll('.search-item').forEach(item => {
    const text = item.innerText.toLowerCase();
    item.style.display = text.includes(query) ? 'block' : 'none';
  });
});

// 관리자 로그인
const loginBtn = document.getElementById('login-btn');
const writeSection = document.getElementById('write-section');
loginBtn.addEventListener('click', () => document.getElementById('login-modal').classList.remove('hidden'));
document.getElementById('login-cancel').addEventListener('click', () => document.getElementById('login-modal').classList.add('hidden'));
document.getElementById('login-confirm').addEventListener('click', () => {
  const id = document.getElementById('admin-id').value;
  const pw = document.getElementById('admin-pw').value;
  if(id==='eonju23' && pw==='200301'){
    alert("관리자 로그인 성공");
    writeSection.classList.remove('hidden');
    document.getElementById('login-modal').classList.add('hidden');
  } else alert("로그인 실패");
});

// 게시글 작성
document.getElementById('post-submit').addEventListener('click', () => {
  const title = document.getElementById('post-title').value.trim();
  const content = document.getElementById('post-content').value.trim();
  if(title && content){
    const div = document.createElement('div');
    div.className = 'border-b py-2 px-4 w-96 flex-shrink-0 search-item';
    div.innerHTML = `<h4 class="font-semibold">${title}</h4><p>${content}</p>`;
    document.getElementById('post-list').appendChild(div);
    document.getElementById('post-title').value = '';
    document.getElementById('post-content').value = '';
  } else alert("제목과 내용을 입력하세요");
});
</script>

</body>
</html>
