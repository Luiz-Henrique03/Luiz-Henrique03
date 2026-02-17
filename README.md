# 🚀 Luiz Henrique da Silva Oliveira  

🎓 Computer Science Student  
💼 Full Developer at Policorp Tecnologia  
📍 Curitiba - PR, Brazil  

---

## 👨‍💻 About Me

I am a Full Developer focused on desktop and backend solutions, with strong experience in:

- C# and .NET ecosystem  
- WPF applications  
- Windows environment and system integration  
- Microsoft Store packaging and publishing  
- Process automation and enterprise internal tools  

Passionate about building reliable software and solving real-world problems.

---

## 🛠 Tech Stack

### 💻 Main Languages
C • C++ • C# • Python • Java  

### ⚙️ Frameworks & Platforms
.NET • WPF • Windows • Linux  

### 🔧 Tools & DevOps
Visual Studio • VS Code • Git • GitHub • Docker • Jenkins • Proxmox  

### 🗄 Databases
MySQL • MongoDB  

---

## 📈 GitHub Stats

![Luiz GitHub Stats](https://github-readme-stats.vercel.app/api?username=Luiz-Henrique03&show_icons=true&theme=dark&hide_border=true)

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=Luiz-Henrique03&layout=compact&theme=dark&hide_border=true)

---

# 🐍 Snake Game (Play Here)

> Use the arrow keys to play!

<div align="center">
  <canvas id="snake" width="400" height="400" style="background-color:#0d1117; border:2px solid #00bfbf;"></canvas>
</div>

<script>
const canvas = document.getElementById("snake");
const ctx = canvas.getContext("2d");

const box = 20;
let snake = [{ x: 9 * box, y: 10 * box }];
let direction = null;
let food = {
  x: Math.floor(Math.random() * 19 + 1) * box,
  y: Math.floor(Math.random() * 19 + 1) * box
};

document.addEventListener("keydown", event => {
  if (event.key === "ArrowLeft" && direction !== "RIGHT") direction = "LEFT";
  if (event.key === "ArrowUp" && direction !== "DOWN") direction = "UP";
  if (event.key === "ArrowRight" && direction !== "LEFT") direction = "RIGHT";
  if (event.key === "ArrowDown" && direction !== "UP") direction = "DOWN";
});

function draw() {
  ctx.fillStyle = "#0d1117";
  ctx.fillRect(0, 0, 400, 400);

  for (let i = 0; i < snake.length; i++) {
    ctx.fillStyle = i === 0 ? "#00bfbf" : "#15e5a6";
    ctx.fillRect(snake[i].x, snake[i].y, box, box);
  }

  ctx.fillStyle = "red";
  ctx.fillRect(food.x, food.y, box, box);

  let snakeX = snake[0].x;
  let snakeY = snake[0].y;

  if (direction === "LEFT") snakeX -= box;
  if (direction === "UP") snakeY -= box;
  if (direction === "RIGHT") snakeX += box;
  if (direction === "DOWN") snakeY += box;

  if (
    snakeX === food.x &&
    snakeY === food.y
  ) {
    food = {
      x: Math.floor(Math.random() * 19 + 1) * box,
      y: Math.floor(Math.random() * 19 + 1) * box
    };
  } else {
    snake.pop();
  }

  let newHead = { x: snakeX, y: snakeY };

  if (
    snakeX < 0 || snakeY < 0 ||
    snakeX >= 400 || snakeY >= 400 ||
    snake.some(segment => segment.x === snakeX && segment.y === snakeY)
  ) {
    clearInterval(game);
    alert("Game Over 😅");
  }

  snake.unshift(newHead);
}

let game = setInterval(draw, 100);
</script>

---

## 📫 Contact

🔗 LinkedIn  
https://www.linkedin.com/in/luiz-henrique-s-b05363226/

---

⭐ If you like technology, system development and problem solving — feel free to connect!
