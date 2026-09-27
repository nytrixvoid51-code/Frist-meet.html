<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">

<meta name="viewport"
      content="width=device-width, initial-scale=1.0,
      maximum-scale=1.0, user-scalable=no">

<title>Our Special Day ❤️</title>

<style>

@import url('https://fonts.googleapis.com/css2?family=Baloo+2:wght@400;500;600;700&family=Pacifico&display=swap');

*{
    box-sizing:border-box;
    -webkit-tap-highlight-color:transparent;
}

html,body{
    margin:0;
    width:100%;
    height:100%;
    overflow:hidden;
}

body{
    font-family:'Baloo 2',cursive;
    color:white;
    background:#86152f;
}

/* MAIN BACKGROUND */

.app{
    width:100vw;
    height:100dvh;
    overflow:hidden;
    position:relative;

    background:
    radial-gradient(circle at 15% 15%,
    rgba(255,255,255,.13),
    transparent 25%),

    radial-gradient(circle at 85% 75%,
    rgba(255,150,180,.18),
    transparent 30%),

    linear-gradient(
    145deg,
    #75102d,
    #b72842,
    #7c102e
    );
}

/* GLOW */

.glow{
    position:absolute;
    width:180px;
    height:180px;
    border-radius:50%;
    background:#ff9fbd;
    filter:blur(35px);
    opacity:.3;
    left:-70px;
    top:100px;
}

.glow2{
    position:absolute;
    width:200px;
    height:200px;
    border-radius:50%;
    background:#ffb8cf;
    filter:blur(40px);
    opacity:.25;
    right:-80px;
    bottom:60px;
}

/* FLOATING EMOJIS */

.floating span{
    position:absolute;
    font-size:25px;
    opacity:.8;
    animation:float 6s ease-in-out infinite;
}

.floating span:nth-child(1){
    left:7%;
    top:15%;
}

.floating span:nth-child(2){
    right:8%;
    top:32%;
    animation-delay:1s;
}

.floating span:nth-child(3){
    left:12%;
    bottom:20%;
    animation-delay:2s;
}

.floating span:nth-child(4){
    right:14%;
    bottom:13%;
    animation-delay:3s;
}

@keyframes float{
    50%{
        transform:translateY(-22px) rotate(8deg);
    }
}

/* PROGRESS */

.progress{
    position:absolute;
    top:0;
    left:0;
    height:4px;
    background:white;
    width:16.66%;
    z-index:50;
    transition:.5s;
}

/* SLIDES */

.slides{
    height:100%;
    display:flex;
    transition:
    transform .65s
    cubic-bezier(.77,0,.18,1);
}

.slide{
    min-width:100%;
    height:100%;

    display:flex;
    justify-content:center;
    align-items:center;

    text-align:center;

    padding:
    30px
    18px
    100px;

    position:relative;
}

.content{
    width:min(94vw,650px);
    position:relative;
    z-index:5;
}

/* TEXT */

.badge{
    display:inline-block;

    background:rgba(255,255,255,.93);
    color:#d13d67;

    padding:8px 17px;

    border-radius:999px;

    font-weight:700;

    margin-bottom:16px;
}

.hero{
    font-family:'Pacifico',cursive;

    font-size:
    clamp(43px,12vw,82px);

    line-height:1.05;

    margin:10px 0 18px;

    text-shadow:
    0 7px 22px
    rgba(70,0,20,.35);
}

.big{
    font-size:
    clamp(23px,6vw,40px);

    line-height:1.22;

    font-weight:700;
}

.small{
    font-size:
    clamp(16px,4.5vw,24px);

    line-height:1.35;

    margin-top:15px;
}

/* DATE */

.date{
    display:inline-block;

    font-size:
    clamp(20px,5.5vw,31px);

    font-weight:700;

    padding:9px 17px;

    border:
    2px solid
    rgba(255,255,255,.65);

    border-radius:18px;

    background:
    rgba(255,255,255,.13);

    margin:15px 0;
}

/* PHOTO FRAME */

.polaroid{

    width:min(75vw,340px);

    height:min(44vw,225px);

    background:white;

    color:#7d1837;

    padding:
    9px
    9px
    35px;

    border-radius:17px;

    margin:
    0 auto 20px;

    box-shadow:
    0 18px 40px
    rgba(50,0,20,.35);

    transform:rotate(-2deg);
}

