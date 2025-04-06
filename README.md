<!DOCTYPE html>
<html>
  <head>
    <title>My Mini App</title>
    <meta charset="UTF-8" />
    <script src="https://telegram.org/js/telegram-web-app.js"></script>
    <style>
      body {
        background: #fff;
        font-family: sans-serif;
        text-align: center;
        margin: 50px;
      }
      button {
        font-size: 18px;
        padding: 10px 20px;
      }
    </style>
  </head>
  <body>
    <h1>Hello, Telegram!</h1>
    <button onclick="sayHi()">Say hi to Telegram</button>
    <script>
      const tg = window.Telegram.WebApp;
      tg.expand();

      function sayHi() {
        tg.sendData("Hi from Mini App!"); // або просто покажемо alert
        alert("Hi, " + tg.initDataUnsafe.user.first_name + "!");
      }
    </script>
  </body>
</html>
