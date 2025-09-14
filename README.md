<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <title>서면나눔5일장</title>
  <meta name="description" content="양양군 서면의 장터, 서면나눔5일장 농산물 직거래 페이지입니다." />
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link href="https://unpkg.com/tailwindcss@^2/dist/tailwind.min.css" rel="stylesheet">
  <style>
    .hero-bg { background: linear-gradient(180deg, rgba(255,99,71,0.08), rgba(255,160,122,0.02)); }
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
      <nav class="space-x-4 text-sm">
        <a href="#schedule" class="hover:underline">장터 일정</a>
        <a href="#products" class="hover:underline">상품</a>
        <a href="#donation" class="hover:underline">기부금 사용내역</a>
        <a href="#contact" class="hover:underline">문의</a>
      </nav>
    </div>
  </header>

  <!-- Hero Section -->
  <section class="hero-bg py-12">
    <div class="max-w-6xl mx-auto px-4 grid md:grid-cols-2 gap-6 items-center">
      <div>
        <h2 class="text-3xl font-extrabold mb-2">맛있는 고추를 저희 장터에서 사세요!🌶</h2>
        <div class="flex space-x-3">
          <a href="#schedule" class="px-4 py-2 bg-red-500 text-white rounded shadow-sm">장터 일정 보기</a>
          <a href="#contact" class="px-4 py-2 border border-gray-300 rounded hover:bg-gray-100">문의 작성하기</a>
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

  <!-- Schedule Section -->
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
              <td class="p-2">생고추, 건고추</td>
            </tr>
            <tr class="border-t bg-white">
              <td class="p-2">매달 14일, 19일</td>
              <td class="p-2">생고추, 건고추</td>
            </tr>
            <tr class="border-t bg-white">
              <td class="p-2">매달 24일, 29일</td>
              <td class="p-2">생고추, 건고추</td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
  </section>

  <!-- Products Section -->
  <section id="products" class="max-w-6xl mx-auto px-4 py-10">
    <h3 class="text-2xl font-bold mb-6 text-center">상품 목록</h3>
    <div class="grid grid-cols-1 md:grid-cols-3 gap-6">

      <!-- 홍고추 -->
      <div class="bg-white rounded-lg shadow p-4 text-center">
        <img src="홍고추.jpg" alt="홍고추" class="mx-auto w-48 h-auto mb-2 rounded">
        <h3 class="font-semibold text-lg">홍고추</h3>
        <p class="text-red-500 font-bold">0원</p>
        <p class="text-sm text-gray-600 mb-2">무료배송 (CJ ONE)</p>
        <a href="tel:01026946608" class="px-4 py-2 bg-green-600 text-white rounded hover:bg-green-700 inline-block">구매 문의</a>
      </div>

      <!-- 풋고추 -->
      <div class="bg-white rounded-lg shadow p-4 text-center">
        <img src="풋고추.jpg" alt="풋고추" class="mx-auto w-48 h-auto mb-2 rounded">
        <h3 class="font-semibold text-lg">풋고추</h3>
        <p class="text-red-500 font-bold">0원</p>
        <p class="text-sm text-gray-600 mb-2">무료배송 (CJ ONE)</p>
        <a href="tel:01026946608" class="px-4 py-2 bg-green-600 text-white rounded hover:bg-green-700 inline-block">구매 문의</a>
      </div>

      <!-- 건고추 -->
      <div class="bg-white rounded-lg shadow p-4 text-center">
        <img src="건고추.jpg" alt="건고추" class="mx-auto w-48 h-auto mb-2 rounded">
        <h3 class="font-semibold text-lg">건고추</h3>
        <p class="text-red-500 font-bold">0원</p>
        <p class="text-sm text-gray-600 mb-2">무료배송 (CJ ONE)</p>
        <a href="tel:01026946608" class="px-4 py-2 bg-green-600 text-white rounded hover:bg-green-700 inline-block">구매 문의</a>
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
          <tbody id="donation-body">
            <!-- JS로 데이터 삽입 -->
          </tbody>
        </table>
      </div>
      <p class="mt-4 text-sm text-gray-500">※ 개인 비용으로 구매한 농산물은 투자 비율만큼 가져간 후 일부 기부, 일부 소유합니다.</p>
    </div>
  </section>

  <!-- Contact -->
  <section id="contact" class="max-w-6xl mx-auto px-4 py-10 text-center">
    <h3 class="text-2xl font-bold mb-3">문의하기</h3>
    <p class="mb-4 text-gray-600">문의나 요청 사항이 있으시면 아래 버튼을 눌러 설문조사 폼을 작성하거나 전화로 문의해주세요.</p>
    <div class="flex flex-col md:flex-row justify-center gap-4">
      <a href="https://forms.gle/h7DNUtKJ9b5EeR3CA" target="_blank" class="px-6 py-3 bg-blue-600 text-white rounded shadow hover:bg-blue-700 transition">설문조사 작성하기</a>
      <a href="tel:01026946608" class="px-6 py-3 bg-green-600 text-white rounded shadow hover:bg-green-700 transition">전화 문의: 010-2694-6608</a>
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

  <!-- JS: 구글 시트 API 불러오기 -->
  <script>
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
      } catch (err) {
        console.error("기부금 데이터 로드 실패:", err);
      }
    }
    loadDonations();
  </script>

</body>
</html>
