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
body {
  font-family: 'Tajawal', sans-serif;
  background-color: #fdfcf9;
  color: #2e7d32;
  margin: 0;
  padding: 0;
}

header {
  background-color: #2e7d32;
  color: white;
  text-align: center;
  padding: 1rem;
  font-size: 1.5rem;
}

.chat-container {
  max-width: 600px;
  margin: 2rem auto;
  border: 2px solid #c2b280;
  border-radius: 10px;
  padding: 1rem;
  background-color: white;
}

.messages {
  height: 300px;
  overflow-y: auto;
  border-bottom: 1px solid #ccc;
  padding-bottom: 1rem;
  margin-bottom: 1rem;
}

.message {
  padding: 0.5rem;
  margin: 0.3rem 0;
  background-color: #e0f2f1;
  border-radius: 5px;
}

.input-area {
  display: flex;
  gap: 0.5rem;
}

input[type="text"] {
  flex-grow: 1;
  padding: 0.5rem;
  border: 1px solid #aaa;
  border-radius: 5px;
}

button {
  background-color: #c2b280;
  border: none;
  padding: 0.5rem 1rem;
  color: #2e7d32;
  font-weight: bold;
  border-radius: 5px;
  cursor: pointer;
}

button:hover {
  background-color: #b0a46e;
}

footer {
  text-align: center;
  margin-top: 2rem;
  padding: 1rem;
  background-color: #f4f4f4;
  font-size: 0.9rem;
}function sendMessage() {
  const input = document.getElementById('messageInput');
  const messages = document.getElementById('messages');
  const text = input.value.trim();

  if (text !== "") {
    const messageElement = document.createElement('div');
    messageElement.classList.add('message');
    messageElement.innerText = text;
    messages.appendChild(messageElement);
    input.value = "";
    messages.scrollTop = messages.scrollHeight;
  }
}<!-- Firebase CDN -->
<script src="https://www.gstatic.com/firebasejs/10.12.0/firebase-app-compat.js"></script>
<script src="https://www.gstatic.com/firebasejs/10.12.0/firebase-database-compat.js"></script>

<script>
  const firebaseConfig = {
    apiKey: "YOUR_API_KEY",
    authDomain: "YOUR_APP.firebaseapp.com",
    databaseURL: "https://YOUR_APP.firebaseio.com",
    projectId: "YOUR_APP",
    storageBucket: "YOUR_APP.appspot.com",
    messagingSenderId: "YOUR_SENDER_ID",
    appId: "YOUR_APP_ID"
  };

  firebase.initializeApp(firebaseConfig);
  const db = firebase.database();
</script>