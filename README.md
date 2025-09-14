
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
