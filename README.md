<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Debeatzgh Music Hub</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
body{
  margin:0;
  font-family:system-ui,-apple-system,BlinkMacSystemFont;
  background:#020617;
  color:#e5e7eb;
}

/* Header */
.header{
  text-align:center;
  padding:30px 16px;
}
.header h1{
  font-size:26px;
  font-weight:800;
}
.header p{
  color:#9ca3af;
  font-size:14px;
}

/* Carousel */
.carousel{
  display:flex;
  gap:22px;
  overflow-x:auto;
  scroll-snap-type:x mandatory;
  padding:20px;
}
.track{
  min-width:320px;
  background:#020617;
  border-radius:18px;
  padding:14px;
  scroll-snap-align:center;
  box-shadow:0 12px 30px rgba(0,0,0,.45);
}
.track h3{
  color:#22c55e;
  margin-bottom:6px;
}
.track p{
  font-size:13px;
  color:#9ca3af;
  margin-bottom:10px;
}
iframe{
  border-radius:12px;
}

/* Floating Mini Player */
.floating-player{
  position:fixed;
  left:12px;
  top:50%;
  transform:translateY(-50%);
  background:#16a34a;
  color:#fff;
  padding:12px 14px;
  border-radius:999px;
  font-weight:800;
  cursor:pointer;
  z-index:9999;
  box-shadow:0 8px 25px rgba(0,0,0,.5);
}

/* Fullscreen Overlay */
.overlay{
  display:none;
  position:fixed;
  inset:0;
  background:#020617;
  z-index:10000;
  overflow-y:auto;
}

.overlay-header{
  display:flex;
  justify-content:space-between;
  align-items:center;
  padding:14px 16px;
  background:#020617;
  position:sticky;
  top:0;
  z-index:10;
}

.overlay-header h2{
  font-size:18px;
  font-weight:800;
}

.close-btn{
  font-size:26px;
  cursor:pointer;
  color:#22c55e;
}

/* Fullscreen carousel */
.full-carousel{
  padding:16px;
  display:grid;
  gap:22px;
}
</style>
</head>

<body>

<div class="header">
  <h1>🎧 Debeatzgh Music Hub</h1>
  <p>AI-curated vibes for study, chill & creative flow</p>
</div>

<!-- NORMAL VIEW -->
<div class="carousel">

  <div class="track">
    <h3>EDM Club Mix</h3>
    <p>⚡ High-energy electronic beats designed to boost mood, focus, and late-night creativity.</p>
    <iframe src="https://audiomack.com/embed/debeatz4/song/12909519" width="100%" height="252" frameborder="0"></iframe>
  </div>

  <div class="track">
    <h3>Chill Study Beats</h3>
    <p>📚 Calm lo-fi rhythms perfect for studying, reading, and deep concentration sessions.</p>
    <iframe src="https://audiomack.com/embed/debeatz4/song/12909474" width="100%" height="252" frameborder="0"></iframe>
  </div>

  <div class="track">
    <h3>Hip-Hop Session</h3>
    <p>🔥 Smooth hip-hop instrumentals with modern bounce and clean underground energy.</p>
    <iframe src="https://audiomack.com/embed/debeatz4/song/12909466" width="100%" height="252" frameborder="0"></iframe>
  </div>

</div>

<!-- FLOATING MINI PLAYER -->
<div class="floating-player" onclick="openPlayer()">
🎵 Play Music
</div>

<!-- FULLSCREEN PLAYER -->
<div class="overlay" id="playerOverlay">
  <div class="overlay-header">
    <h2>🎧 Full Music Mode</h2>
    <span class="close-btn" onclick="closePlayer()">×</span>
  </div>

  <div class="full-carousel">

    <div class="track">
      <h3>Modern Hip-Hop</h3>
      <p>🚀 Contemporary hip-hop beats crafted for creators, workouts, and night drives.</p>
      <iframe src="https://audiomack.com/embed/debeatz4/song/modern-hip-hop-15-07-2020-10-14" width="100%" height="252" frameborder="0"></iframe>
    </div>

    <div class="track">
      <h3>Synth Hip-Hop</h3>
      <p>🎹 Retro synths fused with modern drums for futuristic creative sessions.</p>
      <iframe src="https://audiomack.com/embed/debeatz4/song/synth-hip-beat" width="100%" height="252" frameborder="0"></iframe>
    </div>

    <div class="track">
      <h3>Late-Night Chill Beats</h3>
      <p>🌙 Relaxing ambient vibes for coding, studying, or winding down at night.</p>
      <iframe src="https://audiomack.com/embed/debeatz4/song/chill-study-beats-21-08-2020-08-32" width="100%" height="252" frameborder="0"></iframe>
    </div>

  </div>
</div>

<script>
function openPlayer(){
  document.getElementById("playerOverlay").style.display="block";
}
function closePlayer(){
  document.getElementById("playerOverlay").style.display="none";
}
</script>

</body>
</html>
