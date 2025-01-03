<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>トラップゲーム</title>
  <style>
    body {
      margin: 0;
      overflow: hidden;
    }
    #gameArea {
      position: relative;
      width: 100vw;
      height: 100vh;
      background-color: #f0f0f0;
    }
    .wall {
      position: absolute;
      background-color: red;
      border: 1px solid black;
    }
    #message {
      display: none;
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      font-size: 2rem;
      font-weight: bold;
      color: white;
      background-color: rgba(0, 0, 0, 0.8);
      padding: 20px;
      border-radius: 10px;
    }
  </style>
</head>
<body>
  <div id="gameArea">
    <div id="message">お前下手じゃん</div>
    <div class="wall" style="top: 20%; left: 30%; width: 20%; height: 5%;"></div>
    <div class="wall" style="top: 50%; left: 60%; width: 15%; height: 5%;"></div>
    <div class="wall" style="top: 80%; left: 10%; width: 25%; height: 5%;"></div>
  </div>
  <script>
    const gameArea = document.getElementById('gameArea');
    const message = document.getElementById('message');
    const walls = document.querySelectorAll('.wall');

    // 壁に当たったかどうかを判定する関数
    function checkCollision(event) {
      const x = event.clientX;
      const y = event.clientY;

      for (const wall of walls) {
        const rect = wall.getBoundingClientRect();
        if (x >= rect.left && x <= rect.right && y >= rect.top && y <= rect.bottom) {
          showMessage();
          return;
        }
      }
    }

    // メッセージを表示する関数
    function showMessage() {
      message.style.display = 'block';
      setTimeout(() => {
        message.style.display = 'none';
        alert("リトライしてみてね！");
      }, 2000);
    }

    // マウス移動イベントを監視
    gameArea.addEventListener('mousemove', checkCollision);
  </script>
</body>
</html>
