<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <title>وِصال - تطبيق الدردشة</title>
  <link rel="stylesheet" href="style.css">
  <link href="https://fonts.googleapis.com/css2?family=Tajawal&display=swap" rel="stylesheet">
</head>
<body>
  <header>
    <h1>📨 وِصال</h1>
  </header>

  <main>
    <div class="chat-container">
      <div id="messages" class="messages"></div>
      <div class="input-area">
        <input type="text" id="messageInput" placeholder="اكتب رسالتك...">
        <button onclick="sendMessage()">إرسال</button>
      </div>
    </div>
  </main>

  <footer>
    <p>© 2025 تطبيق وصال - جميع الحقوق محفوظة</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>