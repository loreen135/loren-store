# loren-store
موقع لحساب الاسعار
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />

  <!-- اسم المتجر في أعلى المتصفح -->
  <title>متجر لــورين — محوّل الدولار</title>

  <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@300;400;600;700&display=swap" rel="stylesheet">

  <style>
    body{
      margin:0;
      min-height:100vh;
      font-family:'Cairo', Arial, sans-serif;
      background: linear-gradient(180deg, #f8c6df 0%, #e07aa8 40%, #8f2f6b 100%);
      display:flex;
      align-items:center;
      justify-content:center;
      padding:20px;
      color:#fff;
    }

    .card{
      width:100%;
      max-width:420px;
      background: rgba(0,0,0,0.25);
      border-radius:24px;
      padding:26px;
      box-shadow: 0 10px 30px rgba(0,0,0,0.25);
      text-align:center;
    }

    .logo-wrap{
      width:140px;
      height:140px;
      margin: 0 auto 12px;
      border-radius:50%;
      background: rgba(255,255,255,0.15);
      display:flex;
      align-items:center;
      justify-content:center;
    }

    .logo-wrap img{
      width:85%;
      height:85%;
      object-fit:cover;
      border-radius:50%;
    }

    .store-name{
      font-size:28px;
      font-weight:700;
      margin:10px 0 20px;
    }

    input{
      width:100%;
      padding:14px;
      font-size:18px;
      border-radius:12px;
      border:none;
      margin-bottom:15px;
    }

    button{
      width:100%;
      padding:14px;
      border-radius:12px;
      border:none;
      font-size:18px;
      font-weight:600;
      background:#ff9a2e;
      cursor:pointer;
    }

    .result{
      margin-top:15px;
      font-size:20px;
      font-weight:600;
    }
  </style>
</head>

<body>

  <div class="card">

    <!-- صورة المتجر -->
    <div class="logo-wrap">
      <img src="Picsart_25-12-12_23-44-06-692.jpg" alt="متجر لورين">
    </div>

    <!-- اسم المتجر داخل الصفحة -->
    <div class="store-name">متجر لــورين</div>

    <input type="number" id="usd" placeholder="عدد الدولارات">

    <button onclick="calc()">احسب</button>

    <div class="result" id="result">المبلغ النهائي: — د.ج</div>

  </div>

  <script>
    function calc(){
      let usd = document.getElementById("usd").value;
      let rate = 29;   // سعر الدولار الواحد
      let extra = 20;  // الرسوم الإضافية
      let total = (usd * rate) + extra;

      document.getElementById("result").innerText =
        "المبلغ النهائي: " + total + " د.ج";
    }
  </script>

</body>
</html>
