# javya2025
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Just a Little Wait 💕</title>

<style>
body {
    height: 100vh;
    margin: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    background: linear-gradient(135deg, #ffd6e8, #ffeef5);
    font-family: 'Poppins', sans-serif;
    text-align: center;
}

.container {
    background: white;
    padding: 40px 50px;
    border-radius: 25px;
    box-shadow: 0 20px 40px rgba(0,0,0,0.15);
}

h1 {
    font-size: 2.5rem;
    color: #ff4d88;
    margin-bottom: 20px;
}

#timer {
    font-size: 3rem;
    font-weight: bold;
    color: #ff0066;
}

#message {
    display: none;
}

a {
    display: inline-block;
    margin-top: 20px;
    font-size: 1.5rem;
    text-decoration: none;
    color: white;
    background: #ff4d88;
    padding: 15px 30px;
    border-radius: 50px;
    transition: transform 0.2s;
}

a:hover {
    transform: scale(1.05);
}
</style>
</head>

<body>

<div class="container">
    <h1>Something special is waiting for you 💖</h1>
    <div id="timer"></div>

    <div id="message">
        <h1>It’s Time 💕</h1>
        <a href="https://javya2025.mobirisesite.com/" target="_blank">
            Open Your Surprise 🎁
        </a>
    </div>
</div>

<script>
function updateTimer() {
    const now = new Date();

    // Set tonight 12:00 AM
    const midnight = new Date();
    midnight.setHours(24, 0, 0, 0);

    const diff = midnight - now;

    if (diff <= 0) {
        document.getElementById("timer").style.display = "none";
        document.getElementById("message").style.display = "block";
        return;
    }

    const hours = Math.floor(diff / (1000 * 60 * 60));
    const minutes = Math.floor((diff / (1000 * 60)) % 60);
    const seconds = Math.floor((diff / 1000) % 60);

    document.getElementById("timer").innerHTML =
        `${hours}h ${minutes}m ${seconds}s`;
}

setInterval(updateTimer, 1000);
updateTimer();
</script>

</body>
</html>
