### Made my Nichol
<html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>High Quota Sell Calculator by Nichol</title>
    <style>
        body {
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
            text-align: center;
            font-size: 2em;
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
        }
        th, td {
            padding: 5px; /* 줄인 부분 */
            text-align: center;
            border: 1px solid #33ff33;
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
        th {
            font-size: 1.3em;
            background-color: #66ff66;
            color: #333333;
        }
        table:nth-of-type(2) th {
            background-color: #66ff66; 
            color: #333333; 
}
table:nth-of-type(2) {
    width: 100%; /* 가로폭을 100%로 설정 */
    table-layout: fixed; /* 고정 너비 레이아웃 */
}
table:nth-of-type(2) th:first-child, 
table:nth-of-type(2) td:first-child {
    width: 220px; /* 두 번째 테이블의 첫 번째 열 너비 증가 */
}

table:nth-of-type(2) th:last-child, 
table:nth-of-type(2) td:last-child {
    width: 100px; /* 두 번째 테이블의 두 번째 열 너비 감소 */
        }
        label {
            font-size: 18px;
        }
        input[type="checkbox"] {
            transform: scale(1.5);
            margin: 10px;
        }
        input[type="number"] {
            font-family: serif;
            font-size: 16px; 
            padding: 1px; 
            border: 1px solid #99ff99; 
            background-color: #faffff;
            color: #333333;
            width: 65%;
            font-weight: bold;
            height: 20px;
        }
        input[type="number"]#RequiredQuota {
            width: 25%; 
            margin-right: 20px; 
        }
        select {
            font-family: sans-serif;
            font-size: 16px;
            padding: 5px; 
            border: 1px solid #33ff33; 
            background-color: #333333;
            color: #ffffff; 
            width: 40%; 
            height: 40px; 
            font-weight: bold; 
            box-sizing: border-box; 
        }
        button {
            background-color: #66ff66;
            color: #000000;
            font-size: 1.4em;
            font-weight: bold;
            padding: 15px 35px;
            border: none;
            cursor: pointer;
            display: inline-block;
            margin: 20px; 
        }
        #result {
            font-size: 1.5em; 
            font-weight: bold; 
            color: #33ff33; 
            display: inline-block; 
            margin-left: 10px; 
        }
    </style>
</head>
<body>

