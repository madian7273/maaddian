<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>بوابة طلبات الزواج الرسمية - الداعية مدين</title>
    <link href="https://googleapis.com" rel="stylesheet">
    <style>
        :root {
            --gold: #c5a059;
            --gold-light: #f4ecd8;
            --dark-gold: #8a6d3b;
            --bg-color: #fdfbf7;
        }

        body {
            font-family: 'Noto Kufi Arabic', sans-serif;
            background-color: var(--bg-color);
            margin: 0;
            padding: 20px;
            color: #333;
        }

        .main-container {
            max-width: 700px;
            margin: 40px auto;
            background: #ffffff;
            border-radius: 35px;
            box-shadow: 0 40px 100px rgba(0,0,0,0.08);
            border: 1px solid rgba(197, 160, 89, 0.2);
            overflow: hidden;
        }

        .header-bg {
            background: linear-gradient(135deg, #fffcf5 0%, #f7f1e3 100%);
            padding: 60px 20px 40px;
            text-align: center;
            border-bottom: 1px solid #eee;
        }

        .profile-frame {
            width: 210px;
            height: 210px;
            margin: 0 auto 25px;
            border-radius: 50%;
            padding: 10px;
            background: linear-gradient(45deg, #BF953F, #FCF6BA, #B38728);
            box-shadow: 0 15px 35px rgba(184, 150, 45, 0.2);
        }

        .profile-frame img {
            width: 100%;
            height: 100%;
            border-radius: 50%;
            object-fit: cover;
            border: 5px solid white;
        }

        h1 { font-family: 'Amiri', serif; color: var(--dark-gold); font-size: 3rem; margin: 0; }
        .tagline { color: #999; font-size: 1.1rem; letter-spacing: 1px; }

        .content-body { padding: 40px; }

        /* قسم الشروط المفصلة */
        .shuroot-section {
            background: var(--gold-light);
            border-radius: 20px;
            padding: 25px;
            margin-bottom: 40px;
        }

        .shuroot-section h3 {
            color: var(--dark-gold);
            margin-top: 0;
            border-bottom: 2px solid var(--gold);
            display: inline-block;
            padding-bottom: 5px;
            margin-bottom: 15px;
        }

        .shuroot-list {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 10px;
            list-style: none;
            padding: 0;
            margin: 0;
        }

        .shuroot-list li {
            font-size: 0.9rem;
            color: #5d502f;
            display: flex;
            align-items: center;
        }

        .shuroot-list li::before {
            content: "✦";
            margin-left: 8px;
            color: var(--gold);
        }

        .form-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
        }

        .full-width { grid-column: span 2; }

        .input-box { text-align: right; }
        label { display: block; margin-bottom: 10px; font-weight: 600; color: #555; font-size: 0.85rem; }

        input, select, textarea {
            width: 100%;
            padding: 15px;
            border: 1px solid #e0e0e0;
            border-radius: 12px;
            background: #fcfcfc;
            font-family: 'Noto Kufi Arabic';
            font-size: 1rem;
            box-sizing: border-box;
            transition: 0.3s;
        }

        input:focus, textarea:focus {
            border-color: var(--gold);
            background: #fff;
            outline: none;
            box-shadow: 0 0 10px rgba(197, 160, 89, 0.1);
        }

        .btn-submit {
            width: 100%;
            padding: 22px;
            background: linear-gradient(45deg, #AA771C, #D4AF37);
            border: none;
            border-radius: 15px;
            color: white;
            font-weight: 800;
            font-size: 1.4rem;
            cursor: pointer;
            margin-top: 30px;
            box-shadow: 0 10px 30px rgba(170, 119, 28, 0.3);
            transition: 0.3s;
        }

        .btn-submit:hover { transform: translateY(-3px); box-shadow: 0 15px 40px rgba(170, 119, 28, 0.4); }

        #result-display {
            margin-top: 35px;
            padding: 30px;
            border-radius: 20px;
            text-align: center;
            display: none;
            font-size: 1.6rem;
            font-weight: 800;
        }

        .eligible-res { background: #f0fff4; color: #166534; border: 2px solid #166534; }
        .rejected-res { background: #fff5f5; color: #991b1b; border: 2px solid #991b1b; }

    </style>
</head>
<body>

<div class="main-container">
    <!-- الهيدر والصورة -->
    <div class="header-bg">
        <div class="profile-frame">
            <img src="madin.jpg.jpeg" id="avatar" alt="الداعية مدين" 
                 onerror="this.src='madin.jpg'; this.onerror=function(){this.src='madin.png'}">
        </div>
        <h1>الداعية مدين</h1>
        <p class="tagline">طلب الارتباط الشرعي</p>
    </div>

    <div class="content-body">
        <!-- قسم الشروط المفصل -->
        <div class="shuroot-section">
            <h3>📜 الشروط المطلوبة:</h3>
            <ul class="shuroot-list">
                <li>أن تكون عذراء</li>
                <li>الطول 170 سم فأكثر</li>
                <li>البشرة بيضاء أو حنطية</li>
                <li>الوزن 50 كجم أو أقل</li>
                <li>العمر بين 21 و 25 سنة</li>
                <li>السيرة الطيبة والصلاح</li>
            </ul>
        </div>

        <!-- الاستمارة -->
        <div class="form-grid">
            <div class="input-box full-width">
                <label>الاسم الكامل (الثلاثي)</label>
                <input type="text" id="fname" placeholder="أدخلي اسمك الكامل">
            </div>

            <div class="input-box">
                <label>العمر الحالي</label>
                <input type="number" id="fage" placeholder="مثال: 23">
            </div>

            <div class="input-box">
                <label>لون البشرة</label>
                <select id="fskin">
                    <option value="p">بيضاء</option>
                    <option value="p">حنطية</option>
                    <option value="f">سمراء</option>
                </select>
            </div>

            <div class="input-box">
                <label>الطول (سم)</label>
                <input type="number" id="fheight" placeholder="مثال: 172">
            </div>

            <div class="input-box">
                <label>الوزن الحالي (كجم)</label>
                <input type="number" id="fweight" placeholder="مثال: 48">
            </div>

            <div class="input-box">
                <label>الجنسية</label>
                <input type="text" id="fnation" placeholder="أدخلي جنسيتك">
            </div>

            <div class="input-box">
                <label>هل أنتِ عذراء؟</label>
                <select id="fvirgin">
                    <option value="p">نعم، عذراء</option>
                    <option value="f">غير ذلك</option>
                </select>
            </div>

            <div class="input-box full-width">
                <label>الوظيفة</label>
                <input type="text" id="fjob" placeholder="اذكري وظيفتك إن وجدت">
            </div>

            <div class="input-box full-width">
                <label>حجم الثروة والممتلكات</label>
                <textarea id="fwealth" rows="3" placeholder="يرجى ذكر العقارات، الأرصدة، أو أي ممتلكات شخصية بالتفصيل"></textarea>
            </div>
        </div>

        <button class="btn-submit" onclick="submitApp()">تقديم الطلب للمراجعة</button>

        <!-- صندوق النتيجة -->
        <div id="result-display"></div>
    </div>
</div>

<script>
    function submitApp() {
        const name = document.getElementById('fname').value;
        const age = parseInt(document.getElementById('fage').value);
        const height = parseInt(document.getElementById('fheight').value);
        const weight = parseInt(document.getElementById('fweight').value);
        const skin = document.getElementById('fskin').value;
        const virgin = document.getElementById('fvirgin').value;
        const result = document.getElementById('result-display');

        if(!name || isNaN(age)) {
            alert("يرجى تعبئة كافة البيانات الأساسية");
            return;
        }

        // فحص الشروط برمجياً
        let isPass = (age >= 21 && age <= 25) && (height >= 170) && (weight <= 50) && (skin === 'p') && (virgin === 'p');

        result.style.display = "block";
        if(isPass) {
            result.className = "eligible-res";
            result.innerHTML = `مؤهلة للزواج ✅<br><span style='font-size: 1rem; font-weight: 400;'>تم قبول طلبك المبدئي يا ${name}. سيتم التواصل معك عبر القنوات الرسمية.</span>`;
        } else {
            result.className = "rejected-res";
            result.innerHTML = `مرفوضة للزواج ❌<br><span style='font-size: 1rem; font-weight: 400;'>نعتذر منك يا ${name}، الشروط الحالية لا تتوافق مع ملفك الشخصي.</span>`;
        }
        
        result.scrollIntoView({ behavior: 'smooth' });
    }
</script>

</body>
</html>
