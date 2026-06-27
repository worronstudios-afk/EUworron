
<style>
* { box-sizing: border-box; margin: 0; padding: 0; }
body { font-family: var(--font-mono); }

.root {
  background: var(--surface-1);
  border: 0.5px solid var(--border);
  border-radius: 12px;
  overflow: hidden;
  max-width: 680px;
}

.toolbar {
  background: var(--surface-0);
  border-bottom: 0.5px solid var(--border);
  padding: 10px 14px;
  display: flex;
  align-items: center;
  gap: 10px;
}
.dot { width: 12px; height: 12px; border-radius: 50%; display: inline-block; }
.dot-r { background: #ff5f56; }
.dot-y { background: #ffbd2e; }
.dot-g { background: #27c93f; }
.file-label { font-size: 12px; color: var(--text-muted); margin-left: 6px; font-family: var(--font-mono); }

.md { padding: 28px 32px; }

.hero {
  text-align: center;
  padding-bottom: 24px;
  border-bottom: 0.5px solid var(--border);
  margin-bottom: 24px;
}

.badge-row {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 8px;
  margin-bottom: 18px;
}

.badge {
  font-size: 12px;
  font-family: var(--font-mono);
  padding: 4px 10px;
  border-radius: 20px;
  border: 0.5px solid var(--border-strong);
  color: var(--text-secondary);
  background: var(--surface-2);
  white-space: nowrap;
}
.badge.accent { background: var(--bg-accent); color: var(--text-accent); border-color: var(--border-accent); }

.name {
  font-size: 22px;
  font-weight: 500;
  color: var(--text-primary);
  font-family: var(--font-sans);
  margin-bottom: 6px;
}
.tagline {
  font-size: 14px;
  color: var(--text-muted);
  font-family: var(--font-sans);
  margin-bottom: 16px;
}

.typing-line {
  font-family: var(--font-mono);
  font-size: 13px;
  color: var(--text-accent);
  display: inline-block;
  border-right: 2px solid var(--text-accent);
  padding-right: 2px;
  white-space: nowrap;
  overflow: hidden;
  animation: blink 1s step-end infinite;
  min-height: 20px;
}
@keyframes blink { 0%,100%{border-color:var(--text-accent)} 50%{border-color:transparent} }

.section { margin-bottom: 24px; }
.section-title {
  font-size: 11px;
  font-family: var(--font-mono);
  color: var(--text-muted);
  text-transform: uppercase;
  letter-spacing: 0.1em;
  margin-bottom: 12px;
  display: flex;
  align-items: center;
  gap: 8px;
}
.section-title::after { content: ''; flex: 1; height: 0.5px; background: var(--border); }

.skill-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
  gap: 8px;
}

.skill-card {
  background: var(--surface-2);
  border: 0.5px solid var(--border);
  border-radius: var(--radius);
  padding: 10px 12px;
  display: flex;
  align-items: center;
  gap: 9px;
}
.skill-card.main {
  border-color: var(--border-accent);
  background: var(--bg-accent);
}
.skill-icon { font-size: 18px; color: var(--text-secondary); }
.skill-card.main .skill-icon { color: var(--text-accent); }
.skill-name { font-size: 13px; font-weight: 500; color: var(--text-primary); font-family: var(--font-sans); }
.skill-sub { font-size: 11px; color: var(--text-muted); font-family: var(--font-sans); }

.project-list { display: flex; flex-direction: column; gap: 10px; }
.project-card {
  background: var(--surface-2);
  border: 0.5px solid var(--border);
  border-radius: var(--radius);
  padding: 12px 14px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 12px;
}
.project-info {}
.project-name {
  font-size: 13px;
  font-weight: 500;
  color: var(--text-primary);
  font-family: var(--font-sans);
  margin-bottom: 3px;
}
.project-desc { font-size: 12px; color: var(--text-muted); font-family: var(--font-sans); }
.project-tags { display: flex; gap: 5px; flex-shrink: 0; flex-wrap: wrap; justify-content: flex-end; }
.tag {
  font-size: 11px;
  font-family: var(--font-mono);
  padding: 2px 7px;
  border-radius: 10px;
  border: 0.5px solid var(--border);
  color: var(--text-secondary);
  background: var(--surface-1);
  white-space: nowrap;
}

.lang-bar { margin-top: 6px; }
.lang-row { display: flex; gap: 4px; margin-bottom: 6px; border-radius: 4px; overflow: hidden; height: 8px; }
.lang-seg { height: 100%; }
.lang-legend { display: flex; flex-wrap: wrap; gap: 12px; }
.lang-item { display: flex; align-items: center; gap: 6px; font-size: 12px; font-family: var(--font-sans); color: var(--text-secondary); }
.lang-dot { width: 10px; height: 10px; border-radius: 50%; flex-shrink: 0; }

.connect-row { display: flex; gap: 8px; flex-wrap: wrap; }
.connect-btn {
  font-size: 12px;
  font-family: var(--font-mono);
  padding: 6px 12px;
  border-radius: var(--radius);
  border: 0.5px solid var(--border-strong);
  color: var(--text-secondary);
  background: var(--surface-2);
  cursor: pointer;
  display: flex;
  align-items: center;
  gap: 6px;
  text-decoration: none;
}
.connect-btn:hover { background: var(--surface-1); color: var(--text-primary); }

.footer {
  text-align: center;
  padding-top: 20px;
  border-top: 0.5px solid var(--border);
  margin-top: 24px;
  font-size: 11px;
  font-family: var(--font-mono);
  color: var(--text-muted);
}

.copy-section {
  background: var(--surface-0);
  border: 0.5px solid var(--border);
  border-radius: var(--radius);
  padding: 12px 14px;
  margin-top: 20px;
}
.copy-label { font-size: 11px; font-family: var(--font-mono); color: var(--text-muted); margin-bottom: 8px; }
.copy-btns { display: flex; gap: 8px; flex-wrap: wrap; }
.copy-btn {
  font-size: 12px;
  font-family: var(--font-mono);
  padding: 5px 11px;
  border-radius: var(--radius);
  border: 0.5px solid var(--border-strong);
  color: var(--text-secondary);
  background: var(--surface-2);
  cursor: pointer;
  display: flex;
  align-items: center;
  gap: 5px;
}
.copy-btn:hover { background: var(--surface-1); color: var(--text-primary); }
</style>

<div class="root">
  <div class="toolbar">
    <span class="dot dot-r"></span>
    <span class="dot dot-y"></span>
    <span class="dot dot-g"></span>
    <span class="file-label">README.md — preview</span>
  </div>

  <div class="md">
    <div class="hero">
      <div class="badge-row">
        <span class="badge accent">Unity Game Developer</span>
        <span class="badge">C# · JavaScript · Python · SQL</span>
        <span class="badge">Open to Collabs</span>
      </div>
      <div class="name">EUworron</div>
      <div class="tagline">Building immersive games and side projects that break in interesting ways.</div>
      <div id="typing" class="typing-line"></div>
    </div>

    <div class="section">
      <div class="section-title">stack</div>
      <div class="skill-grid">
        <div class="skill-card main">
          <i class="ti ti-device-gamepad-2 skill-icon" aria-hidden="true"></i>
          <div>
            <div class="skill-name">Unity</div>
            <div class="skill-sub">main engine</div>
          </div>
        </div>
        <div class="skill-card">
          <i class="ti ti-brand-csharp skill-icon" aria-hidden="true"></i>
          <div>
            <div class="skill-name">C#</div>
            <div class="skill-sub">primary language</div>
          </div>
        </div>
        <div class="skill-card">
          <i class="ti ti-code skill-icon" aria-hidden="true"></i>
          <div>
            <div class="skill-name">Godot</div>
            <div class="skill-sub">side projects</div>
          </div>
        </div>
        <div class="skill-card">
          <i class="ti ti-database skill-icon" aria-hidden="true"></i>
          <div>
            <div class="skill-name">SQL / JS</div>
            <div class="skill-sub">web & data</div>
          </div>
        </div>
        <div class="skill-card">
          <i class="ti ti-brand-git skill-icon" aria-hidden="true"></i>
          <div>
            <div class="skill-name">Git & VS</div>
            <div class="skill-sub">day-to-day tools</div>
          </div>
        </div>
        <div class="skill-card">
          <i class="ti ti-cpu skill-icon" aria-hidden="true"></i>
          <div>
            <div class="skill-name">Arduino</div>
            <div class="skill-sub">hardware tinkering</div>
          </div>
        </div>
      </div>
    </div>

    <div class="section">
      <div class="section-title">projects</div>
      <div class="project-list">
        <div class="project-card">
          <div class="project-info">
            <div class="project-name">Hatim (2D RPG)</div>
            <div class="project-desc">Top-down RPG with dialog system, save slots, quests, enemy AI.</div>
          </div>
          <div class="project-tags">
            <span class="tag">Unity</span>
            <span class="tag">C#</span>
            <span class="tag">WIP</span>
          </div>
        </div>
        <div class="project-card">
          <div class="project-info">
            <div class="project-name">HaveIBeenLeaked</div>
            <div class="project-desc">Stealer log search engine — check if your data was exposed.</div>
          </div>
          <div class="project-tags">
            <span class="tag">web</span>
            <span class="tag">JS</span>
          </div>
        </div>
        <div class="project-card">
          <div class="project-info">
            <div class="project-name">2D Engine (Rust)</div>
            <div class="project-desc">Minimal Unity-inspired engine with sprite layers and a Behaviour trait.</div>
          </div>
          <div class="project-tags">
            <span class="tag">Rust</span>
            <span class="tag">minifb</span>
          </div>
        </div>
        <div class="project-card">
          <div class="project-info">
            <div class="project-name">WoT Stats Site</div>
            <div class="project-desc">World of Tanks dashboard using Wargaming API with sortable tables.</div>
          </div>
          <div class="project-tags">
            <span class="tag">Next.js</span>
            <span class="tag">API</span>
          </div>
        </div>
      </div>
    </div>

    <div class="section">
      <div class="section-title">languages</div>
      <div class="lang-bar">
        <div class="lang-row">
          <div class="lang-seg" style="width:55%;background:#3B82F6;"></div>
          <div class="lang-seg" style="width:20%;background:#A78BFA;"></div>
          <div class="lang-seg" style="width:13%;background:#34D399;"></div>
          <div class="lang-seg" style="width:7%;background:#FBBF24;"></div>
          <div class="lang-seg" style="width:5%;background:#F87171;"></div>
        </div>
        <div class="lang-legend">
          <div class="lang-item"><div class="lang-dot" style="background:#3B82F6;"></div>C# 55%</div>
          <div class="lang-item"><div class="lang-dot" style="background:#A78BFA;"></div>JavaScript 20%</div>
          <div class="lang-item"><div class="lang-dot" style="background:#34D399;"></div>Python 13%</div>
          <div class="lang-item"><div class="lang-dot" style="background:#FBBF24;"></div>SQL 7%</div>
          <div class="lang-item"><div class="lang-dot" style="background:#F87171;"></div>Rust 5%</div>
        </div>
      </div>
    </div>

    <div class="section">
      <div class="section-title">connect</div>
      <div class="connect-row">
        <a class="connect-btn" href="mailto:worron.dev@gmail.com">
          <i class="ti ti-mail" aria-hidden="true"></i> worron.dev@gmail.com
        </a>
        <a class="connect-btn" href="https://haveibeenleaked.xyz/" target="_blank">
          <i class="ti ti-external-link" aria-hidden="true"></i> haveibeenleaked.xyz
        </a>
      </div>
    </div>

    <div class="footer">
      made with unity, caffeine, and questionable commit messages.
    </div>

    <div class="copy-section">
      <div class="copy-label">// want to tweak anything? just ask</div>
      <div class="copy-btns">
        <button class="copy-btn" onclick="sendPrompt('Add a GitHub stats widget section to my profile')">
          <i class="ti ti-chart-bar" aria-hidden="true"></i> add stats widget ↗
        </button>
        <button class="copy-btn" onclick="sendPrompt('Generate the full README.md markdown code for my GitHub profile')">
          <i class="ti ti-file-code" aria-hidden="true"></i> export as markdown ↗
        </button>
        <button class="copy-btn" onclick="sendPrompt('Change the vibe of my GitHub profile to more minimalist and dark')">
          <i class="ti ti-palette" aria-hidden="true"></i> change vibe ↗
        </button>
      </div>
    </div>
  </div>
</div>

<script>
const lines = [
  "// currently building: Hatim RPG",
  "// main engine: Unity + C#",
  "// also ships: web apps, tools, experiments",
  "// open to: game dev collabs"
];
let li = 0, ci = 0, del = false;
const el = document.getElementById('typing');
function tick() {
  const t = lines[li];
  if (!del) {
    ci++;
    el.textContent = t.slice(0, ci);
    if (ci === t.length) { del = true; setTimeout(tick, 1800); return; }
  } else {
    ci--;
    el.textContent = t.slice(0, ci);
    if (ci === 0) { del = false; li = (li + 1) % lines.length; setTimeout(tick, 300); return; }
  }
  setTimeout(tick, del ? 30 : 60);
}
tick();
</script>
