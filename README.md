# lunestyles
an online brand website
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>LuneStyles</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <div class="beach-scene">
    <img src="logo.png" alt="LuneStyles Logo" class="logo" />
    <div class="waves"></div>
    <div class="seagulls"></div>
  </div>

  <audio id="beach-sound" autoplay loop>
    <source src="beach-sound.mp3" type="audio/mpeg" />
    Your browser does not support the audio element.
  </audio>

  <script src="script.js"></script>
</body>
</html>
body, html {
  margin: 0;
  padding: 0;
  overflow: hidden;
  height: 100%;
  background: linear-gradient(to top, #fceabb, #f8b500);
}

.beach-scene {
  position: relative;
  width: 100%;
  height: 100%;
  background: url('beach-background.jpg') no-repeat center center/cover;
}

.logo {
  position: absolute;
  top: 20px;
  left: 20px;
  width: 150px;
  animation: fadeIn 3s ease-in-out;
}

.waves {
  position: absolute;
  bottom: 0;
  width: 100%;
  height: 100px;
  background: url('waves.png') repeat-x;
  animation: wave 10s linear infinite;
}

.seagulls {
  position: absolute;
  top: 50px;
  right: 0;
  width: 100px;
  height: 100px;
  background: url('seagulls.png') no-repeat;
  animation: fly 15s linear infinite;
}

@keyframes wave {
  0% { background-position-x: 0; }
  100% { background-position-x: 1000px; }
}

@keyframes fly {
  0% { right: -100px; }
  100% { right: 100%; }
}

@keyframes fadeIn {
  from { opacity: 0; }
  to { opacity: 1; }
}
// Optional: Additional interactivity can be added here
