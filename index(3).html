<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<title>منصة مدارس كفاح البروف – نتائج الطلاب</title>

<meta name="viewport" content="width=device-width, initial-scale=1.0">

<style>
body{font-family:Tahoma;background:#f2f2f2;margin:0}
.container,.intro{
max-width:600px;margin:20px auto;background:#fff;
padding:20px;border-radius:8px;box-shadow:0 0 10px #ccc
}
h1,h2{text-align:center}
input,button{width:100%;padding:10px;margin:8px 0}
button{background:#007bff;color:#fff;border:none}
button:hover{background:#0056b3}
.hidden{display:none}
.result{background:#e9ffe9;padding:10px;border-radius:5px}
.back-btn{background:#6c757d}
</style>
</head>

<body>

<div class="intro">
<h1>منصة مدارس كفاح البروف</h1>
<p>منصة إلكترونية للاستعلام عن نتائج الطلاب</p>
</div>

<!-- الصفحة الرئيسية -->
<div class="container" id="home">
<h2>نظام النتائج المدرسية</h2>
<button onclick="showTeacher()">واجهة المعلم</button>
<button onclick="showStudent()">واجهة الطالب</button>
<button onclick="showChangePass()">تغيير كلمة السر</button>
</div>

<!-- واجهة المعلم -->
<div class="container hidden" id="teacher">
<button class="back-btn" onclick="back()">⬅ رجوع</button>
<h2>واجهة المعلم</h2>
<input type="password" id="pin" placeholder="أدخل كلمة السر">
<button onclick="unlock()">دخول</button>

<div id="teacherPanel" class="hidden">
<input id="t_name" placeholder="اسم الطالب">
<input id="t_seat" placeholder="رقم الجلوس">
<input id="t_result" placeholder="النتيجة">
<input id="t_exam" placeholder="نوع الامتحان (اختياري)">
<input id="t_note" placeholder="ملاحظة (اختياري)">
<button onclick="saveResult()">حفظ النتيجة</button>
<button onclick="clearDatabase()">مسح كل البيانات</button>
</div>
</div>

<!-- واجهة الطالب -->
<div class="container hidden" id="student">
<button class="back-btn" onclick="back()">⬅ رجوع</button>
<h2>واجهة الطالب</h2>
<input id="s_seat" placeholder="رقم الجلوس">
<button onclick="getResult()">عرض النتيجة</button>
<div id="output"></div>
</div>

<!-- صفحة تغيير كلمة السر -->
<div class="container hidden" id="changePass">
<button class="back-btn" onclick="back()">⬅ رجوع</button>
<h2>تغيير كلمة السر</h2>
<input type="password" id="oldPass" placeholder="كلمة السر القديمة">
<input type="password" id="newPass" placeholder="كلمة السر الجديدة">
<button onclick="changePassword()">حفظ التغيير</button>
</div>

<script src="https://www.gstatic.com/firebasejs/9.23.0/firebase-app-compat.js"></script>
<script src="https://www.gstatic.com/firebasejs/9.23.0/firebase-database-compat.js"></script>

<script>
const firebaseConfig = {
  apiKey: "AIzaSyAImNyFTMVJc_aYR4zh9RKUgEVPS_2l2q4",
  databaseURL: "https://school-results-36615-default-rtdb.firebaseio.com",
  projectId: "school-results-36615"
};

firebase.initializeApp(firebaseConfig);
const db = firebase.database();

let currentPassword = "2006";

db.ref("admin/password").once("value").then(s=>{
if(s.exists()) currentPassword = s.val();
});

function hideAll(){
document.querySelectorAll('.container')
.forEach(c=>c.classList.add('hidden'));
}

function showTeacher(){hideAll();teacher.classList.remove('hidden')}
function showStudent(){hideAll();student.classList.remove('hidden')}
function showChangePass(){hideAll();changePass.classList.remove('hidden')}
function back(){hideAll();home.classList.remove('hidden')}

function unlock(){
if(pin.value === currentPassword){
teacherPanel.classList.remove('hidden');
}else alert("كلمة السر غير صحيحة");
}

function changePassword(){
if(oldPass.value !== currentPassword)
return alert("كلمة السر القديمة خاطئة");

if(newPass.value.length < 4)
return alert("كلمة السر ضعيفة");

db.ref("admin/password").set(newPass.value).then(()=>{
currentPassword = newPass.value;
oldPass.value = newPass.value = "";
alert("تم تغيير كلمة السر بنجاح");
});
}

function saveResult(){
if(!t_name.value||!t_seat.value||!t_result.value)
return alert("املأ الحقول الأساسية");

db.ref("students/"+t_seat.value).set({
name:t_name.value,
result:t_result.value,
exam:t_exam.value,
note:t_note.value
}).then(()=>{
t_name.value=t_seat.value=t_result.value=t_exam.value=t_note.value="";
alert("تم الحفظ");
});
}

function getResult(){
if(!s_seat.value)return;
db.ref("students/"+s_seat.value).once("value").then(s=>{
output.innerHTML = s.exists() ?
`<div class="result">
الاسم: ${s.val().name}<br>
النتيجة: ${s.val().result}<br>
نوع الامتحان: ${s.val().exam||'-'}<br>
ملاحظة: ${s.val().note||'-'}
</div>` : "لا توجد نتيجة";
});
}

function clearDatabase(){
if(confirm("هل أنت متأكد؟"))
db.ref("students").remove();
}
</script>

</body>
</html>