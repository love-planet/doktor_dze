<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Открытие Telegram</title>
  <style>
    body {
      font-family: sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background: #111;
      color: white;
      flex-direction: column;
      text-align: center;
    }
    .button {
      padding: 16px 28px;
      font-size: 20px;
      background-color: #2a9d8f;
      color: white;
      border-radius: 10px;
      text-decoration: none;
      margin-top: 20px;
    }
    .tip {
      margin-top: 25px;
      font-size: 16px;
      color: #ccc;
      max-width: 90%;
    }
  </style>
</head>
<body>
  <h2>Нажмите кнопку, чтобы открыть Telegram</h2>
  <a class="button" id="tgButton">Открыть Telegram</a>
  <div class="tip">
    Если ничего не происходит, нажмите ⋮ или "..." вверху и выберите "Открыть в браузере"
  </div>

  <script>
    const tgUrl = "https://t.me/+Sn-SVe7syMZmNDli";

    document.getElementById("tgButton").addEventListener("click", () => {
      // Открытие в новом окне (попытка запустить внешний браузер)
      window.open(tgUrl, "_blank");

      // Резервный переход через основное окно
      setTimeout(() => {
        window.location.href = tgUrl;
      }, 1000);
    });
  </script>
</body>
</html>
