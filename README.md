
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Wedding Invitation</title>
  <style>
    body {
      margin: 0;
      min-height: 100vh;
      display: grid;
      place-items: center;
      background: #fff0e6;
      font-family: Georgia, serif;
      text-align: center;
      color: #703c36;
    }
    .card {
      width: 80%;
      max-width: 420px;
      padding: 30px 20px;
      border: 3px double #b88a46;
      background: #fffaf2;
      border-radius: 18px;
    }
    h1 { color: #a05b32; }
    button {
      padding: 12px 22px;
      background: #8b3a3a;
      color: white;
      border: 0;
      border-radius: 25px;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <main class="card">
    <p>YOU ARE CORDIALLY INVITED</p>
    <h1>Saravanan &amp; Bhargavi</h1>
    <p>Request the pleasure of your company</p>
    <p>at our wedding celebration</p>
    <p><strong>Date:</strong> Add your wedding date</p>
    <p><strong>Venue:</strong> Add your wedding venue</p>

    <button onclick="playMusic()">Open Invitation ♡</button>
    <p id="message">Tap to open the invitation and play music</p>

    <audio id="song" loop>
      <source src="ranjha_tK98YX5S.mp3" type="audio/mpeg">
    </audio>
  </main>

  <script>
    function playMusic() {
      const song = document.getElementById("song");
      song.play().then(() => {
        document.getElementById("message").textContent =
          "Enjoy our wedding invitation ♡";
      }).catch(() => {
        document.getElementById("message").textContent =
          "Please tap again to play the music.";
      });
    }
  </script>
</body>
</html>
