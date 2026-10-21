<title>영무 &amp; 혜리 삿포로</title>
<meta name="claude:viewport-fit-sides" content="cover">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Gowun+Batang:wght@400;700&family=IBM+Plex+Sans+KR:wght@400;500;600&family=IBM+Plex+Mono:wght@500&display=swap">
<style>
/* Layout: snowy hero → transit summary → sticky date rail → one card per day, timed stops with transit lines and venue info */
:root{
  --bg:#eef2f5; --surface:#ffffff; --surface-2:#f4f7f9; --ink:#1c2733; --muted:#5d6b78; --line:#d6dee5;
  --ice:#3f6f8f; --lamp:#b8742a; --lamp-soft:#f6e8d6; --warn:#b4432f; --warn-soft:#f8e3de;
  --c-fix:#b8742a; --c-meal:#a2524a; --c-cafe:#8a6a3e; --c-illum:#4c6fb0; --c-shop:#3e8a73; --c-rest:#7a8794; --c-sight:#2f8a9a; --c-move:#a3afba;
  --hero-a:#dfe7ee; --hero-b:#c9d6e1;
  --f-display:"Gowun Batang","Nanum Myeongjo",serif;
  --f-body:"IBM Plex Sans KR","Apple SD Gothic Neo","Malgun Gothic",system-ui,sans-serif;
  --f-mono:"IBM Plex Mono",ui-monospace,Menlo,monospace;
}
@media (prefers-color-scheme:dark){:root:not([data-theme="light"]){
  --bg:#0f1720; --surface:#16212c; --surface-2:#1b2834; --ink:#e4ebf1; --muted:#93a3b2; --line:#26343f;
  --ice:#8fb6d3; --lamp:#e2a35a; --lamp-soft:#3a2b1a; --warn:#f08c78; --warn-soft:#3d221d;
  --c-fix:#e2a35a; --c-meal:#d98a80; --c-cafe:#c9a675; --c-illum:#8eaaf0; --c-shop:#6fc4a7; --c-rest:#9aa7b3; --c-sight:#6cc3d1; --c-move:#5f6e7b;
  --hero-a:#16222e; --hero-b:#0f1720; color-scheme:dark}}
:root[data-theme="dark"]{
  --bg:#0f1720; --surface:#16212c; --surface-2:#1b2834; --ink:#e4ebf1; --muted:#93a3b2; --line:#26343f;
  --ice:#8fb6d3; --lamp:#e2a35a; --lamp-soft:#3a2b1a; --warn:#f08c78; --warn-soft:#3d221d;
  --c-fix:#e2a35a; --c-meal:#d98a80; --c-cafe:#c9a675; --c-illum:#8eaaf0; --c-shop:#6fc4a7; --c-rest:#9aa7b3; --c-sight:#6cc3d1; --c-move:#5f6e7b;
  --hero-a:#16222e; --hero-b:#0f1720; color-scheme:dark}

*{box-sizing:border-box}
html{scroll-behavior:smooth}
body{background:var(--bg);color:var(--ink);font-family:var(--f-body);font-size:15px;line-height:1.6}
body::before{content:"";position:fixed;inset:0 0 auto;height:env(safe-area-inset-top,0px);z-index:10;background:var(--bg)}
.wrap{max-width:880px;margin:0 auto;padding-left:max(16px,env(safe-area-inset-left,0px));padding-right:max(16px,env(safe-area-inset-right,0px))}
a{color:var(--ice)}

/* hero */
.hero{position:relative;overflow:hidden;background:linear-gradient(180deg,var(--hero-a),var(--hero-b));border-bottom:1px solid var(--line)}
.hero canvas{position:absolute;inset:0;width:100%;height:100%;pointer-events:none}
.hero .wrap{position:relative;padding-block:56px 40px;display:grid;gap:18px}
.eyebrow{font-family:var(--f-mono);font-size:12px;letter-spacing:.14em;color:var(--ice);text-transform:uppercase}
h1{font-family:var(--f-display);font-weight:700;font-size:clamp(30px,6vw,52px);line-height:1.2;margin:0;text-wrap:balance;letter-spacing:-.01em}
h1 em{font-style:normal;color:var(--lamp)}
.lede{color:var(--muted);margin:0;max-width:60ch}
.facts{display:flex;flex-wrap:wrap;gap:10px 28px;margin-top:6px}
.fact{display:grid;gap:2px}
.fact b{font-family:var(--f-display);font-size:22px;font-weight:700}
.fact span{font-size:12px;color:var(--muted);letter-spacing:.04em}

/* transit summary */
.transit{padding-block:28px 4px;display:grid;gap:14px}
.transit h2{font-family:var(--f-display);font-size:20px;margin:0}
.alert{padding:12px 16px;border-radius:10px;background:var(--warn-soft);font-size:14px}
.alert b{color:var(--warn)}
.routes{display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));gap:10px}
.route{background:var(--surface);border:1px solid var(--line);border-radius:12px;padding:14px 16px;display:grid;gap:6px;min-width:0;align-content:start}
.route h3{margin:0;font-size:14.5px;font-weight:600}
.route ol{margin:0;padding-left:18px;font-size:13.5px;display:grid;gap:3px}
.route .sum{font-family:var(--f-mono);font-size:12.5px;color:var(--lamp)}
.route .fine{font-size:12.5px;color:var(--muted)}

/* brief */
.brief{list-style:none;margin:0;padding:0;background:var(--surface);overflow:hidden}
.brief li+li{border-top:1px solid var(--line)}
.brief a{display:grid;grid-template-columns:72px minmax(0,1fr);gap:2px 14px;padding:12px 16px;text-decoration:none;color:var(--ink)}
.brief a:hover{background:var(--surface-2)}
.brief .bd{grid-row:span 2;font-family:var(--f-mono);font-size:13px;color:var(--ice);padding-top:2px;font-variant-numeric:tabular-nums}
.brief b{font-weight:600;font-size:14.5px}
.brief .bl{font-size:13px;color:var(--muted);overflow-wrap:anywhere}
@media (max-width:520px){.brief a{grid-template-columns:56px minmax(0,1fr);padding:11px 12px}}

.mart{display:grid;gap:2px;padding:14px 16px;border-top:1px dashed var(--line);font-size:13px;color:var(--muted)}
.mart b{color:var(--ink);font-size:13.5px}

/* date rail */
.rail{position:sticky;top:env(safe-area-inset-top,0px);z-index:5;background:color-mix(in srgb,var(--bg) 92%,transparent);backdrop-filter:blur(8px);border-bottom:1px solid var(--line);margin-top:24px}
.rail .wrap{display:flex;gap:6px;overflow-x:auto;padding-block:10px;scrollbar-width:none}
.rail .wrap::-webkit-scrollbar{display:none}
.rail a{flex:none;display:grid;justify-items:center;min-width:58px;padding:6px 10px;border-radius:10px;text-decoration:none;color:var(--muted);border:1px solid transparent}
.rail a b{font-family:var(--f-mono);font-size:14px;color:var(--ink);font-variant-numeric:tabular-nums}
.rail a span{font-size:11px}
.rail a:hover{border-color:var(--line)}
.rail a.on{background:var(--surface);border-color:var(--line)}
.rail a.on b{color:var(--lamp)}
a:focus-visible,button:focus-visible{outline:2px solid var(--ice);outline-offset:2px}

/* legend */
.legend{display:flex;flex-wrap:wrap;gap:6px;padding-block:20px 4px}
.legend button{font:inherit;font-size:12.5px;display:inline-flex;align-items:center;gap:6px;padding:4px 10px;border-radius:999px;border:1px solid var(--line);background:var(--surface);color:var(--ink);cursor:pointer}
.legend button[aria-pressed="false"]{opacity:.45}
.dot{width:8px;height:8px;border-radius:50%;background:var(--c)}
.status{font-size:12.5px;color:var(--muted);padding-bottom:8px}

/* day */
main{display:grid;gap:28px;padding-block:16px 48px}
.days{display:grid;gap:28px}
.brief-card .brief{border:0;border-radius:0}
.day{background:var(--surface);border:1px solid var(--line);border-radius:14px;scroll-margin-top:calc(env(safe-area-inset-top,0px) + 76px);overflow:hidden}
.day-head{display:grid;grid-template-columns:auto 1fr;gap:4px 18px;align-items:end;padding:22px 22px 16px;border-bottom:1px solid var(--line)}
.dnum{grid-row:span 2;font-family:var(--f-display);font-weight:700;font-size:44px;line-height:1;color:var(--ice);font-variant-numeric:tabular-nums}
.dmeta{font-family:var(--f-mono);font-size:12px;color:var(--muted);letter-spacing:.06em}
.day h2{font-family:var(--f-display);font-size:22px;margin:0;font-weight:700;text-wrap:balance;min-width:0}
ol.stops{list-style:none;margin:0;padding:10px 22px 6px}
.stop{display:grid;grid-template-columns:52px 14px minmax(0,1fr);gap:0 12px}
.t{font-family:var(--f-mono);padding-top:9px;text-align:right;font-variant-numeric:tabular-nums;line-height:1.3}
.t b{display:block;font-size:13px;font-weight:500;color:var(--ink)}
.t small{display:block;font-size:11px;color:var(--muted)}
.pin{position:relative}
.pin::before{content:"";position:absolute;left:6px;top:0;bottom:0;width:2px;background:var(--line)}
.stop:first-child .pin::before{top:16px}
.stop:last-child .pin::before{bottom:calc(100% - 16px)}
.pin::after{content:"";position:absolute;left:2px;top:12px;width:10px;height:10px;border-radius:50%;background:var(--surface);border:2px solid var(--c)}
.stop.fix .pin::after{background:var(--c)}
.body{padding:8px 0 14px;min-width:0;display:grid;gap:4px}
.name{font-weight:500;overflow-wrap:anywhere}
.stop.fix .name{font-weight:600}
.sub{font-size:13.5px;color:var(--muted);overflow-wrap:anywhere}
.tag{display:inline-block;font-size:11px;font-weight:600;letter-spacing:.04em;padding:1px 7px;border-radius:5px;margin-right:6px;vertical-align:2px}
.tag.ok{background:var(--lamp-soft);color:var(--lamp)}
.tag.tbd{border:1px dashed var(--muted);color:var(--muted)}
.tag.opt{border:1px solid var(--line);color:var(--muted)}
.tag.warn{background:var(--warn-soft);color:var(--warn)}
.go{font-size:13px;border-left:2px solid var(--ice);padding:2px 0 2px 10px;display:grid;gap:1px}
.go span{display:block}
.go .yen{font-family:var(--f-mono);font-size:12px;color:var(--lamp);white-space:nowrap}
.info{font-size:13px;background:var(--surface-2);border-radius:8px;padding:8px 12px;display:grid;gap:2px}
.info .row{display:grid;grid-template-columns:52px minmax(0,1fr);gap:8px}
.info .row>span:first-child{color:var(--muted);font-size:12px;padding-top:1px}
.info .addr{overflow-wrap:anywhere}
.info .addr a{margin-left:6px;font-size:12px;white-space:nowrap}
.info .warnline{color:var(--warn)}
.note{margin:4px 22px 0;padding:10px 14px;border-radius:10px;background:var(--lamp-soft);color:var(--ink);font-size:13.5px}
.note.warn{background:var(--warn-soft)}
.stay{display:flex;gap:10px;align-items:baseline;flex-wrap:wrap;margin-top:14px;padding:14px 22px;border-top:1px dashed var(--line);font-size:13.5px}
.stay span{font-family:var(--f-mono);font-size:11px;letter-spacing:.12em;color:var(--muted);text-transform:uppercase}
.stay b{font-weight:600}

footer{border-top:1px solid var(--line);padding-block:28px 40px;color:var(--muted);font-size:13px}
footer .wrap{display:grid;gap:8px}
footer ul{margin:0;padding-left:18px;display:grid;gap:2px}
@media (max-width:520px){
  .stop{grid-template-columns:44px 14px minmax(0,1fr);gap:0 8px}
  .t b{font-size:12px}
  .day-head{padding:18px 16px 14px}
  ol.stops{padding-inline:12px}
  .note{margin-inline:14px}
  .stay{padding-inline:16px}
  .dnum{font-size:36px}
}
@media (prefers-reduced-motion:reduce){html{scroll-behavior:auto}}
</style>

<header class="hero">
  <canvas id="snow" aria-hidden="true"></canvas>
  <div class="wrap">
    <div class="eyebrow">Sapporo · Winter 2026</div>
    <h1>영무 &amp; 혜리의<br><em>삿포로</em> 신혼여행</h1>
    <p class="lede">2026.12.24 – 2027.01.01. 항공, 조잔케이 송영버스, 12/29 촬영은 확정이고 나머지 시각은 추천안이에요. 식당 예약과 연말 영업은 따로 확인이 필요해요.</p>
    <div class="facts">
      <div class="fact"><b>8박 9일</b><span>12.24 목 – 1.1 금</span></div>
      <div class="fact"><b>APA 8박 예약</b><span>오도리역 도보 7분 · 南2条西7丁目</span></div>
      <div class="fact"><b>조잔케이 1박</b><span>12/25 · 큰 짐은 APA에 두고</span></div>
    </div>
  </div>
</header>





<nav class="rail" aria-label="날짜"><div class="wrap" id="rail"></div></nav>

<div class="wrap">
  <div class="legend" id="legend" role="group" aria-label="카테고리 필터"></div>
  <div class="status" id="status">카테고리를 눌러 켜고 끌 수 있어요.</div>
  <main id="days-wrap"><section class="day brief-card" id="brief" aria-labelledby="plan-h">
  <div class="day-head"><div class="dnum">♢</div><div class="dmeta">OVERVIEW · 12/24 – 1/1</div><h2 id="plan-h">일정 한눈에</h2></div>
  <ol class="brief">
    <li><a href="#d1224"><span class="bd">12/24 목</span><b>입국 · 크리스마스</b><span class="bl">13:00 출국 → 15:45 신치토세 → 18:00 호텔 체크인 → 크리스마스 마켓·오도리 일루미</span></a></li>
    <li><a href="#d1225"><span class="bd">12/25 금</span><b>조잔케이 · 온천</b><span class="bl">삿포로역 점심·키노토야 → 13:00 송영버스 → 온천·석식 (그랜드 브리센 1박)</span></a></li>
    <li><a href="#d1226"><span class="bd">12/26 토</span><b>역 주변 쇼핑 · 빛 산책</b><span class="bl">10:45 송영버스 → 도큐백화점(빅카메라·유니클로·GU)·다이마루 → 아카푸라·에키마에 일루미 → 신나루 본즈 징기스칸</span></a></li>
    <li><a href="#d1227"><span class="bd">12/27 일</span><b>비에이 겨울 투어</b><span class="bl">종일 투어(흰수염폭포·청의호수 등) → 귀환 후 저녁 · 날씨로 취소되면 12/30과 교체</span></a></li>
    <li><a href="#d1228"><span class="bd">12/28 월</span><b>오타루 당일 여행</b><span class="bl">JR로 오타루 → 산카쿠 시장 카이센동 → 택시로 오타루 수족관 → 사카이마치·기타이치홀 → 운하 야경 → 삿포로 저녁</span></a></li>
    <li><a href="#d1229"><span class="bd">12/29 화</span><b>스스키노 촬영 · 기념 저녁</b><span class="bl">오전 준비 → 14:00 촬영 → Majisand → 미나미이치조 일루미 → 17:30 우시토사카나</span></a></li>
    <li><a href="#d1230"><span class="bd">12/30 수</span><b>휴식 · 오도리 쇼핑</b><span class="bl">TREASURE 수프카레 → 미쓰코시 백화점 → Standard Products → 키노토야 BAKE → 다이이치 마트 → 18:00 KANIZA</span></a></li>
    <li><a href="#d1231"><span class="bd">12/31 목</span><b>휴식 · 카운트다운</b><span class="bl">하루카 라멘 → 숙소 휴식·짐 정리 → 저녁 → TV타워 카운트다운 → 미요시 신사 첫 참배</span></a></li>
    <li><a href="#d0101"><span class="bd">1/1 금</span><b>공항 · 귀국</b><span class="bl">10:15 공항 도착 → 수속·쇼핑 → 14:15 출발 → 17:30 한국 도착</span></a></li>
  </ol>
  <div class="mart"><b>호텔 근처 마트</b><span>세이코마트 타누키코지 6초메점 · 南3条西6丁目3-2 · 핫셰프·베이커리 · 6:00–24:00 · 호텔에서 도보 약 3분</span><span>다이이치 스스키노점 · COCONO SUSUKINO B2F · 10:00–21:00 · 도보 약 10분</span></div>
</section><div id="days" class="days"></div></main>
</div>

<footer>
  <div class="wrap">
    <div>시각은 PDF 추천안 기준, 교통 요금은 성인 편도 기준이에요. 영업시간은 2026.10.21에 확인한 정보라 연말연시엔 달라질 수 있어요.</div>
    <div>참고한 곳</div>
    <ul>
      <li><a href="https://www.jtb.co.jp/kokunai-hotel/htl/1529051/access/" target="_blank" rel="noopener">APA 호텔 삿포로 오도리에키마에미나미 액세스 (JTB)</a></li>
      <li><a href="https://ekitan.com/transit/fare/sf-200/st-255" target="_blank" rel="noopener">에키탄: 삿포로–신치토세공항</a></li>
      <li><a href="https://www.cotaru.co/post/a1-sapporo-otaru-access" target="_blank" rel="noopener">삿포로–오타루 교통 정리</a> · <a href="https://www.watch.impress.co.jp/docs/news/2094533.html" target="_blank" rel="noopener">지하철 신용카드 상한운임 (Impress Watch)</a></li>
      <li><a href="https://otaru-aq.jp/guide/openningtime/" target="_blank" rel="noopener">오타루 수족관 영업시간</a> · <a href="https://otaru.gr.jp/tourist/toukieigyou2025-2026" target="_blank" rel="noopener">겨울 입장료</a> · <a href="https://www.cotaru.co/post/otaru-bus-taxi-access-guide" target="_blank" rel="noopener">오타루 택시 요금</a></li>
      <li><a href="https://www.jtb.co.jp/kokunai-hotel/htl/1533A07/access/" target="_blank" rel="noopener">그랜드 브리센 호텔 조잔케이 (JTB)</a></li>
      <li><a href="https://www.sapporo.travel/white-illumination/event/illumination/odori/" target="_blank" rel="noopener">화이트 일루미네이션 오도리 회장</a> · <a href="https://www.sapporo.travel/white-illumination/event/munich/" target="_blank" rel="noopener">뮌헨 크리스마스 마켓</a> · <a href="https://www.visit-hokkaido.jp/event/detail_11003.html" target="_blank" rel="noopener">회장별 기간</a></li>
      <li>쇼핑·마트: <a href="https://biccamera.rakuten.co.jp/c/shop/132.html" target="_blank" rel="noopener">빅카메라 삿포로점</a> · <a href="https://www.tokyu-dept.co.jp/sapporo/shop/detail.html?shopcode=7gu" target="_blank" rel="noopener">도큐백화점 GU·유니클로</a> · <a href="https://www.mitsukoshi.mistore.jp/sapporo/access.html" target="_blank" rel="noopener">삿포로 미쓰코시</a> · <a href="https://www.daimaru.co.jp/sapporo/news/10872.html" target="_blank" rel="noopener">다이마루 연말연시</a> · <a href="https://www.daiichi-d.co.jp/post_shop/ten309" target="_blank" rel="noopener">다이이치 스스키노점</a> · <a href="https://3cco.jp/seicomart-sapporo-central-store/" target="_blank" rel="noopener">세이코마트 시내 점포</a></li>
      <li>새해: <a href="https://x.com/SAPPORO_TVTOWER/status/2005549352861757613" target="_blank" rel="noopener">TV타워 카운트다운 (2025)</a> · <a href="https://www.tv-tower.co.jp/news.html?n=49" target="_blank" rel="noopener">TV타워 연말연시 영업</a> · <a href="https://hokkaidojinjacho.jp/%E4%B8%89%E5%90%89%E7%A5%9E%E7%A4%BE-3/" target="_blank" rel="noopener">미요시 신사 유래</a> · <a href="https://tabi-suki.net/miyoshijinja.html" target="_blank" rel="noopener">미요시 신사 오미쿠지</a> · <a href="https://www.sapporo.travel/find/culture/hokkaido_shrine/" target="_blank" rel="noopener">홋카이도 신궁 제신</a></li>
      <li>Standard Products·시장: <a href="https://www.daiso-sangyo.co.jp/shop/detail/001973" target="_blank" rel="noopener">모유크삿포로점</a> · <a href="https://otaru.gr.jp/shop/otarusankakuichiba" target="_blank" rel="noopener">오타루 산카쿠 시장</a></li>
      <li>식당·카페: <a href="https://majisand.shop/" target="_blank" rel="noopener">Majisand</a> · <a href="https://oagari.com/ushitosakana/" target="_blank" rel="noopener">우시토사카나</a> · <a href="https://www.gltjp.com/ja/directory/item/13957/" target="_blank" rel="noopener">TREASURE</a> · <a href="https://r.gnavi.co.jp/7u7jm7db0000/" target="_blank" rel="noopener">키노토야 다이마루점</a> · <a href="https://www.mapple.net/article/46110/" target="_blank" rel="noopener">키노토야 BAKE</a> · <a href="https://autoreserve.com/fr/restaurants/U6hFLe45tDstsDnErb93" target="_blank" rel="noopener">KANIZA</a> · <a href="https://www.waug.com/en/activities/148141" target="_blank" rel="noopener">신나루 본즈</a> · <a href="https://tabelog.com/en/hokkaido/A0101/A010103/1057373/" target="_blank" rel="noopener">라멘 하루카</a> · <a href="https://johnny88.jp/ramen-sora" target="_blank" rel="noopener">라멘 소라</a> · <a href="https://rurubu.jp/andmore/spot/80000582" target="_blank" rel="noopener">기타이치홀</a> · <a href="https://www.yukoyuko.net/onsen/spot/s0001082" target="_blank" rel="noopener">J.glacee</a></li>
    </ul>
  </div>
</footer>

<script>
const CATS={fix:["확정·투어","--c-fix"],meal:["식사","--c-meal"],cafe:["카페","--c-cafe"],illum:["일루미네이션","--c-illum"],shop:["쇼핑","--c-shop"],sight:["관광","--c-sight"],rest:["휴식","--c-rest"],move:["이동·준비","--c-move"]};
const APA="APA 호텔 삿포로 오도리에키마에미나미";
// 교통 [설명, 요금]
const TO_APA=[["호텔까지 도보 · 오도리에서 약 7분, 스스키노에서 약 10분","도보"]];
const FROM_APA=[["오도리·스스키노·타누키코지까지 도보 7~10분","도보"]];
const TO_STATION=[["호텔 → 삿포로역 도보 약 25분 · 또는 오도리역 → 삿포로역 지하철 난보쿠선 1정거장","도보 / 210엔"]];
const FROM_STATION=[["삿포로역 → 호텔 도보 약 25분 · 또는 지하철로 오도리역 (210엔) + 도보 7분","도보 / 210엔"]];
const SHUTTLE=[["그랜드 브리센 무료 송영버스 · 전날 17:00까지 예약제","무료"]];
// stop: {t, c, n, s, f, go:[[desc,yen]], info:{h, a, x, w}}
const DAYS=[
 {id:"d1224",m:"12",d:"24",w:"목",title:"입국 · 크리스마스",stay:APA,stops:[
  {t:"08:00–12:00",c:"move",n:"출국 준비·공항 이동"},
  {t:"13:00–15:45",c:"fix",n:"항공 13:00 출발",s:"15:45 신치토세 도착",f:"ok"},
  {t:"16:00–17:00",c:"move",n:"입국 수속·수하물 수령",s:"국제선은 30분~1시간 걸릴 수 있어요"},
  {t:"17:00–18:00",c:"move",n:"삿포로 이동·호텔 체크인",s:"18:00 체크인 목표 · 짐만 두고 바로 나가기",go:[["신치토세공항역 → 삿포로역 · JR 쾌속 에어포트 (약 37분)","1,230엔"],["삿포로역 → 오도리역 · 지하철 난보쿠선 1정거장 → 1번 출구 도보 7분","210엔"]],info:{a:"中央区南2条西7丁目"}},
  {t:"18:00–19:30",c:"shop",n:"크리스마스 마켓",s:"먹거리·소품 구경 · 저녁도 마켓 먹거리로",go:[["호텔 → 오도리공원 2초메 도보 약 10분","도보"]],
   info:{h:"11:00–21:00 (L.O. 20:45) · 12/25까지",a:"오도리공원 1·2초메 (中央区大通西2丁目)"}},
  {t:"19:30–20:30",c:"illum",n:"① 오도리공원 화이트 일루미네이션",info:{h:"16:30–22:00, 12/23~25는 24:00까지",a:"오도리공원 (中央区大通西)"}},
  {t:"20:30–21:30",c:"meal",n:"부족하면 간단한 야식",s:"호텔 근처 세이코마트 핫셰프"},
  {t:"",c:"move",n:"호텔 복귀",go:TO_APA},
  {t:"21:30",c:"rest",n:"휴식"}]},
 {id:"d1225",m:"12",d:"25",w:"금",title:"조잔케이 · 온천",stay:"그랜드 브리센 호텔 조잔케이",stops:[
  {t:"08:00–09:30",c:"move",n:"아침·1박 짐 챙기기",s:"큰 짐은 호텔 객실에 두고 출발"},
  {t:"09:30–10:30",c:"move",n:"호텔 → 삿포로역",go:TO_STATION},
  {t:"10:30–11:30",c:"meal",n:"역 주변 이른 점심"},
  {t:"11:30–12:15",c:"cafe",n:"키노토야 다이마루점",s:"디저트·휴식",info:{h:"10:00–20:00",a:"中央区北5条西4 大丸札幌店 B1"}},
  {t:"12:15–13:00",c:"move",n:"북쪽 출구 단체버스 정류장",s:"12:40 도착 목표"},
  {t:"13:00–14:30",c:"fix",n:"송영버스 삿포로역 → 조잔케이",s:"도착 시각은 교통에 따라 변동",f:"ok",go:SHUTTLE},
  {t:"14:30–17:00",c:"rest",n:"호텔 체크인·온천",info:{a:"南区定山渓温泉東4-328"}},
  {t:"",c:"cafe",n:"온천 거리·J.glacee",s:"카페는 도착·영업시간에 따라",f:"opt",info:{h:"9:00–18:00 · 부정기 휴무",a:"南区定山渓温泉西4丁目356"}},
  {t:"17:00–20:00",c:"meal",n:"호텔 석식·온천",s:"식사 시간은 숙소 안내 기준"},
  {t:"20:00",c:"rest",n:"숙소에서 휴식"}]},
 {id:"d1226",m:"12",d:"26",w:"토",title:"역 주변 쇼핑 · 빛 산책",stay:APA,stops:[
  {t:"08:00–10:30",c:"rest",n:"조식·온천·체크아웃",s:"10:45 버스 탑승 준비"},
  {t:"10:45–11:45",c:"fix",n:"송영버스 조잔케이 → 삿포로역",s:"10:45경 출발, 11:45경 도착",f:"ok",go:SHUTTLE},
  {t:"12:00–13:00",c:"meal",n:"역 주변 점심"},
  {t:"13:00–15:30",c:"shop",n:"쇼핑 DAY 1 · 삿포로 도큐백화점",s:"빅카메라 5·6층, 유니클로·GU 7층이 한 건물에 있어요",go:[["삿포로역 남쪽 출구에서 도보 약 3분","도보"]],info:{h:"10:00–20:00 (빅카메라 동일)",a:"中央区北4条西2-1 さっぽろ東急百貨店"}},
  {t:"15:30–16:30",c:"shop",n:"다이마루 백화점",s:"백화점 구경·실내 휴식",info:{h:"10:00–20:00",a:"中央区北5条西4 大丸札幌店"}},
  {t:"16:30–18:00",c:"illum",n:"② 아카푸라 → ③ 에키마에도리 → ④ 삿포로역 남쪽 광장",s:"아카렌가 청사 외관·사진",info:{h:"에키마에도리 2/11까지, 아카푸라·남쪽 광장 3/14까지 점등"}},
  {t:"18:00–19:00",c:"move",n:"스스키노 이동",go:[["삿포로역 → 스스키노역 · 지하철 난보쿠선 2정거장 (또는 도보 약 30분)","210엔"]]},
  {t:"19:00–20:30",c:"meal",n:"신나루 본즈 스스키노 본점",s:"생램 징기스칸 · 예약 추천",info:{h:"저녁 17:00–23:30 (예약 17:00–21:00) · 주말 점심 12:00–15:00",a:"中央区南4条西4丁目2 4ビル 1F"}},
  {t:"20:30",c:"rest",n:"호텔 복귀·휴식",go:TO_APA}]},
 {id:"d1227",m:"12",d:"27",w:"일",title:"비에이 겨울 투어",stay:APA,note:"날씨로 취소되면 12/30을 대체일로 고려. 집결지가 삿포로역 부근이면 호텔에서 도보 약 25분이에요.",stops:[
  {t:"08:00–20:00",c:"fix",n:"비에이 종일 투어",s:"집결·귀환 시각은 예약 상품 일정에 맞춰 조정",f:"opt",go:TO_STATION},
  {t:"",c:"fix",n:"흰수염폭포·청의호수 등",s:"실제 방문지는 상품 코스 기준"},
  {t:"20:00–21:30",c:"meal",n:"귀환 후 가까운 곳에서 저녁"},
  {t:"21:30",c:"rest",n:"호텔 복귀·휴식",go:TO_APA}]},
 {id:"d1228",m:"12",d:"28",w:"월",title:"오타루 당일 여행",stay:APA,stops:[
  {t:"08:00–09:00",c:"move",n:"아침·외출 준비"},
  {t:"09:00–11:00",c:"move",n:"호텔 → 삿포로역 → 오타루",s:"환승·이동 여유 포함",go:[...TO_STATION,["삿포로역 → 오타루역 · JR 쾌속 에어포트 (32~36분) 또는 보통 (50~60분)","800엔"]]},
  {t:"11:00–12:00",c:"meal",n:"카이센동 점심 · 오타루 산카쿠 시장",s:"역 바로 옆 해산물 시장 · 가게마다 영업시간이 달라요",go:[["오타루역에서 도보 1분","도보"]],info:{h:"시장 6:00–17:00 · 식당 7:00–17:00 · 연중무휴",a:"小樽市稲穂3丁目10-16"}},
  {t:"12:00–12:30",c:"move",n:"오타루 수족관으로 이동",go:[["오타루역 → 수족관 · 택시 약 20~30분 (겨울 할증 약 20%)","약 2,000~2,500엔"]]},
  {t:"12:30–14:30",c:"sight",n:"오타루 수족관",s:"겨울엔 해수공원·유원지는 휴장",info:{h:"겨울 10:00–16:00 (최종 입장 15:30) · 2026.12.12~2027.2.23",a:"小樽市祝津3丁目303",x:"입장료 성인 1,300엔 (2025~26 겨울 기준)"}},
  {t:"14:30–15:00",c:"move",n:"사카이마치로 이동",go:[["수족관 → 사카이마치 · 택시 약 20~30분","약 2,000~2,500엔"]],s:"수족관 앞에서 잘 안 잡히면 매표소에 택시 호출 부탁"},
  {t:"15:00–16:00",c:"shop",n:"사카이마치 거리",s:"유리공예·오르골당 주변"},
  {t:"16:00–16:45",c:"cafe",n:"기타이치홀",s:"램프 카페에서 휴식",f:"opt",info:{h:"9:00–17:30 (L.O. 17:00)",a:"小樽市堺町7-26 北一硝子三号館"}},
  {t:"16:45–17:30",c:"illum",n:"오타루 운하",s:"해 진 뒤 가스등 야경",go:[["사카이마치에서 도보 약 10분, 운하에서 오타루역까지 도보 10~12분","무료"]]},
  {t:"17:30–19:00",c:"move",n:"삿포로 복귀",go:[["오타루역 → 삿포로역 · JR","800엔"],...FROM_STATION]},
  {t:"19:00–20:00",c:"meal",n:"저녁 식사"},
  {t:"20:00",c:"rest",n:"호텔 복귀·휴식",go:TO_APA}]},
 {id:"d1229",m:"12",d:"29",w:"화",title:"스스키노 촬영 · 기념 저녁",stay:APA,stops:[
  {t:"08:00–12:00",c:"move",n:"헤어·촬영 준비",s:"오전 관광 일정은 비워두기"},
  {t:"12:00–13:00",c:"meal",n:"스스키노 주변 가벼운 점심",go:FROM_APA},
  {t:"13:00–14:00",c:"move",n:"촬영 장소 이동",s:"13:40 도착 목표"},
  {t:"14:00–15:00",c:"fix",n:"Susukino 촬영 1시간",s:"14:00 – 15:00",f:"ok"},
  {t:"15:00–16:30",c:"cafe",f:"must",n:"Majisand (마지산도)",s:"과일 샌드·디저트·휴식",info:{h:"11:00–20:00 · 연중무휴 (품절 시 조기 마감)",a:"中央区南2条西1丁目5-9 第13広和ビル 1F"}},
  {t:"16:30–17:15",c:"illum",n:"⑤ 미나미이치조도리 화이트 일루미네이션",info:{h:"3/14까지 점등"}},
  {t:"17:30–19:00",c:"meal",n:"우시토사카나 타누키코지",s:"와규·해산물 기념 저녁 · 17:30 예약 추천",info:{h:"11:30–14:30 / 17:00–22:00 (주말 23:00까지)",a:"中央区南3条西5丁目30 三条美松ビル B1",x:"예약 전화 011-522-5980"}},
  {t:"19:00",c:"rest",n:"호텔 복귀·휴식",go:TO_APA}]},
 {id:"d1230",m:"12",d:"30",w:"수",title:"휴식 · 오도리 쇼핑",stay:APA,note:"비에이 투어가 취소되면 이날 일정 조정",stops:[
  {t:"08:00–10:00",c:"rest",n:"늦잠·휴식"},
  {t:"10:00–11:30",c:"move",n:"시내 이동",go:FROM_APA},
  {t:"11:30–12:30",c:"meal",n:"수프카레 TREASURE",s:"대기시간에 따라 뒤 일정 조정",info:{h:"11:30–15:30 / 17:00–21:00 · 부정기 휴무",a:"中央区南2条西1-8-2 アスカビル 1F"}},
  {t:"12:30–14:30",c:"shop",n:"쇼핑 DAY 2 · 미쓰코시 백화점",s:"백화점 + 유니클로·GU 미쓰코시점",go:[["TREASURE에서 도보 약 5분","도보"]],info:{h:"10:00–19:00 (지하 식품관 19:30)",a:"中央区南1条西3丁目8 札幌三越"}},
  {t:"14:30–15:30",c:"shop",n:"Standard Products 모유크삿포로점",s:"다이소의 생활용품 브랜드",go:[["미쓰코시에서 도보 약 3분","도보"]],info:{h:"10:00–20:00",a:"中央区南2条西3丁目20 moyuk SAPPORO 2F"}},
  {t:"15:30–16:15",c:"cafe",n:"키노토야 BAKE 폴타운점",s:"디저트·휴식",info:{h:"10:00–20:00 · 무휴",a:"中央区南2条西3丁目 지하상가 폴타운"}},
  {t:"16:15–17:30",c:"shop",n:"마트 장보기 · 다이이치 스스키노점",s:"홋카이도 지역 슈퍼 · KANIZA까지 도보 약 3분",info:{h:"10:00–21:00",a:"中央区南4条西4丁目1-1 COCONO SUSUKINO B2F"}},
  {t:"18:00–20:00",c:"meal",n:"KANIZA 삿포로 (かに食べ放題 蟹座)",s:"게 샤부샤부 무한리필 · 18:00 예약 추천",f:"must",info:{h:"17:00–22:30 (L.O. 21:00)",a:"中央区南4条西2丁目10-6 南4西2ビル 9F"}},
  {t:"20:00",c:"rest",n:"호텔 복귀·쇼핑 짐 정리",go:TO_APA}]},
 {id:"d1231",m:"12",d:"31",w:"목",title:"휴식 · 카운트다운",stay:APA,stops:[
  {t:"08:00–11:00",c:"rest",n:"늦잠·아침·휴식"},
  {t:"11:00–14:00",c:"meal",n:"시내 이동·라멘 점심",s:"하루카 / 소라 중 연말 영업이 확인되는 곳",go:FROM_APA,
   info:{h:"하루카(悠): 11:00–15:00 / 17:00–23:00 · 부정기 휴무",a:"中央区南5条西3-6 N・グランデビル 1F (원조 라멘 요코초)",w:"소라(空) 본점은 2024년 1월 화재로 영업하지 않아요. 남은 곳은 신치토세공항점뿐이에요."}},
  {t:"14:00–19:00",c:"rest",n:"숙소 휴식·귀국 짐 정리",s:"관광·쇼핑은 추가하지 않기"},
  {t:"19:00–21:00",c:"meal",n:"시내 이동·저녁 식사"},
  {t:"21:00–23:00",c:"rest",n:"따뜻한 실내에서 휴식",s:"23:30쯤 TV타워 쪽으로 이동"},
  {t:"23:30–00:05",c:"illum",n:"삿포로 TV타워 카운트다운",s:"오도리공원 서쪽(니시 2~3초메)에서 TV타워 전광시계를 보며 새해맞이",f:"tbd",go:[["호텔 → TV타워 도보 약 15분","도보"]],info:{a:"中央区大通西1丁目",x:"2025년 12/31에 처음으로 전광시계 카운트다운을 했어요. 전망대는 밤에 닫으니 밖에서 보는 걸로",w:"2026년에도 하는지는 아직 발표 전이에요. 12월에 TV타워 공식 계정 확인 필요"}},
  {t:"00:15–00:45",c:"sight",n:"미요시 신사 첫 참배·오미쿠지",s:"호텔에서 걸어서 3분 거리 동네 신사 · 오미쿠지 100엔",go:[["TV타워 → 미요시 신사 도보 약 15분","도보"]],info:{h:"경내는 24시간 참배 가능 · 사무소 9:00–17:00",a:"中央区南1条西8丁目17",x:"1878년 아키타 출신 이주민이 세운 신사 · 오나무치·스쿠나히코나·미요시 신 등을 모셔요"}},
  {t:"",c:"rest",n:"호텔 복귀",go:[["미요시 신사 → 호텔 도보 약 3분","도보"]]}]},
 {id:"d0101",m:"1",d:"1",w:"금",title:"공항 · 귀국",stay:"한국 도착",stayLabel:"Home",stops:[
  {t:"08:00–10:15",c:"move",n:"체크아웃·공항 이동",s:"교통편에 맞춰 출발 시각 확정",go:[["호텔 → 오도리역 도보 7분 → 지하철 난보쿠선 삿포로역","210엔"],["삿포로역 → 신치토세공항 · JR 쾌속 에어포트 (약 37분)","1,230엔"]]},
  {t:"10:15–12:00",c:"move",n:"공항 도착 10:15~10:30 목표",s:"면세 반출 확인·항공 수속 · 수하물 위탁 전 물품 검사 확인"},
  {t:"12:00–14:00",c:"meal",n:"수속 진행에 맞춰 식사·쇼핑",s:"이후 보안검색·출국심사·탑승 준비"},
  {t:"14:15–17:30",c:"fix",n:"항공 14:15 출발",s:"17:30 한국 도착",f:"ok"},
  {t:"17:30",c:"rest",n:"귀가·휴식"}]}
];
const esc=s=>String(s).replace(/[&<>"]/g,c=>({"&":"&amp;","<":"&lt;",">":"&gt;",'"':"&quot;"}[c]));
const FLAG={must:["꼭","ok"],ok:["확정","ok"],tbd:["미정","tbd"],opt:["선택","opt"]};
const map=a=>`https://www.google.com/maps/search/?api=1&query=${encodeURIComponent(a.replace(/\(.*?\)/g,"").trim())}`;
const timeCell=t=>{if(!t)return"";const[a,b]=t.split("–");return `<b>${a}</b>${b?`<small>${b}</small>`:""}`};
const addrText=a=>/^(中央区|南区)/.test(a)?"北海道札幌市"+a:/^小樽市/.test(a)?"北海道"+a:a;
const goHtml=g=>g?`<div class="go">${g.map(([d,y])=>`<span>${esc(d)} <span class="yen">${esc(y)}</span></span>`).join("")}</div>`:"";
const infoHtml=i=>{if(!i)return"";let r="";
  if(i.h)r+=`<div class="row"><span>영업</span><span>${esc(i.h)}</span></div>`;
  if(i.a)r+=`<div class="row"><span>주소</span><span class="addr">${esc(i.a)}<a href="${map(addrText(i.a))}" target="_blank" rel="noopener">지도</a></span></div>`;
  if(i.x)r+=`<div class="row"><span>참고</span><span>${esc(i.x)}</span></div>`;
  if(i.w)r+=`<div class="row"><span class="warnline">주의</span><span class="warnline">${esc(i.w)}</span></div>`;
  return `<div class="info">${r}</div>`};

document.getElementById("rail").innerHTML=`<a href="#brief" data-id="brief"><b>한눈에</b><span>전체</span></a>`+DAYS.map(d=>`<a href="#${d.id}" data-id="${d.id}"><b>${d.m}/${d.d}</b><span>${d.w}</span></a>`).join("");
document.getElementById("days").innerHTML=DAYS.map((d,i)=>`
<section class="day" id="${d.id}" aria-labelledby="${d.id}-t">
  <div class="day-head">
    <div class="dnum">${String(i+1).padStart(2,"0")}</div>
    <div class="dmeta">DAY ${i+1} · ${d.m}/${d.d} (${d.w})</div>
    <h2 id="${d.id}-t">${esc(d.title)}</h2>
  </div>
  <ol class="stops">${d.stops.map(p=>`
    <li class="stop ${p.c}" data-cat="${p.c}" style="--c:var(${CATS[p.c][1]})">
      <div class="t">${timeCell(p.t)}</div><div class="pin" aria-hidden="true"></div>
      <div class="body"><div class="name">${p.f?`<span class="tag ${FLAG[p.f][1]}">${FLAG[p.f][0]}</span>`:""}${p.info&&p.info.w?`<span class="tag warn">확인 필요</span>`:""}${esc(p.n)}</div>${p.s?`<div class="sub">${esc(p.s)}</div>`:""}${goHtml(p.go)}${infoHtml(p.info)}</div>
    </li>`).join("")}
  </ol>
  ${d.note?`<div class="note${d.noteWarn?" warn":""}">${esc(d.note)}</div>`:""}
  <div class="stay"><span>${d.stayLabel||"Stay"}</span><b>${esc(d.stay)}</b></div>
</section>`).join("");

// legend filter
const on=new Set(Object.keys(CATS));
const lg=document.getElementById("legend");
lg.innerHTML=Object.entries(CATS).map(([k,[l,v]])=>`<button type="button" id="f-${k}" data-k="${k}" aria-pressed="true" style="--c:var(${v})"><i class="dot"></i>${l}</button>`).join("");
lg.addEventListener("click",e=>{
  const b=e.target.closest("button");if(!b)return;
  const k=b.dataset.k;
  on.has(k)?on.delete(k):on.add(k);
  if(!on.size)Object.keys(CATS).forEach(x=>on.add(x));
  lg.querySelectorAll("button").forEach(x=>x.setAttribute("aria-pressed",on.has(x.dataset.k)));
  document.querySelectorAll(".stop").forEach(s=>s.hidden=!on.has(s.dataset.cat));
  const n=document.querySelectorAll(".stop:not([hidden])").length;
  document.getElementById("status").textContent=on.size===Object.keys(CATS).length?"카테고리를 눌러 켜고 끌 수 있어요.":`${n}개 일정 표시 중`;
});

// active day in rail
const links=[...document.querySelectorAll(".rail a")];
const railBox=document.getElementById("rail");
const setOn=id=>links.forEach(a=>{const y=a.dataset.id===id;a.classList.toggle("on",y);if(y){const l=a.offsetLeft-railBox.clientWidth/2+a.clientWidth/2;railBox.scrollTo({left:l,behavior:"smooth"})}});
const io=new IntersectionObserver(es=>{es.forEach(e=>{if(e.isIntersecting)setOn(e.target.id)})},{rootMargin:"-30% 0px -60% 0px"});
document.querySelectorAll(".day").forEach(s=>io.observe(s));
setOn("brief");
if(location.hash){const el=document.getElementById(location.hash.slice(1));if(el)setTimeout(()=>el.scrollIntoView(),50)}

// snowfall
(function(){
  const cv=document.getElementById("snow"),ctx=cv.getContext("2d");
  const still=matchMedia("(prefers-reduced-motion: reduce)").matches;
  let W,H,flakes;
  function size(){const r=cv.getBoundingClientRect(),p=devicePixelRatio||1;W=r.width;H=r.height;cv.width=W*p;cv.height=H*p;ctx.setTransform(p,0,0,p,0,0);
    flakes=Array.from({length:Math.round(W/9)},()=>({x:Math.random()*W,y:Math.random()*H,r:Math.random()*2+.6,s:Math.random()*.4+.2,d:Math.random()*Math.PI*2}))}
  function draw(){
    const m=getComputedStyle(document.body).backgroundColor.match(/\d+/g)||[255,255,255];
    const dark=(+m[0]+ +m[1]+ +m[2])<300;
    ctx.clearRect(0,0,W,H);ctx.fillStyle=dark?"rgba(220,232,245,.55)":"rgba(255,255,255,.9)";
    for(const f of flakes){ctx.beginPath();ctx.arc(f.x,f.y,f.r,0,7);ctx.fill();
      if(!still){f.y+=f.s;f.d+=.01;f.x+=Math.sin(f.d)*.3;if(f.y>H+4){f.y=-4;f.x=Math.random()*W}}}
    if(!still)requestAnimationFrame(draw);
  }
  size();draw();addEventListener("resize",()=>{size();if(still)draw()});
})();
</script>
