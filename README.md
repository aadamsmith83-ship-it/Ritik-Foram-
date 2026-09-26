<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>For Ritik 💌</title>

<style>
* {
  box-sizing: border-box;
}

body {
  margin: 0;
  min-height: 100vh;
  background:
    radial-gradient(circle at top, #fff4f5, transparent 45%),
    linear-gradient(135deg, #ead7d2, #f8eeee, #dfc8c3);
  display: flex;
  justify-content: center;
  align-items: center;
  font-family: Georgia, serif;
  overflow-x: hidden;
}

/* Floating hearts */
.heart {
  position: fixed;
  bottom: -30px;
  font-size: 20px;
  opacity: 0.6;
  animation: float 7s linear infinite;
}

.heart:nth-child(1) { left: 10%; animation-delay: 1s; }
.heart:nth-child(2) { left: 25%; animation-delay: 3s; }
.heart:nth-child(3) { left: 70%; animation-delay: 2s; }
.heart:nth-child(4) { left: 88%; animation-delay: 4s; }

@keyframes float {
  0% {
    transform: translateY(0) rotate(0deg);
    opacity: 0;
  }
  20% { opacity: 0.7; }
  100% {
    transform: translateY(-110vh) rotate(25deg);
    opacity: 0;
  }
}

/* Envelope */
.container {
  text-align: center;
  width: 100%;
  max-width: 650px;
  padding: 25px;
}

.title {
  color: #653f3f;
  font-size: 30px;
  margin-bottom: 30px;
  letter-spacing: 1px;
}

.envelope {
  position: relative;
  width: 330px;
  height: 220px;
  margin: auto;
  cursor: pointer;
  perspective: 1000px;
}

.envelope-back {
  position: absolute;
  width: 100%;
  height: 100%;
  background: #c98f88;
  border-radius: 8px;
  box-shadow: 0 18px 35px rgba(70, 40, 40, 0.25);
}

.envelope-front {
  position: absolute;
  bottom: 0;
  width: 100%;
  height: 55%;
  background: #dca49d;
  clip-path: polygon(0 0, 50% 65%, 100% 0, 100% 100%, 0 100%);
  z-index: 4;
}

.flap {
  position: absolute;
  top: 0;
  width: 100%;
  height: 55%;
  background: #e7b5ae;
  clip-path: polygon(0 0, 100% 0, 50% 100%);
  transform-origin: top;
  transition: transform 1s ease;
  z-index: 5;
}

.seal {
  position: absolute;
  z-index: 6;
  left: 50%;
  top: 47%;
  transform: translate(-50%, -50%);
  width: 48px;
  height: 48px;
  background: #a95358;
  border-radius: 50%;
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 22px;
  box-shadow: 0 4px 10px rgba(0,0,0,.2);
}

.open-text {
  margin-top: 22px;
  color: #653f3f;
  font-size: 17px;
}

/* Letter */
.letter {
  display: none;
  margin: 0 auto;
  width: 100%;
  max-width: 590px;
  min-height: 650px;
  padding: 42px 38px;
  background:
    linear-gradient(rgba(255,255,255,.5), rgba(255,255,255,.5)),
    #fffdf5;
  box-shadow:
    0 20px 45px rgba(60,40,40,.25),
    inset 0 0 35px rgba(130,100,70,.08);
  border: 1px solid #eadfca;
  text-align: left;
  position: relative;
  animation: appear 1.2s ease;
}

@keyframes appear {
  from {
    opacity: 0;
    transform: translateY(40px) scale(.96);
  }
  to {
    opacity: 1;
    transform: translateY(0) scale(1);
  }
}

.letter::before {
  content: "";
  position: absolute;
  inset: 14px;
  border: 1px solid #ead8c0;
  pointer-events: none;
}

.letter h1 {
  text-align: center;
  color: #9a4e55;
  font-size: 31px;
  margin-bottom: 30px;
}

.letter p {
  color: #443737;
  font-size: 17px;
  line-height: 1.8;
  position: relative;
}

.name {
  color: #9a4e55;
  font-weight: bold;
}

.love {
  text-align: center;
  font-size: 28px;
  color: #9a4e55;
  margin: 30px 0;
  font-weight: bold;
}

.signature {
  text-align: right;
  font-size: 19px;
  color: #654747;
  margin-top: 35px;
  line-height: 1.7;
}

.small-note {
  text-align: center;
  margin-top: 30px;
  color: #8a6c6c;
  font-size: 13px;
}

/* Open animation */
.open .flap {
  transform: rotateX(180deg);
}

.open .seal,
.open .open-text,
.open .title {
  opacity: 0;
  transition: opacity .4s;
}

@media(max-width:600px) {
  .envelope {
    width: 290px;
    height: 195px;
  }

  .letter {
    padding: 35px 25px;
  }

  .letter p {
    font-size: 16px;
  }
}
</style>
</head>

<body>

<div class="heart">♡</div>
<div class="heart">♥</div>
<div class="heart">♡</div>
<div class="heart">♥</div>

<div class="container">

  <div class="title">A little something for you, Ritik 💌</div>

  <!-- ENVELOPE -->
  <div class="envelope" id="envelope" onclick="openLetter()">

    <div class="envelope-back"></div>

    <div class="flap"></div>

    <div class="envelope-front"></div>

    <div class="seal">♥</div>

  </div>

  <div class="open-text">Click the envelope to open it 💗</div>

  <!-- LETTER -->
  <div class="letter" id="letter">

    <h1>Happy Boyfriend Day, Ritik ❤️</h1>

    <p>
      Dear <span class="name">Ritik</span>,
    </p>

    <p>
      Happy Boyfriend Day to the person who somehow managed to become
      such an important part of my life. 🥹❤️
    </p>

    <p>
      I honestly don't know how you do it, but you can make me smile
      when I'm annoyed, make me laugh when I'm trying to be serious,
      and somehow make even the most normal conversations memorable.
    </p>

    <p>
      And yes... sometimes you are extremely annoying. 😂
      Like, seriously, sometimes I wonder if annoying me is actually
      your full-time job. But unfortunately for you, I'm still here. 😭😂
    </p>

    <p>
      I love all the little memories we have made together —
      the random conversations, the silly fights, the jokes,
      the late-night talks, and all those tiny moments that probably
      wouldn't mean much to anyone else but mean a lot to me.
    </p>

    <p>
      If someone asked me what I like most about you, I would probably
      need a whole notebook because there are too many things.
      And knowing me, I'd still somehow forget half of them. 😭
    </p>

    <div class="love">
      I LOVE YOU ❤️
    </div>

    <p>
      Thank you for being someone I can laugh with, talk to,
      share stupid thoughts with, and make memories with.
      I hope we always keep that silly side of us alive,
      because honestly, those moments are some of the best ones.
    </p>

    <p>
      Also, one very important announcement:
      You are officially stuck with my random messages,
      my mood swings, my unnecessary questions,
      and my extremely questionable jokes. 😂
    </p>

    <p>
      So... congratulations. You got me. 🤭❤️
    </p>

    <div class="signature">
      With lots of love,<br>
      <strong>Foram 💗</strong>
    </div>

    <div class="small-note">
      P.S. — Don't pretend you didn't smile while reading this. 😌😂
    </div>

  </div>

</div>

<script>
function openLetter() {
  const envelope = document.getElementById("envelope");
  const letter = document.getElementById("letter");

  envelope.classList.add("open");

  setTimeout(() => {
    envelope.style.display = "none";
    letter.style.display = "block";
  }, 900);
}
</script>

</body>
</html>
