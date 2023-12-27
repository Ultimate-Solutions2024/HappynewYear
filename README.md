<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <title>احتفال بالسنة الجديدة</title>
    <style>
        body {
            margin: 0;
            overflow: hidden;
            background-color: #283A97;
        }

        #fireworks {
            position: absolute;
            width: 100%;
            height: 100%;
            z-index: 1;
        }

        #message {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            font-family: Arial, sans-serif;
            font-size: 24px;
            text-align: center;
            color: white;
            z-index: 2;
            display: none;
        }
    </style>
</head>
<body>
    <div id="fireworks"></div>
    <div id="message">
        نجاحنا من نجاحكم<br>
        مستمرون بكم<br>
        كل عام وانتم بخير<br>
        2024
    </div>

    <script>
        // Function to create fireworks
        function createFirework() {
            let firework = document.createElement('div');
            firework.className = 'firework';
            firework.style.left = `${Math.random() * 100}vw`;
            firework.style.animationDuration = `${Math.random() * 2 + 1}s`;
            document.getElementById('fireworks').appendChild(firework);

            setTimeout(() => {
                firework.remove();
            }, 5000);
        }

        // Function to create balloons
        function createBalloons() {
            let balloon = document.createElement('div');
            balloon.className = 'balloon';
            balloon.style.left = `${Math.random() * 100}vw`;
            balloon.style.animationDuration = `${Math.random() * 5 + 3}s`;
            document.getElementById('fireworks').appendChild(balloon);

            setTimeout(() => {
                balloon.remove();
            }, 8000);
        }

        // Function to show the message after 5 seconds
        setTimeout(() => {
            document.getElementById('message').style.display = 'block';
        }, 5000);

        // Trigger fireworks and balloons at intervals
        setInterval(createFirework, 800);
        setInterval(createBalloons, 2000);
    </script>
</body>
</html>
