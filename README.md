<!--DOCTYPE html-->
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>🔒 Grammar Worksheet: since / for & Present Perfect</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: #eef2f5;
            font-family: 'Segoe UI', Roboto, 'Helvetica Neue', sans-serif;
            padding: 40px 20px;
            color: #1e2a3a;
            transition: filter 0.2s;
        }

        /* Blur overlay when locked */
        body.locked .worksheet-container {
            filter: blur(5px);
            pointer-events: none;
            user-select: none;
        }

        body.locked .lock-overlay {
            display: flex;
        }

        .lock-overlay {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.85);
            backdrop-filter: blur(8px);
            z-index: 10000;
            justify-content: center;
            align-items: center;
            font-family: 'Segoe UI', system-ui;
        }

        .lock-card {
            background: white;
            max-width: 460px;
            width: 90%;
            padding: 32px 28px;
            border-radius: 48px;
            text-align: center;
            box-shadow: 0 25px 45px rgba(0,0,0,0.3);
            animation: fadeInUp 0.2s ease;
        }

        .lock-card h2 {
            font-size: 1.8rem;
            margin-bottom: 12px;
            color: #c4452c;
        }

        .lock-card p {
            margin-bottom: 24px;
            color: #2c3e4e;
        }

        .lock-card input {
            width: 100%;
            padding: 14px 18px;
            font-size: 1rem;
            border: 2px solid #d4dee8;
            border-radius: 60px;
            margin-bottom: 18px;
            outline: none;
            text-align: center;
            letter-spacing: 1px;
        }

        .lock-card input:focus {
            border-color: #1f5a7a;
        }

        .lock-card button {
            background: #1f5a7a;
            border: none;
            color: white;
            font-weight: bold;
            padding: 12px 24px;
            border-radius: 60px;
            font-size: 1rem;
            cursor: pointer;
            width: 100%;
            transition: 0.1s;
        }

        .lock-card button:hover {
            background: #0f415b;
        }

        .error-msg {
            color: #d9534f;
            margin-top: 12px;
            font-size: 0.85rem;
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .worksheet-container {
            max-width: 1100px;
            margin: 0 auto;
            background: white;
            border-radius: 28px;
            box-shadow: 0 20px 35px -12px rgba(0, 0, 0, 0.15);
            overflow: hidden;
            padding: 30px 35px 45px;
            transition: all 0.2s;
        }

        h1 {
            font-size: 1.9rem;
            font-weight: 600;
            background: linear-gradient(135deg, #1f4870, #2a6f8f);
            background-clip: text;
            -webkit-background-clip: text;
            color: transparent;
            border-left: 6px solid #2a6f8f;
            padding-left: 20px;
            margin-bottom: 12px;
        }

        .sub {
            color: #4b6f8c;
            margin-bottom: 32px;
            font-size: 1rem;
            border-bottom: 2px solid #e2e8f0;
            padding-bottom: 10px;
        }

        .activity-card {
            background: #fefefe;
            border-radius: 24px;
            margin-bottom: 40px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.03);
            border: 1px solid #e9edf2;
        }

        .activity-title {
            font-size: 1.5rem;
            font-weight: 600;
            background: #f8fafc;
            padding: 16px 24px;
            border-radius: 24px 24px 0 0;
            border-bottom: 2px solid #dee4ec;
            color: #0f3b4f;
        }

        .activity-content {
            padding: 20px 28px 28px 28px;
        }

        .sentence-item {
            background: #f9fafb;
            padding: 12px 16px;
            border-radius: 20px;
            border: 1px solid #eef2f6;
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            justify-content: space-between;
            gap: 12px;
            margin-bottom: 12px;
        }
        .sentence-text {
            flex: 2;
            font-size: 1rem;
            font-weight: 450;
        }
        .option-buttons {
            display: flex;
            gap: 18px;
            align-items: center;
        }
        .option-buttons label {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            cursor: pointer;
            background: white;
            padding: 6px 18px;
            border-radius: 60px;
            border: 1px solid #cfdfed;
        }
        .option-buttons input {
            margin: 0;
            accent-color: #2a6f8f;
            width: 18px;
            height: 18px;
        }

        .fill-input {
            width: auto;
            min-width: 140px;
            padding: 8px 14px;
            border-radius: 40px;
            border: 1px solid #cddfea;
            font-family: monospace;
            font-size: 0.95rem;
            margin-left: 12px;
        }

        .field-row {
            display: flex;
            flex-wrap: wrap;
            align-items: baseline;
            gap: 12px;
            margin-bottom: 18px;
            background: #ffffff;
            padding: 8px 12px;
            border-radius: 18px;
            border: 1px solid #e9edf2;
        }
        .field-label {
            font-weight: 600;
            min-width: 110px;
            color: #1f4e6e;
        }
        .field-input {
            flex: 2;
            padding: 10px 14px;
            border-radius: 40px;
            border: 1px solid #cddfea;
            font-family: 'Segoe UI', monospace;
        }
        .btn-check {
            background: #1f5a7a;
            border: none;
            color: white;
            font-weight: 600;
            padding: 12px 28px;
            border-radius: 60px;
            font-size: 1rem;
            cursor: pointer;
            margin-top: 12px;
            margin-bottom: 18px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        .btn-check:hover {
            background: #0f415b;
            transform: scale(0.98);
        }
        .score-area {
            background: #eef3f7;
            border-radius: 28px;
            padding: 16px 25px;
            margin: 28px 0 10px;
            font-weight: 600;
            font-size: 1.2rem;
            text-align: center;
            border: 1px solid #cde1ec;
        }
        .feedback {
            font-size: 0.85rem;
            margin-top: 8px;
            color: #2c6e2c;
            background: #eef5f9;
            padding: 8px 14px;
            border-radius: 20px;
        }
        .truefalse-group {
            display: flex;
            gap: 20px;
            align-items: center;
            margin-top: 6px;
        }
        .truefalse-group label {
            display: inline-flex;
            align-items: center;
            gap: 6px;
            background: white;
            padding: 4px 14px;
            border-radius: 40px;
            border: 1px solid #bdd7e7;
        }
        .survey-row {
            margin: 12px 0;
            padding: 6px 0;
            border-bottom: 1px dashed #e0e8ef;
        }
        .small-hint {
            background: none;
            border: 1px solid #bdd7e7;
            padding: 6px 14px;
            border-radius: 30px;
            cursor: pointer;
            font-size: 0.75rem;
            margin-top: 8px;
        }
        @media (max-width: 700px) {
            .worksheet-container { padding: 20px; }
            .sentence-item { flex-direction: column; align-items: flex-start; }
        }
    </style>
</head>
<body>

<div id="lockOverlay" class="lock-overlay">
    <div class="lock-card">
        <h2>🔒 Activity Locked</h2>
        <p>⚠️ You left the page, minimized the tab, completed the activity, or the window lost focus.<br>Enter teacher password to continue.</p>
        <input type="password" id="passwordInput" placeholder="Enter password" autocomplete="off">
        <button id="unlockBtn">Unlock Worksheet</button>
        <div id="lockErrorMsg" class="error-msg"></div>
    </div>
</div>

<div class="worksheet-container">
    <h1>📘 since / for & Present Perfect</h1>
    <div class="sub">Complete sentences, true/false, write questions & answers | 🔐 Auto-lock on page leave/minimize + completion lock</div>

    <!-- ACTIVITY 1: Complete with since or for -->
    <div class="activity-card">
        <div class="activity-title">✏️ 1. Complete the sentences with <em>since</em> or <em>for</em></div>
        <div class="activity-content">
            <div class="sentence-item">
                <div class="sentence-text">1️⃣ I've studied English <input type="text" id="gap1" class="fill-input" placeholder="since/for" style="width:100px"> five years.</div>
            </div>
            <div class="sentence-item">
                <div class="sentence-text">2️⃣ We haven't seen Heba <input type="text" id="gap2" class="fill-input" placeholder="since/for" style="width:100px"> last Sunday.</div>
            </div>
            <div class="sentence-item">
                <div class="sentence-text">3️⃣ Kamal's built robots <input type="text" id="gap3" class="fill-input" placeholder="since/for" style="width:100px"> he was nine.</div>
            </div>
            <div class="sentence-item">
                <div class="sentence-text">4️⃣ I've been on the football team <input type="text" id="gap4" class="fill-input" placeholder="since/for" style="width:100px"> several years.</div>
            </div>
            <div class="sentence-item">
                <div class="sentence-text">5️⃣ My cousins have lived in Madaba <input type="text" id="gap5" class="fill-input" placeholder="since/for" style="width:100px"> 2021.</div>
            </div>
            <div class="sentence-item">
                <div class="sentence-text">6️⃣ It hasn't rained here <input type="text" id="gap6" class="fill-input" placeholder="since/for" style="width:100px"> a long time.</div>
            </div>
            <div id="gapFeedback" class="feedback"></div>
        </div>
    </div>

    <!-- ACTIVITY 2: True/False statements (listening implied) -->
    <div class="activity-card">
        <div class="activity-title">🎧 2. Circle T (true) or F (false) — based on the audio/text (inference)</div>
        <div class="activity-content">
            <div class="sentence-item">
                <div class="sentence-text">1️⃣ Habib's been waiting for two hours. (He's been waiting for half an hour) → <strong>False</strong> (example done)</div>
            </div>
            <div class="sentence-item">
                <div class="sentence-text">2️⃣ Asma's lived in Amman since she was six.</div>
                <div class="truefalse-group">
                    <label><input type="radio" name="tf2" value="T"> T</label>
                    <label><input type="radio" name="tf2" value="F"> F</label>
                </div>
            </div>
            <div class="sentence-item">
                <div class="sentence-text">3️⃣ Zeina hasn't seen Samar since last October.</div>
                <div class="truefalse-group">
                    <label><input type="radio" name="tf3" value="T"> T</label>
                    <label><input type="radio" name="tf3" value="F"> F</label>
                </div>
            </div>
            <div class="sentence-item">
                <div class="sentence-text">4️⃣ Hisham's known Mazen for two weeks.</div>
                <div class="truefalse-group">
                    <label><input type="radio" name="tf4" value="T"> T</label>
                    <label><input type="radio" name="tf4" value="F"> F</label>
                </div>
            </div>
            <div class="sentence-item">
                <div class="sentence-text">5️⃣ Ibrahim's wanted to visit London since he was little.</div>
                <div class="truefalse-group">
                    <label><input type="radio" name="tf5" value="T"> T</label>
                    <label><input type="radio" name="tf5" value="F"> F</label>
                </div>
            </div>
            <div id="tfFeedback" class="feedback"></div>
            <div class="example-text" style="margin-top:12px">💡 Explanation: Refer to implied context (standard answers: T, T, T, T based on typical present perfect truth).</div>
        </div>
    </div>

    <!-- ACTIVITY 3: Write survey questions with How long + Present perfect -->
    <div class="activity-card">
        <div class="activity-title">📝 3. Write survey questions with <em>How long</em> and Present Perfect</div>
        <div class="activity-content">
            <div class="field-row"><span class="field-label">1️⃣ you / live / in this town</span> <input type="text" id="surveyQ1" class="field-input" placeholder="How long have you lived in this town?"></div>
            <div class="field-row"><span class="field-label">2️⃣ you / be / a pupil</span> <input type="text" id="surveyQ2" class="field-input" placeholder="How long have you been a pupil?"></div>
            <div class="field-row"><span class="field-label">3️⃣ you / study / English</span> <input type="text" id="surveyQ3" class="field-input" placeholder="How long have you studied English?"></div>
            <div class="field-row"><span class="field-label">4️⃣ you / have / a bicycle</span> <input type="text" id="surveyQ4" class="field-input" placeholder="How long have you had a bicycle?"></div>
            <div class="field-row"><span class="field-label">5️⃣ you / know / your best friend</span> <input type="text" id="surveyQ5" class="field-input" placeholder="How long have you known your best friend?"></div>
            <div class="field-row"><span class="field-label">6️⃣ you / like / your favourite writer</span> <input type="text" id="surveyQ6" class="field-input" placeholder="How long have you liked your favourite writer?"></div>
            <div id="surveyQFeedback" class="feedback"></div>
        </div>
    </div>

    <!-- ACTIVITY 4: Answer the survey questions using since or for -->
    <div class="activity-card">
        <div class="activity-title">📌 4. Answer the survey questions (from Activity 3) with <em>since</em> or <em>for</em></div>
        <div class="activity-content">
            <div class="field-row"><span class="field-label">1️⃣ (for)</span> <input type="text" id="ans1" class="field-input" placeholder="I've lived in this town for ..."></div>
            <div class="field-row"><span class="field-label">2️⃣ (since)</span> <input type="text" id="ans2" class="field-input" placeholder="I've been a pupil since ..."></div>
            <div class="field-row"><span class="field-label">3️⃣ (for)</span> <input type="text" id="ans3" class="field-input" placeholder="I've studied English for ..."></div>
            <div class="field-row"><span class="field-label">4️⃣ (since)</span> <input type="text" id="ans4" class="field-input" placeholder="I've had a bicycle since ..."></div>
            <div class="field-row"><span class="field-label">5️⃣ (for)</span> <input type="text" id="ans5" class="field-input" placeholder="I've known my best friend for ..."></div>
            <div class="field-row"><span class="field-label">6️⃣ (since)</span> <input type="text" id="ans6" class="field-input" placeholder="I've liked my favourite writer since ..."></div>
            <div id="answerFeedback" class="feedback"></div>
        </div>
    </div>

    <!-- ACTIVITY 5: Partner answers (write partner's responses) -->
    <div class="activity-card">
        <div class="activity-title">👥 5. Partner interview: Ask questions & write their answers</div>
        <div class="activity-content">
            <div class="field-row"><span class="field-label">Partner 1 (live in town?)</span> <input type="text" id="partner1" class="field-input" placeholder="e.g., She has lived in this town for 4 years."></div>
            <div class="field-row"><span class="field-label">Partner 2 (been a pupil?)</span> <input type="text" id="partner2" class="field-input" placeholder="He has been a pupil since 2019."></div>
            <div class="field-row"><span class="field-label">Partner 3 (study English?)</span> <input type="text" id="partner3" class="field-input" placeholder="They have studied English for 5 years."></div>
            <div class="field-row"><span class="field-label">Partner 4 (have a bicycle?)</span> <input type="text" id="partner4" class="field-input" placeholder="... has had a bicycle since ..."></div>
            <div class="field-row"><span class="field-label">Partner 5 (know best friend?)</span> <input type="text" id="partner5" class="field-input" placeholder="... has known ... for ..."></div>
            <div class="field-row"><span class="field-label">Partner 6 (like favourite writer?)</span> <input type="text" id="partner6" class="field-input" placeholder="... has liked ... since ..."></div>
            <div id="partnerFeedback" class="feedback"></div>
        </div>
    </div>

    <div style="display: flex; justify-content: center; gap: 20px; flex-wrap: wrap;">
        <button class="btn-check" id="checkAllBtn">✅ Auto-Correct & Score</button>
        <button class="btn-check" id="resetBtn" style="background: #5e7c8c;">⟳ Reset all answers</button>
    </div>
    <div id="totalScoreArea" class="score-area">📊 Total score: -- / 24</div>
</div>

<script>
    /* --- GLOBAL SECURITY - STARTS IMMEDIATELY --- */

// Prevents right-click from the first second
document.oncontextmenu = () => { alert("Right-click disabled"); return false; };

// Locks if they even THINK about leaving the tab
document.addEventListener("visibilitychange", () => {
    if (document.hidden) lockPage();
});

// The actual lock function
function lockPage() {
    document.getElementById('lockOverlay').style.display = 'flex';
    document.body.style.filter = "blur(10px)";
    localStorage.setItem('worksheet_status', 'locked');
}
    // ======================= SECURITY & LOCK MECHANISM =======================
    const TEACHER_PASSWORD = "6060";
    let isLocked = false;
    let resultWasClicked = false;
    const lockOverlay = document.getElementById('lockOverlay');
    const passwordInput = document.getElementById('passwordInput');
    const unlockBtn = document.getElementById('unlockBtn');
    const lockErrorMsg = document.getElementById('lockErrorMsg');

    function lockPage(reason = "generic") {
        if (isLocked) return;
        isLocked = true;
        document.body.classList.add('locked');
        lockOverlay.style.display = 'flex';
        localStorage.setItem("worksheet_status", "locked");
        lockErrorMsg.innerText = '';
        passwordInput.value = '';
    }

    function unlockPage() {
        const entered = passwordInput.value.trim();
        if (entered === TEACHER_PASSWORD) {
            isLocked = false;
            document.body.classList.remove('locked');
            lockOverlay.style.display = 'none';
            lockErrorMsg.innerText = '';
            localStorage.removeItem("worksheet_status");
        } else {
            lockErrorMsg.innerText = '❌ Incorrect password. Access denied.';
            passwordInput.value = '';
        }
    }
    unlockBtn.addEventListener('click', unlockPage);
    passwordInput.addEventListener('keypress', (e) => { if (e.key === 'Enter') unlockPage(); });

    function hasAnyAnswers() {
        const allTexts = document.querySelectorAll('input[type="text"], input.fill-input, input.field-input');
        for (let inp of allTexts) if (inp.value.trim() !== "") return true;
        const radios = document.querySelectorAll('input[type="radio"]');
        for (let r of radios) if (r.checked) return true;
        return false;
    }

    let answerFlag = false;
    function updateFlag() { answerFlag = hasAnyAnswers(); }
    document.addEventListener('change', updateFlag);
    document.addEventListener('input', updateFlag);
    updateFlag();

    document.addEventListener('visibilitychange', function() {
        if (document.hidden && !isLocked && answerFlag) lockPage('tab minimize');
    });
    window.addEventListener("blur", function() {
        if (!isLocked && answerFlag) lockPage('window blur');
    });
    window.addEventListener('beforeunload', function(e) {
        if (answerFlag && !isLocked) sessionStorage.setItem('pendingLock', 'true');
    });
    window.addEventListener('load', function() {
        updateFlag();
        if (localStorage.getItem('worksheet_status') === 'locked') lockPage('persisted');
        if (sessionStorage.getItem('pendingLock') === 'true') {
            sessionStorage.removeItem('pendingLock');
            if (!isLocked && answerFlag) lockPage('reload');
        }
    });
    document.addEventListener('contextmenu', e => e.preventDefault());
    document.addEventListener('keydown', function(e) {
        if (e.key === 'F12' || (e.ctrlKey && e.shiftKey && (e.key === 'I' || e.key === 'J')) || (e.ctrlKey && e.key === 'u') || (e.ctrlKey && e.key === 'r')) {
            e.preventDefault();
        }
    });
    // This starts the moment the browser finishes loading the elements
    window.onload = function() {
    
    // 1. Check if they were already locked from a previous visit
    if (localStorage.getItem('worksheet_status') === 'locked') {
        lockPage();
    }

    // 2. Start monitoring tab-switching IMMEDIATELY
    document.addEventListener('visibilitychange', function() {
        // No "if started" check here - if they leave, it locks.
        if (document.hidden) {
            console.log("Security Trigger: Tab Hidden");
            lockPage();
        }
    });

    // 3. Start monitoring window focus IMMEDIATELY
    window.addEventListener("blur", function() {
        console.log("Security Trigger: Window Lost Focus");
        lockPage();
    });
    };

    // ======================= SCORING LOGIC =======================
    // Activity 1 (since/for) correct answers
    const gapAnswers = {
        gap1: "for", gap2: "since", gap3: "since", gap4: "for", gap5: "since", gap6: "for"
    };
    // Activity 2 true/false (standard answers)
    const tfKeys = { tf2: "T", tf3: "T", tf4: "T", tf5: "T" };
    
    // Activity 3 survey questions: check they are valid questions (not empty, contains "how long" and present perfect roughly)
    function validateSurveyQuestion(inputVal) {
        let val = inputVal.trim().toLowerCase();
        if (val === "") return false;
        return (val.includes("how long") && (val.includes("have you") || val.includes("have you lived") || val.includes("have you been") || val.includes("have you studied") || val.includes("have you had") || val.includes("have you known") || val.includes("have you liked")));
    }
    
    // Activity 4 answers: just check that they are not empty and contain since or for appropriately (lenient)
    function checkAnswerWithSinceFor(val, expectedWord) {
        let v = val.trim().toLowerCase();
        if (v === "") return false;
        if (expectedWord === "for") return v.includes("for");
        if (expectedWord === "since") return v.includes("since");
        return false;
    }
    
    // Activity 5 partner answers: at least not empty (any valid present perfect answer)
    function checkPartnerNotEmpty(val) { return val.trim().length > 3; }
    
    function computeAndDisplayScores() {
        let score1 = 0;
        for (let i = 1; i <= 6; i++) {
            let userVal = document.getElementById(`gap${i}`).value.trim().toLowerCase();
            if (userVal === gapAnswers[`gap${i}`]) score1++;
            else if ((gapAnswers[`gap${i}`] === "for" && (userVal === "for" || userVal === "for.")) ||
                (gapAnswers[`gap${i}`] === "since" && (userVal === "since" || userVal === "since."))) score1++;
        }
        let score2 = 0;
        for (let i = 2; i <= 5; i++) {
            let selected = document.querySelector(`input[name="tf${i}"]:checked`);
            if (selected && selected.value === tfKeys[`tf${i}`]) score2++;
        }
        let score3 = 0;
        const surveyInputs = ['surveyQ1','surveyQ2','surveyQ3','surveyQ4','surveyQ5','surveyQ6'];
        for (let id of surveyInputs) {
            let val = document.getElementById(id).value;
            if (validateSurveyQuestion(val)) score3++;
        }
        let score4 = 0;
        const ansExpected = ['for','since','for','since','for','since'];
        for (let i=1; i<=6; i++) {
            let val = document.getElementById(`ans${i}`).value;
            if (checkAnswerWithSinceFor(val, ansExpected[i-1])) score4++;
        }
        let score5 = 0;
        for (let i=1; i<=6; i++) {
            let val = document.getElementById(`partner${i}`).value;
            if (checkPartnerNotEmpty(val)) score5++;
        }
        let total = score1 + score2 + score3 + score4 + score5;
        let maxTotal = 6+4+6+6+6; // 28? Wait recount: act1=6, act2=4, act3=6, act4=6, act5=6 => total = 28. But display 28.
        document.getElementById('gapFeedback').innerHTML = `📖 since/for: ${score1}/6 ✅`;
        document.getElementById('tfFeedback').innerHTML = `🎧 True/False: ${score2}/4 (answers: T, T, T, T)`;
        document.getElementById('surveyQFeedback').innerHTML = `📝 Survey questions (valid format): ${score3}/6`;
        document.getElementById('answerFeedback').innerHTML = `📌 Personal answers with since/for: ${score4}/6 (any sensible answer accepted)`;
        document.getElementById('partnerFeedback').innerHTML = `👥 Partner’s answers (non-empty): ${score5}/6`;
        document.getElementById('totalScoreArea').innerHTML = `📊 Total score: ${total} / 28  (1:${score1} 2:${score2} 3:${score3} 4:${score4} 5:${score5})`;
        return total;
    }
    
    function onResultClick() {
        if (isLocked) return;
        computeAndDisplayScores();
        if (hasAnyAnswers()) {
            //lockPage('Activity completed — locked');
            alert("✅ Activity Completed and Locked. Please ask teacher to unlock with password.");
        }
    }
    
    const checkBtn = document.getElementById('checkAllBtn');
    const newCheckBtn = checkBtn.cloneNode(true);
    checkBtn.parentNode.replaceChild(newCheckBtn, checkBtn);
    newCheckBtn.addEventListener('click', onResultClick);
    
    function resetAllFields() {
        for (let i=1;i<=6;i++) document.getElementById(`gap${i}`).value = '';
        for (let i=2;i<=5;i++) {
            let radios = document.querySelectorAll(`input[name="tf${i}"]`);
            radios.forEach(r => r.checked = false);
        }
        for (let id of surveyInputs) document.getElementById(id).value = '';
        for (let i=1;i<=6;i++) document.getElementById(`ans${i}`).value = '';
        for (let i=1;i<=6;i++) document.getElementById(`partner${i}`).value = '';
        document.getElementById('gapFeedback').innerHTML = '';
        document.getElementById('tfFeedback').innerHTML = '';
        document.getElementById('surveyQFeedback').innerHTML = '';
        document.getElementById('answerFeedback').innerHTML = '';
        document.getElementById('partnerFeedback').innerHTML = '';
        document.getElementById('totalScoreArea').innerHTML = '📊 Total score: -- / 28';
        updateFlag();
        if (isLocked) alert('All answers cleared. Use teacher password to unlock if needed.');
    }
    document.getElementById('resetBtn').addEventListener('click', resetAllFields);
    
    // prefill example for activity 3 question 1 demo
    if(!document.getElementById('surveyQ1').value) document.getElementById('surveyQ1').placeholder = "How long have you lived in this town?";
    updateFlag();
    if (localStorage.getItem('worksheet_status') === 'locked') lockPage('initial');
</script>
</body>
</html>
