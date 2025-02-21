<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title> Mohammad NAVEED</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root {
            --primary: #7209b7;
            --secondary: #3a0ca3;
            --text: #f8f9fa;
            --dark: #0a0b0c;
            --accent: #4cc9f0;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: var(--dark);
            color: var(--text);
            line-height: 1.6;
        }

        /* Existing styles remain the same up to hero section */
        .space-animation {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
             overflow: hidden;
        }

        .star {
            position: absolute;
            background: #fff;
            border-radius: 50%;
            animation: twinkle var(--duration) infinite;
        }

        @keyframes twinkle {
            0%, 100% { opacity: 0; }
            50% { opacity: 1; }
        }

        .navbar {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(10, 11, 12, 0.95);
            backdrop-filter: blur(10px);
            z-index: 1000;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
            padding: 1rem 2rem;
        }

        .nav-content {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            }

        .logo {
            font-size: 1.8rem;
            font-weight: bold;
            background: linear-gradient(45deg, var(--primary), var(--accent));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-decoration: none;
        }

        .nav-links {
            display: flex;
            gap: 2rem;
            align-items: center;
        }

        .nav-links a {
            color: var(--text);
            text-decoration: none;
            transition: color 0.3s;
            font-weight: 500;
        }

        .nav-links a:hover {
            color: var(--accent);
        }

        .social-links {
            position: fixed;
            left: 2rem;
            top: 50%;
            transform: translateY(-50%);
            display: flex;
            flex-direction: column;
            gap: 2rem;
            z-index: 100;
            background: rgba(255, 255, 255, 0.1);
            padding: 1.5rem;
            border-radius: 1rem;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .social-links a {
            color: var(--text);
            font-size: 2rem;
            transition: all 0.3s;
            width: 40px;
            height: 40px;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        .social-links a:hover {
            color: var(--accent);
            transform: translateY(-3px);
        }

        
        /* Updated Hero Section with Profile Picture */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 6rem 2rem;
            background: linear-gradient(rgba(10, 11, 12, 0.8), rgba(10, 11, 12, 0.8)),
                        radial-gradient(circle at center, var(--secondary) 0%, transparent 70%);
        }

        .hero-content {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 0.5rem;
            font-size: 2.2rem; /* Adjust the font size as desired */

        }

        

        .know-more-btn {
            margin-top: 2rem;
            padding: 1rem 2.5rem;
            font-size: 1.1rem;
            color: var(--text);
            background: rgba(255, 255, 255, 0.1);
            border: 1px solid rgba(255, 255, 255, 0.2);
            border-radius: 2rem;
            cursor: pointer;
            transition: all 0.3s;
            text-decoration: none;
            backdrop-filter: blur(10px);
        }

        .know-more-btn:hover {
            background: rgba(255, 255, 255, 0.2);
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }

        .profile-container {
            width: 275px;
            height: 275px;
            border-radius: 50%;
            overflow: hidden;
            border: 4px solid var(--accent);
            box-shadow: 0 0 20px rgba(76, 201, 240, 0.3);
            animation: fadeInUp 1s ease-out;
        }

        .profile-img {
        width: 100%;
            height: 100%;
            object-fit: cover;
        }

        /* New Sections */
        .section {
            padding: 2.5rem 2rem;
            max-width: 1225px;
            margin: 0 auto;
        }

        .section-title {
            font-size: 2.5rem;
            margin-bottom: 2rem;
            text-align: center;
            background: linear-gradient(45deg, var(--primary), var(--accent));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        /* About Section */
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 2rem;
            align-items: center;
        }

        .about-text {
            background: rgba(255, 255, 255, 0.05);
            padding: 2rem;
            border-radius: 1rem;
            backdrop-filter: blur(10px);
        }


        .card-section {
        background: rgba(22, 28, 36, 0.95);
        border-radius: 1rem;
        padding: 2rem;
        margin: 1rem 0;
        width: 100%;
        box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    }

    .card-header {
        display: flex;
        flex-direction: column;
        gap: 0.5rem;
        margin-bottom: 1.5rem;
    }

    .card-title {
        color: #3a0ca3;
        font-size: 1.5rem;
        font-weight: 600;
        margin: 0;
    }

    .card-subtitle {
        color: #a0a0a0;
        font-size: 1rem;
        display: flex;
        align-items: center;
        gap: 0.5rem;
    }

    .card-date {
        color: #a0a0a0;
        font-size: 0.9rem;
    }

    .card-content {
        color: #f8f9fa;
    }

    .experience-list {
        list-style: none;
        padding: 0;
        margin: 1rem 0;
    }

    .experience-list li {
        margin-bottom: 0.8rem;
        line-height: 1.6;
        padding-left: 1.5rem;
        position: relative;
    }

    .experience-list li::before {
        content: "•";
        color: #3a0ca3;
        position: absolute;
        left: 0;
        top: 0;
    }

    .section-container {
        max-width: 1200px;
        margin: 0 auto;
        padding: 0 2rem;
    }

    @media (max-width: 768px) {
        .section-container {
            padding: 0 1rem;
        }
        
        .card-section {
            padding: 1.5rem;
        }
    }


        /* Skills Section */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 1.5rem;
            padding: 2rem;
        }

        .skill-card {
            background: rgba(20, 24, 30, 0.95);
            padding: 2rem;
            border-radius: 0.5rem;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            gap: 1rem;
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: transform 0.3s, border-color 0.3s;
        }

        .skill-card:hover {
            transform: translateY(-5px);
            border-color: var(--accent);
        }

        .skill-icon {
            font-size: 3rem;
            margin-bottom: 0.5rem;
        }

        .skill-card h3 {
            font-size: 1.2rem;
            text-align: center;
            color: var(--text);
        }
        
        /* HTML Icon */
        .skill-icon.html { color: #E44D26; }
        /* CSS Icon */
        .skill-icon.css { color: #1572B6; }
        /* JavaScript Icon */
        .skill-icon.js { color: #F7DF1E; }
   
        /* data science Icon */
        .skill-icon.data.science { color: #007396; }
        /* Python Icon */
        .skill-icon.python { color: #3776AB; }
        /* SQL Icon */
        .skill-icon.sql { color: #4479A1; }
        

        /* Custom Blazor Icon */
        .blazor-icon {
            width: 48px;
            height: 48px;
            background: #512BD4;
            mask: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24'%3E%3Cpath d='M23.834 8.101a13.912 13.912 0 0 1-13.643 11.72 10.105 10.105 0 0 1-1.994-.12 6.111 6.111 0 0 1-5.082-5.761 5.934 5.934 0 0 1 11.867-.084c.025.983-.401 1.846-1.277 1.846-.721 0-1.107-.463-1.107-1.145V11.24c0-.481-.023-.963-.056-1.436-.279-1.654-1.139-2.393-2.342-2.393s-2.063.739-2.342 2.393c-.033.473-.056.955-.056 1.436v4.042c0 2.323-1.145 3.63-2.89 3.63C2.751 18.912 0 15.24 0 11.24S2.751 3.568 5.913 3.568c1.508 0 2.416.512 3.38 1.307a9.803 9.803 0 0 1 7.017-2.197 1.171 1.171 0 0 1 1.074 1.264v2.043c0 .646-.523 1.169-1.169 1.169s-1.169-.523-1.169-1.169V3.972a7.49 7.49 0 0 0-5.369 1.67 5.909 5.909 0 0 1 1.686 4.157c0 3.259-2.646 5.905-5.905 5.905a5.887 5.887 0 0 1-4.002-1.568 10.088 10.088 0 0 0 8.011 4.845 11.827 11.827 0 0 0 11.433-9.839.866.866 0 0 1 1.7.293z'/%3E%3C/svg%3E");
              -webkit-mask: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24'%3E%3Cpath d='M23.834 8.101a13.912 13.912 0 0 1-13.643 11.72 10.105 10.105 0 0 1-1.994-.12 6.111 6.111 0 0 1-5.082-5.761 5.934 5.934 0 0 1 11.867-.084c.025.983-.401 1.846-1.277 1.846-.721 0-1.107-.463-1.107-1.145V11.24c0-.481-.023-.963-.056-1.436-.279-1.654-1.139-2.393-2.342-2.393s-2.063.739-2.342 2.393c-.033.473-.056.955-.056 1.436v4.042c0 2.323-1.145 3.63-2.89 3.63C2.751 18.912 0 15.24 0 11.24S2.751 3.568 5.913 3.568c1.508 0 2.416.512 3.38 1.307a9.803 9.803 0 0 1 7.017-2.197 1.171 1.171 0 0 1 1.074 1.264v2.043c0 .646-.523 1.169-1.169 1.169s-1.169-.523-1.169-1.169V3.972a7.49 7.49 0 0 0-5.369 1.67 5.909 5.909 0 0 1 1.686 4.157c0 3.259-2.646 5.905-5.905 5.905a5.887 5.887 0 0 1-4.002-1.568 10.088 10.088 0 0 0 8.011 4.845 11.827 11.827 0 0 0 11.433-9.839.866.866 0 0 1 1.7.293z'/%3E%3C/svg%3E");
            mask-size: contain;
            -webkit-mask-size: contain;
            mask-repeat: no-repeat;
            -webkit-mask-repeat: no-repeat;
            mask-position: center;
            -webkit-mask-position: center;
        }

        @media (max-width: 1024px) {
            .skills-grid {
                grid-template-columns: repeat(2, 1fr);
            }
        }

        @media (max-width: 480px) {
            .skills-grid {
                grid-template-columns: 1fr;
            }
        }

        /* Projects Section */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .project-card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 1rem;
               overflow: hidden;
            transition: transform 0.3s;
        }

        .project-card:hover {
            transform: translateY(-5px);
        }

        .project-img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }

        .project-info {
            padding: 1.5rem;
        }

        /* Contact Section */
        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
        }

        .contact-form {
            background: rgba(255, 255, 255, 0.05);
            padding: 2rem;
            border-radius: 1rem;
            backdrop-filter: blur(10px);
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
              margin-bottom: 0.5rem;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 0.8rem;
            background: rgba(255, 255, 255, 0.1);
            border: 1px solid rgba(255, 255, 255, 0.2);
            border-radius: 0.5rem;
            color: var(--text);
        }

        .submit-btn {
            background: var(--accent);
            color: var(--dark);
            padding: 0.8rem 2rem;
            border: none;
            border-radius: 0.5rem;
            cursor: pointer;
            transition: all 0.3s;
        }

        .submit-btn:hover {
            background: var(--primary);
            color: var(--text);
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .nav-content {
                flex-direction: column;
                gap: 1rem;
            }

            .social-links {
                position: static;
                flex-direction: row;
                      justify-content: center;
                margin-top: 2rem;
            }

            .hero-content h1 {
                font-size: 2.5rem;
            }

            .contact-info {
                flex-direction: column;
                gap: 1rem;
            }

            .about-content {
                grid-template-columns: 1fr;
            }

            .profile-container {
                width: 150px;
                height: 150px;
            }
        }
    </style>
</head>
<body>
    <div class="space-animation" id="stars"></div>

    <nav class="navbar">
        <div class="nav-content">
            <a href="#" class="logo">Mohammad Naveed</a>
            <div class="nav-links">
                <a href="#home">Home</a>
                <a href="#about">About</a>
                <a href="#experience">Experience</a>
                <a href="#skills">Skills</a>
                <a href="#projects">Projects</a>
                <a href="#contact">Contact</a>
            </div>
               </div>
    </nav>

    <div class="social-links">
        <a href="https://www.linkedin.com/in/likitha-gali/" target="_blank">
            <i class="fab fa-linkedin"></i>
        </a>
        <a href="https://github.com/galilikitha123" target="_blank">
            <i class="fab fa-github"></i>
        </a>
        <a href="mailto:likithareddy1231@gmail.com">
            <i class="fas fa-envelope"></i>
        </a>
        <a href="tel:+91-9182221948">
            <i class="fas fa-phone"></i>
        </a>
    </div>

    <section id="home" class="hero">
        <div class="hero-content">
            <div class="profile-container">
                <img src="I" alt="Mohammad Naveed" class="profile-img">
            </div>
            <h1>Hi, I'm Mohammad Naveed </h1>
            <p>I,m recently GRADUATION</p>
            <a href="#about" class="know-more-btn">Know More</a>
        </div>
    </section>

    <section id="about" class="section">
        <h2 class="section-title">About Me</h2>
        <div class="section-container">
            <div class="card-section">
                <div class="card-content">
                    <p>.</p>
                    <p style="margin-top: 1rem;">Objective: To acquire knowledge, develop critical thinking skills, and achieve academic excellence through dedication, curiosity, and active participation in the learning process, while contributing positively to the school community and preparing for future professional and personal growth..</p>
                </div>
                            </div>
        </div>
    </section>

    <section id="experience" class="section">
        <h2 class="section-title">Experience</h2>
        <div class="section-container">
            <div class="card-section">
                <div class="card-header">
                    <h3 class="card-title">I'm FRESHER</h3>
                    <div class="card-subtitle">
                        <i class="fas fa-building"></i>
                        Chalapathi institution  of technology (Guntur, India)
                    </div>
                    <div class="card-date">
                        <i class="far fa-calendar-alt"></i>
                        June 2025 - Present
                    </div>
                </div>
                <div class="card-content">
                    <ul class="experience-list">
                        <li>Worked on a Project Titled " ECG MONITOR"</li>
                        <li> ECG mean's (electrocardiogram)   </li>
                        <li>Heart Rate: An ECG can measure your heart rate and detect any irregularities, such as tachycardia (fast heart rate) or bradycardia (slow heart rate)..</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <section id="skills" class="section">
        <h2 class="section-title">Skills</h2>
        <div class="skills-grid">
            <div class="skill-card">
                <i class="fab fa-html5 skill-icon html"></i>
                <h3>HTML</h3>
            </div>
            <div class="skill-card">
                <i class="fab fa-css3-alt skill-icon css"></i>
                <h3>CSS</h3>
            </div>
            <div class="skill-card">
                <i class="fab fa-js skill-icon js"></i>
                <h3>JavaScript</h3>
            </div>
            
            

            <div class="skill-card">
                <i class="fab fa-data science -icon data science"></i>
                <h3>Data science</h3>
            </div>
            <div class="skill-card">
                <i class="fab fa-python skill-icon python"></i>
                <h3>Python</h3>
            </div>
            <div class="skill-card">
                <i class="fas fa-database skill-icon sql"></i>
                <h3>SQL</h3>
            </div>
           
               
            </div>
            <div> </div>
    </section>

    <section id="projects" class="section">
        <h2 class="section-title">Projects</h2>
        <div class="projects-grid">
            <div class="project-card">
                <img src="Images/Project1.png" alt="Project 1" class="project-img">
                <div class="project-info">
                    <h3>ECG - Real-Time  monitoring system </h3>
                    <p>Heart Rate: An ECG can measure your heart rate and detect any irregularities, such as tachycardia (fast heart rate) or bradycardia (slow heart rate)..</p>
                </div>
            </div>
            <div class="project-card">
                <img src="Images/Project2.png" alt="Project 2" class="project-img">
                <div class="project-info">
                    <h3>LOGO Guessing Game</h3>
                    <p>Developed a multiplayer web application for a logo guessing game using ASP.NET Core. Implemented user authentication and room management system using MongoDB. Integrated real-time communication with SignalR for synchronized game-play across users.</p>
                </div>
            </div>
            
                </div>
            
    </section>

    <section id="contact" class="section">
        <h2 class="section-title">Contact Me</h2>
        <div class="contact-grid">
            <div class="contact-form">
                <form>
                    <div class="form-group">
                        <label for="name">Name</label>
                        <input type="text" id="name" required>
                    </div>
                    <div class="form-group">
                        <label for="email">Email</label>
                        <input type="email" id="email" required>
                    </div>
                    <div class="form-group">
                        <label for="message">Message</label>
                        <textarea id="message" rows="3" required></textarea>
                    </div>
                    <button type="submit" class="submit-btn">Send Message</button>
                </form>
                
                <!-- Added social icons with styling -->
                <div style="margin-top: 2rem; display: flex; gap: 1.5rem; justify-content: center;">
                    <a href="https://www.linkedin.com/in/naveed-mahommad-75b796276/" target="_blank" style="color: var(--text); font-size: 1.5rem; transition: color 0.3s;">
                        <i class="fab fa-linkedin"></i>
                    </a>
                    <a href="https://github.com/Hannu7860/hannu" target="_blank" style="color: var(--text); font-size: 1.5rem; transition: color 0.3s;">
                        <i class="fab fa-github"></i>
                    </a>
                    <a href="mailto:naveedmd78600@gmail.com" style="color: var(--text); font-size: 1.5rem; transition: color 0.3s;">
                        <i class="fas fa-envelope"></i>
                    </a>
                    <a href="tel:+91-9182502259" style="color: var(--text); font-size: 1.5rem; transition: color 0.3s;">
                        <i class="fas fa-phone"></i>
                    </a>
                </div>
            </div>
        </div>
    </section>

    <script>
        // Create space background
        function createStars() {
            const container = document.getElementById('stars');
            const starCount = 200;
            
            container.innerHTML = '';
            
            for (let i = 0; i < starCount; i++) {
                const star = document.createElement('div');
                star.className = 'star';
                
                const x = Math.random() * 100;
                const y = Math.random() * 100;
                
                // Random size
                const size = Math.random() * 2;
                
                // Random duration
                const duration = 2 + Math.random() * 3;
                
                star.style.left = `${x}%`;
                star.style.top = `${y}%`;
                star.style.width = `${size}px`;
                star.style.height = `${size}px`;
                star.style.setProperty('--duration', `${duration}s`);
                
                container.appendChild(star);
            }
        }

        // Initialize stars
        window.addEventListener('load', createStars);
        window.addEventListener('resize', createStars);

        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // Form submission handling
        const form = document.querySelector('form');
        form.addEventListener('submit', function(e) {
            e.preventDefault();
            const formData = {
                name: document.getElementById('name').value,
                email: document.getElementById('email').value,
                message: document.getElementById('message').value
            };
            // Here you can add your form submission logic
            console.log('Form submitted:', formData);
            // Reset form after submission
            form.reset();
            alert('Thank you for your message! I will get back to you soon.');
        });

        // Navbar background opacity on scroll
        window.addEventListener('scroll', function() {
            const navbar = document.querySelector('.navbar');
            if (window.scrollY > 50) {
                navbar.style.background = 'rgba(10, 11, 12, 0.98)';
            } else {
                navbar.style.background = 'rgba(10, 11, 12, 0.95)';
            }
        });
    </script>
</body>
</html>
