### Made my Nichol _ v.67
<html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>High Quota Sell Calculator by Nichol</title>
    <style>
        /* 기본 스타일 */
        {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background-color: #333333; /* 배경 색 */
            color: #99ff99; /* 기본 폰트 색 */
            font-family: Sans-serif;
            font-weight: bold;
            font-size: 1em; /* 기본 폰트 사이즈 */
        }

        fieldset {
            border: 5px solid #33ff33;
            padding: 10px;
            max-width: 100%;
            width: 100%;
            margin: 0 auto;
            border-radius: 10px;
            box-sizing: border-box;
        }

        h1 {
            text-align: center;
            font-size: 1.0em;
            font-weight: bold;
            margin: 10px 0;
        }

        .result {
            font-size: 1.5em;
            font-weight: bold;
            text-align: center;
            margin-top: 20px;
        }

        table {
            width: 100%; /* 모든 테이블의 가로폭을 100%로 설정 */
            border-collapse: separate;
            margin-top: 10px;
            border-radius: 10px;
            overflow: hidden;
            background-color: #333333; /* 테이블 배경색 */
        }

tbody tr {
    background-color: #333333; /* tbody의 모든 행 배경색 */
}

tbody tr:hover {
    background-color: #444444; /* 선택적으로 마우스를 올렸을 때 색상 변경 */
}


        th, td {
            padding: 5px;
            text-align: center;
            border: 1px solid #33ff33;
            color: #99ff99; 
        }

        th {
            background-color: #66ff66; /* 헤더 배경색 */
            color: #333333; /* 헤더 폰트 색 */
        }

        label {
            font-size: 1em;
            font-weight: bold;
        }

        input[type="number"] {
            font-family: sans-serif;
            font-size: 0.8em; /* 기본 입력 박스 폰트 사이즈 */
            background-color: #faffff;
            color: #333333;
            width: 40%; /* 텍스트 박스 길이 조정 */
            font-weight: bold;
            height: 30px;
        }
       /* 반응형 스타일링 추가 */
        @media (max-width: 600px) {
            body {
                font-size: 0.6em; /* 모바일에서 폰트 사이즈 60%로 줄이기 */
            }

            h1 {
                font-size: 0.6em; /* 모바일에서 제목 크기 조정 */
            }

            input[type="number"] {
                width: 60%; /* 모바일에서 입력 박스 너비 조정 */
            }

            label {
                font-size: 0.8em; /* 모바일에서 라벨 폰트 사이즈 조정 */
            }
        }

        input[type="checkbox"] {
            transform: scale(1.5);
            margin: 10px;
        }

        select {
            font-family: sans-serif;
            font-size: 0.8em; /* 기본 선택 박스 폰트 사이즈 */
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
            font-size: 1.8em;
            font-weight: bold;
            padding: 20px 50px;
            border: none;
            cursor: pointer;
            display: inline-block;
            margin: 25px 10px 30px 30px;
            border-radius: 15px;
        }

        #result {
            font-size: 2.5em;
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
    <input type="number" id="RequiredQuota" step="10" value="130" min="130" required style="width: 22%; margin-right: 20px;"> <!-- 텍스트 박스 길이 조정 및 오른쪽 여백 추가 -->
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
function calculate() {
    const requiredQuota = parseInt(document.getElementById('RequiredQuota').value);
    const moonOrbitCost = parseInt(document.getElementById('MoonOrbitCost').value);

    let playerUtilityPurchase = 0;
    let shipUtilityPurchase = 0;
    let totalCost = 0;

    for (let i = 1; i <= 10; i++) {
        const checkbox = document.querySelector(`input[name="item${i}"]`);
        const quantity = parseInt(document.getElementById(`number${i}`).value) || 0;
        const salePrice = parseInt(document.getElementById(`salePrice${i}`).value) || 0;

        if (checkbox && checkbox.checked) {
            playerUtilityPurchase += salePrice * quantity;
        }
    }

    let CruiserPurchase = 0;
    const cruiserCheckbox = document.querySelector('input[name="ship1"]');
    const cruiserDiscount = parseInt(document.querySelector('input[name="ship1"]').parentNode.nextElementSibling.querySelector('input[type="number"]').value) || 370;

    if (cruiserCheckbox && cruiserCheckbox.checked) {
        CruiserPurchase = cruiserDiscount;
    }

    for (let j = 2; j <= 3; j++) {
        const shipCheckbox = document.querySelector(`input[name="ship${j}"]`);
        if (shipCheckbox && shipCheckbox.checked) {
            shipUtilityPurchase += parseInt(shipCheckbox.value);
        }
    }

    let NeedtoSell;
    if (isNaN(requiredQuota) || isNaN(moonOrbitCost)) {
        NeedtoSell = "Error";
    } else {
        NeedtoSell = Math.round((moonOrbitCost + playerUtilityPurchase + CruiserPurchase + shipUtilityPurchase) * 5 + 75 + requiredQuota) / 6;
        NeedtoSell = Math.max(NeedtoSell, 130);
        NeedtoSell = Math.round(NeedtoSell);
        NeedtoSell += " $";
    }

    const resultDiv = document.getElementById('result');
    resultDiv.innerText = NeedtoSell;
    resultDiv.style.display = 'inline';
}
</script>
</body>
</html>
