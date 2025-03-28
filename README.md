<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Imed Technology</title>
    <style>
        body {
            background-color: white;
            color: black;
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
        }
        .header {
            background-color: #6a0dad; /* بنفسجي */
            padding: 15px;
            text-align: center;
            color: white;
            font-size: 24px;
            font-weight: bold;
        }
        .container {
            max-width: 1200px;
            margin: 20px auto;
            padding: 20px;
            text-align: center;
        }
        .component-box {
            border: 2px solid #6a0dad;
            padding: 15px;
            margin: 10px;
            display: inline-block;
            width: 250px;
            border-radius: 10px;
            box-shadow: 2px 2px 10px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s, box-shadow 0.3s;
            cursor: pointer;
        }
        .component-box:hover {
            transform: scale(1.05);
            box-shadow: 4px 4px 15px rgba(0, 0, 0, 0.2);
        }
        .button {
            background-color: #6a0dad;
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            margin-top: 10px;
            font-size: 16px;
        }
        .button:hover {
            background-color: #5a0cac;
        }
    </style>
</head>
<body>
    <div class="header">Imed Technology</div>
    <div class="container">
        <h2>اختر مكونات الكمبيوتر الخاص بك</h2>
        <div class="component-box" onclick="selectComponent('المعالج', 300)">المعالج - $300</div>
        <div class="component-box" onclick="selectComponent('كرت الشاشة', 500)">كرت الشاشة - $500</div>
        <div class="component-box" onclick="selectComponent('الذاكرة العشوائية', 100)">الذاكرة العشوائية - $100</div>
        <br>
        <button class="button" onclick="calculateTotal()">احسب التكلفة</button>
    </div>

    <script>
        let totalCost = 0;

        function selectComponent(name, price) {
            alert(`تم اختيار ${name} بسعر $${price}`);
            totalCost += price;
        }

        function calculateTotal() {
            alert(`التكلفة الإجمالية للمكونات المختارة: $${totalCost}`);
        }
    </script>
</body>
</html>
