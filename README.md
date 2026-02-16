# my-website
my-website/
├── index.html
├── style.css
└── script.js
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Interactive Greeting</title>
<link rel="stylesheet" href="style.css">
</head>
<body>
  <h1 id="greeting">Hello, visitor! 👋</h1>
  <button onclick="changeBackground()">Click me for colors!</button>

  <script src="script.js"></script>
</body>
</html>
body {
  font-family: 'Arial', sans-serif;
  text-align: center;
  background: linear-gradient(135deg, #ff9a9e, #fad0c4);
  transition: background 0.5s;
  color: #333;
}

h1 {
  margin-top: 50px;
  font-size: 3em;
}

button {
  padding: 15px 30px;
  margin-top: 30px;
  font-size: 1.2em;
  border: none;
  border-radius: 10px;
  cursor: pointer;
  background-color: #ff6f91;
  color: white;
  transition: transform 0.2s;
}

button:hover {
  transform: scale(1.1);
}
function changeBackground() {
  const colors = [
    'linear-gradient(135deg, #ff9a9e, #fad0c4)',
    'linear-gradient(135deg, #a1c4fd, #c2e9fb)',
    'linear-gradient(135deg, #fbc2eb, #a6c1ee)',
    'linear-gradient(135deg, #fdcbf1, #e6dee9)',
    'linear-gradient(135deg, #84fab0, #8fd3f4)'
  ];
  const randomColor = colors[Math.floor(Math.random() * colors.length)];
  document.body.style.background = randomColor;
}

