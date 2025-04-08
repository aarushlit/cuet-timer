<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Countdown to May 8, 2025</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background: #f4f4f4;
    }
    .countdown {
      background: white;
      padding: 30px;
      border-radius: 16px;
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
      text-align: center;
      font-size: 1.5em;
    }
    .time {
      font-size: 2em;
      color: #0077ff;
      margin-top: 10px;
    }
    .label {
      font-size: 1.2em;
      margin-bottom: 10px;
      color: #333;
    }
  </style>
</head>
<body>
  <div class="countdown">
    <div class="label">CUET - Time left until <strong>May 8, 2025</strong>:</div>
    <div class="time" id="timer"></div>
  </div>

  <script>
    function updateTimer() {
      const futureDate = new Date('May 8, 2025 00:00:00').getTime();
      const now = new Date().getTime();
      const diff = futureDate - now;

      if (diff <= 0) {
        document.getElementById("timer").innerText = "The date has passed!";
        return;
      }

      const days = Math.floor(diff / (1000 * 60 * 60 * 24));
      const hours = Math.floor((diff % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
      const minutes = Math.floor((diff % (1000 * 60 * 60)) / (1000 * 60));
      const seconds = Math.floor((diff % (1000 * 60)) / 1000);

      document.getElementById("timer").innerText = `${days}d ${hours}h ${minutes}m ${seconds}s`;
    }

    updateTimer();
    setInterval(updateTimer, 1000); // update every second
  </script>
</body>
</html>
