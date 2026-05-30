# Anniversary.-
3 years
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy 3rd Anniversary ❤️</title>

<style>
body{
    margin:0;
    padding:0;
    font-family:Arial,sans-serif;
    background:linear-gradient(135deg,#ff758c,#ff7eb3);
    overflow:hidden;
    text-align:center;
    color:white;
}

.container{
    position:relative;
    z-index:10;
    padding-top:50px;
}

h1{
    font-size:50px;
    animation:glow 2s infinite alternate;
}

@keyframes glow{
    from{ text-shadow:0 0 10px white; }
    to{ text-shadow:0 0 30px white; }
}

.photo{
    width:250px;
    height:250px;
    border-radius:50%;
    object-fit:cover;
    border:5px solid white;
    margin:20px 0;
}

.counter{
    font-size:28px;
    font-weight:bold;
    margin:20px;
}

.message{
    max-width:700px;
    margin:auto;
    font-size:20px;
    line-height:1.8;
    padding:20px;
}

.heart{
    position:absolute;
    color:white;
    font-size:20px;
    animation:rise linear infinite;
}

@keyframes rise{
    from{
        transform:translateY(100vh);
        opacity:1;
    }
    to{
        transform:translateY(-100px);
        opacity:0;
    }
}
</style>
</head>
<body>

<div class="container">
    <h1>❤️ Happy Anniversary ❤️</h1>

    <!-- Replace with your image -->
    <img src="xender/image/IMG_20260213_221427_871.jpg" class="photo">

    <div class="counter" id="days"></div>

    <div class="message">
        Three years ago our journey started.
        Since then every moment has become more beautiful because of you.
        Thank you for your love, care, trust and support.
        Here's to many more years together. ❤️
    </div>
</div>

<audio autoplay loop>
    <source src="song.mp3" type="audio/mpeg">
</audio>

<script>

// Anniversary Date
let startDate = new Date("2023-05-31");

function updateCounter(){
    let today = new Date();
    let diff = today - startDate;

    let days = Math.floor(diff / (1000*60*60*24));

    document.getElementById("days").innerHTML =
    "💕 Together for " + days + " Days 💕";
}

updateCounter();

// Floating Hearts
function createHeart(){
    const heart = document.createElement("div");

    heart.classList.add("heart");
    heart.innerHTML = "❤️";

    heart.style.left = Math.random()*100 + "vw";
    heart.style.animationDuration =
    (Math.random()*4 + 4) + "s";

    document.body.appendChild(heart);

    setTimeout(()=>{
        heart.remove();
    },8000);
}

setInterval(createHeart,250);

</script>

</body>
</html>
