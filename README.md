# AR-LIVE-27
<!DOCTYPE html>
<html>
<head>
  <title>AR Live Score</title>
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <style>
    body { font-family: Arial; text-align: center; background:#f4f6f8; }
    .card { background:#fff; margin:16px; padding:16px; border-radius:12px; }
    .score { font-size: 36px; color: #16a34a; margin: 10px 0; }
    .btn { padding:10px 14px; font-size:16px; margin:6px; border:0; border-radius:8px; }
  </style>
</head>
<body>

  <h1>AR LIVE 27</h1>

  <div class="card">
    <h2>Team A vs Team B</h2>
    <div class="score" id="score">0/0 (0.0)</div>

    <button class="btn" onclick="run()">Run +1</button>
    <button class="btn" onclick="wicket()">Wicket</button>
    <button class="btn" onclick="ball()">Ball</button>
  </div>

<script>
  let runs = 0;
  let wickets = 0;
  let balls = 0;

  function run(){
    runs++;
    update();
  }
  function wicket(){
    wickets++;
    update();
  }
  function ball(){
    balls++;
    update();
  }
  function update(){
    const overs = Math.floor(balls/6) + "." + (balls%6);
    document.getElementById("score").innerText =
      runs + "/" + wickets + " (" + overs + ")";
  }
</script>

</body>
</html>
