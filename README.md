INDIAN POLIY TOP 100 QUESTION 
<!DOCTYPE html>
<html lang="hi">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
  <title>Polity 50 Mock Test - 10 Minutes</title>
  <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;500;700&display=swap" rel="stylesheet">
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: 'Roboto', -apple-system, BlinkMacSystemFont, sans-serif;
      -webkit-tap-highlight-color: transparent;
    }

    body {
      background-color: #ffffff;
      color: #1e293b;
      display: flex;
      flex-direction: column;
      height: 100vh;
      overflow: hidden;
    }

    /* 1. TOP APP BAR */
    .top-header {
      background: #002d9c;
      color: #ffffff;
      padding: 10px 14px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      height: 52px;
      flex-shrink: 0;
    }

    .header-left {
      display: flex;
      align-items: center;
      gap: 16px;
      font-size: 20px;
      cursor: pointer;
    }

    .header-right {
      display: flex;
      align-items: center;
      gap: 10px;
    }

    .icon-btn {
      background: transparent;
      border: none;
      color: #ffffff;
      font-size: 19px;
      cursor: pointer;
      display: flex;
      align-items: center;
    }

    .lang-switcher {
      border: 1px solid rgba(255, 255, 255, 0.7);
      border-radius: 4px;
      padding: 3px 6px;
      font-size: 11px;
      font-weight: 700;
      display: flex;
      align-items: center;
      gap: 3px;
      background: rgba(255, 255, 255, 0.1);
    }

    /* 10 MINUTE TIMER DISPLAY */
    .timer-box {
      display: flex;
      gap: 2px;
      background: #ffffff;
      padding: 2px 5px;
      border-radius: 3px;
    }

    .timer-segment {
      background: #ffffff;
      color: #002d9c;
      font-weight: 700;
      font-size: 13px;
      min-width: 18px;
      text-align: center;
    }
    .timer-sep {
      color: #002d9c;
      font-weight: 700;
      font-size: 13px;
    }

    /* 2. SUB BAR */
    .sub-bar {
      background: #e2e8f0;
      padding: 6px 14px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      flex-shrink: 0;
    }

    .test-badge {
      background: #002d9c;
      color: #ffffff;
      display: inline-block;
      font-size: 12px;
      font-weight: 700;
      padding: 4px 14px;
      border-radius: 4px;
    }

    .score-badge {
      font-size: 12px;
      font-weight: 700;
      color: #002d9c;
    }

    /* 3. QUESTION CONTENT AREA */
    .test-body {
      flex: 1;
      overflow-y: auto;
      padding: 16px 16px 90px;
    }

    .q-meta-row {
      display: flex;
      justify-content: space-between;
      align-items: center;
      border-bottom: 1px solid #e2e8f0;
      padding-bottom: 8px;
      margin-bottom: 14px;
    }

    .q-number {
      font-size: 16px;
      font-weight: 700;
      color: #0f172a;
    }

    .q-actions {
      display: flex;
      gap: 16px;
      color: #64748b;
      font-size: 18px;
    }
    .q-action-icon {
      cursor: pointer;
    }
    .q-action-icon.bookmarked {
      color: #002d9c;
    }

    .question-text {
      font-size: 16px;
      line-height: 1.5;
      font-weight: 600;
      color: #1e293b;
      margin-bottom: 20px;
      min-height: 48px;
    }

    /* OPTIONS */
    .options-list {
      display: flex;
      flex-direction: column;
      gap: 12px;
    }

    .option-card {
      border: 1px solid #cbd5e1;
      border-radius: 6px;
      padding: 12px 14px;
      display: flex;
      align-items: center;
      gap: 12px;
      cursor: pointer;
      background: #ffffff;
      transition: all 0.15s ease;
    }

    .option-card:hover {
      background: #f8fafc;
    }

    .option-card.selected {
      border-color: #002d9c;
      background: #eff6ff;
    }

    .custom-radio {
      width: 18px;
      height: 18px;
      border: 1.5px solid #64748b;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      flex-shrink: 0;
    }

    .option-card.selected .custom-radio {
      border-color: #002d9c;
    }

    .option-card.selected .custom-radio::after {
      content: "";
      width: 9px;
      height: 9px;
      background: #002d9c;
      border-radius: 50%;
    }

    .option-title {
      font-size: 14.5px;
      color: #1e293b;
      font-weight: 500;
    }

    /* FLOATING QUESTION PALETTE BUTTON */
    .palette-fab {
      position: fixed;
      right: 18px;
      bottom: 70px;
      width: 48px;
      height: 48px;
      border-radius: 50%;
      background: #22c55e;
      color: #ffffff;
      border: none;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 22px;
      box-shadow: 0 4px 12px rgba(34, 197, 94, 0.4);
      cursor: pointer;
      z-index: 90;
    }

    /* 4. BOTTOM ACTION BAR */
    .bottom-bar {
      position: fixed;
      bottom: 0;
      left: 0;
      right: 0;
      background: #ffffff;
      border-top: 1px solid #e2e8f0;
      display: grid;
      grid-template-columns: 1fr 1fr 1fr 1fr;
      gap: 6px;
      padding: 8px 8px 12px;
      z-index: 100;
    }

    .btn-quiz {
      border: none;
      border-radius: 4px;
      font-size: 11.5px;
      font-weight: 700;
      padding: 9px 4px;
      cursor: pointer;
      text-align: center;
      display: flex;
      align-items: center;
      justify-content: center;
      line-height: 1.2;
    }

    .btn-prev {
      background: #002d9c;
      color: #ffffff;
    }

    .btn-review {
      background: #ffffff;
      color: #002d9c;
      border: 1px solid #002d9c;
    }

    .btn-clear {
      background: #ffffff;
      color: #dc2626;
      border: 1px solid #dc2626;
    }

    .btn-next {
      background: #002d9c;
      color: #ffffff;
    }

    /* DRAWER POPUP FOR 50 QUESTIONS */
    .palette-drawer {
      position: fixed;
      inset: 0;
      background: rgba(0, 0, 0, 0.5);
      display: none;
      justify-content: flex-end;
      z-index: 200;
    }

    .drawer-content {
      width: 86%;
      max-width: 340px;
      background: #ffffff;
      height: 100%;
      padding: 16px;
      display: flex;
      flex-direction: column;
    }

    .drawer-header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      border-bottom: 1px solid #e2e8f0;
      padding-bottom: 10px;
      font-weight: 700;
      font-size: 15px;
    }

    .palette-legend {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      font-size: 11px;
      padding: 10px 0;
      border-bottom: 1px solid #e2e8f0;
    }
    .legend-item { display: flex; align-items: center; gap: 4px; }
    .legend-box { width: 12px; height: 12px; border-radius: 2px; }

    .grid-container {
      display: grid;
      grid-template-columns: repeat(5, 1fr);
      gap: 8px;
      padding: 14px 0;
      overflow-y: auto;
      flex: 1;
    }

    .grid-num {
      height: 38px;
      border: 1px solid #cbd5e1;
      border-radius: 4px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 12px;
      font-weight: 700;
      cursor: pointer;
    }

    .grid-num.current { border: 2px solid #002d9c; }
    .grid-num.answered { background: #22c55e; color: #fff; border-color: #22c55e; }
    .grid-num.reviewed { background: #8b5cf6; color: #fff; border-color: #8b5cf6; }

    .submit-test-btn {
      background: #dc2626;
      color: #fff;
      border: none;
      padding: 12px;
      border-radius: 4px;
      font-weight: 700;
      cursor: pointer;
      margin-top: 10px;
    }

    /* RESULT MODAL POPUP */
    .result-modal {
      position: fixed;
      inset: 0;
      background: rgba(0,0,0,0.6);
      display: none;
      align-items: center;
      justify-content: center;
      z-index: 300;
      padding: 16px;
    }
    .result-card {
      background: #fff;
      border-radius: 8px;
      padding: 24px;
      max-width: 400px;
      width: 100%;
      text-align: center;
    }
    .result-card h3 {
      color: #002d9c;
      font-size: 20px;
      margin-bottom: 10px;
    }
    .score-circle {
      font-size: 32px;
      font-weight: 900;
      color: #22c55e;
      margin: 14px 0;
    }
    .result-details {
      font-size: 13.5px;
      color: #475569;
      text-align: left;
      line-height: 1.8;
      border-top: 1px dashed #cbd5e1;
      border-bottom: 1px dashed #cbd5e1;
      padding: 10px 0;
      margin-bottom: 16px;
    }
    .restart-btn {
      background: #002d9c;
      color: #fff;
      border: none;
      padding: 10px 20px;
      border-radius: 4px;
      font-weight: 700;
      cursor: pointer;
    }
  </style>
</head>
<body>

  <!-- 1. TOP HEADER -->
  <header class="top-header">
    <div class="header-left">
      <span onclick="window.history.back()">←</span>
    </div>
    <div class="header-right">
      <button class="icon-btn" id="pauseBtn" title="Pause">⏸</button>
      
      <div class="lang-switcher">
        <span>हिन्दी A</span>
        <span style="font-size:9px;">▼</span>
      </div>

      <!-- TIMER (00:10:00) -->
      <div class="timer-box">
        <span class="timer-segment" id="tHours">00</span>
        <span class="timer-sep">:</span>
        <span class="timer-segment" id="tMinutes">10</span>
        <span class="timer-sep">:</span>
        <span class="timer-segment" id="tSeconds">00</span>
      </div>
    </div>
  </header>

  <!-- 2. SUB BAR -->
  <div class="sub-bar">
    <div class="test-badge">Indian Polity (50 Questions)</div>
    <div class="score-badge" id="attemptCount">Attempted: 0/50</div>
  </div>

  <!-- 3. QUESTION & OPTIONS BODY (YAHAN QUESTION DIKHEGA) -->
  <main class="test-body">
    <div class="q-meta-row">
      <div class="q-number" id="qNumText">No. 1</div>
      <div class="q-actions">
        <span class="q-action-icon" id="bookmarkBtn" title="Bookmark">🔖</span>
        <span class="q-action-icon" title="Report Issue">⚠️</span>
      </div>
    </div>

    <!-- Question Text -->
    <div class="question-text" id="qText">
      भारत के नियंत्रक एवं महालेखा परीक्षक (CAG) से संबंधित भारतीय संविधान का अनुच्छेद है-
    </div>

    <!-- Options List -->
    <div class="options-list" id="optionsContainer">
      <!-- Options code se direct load honge -->
    </div>
  </main>

  <!-- FLOATING QUESTION PALETTE BUTTON -->
  <button class="palette-fab" id="openPaletteBtn" title="View Question Sheet">
    ☰
  </button>

  <!-- 4. BOTTOM ACTION BAR -->
  <footer class="bottom-bar">
    <button class="btn-quiz btn-prev" id="btnPrev">Previous<br>Question</button>
    <button class="btn-quiz btn-review" id="btnReview">Mark &amp; Save<br>For Review</button>
    <button class="btn-quiz btn-clear" id="btnClear">Clear<br>Response</button>
    <button class="btn-quiz btn-next" id="btnNext">Save &amp; Next</button>
  </footer>

  <!-- QUESTION PALETTE DRAWER -->
  <div class="palette-drawer" id="paletteDrawer">
    <div class="drawer-content">
      <div class="drawer-header">
        <span>Question Palette (1 to 50)</span>
        <span style="cursor:pointer;" id="closePaletteBtn">✕</span>
      </div>
      <div class="palette-legend">
        <div class="legend-item"><div class="legend-box" style="background:#22c55e;"></div> Answered</div>
        <div class="legend-item"><div class="legend-box" style="background:#8b5cf6;"></div> Review</div>
        <div class="legend-item"><div class="legend-box" style="border:1px solid #cbd5e1;"></div> Not Visited</div>
      </div>
      <div class="grid-container" id="gridNumbers"></div>
      <button class="submit-test-btn" id="submitTestBtn">Submit Test &amp; View Result</button>
    </div>
  </div>

  <!-- RESULT POPUP MODAL -->
  <div class="result-modal" id="resultModal">
    <div class="result-card">
      <h3>🎉 Test Complete!</h3>
      <div class="score-circle" id="finalScore">0 / 50</div>
      <div class="result-details">
        <div>Total Questions: <strong>50</strong></div>
        <div>Attempted: <strong id="resAttempted">0</strong></div>
        <div>Correct Answers: <strong style="color:#22c55e;" id="resCorrect">0</strong></div>
        <div>Wrong Answers: <strong style="color:#dc2626;" id="resWrong">0</strong></div>
        <div>Percentage: <strong id="resPercent">0%</strong></div>
      </div>
      <button class="restart-btn" onclick="location.reload()">Re-attempt Test</button>
    </div>
  </div>

  <script>
    const questions = [
      { id: 1, text: "भारत के नियंत्रक एवं महालेखा परीक्षक (CAG) से संबंधित भारतीय संविधान का अनुच्छेद है-", options: ["अनुच्छेद 162", "अनुच्छेद 123", "अनुच्छेद 148", "अनुच्छेद 180"], correct: 2 },
      { id: 2, text: "भारतीय संविधान सभा के स्थायी अध्यक्ष कौन थे?", options: ["डॉ. बी. आर. अम्बेडकर", "डॉ. राजेन्द्र प्रसाद", "डॉ. सच्चिदानंद सिन्हा", "पं. जवाहरलाल नेहरू"], correct: 1 },
      { id: 3, text: "संविधान प्रारूप समिति (Drafting Committee) के अध्यक्ष कौन थे?", options: ["डॉ. बी. आर. अम्बेडकर", "बी. एन. राव", "के. एम. मुंशी", "सरदार वल्लभभाई पटेल"], correct: 0 },
      { id: 4, text: "भारतीय संविधान में मौलिक अधिकार किस देश के संविधान से लिए गए हैं?", options: ["ब्रिटेन", "संयुक्त राज्य अमेरिका", "रूस", "आयरलैंड"], correct: 1 },
      { id: 5, text: "राज्य के नीति निर्देशक तत्व (DPSP) किस देश से प्रेरित हैं?", options: ["आयरलैंड", "कनाडा", "ऑस्ट्रेलिया", "दक्षिण अफ्रीका"], correct: 0 },
      { id: 6, text: "संविधान की प्रस्तावना में 42वें संशोधन (1976) द्वारा कौन-से शब्द जोड़े गए थे?", options: ["समाजवाद, पंथनिरपेक्ष और अखंडता", "स्वतंत्रता, समता और बंधुत्व", "संप्रभुता और लोकतंत्र", "न्याय और एकता"], correct: 0 },
      { id: 7, text: "संविधान के किस अनुच्छेद के तहत अस्पृश्यता (Untouchability) का अंत किया गया है?", options: ["अनुच्छेद 14", "अनुच्छेद 17", "अनुच्छेद 19", "अनुच्छेद 21"], correct: 1 },
      { id: 8, text: "अनुच्छेद 21 निम्नलिखित में से किस अधिकार से संबंधित है?", options: ["भाषण की स्वतंत्रता", "प्राण एवं दैहिक स्वतंत्रता", "धार्मिक स्वतंत्रता", "शिक्षा का अधिकार"], correct: 1 },
      { id: 9, text: "'संवैधानिक उपचारों का अधिकार' (Right to Constitutional Remedies) किस अनुच्छेद में है?", options: ["अनुच्छेद 19", "अनुच्छेद 32", "अनुच्छेद 40", "अनुच्छेद 226"], correct: 1 },
      { id: 10, text: "डॉ. बी. आर. अम्बेडकर ने किसे 'संविधान की आत्मा एवं हृदय' कहा था?", options: ["प्रस्तावना को", "अनुच्छेद 32 को", "मौलिक अधिकारों को", "नीति निर्देशक तत्वों को"], correct: 1 },
      { id: 11, text: "भारतीय संविधान में वर्तमान में मौलिक कर्तव्यों की कुल संख्या कितनी है?", options: ["10", "11", "12", "7"], correct: 1 },
      { id: 12, text: "मौलिक कर्तव्य किस समिति की सिफारिश पर जोड़े गए थे?", options: ["सरकारिया आयोग", "स्वर्ण सिंह समिति", "बलवंत राय मेहता समिति", "वर्मा समिति"], correct: 1 },
      { id: 13, text: "ग्राम पंचायतों का संगठन संविधान के किस अनुच्छेद में वर्णित है?", options: ["अनुच्छेद 36", "अनुच्छेद 40", "अनुच्छेद 44", "अनुच्छेद 48"], correct: 1 },
      { id: 14, text: "समान नागरिक संहिता (Uniform Civil Code) का संबंध किस अनुच्छेद से है?", options: ["अनुच्छेद 42", "अनुच्छेद 44", "अनुच्छेद 45", "अनुच्छेद 50"], correct: 1 },
      { id: 15, text: "भारत के राष्ट्रपति बनने हेतु न्यूनतम आयु सीमा कितनी है?", options: ["25 वर्ष", "30 वर्ष", "35 वर्ष", "21 वर्ष"], correct: 2 },
      { id: 16, text: "राष्ट्रपति पर महाभियोग (Impeachment) चलाने की प्रक्रिया किस अनुच्छेद में है?", options: ["अनुच्छेद 56", "अनुच्छेद 61", "अनुच्छेद 72", "अनुच्छेद 76"], correct: 1 },
      { id: 17, text: "राष्ट्रपति द्वारा क्षमादान की शक्ति किस अनुच्छेद में दी गई है?", options: ["अनुच्छेद 72", "अनुच्छेद 74", "अनुच्छेद 123", "अनुच्छेद 143"], correct: 0 },
      { id: 18, text: "राष्ट्रपति अध्यादेश (Ordinance) किस अनुच्छेद के अंतर्गत जारी करते हैं?", options: ["अनुच्छेद 110", "अनुच्छेद 123", "अनुच्छेद 213", "अनुच्छेद 352"], correct: 1 },
      { id: 19, text: "राज्यसभा का पदेन सभापति (Ex-officio Chairman) कौन होता है?", options: ["राष्ट्रपति", "उपराष्ट्रपति", "प्रधानमंत्री", "लोकसभा अध्यक्ष"], correct: 1 },
      { id: 20, text: "भारत के महान्यायवादी (Attorney General) की नियुक्ति किस अनुच्छेद के तहत होती है?", options: ["अनुच्छेद 76", "अनुच्छेद 148", "अनुच्छेद 165", "अनुच्छेद 280"], correct: 0 },
      { id: 21, text: "राज्य के महाधिवक्ता (Advocate General) की नियुक्ति किस अनुच्छेद से संबंधित है?", options: ["अनुच्छेद 165", "अनुच्छेद 170", "अनुच्छेद 214", "अनुच्छेद 226"], correct: 0 },
      { id: 22, text: "संसद के दोनों सदनों की संयुक्त बैठक (Joint Sitting) की अध्यक्षता कौन करता है?", options: ["राष्ट्रपति", "उपराष्ट्रपति", "लोकसभा अध्यक्ष", "प्रधानमंत्री"], correct: 2 },
      { id: 23, text: "धन विधेयक (Money Bill) की परिभाषा किस अनुच्छेद में दी गई है?", options: ["अनुच्छेद 108", "अनुच्छेद 110", "अनुच्छेद 112", "अनुच्छेद 117"], correct: 1 },
      { id: 24, text: "संविधान में 'वार्षिक वित्तीय विवरण' (बजट) का उल्लेख किस अनुच्छेद में है?", options: ["अनुच्छेद 110", "अनुच्छेद 112", "अनुच्छेद 115", "अनुच्छेद 124"], correct: 1 },
      { id: 25, text: "सर्वोच्च न्यायालय के मुख्य न्यायाधीश की नियुक्ति कौन करता है?", options: ["प्रधानमंत्री", "संसद", "राष्ट्रपति", "कानून मंत्री"], correct: 2 },
      { id: 26, text: "उच्च न्यायालय के न्यायाधीश अपना त्यागपत्र किसे सौंपते हैं?", options: ["राज्यपाल को", "भारत के राष्ट्रपति को", "सर्वोच्च न्यायालय के मुख्य न्यायाधीश को", "मुख्यमंत्री को"], correct: 1 },
      { id: 27, text: "राज्यपाल पद की शपथ कौन दिलाता है?", options: ["राष्ट्रपति", "उच्च न्यायालय के मुख्य न्यायाधीश", "मुख्यमंत्री", "भारत के मुख्य न्यायाधीश"], correct: 1 },
      { id: 28, text: "किस अनुसूची में भारत के राज्यों और केंद्र शासित प्रदेशों का उल्लेख है?", options: ["पहली अनुसूची", "दूसरी अनुसूची", "तीसरी अनुसूची", "सातवीं अनुसूची"], correct: 0 },
      { id: 29, text: "संविधान की आठवीं अनुसूची में कुल कितनी आधिकारिक भाषाएँ हैं?", options: ["18", "20", "22", "24"], correct: 2 },
      { id: 30, text: "दल-बदल विरोधी कानून (Anti-Defection Law) किस अनुसूची से संबंधित है?", options: ["8वीं अनुसूची", "9वीं अनुसूची", "10वीं अनुसूची", "11वीं अनुसूची"], correct: 2 },
      { id: 31, text: "11वीं अनुसूची का संबंध किससे है?", options: ["नगर निगम", "पंचायती राज", "केंद्र-राज्य संबंध", "भाषाएँ"], correct: 1 },
      { id: 32, text: "भारत में त्रि-स्तरीय पंचायती राज व्यवस्था की सिफारिश किसने की थी?", options: ["अशोक मेहता समिति", "बलवंत राय मेहता समिति", "एल. एम. सिंघवी समिति", "पी. के. थुंगन समिति"], correct: 1 },
      { id: 33, text: "73वां संविधान संशोधन किस वर्ष अधिनियमित हुआ था?", options: ["1991", "1992", "1993", "1995"], correct: 1 },
      { id: 34, text: "राष्ट्रीय आपातकाल (National Emergency) किस अनुच्छेद के तहत लगाया जाता है?", options: ["अनुच्छेद 352", "अनुच्छेद 356", "अनुच्छेद 360", "अनुच्छेद 368"], correct: 0 },
      { id: 35, text: "राष्ट्रपति शासन (President's Rule) किस अनुच्छेद के तहत लगाया जाता है?", options: ["अनुच्छेद 352", "अनुच्छेद 356", "अनुच्छेद 360", "अनुच्छेद 370"], correct: 1 },
      { id: 36, text: "वित्तीय आपातकाल (Financial Emergency) का प्रावधान किस अनुच्छेद में है?", options: ["अनुच्छेद 352", "अनुच्छेद 356", "अनुच्छेद 360", "अनुच्छेद 365"], correct: 2 },
      { id: 37, text: "संविधान संशोधन की प्रक्रिया किस अनुच्छेद में वर्णित है?", options: ["अनुच्छेद 356", "अनुच्छेद 368", "अनुच्छेद 370", "अनुच्छेद 390"], correct: 1 },
      { id: 38, text: "संविधान संशोधन की प्रणाली किस देश से ली गई है?", options: ["ऑस्ट्रेलिया", "दक्षिण अफ्रीका", "जर्मनी", "फ्रांस"], correct: 1 },
      { id: 39, text: "भारत के निर्वाचन आयोग (Election Commission) का प्रावधान किस अनुच्छेद में है?", options: ["अनुच्छेद 324", "अनुच्छेद 326", "अनुच्छेद 330", "अनुच्छेद 338"], correct: 0 },
      { id: 40, text: "मतदान की आयु 21 वर्ष से घटाकर 18 वर्ष किस संशोधन द्वारा की गई थी?", options: ["44वां संशोधन", "61वां संशोधन", "73वां संशोधन", "86वां संशोधन"], correct: 1 },
      { id: 41, text: "शिक्षा का अधिकार (RTE) किस संविधान संशोधन द्वारा जोड़ा गया?", options: ["42वां संशोधन", "44वां संशोधन", "86वां संशोधन", "91वां संशोधन"], correct: 2 }# INDIAN-POLITY-TOP-100-QUESTION-
