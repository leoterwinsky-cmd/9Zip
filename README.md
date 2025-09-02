<!DOCTYPE html>
<html lang="de">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Mein Game Projekt</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #111;
      color: #eee;
      margin: 0;
      padding: 0;
    }
    header {
      padding: 1.5rem;
      background: #222;
      text-align: center;
    }
    h1 { margin: 0; }
    main {
      padding: 2rem;
      max-width: 800px;
      margin: auto;
    }
    img {
      max-width: 100%;
      border-radius: 12px;
      margin: 1rem 0;
    }
    audio {
      width: 100%;
      margin: 1rem 0;
    }
    a.button {
      display: inline-block;
      margin: 1rem;
      padding: 1rem 2rem;
      background: #4caf50;
      color: #fff;
      text-decoration: none;
      border-radius: 8px;
      font-weight: bold;
      cursor: pointer;
    }
    a.button:hover { background: #66bb6a; }
    .release {
      background: #1c1c1c;
      padding: 1rem;
      border-radius: 8px;
      margin-bottom: 1rem;
    }
    .release h2 { margin-top: 0; }
    a.download {
      display: inline-block;
      margin-top: .5rem;
      padding: .6rem 1.2rem;
      background: #4caf50;
      color: #fff;
      text-decoration: none;
      border-radius: 6px;
    }
    a.download:hover { background: #66bb6a; }
    .hidden { display: none; }
  </style>
</head>
<body>
  <header>
    <h1>9Zip Official Website</h1>
    <p>Updates, Betas and Releases</p>
  </header>

  <!-- Startseite -->
  <main id="home">
    <p>Welcome to 9Zip we are the official Team.</p>

    <!-- Dein Bild -->
    <img src="dein-bild.png" alt="Screenshot oder Artwork">

    <!-- Dein Audio -->
    <audio controls>
      <source src="Musik.mp3" type="audio/mpeg">
      Dein Browser unterstützt kein Audio.
    </audio>

    <!-- Button zu Releases -->
    <a class="button" onclick="showReleases()">🚀 See all releases</a>
  </main>

  <!-- Releases-Seite -->
  <main id="releases" class="hidden">
    <h2>All Releases</h2>
    <a class="button" onclick="showHome()">⬅ Zurück</a>

    <div class="release">
      <h2>Version 1.0</h2>
      <p>Erste stabile Version! Enthält das Grundspiel.</p>
      <a class="download" href="assets/game-v1.0.zip">⬇ Download</a>
    </div>

    <div class="release">
      <h2>Beta 0.9</h2>
      <p>Frühe Beta-Version mit Test-Features.</p>
      <a class="download" href="assets/game-beta-0.9.zip">⬇ Download</a>
    </div>

    <!-- Neue Releases einfach hier einfügen -->
  </main>

  <script>
    function showReleases() {
      document.getElementById('home').classList.add('hidden');
      document.getElementById('releases').classList.remove('hidden');
    }
    function showHome() {
      document.getElementById('releases').classList.add('hidden');
      document.getElementById('home').classList.remove('hidden');
    }
  </script>
</body>
</html>
