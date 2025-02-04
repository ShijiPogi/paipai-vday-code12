<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>us. valentines. 14?</title>
    <style>
        body {
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: pink;
            font-family: Arial, sans-serif;
            text-align: center;
            overflow: hidden;
        }
        h1 {
            font-size: 2.5rem;
            color: white;
            text-shadow: 2px 2px 4px #ff007f;
        }
        .buttons {
            margin-top: 20px;
            position: relative;
            width: 100%;
            height: 100px;
        }
        button {
            font-size: 1.5rem;
            padding: 10px 20px;
            margin: 10px;
            border: none;
            cursor: pointer;
            border-radius: 10px;
        }
        .yes {
            background-color: red;
            color: white;
        }
        .no-button {
            background-color: white;
            color: red;
            position: absolute;
        }
        @keyframes hearts {
            0% { transform: translateY(0); opacity: 1; }
            100% { transform: translateY(-100vh); opacity: 0; }
        }
        .heart {
            position: absolute;
            color: red;
            font-size: 2rem;
            animation: hearts 3s linear infinite;
        }
    </style>
</head>
<body>
    <h1>be jungkook's valentines! ❤️</h1>
    <div class="buttons">
        <button class="yes" onclick="acceptLove()">Yes!</button>
        <button class="no-button" id="noButton" onmouseover="moveNo()">No 😢</button>
    </div>

    <script>
        function acceptLove() {
            document.body.innerHTML = '<h1>mwehehehe yehey ni agree si paipai </h1>';
        }
        function moveNo() {
            const button = document.getElementById("noButton");
            const x = Math.random() * (window.innerWidth - 100);
            const y = Math.random() * (window.innerHeight - 50);
            button.style.left = `${x}px`;
            button.style.top = `${y}px`;
        }
        function createHearts() {
            const heart = document.createElement("div");
            heart.classList.add("heart");
            heart.innerHTML = "❤️";
            heart.style.left = Math.random() * window.innerWidth + "px";
            heart.style.top = window.innerHeight + "px";
            document.body.appendChild(heart);
            setTimeout(() => heart.remove(), 3000);
        }
        setInterval(createHearts, 500);
    </script>
</body>
</html>
