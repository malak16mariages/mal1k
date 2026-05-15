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
font-family:Tajawal, sans-serif;
}

body{
background:#0e0e0e;
color:white;
}

/* الهيرو */
.hero{
height:100vh;
background:
linear-gradient(rgba(0,0,0,0.6),rgba(0,0,0,0.85)),
url('https://images.unsplash.com/photo-1519741497674-611481863552?q=80&w=1600&auto=format&fit=crop');
background-size:cover;
background-position:center;
display:flex;
justify-content:center;
align-items:center;
text-align:center;
padding:20px;
}

.hero h1{
font-size:55px;
color:#ffd700;
}

.hero p{
font-size:20px;
color:#ddd;
margin-top:10px;
}

/* الحاوية */
.container{
max-width:1000px;
margin:auto;
padding:40px 20px;
}

/* الفورم */
.form-box{
background:#1b1b1b;
padding:30px;
border-radius:20px;
margin-top:-80px;
box-shadow:0 0 25px rgba(255,215,0,0.1);
}

h2{
text-align:center;
color:#ffd700;
margin-bottom:20px;
}

label{
display:block;
margin-top:12px;
margin-bottom:5px;
}

input,select{
width:100%;
padding:14px;
border:none;
border-radius:10px;
background:#2a2a2a;
color:white;
outline:none;
}

button{
width:100%;
margin-top:20px;
padding:15px;
background:#ffd700;
border:none;
border-radius:12px;
font-size:18px;
font-weight:bold;
cursor:pointer;
}

button:hover{
background:white;
}

/* رسالة النجاح */
.success{
display:none;
margin-top:20px;
padding:20px;
border-radius:15px;
background:linear-gradient(135deg,#1e5128,#2d6a4f);
text-align:center;
}

</style>
</head>

<body>

<div class="hero">
<div>
<h1>قاعة ملاك للحفلات</h1>
<p>أجمل الأعراس بأجواء ملكية فاخرة</p>
</div>
</div>

<div class="container">

<div class="form-box">

<h2>حجز موعد عرس</h2>

<form id="form">

<label>الاسم الكامل</label>
<input id="name" required>

<label>رقم الهاتف</label>
<input id="phone" required>

<label>تاريخ الحفل</label>
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

<label>عدد الضيوف</label>
<input type="number" id="guests" required>

<button type="submit">تأكيد الحجز</button>

</form>

<div class="success" id="success">
🎉 تم استلام طلب الحجز بنجاح<br>
سيتم التواصل معك قريباً 💍
</div>

</div>

</div>

<script>

const botToken = "8629591924:AAFZN0zuvHgH19Rkl2wqs0SGp_gEWbJ_IDI";
const chatId = "8735699172";

document.getElementById("form").addEventListener("submit", function(e){
e.preventDefault();

let name = document.getElementById("name").value;
let phone = document.getElementById("phone").value;
let date = document.getElementById("date").value;
let wilaya = document.getElementById("wilaya").value;
let guests = document.getElementById("guests").value;

let message =
`💍 حجز جديد - قاعة ملاك

👤 الاسم: ${name}
📞 الهاتف: ${phone}
📅 التاريخ: ${date}
📍 الولاية: ${wilaya}
👥 الضيوف: ${guests}`;

/* إرسال تيليغرام */
fetch(`https://api.telegram.org/bot${botToken}/sendMessage`, {
method:"POST",
headers:{"Content-Type":"application/json"},
body:JSON.stringify({
chat_id:chatId,
text:message
})
});

/* نجاح مباشر بدون أخطاء */
document.getElementById("success").style.display = "block";
document.getElementById("form").reset();

window.scrollTo({top:document.body.scrollHeight, behavior:"smooth"});

});

</script>

</body>
</html>
