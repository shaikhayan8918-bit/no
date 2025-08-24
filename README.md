# no
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rule-Based Trading System</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700;900&display=swap" rel="stylesheet">
    <style>
        /* CSS Variables for Easy Customization */
        :root {
            --bg-color: #0F172A; /* Dark Slate Blue */
            --primary-text-color: #E2E8F0; /* Light Slate Gray */
            --secondary-text-color: #94A3B8; /* Medium Slate Gray */
            --accent-color: #38BDF8; /* Sky Blue */
            --accent-hover-color: #0EA5E9; /* Brighter Sky Blue */
            --container-bg-color: #1E293B; /* Lighter Slate */
        }

        /* General Body & Reset Styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', sans-serif;
            background-color: var(--bg-color);
            color: var(--primary-text-color);
            line-height: 1.7;
        }

        /* Container & Section Styling */
        .container {
            max-width: 800px;
            margin: 0 auto;
            padding: 0 20px;
        }

        section {
            padding: 80px 0;
            text-align: center;
        }

        section:not(:first-child) {
            border-top: 1px solid var(--container-bg-color);
        }

        /* Typography */
        h1, h2, h3 {
            line-height: 1.3;
            margin-bottom: 20px;
        }

        h1 {
            font-size: 3rem;
            font-weight: 900;
            text-shadow: 0 0 15px rgba(56, 189, 248, 0.3);
        }

        h2 {
            font-size: 2.25rem;
            font-weight: 700;
        }

        h3 {
            font-size: 1.5rem;
            color: var(--primary-text-color);
        }
        
        h4 {
            font-size: 1.2rem;
            color: var(--accent-color);
            margin-bottom: 10px;
        }

        p {
            font-size: 1.1rem;
            color: var(--secondary-text-color);
            margin-bottom: 20px;
            max-width: 700px;
            margin-left: auto;
            margin-right: auto;
        }

        .accent-text {
            color: var(--accent-color);
            font-weight: 700;
        }

        /* Buttons */
        .cta-button {
            display: inline-block;
            background-color: var(--accent-color);
            color: var(--bg-color);
            font-size: 1.2rem;
            font-weight: 700;
            text-decoration: none;
            padding: 18px 36px;
            border-radius: 8px;
            margin-top: 20px;
            margin-bottom: 10px;
            border: none;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 5px 20px rgba(56, 189, 248, 0.2);
        }

        .cta-button:hover {
            background-color: var(--accent-hover-color);
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(56, 189, 248, 0.3);
        }
        
        /* Hero Section */
        .hero {
            padding-top: 60px;
            padding-bottom: 60px;
        }

        .hero h1 {
            margin-bottom: 25px;
        }

        .hero p.subtitle {
            font-size: 1.25rem;
            color: var(--primary-text-color);
            font-weight: 600;
            max-width: 650px;
        }

        .video-placeholder {
            width: 100%;
            aspect-ratio: 16 / 9;
            background-color: #000;
            border: 2px solid var(--container-bg-color);
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 40px auto;
            max-width: 700px;
        }
        
        .video-placeholder .play-button {
            width: 80px;
            height: 80px;
            background-color: rgba(56, 189, 248, 0.8);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            transition: transform 0.2s ease;
        }

        .video-placeholder .play-button:hover {
            transform: scale(1.1);
        }

        .video-placeholder .play-button::after {
            content: '';
            display: block;
            width: 0;
            height: 0;
            border-top: 15px solid transparent;
            border-bottom: 15px solid transparent;
            border-left: 25px solid #fff;
            margin-left: 5px;
        }

        /* Content Sections */
        .story-quote {
            padding: 30px;
            background-color: var(--container-bg-color);
            border-left: 5px solid var(--accent-color);
            margin: 40px auto;
            text-align: left;
            border-radius: 0 8px 8px 0;
        }

        .story-quote p {
            font-style: italic;
            font-size: 1.25rem;
            font-weight: 600;
            color: var(--primary-text-color);
        }

        ul.feature-list {
            list-style: none;
            text-align: left;
            max-width: 500px;
            margin: 30px auto;
            padding: 0;
        }
        
        ul.feature-list li {
            font-size: 1.1rem;
            padding-left: 35px;
            position: relative;
            margin-bottom: 15px;
        }

        ul.feature-list li::before {
            content: '✓';
            position: absolute;
            left: 0;
            top: 0;
            color: var(--accent-color);
            font-weight: 900;
            font-size: 1.2rem;
        }
        
        /* Problem/Solution Section */
        .problem-solution-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 30px;
            text-align: left;
            margin-top: 50px;
        }

        .problem-card {
            background-color: var(--container-bg-color);
            padding: 30px;
            border-radius: 12px;
            border: 1px solid #334155;
        }

        /* What You Get Section */
        .what-you-get-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            text-align: left;
            margin-top: 50px;
        }

        .get-card {
            background-color: var(--container-bg-color);
            padding: 30px;
            border-radius: 12px;
        }

        .get-card ul {
            list-style: none;
        }
        .get-card li {
            padding-left: 25px;
            position: relative;
            margin-bottom: 10px;
            color: var(--secondary-text-color);
        }
        .get-card li::before {
            content: '→';
            position: absolute;
            left: 0;
            color: var(--accent-color);
        }

        /* Investment Section */
        .investment-box {
            background-color: var(--container-bg-color);
            border: 2px solid var(--accent-color);
            border-radius: 12px;
            padding: 40px;
            max-width: 600px;
            margin: 40px auto;
            box-shadow: 0 0 30px rgba(56, 189, 248, 0.15);
        }

        .price {
            font-size: 3.5rem;
            font-weight: 900;
            color: var(--primary-text-color);
            margin: 10px 0 20px;
        }

        .guarantee {
            font-weight: 600;
            color: var(--primary-text-color);
        }

        /* FAQ Section */
        .faq-item {
            background-color: var(--container-bg-color);
            border-radius: 8px;
            margin-bottom: 15px;
            text-align: left;
        }

        .faq-question {
            width: 100%;
            background: none;
            border: none;
            padding: 20px;
            font-size: 1.2rem;
            font-weight: 600;
            color: var(--primary-text-color);
            cursor: pointer;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .faq-question::after {
            content: '+';
            font-size: 2rem;
            font-weight: 300;
            color: var(--accent-color);
            transition: transform 0.3s ease;
        }

        .faq-question.active::after {
            transform: rotate(45deg);
        }

        .faq-answer {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.3s ease, padding 0.3s ease;
        }

        .faq-answer p {
            padding: 0 20px 20px;
            margin-bottom: 0;
        }

        /* Final CTA */
        .final-cta {
            background-color: var(--container-bg-color);
        }

        /* Responsive Styles */
        @media (max-width: 768px) {
            h1 { font-size: 2.5rem; }
            h2 { font-size: 2rem; }
            .problem-solution-grid { grid-template-columns: 1fr; }
        }

    </style>
</head>
<body>

    <header class="hero">
        <div class="container">
            <h1>STOP Jumping From Strategy to Strategy...</h1>
            <p class="subtitle">Finally Build a Simple, Rule-Based Trading System You Can Trust and Stick With</p>
            <p>Without blowing more accounts, wasting years on complicated indicators, or falling for another guru's empty promises.</p>
            
            <div class="video-placeholder" title="Click to play video">
                <div class="play-button"></div>
            </div>
            
            <a href="#call" class="cta-button">BOOK YOUR FREE STRATEGY CALL</a>
        </div>
    </header>

    <main>
        <section>
            <div class="container">
                <h2>You're Sick of Being the "Eternal Student" Who Never Actually Makes Money Trading</h2>
                <p>Let me guess...</p>
                <p>You've bought the courses. Downloaded the indicators. Joined the Discord servers. You've tried scalping, swing trading, news trading, and every "proven system" some guru promised would change your life.</p>
                <p>But here you are... STILL bouncing from strategy to strategy like a ping pong ball. Still losing money. Still blowing accounts. Still wondering if you're just not cut out for this.</p>
                <p class="accent-text">The worst part? Every time you switch systems, that little voice in your head gets louder: "Maybe I'm just not disciplined enough. Maybe I'm the problem."</p>
                <p>But here's the truth nobody wants to tell you... <span class="accent-text">It's NOT your fault.</span> The problem isn't you. It's the overcomplicated garbage you've been fed by affiliate-pushing "mentors" who make more money selling courses than they ever did trading.</p>
            </div>
        </section>

        <section>
            <div class="container">
                <h2>The Day I Almost Quit Trading Forever</h2>
                <p>Three years ago, I was exactly where you are right now. I'd spent $12,000 on courses, signals, and funded account challenges. My desktop looked like a Christmas tree with indicators. RSI, MACD, Bollinger Bands, Fibonacci retracements... you name it, I had it cluttering my charts.</p>
                <p>I was waking up at 4 AM (because some guru said "real traders sacrifice sleep"), chugging coffee, and staring at screens until my eyes burned. The result? I blew seven funded accounts in 18 months. My wife started giving me those looks. You know the ones. The "when are you going to get serious about your life" looks.</p>
                <p>I was about to throw in the towel and accept that trading just wasn't for me... That's when everything changed. I met a prop firm trader who was pulling consistent profits month after month. Nothing flashy. No Lambos on Instagram. Just steady, boring profits.</p>
                <p class="accent-text">His secret? Price action only. Simple rules. Zero indicators.</p>
                <p>When I saw his charts, I laughed. They looked... empty. Just candlesticks and a few lines. "That's it?" I asked.</p>
                <div class="story-quote">
                    <p>He nodded. "Complexity is the enemy of consistency." That sentence changed my trading career.</p>
                </div>
            </div>
        </section>

        <section>
            <div class="container">
                <h2>The Simple Truth About Consistent Trading (That Gurus Don't Want You to Know)</h2>
                <p>Every successful trader I studied had ONE thing in common... <span class="accent-text">They kept it stupidly simple.</span> No rainbow charts. No 47-step morning routines. No complicated algorithms. Just three core elements:</p>
                <ul class="feature-list">
                    <li>Clean price action reading (support, resistance, trends)</li>
                    <li>Fixed risk rules that protect your account NO MATTER WHAT</li>
                    <li>A repeatable routine that fits YOUR lifestyle</li>
                </ul>
                <p>The billion-dollar secret the trading industry doesn't want you to know? <span class="accent-text">Simple beats complex. Every. Single. Time.</span> While other traders are drowning in analysis paralysis, you're taking clear, confident trades based on rules that never change.</p>
            </div>
        </section>

        <section>
            <div class="container">
                <h2>Introducing the Rule-Based Trading System That Finally Makes Trading... Boring</h2>
                <p class="accent-text">(And boring is EXACTLY what you want when it comes to making money)</p>
                <p>This isn't another strategy. It's not a course filled with theory and fluff. It's a simple, step-by-step system that gives you:</p>
                <ul class="feature-list">
                    <li>CLEAR ENTRY RULES that tell you exactly when to trade (no more guessing)</li>
                    <li>BULLETPROOF RISK MANAGEMENT that stops you from ever blowing another account</li>
                    <li>LIFESTYLE-FRIENDLY ROUTINES that work whether you have 30 minutes or 3 hours</li>
                    <li>CONFIDENCE that comes from having a system you actually trust</li>
                </ul>
                <h3>Here's how it works:</h3>
                <p><strong>STEP 1:</strong> Learn to read pure price action (I'll show you the only 3 patterns that matter)<br>
                <strong>STEP 2:</strong> Apply the fixed risk rules that protect your capital (even when you're wrong)<br>
                <strong>STEP 3:</strong> Develop YOUR personal routine that fits your schedule and personality<br>
                <strong>STEP 4:</strong> Trade with confidence knowing your system has your back</p>
                <p class="accent-text" style="font-weight: 700;">No indicators. No complexity. No BS. Just simple rules that work.</p>
            </div>
        </section>

        <section>
            <div class="container">
                <h2>Why Everything Else You've Tried Has Failed You</h2>
                <div class="problem-solution-grid">
                    <div class="problem-card">
                        <h3>Problem #1: Information Overload</h3>
                        <p>Most trading education dumps 500 strategies on you and expects you to "find what works." That's like trying to learn piano by playing every song ever written.</p>
                        <h4>My Solution:</h4>
                        <p>ONE simple approach you can master completely.</p>
                    </div>
                    <div class="problem-card">
                        <h3>Problem #2: Cookie-Cutter Systems</h3>
                        <p>Gurus sell you their exact strategy without considering your personality, schedule, or risk tolerance.</p>
                        <h4>My Solution:</h4>
                        <p>A framework you customize to fit YOUR life.</p>
                    </div>
                    <div class="problem-card">
                        <h3>Problem #3: No Real Risk Management</h3>
                        <p>They teach you how to enter trades but not how to protect your money.</p>
                        <h4>My Solution:</h4>
                        <p>Risk rules so simple a 5-year-old could follow them (and so effective they'll save your account).</p>
                    </div>
                    <div class="problem-card">
                        <h3>Problem #4: Lifestyle Incompatibility</h3>
                        <p>Not everyone can wake up at 4 AM or stare at screens for 12 hours.</p>
                        <h4>My Solution:</h4>
                        <p>Trading routines that work around YOUR schedule, not against it.</p>
                    </div>
                </div>
            </div>
        </section>
        
        <section>
            <div class="container">
                <h2>Here's What You Get When You Work With Me</h2>
                 <div class="what-you-get-grid">
                    <div class="get-card">
                        <h4>THE CORE SYSTEM</h4>
                        <ul>
                            <li>Clean price action methodology (no indicators ever)</li>
                            <li>The only 3 setups you need to know</li>
                            <li>Entry and exit rules that remove all guesswork</li>
                        </ul>
                    </div>
                    <div class="get-card">
                        <h4>BULLETPROOF RISK MANAGEMENT</h4>
                        <ul>
                           <li>Fixed risk percentages that scale with your account</li>
                           <li>Loss recovery protocols that keep you in the game</li>
                           <li>Position sizing rules that prevent catastrophic losses</li>
                        </ul>
                    </div>
                    <div class="get-card">
                        <h4>YOUR PERSONAL TRADING ROUTINE</h4>
                        <ul>
                           <li>Customized schedule that fits your lifestyle</li>
                           <li>Pre-market preparation checklist</li>
                           <li>Post-trade review system for continuous improvement</li>
                        </ul>
                    </div>
                     <div class="get-card">
                        <h4>ONGOING SUPPORT & REFINEMENT</h4>
                        <ul>
                           <li>Direct access to me for questions and guidance</li>
                           <li>System tweaks based on your progress</li>
                           <li>Accountability to keep you on track</li>
                        </ul>
                    </div>
                </div>
                <p style="margin-top: 40px; font-weight: 600;">This isn't about learning "secrets" or "tricks." It's about building a simple, sustainable system you can use for the next 20 years.</p>
            </div>
        </section>

        <section id="call">
            <div class="container">
                <h2>The Investment That Changes Everything</h2>
                <p>You've probably already spent thousands on courses that overcomplicated your trading. You've likely lost even more money jumping from system to system. How much is it worth to finally stop the madness?</p>
                <div class="investment-box">
                    <p>To build ONE system you can trust and stick with? To never blow another account? To trade with confidence instead of constantly second-guessing yourself?</p>
                    <div class="price">$1,997</div>
                    <p class="guarantee">And because I know you might be skeptical, I'm backing this with my 60-day, try-it-risk-free guarantee. If you don't see a dramatic improvement in your consistency and confidence within 60 days, I'll refund every penny. No questions. No hassles.</p>
                </div>
                <a href="#call" class="cta-button">BOOK YOUR FREE STRATEGY CALL NOW</a>
            </div>
        </section>

        <section>
            <div class="container">
                <h2>But Wait... You Probably Have Questions</h2>
                <div class="faq-container">
                    <div class="faq-item">
                        <button class="faq-question">Is this just another strategy that won't work for me?</button>
                        <div class="faq-answer">
                            <p>This isn't a strategy. It's a framework you customize to fit YOUR personality and schedule. The rules are simple enough that you can't mess them up.</p>
                        </div>
                    </div>
                    <div class="faq-item">
                        <button class="faq-question">What if I don't have time to trade full-time?</button>
                        <div class="faq-answer">
                            <p>Perfect. This system is designed for people with real lives. Whether you have 30 minutes or 3 hours, I'll show you how to make it work.</p>
                        </div>
                    </div>
                    <div class="faq-item">
                        <button class="faq-question">I've tried price action before and failed...</button>
                        <div class="faq-answer">
                            <p>You probably tried to learn 47 different patterns. I only teach 3. The ones that actually matter and actually work.</p>
                        </div>
                    </div>
                    <div class="faq-item">
                        <button class="faq-question">What if I blow my account again?</button>
                        <div class="faq-answer">
                            <p>The risk management rules make it virtually impossible to blow your account. You'd have to completely ignore the system to lose everything.</p>
                        </div>
                    </div>
                     <div class="faq-item">
                        <button class="faq-question">How do I know you're not just another guru?</button>
                        <div class="faq-answer">
                            <p>Fair question. I don't promise Lambos or mansions. I don't push affiliate links. I trade the same system I teach, and I'll show you exactly how it works before you invest a dime.</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section class="final-cta">
            <div class="container">
                <h2>The Choice Is Yours</h2>
                <p>You can keep doing what you've been doing... Buying more courses. Trying more strategies. Hoping the next "system" will finally be the one. Or... you can stop the madness TODAY.</p>
                <p class="accent-text" style="font-weight: 700;">The traders who succeed aren't the smartest ones. They're the ones who keep it simple and stick to their rules.</p>
                <a href="#call" class="cta-button">BOOK YOUR FREE STRATEGY CALL</a>
                <p style="font-size: 0.9rem; margin-top: 15px;">On this call, we'll discuss your current trading struggles and see if my rule-based system is a good fit for you. No pressure. No sales pitch. Just an honest conversation about your trading future. Click the button above and let's stop the strategy-hopping madness once and for all.</p>
            </div>
        </section>

    </main>
    
    <script>
        const faqQuestions = document.querySelectorAll('.faq-question');

        faqQuestions.forEach(question => {
            question.addEventListener('click', () => {
                const answer = question.nextElementSibling;
                const questionIsActive = question.classList.contains('active');
                
                // Optional: Close all other open FAQs
                // faqQuestions.forEach(q => {
                //     q.classList.remove('active');
                //     q.nextElementSibling.style.maxHeight = null;
                //     q.nextElementSibling.style.padding = '0 20px';
                // });

                if (!questionIsActive) {
                    question.classList.add('active');
                    answer.style.maxHeight = answer.scrollHeight + 'px';
                    answer.style.padding = '0 20px 20px';
                } else {
                    question.classList.remove('active');
                    answer.style.maxHeight = null;
                    answer.style.padding = '0 20px';
                }
            });
        });
    </script>
</body>
</html>
