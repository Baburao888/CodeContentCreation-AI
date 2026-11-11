
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Smart Content Creation</title>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Segoe UI', sans-serif;
}

body {
    background: #090E24;
    color: white;
}

/* Navbar */
nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 22px 8%;
    background: #111735;
    border-bottom: 1px solid #292F58;
}

.logo {
    font-size: 25px;
    font-weight: bold;
    color: #A855F7;
}

.logo span {
    color: #00D4FF;
}

nav a {
    color: #D5D9F0;
    text-decoration: none;
    margin-left: 25px;
}

/* Hero section */
.hero {
    text-align: center;
    padding: 90px 20px;
    background: linear-gradient(
        120deg,
        #171B45,
        #422477,
        #102D52
    );
}

.hero h1 {
    font-size: 48px;
    margin-bottom: 20px;
}

.hero h1 span {
    color: #00D4FF;
}

.hero p {
    color: #D0D5ED;
    font-size: 18px;
    margin-bottom: 30px;
}

.btn {
    padding: 14px 30px;
    border: none;
    border-radius: 30px;
    background: linear-gradient(
        90deg,
        #7047EB,
        #00BFEF
    );
    color: white;
    font-size: 16px;
    cursor: pointer;
}

/* Main content */
.container {
    padding: 60px 8%;
}

.heading {
    text-align: center;
    margin-bottom: 40px;
}

.heading h2 {
    font-size: 32px;
    color: #A855F7;
    margin-bottom: 12px;
}

/* Cards */
.cards {
    display: grid;
    grid-template-columns: repeat(
        auto-fit,
        minmax(220px, 1fr)
    );
    gap: 25px;
}

.card {
    background: #171F40;
    padding: 30px;
    border-radius: 18px;
    border: 1px solid #303967;
    transition: 0.3s;
}

.card:hover {
    transform: translateY(-8px);
    border-color: #A855F7;
    box-shadow: 0 10px 30px #7047EB30;
}

.card .icon {
    font-size: 38px;
    margin-bottom: 18px;
}

.card h3 {
    margin-bottom: 12px;
    color: #00D4FF;
}

.card p {
    color: #B9C1DD;
    line-height: 1.6;
}

/* Content generator */
.generator {
    margin-top: 70px;
    padding: 40px;
    background: linear-gradient(
        135deg,
        #171B45,
        #292054
    );
    border-radius: 20px;
    border: 1px solid #7047EB;
}

.generator h2 {
    color: #00D4FF;
    margin-bottom: 25px;
}

textarea {
    width: 100%;
    height: 130px;
    padding: 18px;
    border-radius: 12px;
    background: #090E24;
    border: 1px solid #7047EB;
    color: white;
    font-size: 16px;
    outline: none;
    resize: vertical;
    margin-bottom: 20px;
}

textarea:focus {
    border-color: #00D4FF;
}

.result {
    margin-top: 25px;
    padding: 20px;
    background: #102D35;
    border-radius: 12px;
    color: #00D69F;
    display: none;
}

/* Footer */
footer {
    text-align: center;
    padding: 30px;
    background: #111735;
    color: #9BA5C7;
    margin-top: 70px;
}

@media(max-width: 600px) {
    .hero h1 {
        font-size: 32px;
    }

    nav {
        flex-direction: column;
        gap: 15px;
    }

    nav a {
        margin: 8px;
    }

    .generator {
        padding: 22px;
    }
}
</style>
</head>

<body>

<nav>
    <div class="logo">Smart<span>Content AI</span></div>

    <div>
        <a href="#">Home</a>
        <a href="#features">Features</a>
        <a href="#create">Create</a>
    </div>
</nav>

<section class="hero">
    <h1>Create Smarter Content with <span>AI</span></h1>

    <p>
        Generate creative, engaging and intelligent
        content using Artificial Intelligence.
    </p>

    <a href="#create">
        <button class="btn">Start Creating</button>
    </a>
</section>

<section class="container" id="features">

    <div class="heading">
        <h2>Our Smart Features</h2>
        <p>Everything you need to create amazing content.</p>
    </div>

    <div class="cards">

        <div class="card">
            <div class="icon">🤖</div>
            <h3>AI Content Generation</h3>
            <p>Generate creative content automatically
            using AI technology.</p>
        </div>

        <div class="card">
            <div class="icon">✍️</div>
            <h3>Blog Writing</h3>
            <p>Create professional blogs and articles
            within seconds.</p>
        </div>

        <div class="card">
            <div class="icon">📱</div>
            <h3>Social Media Content</h3>
            <p>Generate attractive captions and
            social media posts.</p>
        </div>

        <div class="card">
            <div class="icon">⚡</div>
            <h3>Smart Suggestions</h3>
            <p>Get intelligent suggestions to improve
            your content quality.</p>
        </div>

    </div>

    <div class="generator" id="create">

        <h2>✨ Create Your Content</h2>

        <textarea id="prompt"
        placeholder="Enter your content idea here..."></textarea>

        <button class="btn" onclick="generateContent()">
            Generate Content
        </button>

        <div class="result" id="result"></div>

    </div>

</section>

<footer>
    © 2026 Smart Content Creation | Powered by AI
</footer>

<script>
function generateContent() {

    let prompt = document.getElementById("prompt").value;

    let result = document.getElementById("result");

    if(prompt.trim() === "") {
        alert("Please enter your content idea!");
        return;
    }

    result.style.display = "block";

    result.innerHTML =
        "Your idea: " + prompt +
        "<br><br>Content generation interface is ready! Connect your AI API to generate real content.";
}
</script>

</body>
</html>
