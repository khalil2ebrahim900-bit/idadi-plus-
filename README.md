<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>منهجنا | منصتك التعليمية</title>

<style>
*{box-sizing:border-box;margin:0;padding:0}
body{
    font-family:"Tahoma","Arial",sans-serif;
    background:#f5f7fb;
    color:#172033;
}
button,input,select{font-family:inherit}
.hidden{display:none!important}

/* LOGIN */
.login-page{
    min-height:100vh;
    display:flex;
    align-items:center;
    justify-content:center;
    padding:25px;
    background:linear-gradient(135deg,#0f172a,#123b63,#087f8c);
}
.login-box{
    width:100%;
    max-width:460px;
    background:white;
    padding:40px;
    border-radius:28px;
    box-shadow:0 25px 70px #0004;
}
.logo{
    width:70px;
    height:70px;
    background:linear-gradient(135deg,#087f8c,#155eef);
    color:white;
    border-radius:20px;
    display:flex;
    align-items:center;
    justify-content:center;
    font-size:32px;
    margin:auto auto 18px;
}
.login-box h1{text-align:center;font-size:32px}
.login-box p{text-align:center;color:#697386;margin:10px 0 30px}
.field{margin-bottom:18px}
.field label{
    display:block;
    margin-bottom:8px;
    font-weight:bold;
}
.field input,.field select{
    width:100%;
    padding:14px;
    border:1px solid #dce1ea;
    border-radius:13px;
    outline:none;
    font-size:15px;
}
.field input:focus,.field select:focus{
    border-color:#087f8c;
}
.btn{
    border:0;
    padding:13px 20px;
    border-radius:12px;
    cursor:pointer;
    font-weight:bold;
    transition:.2s;
}
.btn:hover{transform:translateY(-2px)}
.primary{
    background:linear-gradient(135deg,#087f8c,#155eef);
    color:white;
}
.full{width:100%}

/* APP */
.app{
    min-height:100vh;
    display:flex;
}
.sidebar{
    width:250px;
    background:#101827;
    color:white;
    padding:22px 15px;
    position:fixed;
    right:0;
    top:0;
    bottom:0;
}
.brand{
    font-size:25px;
    font-weight:bold;
    padding:12px 15px 28px;
}
.brand small{
    display:block;
    color:#8fa2ba;
    font-size:11px;
    margin-top:5px;
}
.nav{
    width:100%;
    border:0;
    background:transparent;
    color:#bdc7d5;
    padding:14px;
    border-radius:12px;
    text-align:right;
    margin:4px 0;
    cursor:pointer;
    font-size:15px;
}
.nav:hover,.nav.active{
    background:#ffffff15;
    color:white;
}
.logout{color:#ff9b9b;margin-top:25px}

.main{
    margin-right:250px;
    width:calc(100% - 250px);
    padding:28px;
}
.topbar{
    display:flex;
    justify-content:space-between;
    align-items:center;
    margin-bottom:25px;
}
.topbar h2{font-size:25px}
.user-mini{
    background:white;
    padding:10px 15px;
    border-radius:14px;
    box-shadow:0 5px 20px #00000009;
}

/* HERO */
.hero{
    background:linear-gradient(135deg,#0f172a,#087f8c,#155eef);
    color:white;
    padding:35px;
    border-radius:25px;
    margin-bottom:25px;
}
.hero h1{font-size:34px;margin-bottom:12px}
.hero p{color:#e2eff5;line-height:1.8}
.hero .btn{
    background:white;
    color:#087f8c;
    margin-top:20px;
}

/* CARDS */
.grid{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:18px;
}
.card{
    background:white;
    padding:24px;
    border-radius:20px;
    box-shadow:0 8px 30px #00000008;
}
.card .icon{
    font-size:28px;
    margin-bottom:12px;
}
.card h3{margin-bottom:8px}
.card p{color:#697386;line-height:1.7}

.section-title{
    margin:28px 0 15px;
}

/* GRADES */
.grades{
    display:grid;
    grid-template-columns:repeat(2,1fr);
    gap:18px;
}
.grade-card{
    background:white;
    padding:25px;
    border-radius:20px;
    border:1px solid #edf0f5;
    cursor:pointer;
    transition:.2s;
}
.grade-card:hover{
    transform:translateY(-4px);
    box-shadow:0 12px 30px #0001;
}
.grade-number{
    width:55px;
    height:55px;
    border-radius:16px;
    display:flex;
    align-items:center;
    justify-content:center;
    background:#e8f7f8;
    color:#087f8c;
    font-weight:bold;
    margin-bottom:15px;
    font-size:20px;
}

/* EXAMS */
.exam-grid{
    display:grid;
    grid-template-columns:repeat(2,1fr);
    gap:20px;
}
.exam-card{
    color:white;
    padding:30px;
    border-radius:24px;
}
.easy{background:linear-gradient(135deg,#087f8c,#16a085)}
.hard{background:linear-gradient(135deg,#9b2335,#e74c3c)}
.exam-card p{margin:12px 0 20px;color:#fff9;line-height:1.7}
.exam-card .btn{
    background:white;
    color:#172033;
}

/* QUIZ */
.quiz-box{
    max-width:800px;
    margin:auto;
    background:white;
    padding:30px;
    border-radius:24px;
}
.progress{
    height:8px;
    background:#edf0f5;
    border-radius:10px;
    overflow:hidden;
    margin:15px 0 25px;
}
.progress div{
    height:100%;
    background:#087f8c;
    width:0%;
}
.question{
    font-size:22px;
    font-weight:bold;
    line-height:1.6;
    margin-bottom:25px;
}
.answers{
    display:grid;
    gap:12px;
}
.answer{
    padding:16px;
    border:2px solid #e4e8ef;
    background:white;
    border-radius:13px;
    cursor:pointer;
    text-align:right;
}
.answer:hover{
    border-color:#087f8c;
    background:#f3fbfb;
}
.answer.correct{
    background:#dff7e8;
    border-color:#21a35a;
}
.answer.wrong{
    background:#ffe4e4;
    border-color:#e04747;
}
.result{
    text-align:center;
    padding:30px;
}
.score{
    font-size:50px;
    font-weight:bold;
    color:#087f8c;
    margin:15px;
}

/* AI */
.ai-box{
    background:white;
    border-radius:24px;
    overflow:hidden;
    box-shadow:0 8px 30px #00000008;
}
.ai-head{
    padding:20px;
    background:#101827;
    color:white;
}
.chat{
    height:420px;
    overflow:auto;
    padding:20px;
}
.message{
    padding:13px 16px;
    border-radius:15px;
    margin-bottom:12px;
    max-width:80%;
    line-height:1.7;
}
.bot{
    background:#eef7f8;
    margin-left:auto;
}
.me{
    background:#155eef;
    color:white;
    margin-right:auto;
}
.ai-input{
    display:flex;
    gap:10px;
    padding:15px;
    border-top:1px solid #eee;
}
.ai-input input{
    flex:1;
    padding:14px;
    border:1px solid #ddd;
    border-radius:12px;
}

/* PROFILE */
.profile-box{
    max-width:600px;
    background:white;
    padding:28px;
    border-radius:22px;
}
.info{
    display:flex;
    justify-content:space-between;
    padding:16px 0;
    border-bottom:1px solid #eee;
}
.info:last-child{border:0}

/* MOBILE */
@media(max-width:850px){
    .sidebar{
        width:75px;
        padding:15px 8px;
    }
    .brand{
        text-align:center;
        font-size:18px;
    }
    .brand small,.nav span{display:none}
    .nav{text-align:center;font-size:22px}
    .main{
        margin-right:75px;
        width:calc(100% - 75px);
        padding:18px;
    }
    .grid,.grades,.exam-grid{
        grid-template-columns:1fr;
    }
    .hero h1{font-size:27px}
}
</style>
</head>

<body>

<!-- LOGIN -->
<div id="loginPage" class="login-page">
    <div class="login-box">
        <div class="logo">م</div>
        <h1>منهجنا</h1>
        <p>منصتك التعليمية لطلبة البحرين</p>

        <div class="field">
            <label>اسم الطالب</label>
            <input id="studentName" placeholder="اكتب اسمك">
        </div>

        <div class="field">
            <label>الجنس</label>
            <select id="gender">
                <option value="">اختر</option>
                <option>ذكر</option>
                <option>أنثى</option>
            </select>
        </div>

        <div class="field">
            <label>الصف</label>
            <select id="grade">
                <option value="">اختر صفك</option>
                <option value="6">الصف السادس</option>
                <option value="7">الأول الإعدادي</option>
                <option value="8">الثاني الإعدادي</option>
                <option value="9">الثالث الإعدادي</option>
            </select>
        </div>

        <button class="btn primary full" onclick="login()">
            دخول إلى منهجنا
        </button>
    </div>
</div>

<!-- APP -->
<div id="app" class="app hidden">

<aside class="sidebar">
    <div class="brand">
        📚 منهجنا
        <small>تعلم • اختبر • تطور</small>
    </div>

    <button class="nav active" onclick="page('home',this)">
        🏠 <span>الرئيسية</span>
    </button>

    <button class="nav" onclick="page('grades',this)">
        🎓 <span>الصفوف</span>
    </button>

    <button class="nav" onclick="page('exams',this)">
        📝 <span>الاختبارات</span>
    </button>

    <button class="nav" onclick="page('ai',this)">
        🤖 <span>مساعد AI</span>
    </button>

    <button class="nav" onclick="page('profile',this)">
        👤 <span>حسابي</span>
    </button>

    <button class="nav logout" onclick="logout()">
        🚪 <span>تسجيل الخروج</span>
    </button>
</aside>

<main class="main">

<div class="topbar">
    <h2 id="pageTitle">الرئيسية</h2>
    <div class="user-mini" id="miniUser">طالب</div>
</div>

<!-- HOME -->
<section id="homePage">
    <div class="hero">
        <h1>هلا والله 👋</h1>
        <p>
            حياك في <b>منهجنا</b>، منصتك التعليمية لطلبة
            الصف السادس والمرحلة الإعدادية في البحرين.
        </p>
        <button class="btn" onclick="page('exams')">
            ابدأ اختبارك الآن
        </button>
    </div>

    <div class="grid">
        <div class="card">
            <div class="icon">🎓</div>
            <h3>صفوف متعددة</h3>
            <p>السادس والأول والثاني والثالث الإعدادي.</p>
        </div>

        <div class="card">
            <div class="icon">📝</div>
            <h3>اختبارات</h3>
            <p>اختبارات سهلة وصعبة مع حساب نتيجتك.</p>
        </div>

        <div class="card">
            <div class="icon">🤖</div>
            <h3>مساعد AI</h3>
            <p>مكان مخصص لمساعدتك في فهم دروسك.</p>
        </div>
    </div>
</section>

<!-- GRADES -->
<section id="gradesPage" class="hidden">
    <h3 class="section-title">اختر صفك</h3>

    <div class="grades">

        <div class="grade-card" onclick="selectGrade(6)">
            <div class="grade-number">٦</div>
            <h3>الصف السادس</h3>
            <p>المرحلة الابتدائية — التعليم الأساسي.</p>
        </div>

        <div class="grade-card" onclick="selectGrade(7)">
            <div class="grade-number">٧</div>
            <h3>الأول الإعدادي</h3>
            <p>السنة الأولى من المرحلة الإعدادية.</p>
        </div>

        <div class="grade-card" onclick="selectGrade(8)">
            <div class="grade-number">٨</div>
            <h3>الثاني الإعدادي</h3>
            <p>السنة الثانية من المرحلة الإعدادية.</p>
        </div>

        <div class="grade-card" onclick="selectGrade(9)">
            <div class="grade-number">٩</div>
            <h3>الثالث الإعدادي</h3>
            <p>السنة الثالثة من المرحلة الإعدادية.</p>
        </div>

    </div>
</section>

<!-- EXAMS -->
<section id="examsPage" class="hidden">

    <div class="hero">
        <h1>اختبر نفسك 📝</h1>
        <p>
            اختر مستوى الاختبار المناسب لك.
            يتم حساب النتيجة بعد الانتهاء.
        </p>
    </div>

    <div class="exam-grid">

        <div class="exam-card easy">
            <h2>🟢 اختبار سهل</h2>
            <p>
                10 أسئلة تدريبية مناسبة للمراجعة
                وتثبيت المعلومات.
            </p>
            <button class="btn" onclick="startQuiz('easy')">
                ابدأ الاختبار
            </button>
        </div>

        <div class="exam-card hard">
            <h2>🔴 اختبار صعب</h2>
            <p>
                15 سؤالًا بمستوى أعلى لتحدي نفسك.
            </p>
            <button class="btn" onclick="startQuiz('hard')">
                ابدأ الاختبار
            </button>
        </div>

    </div>
</section>

<!-- QUIZ -->
<section id="quizPage" class="hidden">

    <div class="quiz-box">

        <div id="quizTop"></div>

        <div class="progress">
            <div id="progressBar"></div>
        </div>

        <div id="questionArea"></div>

    </div>

</section>

<!-- AI -->
<section id="aiPage" class="hidden">

    <div class="ai-box">

        <div class="ai-head">
            <h2>🤖 مساعد منهجنا AI</h2>
            <p>اسأل عن دروسك وساعد نفسك على الفهم.</p>
        </div>

        <div class="chat" id="chat">

            <div class="message bot">
                هلا! 👋 أنا مساعد منهجنا.
                اكتب سؤالك الدراسي هنا.
            </div>

        </div>

        <div class="ai-input">
            <input id="aiInput"
                   placeholder="اكتب سؤالك هنا..."
                   onkeydown="if(event.key==='Enter')askAI()">

            <button class="btn primary" onclick="askAI()">
                إرسال
            </button>
        </div>

    </div>

</section>

<!-- PROFILE -->
<section id="profilePage" class="hidden">

    <div class="profile-box">

        <h2>👤 حسابي</h2>

        <div class="info">
            <span>الاسم</span>
            <b id="profileName">-</b>
        </div>

        <div class="info">
            <span>الجنس</span>
            <b id="profileGender">-</b>
        </div>

        <div class="info">
            <span>الصف</span>
            <b id="profileGrade">-</b>
        </div>

    </div>

</section>

</main>
</div>

<script>

/* =========================
   DATA
========================= */

const gradeNames = {
    6:"الصف السادس",
    7:"الأول الإعدادي",
    8:"الثاني الإعدادي",
    9:"الثالث الإعدادي"
};

/*
   بنك أسئلة أولي.
   يمكن استبداله لاحقًا ببنك أسئلة
   مطابق لكل خطة دراسية رسمية.
*/

const questions = {

6:{
easy:[
{
q:"ما ناتج 5 × 6؟",
a:["20","25","30","35"],
c:2
},
{
q:"ما ناتج 100 ÷ 4؟",
a:["20","25","30","40"],
c:1
},
{
q:"أي كلمة اسم إشارة؟",
a:["هذا","كتب","طالب","مدرسة"],
c:0
},
{
q:"ما جمع كلمة «كتاب»؟",
a:["كاتب","كتب","مكتوب","كتابة"],
c:1
},
{
q:"أي مما يأتي كوكب؟",
a:["القمر","الشمس","الأرض","المجرة"],
c:2
},
{
q:"ما وحدة قياس الطول؟",
a:["اللتر","المتر","الكيلوغرام","الثانية"],
c:1
},
{
q:"ما عكس كلمة Big؟",
a:["Small","Fast","Tall","Long"],
c:0
},
{
q:"ما ناتج 12 + 18؟",
a:["20","25","30","35"],
c:2
},
{
q:"أي مما يأتي مصدر طبيعي للماء؟",
a:["البحر","الكتاب","السيارة","المبنى"],
c:0
},
{
q:"كم عدد أيام الأسبوع؟",
a:["5","6","7","8"],
c:2
}
],

hard:[
{
q:"إذا كان س = 8، فما قيمة 3س + 4؟",
a:["20","24","28","32"],
c:2
},
{
q:"ما العدد الأولي؟",
a:["21","27","29","33"],
c:2
},
{
q:"ما الكسر المكافئ لـ 1/2؟",
a:["2/3","2/4","3/5","4/6"],
c:1
},
{
q:"إذا كان محيط مربع 20 سم، فما طول ضلعه؟",
a:["4 سم","5 سم","6 سم","10 سم"],
c:1
},
{
q:"أي عملية تحدث للنبات لصنع غذائه؟",
a:["التنفس","البناء الضوئي","الهضم","التبخر"],
c:1
}
]
},

7:{
easy:[
{
q:"ما ناتج 7 × 8؟",
a:["48","54","56","64"],
c:2
},
{
q:"أي مما يأتي اسم؟",
a:["ذهب","مدرسة","يكتب","اقرأ"],
c:1
},
{
q:"ما ناتج 45 ÷ 5؟",
a:["7","8","9","10"],
c:2
},
{
q:"أي عدد يقبل القسمة على 2؟",
a:["15","21","34","45"],
c:2
},
{
q:"ما ضد كلمة «قديم»؟",
a:["صغير","جديد","بعيد","قصير"],
c:1
},
{
q:"ما الكوكب الذي نعيش عليه؟",
a:["المريخ","الأرض","الزهرة","المشتري"],
c:1
},
{
q:"ما وحدة قياس الكتلة؟",
a:["المتر","الثانية","الكيلوغرام","اللتر"],
c:2
},
{
q:"ما ناتج 15 + 27؟",
a:["32","40","42","52"],
c:2
},
{
q:"أي مما يأتي من مصادر الطاقة؟",
a:["الشمس","الكتاب","الطاولة","القلم"],
c:0
},
{
q:"كم ضلعًا للمثلث؟",
a:["2","3","4","5"],
c:1
}
],

hard:[
{
q:"ما قيمة 4²؟",
a:["6","8","12","16"],
c:3
},
{
q:"إذا كان س + 7 = 15، فما قيمة س؟",
a:["6","7","8","9"],
c:2
},
{
q:"أي كسر أكبر؟",
a:["1/4","1/2","1/8","1/10"],
c:1
},
{
q:"محيط مستطيل طوله 8 سم وعرضه 3 سم يساوي؟",
a:["11","16","22","24"],
c:2
},
{
q:"ما العملية التي تحول الماء السائل إلى بخار؟",
a:["التجمد","التبخر","التكاثف","الانصهار"],
c:1
}
]
},

8:{
easy:[
{
q:"ما ناتج 9 × 7؟",
a:["54","63","72","81"],
c:1
},
{
q:"أي عدد من الآتي عدد صحيح؟",
a:["-3","1/2","0.5","3/4"],
c:0
},
{
q:"ما ناتج 81 ÷ 9؟",
a:["7","8","9","10"],
c:2
},
{
q:"ما مفرد كلمة «طلاب»؟",
a:["طالب","طلب","طلاب","طالبة"],
c:0
},
{
q:"أي عضو مسؤول عن ضخ الدم؟",
a:["الرئة","القلب","المعدة","الكبد"],
c:1
},
{
q:"ما مصدر الضوء الطبيعي؟",
a:["الشمس","المصباح","الهاتف","الشاشة"],
c:0
},
{
q:"ما محيط مربع طول ضلعه 4 سم؟",
a:["8","12","16","20"],
c:2
},
{
q:"أي مما يأتي فعل؟",
a:["مدرسة","كتاب","يكتب","قلم"],
c:2
},
{
q:"ما ناتج 100 - 37؟",
a:["53","63","73","83"],
c:1
},
{
q:"ما وحدة قياس الزمن؟",
a:["المتر","الثانية","الكيلوغرام","اللتر"],
c:1
}
],

hard:[
{
q:"حل: 2س + 4 = 14",
a:["3","4","5","6"],
c:2
},
{
q:"ما قيمة 3³؟",
a:["9","18","27","36"],
c:2
},
{
q:"إذا كان نصف العدد 12، فما العدد؟",
a:["6","18","24","36"],
c:2
},
{
q:"مساحة مستطيل طوله 10 وعرضه 4 تساوي؟",
a:["14","28","40","80"],
c:2
},
{
q:"ما الغاز الذي تحتاجه النباتات في البناء الضوئي؟",
a:["الأكسجين","ثاني أكسيد الكربون","النيتروجين","الهيدروجين"],
c:1
}
]
},

9:{
easy:[
{
q:"ما ناتج 12 × 6؟",
a:["62","72","82","92"],
c:1
},
{
q:"ما قيمة √49؟",
a:["5","6","7","8"],
c:2
},
{
q:"إذا كان س = 5، فما قيمة 2س؟",
a:["5","7","10","15"],
c:2
},
{
q:"أي مما يأتي عدد أولي؟",
a:["21","25","31","35"],
c:2
},
{
q:"ما مفرد كلمة «مدارس»؟",
a:["مدرس","مدرسة","درس","دارس"],
c:1
},
{
q:"ما العضو المسؤول عن التنفس؟",
a:["القلب","الرئة","المعدة","الكبد"],
c:1
},
{
q:"ما مساحة مربع طول ضلعه 5؟",
a:["10","20","25","30"],
c:2
},
{
q:"ما ناتج 144 ÷ 12؟",
a:["10","11","12","13"],
c:2
},
{
q:"أي مما يأتي تغير كيميائي؟",
a:["انصهار الثلج","احتراق الورق","قطع الورق","تبخر الماء"],
c:1
},
{
q:"ما عكس كلمة «نجاح»؟",
a:["تفوق","فشل","اجتهاد","تقدم"],
c:1
}
],

hard:[
{
q:"حل: 3س - 5 = 16",
a:["5","6","7","8"],
c:2
},
{
q:"ما قيمة 2⁵؟",
a:["10","16","32","64"],
c:2
},
{
q:"إذا كان محيط دائرة يعتمد على نصف القطر، فماذا يحدث للمحيط عند زيادة نصف القطر؟",
a:["يزداد","ينقص","لا يتغير","يصبح صفرًا"],
c:0
},
{
q:"ما ناتج (8 × 3) + 12 ÷ 4؟",
a:["24","25","27","30"],
c:2
},
{
q:"أي جهاز في الجسم مسؤول بشكل أساسي عن نقل الدم؟",
a:["الجهاز الدوري","الجهاز الهضمي","الجهاز التنفسي","الجهاز العصبي"],
c:0
}
]
}

};

/* =========================
   LOGIN
========================= */

function login(){

    const name=document.getElementById("studentName").value.trim();
    const gender=document.getElementById("gender").value;
    const grade=document.getElementById("grade").value;

    if(!name || !gender || !grade){
        alert("يرجى تعبئة جميع البيانات.");
        return;
    }

    const user={name,gender,grade};

    localStorage.setItem("manhajnaUser",JSON.stringify(user));

    showApp(user);
}

function showApp(user){

    document.getElementById("loginPage").classList.add("hidden");
    document.getElementById("app").classList.remove("hidden");

    document.getElementById("miniUser").textContent =
        user.name + " • " + gradeNames[user.grade];

    document.getElementById("profileName").textContent=user.name;
    document.getElementById("profileGender").textContent=user.gender;
    document.getElementById("profileGrade").textContent=gradeNames[user.grade];
}

function logout(){

    localStorage.removeItem("manhajnaUser");

    document.getElementById("app").classList.add("hidden");
    document.getElementById("loginPage").classList.remove("hidden");
}

/* =========================
   NAVIGATION
========================= */

function page(name,button){

    const pages=[
        "home",
        "grades",
        "exams",
        "quiz",
        "ai",
        "profile"
    ];

    pages.forEach(p=>{
        document.getElementById(p+"Page").classList.add("hidden");
    });

    document.getElementById(name+"Page").classList.remove("hidden");

    if(button){
        document.querySelectorAll(".nav")
            .forEach(x=>x.classList.remove("active"));

        button.classList.add("active");
    }

    const titles={
        home:"الرئيسية",
        grades:"الصفوف",
        exams:"الاختبارات",
        quiz:"الاختبار",
        ai:"مساعد AI",
        profile:"حسابي"
    };

    document.getElementById("pageTitle").textContent=titles[name];
}

function selectGrade(g){

    localStorage.setItem("selectedGrade",g);

    alert(
        "تم اختيار " +
        gradeNames[g] +
        " 🎓\nيمكنك الآن الدخول إلى الاختبارات."
    );

    page("exams");
}

/* =========================
   QUIZ
========================= */

let quizQuestions=[];
let quizIndex=0;
let quizScore=0;

function startQuiz(level){

    const user=JSON.parse(localStorage.getItem("manhajnaUser"));

    const grade=user ? user.grade : "6";

    let easy=questions[grade].easy;
    let hard=questions[grade].hard;

    if(level==="easy"){
        quizQuestions=easy;
    }else{

        /*
          الاختبار الصعب = 10 أسئلة سهلة
          + 5 أسئلة صعبة
          ليصبح المجموع 15.
        */

        quizQuestions=[
            ...easy,
            ...hard
        ];
    }

    quizIndex=0;
    quizScore=0;

    page("quiz");

    showQuestion();
}

function showQuestion(){

    const q=quizQuestions[quizIndex];

    document.getElementById("quizTop").innerHTML=`
        <b>السؤال ${quizIndex+1} من ${quizQuestions.length}</b>
    `;

    document.getElementById("progressBar").style.width=
        ((quizIndex)/quizQuestions.length*100)+"%";

    let html=`
        <div class="question">${q.q}</div>
        <div class="answers">
    `;

    q.a.forEach((answer,i)=>{

        html+=`
            <button class="answer"
                    onclick="answer(${i})">
                ${answer}
            </button>
        `;

    });

    html+=`</div>`;

    document.getElementById("questionArea").innerHTML=html;
}

function answer(index){

    const q=quizQuestions[quizIndex];

    const buttons=document.querySelectorAll(".answer");

    buttons.forEach((b,i)=>{
        b.disabled=true;

        if(i===q.c)
            b.classList.add("correct");

        if(i===index && i!==q.c)
            b.classList.add("wrong");
    });

    if(index===q.c)
        quizScore++;

    setTimeout(()=>{

        quizIndex++;

        if(quizIndex<quizQuestions.length){
            showQuestion();
        }else{
            finishQuiz();
        }

    },650);
}

function finishQuiz(){

    document.getElementById("progressBar").style.width="100%";

    const total=quizQuestions.length;
    const percentage=Math.round((quizScore/total)*100);

    document.getElementById("quizTop").innerHTML="النتيجة النهائية";

    document.getElementById("questionArea").innerHTML=`
        <div class="result">

            <h2>🎉 انتهى الاختبار!</h2>

            <div class="score">
                ${quizScore}/${total}
            </div>

            <p>
                نتيجتك:
                <b>${percentage}%</b>
            </p>

            <br>

            <button class="btn primary"
                    onclick="page('exams')">
                العودة للاختبارات
            </button>

        </div>
    `;
}

/* =========================
   AI PLACEHOLDER
========================= */

function askAI(){

    const input=document.getElementById("aiInput");
    const chat=document.getElementById("chat");

    const text=input.value.trim();

    if(!text)return;

    chat.innerHTML+=`
        <div class="message me">
            ${escapeHTML(text)}
        </div>
    `;

    input.value="";

    setTimeout(()=>{

        chat.innerHTML+=`
            <div class="message bot">
                وصلتني سؤالك 👍
                <br>
                حاليًا هذه نسخة تجريبية من مساعد AI.
                عند ربط واجهة AI حقيقية، أقدر أخلي المساعد
                يشرح الدرس ويحل الأسئلة خطوة بخطوة.
            </div>
        `;

        chat.scrollTop=chat.scrollHeight;

    },500);
}

function escapeHTML(text){

    return text
        .replaceAll("&","&amp;")
        .replaceAll("<","&lt;")
        .replaceAll(">","&gt;")
        .replaceAll('"',"&quot;")
        .replaceAll("'","&#039;");
}

/* =========================
   START
========================= */

const saved=localStorage.getItem("manhajnaUser");

if(saved){

    showApp(JSON.parse(saved));

}else{

    document.getElementById("loginPage").classList.remove("hidden");

}

</script>

</body>
</html>
