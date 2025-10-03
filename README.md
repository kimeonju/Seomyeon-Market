<html>
<head>
  <meta charset="UTF-8">
  <title>서면나눔5일장</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link href="https://unpkg.com/tailwindcss@^2/dist/tailwind.min.css" rel="stylesheet">
  <style>
    .search-item {min-width: 200px;}
    .scroll-x {display:flex; overflow-x:auto; gap:1rem; padding-bottom:0.5rem;}
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
      <nav class="space-x-4 text-sm flex items-center">
        <a href="#schedule" class="hover:underline">장터 일정</a>
        <a href="#donation" class="hover:underline">기부금 사용내역</a>
        <a href="#posts" class="hover:underline">게시글</a>
        <a href="#products" class="hover:underline">상품</a>
      </nav>
    </div>
  </div>
</header>

<!-- Sections Wrapper -->
<div id="sections">

  <!-- Products -->
  <section id="products" class="bg-white py-10">
    <div class="max-w-6xl mx-auto px-4">
      <h3 class="text-2xl font-bold mb-4">상품</h3>
      <div id="product-list" class="scroll-x">
        <div class="border p-4 w-48 flex-shrink-0 search-item text-center bg-gray-50 rounded relative">
          <p class="font-semibold">녹차</p>
          <p class="text-red-500 font-bold">0원</p>
        </div>
      </div>
    </div>
  </section>

  <!-- Posts -->
  <section id="posts" class="bg-white py-10">
    <div class="max-w-6xl mx-auto px-4">
      <h3 class="text-2xl font-bold mb-4">게시글</h3>
      <div id="post-list" class="scroll-x">
        <!-- 기존 게시글 내용 표시 -->
      </div>
    </div>
  </section>

  <!-- Schedule -->
  <section id="schedule" class="bg-white py-8">
    <div class="max-w-6xl mx-auto px-4">
      <h3 class="text-2xl font-bold mb-4">장터 일정</h3>
      <div class="overflow-auto bg-gray-50 p-4 rounded">
        <table class="min-w-full text-sm text-left">
          <thead>
            <tr><th class="p-2">날짜</th><th class="p-2">판매 품목</th></tr>
          </thead>
          <tbody>
            <tr class="border-t"><td class="p-2">매달 4일, 9일</td><td class="p-2">녹차</td></tr>
            <tr class="border-t"><td class="p-2">매달 14일, 19일</td><td class="p-2">녹차</td></tr>
            <tr class="border-t"><td class="p-2">매달 24일, 29일</td><td class="p-2">녹차</td></tr>
          </tbody>
        </table>
      </div>
    </div>
  </section>

  <!-- Donation -->
  <section id="donation" class="bg-white py-10">
    <div class="max-w-6xl mx-auto px-4">
      <h3 class="text-2xl font-bold mb-4">기부금 사용내역</h3>
      <div class="overflow-auto bg-gray-50 p-4 rounded">
        <table class="min-w-full text-sm text-left">
          <thead>
            <tr><th class="p-2">날짜</th><th class="p-2">항목</th><th class="p-2">금액</th><th class="p-2">비고</th></tr>
          </thead>
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

// 검색 기능: 입력 시 상품/게시글 우선 표시
const searchInput = document.getElementById('search-input');
const sections = document.getElementById('sections');

function reorderSections(searching=false){
  sections.innerHTML = "";
  if(searching){
    ['products','posts','schedule','donation'].forEach(id=> sections.appendChild(document.getElementById(id)));
  } else {
    ['schedule','donation','posts','products'].forEach(id=> sections.appendChild(document.getElementById(id)));
  }
}

searchInput.addEventListener('input', ()=>{
  const val = searchInput.value.trim();
  reorderSections(val!=="");
});
</script>

</body>
</html>
