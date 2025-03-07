<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chúc Mừng 8/3</title>
    <style>
        body {
            margin: 0;
            overflow: hidden;
            background-color: #ffebf0;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            height: 100vh;
            font-family: Arial, sans-serif;
            text-align: center;
        }
        .message {
            font-size: 2rem;
            color: #e6005c;
            font-weight: bold;
            white-space: nowrap;
            overflow: hidden;
            border-right: 4px solid;
            width: 0;
            animation: typing 3s steps(30) forwards, blink 0.7s infinite;
        }
        .sub-message {
            font-size: 1.5rem;
            color: #333;
            margin-top: 20px;
            opacity: 0;
            animation: fadeIn 5s ease-in-out forwards;
        }
        @keyframes typing {
            to { width: 100%; }
        }
        @keyframes blink {
            50% { border-color: transparent; }
        }
        @keyframes fadeIn {
            0% { opacity: 0; }
            100% { opacity: 1; }
        }
        .heart {
            position: absolute;
            width: 20px;
            height: 20px;
            background-color: red;
            clip-path: polygon(50% 0%, 100% 35%, 80% 100%, 50% 75%, 20% 100%, 0% 35%);
            opacity: 0.7;
            animation: fall linear infinite;
        }
        @keyframes fall {
            from { transform: translateY(-100px); opacity: 1; }
            to { transform: translateY(100vh); opacity: 0; }
        }
        .button {
            margin-top: 30px;
            padding: 10px 20px;
            font-size: 1.2rem;
            background-color: #ff4081;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: background 0.3s;
        }
        .button:hover {
            background-color: #e6005c;
        }
    </style>
</head>
<body>
    <div class="message">Chúc mừng ngày Quốc tế Phụ nữ 8/3!</div>
    <div class="sub-message">Chúc bạn luôn xinh đẹp, hạnh phúc và thành công!</div>
    <button class="button" onclick="showWish()">Nhận lời chúc đặc biệt</button>
    
    <script>
        function createHeart() {
            const heart = document.createElement("div");
            heart.classList.add("heart");
            heart.style.left = Math.random() * window.innerWidth + "px";
            heart.style.animationDuration = Math.random() * 3 + 2 + "s";
            document.body.appendChild(heart);
            setTimeout(() => heart.remove(), 5000);
        }
        setInterval(createHeart, 300);
        
        function showWish() {
            alert("Chúc bạn có một ngày 8/3 tràn đầy niềm vui, yêu thương và những điều tuyệt vời nhất!");
        }
    </script>
</body>
</html>
