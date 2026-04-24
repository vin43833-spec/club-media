<!DOCTYPE html><html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>نادي الإعلام والتواصل</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: linear-gradient(to right, #0f2027, #203a43, #2c5364);
      color: white;
      min-height: 100vh;
    }
    header {
      text-align: center;
      padding: 40px 20px;
    }
    header h1 {
      font-size: 36px;
      margin-bottom: 10px;
      text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
    }
    header p {
      opacity: 0.9;
      font-size: 18px;
    }
    .container {
      max-width: 600px;
      margin: auto;
      background: rgba(255,255,255,0.08);
      padding: 40px;
      border-radius: 20px;
      box-shadow: 0 15px 40px rgba(0,0,0,0.4);
      backdrop-filter: blur(10px);
      border: 1px solid rgba(255,255,255,0.1);
    }
    form {
      display: grid;
      gap: 20px;
    }
    input {
      padding: 15px;
      border-radius: 12px;
      border: 2px solid rgba(255,255,255,0.1);
      outline: none;
      font-size: 16px;
      background: rgba(255,255,255,0.1);
      color: white;
      transition: all 0.3s;
    }
    input::placeholder {
      color: rgba(255,255,255,0.7);
    }
    input:focus {
      box-shadow: 0 0 20px #00c6ff;
      border-color: #00c6ff;
      background: rgba(255,255,255,0.15);
    }
    button {
      padding: 18px;
      border: none;
      border-radius: 12px;
      background: linear-gradient(45deg, #25D366, #128C7E);
      color: white;
      font-size: 20px;
      font-weight: bold;
      cursor: pointer;
      transition: all 0.3s;
      box-shadow: 0 8px 25px rgba(37,211,102,0.4);
    }
    button:hover {
      transform: translateY(-3px);
      box-shadow: 0 12px 35px rgba(37,211,102,0.6);
    }
    footer {
      text-align: center;
      padding: 30px;
      margin-top: 40px;
      opacity: 0.8;
      font-size: 14px;
    }
    @media (max-width: 480px) {
      header h1 { font-size: 28px; }
      .container { margin: 20px; padding: 30px 20px; }
    }
  </style>
</head>
<body>
  <header>
    <h1>🎥 نادي الإعلام والتواصل</h1>
    <p>استمارة التسجيل السريع</p>
  </header>
  
  <div class="container">
    <form id="registrationForm">
      <input type="text" id="firstName" placeholder="الاسم الشخصي *" required>
      <input type="text" id="lastName" placeholder="النسب *" required>
      <input type="tel" id="phone" placeholder="رقم الهاتف *" required>
      <button type="submit">📱 إرسال عبر واتساب</button>
    </form>
  </div>
  
  <footer>
    © 2026 نادي الإعلام والتواصل | جميع الحقوق محفوظة
  </footer>

  <script>
    const form = document.getElementById('registrationForm');
    form.addEventListener('submit', function(e) {
      e.preventDefault();
      
      // رقمك الجديد
      const clubNumber = "212678479295";
      const message = `أود الانضمام لمجموعة نادي الإعلام والتواصل`;
      
      const whatsappURL = `https://wa.me/${clubNumber}?text=${encodeURIComponent(message)}`;
      window.open(whatsappURL, '_blank');
      
      // رسالة تأكيد
      alert('تم إرسال طلبك بنجاح! 📲');
    });
  </script>
</body>
</html>
