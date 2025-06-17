<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Fighting Game</title>
  <style>
    body {
      font-family: 'Arial', sans-serif;
      background: #111;
      color: #fff;
      display: flex;
      flex-direction: column;
      align-items: center;
      padding-top: 40px;
    }

    .game {
      display: flex;
      justify-content: space-around;
      width: 80%;
      margin-bottom: 20px;
    }

    .player {
      text-align: center;
    }

    .health-bar {
      width: 200px;
      height: 25px;
      background: #444;
      margin: 10px auto;
      border-radius: 5px;
      overflow: hidden;
    }

    .health {
      height: 100%;
      background: limegreen;
      width: 100%;
      transition: width 0.3s;
    }

    button {
      padding: 10px 20px;
      font-size: 16px;
      background: crimson;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }

    .winner {
      font-size: 24px;
      margin-top: 20px;
      color: gold;
    }
  </style>
</head>
<body>
  <h1>⚔️ Fighting Game ⚔️</h1>
  <div class="game">
    <div class="player" id="player1">
      <h2>Player 1</h2>
      <div class="health-bar"><div class="health" id="health1"></div></div>
      <button onclick="attack('player1')">Attack Player 2</button>
    </div>

    <div class="player" id="player2">
      <h2>Player 2</h2>
      <div class="health-bar"><div class="health" id="health2"></div></div>
      <button onclick="attack('player2')">Attack Player 1</button>
    </div>
  </div>

  <div class="winner" id="winner"></div>

  <script>
    let health1 = 100;
    let health2 = 100;

    function attack(attacker) {
      if (health1 <= 0 || health2 <= 0) return;

      const damage = Math.floor(Math.random() * 20) + 5;

      if (attacker === 'player1') {
        health2 = Math.max(0, health2 - damage);
        document.getElementById('health2').style.width = health2 + '%';
      } else {
        health1 = Math.max(0, health1 - damage);
        document.getElementById('health1').style.width = health1 + '%';
      }

      checkWinner();
    }

    function checkWinner() {
      const winnerText = document.getElementById('winner');
      if (health1 <= 0) {
        winnerText.textContent = '🏆 Player 2 Wins!';
      } else if (health2 <= 0) {
        winnerText.textContent = '🏆 Player 1 Wins!';
      }
    }
  </script>
</body>
</html>
