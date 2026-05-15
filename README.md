<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>قاعة ملاك للحفلات</title>

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:Tahoma;
}

body{
background:#111;
color:white;
overflow-x:hidden;
}

/* خلفية */
.hero{
height:100vh;
background:
linear-gradient(rgba(0,0,0,0.65),rgba(0,0,0,0.65)),
url('https://images.unsplash.com/photo-1519741497674-611481863552?q=80&w=1600&auto=format&fit=crop');
background-size:cover;
background-position:center;
display:flex;
justify-content:center;
align-items:center;
text-align:center;
padding:20px;
}

.hero-content h1{
font-size:55px;
color:#ffd700;
margin-bottom:15px;
}

.hero-content p{
font-size:22px;
line-height:1.8;
color:#eee;
}

/* الحاوية */
.container{
max-width:1100px;
margin:auto;
padding:40px 20px;
}

/* البطاقات */
.cards{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
gap:20px;
margin-top:-80px;
position:relative;
z-index:2;
}

.card{
background:#1b1b1b;
padding:25px;
border-radius:20px;
text-align:center;
box-shadow:0 0 20px rgba(255,215,0,0.15);
border:1px solid rgba(255,215,0,0.2);
}

.card h2{
color:#ffd700;
font-size:35px;
margin-bottom:10px;
}

.card p{
font-size:18px;
}

/* الفورم */
.booking{
margin-top:60px;
background:#1a1a1a;
padding:30px;
border-radius:25px;
box-shadow:0 0 20px rgba(255,215,0,0.1);
}

.booking h2{
text-align:center;
margin-bottom:30px;
color:#ffd700;
font-size:38px;
}

label{
display:block;
margin-bottom:8px;
margin-top:18px;
font-size:17px;
}

input,select{
width:100%;
padding:15px;
border:none;
border-radius:12px;
background:#2a2a2a;
color:white;
font-size:16px;
outline:none;
}

button{
width:100%;
margin-top:30px;
padding:16px;
border:none;
border-radius:14px;
background:#ffd700;
color:black;
font-size:20px;
font-weight:bold;
cursor:pointer;
transition:0.3s;
}

button:hover{
background:white;
transform:scale(1.02);
}

/* معرض الصور */
.gallery{
margin-top:70px;
display:grid;
grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
gap:20px;
}

.gallery img{
width:100%;
height:250px;
object-fit:cover;
border-radius:20px;
box-shadow:0 0 15px rgba(255,215,0,0.15);
}

/* الفوتر */
footer{
margin-top:70px;
padding:25px;
text-align:center;
background:#0a0a0a;
color:#aaa;
font-size:16px;
}

.counter{
color:#ffd700;
font-weight:bold;
}

</style>
</head>

<body>

<!-- الواجهة -->
<section class="hero">
<div class="hero-content">
<h1>قاعة ملاك للحفلات</h1>
<p>
أفخم قاعة أعراس وتنظيم حفلات في الجزائر<br>
احجز موعدك الآن واستمتع بليلة زفاف ملكية
</p>
</div>
</section>

<!-- الإحصائيات -->
<div class="container">

<div class="cards">

<div class="card">
<h2 id="visitors">1542</h2>
<p>زائر للموقع</p>
</div>

<div class="card">
<h2 id="bookings">327</h2>
<p>عدد الحجوزات</p>
</div>

<div class="card">
<h2>24/7</h2>
<p>خدمة الزبائن</p>
</div>

</div>

<!-- نموذج الحجز -->
<div class="booking">

<h2>حجز موعد عرس</h2>

<form id="bookingForm">

<label>الاسم الكامل</label>
<input type="text" id="name" placeholder="أدخل اسمك الكامل" required>

<label>رقم الهاتف</label>
<input type="tel" id="phone" placeholder="أدخل رقم الهاتف" required>

<label>تاريخ الموعد</label>
<input type="date" id="date" required>

<label>الولاية</label>
<select id="wilaya" required>

<option value="">اختر الولاية</option>

<option>أدرار</option>
<option>الشلف</option>
<option>الأغواط</option>
<option>أم البواقي</option>
<option>باتنة</option>
<option>بجاية</option>
<option>بسكرة</option>
<option>بشار</option>
<option>البليدة</option>
<option>البويرة</option>
<option>تمنراست</option>
<option>تبسة</option>
<option>تلمسان</option>
<option>تيارت</option>
<option>تيزي وزو</option>
<option>الجزائر</option>
<option>الجلفة</option>
<option>جيجل</option>
<option>سطيف</option>
<option>سعيدة</option>
<option>سكيكدة</option>
<option>سيدي بلعباس</option>
<option>عنابة</option>
<option>قالمة</option>
<option>قسنطينة</option>
<option>المدية</option>
<option>مستغانم</option>
<option>المسيلة</option>
<option>معسكر</option>
<option>ورقلة</option>
<option>وهران</option>
<option>البيض</option>
<option>إليزي</option>
<option>برج بوعريريج</option>
<option>بومرداس</option>
<option>الطارف</option>
<option>تندوف</option>
<option>تيسمسيلت</option>
<option>الوادي</option>
<option>خنشلة</option>
<option>سوق أهراس</option>
<option>تيبازة</option>
<option>ميلة</option>
<option>عين الدفلى</option>
<option>النعامة</option>
<option>عين تموشنت</option>
<option>غرداية</option>
<option>غليزان</option>

</select>

<label>عدد الأشخاص</label>
<input type="number" id="guests" placeholder="مثال: 250" required>

<button type="submit">تأكيد الحجز</button>

</form>

</div>

<!-- الصور -->
<div class="gallery">

<img src="https://images.unsplash.com/photo-1511285560929-80b456fea0bc?q=80&w=1200&auto=format&fit=crop">

<img src="https://images.unsplash.com/photo-1522673607200-164d1b6ce486?q=80&w=1200&auto=format&fit=crop">

<img src="https://images.unsplash.com/photo-1519225421980-715cb0215aed?q=80&w=1200&auto=format&fit=crop">

<img src="https://images.unsplash.com/photo-1519167758481-83f550bb49b3?q=80&w=1200&auto=format&fit=crop">

</div>

</div>

<footer>
© 2026 قاعة ملاك للحفلات - جميع الحقوق محفوظة
</footer>

<script>

// عداد الزوار
let visitors = localStorage.getItem("visitors");

if(!visitors){
visitors = 1542;
}else{
visitors = parseInt(visitors) + 1;
}

localStorage.setItem("visitors", visitors);

document.getElementById("visitors").innerText = visitors;


// عداد الحجوزات
let bookings = localStorage.getItem("bookings");

if(!bookings){
bookings = 327;
}

document.getElementById("bookings").innerText = bookings;


// عند إرسال الحجز
document.getElementById("bookingForm").addEventListener("submit", function(e){

e.preventDefault();

let count = parseInt(localStorage.getItem("bookings")) || 327;

count++;

localStorage.setItem("bookings", count);

document.getElementById("bookings").innerText = count;

alert("تم إرسال طلب الحجز بنجاح، سيتم التواصل معك قريباً.");

this.reset();

});

</script>

</body>
</html>