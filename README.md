<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Christmas Tree</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background: linear-gradient(to bottom, #00111a, #004466);
            overflow: hidden;
        }
        .tree {
            position: relative;
            width: 0;
            height: 0;
            border-left: 60px solid transparent;
            border-right: 60px solid transparent;
            border-bottom: 100px solid green;
            animation: glow 2s infinite alternate;
        }
        .tree:before {
            content: '';
            position: absolute;
            top: -80px;
            left: -40px;
            width: 0;
            height: 0;
            border-left: 50px solid transparent;
            border-right: 50px solid transparent;
            border-bottom: 80px solid green;
        }
        .tree:after {
            content: '';
            position: absolute;
            top: -140px;
            left: -30px;
            width: 0;
            height: 0;
            border-left: 40px solid transparent;
            border-right: 40px solid transparent;
            border-bottom: 60px solid green;
        }
        .trunk {
            position: relative;
            top: -20px;
            width: 20px;
            height: 30px;
            background: #8B4513;
            margin: 0 auto;
        }
        .lights {
            position: absolute;
            top: 0;
            left: -20px;
            width: 140px;
            height: 160px;
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            align-items: flex-start;
            pointer-events: none;
        }
        .light {
            width: 10px;
            height: 10px;
            margin: 5px;
            background: red;
            border-radius: 50%;
            box-shadow: 0 0 10px red;
            animation: twinkle 1.5s infinite alternate;
        }
        .light:nth-child(odd) {
            background: yellow;
            box-shadow: 0 0 10px yellow;
            animation-duration: 2s;
        }
        .light:nth-child(3n) {
            background: blue;
            box-shadow: 0 0 10px blue;
            animation-duration: 2.5s;
        }
        @keyframes glow {
            from {
                filter: brightness(1);
            }
            to {
                filter: brightness(1.5);
            }
        }
        @keyframes twinkle {
            from {
                opacity: 0.7;
                transform: scale(1);
            }
            to {
                opacity: 1;
                transform: scale(1.2);
            }
        }
    </style>
</head>
<body>
    <div>
        <div class="tree">
            <div class="lights">
                <!-- Tạo các bóng đèn -->
                <div class="light"></div>
                <div class="light"></div>
                <div class="light"></div>
                <div class="light"></div>
                <div class="light"></div>
                <div class="light"></div>
                <div class="light"></div>
                <div class="light"></div>
                <div class="light"></div>
                <div class="light"></div>
            </div>
        </div>
        <div class="trunk"></div>
    </div>
</body>
</html>
