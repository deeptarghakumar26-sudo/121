<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Deeptargha</title>
<style>* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Segoe UI", Arial, sans-serif;
}

html {
  scroll-behavior: smooth;
}

/* ===== BODY ===== */
body {
  background: #f5f7fa;
  color: #222;
  line-height: 1.6;
}

/* ===== NAVBAR ===== */
.navbar {
  position: sticky;
  top: 0;
  z-index: 100;
  background: #ffffff;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 15px 40px;
  box-shadow: 0 4px 12px rgba(0,0,0,0.08);
}

.logo {
  color: #e63946;
  font-size: 26px;
  font-weight: 800;
  letter-spacing: 1px;
}

.navbar nav a {
  margin-left: 20px;
  text-decoration: none;
  color: #333;
  font-weight: 600;
  transition: 0.3s;
}

.navbar nav a:hover {
  color: #e63946;
}

/* ===== HOME SECTION ===== */
.home {
  min-height: 90vh;
  display: flex;
  justify-content: space-around;
  align-items: center;
  padding: 60px 30px;
  flex-wrap: wrap;
}

.home h2 {
  font-size: 22px;
  color: #555;
}

.home h1 {
  font-size: 42px;
  color: #e63946;
  margin: 10px 0;
}

.home p {
  font-size: 18px;
  color: #444;
}

.home img {
  width: 280px;
  margin-top: 20px;
  animation: float 3s ease-in-out infinite;
}

/* Floating image animation */
@keyframes float {
  0% { transform: translateY(0); }
  50% { transform: translateY(-12px); }
  100% { transform: translateY(0); }
}

/* ===== BUTTON ===== */
button {
  margin-top: 18px;
  background: #e63946;
  color: white;
  border: none;
  padding: 12px 28px;
  font-size: 15px;
  font-weight: bold;
  border-radius: 6px;
  cursor: pointer;
  transition: 0.3s;
}

button:hover {
  background: #c92d3b;
  transform: translateY(-2px);
}

/* ===== ABOUT & CONTACT ===== */
.about,
.contact {
  background: #ffffff;
  text-align: center;
  padding: 60px 20px;
}

.about h2,
.contact h2 {
  font-size: 32px;
  color: #e63946;
  margin-bottom: 15px;
}

.about p {
  max-width: 700px;
  margin: auto;
  font-size: 17px;
  color: #444;
}

/* ===== CONTACT FORM ===== */
.contact form {
  max-width: 420px;
  margin: 25px auto 0;
  display: flex;
  flex-direction: column;
  gap: 12px;
}

input,
textarea {
  padding: 12px;
  font-size: 15px;
  border-radius: 5px;
  border: 1px solid #ccc;
  outline: none;
}

input:focus,
textarea:focus {
  border-color: #e63946;
}

textarea {
  resize: none;
  min-height: 120px;
}

#status {
  margin-top: 15px;
  font-weight: bold;
}

/* ===== WHATSAPP BUTTON ===== */
.whatsapp {
  position: fixed;
  right: 20px;
  bottom: 20px;
  background: #25d366;
  color: white;
  width: 56px;
  height: 56px;
  border-radius: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 26px;
  text-decoration: none;
  box-shadow: 0 8px 20px rgba(0,0,0,0.2);
  transition: 0.3s;
}

.whatsapp:hover {
  transform: scale(1.1);
}

/* ===== FOOTER ===== */
footer {
  background: #ffffff;
  text-align: center;
  padding: 15px;
  font-size: 14px;
  color: #555;
  margin-top: 30px;
}

/* ===== RESPONSIVE ===== */
@media (max-width: 768px) {
  .navbar {
    padding: 15px 20px;
  }

  .home {
    text-align: center;
  }

  .home h1 {
    font-size: 34px;
  }

  .home img {
    width: 220px;
  }
}
</style>
</head>
<body>

<header class="navbar">
  <h1 class="logo">Deeptargha Kumar</h1>
  <nav>
    <a href="#home">Home</a>
    <a href="#about">About</a>
    <a href="tel:7797380313">📞 Call</a>
  </nav>