.photo{
    width:100%;
    height:100%;

    border-radius:11px;

    overflow:hidden;

    background:
    linear-gradient(
    135deg,
    #ffd4e2,
    #fff2f6
    );

    display:flex;
    justify-content:center;
    align-items:center;
}

.photo img{
    width:100%;
    height:100%;

    object-fit:cover;
}

.caption{
    font-family:'Pacifico',cursive;

    font-size:17px;

    position:relative;

    top:5px;
}

/* WHITE NOTE */

.card{

    background:
    rgba(255,255,255,.94);

    color:#7b1636;

    border-radius:27px;

    padding:25px 20px;

    box-shadow:
    0 18px 45px
    rgba(40,0,15,.3);
}

.card p{

    font-size:
    clamp(21px,5.5vw,31px);

    line-height:1.35;

    font-weight:700;

    margin:0;
}

/* MEMORY GRID */

.grid{

    display:grid;

    grid-template-columns:
    1fr 1fr;

    gap:12px;

    margin:18px 0;
}

.box{

    padding:18px 10px;

    border-radius:22px;

    background:
    rgba(255,255,255,.16);

    border:
    1px solid
    rgba(255,255,255,.3);

    backdrop-filter:blur(8px);
}

.box b{
    display:block;
    font-size:38px;
}

.box span{
    font-size:16px;
}

/* =========================
   SMALL MUSIC PLAYER
========================= */

.music-player{

    width:min(90vw,430px);

    margin:18px auto 0;

    padding:12px 14px;

    border-radius:20px;

    background:
    rgba(255,255,255,.17);

    border:
    1px solid
    rgba(255,255,255,.35);

    backdrop-filter:blur(12px);

    box-shadow:
    0 12px 30px
    rgba(40,0,15,.25);
}

.track{
    display:flex;
    align-items:center;
    gap:10px;

    text-align:left;
}

.album{

    width:44px;
    height:44px;

    flex:none;

    border-radius:14px;

    background:
    linear-gradient(
    135deg,
    white,
    #ffd5e4
    );

    display:grid;
    place-items:center;

    font-size:21px;
}

.title{
    font-size:17px;
    font-weight:700;
}

.sub{
    font-size:11px;
    opacity:.8;
}

.player-row{

    display:flex;

    align-items:center;

    gap:8px;

    margin-top:10px;
}

.play{

    width:38px;
    height:38px;

    border:0;

    border-radius:50%;

    background:white;

    color:#d13d67;

    font-size:16px;

    box-shadow:
    0 6px 15px
    rgba(40,0,15,.2);
}

.seek{

    height:5px;

    flex:1;

    background:
    rgba(255,255,255,.35);

    border-radius:99px;

    overflow:hidden;

    cursor:pointer;
}

.fill{

    width:0%;

    height:100%;

    background:white;

    border-radius:99px;
}

.time{

    font-size:11px;

    width:32px;
}

/* FINAL VIDEO */

.video-box{

    width:min(92vw,600px);

    margin:20px auto;

    border-radius:25px;

    overflow:hidden;

    background:#000;

    box-shadow:
    0 18px 45px
    rgba(40,0,15,.45);

    border:
    3px solid
    rgba(255,255,255,.35);
}

.video-box video{

    width:100%;

    max-height:45vh;

    display:block;

    object-fit:cover;
}

/* FINAL HEART */

.final-heart{

    font-size:105px;

    animation:
    pulse 1.4s infinite;
}

@keyframes pulse{

    50%{
        transform:scale(1.08);
    }

}

/* SLIDE NUMBER */

.num{

    position:absolute;

    top:17px;

    left:18px;

    font-size:13px;

    opacity:.6;
}

/* NAVIGATION */

.controls{

    position:absolute;

    z-index:60;

    bottom:14px;

    left:0;
    right:0;

    display:flex;

    justify-content:center;

    align-items:center;

    gap:10px;
}

.nav{

    border:0;

    background:white;

    color:#d13d67;

    border-radius:999px;

    padding:12px 19px;

    font:
    700 18px
    'Baloo 2';

    box-shadow:
    0 9px 25px
    rgba(40,0,15,.3);
}

.dots{

    display:flex;

    gap:5px;
}

.dot{

    width:8px;
    height:8px;

    border-radius:99px;

    background:
    rgba(255,255,255,.4);
}

.dot.on{

    width:22px;

    background:white;
}

/* SMALL SCREEN */

