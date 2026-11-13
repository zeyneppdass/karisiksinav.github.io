<html>
  <head><meta charset="utf8">
  <meta name="viewport" content="width=device-width,initial-scale=1,viewport-fit=cover">
<style>
  :root{color-scheme:light;box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}html{scroll-padding-top:env(safe-area-inset-top,0px)}body{margin:0;padding:0;font:14px -apple-system,BlinkMacSystemFont,sans-serif;background:#fff;color:#000}img{max-width:100%}[hidden]:not([hidden=until-found i]){display:none!important}
</style>
</head>
<body>
<title>Rehberlik Sınavı</title>
<meta name="claude:viewport-fit-sides" content="cover">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin="">
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=IBM+Plex+Mono:wght@500&amp;family=IBM+Plex+Sans:wght@400;500;600&amp;display=swap">
<style>
/* Layout: tek sütun sınav kâğıdı; üstte sabit sayaç çubuğu, altta soru kartları. Vurgu tek renk (mavi), durum renkleri ayrı. */
:root {
  --bg: #F4F5F8;
  --surface: #FFFFFF;
  --fg: #17202C;
  --muted: #586374;
  --line: #D8DDE5;
  --accent: #2548C8;
  --accent-fg: #FFFFFF;
  --accent-soft: #E6ECFD;
  --good: #146C43;
  --good-bg: #E1F3E8;
  --bad: #AE2A21;
  --bad-bg: #FBE6E3;
  --warn: #8A5700;
  --warn-bg: #FFF1D6;
  --font-text: "IBM Plex Sans", system-ui, -apple-system, "Segoe UI", sans-serif;
  --font-mono: "IBM Plex Mono", ui-monospace, Menlo, Consolas, monospace;
}
@media (prefers-color-scheme: dark) {
  :root:not([data-theme="light"]) {
    --bg: #10151B; --surface: #181F28; --fg: #E7EBF1; --muted: #9AA5B5; --line: #2A3340;
    --accent: #8BA4FF; --accent-fg: #0A1030; --accent-soft: #212C4E;
    --good: #62CF95; --good-bg: #163322; --bad: #FF9087; --bad-bg: #3A1D1B; --warn: #F0BE63; --warn-bg: #3A2D10;
    color-scheme: dark;
  }
}
:root[data-theme="dark"] {
  --bg: #10151B; --surface: #181F28; --fg: #E7EBF1; --muted: #9AA5B5; --line: #2A3340;
  --accent: #8BA4FF; --accent-fg: #0A1030; --accent-soft: #212C4E;
  --good: #62CF95; --good-bg: #163322; --bad: #FF9087; --bad-bg: #3A1D1B; --warn: #F0BE63; --warn-bg: #3A2D10;
  color-scheme: dark;
}
* { box-sizing: border-box; }
body {
  background: var(--bg); color: var(--fg);
  font-family: var(--font-text); font-size: 16px; line-height: 1.55;
  padding-left: max(16px, env(safe-area-inset-left, 0px));
  padding-right: max(16px, env(safe-area-inset-right, 0px));
  padding-block: 20px 56px;
}
body::before { content: ""; position: fixed; inset: 0 0 auto; height: env(safe-area-inset-top, 0px); z-index: 10; background: var(--surface); }
.wrap { max-width: 760px; margin: 0 auto; display: grid; gap: 20px; }
h1, h2, h3, p { margin: 0; }
h1 { font-size: clamp(1.6rem, 4.5vw, 2.1rem); line-height: 1.2; font-weight: 600; text-wrap: balance; letter-spacing: -0.01em; }
h2 { font-size: 1.15rem; font-weight: 600; text-wrap: balance; }
.eyebrow { font-size: .75rem; letter-spacing: .08em; text-transform: uppercase; color: var(--muted); font-weight: 600; }
.mono { font-family: var(--font-mono); font-variant-numeric: tabular-nums; }
button { font: inherit; cursor: pointer; }
:focus-visible { outline: 2px solid var(--accent); outline-offset: 2px; }

.sheet { background: var(--surface); border: 1px solid var(--line); border-radius: 12px; padding: 24px; display: grid; gap: 18px; min-width: 0; }
.meta { display: grid; grid-template-columns: repeat(3, 1fr); gap: 1px; background: var(--line); border: 1px solid var(--line); border-radius: 8px; overflow: hidden; }
.meta div { background: var(--surface); padding: 10px 14px; display: grid; gap: 2px; }
.meta b { font-size: 1.15rem; font-weight: 600; }
.meta span { font-size: .75rem; color: var(--muted); letter-spacing: .04em; text-transform: uppercase; }
.table-scroll { overflow-x: auto; }
table { border-collapse: collapse; width: 100%; font-size: .95rem; }
th, td { text-align: left; padding: 8px 10px; border-bottom: 1px solid var(--line); }
th { font-size: .75rem; letter-spacing: .06em; text-transform: uppercase; color: var(--muted); font-weight: 600; }
td.num, th.num { text-align: right; font-variant-numeric: tabular-nums; white-space: nowrap; }
.field { display: grid; gap: 6px; }
.field label { font-size: .85rem; font-weight: 500; color: var(--muted); }
input[type=text], input[type=number], textarea {
  font: inherit; color: var(--fg); background: var(--bg); border: 1px solid var(--line); border-radius: 8px; padding: 10px 12px; width: 100%;
}
textarea { min-height: 96px; resize: vertical; }
.btn { background: var(--accent); color: var(--accent-fg); border: 1px solid var(--accent); border-radius: 8px; padding: 10px 18px; font-weight: 600; }
.btn.ghost { background: transparent; color: var(--fg); border-color: var(--line); }
.btn:hover { filter: brightness(1.06); }
.rules { color: var(--muted); font-size: .92rem; padding-left: 1.1em; margin: 0; display: grid; gap: 4px; }

/* sticky bar */
.bar { position: sticky; top: env(safe-area-inset-top, 0px); z-index: 5; background: var(--surface); border: 1px solid var(--line); border-radius: 10px; padding: 10px 14px; display: flex; flex-wrap: wrap; align-items: center; gap: 10px 16px; }
.timer { font-family: var(--font-mono); font-size: 1.3rem; font-weight: 500; font-variant-numeric: tabular-nums; }
.timer.low { color: var(--bad); }
.prog { flex: 1 1 140px; display: grid; gap: 4px; min-width: 0; }
.prog small { color: var(--muted); font-size: .8rem; }
.track { height: 6px; background: var(--line); border-radius: 3px; overflow: hidden; }
.track i { display: block; height: 100%; width: 0; background: var(--accent); transition: width .2s; }
.navgrid { display: flex; flex-wrap: wrap; gap: 6px; }
.navgrid button { width: 38px; height: 34px; border: 1px solid var(--line); background: var(--surface); color: var(--fg); border-radius: 6px; font-family: var(--font-mono); font-size: .85rem; }
.navgrid button.done { background: var(--accent-soft); border-color: var(--accent); color: var(--accent); }

.sec-head { display: flex; flex-wrap: wrap; justify-content: space-between; align-items: baseline; gap: 4px 12px; padding-top: 12px; }
.sec-head p { color: var(--muted); font-size: .9rem; }
.q { background: var(--surface); border: 1px solid var(--line); border-radius: 12px; padding: 18px 20px; display: grid; gap: 14px; scroll-margin-top: 110px; min-width: 0; }
.qhead { display: grid; grid-template-columns: auto 1fr; gap: 12px; align-items: start; }
.qn { font-family: var(--font-mono); font-size: .95rem; background: var(--accent-soft); color: var(--accent); border-radius: 6px; min-width: 34px; text-align: center; padding: 2px 8px; }
.qt { overflow-wrap: anywhere; }
.opts { display: grid; gap: 8px; }
.opt { display: grid; grid-template-columns: auto auto 1fr; gap: 10px; align-items: start; border: 1px solid var(--line); border-radius: 8px; padding: 10px 12px; cursor: pointer; min-width: 0; }
.opt input { accent-color: var(--accent); margin-top: 4px; }
.opt .ol { font-family: var(--font-mono); color: var(--muted); }
.opt.sel { background: var(--accent-soft); border-color: var(--accent); }
.tf { grid-template-columns: repeat(2, minmax(0, 1fr)); }
.tf .opt { grid-template-columns: auto 1fr; }
.endrow { display: flex; flex-wrap: wrap; gap: 12px; align-items: center; justify-content: space-between; }

#confirm { position: fixed; left: 0; right: 0; bottom: 0; z-index: 20; background: var(--surface); border-top: 1px solid var(--line); padding: 14px max(16px, env(safe-area-inset-left, 0px)) calc(14px + env(safe-area-inset-bottom, 0px)); }
#confirm > div { max-width: 760px; margin: 0 auto; display: flex; flex-wrap: wrap; gap: 12px; align-items: center; justify-content: space-between; }
#confirm p { flex: 1 1 260px; }
#confirm .acts { display: flex; gap: 8px; }

/* results */
.total { display: flex; flex-wrap: wrap; align-items: baseline; gap: 6px 14px; }
.total .big { font-family: var(--font-mono); font-size: clamp(2.6rem, 9vw, 3.6rem); font-weight: 500; line-height: 1; font-variant-numeric: tabular-nums; }
.total span { color: var(--muted); }
.callout { background: var(--warn-bg); color: var(--warn); border-radius: 8px; padding: 10px 14px; font-size: .92rem; }
.rv { background: var(--surface); border: 1px solid var(--line); border-radius: 12px; padding: 18px 20px; display: grid; gap: 12px; min-width: 0; }
.pill { font-size: .78rem; font-weight: 600; padding: 2px 10px; border-radius: 99px; white-space: nowrap; align-self: start; }
.pill.ok { background: var(--good-bg); color: var(--good); }
.pill.no { background: var(--bad-bg); color: var(--bad); }
.pill.blank { background: var(--warn-bg); color: var(--warn); }
.rvhead { display: grid; grid-template-columns: auto 1fr auto; gap: 12px; align-items: start; }
.ropts { list-style: none; margin: 0; padding: 0; display: grid; gap: 6px; }
.ropts li { border: 1px solid var(--line); border-radius: 8px; padding: 8px 12px; display: flex; flex-wrap: wrap; gap: 4px 10px; justify-content: space-between; }
.ropts li.ok { background: var(--good-bg); border-color: var(--good); }
.ropts li.no { background: var(--bad-bg); border-color: var(--bad); }
.ropts .tag { font-size: .78rem; font-weight: 600; }
.exp { color: var(--muted); font-size: .92rem; }
.given { white-space: pre-wrap; background: var(--bg); border-radius: 8px; padding: 10px 12px; overflow-wrap: anywhere; }
.model { background: var(--good-bg); border-radius: 8px; padding: 10px 14px; display: grid; gap: 6px; font-size: .95rem; }
.model ul { margin: 0; padding-left: 1.1em; display: grid; gap: 3px; }
.scorebox { display: flex; flex-wrap: wrap; align-items: center; gap: 8px 12px; }
.scorebox input { width: 80px; }
.lbl { font-size: .75rem; letter-spacing: .06em; text-transform: uppercase; color: var(--muted); font-weight: 600; }

@media (max-width: 520px) {
  .meta { grid-template-columns: 1fr; }
  .sheet, .q, .rv { padding: 16px; }
  .tf { grid-template-columns: 1fr; }
}
@media (prefers-reduced-motion: reduce) { .track i { transition: none; } }
</style>

<main class="wrap">
  <section id="intro" class="sheet" aria-labelledby="introTitle">
    <div>
      <p class="eyebrow">Üniversite sınavı</p>
      <h1 id="introTitle">Rehberlik ve Psikolojik Danışma</h1>
    </div>
    <div class="meta">
      <div><b>60 dk</b><span>Süre</span></div>
      <div><b>22 soru</b><span>Soru sayısı</span></div>
      <div><b>100</b><span>Toplam puan</span></div>
    </div>
    <div class="table-scroll">
      <table>
        <thead><tr><th>Bölüm</th><th>Soru türü</th><th class="num">Soru × puan</th></tr></thead>
        <tbody>
          <tr><td>I</td><td>Çoktan seçmeli</td><td class="num">10 × 4 = 40</td></tr>
          <tr><td>II</td><td>Doğru / Yanlış</td><td class="num">6 × 3 = 18</td></tr>
          <tr><td>III</td><td>Kısa cevaplı</td><td class="num">4 × 5 = 20</td></tr>
          <tr><td>IV</td><td>Açık uçlu</td><td class="num">2 × 11 = 22</td></tr>
        </tbody>
      </table>
    </div>
    <ul class="rules">
      <li>Süre dolunca sınav kendiliğinden biter.</li>
      <li>Bölüm I ve II otomatik puanlanır. Bölüm III ve IV'ü sınav sonunda cevap anahtarına bakarak kendin puanlarsın.</li>
      <li>Yanlış bulduğun Doğru/Yanlış önermelerini düzeltmen istenir.</li>
    </ul>
    <div class="field">
      <label for="studentName">Ad Soyad (isteğe bağlı)</label>
      <input type="text" id="studentName" autocomplete="off">
    </div>
    <div><button class="btn" id="startBtn" type="button">Sınavı başlat</button></div>
  </section>

  <section id="exam" hidden="">
    <div class="wrap" style="gap:16px">
      <div class="bar" role="group" aria-label="Sınav durumu">
        <div class="timer" id="timer" role="timer" aria-live="off">60:00</div>
        <div class="prog">
          <small id="progText">0 / 22 cevaplandı</small>
          <div class="track"><i id="progBar"></i></div>
        </div>
        <button class="btn ghost" id="finishTop" type="button">Bitir</button>
      </div>
      <nav class="navgrid" id="navgrid" aria-label="Soru gezgini"></nav>
      <div id="questions" class="wrap" style="gap:14px"></div>
      <div class="endrow">
        <p class="exp" id="leftText"></p>
        <button class="btn" id="finishBottom" type="button">Sınavı bitir</button>
      </div>
    </div>
  </section>

  <section id="result" hidden=""></section>
</main>

<div id="confirm" hidden="">
  <div>
    <p id="confirmText"></p>
    <div class="acts">
      <button class="btn ghost" id="confirmNo" type="button">Sınava dön</button>
      <button class="btn" id="confirmYes" type="button">Evet, bitir</button>
    </div>
  </div>
</div>

<script>
(function () {
  var DURATION = 60 * 60 * 1000;

  var Q = [
    { n: 1, t: 'mc', pts: 4, q: 'Aşağıdakilerden hangisi rehberliğin <strong>ne olmadığına</strong> örnektir?',
      o: ['Sistemli ve profesyonel bir yardım sürecidir', 'Bireye öğüt ve nasihat verme işidir', 'Gönüllülüğe dayanır', 'Tüm bireylere yöneliktir'], a: 1,
      e: 'Rehberlik öğüt ve nasihat verme işi değildir; sistemli, gönüllülüğe dayalı ve tüm bireylere yönelik bir yardım sürecidir.' },
    { n: 2, t: 'mc', pts: 4, q: 'Dünyada ilk rehberlik çalışması olan mesleki rehberlik, 1908\'de kim tarafından başlatılmıştır?',
      o: ['Williamson', 'Brewer', 'Frank Parsons', 'Havighurst'], a: 2,
      e: 'Frank Parsons 1908\'de ilk meslek bürosunu açarak işe yerleşmek isteyenlere yardım etti. Bu, özellik-faktör yaklaşımının başlangıcıdır.' },
    { n: 3, t: 'mc', pts: 4, q: 'Okullarda grup rehberliği saatlerinin ayrılmasına yol açan model hangisidir?',
      o: ['Klinik model', 'Eğitimle kaynaştırılmış model', 'Parsons modeli', 'Gelişimsel model'], a: 1,
      e: 'Brewer\'ın eğitimle kaynaştırılmış modeli, rehberliği sınıf içinde verilecek bir hizmet olarak gördüğü için okul programlarında grup rehberliği saatleri ayrılmaya başlandı.' },
    { n: 4, t: 'mc', pts: 4, q: 'Aşağıdakilerden hangisi gelişimsel rehberlik anlayışının özelliklerinden biri <strong>değildir</strong>?',
      o: ['Tüm öğrencilere yöneliktir', 'Önleyici ve geliştiricidir', 'Kriz ve sorun odaklıdır', 'Öğretmen odaklıdır'], a: 2,
      e: 'Kriz ve sorun odaklılık geleneksel rehberliğin özelliğidir. Gelişimsel rehberlik gelişimi kolaylaştırmayı hedefler.' },
    { n: 5, t: 'mc', pts: 4, q: 'Aşağıdakilerden hangisi kapsamlı PDR programının boyutları arasında <strong>yer almaz</strong>?',
      o: ['Rehberlik müfredatı', 'Bireysel planlama', 'Müdahale hizmetleri', 'Disiplin hizmetleri'], a: 3,
      e: 'Dört boyut: rehberlik müfredatı, bireysel planlama, müdahale hizmetleri ve sistem desteği. Disiplin rehberliğin görevi değildir.' },
    { n: 6, t: 'mc', pts: 4, q: 'Öğrencinin anne babasını kaybetmesi sonrasında hemen yapılan rehberlik hangi türdendir?',
      o: ['Önleyici', 'Kriz müdahale', 'Tamamlayıcı', 'Yöneltici'], a: 1,
      e: 'Anne baba kaybı, istismar, doğal afet gibi acil durumlarda sunulan hizmet kriz müdahale rehberliğidir.' },
    { n: 7, t: 'mc', pts: 4, q: 'Grupla psikolojik danışmada grup büyüklüğü genellikle kaç kişidir?',
      o: ['2-3', '6-12', '15-20', '25-30'], a: 1,
      e: 'Grupla psikolojik danışmadaki kişi sayısı genellikle 6-12 arasındadır.' },
    { n: 8, t: 'mc', pts: 4, q: 'Aşağıdakilerden hangisi gizlilik ilkesinin <strong>istisnasıdır</strong>?',
      o: ['Öğrencinin not ortalaması', 'Öğrencinin hayatını tehlikeye sokan intihar girişimi', 'Öğrencinin meslek tercihi', 'Öğrencinin hobileri'], a: 1,
      e: 'Hayati tehlike (intihar, istismar vb.) varsa danışanın izni alınmadan, ama haberdar edilerek gerekli kişilere bilgi verilir.' },
    { n: 9, t: 'mc', pts: 4, q: 'Eğitsel rehberliğin temel amacı aşağıdakilerden hangisidir?',
      o: ['Öğrencinin sınav sonuçlarını yükseltmek', 'Öğrenciye hazır bilgi sunmak', 'Öğrencinin “öğrenmeyi öğrenmesini” sağlamak', 'Öğrencileri disiplin altına almak'], a: 2,
      e: '“Çocuğa balık vermek değil, balık tutmayı öğretmek” eğitsel rehberliğin temel amacını özetler.' },
    { n: 10, t: 'mc', pts: 4, q: 'Aşağıdakilerden hangisi ÖKH\'nin <strong>dolaylı</strong> rehberlik hizmetlerinden biridir?',
      o: ['Bireyi tanıma', 'Oryantasyon', 'Psikolojik danışma', 'Müşavirlik (konsültasyon)'], a: 3,
      e: 'Dolaylı hizmetler: araştırma-değerlendirme, plan ve program hazırlama, müşavirlik, veli ve çevre ile ilişkiler. Diğer şıklar doğrudan hizmetlerdir.' },

    { n: 11, t: 'tf', pts: 3, q: 'Rehberlik hizmetleri yalnızca sorunlu öğrencilere yönelik bir hizmettir.', a: false,
      e: 'Rehberlik tüm öğrencilere yöneliktir.' },
    { n: 12, t: 'tf', pts: 3, q: 'Gelişimsel rehberlik modelini Maslow, Rogers, Mathewson ve Havighurst temsil eder.', a: true,
      e: 'Doğru. Gelişimsel model bu isimlerle anılır ve çağdaş rehberlik modelidir.' },
    { n: 13, t: 'tf', pts: 3, q: 'Kendini gerçekleştirme süreci belirli bir yaşta sona erer.', a: false,
      e: 'Kendini gerçekleştirme süreci yaşam boyu devam eder.' },
    { n: 14, t: 'tf', pts: 3, q: 'Sınav kaygısını tamamen yok etmek eğitsel rehberliğin temel hedefidir.', a: false,
      e: 'Amaç kaygıyı yok etmek değil, kaygıyla yaşamayı öğrenmektir. Normal düzeyde kaygı öğrenme için gereklidir.' },
    { n: 15, t: 'tf', pts: 3, q: 'Klinik model test ve gözlem gibi ölçme araçlarının kullanımına önem verir.', a: true,
      e: 'Doğru. Williamson\'un klinik modeli geçerliği ve güvenirliği yüksek test, gözlem gibi ölçme araçlarını sıklıkla kullanır.' },
    { n: 16, t: 'tf', pts: 3, q: 'Akran danışmanlığında üst sınıftaki uygun nitelikli öğrenciler eğitim alıp denetim altında çalışır.', a: true,
      e: 'Doğru. Üst sınıflardan seçilen öğrenciler eğitim alır ve bir süpervizör denetiminde akranlarına destek olur.' },

    { n: 17, t: 'sa', pts: 5, q: 'Rehberliğin üç işlevini yazınız.',
      m: ['Bireyin kendini tanımasına, anlamasına ve kabul etmesine yardım etmek.', 'Bireyin çevresindeki imkânları fark etmesine yardım etmek.', 'Bireyin potansiyellerini uygun çevre koşullarında kullanmasına yardım etmek.'] },
    { n: 18, t: 'sa', pts: 5, q: 'Kapsamlı PDR programının dört boyutunu sayınız.',
      m: ['Rehberlik müfredatı', 'Bireysel planlama', 'Müdahale hizmetleri', 'Sistem desteği'] },
    { n: 19, t: 'sa', pts: 5, q: 'Kriz müdahale rehberliği ile iyileştirici rehberliği bir cümleyle karşılaştırınız.',
      m: ['Kriz müdahale olay veya problem anında, iyileştirici rehberlik ise olay veya problem sonrasında yapılır.'] },
    { n: 20, t: 'sa', pts: 5, q: 'Sınav kaygısıyla başa çıkmada kullanılabilecek üç bilinçli yöntem yazınız.',
      m: ['Gevşeme ve egzersiz yapma', 'Kaygının kaynağını bulmaya yönelik zihinsel düzenleme', 'Sınavla ilgili yanlış inançları değiştirme', 'Zaman yönetimi', 'Verimli ders çalışma yöntemleri', '(Herhangi üçü yeterlidir.)'] },

    { n: 21, t: 'oe', pts: 11, q: 'Geleneksel ve gelişimsel rehberlik anlayışlarını en az beş açıdan karşılaştırınız.',
      m: ['Kriz ve sorun odaklı ↔ gelişimi sağlayıcı ve kolaylaştırıcı', 'Problemli öğrencilere yönelik ↔ tüm öğrencilere yönelik', 'Uzman odaklı ↔ öğretmen odaklı (sınıf rehber öğretmeni)', 'Tepkisel ↔ önleyici, yaratıcı ve esnek', 'Öğretimden ayrıştırılmış ↔ öğretimle kaynaştırılmış', 'Zaman çizelgesiyle sınırlı ↔ program bütünlüğü içinde, sürekli'],
      r: 'Her doğru karşılaştırma 2 puan (en fazla 10), düzenli anlatım 1 puan.' },
    { n: 22, t: 'oe', pts: 11, q: 'Rehberlik hizmetlerinin ilkelerinden <strong>beş tanesini</strong> açıklayınız. Gizlilik ilkesinin istisnasına mutlaka yer veriniz.',
      m: ['İlkeler: demokratik ve insancıl anlayış, gönüllülük, gizlilik, süreklilik, bireysel farklılıklara saygı, özerklik, tüm öğrencilere yönelik olma, ekip çalışması, planlı ve programlı olma, topluma karşı sorumluluk.', 'Gizlilik istisnası: hayati tehlike (intihar, istismar vb.) varsa danışanın izni alınmadan, ama önceden haberdar edilerek gerekli kişiler bilgilendirilir.'],
      r: 'Her ilke ve açıklaması 2 puan (en fazla 10), gizlilik istisnası 1 puan.' }
  ];

  var SECTIONS = [
    { key: 'mc', roman: 'I', title: 'Çoktan seçmeli', meta: '10 soru × 4 puan', max: 40, auto: true },
    { key: 'tf', roman: 'II', title: 'Doğru / Yanlış', meta: '6 soru × 3 puan · yanlışları düzeltin', max: 18, auto: true },
    { key: 'sa', roman: 'III', title: 'Kısa cevaplı', meta: '4 soru × 5 puan', max: 20, auto: false },
    { key: 'oe', roman: 'IV', title: 'Açık uçlu', meta: '2 soru × 11 puan', max: 22, auto: false }
  ];

  var $ = function (id) { return document.getElementById(id); };
  var ans = {}, fix = {}, manual = {}, timerId = null, endAt = 0, startedAt = 0, name = '', finished = false;

  function esc(s) { return String(s).replace(/[&<>"]/g, function (c) { return { '&': '&amp;', '<': '&lt;', '>': '&gt;', '"': '&quot;' }[c]; }); }
  function isAnswered(q) {
    var v = ans[q.n];
    if (q.t === 'mc' || q.t === 'tf') return v !== undefined;
    return typeof v === 'string' && v.trim() !== '';
  }
  function answeredCount() { return Q.filter(isAnswered).length; }

  /* ---------- exam ---------- */
  function buildExam() {
    var html = '';
    SECTIONS.forEach(function (s) {
      html += '<div class="sec-head"><h2>Bölüm ' + s.roman + ' · ' + s.title + '</h2><p>' + s.meta + '</p></div>';
      Q.filter(function (q) { return q.t === s.key; }).forEach(function (q) {
        html += '<article class="q" id="q' + q.n + '"><div class="qhead"><span class="qn">' + q.n + '</span><p class="qt">' + q.q + '</p></div>';
        if (q.t === 'mc') {
          html += '<div class="opts" role="radiogroup" aria-label="Soru ' + q.n + '">';
          q.o.forEach(function (o, i) {
            html += '<label class="opt"><input type="radio" name="q' + q.n + '" value="' + i + '"><span class="ol">' + 'ABCD'[i] + ')</span><span>' + o + '</span></label>';
          });
          html += '</div>';
        } else if (q.t === 'tf') {
          html += '<div class="opts tf" role="radiogroup" aria-label="Soru ' + q.n + '">' +
            '<label class="opt"><input type="radio" name="q' + q.n + '" value="T"><span>Doğru</span></label>' +
            '<label class="opt"><input type="radio" name="q' + q.n + '" value="F"><span>Yanlış</span></label></div>' +
            '<textarea id="fix' + q.n + '" data-fix="' + q.n + '" placeholder="Yanlış bulduysan önermeyi doğru haliyle yaz (isteğe bağlı)" aria-label="Soru ' + q.n + ' düzeltme"></textarea>';
        } else {
          html += '<textarea id="t' + q.n + '" data-text="' + q.n + '" placeholder="Cevabını buraya yaz" aria-label="Soru ' + q.n + ' cevabı"' + (q.t === 'oe' ? ' style="min-height:180px"' : '') + '></textarea>';
        }
        html += '</article>';
      });
    });
    $('questions').innerHTML = html;
    $('navgrid').innerHTML = Q.map(function (q) { return '<button type="button" data-go="' + q.n + '" id="nv' + q.n + '" aria-label="Soru ' + q.n + '">' + q.n + '</button>'; }).join('');
    refreshProgress();
  }

  function refreshProgress() {
    var c = answeredCount();
    $('progText').textContent = c + ' / ' + Q.length + ' cevaplandı';
    $('progBar').style.width = (c / Q.length * 100) + '%';
    $('leftText').textContent = (Q.length - c) > 0 ? (Q.length - c) + ' soru boş' : 'Tüm sorular cevaplandı';
    Q.forEach(function (q) { var b = $('nv' + q.n); if (b) b.classList.toggle('done', isAnswered(q)); });
  }

  function fmt(ms) {
    var s = Math.max(0, Math.ceil(ms / 1000));
    return String(Math.floor(s / 60)).padStart(2, '0') + ':' + String(s % 60).padStart(2, '0');
  }
  function tick() {
    var left = endAt - Date.now();
    $('timer').textContent = fmt(left);
    $('timer').classList.toggle('low', left <= 5 * 60 * 1000);
    if (left <= 0) finish();
  }

  function start() {
    name = $('studentName').value.trim();
    ans = {}; fix = {}; manual = {}; finished = false;
    buildExam();
    $('intro').hidden = true; $('result').hidden = true; $('exam').hidden = false;
    startedAt = Date.now(); endAt = startedAt + DURATION;
    clearInterval(timerId); timerId = setInterval(tick, 500); tick();
    window.scrollTo(0, 0);
  }

  function askFinish() {
    var left = Q.length - answeredCount();
    $('confirmText').textContent = left > 0 ? left + ' soru boş. Sınavı bitirmek istiyor musun?' : 'Tüm soruları cevapladın. Sınavı bitirmek istiyor musun?';
    $('confirm').hidden = false;
  }

  /* ---------- scoring ---------- */
  function autoScore(q) {
    var v = ans[q.n];
    if (v === undefined) return 0;
    if (q.t === 'mc') return Number(v) === q.a ? q.pts : 0;
    if (q.t === 'tf') return (v === 'T') === q.a ? q.pts : 0;
    return 0;
  }
  function sectionScore(s) {
    return Q.filter(function (q) { return q.t === s.key; }).reduce(function (sum, q) {
      return sum + (s.auto ? autoScore(q) : (manual[q.n] || 0));
    }, 0);
  }
  function totalScore() { return SECTIONS.reduce(function (sum, s) { return sum + sectionScore(s); }, 0); }

  function finish() {
    if (finished) return;
    finished = true;
    clearInterval(timerId);
    $('confirm').hidden = true;
    var used = Math.min(DURATION, Date.now() - startedAt);
    $('exam').hidden = true;
    renderResult(used);
    $('result').hidden = false;
    window.scrollTo(0, 0);
  }

  /* ---------- result ---------- */
  function pill(cls, text) { return '<span class="pill ' + cls + '">' + text + '</span>'; }

  function reviewItem(q) {
    var h = '<article class="rv" id="r' + q.n + '">';
    var v = ans[q.n], head, body = '';
    if (q.t === 'mc') {
      var st = v === undefined ? 'blank' : (Number(v) === q.a ? 'ok' : 'no');
      head = pill(st, (st === 'ok' ? 'Doğru · ' + q.pts : st === 'no' ? 'Yanlış · 0' : 'Boş · 0') + '/' + q.pts);
      body = '<ul class="ropts">' + q.o.map(function (o, i) {
        var cls = i === q.a ? 'ok' : (v !== undefined && Number(v) === i ? 'no' : '');
        var tag = '';
        if (i === q.a && v !== undefined && Number(v) === i) tag = 'Senin cevabın · doğru';
        else if (i === q.a) tag = 'Doğru cevap';
        else if (cls === 'no') tag = 'Senin cevabın';
        return '<li class="' + cls + '"><span><span class="mono">' + 'ABCD'[i] + ')</span> ' + o + '</span>' + (tag ? '<span class="tag">' + tag + '</span>' : '') + '</li>';
      }).join('') + '</ul><p class="exp">' + q.e + '</p>';
    } else if (q.t === 'tf') {
      var okk = v !== undefined && (v === 'T') === q.a;
      var st2 = v === undefined ? 'blank' : (okk ? 'ok' : 'no');
      head = pill(st2, (st2 === 'ok' ? 'Doğru · ' + q.pts : st2 === 'no' ? 'Yanlış · 0' : 'Boş · 0') + '/' + q.pts);
      body = '<p><span class="lbl">Senin cevabın</span><br>' + (v === undefined ? 'Boş bırakıldı' : (v === 'T' ? 'Doğru' : 'Yanlış')) +
        ' &nbsp;·&nbsp; <span class="lbl">Doğru cevap</span> ' + (q.a ? 'Doğru' : 'Yanlış') + '</p>';
      if (fix[q.n] && fix[q.n].trim()) body += '<div><span class="lbl">Düzeltmen</span><div class="given">' + esc(fix[q.n]) + '</div></div>';
      body += '<p class="exp">' + q.e + '</p>';
    } else {
      head = pill('blank', 'Kendin puanla · /' + q.pts);
      body = '<div><span class="lbl">Senin cevabın</span><div class="given">' + (isAnswered(q) ? esc(v) : 'Boş bırakıldı') + '</div></div>' +
        '<div class="model"><span class="lbl">Cevap anahtarı</span><ul>' + q.m.map(function (m) { return '<li>' + m + '</li>'; }).join('') + '</ul>' + (q.r ? '<p class="exp">' + q.r + '</p>' : '') + '</div>' +
        '<div class="scorebox"><label for="s' + q.n + '" class="lbl">Kendi puanın (0-' + q.pts + ')</label><input type="number" id="s' + q.n + '" data-score="' + q.n + '" min="0" max="' + q.pts + '" step="1" value="' + (manual[q.n] || 0) + '"></div>';
    }
    h += '<div class="rvhead"><span class="qn">' + q.n + '</span><p class="qt">' + q.q + '</p>' + head + '</div>' + body + '</article>';
    return h;
  }

  function renderResult(used) {
    var h = '<div class="wrap" style="gap:16px">';
    h += '<div class="sheet"><div><p class="eyebrow">Sınav sonucu' + (name ? ' · ' + esc(name) : '') + '</p><h1>Rehberlik ve Psikolojik Danışma</h1></div>' +
      '<div class="total"><span class="big" id="totalBig">0</span><span>/ 100 puan · <span id="totalPct">0</span>% · kullanılan süre <span class="mono">' + fmt(used) + '</span></span></div>' +
      '<div class="track"><i id="totalBar"></i></div>' +
      '<div class="table-scroll"><table><thead><tr><th>Bölüm</th><th>Puanlama</th><th class="num">Puan</th></tr></thead><tbody>' +
      SECTIONS.map(function (s) { return '<tr><td>' + s.roman + ' · ' + s.title + '</td><td>' + (s.auto ? 'Otomatik' : 'Kendin') + '</td><td class="num"><span id="sec-' + s.key + '">0</span> / ' + s.max + '</td></tr>'; }).join('') +
      '</tbody></table></div>' +
      '<p class="callout">Bölüm III ve IV otomatik puanlanmaz. Cevaplarını cevap anahtarıyla karşılaştırıp her soru için kendi puanını gir; toplam kendiliğinden güncellenir.</p>' +
      '<div><button class="btn" id="retryBtn" type="button">Sınavı yeniden çöz</button></div></div>';
    SECTIONS.forEach(function (s) {
      h += '<div class="sec-head"><h2>Bölüm ' + s.roman + ' · ' + s.title + '</h2><p>' + s.meta + '</p></div>';
      Q.filter(function (q) { return q.t === s.key; }).forEach(function (q) { h += reviewItem(q); });
    });
    h += '</div>';
    $('result').innerHTML = h;
    updateTotals();
  }

  function updateTotals() {
    SECTIONS.forEach(function (s) { $('sec-' + s.key).textContent = sectionScore(s); });
    var t = totalScore();
    $('totalBig').textContent = t;
    $('totalPct').textContent = t;
    $('totalBar').style.width = t + '%';
  }

  /* ---------- events ---------- */
  $('startBtn').addEventListener('click', start);
  $('finishTop').addEventListener('click', askFinish);
  $('finishBottom').addEventListener('click', askFinish);
  $('confirmNo').addEventListener('click', function () { $('confirm').hidden = true; });
  $('confirmYes').addEventListener('click', finish);

  $('navgrid').addEventListener('click', function (e) {
    var b = e.target.closest('[data-go]');
    if (!b) return;
    var el = $('q' + b.getAttribute('data-go'));
    if (el) el.scrollIntoView({ behavior: window.matchMedia('(prefers-reduced-motion: reduce)').matches ? 'auto' : 'smooth', block: 'start' });
  });

  $('questions').addEventListener('change', function (e) {
    var t = e.target;
    if (t.type !== 'radio') return;
    var n = Number(t.name.slice(1));
    ans[n] = t.value;
    var group = $('questions').querySelectorAll('input[name="q' + n + '"]');
    group.forEach(function (r) { r.closest('.opt').classList.toggle('sel', r.checked); });
    refreshProgress();
  });
  $('questions').addEventListener('input', function (e) {
    var t = e.target;
    if (t.dataset.text) { ans[Number(t.dataset.text)] = t.value; refreshProgress(); }
    else if (t.dataset.fix) { fix[Number(t.dataset.fix)] = t.value; }
  });

  $('result').addEventListener('input', function (e) {
    var t = e.target;
    if (!t.dataset.score) return;
    var n = Number(t.dataset.score), q = Q.filter(function (x) { return x.n === n; })[0];
    var v = parseInt(t.value, 10);
    if (isNaN(v)) v = 0;
    manual[n] = Math.max(0, Math.min(q.pts, v));
    updateTotals();
  });
  $('result').addEventListener('change', function (e) {
    var t = e.target;
    if (t.dataset.score) t.value = manual[Number(t.dataset.score)] || 0;
  });
  $('result').addEventListener('click', function (e) {
    if (e.target.id === 'retryBtn') {
      $('result').hidden = true; $('intro').hidden = false;
      window.scrollTo(0, 0);
    }
  });
})();
</script>

</body></html>
