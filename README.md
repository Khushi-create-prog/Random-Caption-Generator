# Random-Caption-Generator
# HTML CODE

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Random caption Generator</title>
    <link rel="stylesheet" href="k.css">
</head>
<body>
    <div class="container">
        <h1>Random caption Generator</h1>
        <blockquote id="caption">"Click the button to generate a caption!"</blockquote>
        <button id="new-caption">New caption</button>
    </div>
    <script src="main.js"></script>
</body>
</html>

# CSS CODE

body {
    font-family: Arial, sans-serif;
    background-color: rgb(204, 189, 189);
    margin: 0;
    padding: 0;
}

.container {
    text-align: center;
    background: rgb(190, 177, 177);
    padding: 20px;
}

h1 {
    color: rgb(34, 31, 31);
    background-color: brown;
    font-weight: bold;
    margin: 4cm 0 2cm 0;
    padding: 10px 0;
    text-align: center;
}

blockquote {
    font-size: 28px;
    margin: 0 0 2cm 0;
    color: #8b5656;
    height: 4.5em;
    overflow: hidden;
}

button {
    display: block;
    margin: 0 auto;
    padding: 10px 20px;
    font-size: 1em;
    border: none;
    border-radius: 5px;
    background-color: #2e4b69;
    color: rgb(240, 227, 227);
    cursor: pointer;
}

button:hover {
    background-color: #0056b3;
}

# JS CODE 

const caption = [
    "Life is a journey, not a destination.",
     "Stay positive, work hard, make it happen.",
     "Good things come to those who hustle.",
     "Dream big. Work hard. Stay focused.",
     "Believe you can and you're halfway there.",
     "Do more of what makes you happy.",
     "Don't wait for opportunity. Create it.",
     "Success is the sum of small efforts.",
     "It always seems impossible until it’s done.",
     "You are capable of amazing things."
];

const captionElement = document.getElementById('caption');
const button = document.getElementById('new-caption');

button.addEventListener('click', () => {
    const randomIndex = Math.floor(Math.random() * caption.length);
    captionElement.textContent = caption[randomIndex];
});

