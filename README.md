<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Cheezal Dental Clinic | Smile Brighter</title>

<style>
body {
  margin:0;
  font-family: Arial, sans-serif;
  background:#f7f9fc;
  color:#222;
}

/* HERO */
.hero {
  background: linear-gradient(120deg, #0ea5e9, #2563eb);
  color:white;
  padding:80px 20px;
  text-align:center;
}
.hero h1 {
  font-size:40px;
  margin-bottom:10px;
}
.hero p {
  font-size:18px;
}

/* BUTTON */
.btn {
  background:white;
  color:#2563eb;
  padding:12px 20px;
  border-radius:8px;
  text-decoration:none;
  font-weight:bold;
}

/* SECTIONS */
section {
  padding:50px 20px;
  max-width:1100px;
  margin:auto;
}

.card {
  background:white;
  padding:20px;
  border-radius:12px;
  box-shadow:0 5px 15px rgba(0,0,0,0.1);
  margin:10px;
}

/* GRID */
.grid {
  display:flex;
  flex-wrap:wrap;
}

/* FORM */
input, textarea {
  width:100%;
  padding:10px;
  margin:8px 0;
  border-radius:8px;
  border:1px solid #ccc;
}

button {
  background:#2563eb;
  color:white;
  padding:12px;
  border:none;
  width:100%;
  border-radius:8px;
  cursor:pointer;
}

/* CHATBOT */
#chatbox {
  position:fixed;
  bottom:90px;
  right:20px;
  width:260px;
  background:white;
  border-radius:12px;
  box-shadow:0 5px 20px rgba(0,0,0,0.2);
  display:none;
  overflow:hidden;
}

#chatHeader {
  background:#2563eb;
  color:white;
  padding:10px;
}

#messages {
  height:200px;
  overflow:auto;
  padding:10px;
  font-size:14px;
}

#chatInput {
  display:flex;
}

#chatInput input {
  flex:1;
  border:none;
}

/* WhatsApp Button */
.whatsapp {
  position:fixed;
  bottom:20px;
  right:20px;
  background:#25D366;
  color:white;
  padding:15px;
  border-radius:50%;
  font-size:20px;
  text-decoration:none;
}
</style>
</head>

<body>

<!-- HERO -->
<div class="hero">
  <h1>Cheezal Dental Clinic</h1>
  <p>World-Class Dental Care • Modern Technology • Beautiful Smiles</p>
  <a class="btn" href="#booking">Book Appointment</a>
</div>

<!-- SERVICES -->
<section>
<h2>Our Services</h2>
<div class="grid">
  <div class="card">Teeth Whitening</div>
  <div class="card">Dental Implants</div>
  <div class="card">Braces & Aligners</div>
  <div class="card">Root Canal</div>
  <div class="card">Scaling & Polishing</div>
</div>
</section>

<!-- DOCTORS -->
<section>
<h2>Expert Dentists</h2>
<div class="card">
  <p>Highly trained specialists with modern equipment & years of experience.</p>
</div>
</section>

<!-- BOOKING -->
<section id="booking">
<h2>Book Appointment</h2>
<div class="card">
  <input type="text" placeholder="Your Name">
  <input type="text" placeholder="Phone Number">
  <input type="text" placeholder="Preferred Date">
  <textarea placeholder="Your Problem"></textarea>
  <button>Submit Appointment</button>
</div>
</section>

<!-- LOCATIONS -->
<section>
<h2>Our Locations</h2>
<div class="card">
  <p>DHA Karachi • Gulshan-e-Iqbal • Gulistan-e-Johar</p>
</div>
</section>

<!-- CHATBOT -->
<div id="chatbox">
  <div id="chatHeader">Cheezal AI Assistant</div>
  <div id="messages"></div>
  <div id="chatInput">
    <input id="userMsg" placeholder="Type...">
    <button onclick="sendMsg()">➤</button>
  </div>
</div>

<!-- WhatsApp -->
<a class="whatsapp" href="https://wa.me/923003774836" target="_blank">💬</a>

<button onclick="toggleChat()" style="position:fixed;bottom:20px;left:20px;padding:10px;background:#2563eb;color:white;border:none;border-radius:10px;">
Chat
</button>

<script>
function toggleChat(){
  let box = document.getElementById("chatbox");
  box.style.display = box.style.display === "block" ? "none" : "block";
}

function sendMsg(){
  let input = document.getElementById("userMsg");
  let msg = input.value;

  let messages = document.getElementById("messages");
  messages.innerHTML += "<div><b>You:</b> " + msg + "</div>";

  let reply = "Thank you! Our clinic will contact you soon for appointment confirmation.";

  setTimeout(()=>{
    messages.innerHTML += "<div><b>Clinic:</b> " + reply + "</div>";
  },500);

  input.value = "";
}
</script>

</body>
</html># Cheezal_DentalClinic
