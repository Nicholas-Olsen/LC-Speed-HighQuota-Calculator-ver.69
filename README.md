### Speed High Quota Sell Helper 
### Made my Nichol ### ver.68
<html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>High Quota Sell Calculator by Nichol</title>
    <style>

#DaysLeft {
    width: 12%;
    margin-right: 10px;
}

#MoonOrbitCost {
    width: 20%;
}

    @media screen and (max-width: 768px) {
   body {
        font-size: 60%; /* 모바일 폰트 크기 */
        background-color: #333333;
        color: #99ff99;
        font-family: Sans-serif;
        font-weight: bold;
    }

        
        fieldset {
            border: 5px solid #33ff33;
            padding: 5px;
            max-width: 650px;
            margin: 30px auto;
            border-radius: 10px;
        }
        
        h1 {
            font-size: 1.5em; /* 제목 폰트 크기 축소 */
            text-align: center;
            font-weight: bold;
        }
        
        .result {
            font-size: 1.5em;
            font-weight: bold;
            text-align: center;
            margin-top: 20px;
        }
        
        table {
            width: 100%;
            border-collapse: separate;
            margin-top: 10px;
            border-radius: 10px;
            overflow: hidden;
            table-layout: fixed; /* 변경된 부분: 테이블 레이아웃 고정 */
        }

        th, td {
            font-size: 0.9em; 
            padding: 5px;
            text-align: center;
            border: 1px solid #33ff33 !important; /* 중요도를 높임 */
            background-color: #333333;
            color: #99ff99;
        }

        th:first-child, td:first-child {
            width: 210px;
        }


        th:nth-child(3), td:nth-child(3) {
            width: 20%;
        }

        th:nth-child(4), td:nth-child(4) {
            width: 25%;
        }

        /* 모든 테이블에서 첫 번째 행 제외하고 1열에 적용 */
        table tr, td:first-child {
            font-size: 1.1em;
            font-weight: bold;
        }

        th {
            font-size: 1.3em;
            background-color: #66ff66;
            color: #333333;
        }

        /* 두 번째 테이블에 대한 스타일 */
        table:nth-of-type(2) th,
        table:nth-of-type(2) td {
            background-color: #66ff66;
            color: #333333;
        }

        /* 세 번째 테이블 너비 조정 */
        table:nth-of-type(3) {
            width: 100%; /* 가로폭을 100%로 설정 */
        }

        table:nth-of-type(3) th:first-child,
        table:nth-of-type(3) td:first-child {
            width: 50%; /* 첫 번째 열 50% */
        }

        table:nth-of-type(3) th:nth-child(2),
        table:nth-of-type(3) td:nth-child(2) {
            width: 50%; /* 두 번째 열 50% */
        }

        label {
           font-size: 0.8em;
        }

        input[type="checkbox"] {
            transform: scale(1.5);
            margin: 10px;
        }

        input[type="number"]t {
            font-family: sans-serif;
            font-size: 0.9em;
            background-color: #faffff;
            color: #333333;
            width: 65%;
            font-weight: bold;
            height: 30px;
        }

        input[type="number"]#RequiredQuota {
            width: 22%; 
            margin-right: 22px; 
            font-size: 30px; 
            height: 40px;
        }

        select {
            font-family: sans-serif;
            font-size: 16px;
            padding: 5px; 
            border: 1px solid #33ff33; 
            background-color: #333333;
            color: #ffffff; 
            width: 35%; 
            height: 40px; 
            font-weight: bold; 
            box-sizing: border-box; 
        }

        button {
            background-color: #66ff66;
            color: #1C1C1C;
            font-size: 1.2em;
            font-weight: bold;
            padding: 15px 30px;
            border: none;
            cursor: pointer;
            display: inline-block;
            margin: 25px 10px 30px 30px; 
            border-radius: 15px; 
        }

        #result {
            font-size: 2em; 
            font-weight: bold; 
            color: #ccffcc; 
            display: inline-block; 
            margin-left: 20px; 
        }
    </style>
</head>
<body>

<fieldset>
    <h1>High Quota Challenge <br> Sell & Purchase Calculator <br> 할당량 챌린지 상점 계산기</h1>

<div style="display: flex; align-items: center; margin-bottom: 10px;">
    <label for="RequiredQuota">&nbsp;할당량 :&nbsp;</label>
    <input type="number" id="RequiredQuota" step="10" value="130" min="130" required>
    <label for="DaysLeft">&nbsp;남은 마감일 :&nbsp;</label>
    <select id="DaysLeft" required>
        <option value="0">0일</option>
        <option value="1">1일</option>
        <option value="2">2일</option>
        <option value="3">3일</option>
    </select>
    <label for="MoonOrbitCost">다음 목적지 :&nbsp;</label>
    <select id="MoonOrbitCost" required>
        <option value="0">*무료 위성</option>
        <option value="150">엠브리온</option>
        <option value="550">렌드</option>
        <option value="600">다인</option>
        <option value="700">타이탄</option>
        <option value="1500">아터피스</option>
    </select>
