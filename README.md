<html>
<head>
  <title>서면나눔5일장</title>
  <meta name="description" content="양양군 서면의 장터, 서면나눔5일장 농산물 직거래 페이지입니다." />
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link href="https://unpkg.com/tailwindcss@^2/dist/tailwind.min.css" rel="stylesheet">
  <style>
    .hero-bg {background: linear-gradient(180deg, rgba(255,99,71,0.08), rgba(255,160,122,0.02));}
    .search-container {position: absolute; top: 1rem; right: 1rem;}
  </style>
</head>
<body class="font-sans text-gray-800 bg-gray-50">

<!-- Header -->
<header class="bg-white shadow-sm relative">
  <div class="max-w-6xl mx-auto px-4 py-4 flex flex-col md:flex-row items-center justify-between">
    <div class="flex items-center space-x-3 mb-2 md:mb-0">
      <div class="w-12 h-12 bg-red-500 rounded-md flex items-center justify-center text-white font-bold">5일</div>
      <div>
        <h1 class="text-lg font-semibold">서면나눔5일장</h1>
        <p class="text-xs text-gray-500">양양군 서면 구룡령로 1906-89</p>
      </div>
    </div>
    <nav class="space-x-4 text-sm mb-2 md:mb-0">
      <a href="#schedule" class="hover:underline">장터 일정</a>
      <a href="#donation" class="hover:underline">기부금 사용내역</a>
      <a href="#products" class="hover:underline">상품</a>
      <a href="#posts" class="hover:underline">게시글</a>
      <a href="#contact" class="hover:underline">문의</a>
    </nav>
    <div class="search-container">
      <input id="global-search" type="text" placeholder="사이트 전체 검색..." class="border p-1 rounded w-64"/>
    </div>
  </div>
</header>

<!-- Hero Section -->
<section class="hero-bg py-12 search-item">
  <div class="max-w-6xl mx-auto px-4 grid md:grid-cols-2 gap-6 items-center">
    <div>
      <h2 class="text-3xl font-extrabold mb-2">맛있는 고추를 저희 장터에서 사세요!🌶</h2>
      <div class="flex space-x-3">
        <a href="#schedule" class="px-4 py-2 bg-red-500 text-white rounded shadow-sm">장터 일정 보기</a>
        <a href="https://forms.gle/h7DNUtKJ9b5EeR3CA" target="_blank"
           class="px-4 py-2 border border-gray-300 rounded hover:bg-gray-100">문의 작성하기</a>
        <a href="tel:01026946608"
           class="px-4 py-2 border border-gray-300 rounded hover:bg-gray-100">전화 문의</a>
      </div>
