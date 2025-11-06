<html>
<head>
<meta charset="UTF-8">
<title>서면나눔5일장</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<link href="https://unpkg.com/tailwindcss@^2/dist/tailwind.min.css" rel="stylesheet">
<style>
.hero-bg {background: linear-gradient(180deg, rgba(255,99,71,0.08), rgba(255,160,122,0.02));}
.search-item {min-width: 300px; display: flex; flex-direction: column; justify-content: center;}
.scroll-container {display:flex; overflow-x:auto; gap:1rem;}
</style>
</head>
<body class="font-sans text-gray-800 bg-gray-50">

<!-- Header -->
<header class="bg-white shadow-sm">
  <div class="max-w-6xl mx-auto px-4 py-4 flex items-center justify-between">
    <div class="flex items-center space-x-3">
      <div class="w-12 h-12 bg-green-500 rounded-md flex items-center justify-center text-white font-bold">5일</div>
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
      </nav>
    </div>
  </div>
</header>

<!-- Hero -->
<section class="hero-bg py-12">
  <div class="max-w-6xl mx-auto px-4 grid md:grid-cols-2 gap-6 items-center">
    <div>
      <h2 class="text-3xl font-extrabold mb-2">맛있는 녹차를 저희 장터에서 사세요!🍵</h2>
      <div class="flex space-x-3">
        <a href="#schedule" class="px-4 py-2 bg-green-500 text-white rounded shadow-sm">장터 일정 보기</a>
        <a href="https://forms.gle/h7DNUtKJ9b5EeR3CA" target="_blank" class="px-4 py-2 border border-gray-300 rounded hover:bg-gray-100">문의 작성하기</a>
        <a href="tel:01026946608" class="px-4 py-2 border border-gray-300 rounded hover:bg-gray-100">전화 문의</a>
      </div>
    </div>
    <div class="bg-white rounded-lg shadow-inner p-4 text-center">
      <p class="font-semibold">녹차</p>
      <p class="text-red-500 font-bold mt-1">0원</p>
    </div>
  </div>
</section>

<div id="sections">

  <!-- 상품 -->
  <section id="products" class="bg-white py-10">
    <div class="max-w-6xl mx-auto px-4">
      <h3 class="text-2xl font-bold mb-4">상품</h3>
      <div id="product-list" class="scroll-container">
        <div class="border p-4 w-60 flex-shrink-0 search-item text-center bg-gray-50 rounded relative">
          <p class="font-semibold">녹차</p>
          <p class="text-red-500 font-bold mt-1">0원</p>
        </div>
        <div class="border p-4 w-60 flex-shrink-0 search-item text-center bg-gray-50 rounded relative">
          <p class="font-semibold">표고버섯(1kg)</p>
          <p class="text-red-500 font-bold mt-1">3,000원</p>
        </div>
      </div>
    </div>
  </section>

  <!-- 게시글 -->
  <section id="posts" class="bg-white py-10">
    <div class="max-w-6xl mx-auto px-4">
      <h3 class="text-2xl font-bold mb-4">게시글</h3>
      <div id="post-list" class="scroll-container">
        <div class="border p-4 w-96 flex-shrink-0 search-item bg-gray-50 rounded relative">
          <h4 class="font-semibold">환영 인사</h4>
          <p>서면나눔5일장 홈페이지에 오신 것을 환영합니다! 🍵</p>
        </div>
      </div>
    </div>
  </section>

  <!-- 문의 -->
  <section id="inquiry" class="bg-white py-10">
    <div class="max-w-6xl mx-auto px-4">
      <h3 class="text-2xl font-bold mb-4">문의</h3>
      <p class="mb-3">궁금한 점이나 요청사항이 있으면 아래 링크를 통해 문의해 주세요.</p>
      <a href="https://forms.gle/h7DNUtKJ9b5EeR3CA" target="_blank"
         class="px-4 py-2 bg-green-500 text-white rounded shadow-sm">문의 작성하기</a>
      <a href="tel:01026946608"
         class="ml-2 px-4 py-2 border border-gray-300 rounded hover:bg-gray-100">전화 문의</a>
    </div>
  </section>

  <!-- 장터 일정 -->
  <section id="schedule" class="bg-white py-8">
    <div class="max-w-6xl mx-auto px-4">
      <h3 class="text-2xl font-bold mb-4">장터 일정</h3>
      <div class="overflow-auto bg-gray-50 p-4 rounded">
        <table class="min-w-full text-sm text-left">
          <thead><tr><th class="p-2">날짜</th><th class="p-2">판매 품목</th></tr></thead>
          <tbody>
            <tr class="border-t"><td class="p-2">매달 4일, 9일</td><td class="p-2">녹차</td></tr>
            <tr class="border-t"><td class="p-2">매달 14일, 19일</td><td class="p-2">녹차</td></tr>
            <tr class="border-t"><td class="p-2">매달 24일, 29일</td><td class="p-2">녹차</td></tr>
          </tbody>
        </table>
      </div>
    </div>
  </section>

  <!-- 기부금 사용내역 -->
  <section id="donation" class="bg-white py-10">
    <div class="max-w-6xl mx-auto px-4">
      <h3 class="text-2xl font-bold mb-4">기부금 사용내역</h3>
      <div class="overflow-auto bg-gray-50 p-4 rounded">
        <table class="min-w-full text-sm text-left">
          <thead>
            <tr>
              <th class="p-2">날짜</th>
              <th class="p-2">항목</th>
              <th class="p-2">금액</th>
              <th class="p-2">비고</th>
            </tr>
          </thead>
          <tbody>
          </tbody>
        </table>
      </div>
    </div>
  </section>

</div>

<div id="no-results" class="hidden text-center text-gray-500 py-6">검색 결과가 없습니다.</div>

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
const searchInput = document.getElementById('search-input');
const sections = document.getElementById('sections');
const productList = document.getElementById('product-list');
const postList = document.getElementById('post-list');
const noResults = document.getElementById('no-results');

searchInput.addEventListener('input', ()=>{
  const query = searchInput.value.trim().toLowerCase();
  const productItems = Array.from(productList.children);
  const postItems = Array.from(postList.children);

  sections.appendChild(document.getElementById('products'));
  sections.appendChild(document.getElementById('posts'));
  sections.appendChild(document.getElementById('inquiry'));
  sections.appendChild(document.getElementById('schedule'));
  sections.appendChild(document.getElementById('donation'));

  let productVisible = false;
  let postVisible = false;

  productItems.forEach(div=>{
    if(query === "" || div.textContent.toLowerCase().includes(query)) {
      div.style.display = 'block';
      productVisible = true;
    } else div.style.display = 'none';
  });

  postItems.forEach(div=>{
    if(query === "" || div.textContent.toLowerCase().includes(query)) {
      div.style.display = 'block';
      postVisible = true;
    } else div.style.display = 'none';
  });

  if(query!=="" && !productVisible && !postVisible) noResults.classList.remove('hidden');
  else noResults.classList.add('hidden');
});
</script>

</body>
</html>
