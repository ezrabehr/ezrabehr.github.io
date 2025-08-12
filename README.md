<html lang="en">
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width,initial-scale=1" />
    <title>Wedding Countdown — 15/09/2025</title>
    <style>
      :root {
        --bg: #0f1724;
        --card: #0b1220;
        --accent: #ff6b6b;
        --glass: rgba(255, 255, 255, 0.06);
        --text: #e6eef8;
      }
      * {
        box-sizing: border-box;
      }
      html,
      body {
        height: 100%;
      }
      body {
        margin: 0;
        background: linear-gradient(160deg, #071028 0%, #0b1730 60%);
        color: var(--text);
        font-family: Inter, system-ui, -apple-system, "Segoe UI", Roboto,
          "Helvetica Neue", Arial;
        display: flex;
        align-items: center;
        justify-content: center;
        padding: 24px;
      }
      .card {
        width: min(920px, 96%);
        background: linear-gradient(
          180deg,
          rgba(255, 255, 255, 0.02),
          rgba(255, 255, 255, 0.01)
        );
        border-radius: 16px;
        padding: 28px;
        box-shadow: 0 10px 30px rgba(2, 6, 23, 0.6);
        display: grid;
        grid-template-columns: 1fr 340px;
        gap: 20px;
        align-items: center;
      }
      .left {
        padding: 10px 8px;
      }
      h1 {
        margin: 0 0 8px 0;
        font-size: 28px;
        letter-spacing: -0.4px;
        display: flex;
        align-items: center;
        gap: 12px;
      }
      .sub {
        margin: 0 0 18px 0;
        color: #c8d7f0;
        opacity: 0.9;
      }
      .timer {
        display: flex;
        gap: 14px;
        flex-wrap: wrap;
        align-items: center;
      }
      .unit {
        background: var(--glass);
        padding: 18px 16px;
        border-radius: 12px;
        min-width: 110px;
        text-align: center;
        backdrop-filter: blur(6px);
      }
      .unit .big {
        font-size: 34px;
        font-weight: 700;
      }
      .unit .label {
        font-size: 12px;
        color: #b9c6e6;
        margin-top: 6px;
      }
      .progressWrap {
        margin-top: 18px;
      }
      .progress {
        height: 12px;
        background: rgba(255, 255, 255, 0.06);
        border-radius: 999px;
        overflow: hidden;
      }
      .progress > i {
        display: block;
        height: 100%;
        width: 0%;
        background: linear-gradient(90deg, var(--accent), #ffb46b);
        transition: width 0.5s ease;
      }
      .meta {
        margin-top: 12px;
        color: #b8c4de;
        font-size: 13px;
      }
      .right {
        background: linear-gradient(
          180deg,
          rgba(255, 255, 255, 0.02),
          rgba(255, 255, 255, 0.01)
        );
        padding: 18px;
        border-radius: 12px;
        display: flex;
        flex-direction: column;
        gap: 12px;
        align-items: center;
        justify-content: center;
      }
      .when {
        font-weight: 600;
        font-size: 15px;
        color: var(--accent);
        text-align: center;
      }
      .location {
        font-size: 13px;
        color: #bcd0f7;
        text-align: center;
      }
      .bigMsg {
        margin-top: 8px;
        font-size: 18px;
        text-align: center;
        color: #dff1e7;
      }
      .celebrate {
        margin-top: 12px;
        padding: 14px 28px;
        border-radius: 999px;
        font-size: 16px;
        font-weight: 600;
        color: white;
        background: linear-gradient(90deg, #ff6b6b, #ffb36b);
        box-shadow: 0 0 12px rgba(255, 107, 107, 0.5);
        cursor: pointer;
        border: none;
        transition: all 0.25s ease;
      }
      .celebrate:hover {
        transform: scale(1.08);
        box-shadow: 0 0 18px rgba(255, 179, 107, 0.8),
          0 0 30px rgba(255, 107, 107, 0.5);
      }
      .celebrate:active {
        transform: scale(0.96);
      }

      /* simple confetti pieces */
      .confetti {
        position: fixed;
        left: 0;
        top: 0;
        right: 0;
        bottom: 0;
        pointer-events: none;
        overflow: hidden;
      }
      .confetti .p {
        position: absolute;
        width: 10px;
        height: 16px;
        opacity: 0;
        transform-origin: center;
        animation: drop 3000ms linear forwards;
      }
      @keyframes drop {
        0% {
          opacity: 1;
          transform: translateY(-10vh) rotate(0deg);
        }
        100% {
          opacity: 1;
          transform: translateY(120vh) rotate(720deg);
        }
      }
      footer {
        grid-column: 1 / -1;
        margin-top: 10px;
        text-align: center;
        color: #9fb1e0;
        font-size: 13px;
      }
      @media (max-width: 760px) {
        .card {
          grid-template-columns: 1fr;
          padding: 18px;
        }
        .timer .unit {
          min-width: 80px;
          padding: 14px;
        }
      }
    </style>
  </head>
  <body>
    <div class="card" role="region" aria-label="Wedding countdown">
      <div class="left">
        <h1>Countdown to our wedding <span aria-hidden>💍</span></h1>
        <p class="sub">Hold tight — counting down to the big day!</p>

        <div class="timer" id="timer">
          <div class="unit">
            <div class="big" id="days">0</div>
            <div class="label">Days</div>
          </div>
          <div class="unit">
            <div class="big" id="hours">00</div>
            <div class="label">Hours</div>
          </div>
          <div class="unit">
            <div class="big" id="minutes">00</div>
            <div class="label">Minutes</div>
          </div>
          <div class="unit">
            <div class="big" id="seconds">00</div>
            <div class="label">Seconds</div>
          </div>
        </div>

        <div class="progressWrap">
          <div class="progress" aria-hidden>
            <i id="progressBar"></i>
          </div>
          <div class="meta" id="meta">Time remaining of the countdown</div>
        </div>
      </div>

      <div class="right">
        <div class="when" id="targetText">
          Mon, 15 Sep 2025 — 18:30 (Asia/Jerusalem)
        </div>
        <div class="location">Gush Etzion Winery</div>
        <div class="bigMsg" id="statusMsg">See you on the dance floor 🕺💃</div>
        <button class="celebrate" id="celebrateBtn">Celebrate now</button>
      </div>

      <footer>
        Tip: save this page and open it anytime to see the live countdown.
      </footer>
    </div>

    <div class="confetti" id="confettiArea" aria-hidden></div>

    <script>
      // === CONFIGURE TARGET DATE/TIME (ISO with timezone) ===
      // Using Asia/Jerusalem offset +03:00 (adjust here if needed)
      const targetISO = "2025-09-15T18:30:00+03:00";
      const targetDate = new Date(targetISO);

      // Elements
      const daysEl = document.getElementById("days");
      const hoursEl = document.getElementById("hours");
      const minutesEl = document.getElementById("minutes");
      const secondsEl = document.getElementById("seconds");
      const progressBar = document.getElementById("progressBar");
      const meta = document.getElementById("meta");
      const statusMsg = document.getElementById("statusMsg");
      const confettiArea = document.getElementById("confettiArea");
      const celebrateBtn = document.getElementById("celebrateBtn");
      const targetText = document.getElementById("targetText");

      // Show formatted target date (localized)
      try {
        const fmt = new Intl.DateTimeFormat(undefined, {
          weekday: "short",
          year: "numeric",
          month: "short",
          day: "numeric",
          hour: "2-digit",
          minute: "2-digit",
          timeZoneName: "short",
        });
        targetText.textContent = fmt.format(targetDate);
      } catch (e) {
        // fallback
        targetText.textContent = targetDate.toString();
      }

      // For progress: set a start reference (now) and compute percent passed until target
      const startDate = new Date(); // when countdown was created; progress measures from now -> target
      let totalSpan = targetDate - startDate;
      if (totalSpan < 0) totalSpan = 1; // avoid div/zero

      // update timer every second
      let interval = setInterval(update, 1000);
      update(); // initial render

      function update() {
        const now = new Date();
        const diff = targetDate - now;

        if (diff <= 0) {
          // reached or passed
          daysEl.textContent = "0";
          hoursEl.textContent = "00";
          minutesEl.textContent = "00";
          secondsEl.textContent = "00";
          progressBar.style.width = "100%";
          meta.textContent = "It’s time! The countdown has finished.";
          statusMsg.textContent = "We're married! 🎉";
          triggerConfetti();
          clearInterval(interval);
          return;
        }

        // breakdown
        const sec = Math.floor(diff / 1000) % 60;
        const min = Math.floor(diff / (1000 * 60)) % 60;
        const hr = Math.floor(diff / (1000 * 60 * 60)) % 24;
        const dy = Math.floor(diff / (1000 * 60 * 60 * 24));

        daysEl.textContent = dy;
        hoursEl.textContent = String(hr).padStart(2, "0");
        minutesEl.textContent = String(min).padStart(2, "0");
        secondsEl.textContent = String(sec).padStart(2, "0");

        // progress from startDate -> targetDate (clamped 0-100)
        const passed = now - startDate;
        const pct = Math.max(0, Math.min(1, passed / totalSpan));
        progressBar.style.width = pct * 100 + "%";

        // meta text
        meta.textContent = `Approx. ${dy} days ${hr} hours remaining • Target: ${targetDate.toLocaleString()}`;
      }

      // Simple confetti generator
      function triggerConfetti(amount = 80) {
        confettiArea.innerHTML = "";
        const colors = ["#ff6b6b", "#ffd166", "#6bf7d3", "#6bb6ff", "#c18cff"];
        for (let i = 0; i < amount; i++) {
          const el = document.createElement("div");
          el.className = "p";
          el.style.left = Math.random() * 100 + "%";
          el.style.top = -10 - Math.random() * 20 + "vh";
          el.style.background =
            colors[Math.floor(Math.random() * colors.length)];
          el.style.width = 6 + Math.random() * 12 + "px";
          el.style.height = 10 + Math.random() * 18 + "px";
          el.style.borderRadius = Math.random() > 0.5 ? "2px" : "50%";
          el.style.transform = `rotate(${Math.random() * 360}deg)`;
          el.style.animationDuration = 2000 + Math.random() * 2200 + "ms";
          el.style.opacity = 1;
          confettiArea.appendChild(el);
          // remove after animation
          setTimeout(() => {
            el.remove();
          }, 6000);
        }
      }

      celebrateBtn.addEventListener("click", () => {
        triggerConfetti(60);
      });

      // Accessibility: update title every minute
      setInterval(() => {
        document.title = `${daysEl.textContent}d ${hoursEl.textContent}h ${minutesEl.textContent}m — Wedding countdown`;
      }, 60_000);
    </script>
  </body>
</html>
