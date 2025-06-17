<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Enhanced Fighting Game</title>
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
      margin-top: 10px;
    }

    .winner {
      font-size: 24px;
      margin-top: 20px;
      color: gold;
    }

    .flash {
