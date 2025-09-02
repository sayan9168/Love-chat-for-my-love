<!DOCTYPE html>
<html lang="bn">
<head>
  <meta charset="UTF-8">
  <title>Love Chat ❤️</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: Arial, sans-serif;
      background: url('https://images.unsplash.com/photo-1506748686214-e9df14d4d9d0') no-repeat center center fixed;
      background-size: cover;
    }

    /* Login Page */
    #loginPage {
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      background: rgba(0,0,0,0.6);
      color: white;
    }

    #chatPage {
      display: none;
      height: 100vh;
      background: rgba(255,255,255,0.85);
      padding: 20px;
    }

    .chat-box {
      height: 70vh;
      overflow-y: auto;
      border: 2px solid #ff4da6;
      padding: 10px;
      border-radius: 10px;
      background: white;
    }

    .message {
      margin: 5px 0;
      padding: 8px;
      border-radius: 10px;
      max-width: 70%;
    }

    .me {
      background: #ffb6c1;
      text-align: right;
      margin-left: auto;
    }

    .gf {
      background: #ffcce0;
      text-align: left;
      margin-right: auto;
    }

    input, button, select {
      padding: 10px;
      margin-top: 10px;
      border-radius: 5px;
      border: none;
    }

    button {
      background: #ff4da6;
      color: white;
      cursor: pointer;
    }
  </style>
</head>
<body>

  <!-- Background Music -->
  <audio id="bgMusic" autoplay loop>
    <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
    আপনার ব্রাউজার অডিও সাপোর্ট করছে না।
  </audio>

  <!-- Login Page -->
  <div id="loginPage">
    <h1>🔐 Enter Password</h1>
    <input type="password" id="passwordInput" placeholder="Enter Password">
    <button onclick="checkPassword()">Login</button>
  </div>

  <!-- Chat Page -->
  <div id="chatPage">
    <h2>💌 Love Chat For My Love 💌</h2>
    <div class="chat-box" id="chatBox"></div>
    <select id="sender">
      <option value="me">Me</option>
      <option value="gf">My Love</option>
    </select>
    <input type="text" id="msgInput" placeholder="Type a message...">
    <button onclick="sendMessage()">Send</button>
  </div>

  <script>
    const correctPassword = "SAYAN AND ANU"; // এখান থেকে Password বদলাও

    function checkPassword() {
      const pass = document.getElementById("passwordInput").value;
      if(pass === correctPassword) {
        document.getElementById("loginPage").style.display = "none";
        document.getElementById("chatPage").style.display = "block";
        document.getElementById("bgMusic").play(); // Login করলে গান চালু হবে
      } else {
        alert("❌ Wrong Password!");
      }
    }

    function sendMessage() {
      const msgBox = document.getElementById("chatBox");
      const msgInput = document.getElementById("msgInput");
      const sender = document.getElementById("sender").value;
      const message = msgInput.value;

      if(message.trim() !== "") {
        const newMsg = document.createElement("div");
        newMsg.classList.add("message", sender);

        if(sender === "me") {
          newMsg.innerText = "Me: " + message;
        } else {
          newMsg.innerText = "My Love: " + message;
        }

        msgBox.appendChild(newMsg);
        msgInput.value = "";
        msgBox.scrollTop = msgBox.scrollHeight;
      }
    }
  </script>

</body>
</html><!DOCTYPE html>
<html lang="bn">
<head>
  <meta charset="UTF-8">
  <title>Love Chat ❤️</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: Arial, sans-serif;
      background: url('https://images.unsplash.com/photo-1506748686214-e9df14d4d9d0') no-repeat center center fixed;
      background-size: cover;
    }

    /* Login Page */
    #loginPage {
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      background: rgba(0,0,0,0.6);
      color: white;
    }

    #chatPage {
      display: none;
      height: 100vh;
      background: rgba(255,255,255,0.85);
      padding: 20px;
    }

    .chat-box {
      height: 70vh;
      overflow-y: auto;
      border: 2px solid #ff4da6;
      padding: 10px;
      border-radius: 10px;
      background: white;
    }

    .message {
      margin: 5px 0;
      padding: 8px;
      border-radius: 10px;
      max-width: 70%;
    }

    .me {
      background: #ffb6c1;
      text-align: right;
      margin-left: auto;
    }

    .gf {
      background: #ffcce0;
      text-align: left;
      margin-right: auto;
    }

    input, button, select {
      padding: 10px;
      margin-top: 10px;
      border-radius: 5px;
      border: none;
    }

    button {
      background: #ff4da6;
      color: white;
      cursor: pointer;
    }
  </style>
</head>
<body>

  <!-- Background Music -->
  <audio id="bgMusic" autoplay loop>
    <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
    আপনার ব্রাউজার অডিও সাপোর্ট করছে না।
  </audio>

  <!-- Login Page -->
  <div id="loginPage">
    <h1>🔐 Enter Password</h1>
    <input type="password" id="passwordInput" placeholder="Enter Password">
    <button onclick="checkPassword()">Login</button>
  </div>

  <!-- Chat Page -->
  <div id="chatPage">
    <h2>💌 Love Chat For My Love 💌</h2>
    <div class="chat-box" id="chatBox"></div>
    <select id="sender">
      <option value="me">Me</option>
      <option value="gf">My Love</option>
    </select>
    <input type="text" id="msgInput" placeholder="Type a message...">
    <button onclick="sendMessage()">Send</button>
  </div>

  <script>
    const correctPassword = "SAYAN AND ANU"; // এখান থেকে Password বদলাও

    function checkPassword() {
      const pass = document.getElementById("passwordInput").value;
      if(pass === correctPassword) {
        document.getElementById("loginPage").style.display = "none";
        document.getElementById("chatPage").style.display = "block";
        document.getElementById("bgMusic").play(); // Login করলে গান চালু হবে
      } else {
        alert("❌ Wrong Password!");
      }
    }

    function sendMessage() {
      const msgBox = document.getElementById("chatBox");
      const msgInput = document.getElementById("msgInput");
      const sender = document.getElementById("sender").value;
      const message = msgInput.value;

      if(message.trim() !== "") {
        const newMsg = document.createElement("div");
        newMsg.classList.add("message", sender);

        if(sender === "me") {
          newMsg.innerText = "Me: " + message;
        } else {
          newMsg.innerText = "My Love: " + message;
        }

        msgBox.appendChild(newMsg);
        msgInput.value = "";
        msgBox.scrollTop = msgBox.scrollHeight;
      }
    }
  </script>

</body>
</html>
