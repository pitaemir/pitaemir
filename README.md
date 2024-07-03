body {
    font-family: 'Arial', sans-serif;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-color: #f0f0f0;
}

.animation-container {
    position: relative;
    width: 600px;
    height: 400px;
    background-color: #fff;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    overflow: hidden;
}

.frame {
    position: absolute;
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    font-size: 24px;
    opacity: 0;
    transition: opacity 1s ease-in-out;
}

#frame2, #frame3, #frame4 {
    font-size: 20px;
}

ul {
    list-style: none;
    padding: 0;
}

ul li {
    margin: 5px 0;
}

const frames = document.querySelectorAll('.frame');
let currentFrame = 0;

function showNextFrame() {
    frames[currentFrame].style.opacity = '0';
    currentFrame = (currentFrame + 1) % frames.length;
    frames[currentFrame].style.opacity = '1';
}

setInterval(showNextFrame, 3000);
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Animated Profile</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="animation-container">
        <div class="frame" id="frame1">Meet Emir Bráz</div>
        <div class="frame" id="frame2">
            <p>Currently studying at the</p>
            <p>Federal University of Santa Catarina</p>
            <p>Computer Engineering</p>
        </div>
        <div class="frame" id="frame3">
            <p>Interests</p>
            <ul>
                <li>Hardware</li>
                <li>Semiconductor</li>
                <li>Silicon</li>
                <li>Game Developing</li>
                <li>Backend Developing</li>
            </ul>
        </div>
        <div class="frame" id="frame4">Future Innovator in Technology</div>
    </div>

    <script src="script.js"></script>
</body>
</html>