<fieldset>
    <h1>High Quota Challenge <br> Sell & Purchase Calculator <br> 할당량 챌린지 상점 계산기</h1>

    <div style="display: flex; align-items: center; margin-bottom: 10px;">
        <label for="RequiredQuota">할당량 :&nbsp;</label>
        <input type="number" id="RequiredQuota" step="10" value="130" required>
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
                <td><input type="number" step="1" id="salePrice1" value="30"></td>
            </tr>
            <tr>
                <td>자물쇠 따개</td>
                <td><input type="checkbox" name="item2" value="20"></td>
                <td><input type="number" min="0" id="number2"></td>
                <td><input type="number" step="1" id="salePrice2" value="20"></td>
            </tr>
            <tr>
                <td>제초제</td>
                <td><input type="checkbox" name="item3" value="25"></td>
                <td><input type="number" min="0" id="number3"></td>
                <td><input type="number" step="1" id="salePrice3" value="25"></td>
            </tr>
            <tr>
                <td>제트팩</td>
                <td><input type="checkbox" name="item4" value="900"></td>
                <td><input type="number" min="0" id="number4"></td>
                <td><input type="number" step="10.0" id="salePrice4" value="900"></td>
            </tr>
            <tr>
                <td>페인트 스프레이</td>
                <td><input type="checkbox" name="item5" value="50"></td>
                <td><input type="number" min="0" id="number5"></td>
                <td><input type="number" step="1" id="salePrice5" value="50"></td>
            </tr>
            <tr>
                <td>벨트 배낭</td>
                <td><input type="checkbox" name="item6" value="45"></td>
                <td><input type="number" min="0" id="number6"></td>
                <td><input type="number" step="1" id="salePrice6" value="45"></td>
            </tr>
            <tr>
                <td>TZP-흡입제</td>
                <td><input type="checkbox" name="item7" value="80"></td>
                <td><input type="number" min="0" id="number7"></td>
                <td><input type="number" step="1" id="salePrice7"  value="80"></td>
            </tr>
            <tr>
                <td>프로 손전등</td>
                <td><input type="checkbox" name="item8" value="25"></td>
                <td><input type="number" min="0" id="number8"></td>
                <td><input type="number" step="1" id="salePrice8" value="25"></td>
            </tr>
            <tr>
                <td>기절 수류탄</td>
                <td><input type="checkbox" name="item9" value="30"></td>
                <td><input type="number" min="0" id="number9"></td>
                <td><input type="number" step="1" id="salePrice9" value="30"></td>
            </tr>
            <tr>
                <td>연장형 사다리</td>
                <td><input type="checkbox" name="item10" value="60"></td>
                <td><input type="number" min="0" id="number10"></td>
                <td><input type="number" step="1" id="salePrice10" value="60"></td>
            </tr>
            <tr>
                <td>무전기</td>
                <td><input type="checkbox" name="item11" value="12"></td>
                <td><input type="number" min="0" id="number11"></td>
                <td><input type="number" step="1.0" id="salePrice11" value="12"></td>
            </tr>
        </tbody>
    </table>

    <table>
        <thead>
            <tr>
                <th>장비</th>
                <th>구매 여부</th>
            </tr>
        </thead>
        <tbody>
            <tr>
                <td>크루저 (트럭)</td>
                <td><input type="checkbox" name="ship1" value="370"></td>
            </tr>
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
function calculate() {
    const requiredQuota = parseInt(document.getElementById('RequiredQuota').value);
    const moonOrbitCost = parseInt(document.getElementById('MoonOrbitCost').value);

    let playerUtilityPurchase = 0; // 플레이어 유틸리티 구매 초기화
    let shipUtilityPurchase = 0; // 선박 유틸리티 구매 초기화
    let totalCost = 0; // 총 비용 초기화

// 각 항목에 대한 비용 계산
for (let i = 1; i <= 10; i++) {
    const checkbox = document.querySelector(`input[name="item${i}"]`);
    const quantity = parseInt(document.getElementById(`number${i}`).value) || 0;
    const salePrice = parseInt(document.getElementById(`salePrice${i}`).value) || 0;

    if (checkbox && checkbox.checked) { // checkbox가 정의된 경우에만 체크
        playerUtilityPurchase += salePrice * quantity; // 플레이어 유틸리티 구매 합산
    }
}

// 선박 유틸리티 구매 계산
for (let j = 1; j <= 3; j++) {
    const shipCheckbox = document.querySelector(`input[name="ship${j}"]`);
    if (shipCheckbox && shipCheckbox.checked) { // checkbox가 정의된 경우에만 체크
        shipUtilityPurchase += parseInt(shipCheckbox.value); // 선박 유틸리티 구매 합산
    }
}

// NeedtoSell 계산
let NeedtoSell;
if (isNaN(requiredQuota) || isNaN(moonOrbitCost)) {
    NeedtoSell = "Error"; // 오류가 발생할 경우 "Error" 출력
} else {
    NeedtoSell = Math.round((moonOrbitCost + playerUtilityPurchase + shipUtilityPurchase) * 5 + 75 + requiredQuota) / 6;
    NeedtoSell = Math.max(NeedtoSell, 130); // 결과값을 130 이상으로 보장
    NeedtoSell = Math.round(NeedtoSell); // 결과값을 소수점 첫째 자리에서 반올림
    NeedtoSell += " $"; // 결과에 "$" 추가
}

    // 결과 출력
    const resultDiv = document.getElementById('result');
    resultDiv.innerText = NeedtoSell; // 결과 값 출력
    resultDiv.style.display = 'inline'; // 결과를 표시
}
</script>
</body>
</html>
