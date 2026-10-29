
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Serenity Wellness | Yoga & Meditation</title>

    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600;700&family=Poppins:wght@300;400;500;600&display=swap" rel="stylesheet">

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Poppins', sans-serif;
            background: #f8faf6;
            color: #34483d;
            line-height: 1.7;
        }

        h1, h2, h3 {
            font-family: 'Playfair Display', serif;
        }

        header {
            background: #e8f0e7;
            padding: 18px 7%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 15px;
            position: sticky;
            top: 0;
            z-index: 100;
        }

        .logo {
            font-size: 27px;
            font-weight: 700;
            color: #52745d;
        }

        nav {
            display: flex;
            gap: 20px;
            flex-wrap: wrap;
        }

        nav a {
            text-decoration: none;
            color: #34483d;
            font-size: 13px;
        }

        nav a:hover {
            color: #799c7b;
        }

        .hero {
            min-height: 580px;
            padding: 80px 8%;
            display: flex;
            align-items: center;
            background:
                linear-gradient(90deg, #f1f5ed 10%, #f1f5eddd 45%, #f1f5ed20),
                url('https://images.unsplash.com/photo-1544367567-0f2fcb009e0b?auto=format&fit=crop&w=1800&q=85')
                center/cover;
        }

        .hero-content {
            max-width: 560px;
        }

        .hero h1 {
            font-size: clamp(38px, 5vw, 64px);
            line-height: 1.2;
            color: #345742;
            margin-bottom: 20px;
        }

        .hero p {
            margin-bottom: 25px;
            color: #526658;
        }

        .btn {
            display: inline-block;
            padding: 12px 24px;
            background: #64866a;
            color: white;
            text-decoration: none;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font: inherit;
            transition: 0.3s;
        }

        .btn:hover {
            background: #42654a;
        }

        section {
            padding: 75px 8%;
            scroll-margin-top: 90px;
        }

        .section-title {
            font-size: 37px;
            color: #345742;
            margin-bottom: 10px;
        }

        .subtitle {
            color: #778579;
            margin-bottom: 35px;
        }

        .center {
            text-align: center;
        }

        .grid {
            display: grid;
            grid-template-columns: repeat(3, minmax(0, 1fr));
            gap: 25px;
            margin-top: 30px;
        }

        .card {
            background: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 5px 22px #3457420d;
            transition: transform 0.3s;
        }

        .card:hover {
            transform: translateY(-5px);
        }

        .card img {
            width: 100%;
            height: 235px;
            object-fit: cover;
            display: block;
        }

        .card-content {
            padding: 22px;
        }

        .card h3 {
            font-size: 22px;
            margin-bottom: 9px;
            color: #42654a;
        }

        .card p {
            font-size: 14px;
            color: #68776b;
        }

        .yoga {
            background: #edf3e9;
        }

        .meditation {
            background: #e5eeeb;
        }

        .instructors .card img {
            height: 280px;
        }

        .schedule-wrapper {
            overflow-x: auto;
            border-radius: 10px;
            box-shadow: 0 5px 22px #3457420d;
        }

        table {
            width: 100%;
            border-collapse: collapse;
            background: white;
            min-width: 600px;
        }

        th, td {
            text-align: left;
            padding: 16px;
            border-bottom: 1px solid #e1e9df;
        }

        th {
            background: #52745d;
            color: white;
        }

        tr:hover td {
            background: #f0f6ed;
        }

        .plans {
            background: #edf3e9;
        }

        .plan-card {
            padding: 30px 24px;
            text-align: center;
            border: 1px solid #d9e4d5;
        }

        .plan-card.featured {
            border: 2px solid #64866a;
        }

        .price {
            font-size: 34px;
            font-weight: 700;
            color: #52745d;
            margin: 15px 0;
        }

        .plan-card ul {
            list-style: none;
            margin: 22px 0;
        }

        .plan-card li {
            margin: 10px 0;
            font-size: 14px;
        }

        .articles .card img {
            height: 210px;
        }

        .article-tag {
            display: inline-block;
            color: #64866a;
            font-size: 12px;
            font-weight: 600;
            margin-bottom: 8px;
        }

        .newsletter {
            background: #52745d;
            color: white;
            text-align: center;
        }

        .newsletter h2 {
            color: white;
        }

        .newsletter p {
            margin: 12px 0 22px;
        }

        .newsletter form {
            display: flex;
            gap: 10px;
            max-width: 500px;
            margin: auto;
        }

        .newsletter input {
            flex: 1;
            min-width: 0;
            padding: 13px;
            border: none;
            border-radius: 5px;
            font: inherit;
        }

        .newsletter button {
            background: #e2ecdd;
            color: #345742;
        }

        footer {
            background: #283f32;
            color: #e3ebe2;
            padding: 30px 8%;
            text-align: center;
        }

        footer a {
            color: #d6e7d0;
            text-decoration: none;
        }

        .message {
            margin-top: 15px;
            font-size: 14px;
        }

        @media (max-width: 900px) {
            .grid {
                grid-template-columns: repeat(2, minmax(0, 1fr));
            }

            header {
                padding: 16px 5%;
            }

            section {
                padding: 60px 6%;
            }
        }

        @media (max-width: 600px) {
            header {
                flex-direction: column;
                align-items: flex-start;
            }

            nav {
                gap: 10px 15px;
            }

            nav a {
                font-size: 12px;
            }

            .hero {
                min-height: 470px;
                padding: 55px 6%;
                background-position: 60% center;
            }

            .hero h1 {
                font-size: 39px;
            }

            .grid {
                grid-template-columns: 1fr;
            }

            .section-title {
                font-size: 30px;
            }

            .newsletter form {
                flex-direction: column;
            }

            .card img {
                height: 250px;
            }
        }
    </style>
</head>

<body>

<!-- NAVIGATION -->
<header>
    <div class="logo">Serenity Wellness</div>

    <nav>
        <a href="#home">Home</a>
        <a href="#yoga">Yoga</a>
        <a href="#meditation">Meditation</a>
        <a href="#instructors">Instructors</a>
        <a href="#schedule">Classes</a>
        <a href="#plans">Membership</a>
        <a href="#articles">Articles</a>
    </nav>
</header>

<!-- HERO SECTION -->
<section class="hero" id="home">
    <div class="hero-content">
        <h1>Find Your Balance, Find Yourself</h1>
        <p>
            Create space for calm, build healthy habits, and reconnect
            with your body and mind through yoga and meditation.
        </p>
        <a href="#schedule" class="btn">Explore Our Classes</a>
    </div>
</section>

<!-- YOGA POSES -->
<section class="yoga" id="yoga">
    <div class="center">
        <h2 class="section-title">Explore Yoga</h2>
        <p class="subtitle">Move mindfully. Breathe deeply. Grow stronger.</p>
    </div>

    <div class="grid">
        <article class="card">
            <img src="https://images.unsplash.com/photo-1506126613408-eca07ce68773?auto=format&fit=crop&w=900&q=85"
                 alt="Person practicing yoga">
            <div class="card-content">
                <h3>Mountain Pose</h3>
                <p><strong>Level:</strong> Beginner</p>
                <p>A foundational standing posture for practicing alignment, balance, and awareness.</p>
            </div>
        </article>

        <article class="card">
            <img src="https://images.unsplash.com/photo-1545389336-cf090694435e?auto=format&fit=crop&w=900&q=85"
                 alt="Yoga stretching practice">
            <div class="card-content">
                <h3>Tree Pose</h3>
                <p><strong>Level:</strong> Beginner to Intermediate</p>
                <p>A balancing posture that develops concentration, stability, and body awareness.</p>
            </div>
        </article>

        <article class="card">
            <img src="https://images.unsplash.com/photo-1599447421416-3414500d18a5?auto=format&fit=crop&w=900&q=85"
                 alt="Yoga session in a peaceful space">
            <div class="card-content">
                <h3>Child's Pose</h3>
                <p><strong>Level:</strong> Gentle</p>
                <p>A resting posture often used to pause, relax, and reconnect with the breath.</p>
            </div>
        </article>
    </div>
</section>

<!-- MEDITATION TECHNIQUES -->
<section class="meditation" id="meditation">
    <div class="center">
        <h2 class="section-title">Meditation & Mindfulness</h2>
        <p class="subtitle">Small moments of stillness can make room for awareness.</p>
    </div>

    <div class="grid">
        <article class="card">
            <img src="https://images.unsplash.com/photo-1470252649378-9c29740c9fa8?auto=format&fit=crop&w=900&q=85"
                 alt="Peaceful sunrise in nature">
            <div class="card-content">
                <h3>Mindful Breathing</h3>
                <p>Spend 5 minutes noticing your natural breath without trying to change it. Gently return your attention whenever it wanders.</p>
            </div>
        </article>

        <article class="card">
            <img src="https://images.unsplash.com/photo-1500530855697-b586d89ba3ee?auto=format&fit=crop&w=900&q=85"
                 alt="Calm natural landscape">
            <div class="card-content">
                <h3>Body Scan</h3>
                <p>Bring attention gradually to different parts of your body, noticing sensations without judging them.</p>
            </div>
        </article>

        <article class="card">
            <img src="https://images.unsplash.com/photo-1441974231531-c6227db76b6e?auto=format&fit=crop&w=900&q=85"
                 alt="Quiet forest environment">
            <div class="card-content">
                <h3>Nature Meditation</h3>
                <p>Notice the sounds, sights, and sensations around you. Let your attention rest in the present moment.</p>
            </div>
        </article>
    </div>
</section>

<!-- INSTRUCTOR PROFILES -->
<section class="instructors" id="instructors">
    <div class="center">
        <h2 class="section-title">Meet Our Instructors</h2>
        <p class="subtitle">Supportive guidance for your wellness journey.</p>
    </div>

    <div class="grid">
        <article class="card">
            <img src="https://images.unsplash.com/photo-1551836022-d5d88e9218df?auto=format&fit=crop&w=900&q=85"
                 alt="Wellness instructor portrait">
            <div class="card-content">
                <h3>Ananya Sharma</h3>
                <p><strong>Yoga Instructor</strong></p>
                <p>Focuses on beginner-friendly movement, posture awareness, and gentle yoga sequences.</p>
            </div>
        </article>

        <article class="card">
            <img src="https://images.unsplash.com/photo-1500648767791-00dcc994a43e?auto=format&fit=crop&w=900&q=85"
                 alt="Meditation instructor portrait">
            <div class="card-content">
                <h3>Arjun Mehta</h3>
                <p><strong>Meditation Guide</strong></p>
                <p>Leads mindfulness sessions and guided relaxation for everyday practice.</p>
            </div>
        </article>

        <article class="card">
            <img src="https://images.unsplash.com/photo-1580489944761-15a19d654956?auto=format&fit=crop&w=900&q=85"
                 alt="Wellness coach portrait">
            <div class="card-content">
                <h3>Meera Rao</h3>
                <p><strong>Wellness Coach</strong></p>
                <p>Encourages sustainable routines, mindful movement, and balanced daily habits.</p>
            </div>
        </article>
    </div>
</section>

<!-- CLASS SCHEDULE -->
<section class="yoga" id="schedule">
    <div class="center">
        <h2 class="section-title">Weekly Class Schedule</h2>
        <p class="subtitle">Choose a session that works for you.</p>
    </div>

    <div style="overflow-x:auto;">
        <table style="width:100%;border-collapse:collapse;background:white;min-width:600px;">
            <thead>
                <tr style="background:#52745d;color:white;">
                    <th style="padding:15px;text-align:left;">Class</th>
                    <th style="padding:15px;text-align:left;">Day</th>
                    <th style="padding:15px;text-align:left;">Time</th>
                    <th style="padding:15px;text-align:left;">Instructor</th>
                    <th style="padding:15px;text-align:left;">Level</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td style="padding:15px;border-bottom:1px solid #ddd;">Gentle Yoga</td>
                    <td style="padding:15px;border-bottom:1px solid #ddd;">Monday</td>
                    <td style="padding:15px;border-bottom:1px solid #ddd;">7:00 AM</td>
                    <td style="padding:15px;border-bottom:1px solid #ddd;">Ananya</td>
                    <td style="padding:15px;border-bottom:1px solid #ddd;">Beginner</td>
                </tr>
                <tr>
                    <td style="padding:15px;border-bottom:1px solid #ddd;">Mindful Meditation</td>
                    <td style="padding:15px;border-bottom:1px solid #ddd;">Tuesday</td>
                    <td style="padding:15px;border-bottom:1px solid #ddd;">6:00 PM</td>
                    <td style="padding:15px;border-bottom:1px solid #ddd;">Arjun</td>
                    <td style="padding:15px;border-bottom:1px solid #ddd;">All levels</td>
                </tr>
                <tr>
                    <td style="padding:15px;border-bottom:1px solid #ddd;">Flow Yoga</td>
                    <td style="padding:15px;border-bottom:1px solid #ddd;">Wednesday</td>
                    <td style="padding:15px;border-bottom:1px solid #ddd;">7:30 AM</td>
                    <td style="padding:15px;border-bottom:1px solid #ddd;">Ananya</td>
                    <td style="padding:15px;border-bottom:1px solid #ddd;">Intermediate</td>
                </tr>
                <tr>
                    <td style="padding:15px;border-bottom:1px solid #ddd;">Body Scan Meditation</td>
                    <td style="padding:15px;border-bottom:1px solid #ddd;">Friday</td>
                    <td style="padding:15px;border-bottom:1px solid #ddd;">6:30 PM</td>
                    <td style="padding:15px;border-bottom:1px solid #ddd;">Arjun</td>
                    <td style="padding:15px;border-bottom:1px solid #ddd;">All levels</td>
                </tr>
                <tr>
                    <td style="padding:15px;">Weekend Wellness</td>
                    <td style="padding:15px;">Saturday</td>
                    <td style="padding:15px;">9:00 AM</td>
                    <td style="padding:15px;">Meera</td>
                    <td style="padding:15px;">All levels</td>
                </tr>
            </tbody>
        </table>
    </div>
</section>

<!-- MEMBERSHIP PLANS -->
<section class="plans" id="plans">
    <div class="center">
        <h2 class="section-title">Membership Plans</h2>
        <p class="subtitle">Find a plan that fits your routine.</p>
    </div>

    <div class="grid">
        <article class="card plan-card">
            <h3>Starter</h3>
            <p class="price">₹499</p>
            <p>Per month</p>
            <ul>
                <li>4 yoga classes</li>
                <li>2 guided meditation sessions</li>
                <li>Beginner wellness articles</li>
            </ul>
            <a href="#newsletter" class="btn">Choose Starter</a>
        </article>

        <article class="card plan-card featured">
            <h3>Balance</h3>
            <p class="price">₹999</p>
            <p>Per month</p>
            <ul>
                <li>Unlimited regular group classes</li>
                <li>Weekly meditation sessions</li>
                <li>Wellness workshop access</li>
            </ul>
            <a href="#newsletter" class="btn">Choose Balance</a>
        </article>

        <article class="card plan-card">
            <h3>Premium</h3>
            <p class="price">₹1,999</p>
            <p>Per month</p>
            <ul>
                <li>All regular group classes</li>
                <li>One private session monthly</li>
                <li>Personal wellness consultation</li>
            </ul>
            <a href="#newsletter" class="btn">Choose Premium</a>
        </article>
    </div>
</section>

<!-- WELLNESS ARTICLES -->
<section class="articles" id="articles">
    <div class="center">
        <h2 class="section-title">Wellness Journal</h2>
        <p class="subtitle">Simple ideas for a more mindful lifestyle.</p>
    </div>

    <div class="grid">
        <article class="card">
            <img src="https://images.unsplash.com/photo-1506126613408-eca07ce68773?auto=format&fit=crop&w=900&q=85"
                 alt="Morning mindfulness practice">
            <div class="card-content">
                <span class="article-tag">MINDFULNESS</span>
                <h3>Building a Morning Ritual</h3>
                <p>Start small with a few quiet minutes, gentle movement, and a realistic routine you can maintain.</p>
            </div>
        </article>

        <article class="card">
            <img src="https://images.unsplash.com/photo-1544367567-0f2fcb009e0b?auto=format&fit=crop&w=900&q=85"
                 alt="Yoga practice">
            <div class="card-content">
                <span class="article-tag">YOGA</span>
                <h3>Yoga for Beginners</h3>
                <p>Learn how to begin with comfortable poses, modifications, and attention to your body's limits.</p>
            </div>
        </article>

        <article class="card">
            <img src="https://images.unsplash.com/photo-1470252649378-9c29740c9fa8?auto=format&fit=crop&w=900&q=85"
                 alt="Peaceful sunrise">
            <div class="card-content">
                <span class="article-tag">LIFESTYLE</span>
                <h3>Making Space for Rest</h3>
                <p>Explore simple ways to build restful breaks and moments of calm into a busy day.</p>
            </div>
        </article>
    </div>
</section>

<!-- NEWSLETTER -->
<sectio
