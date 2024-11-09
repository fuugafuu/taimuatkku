# taimuatkku
<title>算数タイムアタックゲーム</title> <style> body { font-family: Arial, sans-serif; text-align: center; margin-top: 50px; } .question { font-size: 24px; margin: 20px 0; } input[type="text"] { padding: 5px; font-size: 18px; width: 60px; } button { padding: 10px 20px; font-size: 16px; cursor: point; } .result { font-size: 20px; margin-top: 20px; } .timer { font-size: 30px; color: red; margin-bottom: 20px; } .score { font-size: 20px; margin-top: 20px; } #retryButton { display: none; margin-top: 20px; } .ranking { margin-top: 30px; } .ranking h2 { font-size: 24px; } .ranking ol { text-align: left; list-style-type: decimal; padding-left: 20px; } </style>
<h1>算数タイムアタックゲーム</h1>
<p>制限時間内にできるだけ多くの問題を解こう！</p>

<div>
    <label for="gameTime">ゲームの時間（秒）:</label>
    <input type="number" id="gameTime" min="10" max="300" value="30">
    <button id="startButton" onclick="startGame()">スタート</button>
</div>

<div id="timer" class="timer">30</div>

<div id="problem" class="question">スタートボタンを押してゲームを開始してください。</div>

<input type="text" id="answer" placeholder="答えを入力" disabled/>

<button id="retryButton" onclick="startGame()">リトライ</button>

<div id="result" class="result"></div>
<div id="score" class="score">得点: 0</div>

<div class="ranking">
    <h2>ランキング</h2>
    <ol id="rankingList"></ol>
</div>

<script>
    let num1, num2, correctAnswer, operator;
    let score = 0;
    let timeLeft = 30;
    let timerInterval;
    let gameOver = false;

    function loadRanking() {
        const ranking = JSON.parse(localStorage.getItem('ranking')) || [];
        ranking.sort((a, b) => b.score - a.score);
        const rankingList = document.getElementById("rankingList");
        rankingList.innerHTML = "";
        ranking.slice(0, 10).forEach((entry, index) => {
            const li = document.createElement("li");
            li.textContent = `第${index + 1}位: ${entry.name} - ${entry.score}点`;
            rankingList.appendChild(li);
        });
    }

    window.onload = loadRanking;

    function startGame() {
        const gameTimeInput = document.getElementById("gameTime");
        const inputTime = parseInt(gameTimeInput.value, 10);
        if (isNaN(inputTime) || inputTime < 10 || inputTime > 300) {
            alert("ゲームの時間を10秒以上300秒以下で設定してください。");
            return;
        }

        score = 0;
        timeLeft = inputTime;
        gameOver = false;
        document.getElementById("score").textContent = `得点: ${score}`;
        document.getElementById("answer").disabled = false;
        document.getElementById("startButton").style.display = "none";
        document.getElementById("retryButton").style.display = "none";
        document.getElementById("timer").textContent = timeLeft;
        generateProblem();
        timerInterval = setInterval(updateTimer, 1000);
    }

    function generateProblem() {
        const operators = ['+', '-', '*'];
        operator = operators[Math.floor(Math.random() * operators.length)];
        num1 = Math.floor(Math.random() * 100) + 1;
        num2 = Math.floor(Math.random() * 100) + 1;
        if (operator === '+') {
            correctAnswer = num1 + num2;
        } else if (operator === '-') {
            correctAnswer = num1 - num2;
        } else if (operator === '*') {
            correctAnswer = num1 * num2;
        }
        document.getElementById("problem").textContent = `${num1} ${operator} ${num2} = ?`;
        document.getElementById("result").textContent = "";
    }

    function updateTimer() {
        if (timeLeft <= 0) {
            clearInterval(timerInterval);
            gameOver = true;
            document.getElementById("timer").textContent = "時間終了！";
            document.getElementById("retryButton").style.display = "block";
            document.getElementById("answer").disabled = true;
            saveScore();
        } else {
            document.getElementById("timer").textContent = --timeLeft;
        }
    }

    function checkAnswer() {
        const answer = parseInt(document.getElementById("answer").value, 10);
        if (isNaN(answer)) return;

        if (answer === correctAnswer) {
            score++;
            document.getElementById("score").textContent = `得点: ${score}`;
            generateProblem();
        } else {
            document.getElementById("result").textContent = `不正解！ 正しい答えは ${correctAnswer} です。`;
        }

        document.getElementById("answer").value = '';
    }

    document.getElementById("answer").addEventListener("keypress", function(event) {
        if (event.key === "Enter") {
            checkAnswer();
        }
    });

    function saveScore() {
        const playerName = prompt("名前を入力してください:");
        if (!playerName) return;

        const ranking = JSON.parse(localStorage.getItem('ranking')) || [];
        ranking.push({ name: playerName, score: score });
        localStorage.setItem('ranking', JSON.stringify(ranking));

        loadRanking();
    }
</script>
