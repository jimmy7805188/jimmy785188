<!DOCTYPE html>
<html lang="zh-Hant">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
<meta name="theme-color" content="#F5EFEB">
<title>保單健檢自查表 | JIMMY</title>
<meta property="og:title" content="保單健檢自查表">
<meta property="og:description" content="10 個問題 抓出你的保單破洞">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,500;0,700;1,300;1,500&family=DM+Sans:wght@400;500;600&family=Noto+Sans+TC:wght@400;500&family=Noto+Serif+TC:wght@500;700;900&display=swap" rel="stylesheet">
<style>
  :root{
    --paper:#F5EFEB;
    --paper-deep:#EFE8E2;
    --navy:#2F4156;
    --steel:#567C8D;
    --mist:#C8D9E6;
    --ink:#1A1814;
    --sub:#7A7468;
    --line:rgba(26,24,20,0.10);
    --gap-h:24px;
  }
  *{margin:0;padding:0;box-sizing:border-box;-webkit-tap-highlight-color:transparent;}
  html,body{
    background:var(--paper);
    color:var(--ink);
    font-family:'DM Sans','Noto Sans TC',sans-serif;
    -webkit-font-smoothing:antialiased;
    min-height:100vh;
    overflow-x:hidden;
  }
  body{
    background-image:
      repeating-linear-gradient(93deg, transparent, transparent 2px, rgba(140,128,100,0.025) 2px, rgba(140,128,100,0.025) 3px),
      repeating-linear-gradient(2deg, transparent, transparent 3px, rgba(140,128,100,0.018) 3px, rgba(140,128,100,0.018) 4px);
  }

  /* ===== sticky progress bar ===== */
  .progress-bar{
    position:fixed;top:0;left:0;right:0;
    height:3px;background:rgba(47,65,86,0.10);
    z-index:50;
  }
  .progress-fill{
    height:100%;width:0%;
    background:var(--navy);
    transition:width .35s cubic-bezier(.22,.61,.36,1);
  }
  .progress-label{
    position:fixed;top:14px;right:20px;
    font-size:10px;font-weight:600;letter-spacing:2px;
    color:rgba(26,24,20,0.50);
    background:rgba(245,239,235,0.85);
    backdrop-filter:blur(8px);
    padding:5px 10px;border-radius:20px;
    z-index:50;
    font-family:'DM Sans',sans-serif;
    transition:opacity .3s;
  }
  .progress-label.hide{opacity:0;pointer-events:none;}

  /* ===== container ===== */
  .wrap{
    max-width:560px;margin:0 auto;
    padding:48px 26px 80px;
    position:relative;
  }

  /* watermarks */
  .wm{
    position:absolute;
    font-family:'Cormorant Garamond',serif;font-weight:500;
    color:rgba(47,65,86,0.045);
    line-height:.82;letter-spacing:-2px;
    pointer-events:none;user-select:none;white-space:nowrap;
    z-index:0;
  }

  /* ===== TOP brand row ===== */
  .top-row{
    display:flex;justify-content:space-between;align-items:center;
    font-size:9px;font-weight:600;letter-spacing:2.5px;
    color:rgba(26,24,20,0.40);
    margin-bottom:32px;
    position:relative;z-index:2;
  }

  /* ===== Hero ===== */
  .hero{position:relative;z-index:2;margin-bottom:32px;}
  .eng{
    font-family:'Cormorant Garamond',serif;
    font-style:italic;font-weight:300;font-size:14px;
    color:var(--steel);letter-spacing:.5px;margin-bottom:14px;
  }
  h1{
    font-family:'Noto Serif TC',serif;font-weight:900;
    font-size:42px;line-height:1.1;letter-spacing:-1px;
    color:var(--ink);
  }
  .sub{
    font-family:'Noto Serif TC',serif;font-weight:500;
    font-size:16px;color:var(--steel);margin-top:14px;letter-spacing:.3px;
  }
  .lead{
    margin-top:22px;
    font-size:14px;line-height:1.8;color:var(--sub);
  }
  .lead b{color:var(--navy);font-weight:600;}

  /* ===== how-to card ===== */
  .how-to{
    margin-top:24px;
    background:rgba(86,124,141,0.06);
    border-left:2px solid var(--navy);
    border-radius:8px;
    padding:18px 22px;
    position:relative;z-index:2;
  }
  .how-to .label{
    font-size:9px;letter-spacing:3px;text-transform:uppercase;
    color:var(--steel);font-weight:600;margin-bottom:10px;
    font-family:'DM Sans',sans-serif;
  }
  .how-to ol{list-style:none;counter-reset:step;}
  .how-to li{
    counter-increment:step;
    font-size:13px;line-height:1.7;color:var(--ink);
    padding-left:24px;position:relative;
    margin-bottom:4px;
  }
  .how-to li:last-child{margin-bottom:0;}
  .how-to li:before{
    content:counter(step,decimal-leading-zero);
    position:absolute;left:0;top:0;
    font-family:'Cormorant Garamond',serif;font-weight:500;
    color:var(--navy);font-size:14px;letter-spacing:.5px;
  }

  /* ===== begin button ===== */
  .begin-btn{
    margin-top:32px;
    width:100%;
    background:var(--navy);
    color:#fff;
    border:none;
    font-family:'Noto Serif TC',serif;font-weight:700;
    font-size:16px;letter-spacing:1.5px;
    padding:18px 24px;
    border-radius:60px;
    cursor:pointer;
    transition:transform .2s, box-shadow .2s;
    box-shadow:0 6px 20px rgba(47,65,86,0.25);
    position:relative;z-index:2;
  }
  .begin-btn:hover{transform:translateY(-2px);box-shadow:0 10px 28px rgba(47,65,86,0.35);}
  .begin-btn:active{transform:translateY(0);}
  .begin-btn .ar{display:inline-block;margin-left:8px;transition:transform .2s;}
  .begin-btn:hover .ar{transform:translateX(4px);}

  /* ===== STAGE label ===== */
  .stage-label{
    font-size:10px;letter-spacing:3px;text-transform:uppercase;
    color:var(--steel);font-weight:600;margin-top:12px;
    font-family:'DM Sans',sans-serif;
    position:relative;z-index:2;
  }
  .stage-divider{
    margin:48px 0 28px;
    position:relative;z-index:2;
    display:flex;align-items:center;gap:14px;
  }
  .stage-divider .num{
    font-family:'Cormorant Garamond',serif;font-weight:500;font-style:italic;
    font-size:34px;color:var(--navy);line-height:1;
  }
  .stage-divider .text{
    font-family:'Noto Serif TC',serif;font-weight:700;font-size:17px;
    line-height:1.4;color:var(--ink);
  }
  .stage-divider .text small{
    display:block;font-size:10px;font-weight:600;letter-spacing:2px;
    color:var(--steel);text-transform:uppercase;margin-top:2px;
    font-family:'DM Sans',sans-serif;
  }

  /* ===== Question card ===== */
  .q-card{
    background:rgba(255,255,255,0.55);
    border:1px solid var(--line);
    border-radius:14px;
    padding:24px 22px;
    margin-bottom:18px;
    position:relative;z-index:2;
    transition:border-color .25s, box-shadow .25s, transform .25s;
  }
  .q-card.answered{
    background:rgba(255,255,255,0.85);
    border-color:rgba(47,65,86,0.20);
    box-shadow:0 4px 18px rgba(47,65,86,0.06);
  }
  .q-num{
    font-family:'Cormorant Garamond',serif;font-weight:500;
    font-size:20px;color:var(--navy);line-height:1;
    margin-bottom:10px;letter-spacing:.5px;
  }
  .q-text{
    font-family:'Noto Serif TC',serif;font-weight:700;
    font-size:16px;line-height:1.55;color:var(--ink);
    margin-bottom:18px;
  }
  .choices{display:flex;flex-direction:column;gap:9px;margin-bottom:14px;}
  .choice{
    display:flex;align-items:center;gap:12px;
    padding:13px 16px;
    border:1.3px solid var(--line);
    border-radius:10px;
    background:#fff;
    cursor:pointer;
    transition:border-color .2s, background .2s, transform .15s;
    user-select:none;
  }
  .choice:hover{border-color:rgba(47,65,86,0.30);background:rgba(86,124,141,0.04);}
  .choice:active{transform:scale(0.98);}
  .choice .box{
    width:18px;height:18px;
    border:1.5px solid var(--navy);
    border-radius:4px;
    flex-shrink:0;
    display:flex;align-items:center;justify-content:center;
    transition:background .2s;
    position:relative;
  }
  .choice .box svg{
    width:11px;height:11px;
    opacity:0;transform:scale(.6);
    transition:opacity .2s, transform .2s;
  }
  .choice.selected{
    border-color:var(--navy);
    background:rgba(47,65,86,0.07);
  }
  .choice.selected .box{background:var(--navy);}
  .choice.selected .box svg{opacity:1;transform:scale(1);}
  .choice .label{
    font-size:14px;font-weight:500;color:var(--ink);
    font-family:'DM Sans','Noto Sans TC',sans-serif;
  }
  .choice .pts{
    margin-left:auto;
    font-family:'Cormorant Garamond',serif;
    font-size:13px;color:rgba(47,65,86,0.0);
    font-style:italic;
    transition:color .25s;
  }
  .choice.selected .pts{color:var(--steel);}
  .hint{
    padding-left:14px;border-left:2px solid var(--mist);
    font-size:12px;color:var(--sub);line-height:1.55;
    font-style:italic;
    font-family:'DM Sans','Noto Sans TC',sans-serif;
  }

  /* ===== Submit area ===== */
  .submit-area{
    margin-top:30px;
    position:relative;z-index:2;
  }
  .submit-status{
    text-align:center;
    font-size:12px;letter-spacing:1.5px;color:var(--sub);
    margin-bottom:14px;font-weight:500;
    font-family:'DM Sans','Noto Sans TC',sans-serif;
  }
  .submit-status b{color:var(--navy);font-family:'Cormorant Garamond',serif;font-weight:700;font-size:16px;font-style:italic;margin:0 3px;}
  .submit-btn{
    width:100%;background:var(--navy);color:#fff;border:none;
    font-family:'Noto Serif TC',serif;font-weight:700;font-size:16px;
    letter-spacing:1.5px;padding:18px 24px;border-radius:60px;
    cursor:pointer;transition:transform .2s, box-shadow .2s, opacity .25s;
    box-shadow:0 6px 20px rgba(47,65,86,0.25);
  }
  .submit-btn:hover{transform:translateY(-2px);box-shadow:0 10px 28px rgba(47,65,86,0.35);}
  .submit-btn:disabled{opacity:.35;cursor:not-allowed;transform:none;box-shadow:none;}

  /* ===== RESULT screen ===== */
  .result{
    position:relative;z-index:2;
    animation:fadeUp .55s cubic-bezier(.22,.61,.36,1);
  }
  @keyframes fadeUp{from{opacity:0;transform:translateY(20px);}to{opacity:1;transform:translateY(0);}}

  .score-hero{
    text-align:center;margin-bottom:32px;
  }
  .score-eng{
    font-family:'Cormorant Garamond',serif;font-style:italic;font-weight:300;
    font-size:14px;color:var(--steel);letter-spacing:.5px;margin-bottom:12px;
  }
  .score-circle{
    width:200px;height:200px;
    margin:0 auto 22px;
    position:relative;
    display:flex;align-items:center;justify-content:center;
  }
  .score-circle svg{position:absolute;inset:0;transform:rotate(-90deg);}
  .score-circle .track{fill:none;stroke:rgba(47,65,86,0.10);stroke-width:6;}
  .score-circle .arc{
    fill:none;stroke:var(--navy);stroke-width:6;stroke-linecap:round;
    stroke-dasharray:565;stroke-dashoffset:565;
    transition:stroke-dashoffset 1.4s cubic-bezier(.22,.61,.36,1) .15s;
  }
  .score-circle.warn .arc{stroke:#B89968;}
  .score-circle.alert .arc{stroke:#C1543D;}
  .score-num{
    font-family:'Cormorant Garamond',serif;font-weight:700;
    font-size:80px;color:var(--navy);line-height:1;
  }
  .score-num small{font-size:24px;color:var(--sub);font-weight:500;}
  .score-circle.alert .score-num{color:#C1543D;}
  .score-circle.warn .score-num{color:#B89968;}

  .level-title{
    font-family:'Noto Serif TC',serif;font-weight:900;
    font-size:30px;line-height:1.2;color:var(--ink);
    margin-bottom:10px;
  }
  .level-desc{
    font-size:14px;line-height:1.75;color:var(--sub);
    max-width:420px;margin:0 auto;
  }
  .level-desc b{color:var(--navy);font-weight:600;}

  /* breakdown of weak items */
  .weak-list{
    margin-top:32px;
    background:#fff;
    border:1px solid var(--line);
    border-radius:12px;
    padding:20px 22px;
  }
  .weak-list .head{
    font-size:9px;letter-spacing:3px;text-transform:uppercase;
    color:var(--steel);font-weight:600;margin-bottom:14px;
    font-family:'DM Sans',sans-serif;
  }
  .weak-list .empty{
    font-family:'Noto Serif TC',serif;font-size:14px;color:var(--steel);
    text-align:center;padding:6px 0;
  }
  .weak-item{
    display:flex;gap:12px;
    padding:10px 0;
    border-bottom:1px dashed var(--line);
  }
  .weak-item:last-child{border-bottom:none;}
  .weak-item .wn{
    font-family:'Cormorant Garamond',serif;font-weight:500;font-style:italic;
    color:var(--navy);font-size:13px;flex-shrink:0;width:20px;
  }
  .weak-item .wt{
    font-family:'Noto Sans TC',sans-serif;font-weight:500;
    font-size:13px;line-height:1.5;color:var(--ink);
  }

  /* CTA */
  .cta-block{
    margin-top:30px;
    background:var(--navy);
    border-radius:14px;
    padding:30px 26px;
    color:#fff;
    position:relative;overflow:hidden;
  }
  .cta-block:before{
    content:"JIMMY";
    position:absolute;top:-18px;right:-12px;
    font-family:'Cormorant Garamond',serif;font-weight:700;
    font-size:110px;color:rgba(255,255,255,0.06);
    letter-spacing:-2px;line-height:1;
  }
  .cta-block .label{
    font-size:9px;letter-spacing:3px;text-transform:uppercase;
    color:rgba(255,255,255,0.55);font-weight:600;margin-bottom:12px;
    font-family:'DM Sans',sans-serif;position:relative;z-index:2;
  }
  .cta-block .htitle{
    font-family:'Noto Serif TC',serif;font-weight:900;
    font-size:22px;line-height:1.3;color:#fff;
    margin-bottom:14px;position:relative;z-index:2;
  }
  .cta-block .htext{
    font-size:13px;line-height:1.7;color:rgba(255,255,255,0.78);
    margin-bottom:22px;position:relative;z-index:2;
  }
  .cta-actions{display:flex;flex-direction:column;gap:10px;position:relative;z-index:2;}
  .cta-btn{
    display:flex;align-items:center;justify-content:center;gap:8px;
    background:#fff;color:var(--navy);
    font-family:'Noto Serif TC',serif;font-weight:700;
    font-size:14px;letter-spacing:.8px;
    padding:15px 20px;border-radius:60px;
    text-decoration:none;
    transition:transform .2s, box-shadow .2s;
  }
  .cta-btn:hover{transform:translateY(-2px);box-shadow:0 6px 18px rgba(0,0,0,0.18);}
  .cta-btn.secondary{
    background:transparent;color:#fff;
    border:1.5px solid rgba(255,255,255,0.40);
  }
  .cta-btn svg{width:16px;height:16px;flex-shrink:0;}

  .signoff{
    text-align:center;margin-top:36px;
    font-family:'Cormorant Garamond',serif;font-style:italic;font-weight:300;
    font-size:15px;color:var(--steel);line-height:1.6;
  }
  .restart{
    text-align:center;margin-top:18px;
  }
  .restart button{
    background:none;border:none;
    font-size:12px;color:var(--sub);letter-spacing:1px;
    cursor:pointer;font-family:'DM Sans','Noto Sans TC',sans-serif;
    text-decoration:underline;text-underline-offset:3px;
    text-decoration-color:rgba(122,116,104,0.30);
  }
  .restart button:hover{color:var(--navy);text-decoration-color:var(--navy);}

  /* footer */
  .footer{
    margin-top:60px;padding-top:24px;
    border-top:1px solid var(--line);
    display:flex;justify-content:space-between;
    font-size:9px;letter-spacing:2px;font-weight:600;
    color:rgba(26,24,20,0.35);
    position:relative;z-index:2;
  }

  /* tiny screens */
  @media (max-width:380px){
    .wrap{padding:36px 18px 70px;}
    h1{font-size:34px;}
    .score-circle{width:170px;height:170px;}
    .score-num{font-size:66px;}
    .level-title{font-size:24px;}
  }

  /* ===== contact-info step ===== */
  .contact-step{
    position:relative;z-index:2;
    animation:fadeUp .45s cubic-bezier(.22,.61,.36,1);
  }
  .contact-step .eng{margin-top:6px;}
  .contact-step h2{
    font-family:'Noto Serif TC',serif;font-weight:900;
    font-size:30px;line-height:1.2;color:var(--ink);
    margin-bottom:14px;
  }
  .contact-step .desc{
    font-size:13.5px;line-height:1.7;color:var(--sub);
    margin-bottom:28px;
  }
  .contact-step .desc b{color:var(--navy);font-weight:600;}
  .field-group{margin-bottom:18px;}
  .field-group label{
    display:block;
    font-size:11px;letter-spacing:2px;text-transform:uppercase;
    color:var(--steel);font-weight:600;
    margin-bottom:8px;
    font-family:'DM Sans',sans-serif;
  }
  .field-group label .req{color:#C1543D;margin-left:2px;}
  .field-group label .opt{
    color:var(--sub);font-weight:500;font-size:10px;
    letter-spacing:1px;text-transform:none;margin-left:6px;
  }
  .field-group input{
    width:100%;
    border:none;
    border-bottom:1.5px solid rgba(26,24,20,0.20);
    background:transparent;
    padding:8px 0 10px;
    font-size:16px;
    font-family:'DM Sans','Noto Sans TC',sans-serif;
    color:var(--ink);
    outline:none;
    transition:border-color .2s;
  }
  .field-group input:focus{border-color:var(--navy);}
  .field-group input::placeholder{color:rgba(26,24,20,0.25);}
  .privacy-note{
    font-size:11.5px;line-height:1.65;color:var(--sub);
    background:rgba(86,124,141,0.06);
    border-left:2px solid var(--steel);
    padding:12px 14px;
    border-radius:6px;
    margin:24px 0 22px;
  }
  .privacy-note b{color:var(--navy);font-weight:600;}
  .step-buttons{display:flex;gap:10px;}
  .step-buttons .back{
    flex:0 0 auto;
    background:transparent;color:var(--sub);
    border:1.5px solid rgba(26,24,20,0.15);
    font-family:'DM Sans','Noto Sans TC',sans-serif;font-weight:500;
    font-size:14px;
    padding:0 22px;border-radius:60px;
    cursor:pointer;transition:border-color .2s, color .2s;
  }
  .step-buttons .back:hover{border-color:var(--navy);color:var(--navy);}
  .step-buttons .next{flex:1;}
  .submit-loading{
    display:none;
    text-align:center;font-size:12px;color:var(--sub);
    margin-top:14px;letter-spacing:1px;
  }
  .submit-loading.on{display:block;}

  /* hide sections */
  .hide{display:none !important;}

  /* smooth scroll to next question */
  html{scroll-behavior:smooth;}
</style>
</head>
<body>

<div class="progress-bar"><div class="progress-fill" id="progFill"></div></div>
<div class="progress-label" id="progLabel">0 / 10</div>

<div class="wrap">

  <!-- ===== INTRO (visible by default) ===== -->
  <section id="intro">
    <div class="wm" style="font-size:240px;top:-20px;right:-50px;">健</div>

    <div class="top-row">
      <span>@JIMMY780518</span>
      <span>POLICY CHECK UP</span>
    </div>

    <div class="hero">
      <div class="eng">A policy check up · self assessment</div>
      <h1>保單健檢<br>自查表</h1>
      <p class="sub">10 個問題 抓出你的保單破洞</p>
      <p class="lead">
        不是要你解約 也不是要你多花錢<br>
        只是把所有保單攤開來 <b>看看你繳的錢 有沒有買到真正的保障</b><br><br>
        九成的家庭 都有重複保單<br>
        問題不在買得不夠 而是 <b>同樣預算 買錯位置</b>
      </p>
    </div>

    <div class="how-to">
      <div class="label">使用方式</div>
      <ol>
        <li>把你目前所有的保單一次攤開放在桌上</li>
        <li>對照下面 10 個問題 逐題誠實作答</li>
        <li>系統會自動計算你的破洞數</li>
        <li>勾不出來的題目 就是你需要重新檢視的位置</li>
      </ol>
    </div>

    <button class="begin-btn" id="beginBtn">
      開始自查 <span class="ar">→</span>
    </button>

    <div class="footer">
      <span>JIMMY 780518</span>
      <span>BY JIMMY</span>
    </div>
  </section>

  <!-- ===== QUESTIONS (hidden until begin) ===== -->
  <section id="quiz" class="hide">
    <div class="wm" style="font-size:240px;top:-20px;right:-50px;">問</div>

    <div class="top-row">
      <span>@JIMMY780518</span>
      <span id="qProgress">第 1 / 10 題</span>
    </div>

    <div class="stage-divider" id="stage1">
      <div class="num">I</div>
      <div class="text">你對自己的保單了解多少<small>STAGE ONE · ABOUT YOUR POLICIES</small></div>
    </div>

    <div id="questionList"></div>

    <div class="stage-divider hide" id="stage2">
      <div class="num">II</div>
      <div class="text">你的保障真的賠得到嗎<small>STAGE TWO · WHEN IT MATTERS</small></div>
    </div>

    <div id="questionList2"></div>

    <div class="submit-area">
      <p class="submit-status">已完成 <b id="cnt">0</b> / 10 題</p>
      <button class="submit-btn" id="submitBtn" disabled>看看我的破洞數</button>
    </div>

    <div class="footer">
      <span>JIMMY 780518</span>
      <span>POLICY CHECK UP</span>
    </div>
  </section>

  <!-- ===== CONTACT INFO STEP (hidden until quiz complete) ===== -->
  <section id="contactStep" class="hide">
    <div class="wm" style="font-size:240px;top:-20px;right:-50px;">送</div>

    <div class="top-row">
      <span>@JIMMY780518</span>
      <span>最後一步</span>
    </div>

    <div class="contact-step">
      <div class="eng">One last step</div>
      <h2>留個聯絡方式<br>看你的健檢結果</h2>
      <p class="desc">
        把報告留個地方寄回給你 <b>我會用一個 Email 給你完整健檢分析</b><br>
        包括你的破洞清單 預算建議 和下一步該怎麼做
      </p>

      <div class="field-group">
        <label>姓名 <span class="req">*</span></label>
        <input type="text" id="fName" placeholder="王小明" autocomplete="name">
      </div>
      <div class="field-group">
        <label>Email <span class="req">*</span></label>
        <input type="email" id="fEmail" placeholder="your@email.com" autocomplete="email">
      </div>
      <div class="field-group">
        <label>電話 <span class="opt">選填</span></label>
        <input type="tel" id="fPhone" placeholder="0912-345-678" autocomplete="tel">
      </div>

      <div class="privacy-note">
        <b>不打擾保證</b>：你的資料只會用來寄健檢結果 不會推銷 不會轉給其他人 不留就看不到報告
      </div>

      <div class="step-buttons">
        <button class="back" id="backBtn">返回</button>
        <button class="submit-btn next" id="finalSubmitBtn">送出 看我的結果</button>
      </div>
      <p class="submit-loading" id="loadingMsg">送出中 請稍候</p>
    </div>

    <div class="footer">
      <span>JIMMY 780518</span>
      <span>SECURE · PRIVATE</span>
    </div>
  </section>

  <!-- ===== RESULT (hidden until submit) ===== -->
  <section id="result" class="hide">
    <div class="wm" style="font-size:280px;top:-30px;right:-60px;">解</div>

    <div class="top-row">
      <span>@JIMMY780518</span>
      <span>YOUR RESULT</span>
    </div>

    <div class="result">
      <div class="score-hero">
        <div class="score-eng">Read your result</div>
        <div class="score-circle" id="scoreCircle">
          <svg viewBox="0 0 200 200">
            <circle class="track" cx="100" cy="100" r="90"/>
            <circle class="arc" id="scoreArc" cx="100" cy="100" r="90"/>
          </svg>
          <div class="score-num"><span id="scoreNum">0</span><small> / 10</small></div>
        </div>
        <h2 class="level-title" id="lvlTitle">狀態尚可</h2>
        <p class="level-desc" id="lvlDesc"></p>
      </div>

      <div class="weak-list">
        <div class="head">需要重新檢視的位置</div>
        <div id="weakItems"></div>
      </div>

      <div class="cta-block">
        <div class="label">下一步 NEXT STEP</div>
        <div class="htitle" id="ctaTitle">想找人陪你<br>把錢放回對的位置</div>
        <p class="htext">我會用一個小時 帶你把所有保單攤開<br>標出重複 找出破洞 不推銷 不催解約 只把現況講清楚</p>
        <div class="cta-actions">
          <a class="cta-btn" href="https://www.instagram.com/jimmy780518/" target="_blank" rel="noopener">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="3" y="3" width="18" height="18" rx="5"/><circle cx="12" cy="12" r="4"/><circle cx="17.5" cy="6.5" r="1" fill="currentColor"/></svg>
            追蹤 @jimmy780518
          </a>
          <a class="cta-btn secondary" href="https://www.instagram.com/jimmy780518/" target="_blank" rel="noopener">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M21 11.5a8.5 8.5 0 0 1-12 7.7L3 21l1.8-6a8.5 8.5 0 1 1 16.2-3.5z"/></svg>
            私訊「健檢」預約
          </a>
        </div>
      </div>

      <p class="signoff">Your policy should pay you back<br>not just take payments</p>

      <div class="restart">
        <button id="restartBtn">重新作答</button>
      </div>
    </div>

    <div class="footer">
      <span>JIMMY 780518</span>
      <span>BY JIMMY</span>
    </div>
  </section>

</div>

<script>
/* =================================================================
   QUESTION DATA
   - first option of each = "knows it" (0 pt = no gap)
   - the rest score 1 (gap)
   ================================================================= */
const QUESTIONS = [
  // stage 1
  {stage:1, q:'你能立刻說出 自己目前共有幾張保單嗎', hint:'連有幾張都答不出來 是健檢的第一個訊號',
    options:[{t:'可以',pt:0},{t:'大概',pt:1},{t:'不行',pt:1}]},
  {stage:1, q:'你知道自己每年繳出去的保費總額是多少嗎', hint:'預算沒概念 就永遠不知道是不是繳太多',
    options:[{t:'清楚知道',pt:0},{t:'大概有概念',pt:1},{t:'完全不知道',pt:1}]},
  {stage:1, q:'你分得清「實支實付」和「日額型」醫療險的差別嗎', hint:'兩種理賠邏輯完全不同 買錯位置 是最常見的錢花在沒用的地方',
    options:[{t:'分得清',pt:0},{t:'分不清',pt:1}]},
  {stage:1, q:'你目前是否有 2 張以上同類型的醫療險', hint:'重複保障是同一筆預算的浪費起點 看完所有保單才知道',
    options:[{t:'沒有',pt:0},{t:'有',pt:1},{t:'不確定',pt:1}]},
  {stage:1, q:'你知道「重大疾病」和「重大傷病」的差別在哪嗎', hint:'一字之差 理賠範圍可以差 3 倍以上',
    options:[{t:'知道差別',pt:0},{t:'聽過但分不清',pt:1},{t:'從來沒注意',pt:1}]},
  // stage 2
  {stage:2, q:'你的意外險保額 有達到年收入的 10 倍以上嗎', hint:'萬一意外發生 家人靠這筆要撐多久',
    options:[{t:'有',pt:0},{t:'沒有',pt:1},{t:'不知道保額',pt:1}]},
  {stage:2, q:'如果今天確診重大傷病 你的保單能一次給付多少', hint:'治療空窗期最燒錢 一次給付是救急的生命線',
    options:[{t:'知道金額',pt:0},{t:'大概有印象',pt:1},{t:'完全不知道',pt:1}]},
  {stage:2, q:'你的失能扶助 每月可領多少 領多久', hint:'失能不是一次性 是要撐 10 年 20 年的長期支出',
    options:[{t:'都知道',pt:0},{t:'只知道金額',pt:1},{t:'都不知道',pt:1}]},
  {stage:2, q:'家中經濟支柱的壽險保額 夠家人撐幾年生活', hint:'壽險不是保自己 是留給家人的時間緩衝',
    options:[{t:'5 年以上',pt:0},{t:'不到 5 年',pt:1},{t:'不知道',pt:1}]},
  {stage:2, q:'你最後一次把所有保單攤開重新看過 是什麼時候', hint:'保單就像體檢 三年沒看一次 多繳少賠都不奇怪',
    options:[{t:'一年內',pt:0},{t:'三年內',pt:1},{t:'超過三年',pt:1},{t:'沒看過',pt:1}]},
];

const RESULTS = {
  low:{
    range:'0-3',
    title:'狀態尚可 但別鬆懈',
    desc:'你對自己的保單有<b>基本掌握</b> 建議每年回顧一次 確認保障跟人生階段同步 別讓時間把好保單變成過時保單',
    ctaTitle:'維持每年健檢一次<br>確保保障跟得上人生',
    klass:'low',
  },
  mid:{
    range:'4-6',
    title:'有破洞 該重新檢視',
    desc:'你正在繳費 卻沒搞清楚自己到底買到什麼 同樣的預算 <b>有很大機率可以買到更對的保障</b>',
    ctaTitle:'你的預算可能買錯位置<br>來聊聊怎麼補回來',
    klass:'warn',
  },
  high:{
    range:'7-10',
    title:'嚴重 建議盡快健檢',
    desc:'你可能正在<b>重複繳費</b> 卻沒蓋到真正的風險缺口 不是錢的問題 是位置的問題 越早整理 省下來的越多',
    ctaTitle:'你的保單破洞太多<br>越早整理 越早止血',
    klass:'alert',
  },
};

/* =================================================================
   STATE + RENDER
   ================================================================= */
const state = { answers:new Array(QUESTIONS.length).fill(null) };

function renderQuestions(){
  const list1 = document.getElementById('questionList');
  const list2 = document.getElementById('questionList2');
  list1.innerHTML=''; list2.innerHTML='';
  QUESTIONS.forEach((q,idx)=>{
    const card = document.createElement('div');
    card.className='q-card';
    card.id=`q${idx}`;
    card.innerHTML=`
      <div class="q-num">${String(idx+1).padStart(2,'0')}</div>
      <p class="q-text">${q.q}</p>
      <div class="choices">
        ${q.options.map((o,i)=>`
          <div class="choice" data-q="${idx}" data-i="${i}" data-pt="${o.pt}">
            <span class="box"><svg viewBox="0 0 16 16" fill="none" stroke="white" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"><path d="M3 8.5l3.2 3.2L13 5"/></svg></span>
            <span class="label">${o.t}</span>
            <span class="pts">${o.pt===0?'安全':'有破洞'}</span>
          </div>
        `).join('')}
      </div>
      <p class="hint">${q.hint}</p>
    `;
    (q.stage===1?list1:list2).appendChild(card);
  });

  document.querySelectorAll('.choice').forEach(el=>{
    el.addEventListener('click',()=>{
      const qi = +el.dataset.q;
      const ii = +el.dataset.i;
      const card = document.getElementById('q'+qi);
      card.querySelectorAll('.choice').forEach(c=>c.classList.remove('selected'));
      el.classList.add('selected');
      card.classList.add('answered');
      state.answers[qi] = +el.dataset.pt;
      updateProgress();
      // auto-scroll to next unanswered question
      const next = state.answers.findIndex(a=>a===null);
      if(next>=0 && next!==qi){
        setTimeout(()=>{
          const nextCard = document.getElementById('q'+next);
          if(nextCard) nextCard.scrollIntoView({behavior:'smooth', block:'center'});
        },220);
      }
    });
  });
}

function updateProgress(){
  const done = state.answers.filter(a=>a!==null).length;
  const pct = (done/QUESTIONS.length)*100;
  document.getElementById('progFill').style.width = pct+'%';
  document.getElementById('progLabel').textContent = `${done} / 10`;
  document.getElementById('cnt').textContent = done;
  document.getElementById('qProgress').textContent = `第 ${Math.min(done+1,10)} / 10 題`;
  const btn = document.getElementById('submitBtn');
  btn.disabled = done < QUESTIONS.length;
}

function showResult(){
  const score = state.answers.reduce((s,v)=>s+(v||0),0);
  const tier = score<=3?'low':score<=6?'mid':'high';
  const meta = RESULTS[tier];

  // hide quiz, show result
  document.getElementById('quiz').classList.add('hide');
  document.getElementById('result').classList.remove('hide');
  window.scrollTo({top:0, behavior:'instant'});

  // animate score number
  const numEl = document.getElementById('scoreNum');
  let cur = 0;
  const step = ()=>{
    cur += score/24;
    if(cur >= score){ numEl.textContent = score; return; }
    numEl.textContent = Math.round(cur);
    requestAnimationFrame(step);
  };
  step();

  // animate arc
  const circ = document.getElementById('scoreCircle');
  circ.classList.remove('warn','alert');
  if(meta.klass==='warn') circ.classList.add('warn');
  if(meta.klass==='alert') circ.classList.add('alert');
  const arc = document.getElementById('scoreArc');
  const total = 2*Math.PI*90;
  const offset = total * (1 - score/10);
  requestAnimationFrame(()=>{ arc.style.strokeDashoffset = offset; });

  // titles
  document.getElementById('lvlTitle').textContent = meta.title;
  document.getElementById('lvlDesc').innerHTML = meta.desc;
  document.getElementById('ctaTitle').innerHTML = meta.ctaTitle;

  // weak-item list
  const weakWrap = document.getElementById('weakItems');
  weakWrap.innerHTML = '';
  const weak = QUESTIONS.map((q,i)=>({q,i,gap:state.answers[i]})).filter(x=>x.gap>0);
  if(weak.length===0){
    weakWrap.innerHTML = '<p class="empty">沒有破洞 你已經做到大多數人都沒做的事</p>';
  }else{
    weak.forEach(w=>{
      const row = document.createElement('div');
      row.className='weak-item';
      row.innerHTML = `<span class="wn">${String(w.i+1).padStart(2,'0')}</span><span class="wt">${w.q.q}</span>`;
      weakWrap.appendChild(row);
    });
  }

  // hide top progress label on result
  document.getElementById('progLabel').classList.add('hide');
  document.getElementById('progFill').style.width = '100%';
}

function restart(){
  state.answers = new Array(QUESTIONS.length).fill(null);
  document.getElementById('result').classList.add('hide');
  document.getElementById('quiz').classList.remove('hide');
  document.getElementById('progLabel').classList.remove('hide');
  document.querySelectorAll('.choice').forEach(c=>c.classList.remove('selected'));
  document.querySelectorAll('.q-card').forEach(c=>c.classList.remove('answered'));
  // reset arc
  document.getElementById('scoreArc').style.strokeDashoffset = 565;
  updateProgress();
  window.scrollTo({top:0, behavior:'smooth'});
}

/* =================================================================
   GOOGLE FORM CONFIG
   ================================================================= */
const FORM_URL = 'https://docs.google.com/forms/d/e/1FAIpQLScxpZaOZ-wvBptM7VkS7OLBpNBYWNf_-B0-oJYC60-R-ceQ6A/formResponse';
const ENTRY = {
  name:    'entry.476516404',
  email:   'entry.623678524',
  phone:   'entry.1530476829',
  score:   'entry.1545325841',
  weak:    'entry.1639096854',
  q1:      'entry.316693669',
  q2:      'entry.1871763683',
  q3:      'entry.792263351',
  q4:      'entry.1458294786',
  q5:      'entry.1950029648',
  q6:      'entry.6701509',
  q7:      'entry.107697149',
  q8:      'entry.750779288',
  q9:      'entry.1984276842',
  q10:     'entry.2118661792',
};

// Submit via hidden iframe + form (most compatible method)
// Works in iOS Safari, all in-app browsers (LINE, Threads, Instagram, Facebook),
// and avoids cross-origin fetch restrictions entirely.
function sendToGoogleForm(payload){
  return new Promise((resolve)=>{
    // create or reuse hidden iframe
    let iframe = document.getElementById('gform-iframe');
    if(!iframe){
      iframe = document.createElement('iframe');
      iframe.id = 'gform-iframe';
      iframe.name = 'gform-iframe';
      iframe.style.cssText = 'position:absolute;width:0;height:0;border:0;visibility:hidden;';
      document.body.appendChild(iframe);
    }

    // build a hidden form pointing at the iframe
    const form = document.createElement('form');
    form.action = FORM_URL;
    form.method = 'POST';
    form.target = 'gform-iframe';
    form.style.display = 'none';
    form.acceptCharset = 'UTF-8';

    for(const k in payload){
      const input = document.createElement('input');
      input.type = 'hidden';
      input.name = k;
      input.value = (payload[k] === undefined || payload[k] === null) ? '' : String(payload[k]);
      form.appendChild(input);
    }

    document.body.appendChild(form);

    // resolve when iframe finishes loading (or after timeout fallback)
    let done = false;
    const finish = ()=>{ if(done) return; done = true; resolve(); };
    iframe.addEventListener('load', finish, {once:true});
    setTimeout(finish, 2500); // safety timeout

    try{
      form.submit();
    }catch(err){
      console.warn('form submit threw', err);
      finish();
    }

    // cleanup form element after submit
    setTimeout(()=>{ try{ form.remove(); }catch(e){} }, 3000);
  });
}

function buildPayload(){
  const score = state.answers.reduce((s,v)=>s+(v||0),0);
  const weakItems = QUESTIONS
    .map((q,i)=>({q,i,gap:state.answers[i]}))
    .filter(x=>x.gap>0)
    .map(x=>`Q${x.i+1}: ${x.q.q}`)
    .join('\n');

  // capture each question's selected option text
  const qTexts = {};
  QUESTIONS.forEach((q,i)=>{
    const card = document.getElementById('q'+i);
    const selected = card ? card.querySelector('.choice.selected .label') : null;
    qTexts['q'+(i+1)] = selected ? selected.textContent.trim() : '';
  });

  return {
    [ENTRY.name]:  document.getElementById('fName').value.trim(),
    [ENTRY.email]: document.getElementById('fEmail').value.trim(),
    [ENTRY.phone]: document.getElementById('fPhone').value.trim(),
    [ENTRY.score]: `${score} / 10`,
    [ENTRY.weak]:  weakItems || '（沒有破洞）',
    [ENTRY.q1]:    qTexts.q1,
    [ENTRY.q2]:    qTexts.q2,
    [ENTRY.q3]:    qTexts.q3,
    [ENTRY.q4]:    qTexts.q4,
    [ENTRY.q5]:    qTexts.q5,
    [ENTRY.q6]:    qTexts.q6,
    [ENTRY.q7]:    qTexts.q7,
    [ENTRY.q8]:    qTexts.q8,
    [ENTRY.q9]:    qTexts.q9,
    [ENTRY.q10]:   qTexts.q10,
  };
}

function validateContact(){
  const name = document.getElementById('fName').value.trim();
  const email = document.getElementById('fEmail').value.trim();
  if(!name){ alert('請填寫姓名'); document.getElementById('fName').focus(); return false; }
  if(!email){ alert('請填寫 Email'); document.getElementById('fEmail').focus(); return false; }
  if(!/^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(email)){
    alert('Email 格式好像不對'); document.getElementById('fEmail').focus(); return false;
  }
  return true;
}

/* =================================================================
   WIRE
   ================================================================= */
document.getElementById('beginBtn').addEventListener('click',()=>{
  document.getElementById('intro').classList.add('hide');
  document.getElementById('quiz').classList.remove('hide');
  document.getElementById('progLabel').classList.remove('hide');
  window.scrollTo({top:0, behavior:'instant'});
});

// "看看我的破洞數" -> show contact step
document.getElementById('submitBtn').addEventListener('click',()=>{
  document.getElementById('quiz').classList.add('hide');
  document.getElementById('contactStep').classList.remove('hide');
  document.getElementById('progLabel').classList.add('hide');
  window.scrollTo({top:0, behavior:'instant'});
});

// back button
document.getElementById('backBtn').addEventListener('click',()=>{
  document.getElementById('contactStep').classList.add('hide');
  document.getElementById('quiz').classList.remove('hide');
  document.getElementById('progLabel').classList.remove('hide');
  window.scrollTo({top:document.body.scrollHeight, behavior:'instant'});
});

// final submit -> post to google form -> show result
document.getElementById('finalSubmitBtn').addEventListener('click', async ()=>{
  if(!validateContact()) return;
  const btn = document.getElementById('finalSubmitBtn');
  const loading = document.getElementById('loadingMsg');
  btn.disabled = true;
  btn.textContent = '送出中...';
  loading.classList.add('on');

  const payload = buildPayload();
  await sendToGoogleForm(payload);

  // small delay so user feels the submit happened, then reveal result
  setTimeout(()=>{
    document.getElementById('contactStep').classList.add('hide');
    showResult();
    btn.disabled = false;
    btn.textContent = '送出 看我的結果';
    loading.classList.remove('on');
  }, 500);
});

document.getElementById('restartBtn').addEventListener('click',restart);

renderQuestions();
updateProgress();
document.getElementById('progLabel').classList.add('hide');
</script>
</body>
</html>
