<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <title>서면나눔5일장 상품 목록</title>
  <meta name="description" content="서면나눔5일장의 다양한 농산물 상품 목록 페이지입니다.">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link href="https://unpkg.com/tailwindcss@^2/dist/tailwind.min.css" rel="stylesheet">
  <style>
    .hero-bg{background:linear-gradient(180deg, rgba(255,99,71,0.08), rgba(255,160,122,0.02));}
  </style>
</head>
<body class="bg-gray-50 font-sans text-gray-800">

  <!-- Header -->
  <header class="bg-white shadow-sm">
    <div class="max-w-6xl mx-auto px-4 py-4 flex items-center justify-between">
      <div class="flex items-center space-x-3">
        <h1 class="text-lg font-semibold">서면나눔5일장 상품 목록</h1>
      </div>
      <nav class="space-x-4 text-sm">
        <a href="index.html" class="hover:underline">홈</a>
        <a href="products.html" class="hover:underline font-bold">상품</a>
        <a href="#contact" class="hover:underline">문의</a>
      </nav>
    </div>
  </header>

  <!-- Hero Section -->
  <section class="hero-bg py-12">
    <div class="max-w-6xl mx-auto px-4 text-center">
      <h2 class="text-3xl font-extrabold mb-2">서면나눔5일장의 다양한 농산물을 만나보세요!</h2>
      <p class="text-gray-600 mb-4">신선하고 안전한 농산물을 직거래로 제공합니다.</p>
    </div>
  </section>

  <!-- Products Section -->
  <section class="max-w-6xl mx-auto px-4 py-10">
    <h2 class="text-3xl font-bold mb-6 text-center">상품 목록</h2>
    <div class="grid grid-cols-1 md:grid-cols-3 gap-6">

      <!-- 상품 1 -->
      <div class="bg-white rounded-lg shadow p-4 text-center">
        <img src="홍고추.jpg" alt="홍고추" class="mx-auto w-48 h-auto mb-2 rounded">
        <h3 class="font-semibold text-lg">홍고추</h3>
        <p class="text-red-500 font-bold">0원</p>
        <p class="text-sm text-gray-600 mb-2">무료배송 (CJ ONE)</p>
        <a href="tel:01026946608" class="px-4 py-2 bg-green-600 text-white rounded hover:bg-green-700 inline-block">구매 문의</a>
      </div>

      <!-- 상품 2 -->
      <div class="bg-white rounded-lg shadow p-4 text-center">
        <img src="풋고추.jpg" alt="풋고추" class="mx-auto w-48 h-auto mb-2 rounded">
        <h3 class="font-semibold text-lg">풋고추</h3>
        <p class="text-red-500 font-bold">0원</p>
        <p class="text-sm text-gray-600 mb-2">무료배송 (CJ ONE)</p>
        <a href="tel:01026946608" class="px-4 py-2 bg-green-600 text-white rounded hover:bg-green-700 inline-block">구매 문의</a>
      </div>

      <!-- 상품 3 -->
      <div class="bg-white rounded-lg shadow p-4 text-center">
        <img src="건고추.jpg" alt="건고추" class="mx-auto w-48 h-auto mb-2 rounded">
        <h3 class="font-semibold text-lg">건고추</h3>
        <p class="text-red-500 font-bold">0원</p>
        <p class="text-sm text-gray-600 mb-2">무료배송 (CJ ONE)</p>
        <a href="tel:01026946608" class="px-4 py-2 bg-green-600 text-white rounded hover:bg-green-700 inline-block">구매 문의</a>
      </div>

    </div>
  </section>

  <!-- Contact Section -->
  <section id="contact" class="max-w-6xl mx-auto px-4 py-10 text-center">
    <h3 class="text-2xl font-bold mb-3">문의하기</h3>
    <p class="mb-4 text-gray-600">문의나 요청 사항이 있으시면 아래 버튼을 눌러 설문조사 폼을 작성하거나 전화로 문의해주세요.</p>
    <div class="flex flex-col md:flex-row justify-center gap-4">
      <a href="https://forms.gle/h7DNUtKJ9b5EeR3CA" target="_blank"
         class="px-6 py-3 bg-blue-600 text-white rounded shadow hover:bg-blue-700 transition">
        설문조사 작성하기
      </a>
      <a href="tel:01026946608"
         class="px-6 py-3 bg-green-600 text-white rounded shadow hover:bg-green-700 transition">
        전화 문의: 010-2694-6608
      </a>
    </div>
  </section>

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

</body>
</html>
