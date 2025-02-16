<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>حاسبة قيمة استهلاك الكهرب</title>
    <script>
        function calculate() {
            var number = parseFloat(document.getElementById("inputNumber").value);
            
            if (isNaN(number)) {
                alert("يرجى إدخال رقم صحيح");
                return;
            }

            // ضرب الرقم في 18
            var result = number * 18;
            
            // تقسيم الناتج على 100
            result = result / 100;
            
            // إضافة 15% إلى الناتج
            result = result + (result * 0.15);
            
            // عرض النتيجة
            document.getElementById("result").innerText = "النتيجة: " + result.toFixed(2);
        }
    </script>
</head>
<body>
    <h1>آلة حاسبة</h1>
    <label for="inputNumber">أدخل رقم:</label>
    <input type="number" id="inputNumber" placeholder="أدخل الرقم هنا">
    <button onclick="calculate()">احسب</button>
    <p id="result"></p>
</body>
</html>
