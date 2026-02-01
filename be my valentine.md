<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Be My Valentine? 💘</title>

<style>
body {
height: 100vh;
margin: 0;
font-family: Arial, sans-serif;
background: #ffe6eb;
display: flex;
flex-direction: column;
align-items: center;
justify-content: center;
overflow: hidden;
}

h1 {
margin-bottom: 40px;
font-size: 2.5rem;
}

button {
padding: 15px 30px;
font-size: 1.2rem;
border: none;
border-radius: 10px;
cursor: pointer;
position: absolute;
}

#yes {
background-color: #ff4d6d;
color: white;
left: 40%;
top: 55%;
}

#no {
background-color: #ccc;
left: 55%;
top: 55%;
transition: left 0.2s ease, top 0.2s ease;
}
</style>
</head>
<body>

<h1>Will you be my Valentine? 💖</h1>

<button id="yes" onclick="yesClicked()">Yes 💘</button>
<button id="no">No 😅</button>

<script>
const noButton = document.getElementById("no");

noButton.addEventListener("mouseenter", runAway);

function runAway() {
const maxX = window.innerWidth - noButton.offsetWidth;
const maxY = window.innerHeight - noButton.offsetHeight;

const randomX = Math.random() * maxX;
const randomY = Math.random() * maxY;

noButton.style.left = randomX + "px";
noButton.style.top = randomY + "px";
}

function yesClicked() {
document.body.innerHTML = `
<h1>YAY!!! 💕🥰</h1>
<p>You’re officially my Valentine 💘</p>
`;
}
</script>

</body>
</html>