</div>

    <table>
        <thead>
            <tr>
                <th>장비</th>
                <th>구매 여부</th>
                <th>개수</th>
                <th>할인가(선택)</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>철제 삽</td>
                <td><input type="checkbox" name="item1" value="30"></td>
                <td><input type="number" min="0" id="number1"></td>
                <td><input type="number" step="3" id="salePrice1" value="30" max="30"></td>
            </tr>
            <tr>
                <td>자물쇠 따개</td>
                <td><input type="checkbox" name="item2" value="20"></td>
                <td><input type="number" min="0" id="number2"></td>
                <td><input type="number" step="2" id="salePrice2" value="20" max="20"></td>
            </tr>
            <tr>
                <td>제초제</td>
                <td><input type="checkbox" name="item3" value="25"></td>
                <td><input type="number" min="0" id="number3"></td>
                <td><input type="number" step="2.5" id="salePrice3" value="25" max="25"></td>
            </tr>
            <tr>
                <td>제트팩</td>
                <td><input type="checkbox" name="item4" value="900"></td>
                <td><input type="number" min="0" id="number4"></td>
                <td><input type="number" step="90" id="salePrice4" value="900" max="900"></td>
            </tr>
            <tr>
                <td>페인트 스프레이</td>
                <td><input type="checkbox" name="item5" value="50"></td>
                <td><input type="number" min="0" id="number5"></td>
                <td><input type="number" step="5" id="salePrice5" value="50" max="50"></td>
            </tr>
            <tr>
                <td>벨트 배낭</td>
                <td><input type="checkbox" name="item6" value="45"></td>
                <td><input type="number" min="0" id="number6"></td>
                <td><input type="number" step="4.5" id="salePrice6" value="45" max="45"></td>
            </tr>
            <tr>
                <td>TZP-흡입제</td>
                <td><input type="checkbox" name="item7" value="80"></td>
                <td><input type="number" min="0" id="number7"></td>
                <td><input type="number" step="8" id="salePrice7"  value="80" max="80"></td>
            </tr>
            <tr>
                <td>프로 손전등</td>
                <td><input type="checkbox" name="item8" value="25"></td>
                <td><input type="number" min="0" id="number8"></td>
                <td><input type="number" step="2.5" id="salePrice8" value="25" max="25"></td>
            </tr>
            <tr>
                <td>기절 수류탄</td>
                <td><input type="checkbox" name="item9" value="30"></td>
                <td><input type="number" min="0" id="number9"></td>
                <td><input type="number" step="3" id="salePrice9" value="30" max="30"></td>
            </tr>
            <tr>
                <td>연장형 사다리</td>
                <td><input type="checkbox" name="item10" value="60"></td>
                <td><input type="number" min="0" id="number10"></td>
                <td><input type="number" step="6" id="salePrice10" value="60" max="60"></td>
            </tr>
            <tr>
                <td>무전기</td>
                <td><input type="checkbox" name="item11" value="12"></td>
                <td><input type="number" min="0" id="number11"></td>
                <td><input type="number" step="0.2" id="salePrice11" value="12" max="12"></td>
            </tr>
        </tbody>
    </table>

    <!-- 두 번째 테이블 -->
    <table>
        <thead>
            <tr>
                <th>장비</th>
                <th>구매 여부</th>
                <th>할인가(선택)</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>크루저 (트럭)</td>
                <td><input type="checkbox" name="ship1" value="370"></td>
                <td><input type="number" step="10" value="370" max="370"></td>
            </tr>

        </tbody>
    </table>

    <!-- 세 번째 테이블 -->
    <table>
        <thead>
            <tr>
                <th>장비</th>
                <th>구매 여부</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>순간이동기</td>
                <td><input type="checkbox" name="ship2" value="375"></td>
            </tr>
            <tr>
                <td>신호 해석기</td>
                <td><input type="checkbox" name="ship3" value="255"></td>
            </tr>
        </tbody>
    </table>

    <button onclick="calculate()">계산</button>
    <div id="result"></div> <!-- 결과 표시 공간 -->
</fieldset>


