<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Francis Mutua - Portfolio</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        header {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            transition: all 0.3s ease;
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 0;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: bold;
            color: #667eea;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            text-decoration: none;
            color: #333;
            font-weight: 500;
            transition: color 0.3s ease;
        }

        .nav-links a:hover {
            color: #667eea;
        }

        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
        }

        .hero-content h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            opacity: 0;
            animation: fadeInUp 1s ease forwards;
        }

        .hero-content p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            opacity: 0;
            animation: fadeInUp 1s ease 0.3s forwards;
        }

        .cta-button {
            display: inline-block;
            padding: 12px 30px;
            background: rgba(255, 255, 255, 0.2);
            color: white;
            text-decoration: none;
            border-radius: 50px;
            border: 2px solid white;
            transition: all 0.3s ease;
            opacity: 0;
            animation: fadeInUp 1s ease 0.6s forwards;
        }

        .cta-button:hover {
            background: white;
            color: #667eea;
            transform: translateY(-2px);
        }

        .section {
            padding: 80px 0;
            background: white;
        }

        .section:nth-child(even) {
            background: #f8f9fa;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: #333;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 50px;
            height: 3px;
            background: #667eea;
            margin: 10px auto;
        }

        .about-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            align-items: center;
        }

        .about-text {
            font-size: 1.1rem;
            line-height: 1.8;
        }

        .about-image {
            text-align: center;
        }

        .profile-placeholder {
            width: 250px;
            height: 250px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 3rem;
            font-weight: bold;
            margin: 0 auto;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
        }

        .education-card {
            background: white;
            padding: 2rem;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            margin-bottom: 2rem;
            border-left: 4px solid #667eea;
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
        }

        .skill-card {
            background: white;
            padding: 1.5rem;
            border-radius: 10px;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease;
        }

        .skill-card:hover {
            transform: translateY(-5px);
        }

        .skill-icon {
            font-size: 2.5rem;
            margin-bottom: 1rem;
        }

        .interests-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1.5rem;
        }

        .interest-item {
            background: #667eea;
            color: white;
            padding: 1.5rem;
            border-radius: 10px;
            text-align: center;
            transition: all 0.3s ease;
        }

        .interest-item:hover {
            background: #764ba2;
            transform: scale(1.05);
        }

        .contact {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            text-align: center;
        }

        .contact .section-title {
            color: white;
        }

        .contact .section-title::after {
            background: white;
        }

        footer {
            background: #333;
            color: white;
            text-align: center;
            padding: 2rem 0;
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @media (max-width: 768px) {
            .hero-content h1 {
                font-size: 2.5rem;
            }
            
            .about-grid {
                grid-template-columns: 1fr;
                text-align: center;
            }
            
            .nav-links {
                display: none;
            }
        }
    </style>
</head>
<body>
    <header>
        <nav class="container">
            <div class="logo">Francis Mutua</div>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#education">Education</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#interests">Interests</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <section id="home" class="hero">
            <div class="hero-content">
                <h1>Francis Mutua</h1>
                <p>Science Graduate | Freelancer | Future Logistics Professional</p>
                <a href="#about" class="cta-button">Learn More About Me</a>
            </div>
        </section>

        <section id="about" class="section">
            <div class="container">
                <h2 class="section-title">About Me</h2>
                <div class="about-grid">
                    <div class="about-text">
                        <p>Hello! I'm Francis Mutua, a passionate and driven individual with a strong academic background and a zest for continuous learning. As the youngest in my family, I've always been motivated to carve my own path and make a meaningful impact.</p>
                        
                        <p>Coming from an average family background, I understand the value of hard work and determination. Throughout my academic journey, I've excelled in various subjects including science, literature, mathematics, and business studies, which has given me a well-rounded perspective on problem-solving and critical thinking.</p>
                        
                        <p>Currently working as a freelancer, I've been building my professional experience since my university days. I'm excited about transitioning into the logistics field, where I believe my analytical skills and business acumen will make a significant contribution.</p>
                    </div>
                    <div class="about-image">
                        <div class="profile-placeholder">FM</div>
                    </div>
                </div>
            </div>
        </section>

        <section id="education" class="section">
            <div class="container">
                <h2 class="section-title">Education</h2>
                <div class="education-card">
                    <h3>Bachelor of Science</h3>
                    <h4>Egerton University</h4>
                    <p><strong>Achievement:</strong> Second-Class Honors, Upper Division</p>
                    <p>During my undergraduate studies, I developed a strong foundation in scientific principles while also nurturing my interests in literature, mathematics, and business studies. This diverse academic exposure has equipped me with analytical thinking skills and a multidisciplinary approach to problem-solving.</p>
                </div>
            </div>
        </section>

        <section id="skills" class="section">
            <div class="container">
                <h2 class="section-title">Core Strengths</h2>
                <div class="skills-grid">
                    <div class="skill-card">
                        <div class="skill-icon">🔬</div>
                        <h3>Science</h3>
                        <p>Strong analytical and research capabilities with a solid foundation in scientific methodology</p>
                    </div>
                    <div class="skill-card">
                        <div class="skill-icon">📚</div>
                        <h3>Literature</h3>
                        <p>Excellent communication and writing skills with a deep appreciation for language and storytelling</p>
                    </div>
                    <div class="skill-card">
                        <div class="skill-icon">📊</div>
                        <h3>Mathematics</h3>
                        <p>Advanced mathematical reasoning and problem-solving abilities for complex calculations</p>
                    </div>
                    <div class="skill-card">
                        <div class="skill-icon">💼</div>
                        <h3>Business Studies</h3>
                        <p>Understanding of business principles, strategy, and commercial operations</p>
                    </div>
                    <div class="skill-card">
                        <div class="skill-icon">💻</div>
                        <h3>Freelancing</h3>
                        <p>Self-motivated professional with experience in independent project management</p>
                    </div>
                    <div class="skill-card">
                        <div class="skill-icon">🚚</div>
                        <h3>Future: Logistics</h3>
                        <p>Preparing to enter the logistics industry with enthusiasm and strategic thinking</p>
                    </div>
                </div>
            </div>
        </section>

        <section id="interests" class="section">
            <div class="container">
                <h2 class="section-title">Personal Interests</h2>
                <div class="interests-grid">
                    <div class="interest-item">
                        <h3>⚽ Manchester City</h3>
                        <p>Passionate supporter of MCFC</p>
                    </div>
                    <div class="interest-item">
                        <h3>♟️ Chess</h3>
                        <p>Learning the art of strategic thinking</p>
                    </div>
                    <div class="interest-item">
                        <h3>🃏 Card Games</h3>
                        <p>Enjoying strategic gameplay</p>
                    </div>
                    <div class="interest-item">
                        <h3>🎮 eFootball</h3>
                        <p>Digital football enthusiast</p>
                    </div>
                </div>
            </div>
        </section>

        <section id="contact" class="section contact">
            <div class="container">
                <h2 class="section-title">Let's Connect</h2>
                <p style="font-size: 1.2rem; margin-bottom: 2rem;">I'm always open to new opportunities and meaningful conversations. Whether you're interested in discussing logistics, business, or just want to talk about Manchester City's latest match, feel free to reach out!</p>
                <a href="mailto:francis.mutua@email.com" class="cta-button">Get In Touch</a>
            </div>
        </section>
    </main>

    <footer>
        <div class="container">
            <p>&copy; 2025 Francis Mutua. All rights reserved.</p>
        </div>
    </footer>

    <script>
        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                target.scrollIntoView({
                    behavior: 'smooth',
                    block: 'start'
                });
            });
        });

        // Header background change on scroll
        window.addEventListener('scroll', function() {
            const header = document.querySelector('header');
            if (window.scrollY > 100) {
                header.style.background = 'rgba(255, 255, 255, 0.98)';
            } else {
                header.style.background = 'rgba(255, 255, 255, 0.95)';
            }
        });

        // Intersection Observer for animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver(function(entries) {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, observerOptions);

        // Observe skill cards and interest items for scroll animations
        document.querySelectorAll('.skill-card, .interest-item, .education-card').forEach(el => {
            el.style.opacity = '0';
            el.style.transform = 'translateY(20px)';
            el.style.transition = 'all 0.6s ease';
            observer.observe(el);
        });
    </script>
</body>
</html>
