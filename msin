<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>祝妈妈生日快乐</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            background: linear-gradient(135deg, #ff9a9e 0%, #fecfef 50%, #fecfef 100%);
            overflow: hidden;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .container {
            position: relative;
            width: 100%;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .title {
            position: absolute;
            top: 10%;
            font-size: 2.5rem;
            color: #8b005d;
            text-align: center;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
            z-index: 10;
        }

        /* 礼物盒样式 */
        .gift-box {
            position: relative;
            width: 300px;
            height: 250px;
            cursor: pointer;
            transition: transform 0.3s ease;
            z-index: 5;
            transform-style: preserve-3d;
        }

        .gift-box:hover {
            transform: scale(1.05) rotateY(5deg);
        }

        .gift-top {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 60px;
            background: linear-gradient(45deg, #ff6b6b, #ee5a52);
            border: 3px solid #e74c3c;
            border-radius: 5px 5px 0 0;
            z-index: 2;
            transition: all 0.5s ease;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3), inset 0 2px 4px rgba(255, 255, 255, 0.3);
            transform-origin: bottom center;
        }

        .gift-box.open .gift-top {
            transform: translateY(-100%) rotateX(180deg);
        }

        .gift-ribbon-horizontal {
            position: absolute;
            top: 20px;
            left: 0;
            width: 100%;
            height: 20px;
            background: linear-gradient(90deg, #fff, #f8f9fa);
            z-index: 3;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
        }

        .gift-ribbon-vertical {
            position: absolute;
            top: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 20px;
            height: 100%;
            background: linear-gradient(180deg, #fff, #f8f9fa);
            z-index: 3;
            box-shadow: 2px 0 4px rgba(0, 0, 0, 0.2);
        }

        .gift-bottom {
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 190px;
            background: linear-gradient(45deg, #ff6b6b, #ee5a52);
            border: 3px solid #e74c3c;
            border-radius: 0 0 5px 5px;
            z-index: 1;
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.3), inset 0 -2px 4px rgba(255, 255, 255, 0.3);
        }

        /* 礼物盒底部阴影 */
        .gift-box::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 80%;
            height: 20px;
            background: rgba(0, 0, 0, 0.3);
            border-radius: 50%;
            z-index: 0;
            filter: blur(10px);
        }

        /* 祝福话语样式 */
        .wishes {
            position: absolute;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: 10;
        }

        .wish {
            position: absolute;
            font-size: 1.2rem;
            font-weight: bold;
            color: #8b005d;
            text-align: center;
            padding: 12px 20px;
            background: linear-gradient(135deg, #fff, #f8f9fa);
            border: 3px solid #ff6b6b;
            border-radius: 25px;
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.3), 0 0 10px rgba(255, 107, 107, 0.5);
            opacity: 0;
            animation: float 3s ease-out forwards;
            max-width: 200px;
            word-wrap: break-word;
        }

        /* 对话框小三角 */
        .wish::after {
            content: '';
            position: absolute;
            bottom: -8px;
            left: 50%;
            transform: translateX(-50%) rotate(45deg);
            width: 16px;
            height: 16px;
            background: linear-gradient(135deg, #fff, #f8f9fa);
            border-right: 3px solid #ff6b6b;
            border-bottom: 3px solid #ff6b6b;
            z-index: -1;
        }

        @keyframes float {
            0% {
                transform: translate(-50%, -50%) scale(0);
                opacity: 0;
            }
            20% {
                opacity: 1;
                transform: translate(-50%, -50%) scale(1.1);
            }
            50% {
                transform: translate(-50%, calc(-50% - 30px)) scale(1);
            }
            100% {
                transform: translate(calc(-50% + var(--dx, 0px)), calc(-50% - var(--dy, 150px))) scale(1);
                opacity: 0;
            }
        }

        /* 装饰气球 */
        .balloon {
            position: absolute;
            width: 60px;
            height: 80px;
            border-radius: 50% 50% 50% 50% / 60% 60% 40% 40%;
            animation: float-up 6s ease-in-out infinite;
            opacity: 0.8;
        }

        .balloon::before {
            content: '';
            position: absolute;
            bottom: -15px;
            left: 50%;
            transform: translateX(-50%);
            width: 2px;
            height: 20px;
            background: #333;
        }

        @keyframes float-up {
            0%, 100% {
                transform: translateY(0) rotate(5deg);
            }
            50% {
                transform: translateY(-20px) rotate(-5deg);
            }
        }

        /* 响应式设计 */
        @media (max-width: 768px) {
            .title {
                font-size: 2rem;
            }
            
            .gift-box {
                width: 250px;
                height: 200px;
            }
            
            .gift-top {
                height: 50px;
            }
            
            .gift-bottom {
                height: 150px;
            }
        }

        @media (max-width: 480px) {
            .title {
                font-size: 1.5rem;
            }
            
            .gift-box {
                width: 200px;
                height: 160px;
            }
            
            .gift-top {
                height: 40px;
            }
            
            .gift-bottom {
                height: 120px;
            }
            
            .gift-ribbon-horizontal,
            .gift-ribbon-vertical {
                width: 15px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1 class="title">祝妈妈生日快乐！</h1>
        
        <!-- 礼物盒 -->
        <div class="gift-box" id="giftBox">
            <div class="gift-top">
                <div class="gift-ribbon-horizontal"></div>
                <div class="gift-ribbon-vertical"></div>
            </div>
            <div class="gift-bottom">
                <div class="gift-ribbon-vertical"></div>
            </div>
        </div>
        
        <!-- 祝福话语容器 -->
        <div class="wishes" id="wishes"></div>
    </div>

    <script>
        // 祝福话语列表
        const wishMessages = [
            '妈妈生日快乐！',
            '身体健康，永远年轻！',
            '我爱您！',
            '天天开心！',
            '万事如意！',
            '永远美丽！',
            '幸福美满！',
            '笑口常开！',
            '平安喜乐！',
            '心想事成！'
        ];

        // 创建装饰气球
        function createBalloons() {
            const colors = ['#ff6b6b', '#4ecdc4', '#45b7d1', '#96ceb4', '#ffeaa7', '#dda0dd'];
            const container = document.querySelector('.container');
            
            for (let i = 0; i < 10; i++) {
                const balloon = document.createElement('div');
                balloon.className = 'balloon';
                balloon.style.background = colors[Math.floor(Math.random() * colors.length)];
                balloon.style.left = Math.random() * 100 + '%';
                balloon.style.bottom = Math.random() * 20 + '%';
                balloon.style.animationDelay = Math.random() * 3 + 's';
                container.appendChild(balloon);
            }
        }

        // 生成随机祝福话语
        function generateWish() {
            const wish = document.createElement('div');
            wish.className = 'wish';
            wish.textContent = wishMessages[Math.floor(Math.random() * wishMessages.length)];
            
            // 随机位置和动画参数
            const x = Math.random() * window.innerWidth;
            const y = Math.random() * window.innerHeight;
            const dx = (Math.random() - 0.5) * 200;
            const dy = Math.random() * 150 + 100;
            
            wish.style.left = x + 'px';
            wish.style.top = y + 'px';
            wish.style.setProperty('--dx', dx + 'px');
            wish.style.setProperty('--dy', dy + 'px');
            wish.style.animationDelay = Math.random() * 0.5 + 's';
            
            return wish;
        }

        // 点击礼物盒事件
        document.getElementById('giftBox').addEventListener('click', function() {
            this.classList.add('open');
            
            // 生成多个祝福话语
            const wishesContainer = document.getElementById('wishes');
            for (let i = 0; i < 20; i++) {
                const wish = generateWish();
                wishesContainer.appendChild(wish);
                
                // 动画结束后移除元素
                setTimeout(() => {
                    wish.remove();
                }, 3000);
            }
        });

        // 初始化
        createBalloons();
    </script>
</body>
</html>
