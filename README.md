<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Griffins</title>
  <style>
    :root {
      --bg: #050505;
      --panel: rgba(255, 255, 255, 0.02);
      --text: #f2f2f2;
      --muted: #d1d1d1;
      --accent: #d76a2b;
      --accent-soft: rgba(215, 106, 43, 0.28);
    }

    * { box-sizing: border-box; }

    html, body {
      margin: 0;
      height: 100%;
      background: var(--bg);
      color: var(--text);
      font-family: Arial, Helvetica, sans-serif;
      overflow: hidden;
    }

    body {
      display: grid;
      place-items: center;
      background:
        radial-gradient(circle at 20% 20%, rgba(255,255,255,0.03), transparent 30%),
        radial-gradient(circle at 80% 35%, rgba(255,120,0,0.04), transparent 28%),
        linear-gradient(135deg, #020202, #0a0a0a 30%, #050505);
    }

    .page {
      position: relative;
      width: 100%;
      height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 40px;
      overflow: hidden;
    }

    .lion-bg {
      position: absolute;
      inset: 0;
      display: flex;
      align-items: center;
      justify-content: center;
      opacity: 0.14;
      filter: blur(0.5px);
      pointer-events: none;
    }

    .lion-bg svg {
      width: 110%;
      height: 110%;
      transform: translateY(12px);
    }

    .content {
      position: relative;
      z-index: 2;
      width: min(900px, 90vw);
      padding: 32px 28px;
      border-left: 2px solid rgba(255,255,255,0.08);
      background: rgba(255,255,255,0.01);
      backdrop-filter: blur(2px);
      box-shadow: 0 0 30px rgba(0,0,0,0.18);
    }

    .line {
      display: block;
      margin: 0;
      font-weight: 700;
      letter-spacing: 0.04em;
      text-transform: uppercase;
    }

    .line1 {
      font-size: clamp(2rem, 3vw, 4rem);
      line-height: 1.1;
      margin-bottom: 10px;
      color: #f5f5f5;
    }

    .line2 {
      font-size: clamp(1rem, 1.2vw, 1.7rem);
      line-height: 1.5;
      color: var(--muted);
      margin-bottom: 28px;
      font-weight: 500;
      letter-spacing: 0.08em;
      text-transform: none;
    }

    .line3 {
      font-size: clamp(1.8rem, 2.2vw, 3rem);
      line-height: 1.2;
      margin: 24px 0 0;
      color: #f0f0f0;
    }

    .line4 {
      font-size: clamp(0.9rem, 1.2vw, 1.4rem);
      line-height: 1.8;
      color: #d8d8d8;
      margin-top: 26px;
      font-weight: 600;
      letter-spacing: 0.12em;
      text-transform: uppercase;
    }

    .accent {
      color: var(--accent);
      text-shadow: 0 0 18px rgba(215, 106, 43, 0.25);
    }
  </style>
</head>
<body>
  <div class="page">
    <div class="lion-bg" aria-hidden="true">
      <svg viewBox="0 0 800 800" xmlns="http://www.w3.org/2000/svg">
        <defs>
          <linearGradient id="lionGlow" x1="0%" x2="100%" y1="0%" y2="100%">
            <stop offset="0%" stop-color="#ff9b50" stop-opacity="0.7" />
            <stop offset="35%" stop-color="#d65b1a" stop-opacity="0.55" />
            <stop offset="100%" stop-color="#4a1b08" stop-opacity="0.3" />
          </linearGradient>
        </defs>

        <g fill="url(#lionGlow)">
          <!-- mane -->
          <circle cx="400" cy="360" r="210" opacity="0.75"/>
          <circle cx="300" cy="300" r="120" opacity="0.7"/>
          <circle cx="500" cy="300" r="120" opacity="0.7"/>
          <circle cx="220" cy="400" r="115" opacity="0.7"/>
          <circle cx="580" cy="400" r="115" opacity="0.7"/>
          <circle cx="350" cy="220" r="85" opacity="0.7"/>
          <circle cx="450" cy="220" r="85" opacity="0.7"/>

          <!-- face -->
          <path d="
            M270 420
            C290 330, 340 280, 400 280
            C460 280, 510 330, 530 420
            L560 510
            C575 545, 570 590, 540 610
            L500 640
            C465 660, 425 670, 400 670
            C375 670, 335 660, 300 640
            L260 610
            C230 590, 225 545, 240 510
            Z" opacity="0.7"/>

          <!-- muzzle -->
          <path d="
            M330 470
            C350 500, 370 520, 400 520
            C430 520, 450 500, 470 470
            L500 530
            C470 585, 435 610, 400 610
            C365 610, 330 585, 300 530
            Z" opacity="0.8"/>

          <!-- eyes -->
          <ellipse cx="350" cy="385" rx="18" ry="12" fill="#1f0d08" opacity="0.9"/>
          <ellipse cx="450" cy="385" rx="18" ry="12" fill="#1f0d08" opacity="0.9"/>

          <!-- nose -->
          <path d="M390 420 L400 440 L410 420 Z" fill="#1f0d08" opacity="0.8"/>

          <!-- mouth -->
          <path d="M350 500 C370 520, 390 530, 400 530 C410 530, 430 520, 450 500" fill="none" stroke="#1f0d08" stroke-width="8" stroke-linecap="round" opacity="0.9"/>
        </g>
      </svg>
    </div>

    <div class="content">
      <span class="line line1">Hello, I'm <span class="accent">Griffins</span></span>
      <span class="line line2">just a random boy from a humble beginning</span>

      <span class="line line3">Web Developer</span>

      <span class="line line4">not your regular recently</span>
    </div>
  </div>
</body>
</html>
