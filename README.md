# website.noe
<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Noe's Little Universe</title>

<link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@300;400;500;600&family=Playfair+Display:ital,wght@0,400;0,500;1,400&display=swap" rel="stylesheet">

<style>
:root {
  --blue: #829bc2;
  --dark: #526b91;
  --lavender: #aaa4cc;
  --light: #f5f7fc;
  --text: #65758f;
  --white: #ffffff;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  scroll-behavior: smooth;
}

body {
  font-family: 'DM Sans', sans-serif;
  background: var(--light);
  color: var(--text);
  overflow-x: hidden;
}

h1, h2, h3 {
  font-family: 'Playfair Display', serif;
  font-weight: 400;
}

button {
  font-family: inherit;
  cursor: pointer;
}

/* INTRO */

.intro {
  position: fixed;
  inset: 0;
  z-index: 9999;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  padding: 25px;
  background:
    radial-gradient(circle at 20% 20%, #dceaff, transparent 40%),
    radial-gradient(circle at 80% 80%, #e8dcff, transparent 40%),
    #f8f9ff;
  transition: 1s;
}

.intro.hide {
  opacity: 0;
  visibility: hidden;
}

.intro-content {
  animation: appear 1.5s ease;
}

.intro-small {
  font-size: 10px;
  letter-spacing: 4px;
  color: #8b9dbb;
}

.intro h1 {
  font-size: clamp(42px, 10vw, 70px);
  line-height: 1.3;
  color: var(--dark);
  margin: 25px 0;
}

.intro h1 span {
  color: var(--lavender);
  font-style: italic;
}

.intro-description {
  font-size: 12px;
  line-height: 2;
  max-width: 300px;
  margin: auto;
}

.intro-flower {
  font-size: 30px;
  margin: 25px;
  color: var(--lavender);
}

#enterBtn {
  background: var(--blue);
  color: white;
  border: none;
  border-radius: 30px;
  padding: 14px 30px;
  margin-top: 10px;
  transition: .3s;
}

#enterBtn:hover {
  background: var(--dark);
  transform: translateY(-4px);
}

.intro-footer {
  font-size: 10px;
  margin-top: 25px;
  color: #a0a9bd;
}

/* NAVBAR */

nav {
  position: sticky;
  top: 0;
  z-index: 100;
  background: #ffffffd9;
  backdrop-filter: blur(15px);
  padding: 18px 7%;
  display: flex;
  align-items: center;
  justify-content: space-between;
  box-shadow: 0 3px 20px #829bc214;
}

.logo {
  font-family: 'Playfair Display', serif;
  color: var(--dark);
  font-size: 21px;
}

.nav-links {
  display: flex;
  gap: 25px;
}

.nav-links a {
  text-decoration: none;
  color: var(--text);
  font-size: 12px;
  transition: .3s;
}

.nav-links a:hover {
  color: var(--lavender);
}

.menu-btn {
  display: none;
  background: none;
  border: none;
  color: var(--dark);
  font-size: 23px;
}

/* HERO */