<script>

    function validateNumber(input) {
    const value = parseInt(input.value, 10);
    if (isNaN(value) || value < 0) {
        input.value = "";
        displayError("# 개수 혹은 할인가에 값을 바르게 입력하세요");
    }
}
    function validateDiscount(input) {
    const value = parseFloat(input.value);
    if (isNaN(value) || value <= 0) {
        input.value = "";
        displayError("# 개수 혹은 할인가에 값을 바르게 입력하세요");
    }
}
    function displayError(message) {
    const resultDiv = document.getElementById("result");
    resultDiv.textContent = message;
    resultDiv.style.color = "#ff6666";
}
function calculate() {
    const numberInputs = document.querySelectorAll("input[type='number']");
    let isValid = true;

    numberInputs.forEach(input => {
        if (input.value === "" || parseInt(input.value, 10) < 0) {
            isValid = false;
        }
    });

    if (!isValid) {
        displayError("# 개수 혹은 할인가에 값을 바르게 입력하세요");
        return;
    }

    const resultDiv = document.getElementById("result");
    resultDiv.textContent = "계산 완료!";
    resultDiv.style.color = "#ccffcc";
}

    

    function calculate() {
    const requiredQuota = parseInt(document.getElementById('RequiredQuota').value);
    const moonOrbitCost = parseInt(document.getElementById('MoonOrbitCost').value);
    const daysLeft = parseInt(document.getElementById('DaysLeft').value);


    let playerUtilityPurchase = 0; // 플레이어 유틸리티 구매 초기화
    let shipUtilityPurchase = 0; // 선박 유틸리티 구매 초기화
    let totalCost = 0; // 총 비용 초기화

    // 각 항목에 대한 비용 계산
   for (let i = 1; i <= 10; i++) {
        const checkbox = document.querySelector(`input[name="item${i}"]`);
        const quantity = parseInt(document.getElementById(`number${i}`).value) || 0;
        const salePrice = parseInt(document.getElementById(`salePrice${i}`).value) || 0;
        if (checkbox && checkbox.checked) {
            playerUtilityPurchase += salePrice * quantity;
        }
    }

   // 크루저 구매 금액 설정
    let CruiserPurchase = 0;
    const cruiserCheckbox = document.querySelector('input[name="ship1"]');
    const cruiserDiscount = parseInt(document.querySelector('input[name="ship1"]').parentNode.nextElementSibling.querySelector('input[type="number"]').value) || 370;

    if (cruiserCheckbox && cruiserCheckbox.checked) {
        CruiserPurchase = cruiserDiscount;
    }

    // 선박 유틸리티 구매 계산
    for (let j = 2; j <= 3; j++) {
        const shipCheckbox = document.querySelector(`input[name="ship${j}"]`);
        if (shipCheckbox && shipCheckbox.checked) { // checkbox가 정의된 경우에만 체크
            shipUtilityPurchase += parseInt(shipCheckbox.value); // 선박 유틸리티 구매 합산
        }
    }

    // 필요할 경우 할당량보다 낮은지 확인
    const totalPurchaseCost = moonOrbitCost + playerUtilityPurchase + CruiserPurchase + shipUtilityPurchase;

if (totalPurchaseCost < requiredQuota) {
    const resultDiv = document.getElementById('result');
    resultDiv.innerText = "# 할당량이 필요 자금보다 높음";
    resultDiv.classList.add('small-font'); // 작은 폰트 스타일 적용
    resultDiv.style.display = 'inline';
    return;
} else {
    const resultDiv = document.getElementById('result');
    resultDiv.classList.remove('small-font'); // 작은 폰트 스타일 제거
}

     // NeedtoSell 계산
       let NeedtoSell;
    if (isNaN(requiredQuota) || isNaN(moonOrbitCost)) {
        NeedtoSell = "Error";
    } else {
        let baseValue = Math.round((moonOrbitCost + playerUtilityPurchase + CruiserPurchase + shipUtilityPurchase) * 5 + 75 + requiredQuota) / 6;

        switch (daysLeft) {
            case 0:
                NeedtoSell = baseValue;
                break;
            case 1:
                baseValue = Math.round((moonOrbitCost + playerUtilityPurchase + CruiserPurchase + shipUtilityPurchase) * 5 + requiredQuota) / 6;
                baseValue /= 0.77;
                NeedtoSell = Math.ceil(baseValue % 1 >= 0.4 ? Math.ceil(baseValue) + 2 : Math.ceil(baseValue) + 1);
                break;
            case 2:
                baseValue = Math.round((moonOrbitCost + playerUtilityPurchase + CruiserPurchase + shipUtilityPurchase) * 5 - 75 + requiredQuota) / 6;
                NeedtoSell = Math.floor(baseValue / 0.53);
                break;
            case 3:
                baseValue = Math.round((moonOrbitCost + playerUtilityPurchase + CruiserPurchase + shipUtilityPurchase) * 5 - 150 + requiredQuota) / 6;
                NeedtoSell = Math.ceil(baseValue / 0.3);
                break;
        }

        NeedtoSell = Math.ceil(NeedtoSell, 130);
        NeedtoSell += " $";
    }

    // 결과 출력
      const resultDiv = document.getElementById('result');
    resultDiv.innerText = NeedtoSell;
    resultDiv.style.display = 'inline';
}

</script>
</body>
</html>