@media(max-height:650px){

    .slide{
        padding-bottom:82px;
    }

    .hero{
        font-size:45px;
    }

    .polaroid{
        height:175px;
    }

    .big{
        font-size:21px;
    }

    .small{
        font-size:16px;
    }

}

</style>
</head>

<body>

<div class="app">

<div class="glow"></div>
<div class="glow2"></div>

<!-- FLOATING EMOJIS -->

<div class="floating">

<span>💗</span>
<span>✨</span>
<span>🌸</span>
<span>💕</span>

</div>

<div
class="progress"
id="progress">
</div>


<div
class="slides"
id="slides">


<!-- =========================
     SLIDE 1
     MUSIC
========================= -->

<section class="slide">

<div class="content">

<div class="badge">
🎵 A little song for you
</div>

<div class="polaroid">

<div class="photo">

<!-- নিজের PNG চাইলে এখানে -->
<img
src="pic1.png"
alt="Our memory">

</div>

<div class="caption">
Our Special Day 💗
</div>

</div>

<h1 class="hero">
See You Soon,<br>
Love ❤️
</h1>

<p class="big">

“Some moments deserve
their own soundtrack… 🎶
and this little song is for
the moment when I finally
get to see you.”

</p>


<!-- SMALL MUSIC PLAYER -->

<div class="music-player">

<div class="track">

<div class="album">
🎵
</div>

<div>

<div class="title">
Our Special Song 💗
</div>

<div class="sub">
17 October 2026 • Just for you
</div>

</div>

</div>


<div class="player-row">

<button
class="play"
id="play"
onclick="toggleMusic()">

🌕

</button>


<div
class="seek"
onclick="seek(event)">

<div
class="fill"
id="fill">
</div>

</div>


<div
class="time"
id="time">

0:00

</div>

</div>

</div>

</div>

<div class="num">
01 / 06
</div>

</section>



<!-- =========================
     SLIDE 2
========================= -->

<section class="slide">

<div class="content">

<div class="badge">
🌸 Finally, that day...
</div>

<div class="card">

<p>

“I don't know how that
first moment will feel,
but I know one thing—
after waiting for so long,
seeing you in front of me
will make this day
unforgettable.” 🥹❤️

</p>

</div>

<p class="small">

Maybe I'll be nervous,
maybe I'll smile too much…
but I'll be genuinely happy
that you're there. 🫶

</p>

</div>

<div class="num">
02 / 06
</div>

</section>



<!-- =========================
     SLIDE 3
========================= -->

<section class="slide">

<div class="content">

<div class="badge">
📸 Little moments,
big memories
</div>


<div class="grid">

<div class="box">
<b>🥹</b>
<span>That first look</span>
</div>

<div class="box">
<b>😊</b>
<span>That first smile</span>
</div>

<div class="box">
<b>💬</b>
<span>Our first real talk</span>
</div>

<div class="box">
<b>💗</b>
<span>A memory to keep</span>
</div>

</div>


<!-- PNG 2 -->

<div class="polaroid">

<div class="photo">

<img
src="pic2.png"
alt="Memory">

</div>

<div class="caption">
A memory to remember 💕
</div>

</div>


<p class="big">

“We don't need a perfect day.
We just need one honest
moment where we can look
at each other and think…

finally.” ✨

</p>

</div>

<div class="num">
03 / 06
</div>

</section>



<!-- =========================
     SLIDE 4
========================= -->

<section class="slide">

<div class="content">

<div class="polaroid"
style="transform:rotate(2deg)">

<div class="photo">

<img
src="pic3.png"
alt="Special memory">

</div>

<div class="caption">
Just us & this moment 💕
</div>

</div>


<p class="big">

“If I could pause one moment
that day, I'd choose the
moment when all the waiting
disappears and I realize…

you're really here.” 🥹💗

</p>


<p class="small">

And yes…
I'll probably remember
the smallest details too. 🌷✨

</p>

</div>

<div class="num">
04 / 06
</div>

</section>



<!-- =========================
     SLIDE 5
========================= -->

<section class="slide">

<div class="content">

<div class="badge">
💌 One special thought
</div>


<div class="card">

<p>

“I don't need a perfect
movie-like moment.

Just your smile,
my happiness,
and a little time together.

That's enough to make
17 October 2026 special.” ❤️

</p>

</div>


<p class="small">

Some memories become
special simply because
they are real. 🌸

</p>


