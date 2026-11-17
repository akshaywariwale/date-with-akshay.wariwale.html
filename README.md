# file-home-Dhaninfo-Downloads-date-invite-standalone-1-.html
#dating site

<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Date Invitation</title>
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,500;0,9..144,700;1,9..144,500&family=DM+Sans:wght@400;500;700&display=swap">
<style>
/* Layout: one centered card-less stage, one question per screen, wine-night ground with a rose accent */
:root {
  --bg: #1b0f1e;
  --surface: #2b1832;
  --surface-hi: #3a2243;
  --line: #4d3158;
  --ink: #fdf0f2;
  --muted: #cdaebe;
  --accent: #ff6f86;
  --accent-ink: #2a0b14;
  --gold: #ffd58a;
  --display: "Fraunces", Georgia, "Times New Roman", serif;
  --body: "DM Sans", system-ui, -apple-system, "Segoe UI", sans-serif;
  color-scheme: dark;
}
* { box-sizing: border-box; }
html, body { min-height: 100%; }
body {
  background: var(--bg);
  color: var(--ink);
  font-family: var(--body);
  font-size: 16px;
  line-height: 1.5;
  padding-left: max(16px, env(safe-area-inset-left, 0px));
  padding-right: max(16px, env(safe-area-inset-right, 0px));
  padding-block: 28px 40px;
  background-image:
    radial-gradient(60rem 30rem at 85% -10%, rgba(255,111,134,.22), transparent 60%),
    radial-gradient(50rem 30rem at -10% 110%, rgba(255,213,138,.10), transparent 60%);
  background-attachment: fixed;
}
.hearts { position: fixed; inset: 0; pointer-events: none; overflow: hidden; z-index: 0; }
.hearts svg { position: absolute; bottom: -60px; width: 28px; height: 28px; color: var(--accent); opacity: .14; animation: rise 16s linear infinite; }
.hearts svg:nth-child(1) { left: 8%;  animation-duration: 18s; }
.hearts svg:nth-child(2) { left: 26%; animation-duration: 14s; animation-delay: -6s; width: 18px; height: 18px; }
.hearts svg:nth-child(3) { left: 47%; animation-duration: 20s; animation-delay: -11s; }
.hearts svg:nth-child(4) { left: 66%; animation-duration: 15s; animation-delay: -3s; width: 20px; height: 20px; }
.hearts svg:nth-child(5) { left: 82%; animation-duration: 19s; animation-delay: -9s; width: 34px; height: 34px; }
.hearts svg:nth-child(6) { left: 94%; animation-duration: 13s; animation-delay: -5s; width: 16px; height: 16px; }
@keyframes rise { to { transform: translateY(-115vh) rotate(18deg); } }

.stage { position: relative; z-index: 1; width: 100%; max-width: 520px; margin: 0 auto; }
.progress { display: flex; gap: 8px; margin-bottom: 36px; }
.progress i { flex: 1; height: 4px; border-radius: 4px; background: var(--line); transition: background .3s; }
.progress i.on { background: var(--accent); }

.step { display: flex; flex-direction: column; gap: 22px; animation: in .45s ease both; }
@keyframes in { from { opacity: 0; transform: translateY(10px); } to { opacity: 1; transform: none; } }
.eyebrow { font-size: 12px; letter-spacing: .14em; text-transform: uppercase; color: var(--gold); font-weight: 700; margin: 0; }
h1, h2 { font-family: var(--display); font-weight: 700; line-height: 1.08; margin: 0; text-wrap: balance; }
h1 { font-size: clamp(2.3rem, 9vw, 3.4rem); }
h1 em { font-style: italic; font-weight: 500; color: var(--accent); }
h2 { font-size: clamp(1.8rem, 7vw, 2.4rem); }
h1:focus, h2:focus { outline: none; }
.lede { color: var(--muted); margin: 0; max-width: 46ch; }