</header>

<section id="home" class="home">
  <div>
    <h2>Hello, I'm</h2>
    <h1>Deeptargha Kumar</h1>
    <p>Professional Full-Stack Web Developer</p>
    <button onclick="scrollToContact()">Hire Me</button>
  </div>
  <img src="https://i.imgur.com/8Km9tLL.png" alt="Developer">
</section>

<section id="about" class="about">
  <h2>About Me</h2>
  <p>
    
    am Deeptargha Kumar, a motivated Full-Stack Web Developer and a Class 9 student who is passionate about web technologies. I build complete web solutions—from clean and responsive front-end designs to secure and scalable back-end systems—using HTML, CSS, JavaScript, Node.js, and MongoDB.

I believe in writing clean code, learning continuously, and delivering quality work. I am open to freelance opportunities, collaborations, and real-world projects that help me grow as a developer.
  </p>
</section>

<section id="contact" class="contact">
  <h2>Hire Me</h2>

  <form id="contactForm">
    <input type="text" id="name" placeholder="Your Name" required>
    <input type="email" id="email" placeholder="Your Email" required>
    <textarea id="message" placeholder="Your Message" required></textarea>
    <button type="submit">Send</button>
  </form>

  <p id="status"></p>
</section>

<a class="whatsapp" href="https://wa.me/917797380313">💬</a>

<footer>© 2026 Deeptargha Kumar</footer>

<script src="script.js">function scrollToContact() {
  document.getElementById("contact")
    .scrollIntoView({ behavior: "smooth" });
}

const form = document.getElementById("contactForm");
const status = document.getElementById("status");

form.addEventListener("submit", async (e) => {
  e.preventDefault();

  status.innerText = "Sending...";
  status.style.color = "blue";

  const data = {
    name: name.value.trim(),
    email: email.value.trim(),
    message: message.value.trim()
  };

  try {
    const res = await fetch("http://localhost:3000/messages", {
      method: "POST",
      headers: { "Content-Type": "application/json" },
      body: JSON.stringify(data)
    });

    if (!res.ok) throw new Error("Failed");

    status.innerText = "✅ Message sent successfully!";
    status.style.color = "green";
    form.reset();

  } catch (err) {
    status.innerText = "❌ Server error. Try again.";
    status.style.color = "red";
  }
});
</script>
<!-- Code injected by live-server -->
<script>
	// <![CDATA[  <-- For SVG support
	if ('WebSocket' in window) {
		(function () {
			function refreshCSS() {
				var sheets = [].slice.call(document.getElementsByTagName("link"));
				var head = document.getElementsByTagName("head")[0];
				for (var i = 0; i < sheets.length; ++i) {
					var elem = sheets[i];
					var parent = elem.parentElement || head;
					parent.removeChild(elem);
					var rel = elem.rel;
					if (elem.href && typeof rel != "string" || rel.length == 0 || rel.toLowerCase() == "stylesheet") {
						var url = elem.href.replace(/(&|\?)_cacheOverride=\d+/, '');
						elem.href = url + (url.indexOf('?') >= 0 ? '&' : '?') + '_cacheOverride=' + (new Date().valueOf());
					}
					parent.appendChild(elem);
				}
			}
			var protocol = window.location.protocol === 'http:' ? 'ws://' : 'wss://';
			var address = protocol + window.location.host + window.location.pathname + '/ws';
			var socket = new WebSocket(address);
			socket.onmessage = function (msg) {
				if (msg.data == 'reload') window.location.reload();
				else if (msg.data == 'refreshcss') refreshCSS();
			};
			if (sessionStorage && !sessionStorage.getItem('IsThisFirstTime_Log_From_LiveServer')) {
				console.log('Live reload enabled.');
				sessionStorage.setItem('IsThisFirstTime_Log_From_LiveServer', true);
			}
		})();
	}
	else {
		console.error('Upgrade your browser. This Browser is NOT supported WebSocket for Live-Reloading.');
	}
	// ]]>
</script>
</body>
</html>