<div class="date">

17 • 10 • 2026 💞

</div>

</div>

<div class="num">
05 / 06
</div>

</section>



<!-- =========================
     SLIDE 6
     FINAL VIDEO
========================= -->

<section class="slide">

<div class="content">

<div class="badge">
🎬 One last thing...
</div>


<div class="video-box">

<video
controls
playsinline
poster="pic1.png">

<source
src="final-video.mp4"
type="video/mp4">

Your browser does not support
the video tag.

</video>

</div>


<h1 class="hero">
Our First Meet ❤️
</h1>


<p class="big">

“17 October 2026 —
the day a long wait
turns into one beautiful
memory.” 🥹✨

</p>


<p class="small">

See you soon, love. 💗

Until then…
keep smiling,
keep shining,
and save a little smile
for me. 🌸

</p>


<div class="date">

17 • 10 • 2026 💞

</div>

</div>

<div class="num">
06 / 06
</div>

</section>


</div>


<!-- NAVIGATION -->

<div class="controls">

<button
class="nav"
onclick="prev()">

⬅️ Back

</button>


<div
class="dots"
id="dots">
</div>


<button
class="nav"
onclick="next()">

Next ➡️

</button>

</div>


</div>


<!-- =========================
     YOUR SONG
========================= -->

<audio
id="audio"
preload="metadata">

<source
src="song.mp3"
type="audio/mpeg">

</audio>



<script>

/* =========================
   SLIDE SYSTEM
========================= */

let current = 0;

const total = 6;

const slides =
document.getElementById("slides");

const dots =
document.getElementById("dots");

const progress =
document.getElementById("progress");


/* CREATE DOTS */

for(let i=0;i<total;i++){

    let dot =
    document.createElement("i");

    dot.className =
    "dot" +
    (i === 0 ? " on" : "");

    dot.onclick =
    () => goTo(i);

    dots.appendChild(dot);
}


/* CHANGE SLIDE */

function goTo(index){

    current =
    (index + total) % total;

    slides.style.transform =
    `translateX(-${current * 100}%)`;


    [...dots.children].forEach(
        (dot,i)=>{

            dot.classList.toggle(
                "on",
                i === current
            );

        }
    );


    progress.style.width =
    ((current + 1) / total * 100)
    + "%";
}


function next(){

    goTo(current + 1);

}


function prev(){

    goTo(current - 1);

}


/* =========================
   MUSIC PLAYER
========================= */

const audio =
document.getElementById("audio");

const play =
document.getElementById("play");

const fill =
document.getElementById("fill");

const time =
document.getElementById("time");


/* PLAY / PAUSE */

function toggleMusic(){

    if(audio.paused){

        audio.play();

        play.textContent =
        "🧿";

    }else{

        audio.pause();

        play.textContent =
        "🌕";

    }

}


/* MUSIC PROGRESS */

audio.addEventListener(
"timeupdate",
()=>{

    if(!audio.duration)
        return;


    let percent =
    (audio.currentTime /
    audio.duration) * 100;


    fill.style.width =
    percent + "%";


    let seconds =
    Math.floor(
        audio.currentTime
    );


    let minutes =
    Math.floor(seconds / 60);


    seconds =
    seconds % 60;


    time.textContent =
    minutes +
    ":" +
    String(seconds)
    .padStart(2,"0");

});


/* RESET AFTER SONG */

audio.addEventListener(
"ended",
()=>{

    play.textContent =
    "🌕";

    fill.style.width =
    "0%";

    time.textContent =
    "0:00";

});


/* SEEK */

function seek(event){

    if(!audio.duration)
        return;


    const bar =
    event.currentTarget;

    const rect =
    bar.getBoundingClientRect();


    const position =
    (event.clientX -
    rect.left) /
    rect.width;


    audio.currentTime =
    position *
    audio.duration;

}


/* =========================
   SWIPE
========================= */

let startX = 0;


document.addEventListener(
"touchstart",
event=>{

    startX =
    event.changedTouches[0]
    .screenX;

},
{passive:true}
);


document.addEventListener(
"touchend",
event=>{

    let endX =
    event.changedTouches[0]
    .screenX;


    let difference =
    endX - startX;


    if(Math.abs(difference) > 55){

        if(difference < 0){

            next();

        }else{

            prev();

        }

    }

},
{passive:true}
);


/* START */

goTo(0);

</script>

</body>
</html>
