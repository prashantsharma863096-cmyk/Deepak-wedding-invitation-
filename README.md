
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Our Wedding Invitation</title>
<style>
* { box-sizing: border-box; }
body {
  margin: 0;
  background: #fff8ed;
  color: #713e35;
  font-family: Georgia, serif;
  text-align: center;
}
.hero {
  min-height: 100vh;
  padding: 65px 20px;
  background: linear-gradient(#fff8ed, #f4d9d0);
  border: 12px double #c69b51;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.om { font-size: 42px; color: #ad792c; }
h1 {
  font-size: clamp(38px, 9vw, 65px);
  color: #912f43;
  margin: 18px 0;
}
h2 { color: #912f43; }
.gold { color: #b38a45; }
.divider { font-size: 30px; margin: 20px; }
section { padding: 45px 20px; }
.card {
  max-width: 500px;
  margin: 20px auto;
  padding: 30px;
  border: 2px solid #c69b51;
  border-radius: 18px;
  background: white;
  box-shadow: 0 8px 25px #713e3520;
}
button, .btn {
  display: inline-block;
  padding: 14px 26px;
  margin: 10px;
  background: #912f43;
  color: white;
  border: none;
  border-radius: 30px;
  text-decoration: none;
  font-size: 16px;
  cursor: pointer;
}
#countdown { font-size: 22px; font-weight: bold; }
footer { padding: 30px; background: #912f43; color: white; }
</style>
</head>
<body>

<div class="hero">
  <div class="om">ॐ श्री गणेशाय नमः</div>
  <p class="gold">TOGETHER WITH OUR FAMILIES</p>
  <p>We joyfully invite you to celebrate</p>
  <p class="gold">THE WEDDING OF</p>
  <h1>Rahul <span class="gold">&</span> Priya</h1>
  <div class="divider">❀ ♥ ❀</div>
  <h2>15 December 2026</h2>
  <p>Tuesday | 7:00 PM onwards</p>
  <a href="#details" class="btn">Open Invitation ♡</a>
</div>

<section id="details">
  <h2>Our Special Day</h2>
  <p>Two hearts, one beautiful journey.</p>

  <div class="card">
    <h2>Wedding Ceremony</h2>
    <p>15 December 2026</p>
    <p>7:00 PM onwards</p>
    <p>Royal Palace Banquet Hall</p>
    <p>Mathura, Uttar Pradesh</p>
    <a class="btn"
       href="https://www.google.com/maps/search/?api=1&query=Mathura"
       target="_blank" rel="noopener">
       Get Directions
    </a>
  </div>

  <div class="card">
    <h2>Countdown to Forever</h2>
    <p id="countdown"></p>
  </div>

  <div class="card">
    <h2>RSVP</h2>
    <p>Your presence is our greatest blessing.</p>
    <a class="btn" id="rsvp"
       href="https://wa.me/919999999999"
       target="_blank" rel="noopener">
       Confirm on WhatsApp
    </a>
  </div>
</section>

<footer>
  <h2 style="color:white">Rahul ♥ Priya</h2>
  <p>We can't wait to celebrate with you!</p>
</footer>

<script>
const weddingDate = new Date("2026-12-15T19:00:00+05:30");

function updateCountdown() {
  const distance = weddingDate - new Date();
  const el = document.getElementById("countdown");
  if (distance <= 0) {
    el.textContent = "Our special day is here! ♥";
    return;
  }
  const days = Math.floor(distance / 86400000);
  const hours = Math.floor(distance / 3600000) % 24;
  const minutes = Math.floor(distance / 60000) % 60;
  const seconds = Math.floor(distance / 1000) % 60;
  el.textContent =
    `${days} Days ${hours} Hours ${minutes} Min ${seconds} Sec`;
}
updateCountdown();
setInterval(updateCountdown, 1000);
</script>

</body>
</html>

