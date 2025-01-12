<!FORSE>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Minimalist Racer</title>
  <style>
    body {
      margin: 0;
      overflow: hidden;
      font-family: Arial, sans-serif;
      background: #111;
      color: #fff;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }

    #gameCanvas {
      border: 2px solid white;
      background: #222;
    }
  </style>
</head>
<body>
  <canvas id="gameCanvas"></canvas>
  <script>
    const canvas = document.getElementById("gameCanvas");
    const ctx = canvas.getContext("2d");

    // Adjust canvas size to fit the screen
    function resizeCanvas() {
      canvas.width = window.innerWidth * 0.9;
      canvas.height = window.innerHeight * 0.9;
    }
    resizeCanvas();
    window.addEventListener("resize", resizeCanvas);

    // Game variables
    const player = {
      x: canvas.width / 2 - 15,
      y: canvas.height - 60,
      width: 30,
      height: 30,
      speed: canvas.width * 0.02, // Adjust speed based on canvas width
    };
    let obstacles = [];
    let gameSpeed = canvas.height * 0.0025; // Adjust speed based on canvas height
    let isGameOver = false;
    let score = 0;

    let touchStartX = null;
    let touchEndX = null;

    // Function to create obstacles
    function createObstacle() {
      const obstacleWidth = Math.random() * (canvas.width * 0.2) + canvas.width * 0.1;
      const obstacleX = Math.random() * (canvas.width - obstacleWidth);
      obstacles.push({
        x: obstacleX,
        y: -20,
        width: obstacleWidth,
        height: canvas.height * 0.03,
      });
    }

    // Function to draw the player
    function drawPlayer() {
      ctx.fillStyle = "white";
      ctx.fillRect(player.x, player.y, player.width, player.height);
    }

    // Function to draw obstacles
    function drawObstacles() {
      ctx.fillStyle = "red";
      obstacles.forEach((obs) => {
        ctx.fillRect(obs.x, obs.y, obs.width, obs.height);
      });
    }

    // Update game state
    function updateGame() {
      if (isGameOver) return;

      // Move obstacles
      obstacles.forEach((obs) => {
        obs.y += gameSpeed;
      });

      // Remove off-screen obstacles
      obstacles = obstacles.filter((obs) => obs.y < canvas.height);

      // Collision detection
      obstacles.forEach((obs) => {
        if (
          player.x < obs.x + obs.width &&
          player.x + player.width > obs.x &&
          player.y < obs.y + obs.height &&
          player.y + player.height > obs.y
        ) {
          isGameOver = true;
        }
      });

      // Increase difficulty
      score++;
      if (score % 100 === 0) {
        gameSpeed += canvas.height * 0.0005;
      }
    }

    // Draw game elements
    function drawGame() {
      ctx.clearRect(0, 0, canvas.width, canvas.height);

      // Draw player and obstacles
      drawPlayer();
      drawObstacles();

      // Display score
      ctx.fillStyle = "white";
      ctx.font = `${canvas.width * 0.05}px Arial`;
      ctx.fillText(`Score: ${score}`, canvas.width * 0.05, canvas.height * 0.1);

      // End screen
      if (isGameOver) {
        ctx.fillStyle = "white";
        ctx.font = `${canvas.width * 0.08}px Arial`;
        ctx.fillText("Game Over", canvas.width / 2 - canvas.width * 0.2, canvas.height / 2);
        ctx.font = `${canvas.width * 0.05}px Arial`;
        ctx.fillText(`Final Score: ${score}`, canvas.width / 2 - canvas.width * 0.15, canvas.height / 2 + canvas.height * 0.05);
      }
    }

    // Touch controls
    canvas.addEventListener("touchstart", (e) => {
      touchStartX = e.touches[0].clientX;
    });

    canvas.addEventListener("touchend", (e) => {
      touchEndX = e.changedTouches[0].clientX;
      const deltaX = touchEndX - touchStartX;

      if (deltaX > 50 && player.x + player.width < canvas.width) {
        player.x += player.speed;
      } else if (deltaX < -50 && player.x > 0) {
        player.x -= player.speed;
      }
    });

    // Game loop
    function gameLoop() {
      updateGame();
      drawGame();
      if (!isGameOver) {
        requestAnimationFrame(gameLoop);
      }
    }

    // Add obstacles at intervals
    setInterval(createObstacle, 1000);
    gameLoop();
  </script>
</body>
</html>