.row { display: flex; flex-wrap: wrap; gap: 12px; }
.btn {
  font: inherit; font-weight: 700; cursor: pointer;
  border-radius: 999px; padding: 14px 28px; min-height: 52px;
  border: 2px solid var(--line); background: transparent; color: var(--ink);
  transition: transform .15s, background .2s, border-color .2s, opacity .2s;
}
.btn:hover:not(:disabled) { transform: translateY(-1px); border-color: var(--muted); }
.btn.primary { background: var(--accent); border-color: var(--accent); color: var(--accent-ink); }
.btn.primary:hover:not(:disabled) { background: #ff8a9d; border-color: #ff8a9d; }
.btn:disabled { opacity: .4; cursor: not-allowed; }
.btn.big { flex: 1 1 140px; font-size: 1.1rem; }
:focus-visible { outline: 3px solid var(--gold); outline-offset: 3px; }

/* calendar */
.cal { background: var(--surface); border: 1px solid var(--line); border-radius: 20px; padding: 16px; }
.cal-head { display: flex; align-items: center; justify-content: space-between; margin-bottom: 10px; }
.cal-head strong { font-family: var(--display); font-size: 1.25rem; font-weight: 700; }
.cal-nav { width: 44px; height: 44px; border-radius: 50%; border: 1px solid var(--line); background: transparent; color: var(--ink); font-size: 1.1rem; cursor: pointer; }
.cal-nav:disabled { opacity: .3; cursor: not-allowed; }
.cal-grid { display: grid; grid-template-columns: repeat(7, minmax(0, 1fr)); gap: 4px; }
.cal-grid .dow { text-align: center; font-size: 12px; color: var(--muted); padding: 6px 0; letter-spacing: .05em; }
.day { aspect-ratio: 1; max-width: 100%; border: 0; border-radius: 12px; background: transparent; color: var(--ink); font: inherit; font-variant-numeric: tabular-nums; cursor: pointer; }
.day:hover:not(:disabled) { background: var(--surface-hi); }
.day:disabled { color: #7d6488; cursor: not-allowed; }
.day[aria-pressed="true"] { background: var(--accent); color: var(--accent-ink); font-weight: 700; }
.pick { margin: 0; color: var(--gold); font-weight: 500; min-height: 1.5em; }

/* time + food */
.times { display: grid; grid-template-columns: repeat(auto-fill, minmax(104px, 1fr)); gap: 10px; }
.chip {
  font: inherit; font-weight: 500; font-variant-numeric: tabular-nums; cursor: pointer;
  padding: 14px 8px; border-radius: 14px; min-height: 52px;
  border: 1px solid var(--line); background: var(--surface); color: var(--ink);
  transition: background .2s, border-color .2s, transform .15s;
}
.chip:hover { border-color: var(--muted); }
.chip[aria-pressed="true"] { background: var(--accent); border-color: var(--accent); color: var(--accent-ink); font-weight: 700; }
.foods { display: grid; grid-template-columns: repeat(3, minmax(0, 1fr)); gap: 10px; }
.food {
  font: inherit; cursor: pointer; display: flex; flex-direction: column; align-items: center; gap: 4px;
  padding: 14px 4px 12px; border-radius: 18px; border: 1px solid var(--line); background: var(--surface); color: var(--ink);
  transition: background .2s, border-color .2s, transform .15s;
  min-width: 0;
}
.food .pic { font-size: 2.6rem; line-height: 1.1; transition: transform .2s; }
.food .nm { font-size: .92rem; font-weight: 500; overflow-wrap: anywhere; }
.food:hover { border-color: var(--muted); }
.food:hover .pic { transform: scale(1.12) rotate(-4deg); }
.food[aria-pressed="true"] { background: var(--surface-hi); border-color: var(--accent); box-shadow: inset 0 0 0 1px var(--accent); }
.food[aria-pressed="true"] .nm { color: var(--accent); font-weight: 700; }

/* movies */
.movies { display: grid; grid-template-columns: repeat(auto-fill, minmax(230px, 1fr)); gap: 10px; }
.movie {
  font: inherit; cursor: pointer; display: flex; align-items: flex-start; gap: 12px; text-align: left;
  padding: 14px; border-radius: 18px; border: 1px solid var(--line); background: var(--surface); color: var(--ink);
  transition: background .2s, border-color .2s; min-width: 0;
}
.movie .pic { font-size: 2.1rem; line-height: 1; flex: none; }
.movie .mt { display: flex; flex-direction: column; gap: 2px; min-width: 0; }
.movie .nm { font-weight: 700; line-height: 1.25; overflow-wrap: anywhere; }
.movie .mg { font-size: .85rem; color: var(--muted); overflow-wrap: anywhere; }
.movie .badge { font-size: .75rem; letter-spacing: .06em; text-transform: uppercase; font-weight: 700; color: var(--gold); margin-top: 4px; }
.movie:hover:not(:disabled) { border-color: var(--muted); }
.movie[aria-pressed="true"] { background: var(--surface-hi); border-color: var(--accent); box-shadow: inset 0 0 0 1px var(--accent); }
.movie[aria-pressed="true"] .nm { color: var(--accent); }
.movie:disabled { opacity: .45; cursor: not-allowed; }
.movie:disabled .badge { color: var(--muted); }
.skip { align-self: flex-start; padding-inline: 20px; }

/* confirmation */
.big-heart { width: 72px; height: 72px; color: var(--accent); animation: beat 1.6s ease-in-out infinite; }
@keyframes beat { 0%, 100% { transform: scale(1); } 15% { transform: scale(1.15); } 30% { transform: scale(1); } 45% { transform: scale(1.1); } }
.summary { display: grid; gap: 0; background: var(--surface); border: 1px solid var(--line); border-radius: 20px; overflow: hidden; margin: 0; }
.summary div { display: grid; grid-template-columns: 5.5rem minmax(0, 1fr); gap: 12px; padding: 14px 18px; border-top: 1px solid var(--line); }
.summary div:first-child { border-top: 0; }
.summary dt { color: var(--muted); font-size: 13px; letter-spacing: .08em; text-transform: uppercase; align-self: center; }
.summary dd { margin: 0; font-weight: 500; overflow-wrap: anywhere; }
.note { color: var(--muted); font-size: 14px; margin: 0; }
.foot-pics { font-size: 1.7rem; letter-spacing: .15em; }

@media (prefers-reduced-motion: reduce) {
  .hearts svg, .big-heart, .step { animation: none; }
  .btn, .chip, .food, .food .pic { transition: none; }
}
a.btn { text-decoration: none; display: inline-flex; align-items: center; justify-content: center; }
[hidden] { display: none !important; }
body { margin: 0; }
</style>

</head>
<body>
<svg width="0" height="0" style="position:absolute" aria-hidden="true">
  <symbol id="heart" viewBox="0 0 24 24"><path fill="currentColor" d="M12 21s-7.5-4.6-9.6-9.3C.8 8.2 2.7 4.5 6.3 4.5c2 0 3.6 1.1 4.4 2.6.3.5 1.3.5 1.6 0 .8-1.5 2.4-2.6 4.4-2.6 3.6 0 5.5 3.7 3.9 7.2C19.5 16.4 12 21 12 21z"/></symbol>
</svg>
<div class="hearts" aria-hidden="true">
  <svg><use href="#heart"/></svg><svg><use href="#heart"/></svg><svg><use href="#heart"/></svg>
  <svg><use href="#heart"/></svg><svg><use href="#heart"/></svg><svg><use href="#heart"/></svg>
</div>

<main class="stage">
  <div class="progress" id="progress" aria-hidden="true"><i></i><i></i><i></i><i></i><i></i></div>

  <section class="step" id="s-q">
    <p class="eyebrow">A question worth asking</p>
    <h1 tabindex="-1">Will you go on a <em>date</em> with me?</h1>
    <p class="lede">No pressure at all. Whatever you pick, I will be happy you took a moment to answer.</p>
    <div class="row">
      <button class="btn primary big" id="yes" type="button">Yes</button>
      <button class="btn big" id="no" type="button">No</button>
    </div>
  </section>

  <section class="step" id="s-no" hidden>
    <p class="eyebrow">Thank you</p>
    <h2 tabindex="-1">That is completely okay.</h2>
    <p class="lede">I appreciate you being honest with me. I hope your day is a good one.</p>
    <div class="row"><a class="btn primary" id="send-mail-no" hidden target="_blank" rel="noopener">Let me know by email</a><button class="btn" id="undo" type="button">I changed my mind</button></div>
  </section>

  <section class="step" id="s-day" hidden>
    <p class="eyebrow">Yes. Now the day</p>
    <h2 tabindex="-1">Which day works for you?</h2>
    <div class="cal">
      <div class="cal-head">
        <button class="cal-nav" id="prev" type="button" aria-label="Previous month">&#8592;</button>
        <strong id="cal-title"></strong>
        <button class="cal-nav" id="next" type="button" aria-label="Next month">&#8594;</button>
      </div>
      <div class="cal-grid" id="cal-grid"></div>
    </div>
    <p class="pick" id="pick-day" aria-live="polite"></p>
    <div class="row">
      <button class="btn" data-back="q" type="button">Back</button>
      <button class="btn primary" id="day-next" type="button" disabled>Choose the time</button>
    </div>
  </section>

  <section class="step" id="s-time" hidden>
    <p class="eyebrow" id="time-eyebrow">Now the time</p>
    <h2 tabindex="-1">What time suits you?</h2>
    <div class="times" id="times"></div>
    <div class="row">
      <button class="btn" data-back="day" type="button">Back</button>
      <button class="btn primary" id="time-next" type="button" disabled>Choose the food</button>
    </div>
  </section>

  <section class="step" id="s-food" hidden>
    <p class="eyebrow">Almost there</p>
    <h2 tabindex="-1">What shall we eat?</h2>
    <p class="lede">Tap as many as you like.</p>
    <div class="foods" id="foods"></div>
    <div class="row">
      <button class="btn" data-back="time" type="button">Back</button>
      <button class="btn primary" id="go" type="button" disabled>Choose the movie</button>
    </div>
  </section>

  <section class="step" id="s-movie" hidden>
    <p class="eyebrow">Last thing</p>
    <h2 tabindex="-1">Which movie shall we watch?</h2>
    <p class="lede" id="movie-lede">Films that are in cinemas on your day.</p>
    <div class="movies" id="movies"></div>
    <button class="chip skip" id="movie-none" type="button" aria-pressed="false">Skip the movie, just us</button>
    <p class="note">Release dates come from Esquire India and Filmibeat. Showtimes can change, so check before booking.</p>
    <div class="row">
      <button class="btn" data-back="food" type="button">Back</button>
      <button class="btn primary" id="finish" type="button" disabled>Let's go</button>
    </div>
  </section>

  <section class="step" id="s-done" hidden>
    <svg class="big-heart" aria-hidden="true"><use href="#heart"/></svg>
    <p class="eyebrow">It is a date</p>
    <h2 tabindex="-1">I will see you there.</h2>
    <dl class="summary">
      <div><dt>Day</dt><dd id="sum-day"></dd></div>
      <div><dt>Time</dt><dd id="sum-time"></dd></div>
      <div><dt>Food</dt><dd id="sum-food"></dd></div>
      <div><dt>Movie</dt><dd id="sum-movie"></dd></div>
    </dl>
    <p class="foot-pics" id="sum-pics" aria-hidden="true"></p>
    <p class="note" id="save-note" aria-live="polite"></p>
    <div class="row">
      <a class="btn primary" id="send-mail" hidden target="_blank" rel="noopener">Send by email</a>
      <a class="btn primary" id="send-wa" hidden target="_blank" rel="noopener">Send on WhatsApp</a>
      <button class="btn" id="copy" type="button">Copy these details</button>
      <button class="btn" id="redo" type="button">Change something</button>
    </div>
  </section>
</main>

<script>
(function () {
  /* ---- FILL THESE IN BEFORE YOU PUBLISH ---- */
  var YOUR_EMAIL = "";      /* e.g. "you@example.com" : answers arrive here */
  var YOUR_WHATSAPP = "";   /* digits only with country code, e.g. "919876543210" */
  /* ------------------------------------------ */
  var FOODS = [
    { n: "Sushi", e: "🍣" }, { n: "Pasta", e: "🍝" }, { n: "Pizza", e: "🍕" },
    { n: "Biryani", e: "🍛" }, { n: "Kebabs", e: "🍢" }, { n: "Tacos", e: "🌮" },
    { n: "Ramen", e: "🍜" }, { n: "Burgers", e: "🍔" }, { n: "Dessert", e: "🍰" }
  ];
  var TIMES = ["12:30 PM", "1:30 PM", "4:00 PM", "5:30 PM", "7:00 PM", "8:00 PM", "9:00 PM"];
  var MOVIES = [
    { id: "ramayana", t: "Ramayana: Rise of a Legend, Part One", g: "Mythological epic", c: "Ranbir Kapoor, Sai Pallavi", d: "2026-11-05", e: "🏹" },
    { id: "wildwood", t: "Wildwood", g: "Animated fantasy adventure", c: "", d: "2026-11-13", e: "🌲" },
    { id: "rocky", t: "I Play Rocky", g: "Biographical drama", c: "Anthony Ippolito, Anna Sophia Robb", d: "2026-11-13", e: "🥊" },
    { id: "ghost", t: "Ghost Soldier", g: "Action thriller", c: "Jim Caviezel", d: "2026-11-13", e: "🪖" },
    { id: "heist", t: "How to Rob a Bank", g: "Action comedy heist", c: "", d: "2026-11-19", e: "💰" },
    { id: "hunger", t: "The Hunger Games: Sunrise on the Reaping", g: "Young-adult dystopian", c: "", d: "2026-11-20", e: "🔥" },
    { id: "godzilla", t: "Godzilla Minus Zero", g: "Kaiju", c: "", d: "2026-11-20", e: "🦖" },
    { id: "suryaa", t: "Suryaa: Ant Se Aarambh Tak", g: "Hindi crime thriller", c: "Sunny Deol", d: "2026-11-20", e: "🎬" },
    { id: "prem", t: "Yeh Prem Mol Liya", g: "Romantic family musical", c: "Ayushmann Khurrana, Sharvari", d: "2026-11-27", e: "💞" },
    { id: "g9", t: "Gunmaaster G9", g: "Hindi action drama", c: "Emraan Hashmi", d: "2026-11-27", e: "🎯" }
  ];
  var STEPS = ["q", "no", "day", "time", "food", "movie", "done"];
  var PROG = { q: 0, no: 0, day: 1, time: 2, food: 3, movie: 4, done: 4 };
  var state = { date: null, time: null, foods: [], movie: null };

  function $(id) { return document.getElementById(id); }
  function pad(n) { return (n < 10 ? "0" : "") + n; }
  function key(d) { return d.getFullYear() + "-" + pad(d.getMonth() + 1) + "-" + pad(d.getDate()); }
  function longDate(d) { return d.toLocaleDateString(undefined, { weekday: "long", day: "numeric", month: "long", year: "numeric" }); }

  function go(name) {
    STEPS.forEach(function (s) { $("s-" + s).hidden = s !== name; });
    var dots = $("progress").children, p = PROG[name];
    for (var i = 0; i < dots.length; i++) dots[i].className = i <= p ? "on" : "";
    var h = $("s-" + name).querySelector("h1,h2");
    if (h) { try { h.focus({ preventScroll: true }); } catch (e) {} }
    window.scrollTo(0, 0);
  }


  /* calendar */
  var now = new Date();
  var minDate = new Date(now.getFullYear(), now.getMonth(), now.getDate() + 1);
  var firstView = new Date(minDate.getFullYear(), minDate.getMonth(), 1);
  var lastView = new Date(minDate.getFullYear(), minDate.getMonth() + 2, 1);
  var view = new Date(firstView.getTime());

  function renderCal() {
    $("cal-title").textContent = view.toLocaleDateString(undefined, { month: "long", year: "numeric" });
    $("prev").disabled = view.getTime() <= firstView.getTime();
    $("next").disabled = view.getTime() >= lastView.getTime();
    var grid = $("cal-grid"); grid.innerHTML = "";
    ["Mon", "Tue", "Wed", "Thu", "Fri", "Sat", "Sun"].forEach(function (d) {
      var s = document.createElement("div"); s.className = "dow"; s.textContent = d; grid.appendChild(s);
    });
    var y = view.getFullYear(), m = view.getMonth();
    var offset = (new Date(y, m, 1).getDay() + 6) % 7;
    var count = new Date(y, m + 1, 0).getDate();
    for (var i = 0; i < offset; i++) grid.appendChild(document.createElement("div"));
    for (var d = 1; d <= count; d++) {
      var dt = new Date(y, m, d);
      var b = document.createElement("button");
      b.type = "button"; b.className = "day"; b.textContent = d;
      b.setAttribute("aria-label", longDate(dt));
      b.disabled = dt < minDate;
      b.setAttribute("aria-pressed", state.date && key(state.date) === key(dt) ? "true" : "false");
      (function (dtc) { b.addEventListener("click", function () { state.date = dtc; renderCal(); showPick(); }); })(dt);
      grid.appendChild(b);
    }
  }
  function showPick() {
    $("pick-day").textContent = state.date ? longDate(state.date) : "";
    $("day-next").disabled = !state.date;
  }

  /* times */
  function renderTimes() {
    var box = $("times"); box.innerHTML = "";
    TIMES.forEach(function (t) {
      var b = document.createElement("button");
      b.type = "button"; b.className = "chip"; b.textContent = t;
      b.setAttribute("aria-pressed", state.time === t ? "true" : "false");
      b.addEventListener("click", function () { state.time = t; renderTimes(); $("time-next").disabled = false; });
      box.appendChild(b);
    });
    $("time-next").disabled = !state.time;
    $("time-eyebrow").textContent = state.date ? longDate(state.date) : "Now the time";
  }

  /* food */
  function renderFoods() {
    var box = $("foods"); box.innerHTML = "";
    FOODS.forEach(function (f) {
      var b = document.createElement("button");
      b.type = "button"; b.className = "food";
      b.setAttribute("aria-pressed", state.foods.indexOf(f.n) >= 0 ? "true" : "false");
      b.innerHTML = '<span class="pic" aria-hidden="true">' + f.e + '</span><span class="nm">' + f.n + "</span>";
      b.addEventListener("click", function () {
        var i = state.foods.indexOf(f.n);
        if (i >= 0) state.foods.splice(i, 1); else state.foods.push(f.n);
        renderFoods();
      });
      box.appendChild(b);
    });
    $("go").disabled = state.foods.length === 0;
  }

  /* movies: only films already out on the chosen day can be picked */
  function movieById(id) { return MOVIES.filter(function (m) { return m.id === id; })[0]; }
  function movieName() { return state.movie && state.movie !== "none" ? movieById(state.movie).t : "No movie, just us"; }
  function renderMovies() {
    var dayKey = key(state.date), todayKey = key(new Date());
    var cur = state.movie && state.movie !== "none" ? movieById(state.movie) : null;
    if (cur && cur.d > dayKey) state.movie = null;
    $("movie-lede").textContent = "Films in cinemas on " + longDate(state.date) + ".";
    var box = $("movies"); box.innerHTML = "";
    MOVIES.forEach(function (m) {
      var out = m.d <= dayKey;
      var label = m.d <= todayKey ? "In cinemas now"
        : (out ? "Opens " : "Not out on your day, opens ") + new Date(m.d + "T00:00:00").toLocaleDateString(undefined, { day: "numeric", month: "short" });
      var b = document.createElement("button");
      b.type = "button"; b.className = "movie"; b.disabled = !out;
      b.setAttribute("aria-pressed", state.movie === m.id ? "true" : "false");
      var meta = m.g + (m.c ? " · " + m.c : "");
      b.innerHTML = '<span class="pic" aria-hidden="true">' + m.e + '</span><span class="mt"><span class="nm"></span><span class="mg"></span><span class="badge"></span></span>';
      b.querySelector(".nm").textContent = m.t;
      b.querySelector(".mg").textContent = meta;
      b.querySelector(".badge").textContent = label;
      b.addEventListener("click", function () { state.movie = m.id; renderMovies(); });
      box.appendChild(b);
    });
    $("movie-none").setAttribute("aria-pressed", state.movie === "none" ? "true" : "false");
    $("finish").disabled = !state.movie;
  }

  function setupLinks(text) {
    var enc = encodeURIComponent(text);
    var digits = YOUR_WHATSAPP.replace(/\D/g, "");
    var mail = YOUR_EMAIL ? "mailto:" + YOUR_EMAIL + "?subject=" + encodeURIComponent("My answer") + "&body=" + enc : "";
    var wa = digits ? "https://wa.me/" + digits + "?text=" + enc : "";
    [["send-mail", mail], ["send-mail-no", mail], ["send-wa", wa]].forEach(function (p) {
      var a = $(p[0]); if (!a) return;
      a.hidden = !p[1]; if (p[1]) a.href = p[1];
    });
    $("save-note").textContent = (mail || wa)
      ? "Tap a button to send me your answer."
      : "Copy the details below and send them to me.";
  }

  function summaryText() {
    return "Yes, it's a date! " + longDate(state.date) + " at " + state.time + ". Food: " + state.foods.join(", ") + ". Movie: " + movieName() + ".";
  }

  /* wiring */
  $("yes").addEventListener("click", function () { renderCal(); showPick(); go("day"); });
  $("no").addEventListener("click", function () { setupLinks("No, thank you. Thanks for asking me."); go("no"); });
  $("undo").addEventListener("click", function () { go("q"); });
  $("prev").addEventListener("click", function () { view = new Date(view.getFullYear(), view.getMonth() - 1, 1); renderCal(); });
  $("next").addEventListener("click", function () { view = new Date(view.getFullYear(), view.getMonth() + 1, 1); renderCal(); });
  $("day-next").addEventListener("click", function () { renderTimes(); go("time"); });
  $("time-next").addEventListener("click", function () { renderFoods(); go("food"); });
  document.querySelectorAll("[data-back]").forEach(function (b) {
    b.addEventListener("click", function () {
      var to = b.getAttribute("data-back");
      if (to === "day") { renderCal(); showPick(); }
      if (to === "time") renderTimes();
      if (to === "food") renderFoods();
      go(to);
    });
  });
  $("go").addEventListener("click", function () { renderMovies(); go("movie"); });
  $("movie-none").addEventListener("click", function () { state.movie = "none"; renderMovies(); });
  $("finish").addEventListener("click", function () {
    $("sum-movie").textContent = movieName();
    $("sum-day").textContent = longDate(state.date);
    $("sum-time").textContent = state.time;
    $("sum-food").textContent = state.foods.join(", ");
    var pics = FOODS.filter(function (f) { return state.foods.indexOf(f.n) >= 0; }).map(function (f) { return f.e; }).join(" ");
    $("sum-pics").textContent = pics;
    setupLinks(summaryText());
    go("done");
  });
  $("redo").addEventListener("click", function () { renderCal(); showPick(); go("day"); });
  $("copy").addEventListener("click", function () {
    var text = summaryText(), btn = $("copy");
    function ok() { btn.textContent = "Copied"; setTimeout(function () { btn.textContent = "Copy these details"; }, 1800); }
    function fallback() {
      var r = document.createRange(); r.selectNodeContents($("sum-food").parentNode.parentNode);
      var s = window.getSelection(); s.removeAllRanges(); s.addRange(r);
      btn.textContent = "Selected, press copy";
    }
    try { navigator.clipboard.writeText(text).then(ok, fallback); } catch (e) { fallback(); }
  });

  go("q");
})();
</script>

</body>
</html>
