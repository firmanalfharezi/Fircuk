# Fircuk
Game Gaja
const box = document.getElementById("box");
const scoreText = document.getElementById("score");

let score = 0;

function moveBox() {
  const area = document.getElementById("gameArea");
  const maxX = area.clientWidth - box.clientWidth;
  const maxY = area.clientHeight - box.clientHeight;

  const x = Math.random() * maxX;
  const y = Math.random() * maxY;

  box.style.left = x + "px";
  box.style.top = y + "px";
}

box.addEventListener("click", () => {
  score++;
  scoreText.textContent = score;
  moveBox();
});

moveBox();