.hero {
  min-height: 85vh;
  padding: 80px 8%;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 40px;
  background:
    radial-gradient(circle at 80% 30%, #e5e5ff, transparent 35%),
    linear-gradient(135deg, #f7faff, #edf2fc);
}

.hero-text {
  max-width: 530px;
}

.label {
  display: inline-block;
  background: #e5ebf8;
  color: var(--blue);
  border-radius: 30px;
  padding: 9px 17px;
  font-size: 10px;
  letter-spacing: 2px;
  margin-bottom: 25px;
}

.hero h1 {
  font-size: clamp(45px, 8vw, 75px);
  color: var(--dark);
  line-height: 1.15;
}

.hero h1 span {
  color: var(--lavender);
  font-style: italic;
}

.hero p {
  font-size: 13px;
  line-height: 2;
  margin: 25px 0;
  max-width: 400px;
}

.main-button {
  display: inline-block;
  background: var(--blue);
  color: white;
  padding: 14px 25px;
  border-radius: 30px;
  text-decoration: none;
  font-size: 12px;
  transition: .3s;
}

.main-button:hover {
  background: var(--dark);
  transform: translateY(-4px);
}

.hero-image {
  width: 290px;
  height: 370px;
  border-radius: 150px 150px 25px 25px;
  object-fit: cover;
  box-shadow: 15px 15px 0 #dce3f4;
}

/* GENERAL SECTION */

section {
  padding: 85px 8%;
}

.section-title {
  text-align: center;
  margin-bottom: 45px;
}

.section-title small {
  color: var(--lavender);
  font-size: 10px;
  letter-spacing: 4px;
}

.section-title h2 {
  font-size: 39px;
  color: var(--dark);
  margin-top: 12px;
}

/* ABOUT */

.about {
  background: white;
  text-align: center;
}

.about-box {
  max-width: 650px;
  margin: auto;
  padding: 35px;
  background: #f6f8fd;
  border-radius: 20px;
  line-height: 2;
  font-size: 13px;
}

.about-box span {
  color: var(--lavender);
  font-weight: 600;
}

/* FAVORITES */

.favorites {
  background: #f1f4fb;
}

.favorite-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
}

.favorite-card {
  background: white;
  padding: 30px 20px;
  border-radius: 18px;
  text-align: center;
  transition: .3s;
}

.favorite-card:hover {
  transform: translateY(-8px);
}

.favorite-icon {
  font-size: 28px;
  margin-bottom: 15px;
  color: var(--lavender);
}

.favorite-card h3 {
  color: var(--dark);
  font-size: 21px;
  margin-bottom: 10px;
}

.favorite-card p {
  font-size: 12px;
  line-height: 1.8;
}

/* GALLERY */

.gallery {
  background: white;
}

.gallery-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 17px;
}

.gallery-grid img {
  width: 100%;
  height: 240px;
  object-fit: cover;
  border-radius: 15px;
  transition: .4s;
}

.gallery-grid img:hover {
  transform: scale(1.03);
}

/* MUSIC */

.music {
  background: linear-gradient(135deg, #e9eefb, #f3edfb);
  text-align: center;
}

.music-box {
  max-width: 450px;
  margin: auto;
  padding: 35px;
  border-radius: 22px;
  background: #ffffffc9;
}

.music-box h3 {
  font-size: 27px;
  color: var(--dark);
  margin: 15px;
}

.music-box p {
  font-size: 12px;
  line-height: 1.8;
}

#musicBtn {
  border: none;
  background: var(--blue);
  color: white;
  border-radius: 30px;
  padding: 13px 28px;
  margin-top: 22px;
}

/* DIARY */

.diary {
  background: white;
  text-align: center;
}

.diary-box {
  max-width: 550px;
  margin: auto;
  padding: 35px;
  background: #f6f8fd;
  border-radius: 20px;
  line-height: 2;
  font-size: 13px;
  font-style: italic;
}

/* QUOTE */

.quote {
  background: #f1f4fb;
  text-align: center;
}

.quote-box {
  max-width: 550px;
  margin: auto;
}

.quote-box h3 {
  font-size: 25px;
  line-height: 1.7;
  color: var(--dark);
  margin-bottom: 25px;
}

.quote-box button {
  border: 1px solid var(--blue);
  color: var(--dark);
  background: transparent;
  border-radius: 30px;
  padding: 12px 25px;
}

/* FOOTER */

footer {
  background: #526b91;
  color: white;
  text-align: center;
  padding: 35px 20px;
  font-size: 11px;
  line-height: 2;
}

footer h3 {
  font-size: 25px;
  margin-bottom: 10px;
}

/* MUSIC BUTTON */

.music-button {
  position: fixed;
  bottom: 20px;
  left: 15px;
  z-index: 500;
  border: 1px solid white;
  border-radius: 30px;
  background: #ffffffed;
  color: var(--dark);
  padding: 12px 18px;
  font-size: 11px;
  box-shadow: 0 5px 20px #809bc222;
}

/* ANIMATION */

.reveal {
  opacity: 0;
  transform: translateY(30px);
  transition: .8s;
}

.reveal.active {
  opacity: 1;
  transform: translateY(0);
}

