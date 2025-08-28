<!-- ====== GAME HUD / CANVAS-STYLE GITHUB STATS (README SAFE) ====== -->
<div align="center">

  <div style="
    display:inline-block;
    background: #0b0f14;
    border: 2px solid #00ffc6;
    border-radius: 18px;
    padding: 22px;
    color: #e6fff9;
    font-family: Consolas, Menlo, Monaco, 'Courier New', monospace;
    box-shadow: 0 0 18px rgba(0,255,198,.35), inset 0 0 12px rgba(0,255,198,.2);
    text-align:left;
    width: 520px;
    position:relative;
  ">

    <!-- top bar -->
    <div style="display:flex; align-items:center; justify-content:space-between; margin-bottom:14px;">
      <div style="font-weight:700; letter-spacing:.5px; text-shadow:0 0 8px #00ffc6;">
        ▶ TamerCan // GITHUB HUD
      </div>
      <div style="display:flex; gap:6px;">
        <span style="width:10px; height:10px; border-radius:2px; background:#ff4d4d; box-shadow:0 0 8px #ff4d4d;"></span>
        <span style="width:10px; height:10px; border-radius:2px; background:#ffd24d; box-shadow:0 0 8px #ffd24d;"></span>
        <span style="width:10px; height:10px; border-radius:2px; background:#4dff88; box-shadow:0 0 8px #4dff88;"></span>
      </div>
    </div>

    <!-- body -->
    <div style="display:flex; gap:16px; align-items:stretch;">
      <!-- left: stats list -->
      <div style="flex:1; border:1px solid rgba(0,255,198,.35); border-radius:12px; padding:14px;">
        <div style="opacity:.8; font-size:12px; margin-bottom:8px;">SYSTEM // METRICS</div>

        <div style="display:flex; justify-content:space-between; padding:8px 0; border-bottom:1px dashed rgba(0,255,198,.25);">
          <span>⭐ Total Stars</span><b>44</b>
        </div>
        <div style="display:flex; justify-content:space-between; padding:8px 0; border-bottom:1px dashed rgba(0,255,198,.25);">
          <span>🌀 Commits (2025)</span><b>5</b>
        </div>
        <div style="display:flex; justify-content:space-between; padding:8px 0; border-bottom:1px dashed rgba(0,255,198,.25);">
          <span>🔀 Pull Requests</span><b>1</b>
        </div>
        <div style="display:flex; justify-content:space-between; padding:8px 0; border-bottom:1px dashed rgba(0,255,198,.25);">
          <span>❗ Issues</span><b>0</b>
        </div>
        <div style="display:flex; justify-content:space-between; padding:8px 0;">
          <span>💻 Contributed (last year)</span><b>0</b>
        </div>

        <!-- static progress bar (readme-safe) -->
        <div style="margin-top:12px;">
          <div style="opacity:.8; font-size:12px; margin-bottom:6px;">XP / Next Rank</div>
          <div style="
              height:14px; border:1px solid rgba(0,255,198,.4); border-radius:8px; overflow:hidden;
              background: linear-gradient(90deg, rgba(0,255,198,.08), rgba(0,170,255,.08));
          ">
            <!-- fill width%: adjust for your liking -->
            <div style="
                height:100%; width:68%;
                background: linear-gradient(90deg, #00ffc6, #00aaff);
                box-shadow: 0 0 10px #00ffc6;
            "></div>
          </div>
        </div>
      </div>

      <!-- right: radial gauge (pure SVG, no animation) -->
      <div style="
        width:180px; border:1px solid rgba(0,255,198,.35);
        border-radius:12px; padding:12px; display:flex; align-items:center; justify-content:center;
      ">
        <svg width="140" height="140" viewBox="0 0 120 120" role="img" aria-label="Rank gauge">
          <defs>
            <linearGradient id="ring" x1="0" y1="0" x2="1" y2="1">
              <stop offset="0%" stop-color="#00ffc6"/>
              <stop offset="100%" stop-color="#00aaff"/>
            </linearGradient>
            <filter id="glow">
              <feGaussianBlur stdDeviation="2.5" result="coloredBlur"/>
              <feMerge>
                <feMergeNode in="coloredBlur"/>
                <feMergeNode in="SourceGraphic"/>
              </feMerge>
            </filter>
          </defs>

          <!-- track -->
          <circle cx="60" cy="60" r="52"
                  stroke="rgba(0,255,198,.15)" stroke-width="10"
                  fill="none" />

          <!-- value (edit stroke-dashoffset for % ) -->
          <!-- circumference for r=52 is ~326.73 -->
          <!-- 68% => dashoffset ≈ 104.55 -->
          <circle cx="60" cy="60" r="52"
                  stroke="url(#ring)" stroke-width="10"
                  stroke-linecap="round"
                  stroke-dasharray="326.73"
                  stroke-dashoffset="104.55"
                  transform="rotate(-90 60 60)"
                  fill="none" filter="url(#glow)"/>

          <!-- center text -->
          <g font-family="Consolas, monospace" text-anchor="middle">
            <text x="60" y="60" dy="7" font-size="22" fill="#e6fff9" style="letter-spacing:1px;">C+</text>
            <text x="60" y="86" font-size="10" fill="rgba(230,255,249,.7)">RANK</text>
          </g>
        </svg>
      </div>
    </div>

    <!-- subtle scanline overlay -->
    <div style="
      content:''; position:absolute; inset:0; pointer-events:none; border-radius:18px;
      background-image: linear-gradient(to bottom, rgba(255,255,255,.06) 1px, transparent 1px);
      background-size: 100% 3px; opacity:.25;
    "></div>

  </div>
</div>
