<html>
<head>
  <meta charset="UTF-8">
  <title>서면나눔5일장</title>
  <meta name="description" content="양양군 서면의 장터, 서면나눔5일장 농산물 직거래 페이지입니다.">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link href="https://unpkg.com/tailwindcss@^2/dist/tailwind.min.css" rel="stylesheet">
  <style>
    .hero-bg{background:linear-gradient(180deg, rgba(255,99,71,0.08), rgba(255,160,122,0.02));}
    .scroll-container{display:flex;overflow-x:auto;scroll-behavior:smooth;}
    .search-item{min-width:300px;margin-right:12px;flex-shrink:0;}
    table {border-collapse: collapse;}
    th, td {border: 1px solid #ccc; padding: 8px;}
  </style>
</head>
<body class="font-sans text-gray-800 bg-gray-50">

  <!-- Header + Search + Menu -->
  <header class="bg-white shadow-sm">
    <div class="max-w-6xl mx-auto px-4 py-4 flex flex-col md:flex-row justify-between items-center space-y-2 md:space-y-0">
      <div class="flex items-center space-x-3">
        <div class="w-12 h-12 bg-red-500 rounded-md flex items-center justify-center text-white font-bold">5일</div>
        <div>
          <h1 class="text-lg font-semibold">서면나눔5일장</h1>
          <p class="text-xs text-gray-500">양양군 서면 구룡령로 1906-89</p>
        </div>
      </div>
      <input id="search-input" type="text" placeholder="검색..." class="px-3 py-1 border rounded w-full md:w-64">
      <nav class="space-x-4 text-sm mt-2 md:mt-0">
        <a href="#schedule" class="hover:underline">장터 일정</a>
        <a href="#donation" class="hover:underline">기부금 사용내역</a>
        <a href="#posts-section" class="hover:underline">게시글</a>
        <a href="#hero-section" class="hover:underline">상품</a>
        <a href="#contact" class="hover:underline">문의</a>
      </nav>
    </div>
  </header>

  <!-- Hero / Product Section -->
  <section id="hero-section" class="hero-bg py-12">
    <div class="max-w-6xl mx-auto px-4">
      <h2 class="text-3xl font-extrabold mb-6 text-center">맛있는 고추를 저희 장터에서 사세요!🌶</h2>
      <div class="scroll-container" id="product-container">
        <div class="bg-white rounded-lg shadow-inner p-4 text-center search-item">
          <img src="홍고추.jpg" alt="홍고추 상품 이미지" class="mx-auto w-48 h-auto mb-2 rounded">
          <p class="font-semibold">홍고추</p>
          <p class="text-red-500 font-bold">0원</p>
          <p class="text-sm text-gray-600">무료배송 (CJ ONE)</p>
        </div>
        <div class="bg-white rounded-lg shadow-inner p-4 text-center search-item">
          <img src="풋고추.jpg" alt="풋고추 상품 이미지" class="mx-auto w-48 h-auto mb-2 rounded">
          <p class="font-semibold">풋고추</p>
          <p class="text-red-500 font-bold">0원</p>
          <p class="text-sm text-gray-600">무료배송 (CJ ONE)</p>
        </div>
      </div>
    </div>
  </section>

  <!-- Posts Section -->
  <section id="posts-section" class="bg-white py-10">
    <div class="max-w-6xl mx-auto px-4">
      <div class="flex justify-between items-center mb-4">
        <h3 class="text-2xl font-bold">게시글</h3>
        <button id="login-btn" class="px-3 py-1 bg-blue-600 text-white rounded">관리자 로그인</button>
      </div>
      <div id="write-post-section" class="mb-4 hidden">
        <input type="text" id="post-title" placeholder="제목" class="border p-2 w-full mb-2 rounded">
        <textarea id="post-content" placeholder="내용" class="border p-2 w-full mb-2 rounded"></textarea>
        <button id="submit-post" class="px-3 py-1 bg-green-600 text-white rounded">게시</button>
      </div>
      <div class="scroll-container" id="posts-container">
        <div class="border-b py-2 px-4 w-96 flex-shrink-0 search-item">
          <h4 class="font-semibold">2025년 9월 20일 장터 준비 안내</h4>
          <p>이번 주 장터는 홍고추와 풋고추를 중심으로 진행됩니다.</p>
        </div>
        <div class="border-b py-2 px-4 w-96 flex-shrink-0 search-item">
          <h4 class="font-semibold">2025년 9월 15일 장터 후기</h4>
          <p>지난 장터에서는 다양한 생고추가 판매되었습니다.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- Schedule Section -->
  <section id="schedule" class="bg-white py-8">
    <div class="max-w-6xl mx-auto px-4">
      <h3 class="text-2xl font-bold mb-4">장터 일정</h3>
      <p class="text-gray-600 mb-4">본 장터는 5일 간격으로 운영됩니다.</p>
      <div class="overflow-auto scroll-container bg-gray-50 p-4 rounded">
        <table class="min-w-full text-sm text-left border">
          <thead class="bg-gray-100">
            <tr>
              <th class="p-2">날짜</th>
              <th class="p-2">판매 품목</th>
            </tr>
          </thead>
          <tbody id="schedule-body">
            <tr>
              <td class="p-2">매달 4일, 9일</td>
              <td class="p-2">홍고추, 풋고추</td>
            </tr>
            <tr>
              <td class="p-2">매달 14일, 19일</td>
              <td class="p-2">홍고추, 풋고추</td>
            </tr>
            <tr>
              <td class="p-2">매달 24일, 29일</td>
              <td class="p-2">홍고추, 풋고추</td>
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
      <div class="overflow-auto scroll-container bg-gray-50 p-4 rounded">
        <table class="min-w-full text-sm text-left border">
          <thead class="bg-gray-100">
            <tr>
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

  <!-- Contact Section -->
  <section id="contact" class="max-w-6xl mx-auto px-4 py-10 text-center">
    <h3 class="text-2xl font-bold mb-3">문의하기</h3>
    <p class="mb-4 text-gray-600">문의나 요청 사항이 있으시면 설문조사 폼 작성 또는 전화 문의해주세요.</p>
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

  <!-- Scripts -->
  <script>
    // 관리자 로그인
    const loginBtn = document.getElementById('login-btn');
    const writeSection = document.getElementById('write-post-section');
    loginBtn.addEventListener('click', ()=>{
      const id = prompt("관리자 ID를 입력하세요:");
      const pw = prompt("비밀번호를 입력하세요:");
      if(id==='eonju23' && pw==='200301'){
        alert("관리자 로그인 성공");
        writeSection.classList.remove('hidden');
      } else {
        alert("로그인 실패");
      }
    });

    // 게시글 작성
    const submitPostBtn = document.getElementById('submit-post');
    submitPostBtn.addEventListener('click', ()=>{
      const title = document.getElementById('post-title').value;
      const content = document.getElementById('post-content').value;
      if(title && content){
        const postDiv = document.createElement('div');
        postDiv.className = "border-b py-2 px-4 w-96 flex-shrink-0 search-item";
        postDiv.innerHTML = `<h4 class="font-semibold">${title}</h4><p>${content}</p>`;
        document.getElementById('posts-container').prepend(postDiv);
        document.getElementById('post-title').value='';
        document.getElementById('post-content').value='';
      }
    });

    // 구글 시트 API 불러오기
    async function loadDonations() {
      const sheetId = "1BonKPabCsJpnpmatmyoabENRZjgxpOmN7q73cgQdFD8";
      const sheetName = "Sheet1";
      const url = `https://opensheet.elk.sh/${sheetId}/${sheetName}`;
      try{
        const res = await fetch(url);
        const data = await res.json();
        const tbody = document.getElementById("donation-body");
        tbody.innerHTML = "";
        data.forEach(row=>{
          const tr = document.createElement('tr');
          tr.innerHTML = `<td class="p-2 border">${row.날짜||''}</td><td class="p-2 border">${row.항목||''}</td><td class="p-2 border">${row.금액||''}</td><td class="p-2 border">${row.비고||''}</td>`;
          tbody.appendChild(tr);
        });
      }catch(err){console.error(err);}
    }
    loadDonations();

    // 검색
    const searchInput = document.getElementById('search-input');
    searchInput.addEventListener('input', function(){
      const q = this.value.toLowerCase();
      // 상품
      document.querySelectorAll('#product-container .search-item').forEach(item=>{
        item.style.display = item.textContent.toLowerCase().includes(q)?'block':'none';
      });
      // 게시글
      document.querySelectorAll('#posts-container .search-item').forEach(item=>{
        item.style.display = item.textContent.toLowerCase().includes(q)?'block':'none';
      });
    });
  </script>

</body>
</html>
