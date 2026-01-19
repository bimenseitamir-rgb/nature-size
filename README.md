# nature-size <!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Мир живой природы — Путешествие</title>
<style>
:root{
  --bg:#0b132b;
  --card:#1c2541;
  --accent:#5bc0be;
  --text:#eaeaea;
  --muted:#a7b7c7;
}
*{box-sizing:border-box;}
body{
  margin:0;
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Arial;
  background: radial-gradient(1200px 600px at 20% -10%, #1b2a4a, var(--bg));
  color:var(--text);
  overflow-x:hidden;
}
.screen{
  position:absolute;
  inset:0;
  padding:24px;
  display:none;
  animation: fadeIn .6s ease;
}
.screen.active{display:block;}
header{
  display:flex;
  align-items:center;
  justify-content:space-between;
}
h1,h2,h3{margin:0 0 12px;}
p{line-height:1.6;color:var(--muted);}
.nav{
  position:fixed;
  bottom:18px;
  left:0; right:0;
  display:flex;
  justify-content:center;
  gap:12px;
}
button{
  background: linear-gradient(135deg, var(--accent), #8be9e6);
  border:none;
  color:#052b2b;
  padding:12px 18px;
  border-radius:14px;
  font-weight:700;
  cursor:pointer;
  box-shadow:0 10px 30px rgba(0,0,0,.25);
}
button.secondary{
  background:#243b55;
  color:var(--text);
}
.cards{
  display:grid;
  grid-template-columns: repeat(auto-fit,minmax(220px,1fr));
  gap:16px;
  margin-top:16px;
}
.card{
  background: linear-gradient(180deg, #223b63, var(--card));
  border-radius:18px;
  padding:16px;
  min-height:160px;
  box-shadow: inset 0 0 0 1px rgba(255,255,255,.06), 0 20px 40px rgba(0,0,0,.35);
  transition: transform .3s ease;
}
.card:hover{transform: translateY(-4px);}
.hero{
  display:grid;
  grid-template-columns:1.2fr .8fr;
  gap:18px;
  align-items:center;
}
.art{
  width:100%;
  height:260px;
  border-radius:20px;
  background:
    radial-gradient(120px 120px at 20% 30%, #9ae6b4, transparent 60%),
    radial-gradient(160px 160px at 70% 40%, #63b3ed, transparent 60%),
    linear-gradient(135deg, #1a365d, #2a4365);
}
.quote{
  font-style:italic;
  border-left:4px solid var(--accent);
  padding-left:12px;
  color:#dff;
}
.tag{
  display:inline-block;
  padding:6px 10px;
  border-radius:999px;
  background:#0ea5a4;
  color:#042f2e;
  font-weight:700;
  margin-right:6px;
}
.timeline{
  display:grid;
  grid-template-columns: 1fr 3fr;
  gap:12px;
}
.badge{
  background:#0ea5a4;
  color:#042f2e;
  border-radius:10px;
  padding:6px 10px;
  font-weight:800;
  width:max-content;
}
.video{
  border-radius:18px;
  height:220px;
  background: linear-gradient(135deg,#0f766e,#22d3ee);
  display:flex;
  align-items:center;
  justify-content:center;
  font-size:22px;
  font-weight:900;
  color:#003a3a;
}
@keyframes fadeIn{from{opacity:0; transform:translateY(6px);} to{opacity:1; transform:none;}}
</style>
</head>
<body>

<!-- START -->
<section class="screen active" id="start">
  <header>
    <h1>Мир живой природы 🌍</h1>
    <span class="tag">Интерактивное путешествие</span>
  </header>
  <div class="hero">
    <div>
      <h2>Начать путешествие</h2>
      <p>
        Добро пожаловать в интерактивную презентацию о живой природе Земли.
        Здесь ты увидишь факты, цитаты учёных, красивые сцены и видео-блоки.
        Нажимай кнопки и двигайся дальше — как по сайту.
      </p>
      <div class="quote">
        «В природе нет наград и наказаний — есть последствия.» — Роберт Ингерсолл
      </div>
    </div>
    <div class="art"></div>
  </div>
  <div class="nav">
    <button onclick="go('biodiversity')">🚀 Начать путешествие</button>
  </div>
</section>

<!-- BIODIVERSITY -->
<section class="screen" id="biodiversity">
  <h2>Биоразнообразие</h2>
  <p>
    Биоразнообразие — это разнообразие всех живых организмов на Земле:
    животных, растений, грибов и микроорганизмов.
  </p>
  <div class="cards">
    <div class="card">
      <h3>Факт</h3>
      <p>На Земле описано более <b>2 миллионов</b> видов живых существ.</p>
    </div>
    <div class="card">
      <h3>Факт</h3>
      <p>Каждый год учёные открывают около <b>18 000</b> новых видов.</p>
    </div>
    <div class="card">
      <h3>Цитата</h3>
      <p class="quote">«Разнообразие жизни — это библиотека, которую мы ещё не прочитали.»</p>
    </div>
  </div>
  <div class="nav">
    <button class="secondary" onclick="go('start')">⬅ Назад</button>
    <button onclick="go('ecosystems')">➡ Далее</button>
  </div>
</section>

<!-- ECOSYSTEMS -->
<section class="screen" id="ecosystems">
  <h2>Экосистемы</h2>
  <p>
    Экосистема — это сообщество живых организмов и среды их обитания,
    которые взаимодействуют между собой.
  </p>
  <div class="cards">
    <div class="card">
      <h3>Лес</h3>
      <p>Производит кислород и является домом для 80% наземных видов.</p>
    </div>
    <div class="card">
      <h3>Океан</h3>
      <p>Покрывает 71% Земли и регулирует климат планеты.</p>
    </div>
    <div class="card">
      <h3>Пустыня</h3>
      <p>Несмотря на суровые условия, там существует жизнь.</p>
    </div>
  </div>
  <div class="nav">
    <button class="secondary" onclick="go('biodiversity')">⬅ Назад</button>
    <button onclick="go('evolution')">➡ Далее</button>
  </div>
</section>

<!-- EVOLUTION -->
<section class="screen" id="evolution">
  <h2>Эволюция жизни</h2>
  <div class="timeline">
    <div class="badge">3.8 млрд лет</div>
    <p>Появление первых микроорганизмов.</p>
    <div class="badge">540 млн лет</div>
    <p>Кембрийский взрыв — резкий рост разнообразия жизни.</p>
    <div class="badge">200 тыс. лет</div>
    <p>Появление современного человека.</p>
  </div>
  <div class="quote">
    «Ничто в биологии не имеет смысла, кроме как в свете эволюции.» — Феодосий Добжанский
  </div>
  <div class="nav">
    <button class="secondary" onclick="go('ecosystems')">⬅ Назад</button>
    <button onclick="go('video')">🎬 Видео</button>
  </div>
</section>

<!-- VIDEO -->
<section class="screen" id="video">
  <h2>Видео о живой природе</h2>
  <div class="video">
    ▶ Здесь может быть видео о природе
  </div>
  <p>
    В реальном проекте сюда легко вставляется YouTube или локальное видео
    про животных, леса, океаны и планету Земля.
  </p>
  <div class="nav">
    <button class="secondary" onclick="go('evolution')">⬅ Назад</button>
    <button onclick="go('finish')">🏁 Завершить</button>
  </div>
</section>

<!-- FINISH -->
<section class="screen" id="finish">
  <h2>Береги природу 🌱</h2>
  <p>
    Человек — часть природы. Сохраняя биоразнообразие,
    мы сохраняем будущее планеты и своё собственное.
  </p>
  <div class="quote">
    «Мы не наследуем Землю у наших предков — мы берём её взаймы у наших детей.»
  </div>
  <div class="nav">
    <button onclick="go('start')">🔁 Начать заново</button>
  </div>
</section>

<script>
function go(id){
  document.querySelectorAll('.screen').forEach(s=>s.classList.remove('active'));
  document.getElementById(id).classList.add('active');
}
</script>

</body>
</html>
