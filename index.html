<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<title>Giải Cứu Công Chúa</title>
<style>
    body {
        margin: 0;
        background: linear-gradient(#87ceeb, #e0f7ff);
        text-align: center;
        font-family: Arial, sans-serif;
    }
    canvas {
        background: #9be7ff;
        border: 4px solid #333;
        display: block;
        margin: auto;
    }
    button {
        padding: 10px 25px;
        font-size: 18px;
        margin: 10px;
        cursor: pointer;
    }
</style>
</head>
<body>

<h1>🏃‍♂️ GIẢI CỨU CÔNG CHÚA 👑</h1>
<p>SPACE: nhảy | SPACE x2: nhảy cao</p>

<button id="startBtn">▶ BẮT ĐẦU</button>
<button id="restartBtn" style="display:none;">🔁 CHƠI LẠI</button>
<button id="nextBtn" style="display:none;">🔥 CHƠI TIẾP (KHÓ HƠN)</button>

<canvas id="game" width="1000" height="450"></canvas>

<script>
const canvas = document.getElementById("game");
const ctx = canvas.getContext("2d");

const startBtn = document.getElementById("startBtn");
const restartBtn = document.getElementById("restartBtn");
const nextBtn = document.getElementById("nextBtn");

let gameRunning = false;
let gameOver = false;
let win = false;

let level = 1;
let speed = 5;
let distance = 0;
let targetDistance = 2000;

// ================= HERO =================
const hero = {
    x: 120, y: 300, w: 40, h: 60,
    vy: 0,
    jumpCount: 0,
    maxJump: 2
};

// ================= OBSTACLES =================
const obstacleTypes = ["rock", "spike", "hole"];
let obstacles = [];

document.addEventListener("keydown", e => {
    if (e.code === "Space" && gameRunning && !gameOver) {
        if (hero.jumpCount < hero.maxJump) {
            hero.vy = hero.jumpCount === 0 ? -16 : -20; // nhảy lần 2 cao hơn
            hero.jumpCount++;
        }
    }
});

// ================= BUTTONS =================
startBtn.onclick = () => {
    level = 1;
    speed = 5;
    targetDistance = 2000;
    resetGame();
    gameRunning = true;
    startBtn.style.display = "none";
};

restartBtn.onclick = () => {
    resetGame();
    gameRunning = true;
    restartBtn.style.display = "none";
};

nextBtn.onclick = () => {
    level++;
    speed += 0.8;
    targetDistance += 900;
    resetGame();
    gameRunning = true;
    nextBtn.style.display = "none";
};

// ================= GAME SETUP =================
function createObstacle(x) {
    return {
        x,
        y: 340,
        w: 40,
        h: 40,
        type: obstacleTypes[Math.floor(Math.random() * obstacleTypes.length)]
    };
}

function initObstacles() {
    obstacles = [];
    let baseGap = 520 - level * 30;   // GIÃN XA
    if (baseGap < 350) baseGap = 350;

    let count = 3 + Math.floor(level / 2);
    let x = 1000;

    for (let i = 0; i < count; i++) {
        obstacles.push(createObstacle(x));
        x += baseGap + Math.random() * 200;
    }
}

function resetGame() {
    gameOver = false;
    win = false;
    distance = 0;
    hero.y = 300;
    hero.vy = 0;
    hero.jumpCount = 0;
    initObstacles();
}

// ================= UPDATE =================
function update() {
    if (!gameRunning || gameOver) return;

    hero.y += hero.vy;
    hero.vy += 1;

    if (hero.y >= 300) {
        hero.y = 300;
        hero.vy = 0;
        hero.jumpCount = 0; // chạm đất reset jump
    }

    obstacles.forEach(ob => {
        ob.x -= speed;

        if (ob.x < -80) {
            ob.x = 1000 + Math.random() * 600;
            ob.type = obstacleTypes[Math.floor(Math.random() * obstacleTypes.length)];
        }

        if (
            hero.x < ob.x + ob.w &&
            hero.x + hero.w > ob.x &&
            hero.y < ob.y + ob.h &&
            hero.y + hero.h > ob.y
        ) {
            gameOver = true;
            restartBtn.style.display = "inline-block";
        }
    });

    distance++;
    if (distance >= targetDistance) {
        win = true;
        gameOver = true;
        nextBtn.style.display = "inline-block";
    }
}

// ================= DRAW =================
function drawRoad() {
    ctx.fillStyle = "#3b7a1c";
    ctx.fillRect(0, 330, canvas.width, 20);
    ctx.fillStyle = "#6b3e26";
    ctx.fillRect(0, 350, canvas.width, 100);
}

function drawHero() {
    ctx.fillStyle = "#ff4d4d";
    ctx.fillRect(hero.x, hero.y, hero.w, hero.h);
    ctx.fillStyle = "#ffe0bd";
    ctx.beginPath();
    ctx.arc(hero.x + 20, hero.y - 10, 15, 0, Math.PI * 2);
    ctx.fill();
}

function drawObstacle(ob) {
    if (ob.type === "rock") {
        ctx.fillStyle = "#555";
        ctx.beginPath();
        ctx.arc(ob.x + 20, ob.y + 20, 20, 0, Math.PI * 2);
        ctx.fill();
    }
    if (ob.type === "spike") {
        ctx.fillStyle = "#333";
        ctx.beginPath();
        ctx.moveTo(ob.x, ob.y + 40);
        ctx.lineTo(ob.x + 20, ob.y);
        ctx.lineTo(ob.x + 40, ob.y + 40);
        ctx.fill();
    }
    if (ob.type === "hole") {
        ctx.fillStyle = "#000";
        ctx.ellipse(ob.x + 20, ob.y + 40, 25, 10, 0, 0, Math.PI * 2);
        ctx.fill();
    }
}

function draw() {
    ctx.clearRect(0, 0, canvas.width, canvas.height);

    drawRoad();
    drawHero();
    obstacles.forEach(drawObstacle);

    ctx.fillStyle = "#000";
    ctx.font = "18px Arial";
    ctx.fillText("Level: " + level, 20, 25);
    ctx.fillText("Distance: " + distance + " / " + targetDistance, 20, 50);

    if (!gameRunning) {
        ctx.font = "32px Arial";
        ctx.fillText("NHẤN BẮT ĐẦU ĐỂ CHƠI", 320, 220);
    }

    if (gameOver) {
        ctx.fillStyle = "rgba(0,0,0,0.7)";
        ctx.fillRect(0, 0, canvas.width, canvas.height);
        ctx.fillStyle = "#fff";
        ctx.font = "36px Arial";

        if (win) {
            ctx.fillText("🎉 HOÀN THÀNH LEVEL " + level + " 🎉", 260, 220);
        } else {
            ctx.fillText("💥 GAME OVER 💥", 380, 220);
        }
    }
}

// ================= LOOP =================
function loop() {
    update();
    draw();
    requestAnimationFrame(loop);
}
loop();
</script>

</body>
</html>
