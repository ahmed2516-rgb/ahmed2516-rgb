```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Balloons on Click</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div id="container">
        <a href="#" id="balloon-link" onclick="addBalloons()">Click me to add balloons!</a>
    </div>
    <script src="script.js"></script>
</body>
</html>
```
```css
#container {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
}

.balloon {
    position: absolute;
    width: 50px;
    height: 50px;
    background-color: #ffcccc;
    border-radius: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 24px;
    color: #333;
    box-shadow: 0 0 5px rgba(0, 0, 0, 0.5);
    animation: bounce 2s infinite ease-in-out;
}

@keyframes bounce {
    0%, 20%, 50%, 80%, 100% {
        transform: translateY(0);
    }
    40% {
        transform: translateY(-30px);
    }
    60% {
        transform: translateY(-15px);
    }
}
```
    
    for (let i = 0; i < numberOfBalloons; i++) {
        const balloon = document.createElement('div');
        balloon.classList.add('balloon');
        balloon.textContent = '🎈';
        container.appendChild(balloon);
        
        // Add some randomness to the position and size of the balloons
        balloon.style.left = `${Math.random() * window.innerWidth}px`;
        balloon.style.top = `${Math.random() * window.innerHeight}px`;
        balloon.style.width = `${Math.random() * 100}px`;
        balloon.style.height = `${Math.random() * 100}px`;
    }
}
```