@keyframes appear {
  from {
    opacity: 0;
    transform: translateY(25px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* MOBILE */

@media(max-width: 700px) {
  nav {
    padding: 15px 6%;
  }

  .menu-btn {
    display: block;
  }

  .nav-links {
    display: none;
    position: absolute;
    top: 60px;
    left: 0;
    width: 100%;
    background: white;
    padding: 25px;
    flex-direction: column;
    text-align: center;
    gap: 20px;
  }

  .nav-links.show {
    display: flex;
  }

  .hero {
    flex-direction: column-reverse;
    text-align: center;
    padding: 60px 7%;
  }

  .hero p {
    margin: 20px auto;
  }

  .hero-image {
    width: 220px;
    height: 270px;
  }

  section {
    padding: 65px 7%;
  }

  .favorite-grid {
    grid-template-columns: 1fr;
  }

  .gallery-grid {
    grid-template-columns: repeat(2, 1fr);
  }

  .gallery-grid img {
    height: 180px;
  }

  .section-title h2 {
    font-size: 32px;
  }
}
</style>
</head>

<body>

<!-- OPENING SCREEN -->

<div class="intro" id="intro">
  <div class="intro-content">
    <p class="intro-small">A SPECIAL PLACE FOR LITTLE THINGS</p>
    <h1>A little world<br>made by <span>Noe.</span></h1>
    <p class="intro-description">
      Memories, dreams, and everything that makes my world beautiful.
    </p>
    <div class="intro-flower">✿ ♡ ✧</div>
    <button id="enterBtn">Enter My Universe →</button>
    <p class="intro-footer">take a little look around</p>
  </div>
</div>

<!-- NAVIGATION -->

<nav>
  <div class="logo">Noe's Universe.</div>

  <button class="menu-btn" id="menuBtn">☰</button>

  <div class="nav-links" id="navLinks">
    <a href="#home">Home</a>
    <a href="#about">About</a>
    <a href="#favorites">Favorites</a>
    <a href="#gallery">Gallery</a>
    <a href="#diary">Diary</a>
  </div>
</nav>

<!-- HOME -->

<div class="hero" id="home">
  <div class="hero-text reveal">
    <span class="label">WELCOME TO MY LITTLE WORLD</span>

    <h1>Welcome to<br>my <span>universe.</span></h1>

    <p>
      A little corner of the internet where I keep my memories,
      favorite things, little dreams, and pieces of my story.
    </p>

    <a href="#about" class="main-button">Discover My World →</a>
  </div>

  <img
    class="hero-image"
    src="https://images.unsplash.com/photo-1470252649378-9c29740c9fa8?w=700"
    alt="Dreamy landscape">
</div>

<!-- ABOUT -->

<section class="about" id="about">
  <div class="section-title reveal">
    <small>GET TO KNOW ME</small>
    <h2>About Me</h2>
  </div>

  <div class="about-box reveal">
    <p>
      Hello! Welcome to my little universe.

      This website is a small collection of things about me.
      I love listening to music, collecting memories,
      enjoying beautiful places, and discovering new things.

      <br><br>

      <span>Just a little space to be myself.</span>
    </p>
  </div>
</section>

<!-- FAVORITES -->

<section class="favorites" id="favorites">
  <div class="section-title reveal">
    <small>THE LITTLE THINGS I LOVE</small>
    <h2>My Favorites</h2>
  </div>

  <div class="favorite-grid">

    <div class="favorite-card reveal">
      <div class="favorite-icon">♫</div>
      <h3>Music</h3>
      <p>Listening to songs and enjoying every little melody.</p>
    </div>

    <div class="favorite-card reveal">
      <div class="favorite-icon">✿</div>
      <h3>Nature</h3>
      <p>Beautiful views, fresh air, and peaceful places.</p>
    </div>

    <div class="favorite-card reveal">
      <div class="favorite-icon">♡</div>
      <h3>Memories</h3>
      <p>Keeping little moments that mean something to me.</p>
    </div>

  </div>
</section>

<!-- GALLERY -->

<section class="gallery" id="gallery">
  <div class="section-title reveal">
    <small>CAPTURED MOMENTS</small>
    <h2>Little Gallery</h2>
  </div>

  <div class="gallery-grid reveal">

    <img src="https://images.unsplash.com/photo-1470770841072-f978cf4d019e?w=600" alt="Mountain view">

    <img src="https://images.unsplash.com/photo-1490750967868-88aa4486c946?w=600" alt="Flowers">

    <img src="https://images.unsplash.com/photo-1500530855697-b586d89ba3ee?w=600" alt="Nature">

    <img src="https://images.unsplash.com/photo-1470252649378-9c29740c9fa8?w=600" alt="Sunrise">

    <img src="https://images.unsplash.com/photo-1501785888041-af3ef285b470?w=600" alt="Lake">

    <img src="https://images.unsplash.com/photo-1497250681960-ef046c08a56e?w=600" alt="Plants">

  </div>
</section>

<!-- MUSIC -->

<section class="music">
  <div class="section-title reveal">
    <small>A LITTLE MELODY</small>
    <h2>Music Corner</h2>
  </div>

  <div class="music-box reveal">
    <div style="font-size:35px;color:#aaa4cc;">♫</div>

    <h3>My Little Playlist</h3>

    <p>
      A little music to make this corner feel more special.
    </p>

    <button id="musicBtn">♫ Play Music</button>
  </div>
</section>

<!-- DIARY -->

<section class="diary" id="diary">
  <div class="section-title reveal">
    <small>WORDS FROM MY HEART</small>
    <h2>Little Diary</h2>
  </div>

  <div class="diary-box reveal">
    "Every little moment has its own story.
    Some are worth remembering, some are worth learning from,
    and some are simply beautiful because they happened."
  </div>
</section>

<!-- RANDOM QUOTE -->

<section class="quote">
  <div class="quote-box reveal">
    <div class="section-title">
      <small>A LITTLE REMINDER</small>
      <h2>For Today</h2>
    </div>

    <h3 id="quoteText">
      "You are allowed to grow at your own pace."
    </h3>

    <button id="quoteBtn">Another Reminder ♡</button>
  </div>
</section>

<!-- FOOTER -->

<footer>
  <h3>Noe's Little Universe</h3>
  <p>Made with love, dreams, and little memories.</p>
  <p>© 2026 Noe. All rights reserved.</p>
</footer>

<!-- MUSIC FILE -->

<audio id="backgroundMusic" loop src="music.mp3"></audio>

<!-- JAVASCRIPT -->

<script>

// INTRO BUTTON

const intro = document.getElementById("intro");

document.getElementById("enterBtn").addEventListener("click", () => {
  intro.classList.add("hide");
});

// MOBILE MENU

const menuBtn = document.getElementById("menuBtn");
const navLinks = document.getElementById("navLinks");

menuBtn.addEventListener("click", () => {
  navLinks.classList.toggle("show");
});

document.querySelectorAll(".nav-links a").forEach(link => {
  link.addEventListener("click", () => {
    navLinks.classList.remove("show");
  });
});

// MUSIC BUTTON

const music = document.getElementById("backgroundMusic");
const musicBtn = document.getElementById("musicBtn");

musicBtn.addEventListener("click", async () => {

  if (music.paused) {
    try {
      await music.play();
      musicBtn.textContent = "♫ Pause Music";
    } catch (error) {
      musicBtn.textContent = "Add music.mp3 first";
    }
  } else {
    music.pause();
    musicBtn.textContent = "♫ Play Music";
  }

});

// RANDOM QUOTES

const quotes = [
  "You are allowed to grow at your own pace.",
  "Small steps are still progress.",
  "Make room for the things that make you happy.",
  "Every day is a new page of your story.",
  "Beautiful things take time.",
  "Keep your dreams a little bigger than your fears."
];

document.getElementById("quoteBtn").addEventListener("click", () => {

  const random = Math.floor(Math.random() * quotes.length);

  document.getElementById("quoteText").textContent =
    '"' + quotes[random] + '"';

});

// SCROLL ANIMATION

const observer = new IntersectionObserver(entries => {

  entries.forEach(entry => {

    if (entry.isIntersecting) {
      entry.target.classList.add("active");
    }

  });

});

document.querySelectorAll(".reveal").forEach(element => {
  observer.observe(element);
});

</script>

</body>
</html>