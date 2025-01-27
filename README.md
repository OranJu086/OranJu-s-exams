<!DOCTYPE html>
<html lang="zh">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>新年快乐</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            background-color: #FF0000;
            font-family: "Microsoft YaHei", "微软雅黑", sans-serif;
            overflow: hidden;
        }

        .greeting {
            color: #FFD700;
            font-size: 4em;
            font-weight: bold;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
            position: relative;
            animation: floating 5s ease-in-out infinite;
        }

        @keyframes floating {
            0% {
                transform: translate(0, 0) rotate(0deg);
            }
            25% {
                transform: translate(50px, 30px) rotate(5deg);
            }
            50% {
                transform: translate(-30px, -20px) rotate(-5deg);
            }
            75% {
                transform: translate(-50px, 40px) rotate(3deg);
            }
            100% {
                transform: translate(0, 0) rotate(0deg);
            }
        }

        .container {
            height: 200vh;
            overflow-y: auto;
            scroll-snap-type: y mandatory;
        }

        .page {
            height: 100vh;
            scroll-snap-align: start;
            position: relative;
            display: flex;
            justify-content: center;
            align-items: center;
            background-color: #FF0000;
        }

        .scroll-arrow {
            position: absolute;
            bottom: 40px;
            left: 50%;
            transform: translateX(-50%);
            color: #FFD700;
            font-size: 1.5em;
            animation: bounce 2s infinite;
            cursor: pointer;
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .arrow {
            width: 20px;
            height: 20px;
            border-left: 3px solid #FFD700;
            border-bottom: 3px solid #FFD700;
            transform: rotate(-45deg);
            margin-bottom: 10px;
        }

        .scroll-text {
            font-size: 0.8em;
            text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.3);
        }

        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% {
                transform: translateY(0) translateX(-50%);
            }
            40% {
                transform: translateY(-20px) translateX(-50%);
            }
            60% {
                transform: translateY(-10px) translateX(-50%);
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="page">
            <div class="greeting">新年快乐</div>
            <div class="scroll-arrow">
                <div class="arrow"></div>
                <div class="scroll-text">向上滑动</div>
            </div>
        </div>
        <div class="page">
            <div class="greeting">蛇年大吉</div>
        </div>
    </div>
</body>
</html> 
