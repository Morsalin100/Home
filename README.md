
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Welcome Page</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background: linear-gradient(to right, #00c6ff, #0072ff);
      height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      overflow: hidden;
      font-family: 'Segoe UI', sans-serif;
    }

    h1 {
      color: white;
      font-size: 4em;
      text-align: center;
      animation: shake 2s infinite;
      text-shadow: 2px 2px 10px rgba(0, 0, 0, 0.4);
    }

    @keyframes shake {
      0% { transform: translateX(0); }
      25% { transform: translateX(-5px); }
      50% { transform: translateX(5px); }
      75% { transform: translateX(-3px); }
      100% { transform: translateX(0); }
    }
  </style>
</head>
<body>
  <h1 id="welcomeText">Welcome!</h1>

  <script>
    // Change color every 2 seconds for some variation
    const welcomeText = document.getElementById('welcomeText');
    const colors = ['#ffffff', '#ffeb3b', '#00ffcc', '#ff4081'];

    let index = 0;
    setInterval(() => {
      welcomeText.style.color = colors[index];
      index = (index + 1) % colors.length;
    }, 2000);
  </script>
</body>
</html>
