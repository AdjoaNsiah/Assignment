<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>NanaAdjoa</title>
    <link rel="stylesheet" href="adjoa.css"> 
    <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.4.0"></script>
</head>
<body onload="checkAccess()">


    <button class="toggle-btn" onclick="toggleDarkMode()">Toggle Dark Mode</button>


    <label for="fontSelector">Change Font:</label>
    <select id="fontSelector" onchange="changeFont()">
        <option value="Comic Sans MS">Comic Sans</option>
        <option value="Georgia">Georgia</option>
        <option value="Arial">Arial</option>
    </select>


    <audio id="background-music" loop autoplay>
        <source src="coldrain-coexist-official-music-video-128-ytshorts.savetube.me.mp3" type="audio/mp3">
        Your browser does not support the audio element.
    </audio>

    <h1 class="hey">👋 INTRO</h1>
    <p>Hey there! I’m <strong>Nana Adjoa Nsiah-Asare</strong>, but you can call me <strong>Adjoa</strong>. I’m an <strong>18-year-old</strong> computer engineering student at <strong>Kwame Nkrumah University of Science and Technology (KNUST)</strong>.</p>
    <p>💭 <em>Why computer engineering?</em> Honestly… I don’t know! I wanted to be a <strong>dentist</strong>, but my dad said no, so here I am—figuring things out as I go!</p>
    <p>🎓 I’m a proud graduate of <strong>Wesley Girls' High School, Cape Coast</strong>.</p>

    <h2 class="hey">🎸 STUFF I'M INTO</h2>
    <p>🎨 <strong>Art & Calligraphy</strong> – I love to <strong>draw</strong> and practice <strong>calligraphy</strong>, which earned me a little *"celebrity status"* back in Wesley Girls'. There's something magical about turning letters into art.</p>
    <p>🎵 <strong>Rock Music Enthusiast</strong> – My go-to study and work music? <strong>Rock.</strong> The <strong>Japanese rock scene</strong> owns my soul, especially bands like <strong>Coldrain</strong> and <strong>ONE OK ROCK</strong>. If you see me vibing with headphones in, assume it’s one of their songs.</p>
    <p>🎮 <strong>Gamer Life</strong> – My latest obsession? <strong>Genshin Impact</strong>, an action-adventure RPG with stunning visuals, cool characters, and an open world that I can’t stop exploring.</p>
    <p>🍤 <strong>Foodie at Heart</strong> – If I had to live on one dish forever, it’d be <strong>shrimp fried rice</strong>. Simple but <em>*chef’s kiss*</em> perfection.</p>

    <h3 class="hey">🕹 HOBBIES</h3>
    <p>When I’m not buried in engineering coursework, you’ll probably find me <strong>grinding in Genshin Impact</strong>, practicing <strong>calligraphy</strong>, or sketching whatever inspires me.</p>
    <p>🤟 <strong>Sign Language</strong> – Lately, my interest in <strong>sign language</strong> has been making a comeback! Every now and then, I practice a few words and sentences—it’s a beautiful way to communicate, and I’d love to get better at it.</p>

    <h3 class="hey">🎵 My Playlist</h3>
    <p>Here's a playlist of some of my favorite songs!</p>
    <iframe style="border-radius:12px" src="https://open.spotify.com/embed/playlist/37i9dQZF1EIYhQAQ3RB0gT?utm_source=generator" width="100%" height="352" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>

    <h3 class="hey">🌐 Check This Out</h3>
    <p>If you're into Genshin Impact, check out the official site:</p>
    <a href="https://genshin.hoyoverse.com/en/" target="_blank">Visit Genshin Impact's Official Website</a>

    <script>
    
        function checkAccess() {
            const correctCode = "wriothesley"; 
            let userCode = prompt("Enter the teacher's access code:");

            if (userCode === correctCode) {
                alert("Access Granted! Welcome, Teacher.");
                startConfetti();
            } else {
                alert("Access Denied! Redirecting...");
                window.location.href = "https://www.google.com"; 
            }
        }

        function startConfetti() {
            const duration = 3 * 1000; 
            const end = Date.now() + duration;

            (function frame() {
                confetti({
                    particleCount: 5,
                    spread: 160,
                    origin: { y: 0.6 }
                });

                if (Date.now() < end) {
                    requestAnimationFrame(frame);
                }
            })();
        }

        function toggleDarkMode() {
            document.body.classList.toggle("dark-mode");
        }

        function changeFont() {
            const selectedFont = document.getElementById("fontSelector").value;
            document.body.style.fontFamily = selectedFont;
        }
    </script>

</body>
</html>
