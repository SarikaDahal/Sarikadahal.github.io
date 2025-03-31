<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sarika Dahal | Academic Tutor & Cybersecurity Scholar</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&family=Open+Sans:wght@400;600&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #2c3e50;
            --secondary: #f1c40f;
            --accent: #1abc9c;
            --light: #ecf0f1;
            --dark: #2c3e50;
            --gray: #95a5a6;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Open Sans', sans-serif;
            line-height: 1.6;
            color: #333;
            background-color: #fff;
        }

        h1, h2, h3, h4 {
            font-family: 'Poppins', sans-serif;
            font-weight: 700;
            color: var(--primary);
        }

        a {
            text-decoration: none;
            color: var(--accent);
            transition: all 0.3s ease;
        }

        a:hover {
            color: var(--secondary);
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }

        section {
            padding: 80px 0;
        }

        .section-title {
            text-align: center;
            margin-bottom: 50px;
            position: relative;
        }

        .section-title h2 {
            font-size: 2.5rem;
            display: inline-block;
            position: relative;
            padding-bottom: 15px;
        }

        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 3px;
            background-color: var(--accent);
        }

        /* Header */
        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;
            background-color: rgba(255, 255, 255, 0.95);
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            transition: all 0.3s ease;
        }

        header.scrolled {
            background-color: rgba(44, 62, 80, 0.95);
        }

        header.scrolled nav ul li a {
            color: white;
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--primary);
        }

        header.scrolled .logo {
            color: white;
        }

        nav ul {
            display: flex;
            list-style: none;
        }

        nav ul li {
            margin-left: 30px;
        }

        nav ul li a {
            font-weight: 600;
            color: var(--primary);
            position: relative;
        }

        nav ul li a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background-color: var(--accent);
            transition: width 0.3s ease;
        }

        nav ul li a:hover::after {
            width: 100%;
        }

        .menu-toggle {
            display: none;
            cursor: pointer;
            font-size: 1.5rem;
        }

        /* Hero Section */
        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            background: linear-gradient(rgba(44, 62, 80, 0.8), rgba(44, 62, 80, 0.8)), url('https://images.unsplash.com/photo-1522202176988-66273c2fd55f?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80') no-repeat center center/cover;
            color: white;
            text-align: center;
        }

        .hero-content {
            max-width: 800px;
            margin: 0 auto;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 20px;
            color: white;
        }

        .hero h2 {
            font-size: 2rem;
            margin-bottom: 30px;
            color: var(--secondary);
        }

        .hero-bio {
            font-size: 1.1rem;
            margin-bottom: 40px;
            line-height: 1.8;
        }

        .hero-buttons {
            display: flex;
            justify-content: center;
            gap: 20px;
        }

        .btn {
            display: inline-block;
            padding: 12px 30px;
            border-radius: 50px;
            font-weight: 600;
            transition: all 0.3s ease;
        }

        .btn-primary {
            background-color: var(--accent);
            color: white;
        }

        .btn-primary:hover {
            background-color: #16a085;
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }

        .btn-outline {
            border: 2px solid white;
            color: white;
        }

        .btn-outline:hover {
            background-color: white;
            color: var(--primary);
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }

        /* About Section */
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            align-items: center;
        }

        .about-img {
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 20px 30px rgba(0, 0, 0, 0.1);
        }

        .about-img img {
            width: 100%;
            height: auto;
            display: block;
        }

        .about-text h3 {
            font-size: 1.8rem;
            margin-bottom: 20px;
        }

        .about-text p {
            margin-bottom: 20px;
            color: #555;
        }

        .skills {
            margin-top: 30px;
        }

        .skill-item {
            margin-bottom: 20px;
        }

        .skill-info {
            display: flex;
            justify-content: space-between;
            margin-bottom: 10px;
        }

        .skill-bar {
            height: 10px;
            background-color: #eee;
            border-radius: 5px;
            overflow: hidden;
        }

        .skill-progress {
            height: 100%;
            background-color: var(--accent);
            border-radius: 5px;
            transition: width 1s ease;
        }

        /* Experience Section */
        .experience {
            background-color: #f9f9f9;
        }

        .timeline {
            position: relative;
            max-width: 800px;
            margin: 0 auto;
        }

        .timeline::before {
            content: '';
            position: absolute;
            top: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 2px;
            height: 100%;
            background-color: var(--accent);
        }

        .timeline-item {
            padding: 20px 40px;
            position: relative;
            width: 50%;
            margin-bottom: 30px;
        }

        .timeline-item:nth-child(odd) {
            left: 0;
        }

        .timeline-item:nth-child(even) {
            left: 50%;
        }

        .timeline-content {
            padding: 20px;
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            position: relative;
        }

        .timeline-content::before {
            content: '';
            position: absolute;
            top: 30px;
            right: -15px;
            width: 0;
            height: 0;
            border-style: solid;
            border-width: 10px 0 10px 15px;
            border-color: transparent transparent transparent white;
        }

        .timeline-item:nth-child(even) .timeline-content::before {
            left: -15px;
            right: auto;
            border-width: 10px 15px 10px 0;
            border-color: transparent white transparent transparent;
        }

        .timeline-date {
            font-weight: 600;
            color: var(--accent);
            margin-bottom: 10px;
        }

        .timeline-title {
            font-size: 1.3rem;
            margin-bottom: 10px;
        }

        .timeline-company {
            color: var(--gray);
            margin-bottom: 15px;
        }

        .timeline-desc {
            color: #555;
        }

        .timeline-desc ul {
            margin-left: 20px;
        }

        .timeline-desc li {
            margin-bottom: 5px;
        }

        .timeline-icon {
            position: absolute;
            top: 30px;
            right: -60px;
            width: 40px;
            height: 40px;
            background-color: var(--accent);
            color: white;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 1;
        }

        .timeline-item:nth-child(even) .timeline-icon {
            left: -60px;
            right: auto;
        }

        /* Education Section */
        .education-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .education-card {
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            padding: 30px;
            transition: transform 0.3s ease;
        }

        .education-card:hover {
            transform: translateY(-10px);
        }

        .education-degree {
            font-size: 1.3rem;
            margin-bottom: 10px;
            color: var(--primary);
        }

        .education-institution {
            font-weight: 600;
            color: var(--accent);
            margin-bottom: 15px;
        }

        .education-date {
            color: var(--gray);
            margin-bottom: 15px;
        }

        .education-desc {
            color: #555;
        }

        /* Projects Section */
        .projects {
            background-color: #f9f9f9;
        }

        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .project-card {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease;
        }

        .project-card:hover {
            transform: translateY(-10px);
        }

        .project-img {
            height: 200px;
            overflow: hidden;
        }

        .project-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }

        .project-card:hover .project-img img {
            transform: scale(1.1);
        }

        .project-content {
            padding: 20px;
        }

        .project-title {
            font-size: 1.3rem;
            margin-bottom: 10px;
        }

        .project-tech {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-bottom: 15px;
        }

        .tech-tag {
            background-color: var(--light);
            color: var(--primary);
            padding: 5px 10px;
            border-radius: 20px;
            font-size: 0.8rem;
            font-weight: 600;
        }

        .project-desc {
            color: #555;
            margin-bottom: 20px;
        }

        .project-links {
            display: flex;
            gap: 15px;
        }

        .project-link {
            display: inline-flex;
            align-items: center;
            gap: 5px;
            font-weight: 600;
        }

        /* Achievements Section */
        .achievements-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .achievement-card {
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            padding: 30px;
            text-align: center;
            transition: transform 0.3s ease;
        }

        .achievement-card:hover {
            transform: translateY(-10px);
        }

        .achievement-icon {
            font-size: 3rem;
            color: var(--secondary);
            margin-bottom: 20px;
        }

        .achievement-title {
            font-size: 1.3rem;
            margin-bottom: 15px;
        }

        .achievement-desc {
            color: #555;
        }

        /* Contact Section */
        .contact {
            background-color: #f9f9f9;
        }

        .contact-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 50px;
        }

        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .contact-icon {
            width: 50px;
            height: 50px;
            background-color: var(--accent);
            color: white;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 1.2rem;
        }

        .contact-text h3 {
            font-size: 1.2rem;
            margin-bottom: 5px;
        }

        .contact-text p, .contact-text a {
            color: #555;
        }

        .contact-form {
            background-color: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            margin-bottom: 5px;
            font-weight: 600;
        }

        .form-control {
            width: 100%;
            padding: 12px 15px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-family: 'Open Sans', sans-serif;
            transition: border-color 0.3s ease;
        }

        .form-control:focus {
            outline: none;
            border-color: var(--accent);
        }

        textarea.form-control {
            min-height: 150px;
            resize: vertical;
        }

        .submit-btn {
            background-color: var(--accent);
            color: white;
            border: none;
            padding: 12px 30px;
            border-radius: 50px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .submit-btn:hover {
            background-color: #16a085;
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }

        /* Footer */
        footer {
            background-color: var(--primary);
            color: white;
            text-align: center;
            padding: 30px 0;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-bottom: 20px;
        }

        .social-link {
            width: 40px;
            height: 40px;
            background-color: rgba(255, 255, 255, 0.1);
            color: white;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            transition: all 0.3s ease;
        }

        .social-link:hover {
            background-color: var(--accent);
            transform: translateY(-3px);
        }

        .copyright {
            color: rgba(255, 255, 255, 0.7);
            font-size: 0.9rem;
        }

        /* Responsive Design */
        @media (max-width: 992px) {
            .about-content {
                grid-template-columns: 1fr;
            }

            .about-img {
                max-width: 500px;
                margin: 0 auto;
            }

            .timeline::before {
                left: 40px;
            }

            .timeline-item {
                width: 100%;
                padding-left: 70px;
                padding-right: 0;
            }

            .timeline-item:nth-child(even) {
                left: 0;
            }

            .timeline-content::before {
                left: -15px !important;
                right: auto !important;
                border-width: 10px 15px 10px 0 !important;
                border-color: transparent white transparent transparent !important;
            }

            .timeline-icon {
                left: 20px !important;
                right: auto !important;
            }
        }

        @media (max-width: 768px) {
            .menu-toggle {
                display: block;
            }

            nav ul {
                position: fixed;
                top: 80px;
                left: -100%;
                width: 100%;
                height: calc(100vh - 80px);
                background-color: var(--primary);
                flex-direction: column;
                align-items: center;
                padding-top: 40px;
                transition: all 0.5s ease;
            }

            nav ul.active {
                left: 0;
            }

            nav ul li {
                margin: 15px 0;
            }

            nav ul li a {
                color: white;
            }

            .hero h1 {
                font-size: 2.5rem;
            }

            .hero h2 {
                font-size: 1.5rem;
            }

            .hero-buttons {
                flex-direction: column;
                align-items: center;
            }

            section {
                padding: 60px 0;
            }
        }

        @media (max-width: 576px) {
            .section-title h2 {
                font-size: 2rem;
            }

            .hero h1 {
                font-size: 2rem;
            }

            .hero h2 {
                font-size: 1.2rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header id="header">
        <div class="container">
            <nav>
                <a href="#" class="logo">Sarika Dahal</a>
                <div class="menu-toggle">
                    <i class="fas fa-bars"></i>
                </div>
                <ul id="nav-menu">
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#experience">Experience</a></li>
                    <li><a href="#education">Education</a></li>
                    <li><a href="#projects">Projects</a></li>
                    <li><a href="#achievements">Achievements</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="container">
            <div class="hero-content">
                <h1>Sarika Dahal</h1>
                <h2>Academic Tutor & Cybersecurity Scholar</h2>
                <p class="hero-bio">I have always been passionate about education and learning, which led me to work as a Graduate Teaching Assistant (GTA) for a year at Itahari International College. In this role, I provided academic support to both students and faculty, enhancing my communication, organizational, and instructional skills. I am driven by the opportunity to contribute to others' learning journeys while continually expanding my own knowledge and skills.</p>
                <div class="hero-buttons">
                    <a href="#projects" class="btn btn-primary">View My Projects</a>
                    <a href="#contact" class="btn btn-outline">Contact Me</a>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="about">
        <div class="container">
            <div class="section-title">
                <h2>About Me</h2>
            </div>
            <div class="about-content">
                <div class="about-img">
                    <img src="https://images.unsplash.com/photo-1573496359142-b8d87734a5a2?ixlib=rb-1.2.1&auto=format&fit=crop&w=634&q=80" alt="Sarika Dahal">
                </div>
                <div class="about-text">
                    <h3>Academic Tutor & Cybersecurity Student</h3>
                    <p>I am currently pursuing my Master's degree in Cybersecurity at Islington College while maintaining a strong passion for education and teaching. My background in BIT (Computing) and experience as a Graduate Teaching Assistant has equipped me with both technical and pedagogical skills.</p>
                    <p>I enjoy creating applications that solve real-world problems, as demonstrated by my projects like the Student Registration App and Mahibari App. My goal is to bridge the gap between technology and education to create impactful learning experiences.</p>
                    
                    <div class="skills">
                        <div class="skill-item">
                            <div class="skill-info">
                                <span>Teaching/Instruction</span>
                                <span>90%</span>
                            </div>
                            <div class="skill-bar">
                                <div class="skill-progress" style="width: 90%;"></div>
                            </div>
                        </div>
                        <div class="skill-item">
                            <div class="skill-info">
                                <span>Flutter & Django</span>
                                <span>85%</span>
                            </div>
                            <div class="skill-bar">
                                <div class="skill-progress" style="width: 85%;"></div>
                            </div>
                        </div>
                        <div class="skill-item">
                            <div class="skill-info">
                                <span>Cybersecurity</span>
                                <span>75%</span>
                            </div>
                            <div class="skill-bar">
                                <div class="skill-progress" style="width: 75%;"></div>
                            </div>
                        </div>
                        <div class="skill-item">
                            <div class="skill-info">
                                <span>Bilingual (Nepali/English)</span>
                                <span>100%</span>
                            </div>
                            <div class="skill-bar">
                                <div class="skill-progress" style="width: 100%;"></div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Experience Section -->
    <section id="experience" class="experience">
        <div class="container">
            <div class="section-title">
                <h2>My Experience</h2>
            </div>
            <div class="timeline">
                <div class="timeline-item">
                    <div class="timeline-icon">
                        <i class="fas fa-briefcase"></i>
                    </div>
                    <div class="timeline-content">
                        <span class="timeline-date">Jul 2023 - Sep 2024</span>
                        <h3 class="timeline-title">Graduate Teaching Assistant</h3>
                        <p class="timeline-company">Itahari International College</p>
                        <div class="timeline-desc">
                            <ul>
                                <li>Assisted faculty members in delivering lectures, grading assignments, and conducting tutorials</li>
                                <li>Gained valuable experience in an academic setting, fostering a deep interest in educational development</li>
                                <li>Postgraduate Scholarship Recipient: Currently pursuing further studies to deepen my expertise and continue contributing to the education sector</li>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Education Section -->
    <section id="education" class="education">
        <div class="container">
            <div class="section-title">
                <h2>My Education</h2>
            </div>
            <div class="education-grid">
                <div class="education-card">
                    <h3 class="education-degree">Master's in Cyber Security</h3>
                    <p class="education-institution">Islington College</p>
                    <p class="education-date">Sep 2024 - Present</p>
                    <p class="education-desc">Currently pursuing advanced studies in cybersecurity to deepen my technical expertise and contribute to the growing field of information security.</p>
                </div>
                <div class="education-card">
                    <h3 class="education-degree">Bachelor's in BIT (Computing)</h3>
                    <p class="education-institution">Itahari International College</p>
                    <p class="education-date">Feb 2021 - Dec 2023</p>
                    <p class="education-desc">Completed comprehensive studies in computing with a focus on practical applications and theoretical foundations of information technology.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="projects">
        <div class="container">
            <div class="section-title">
                <h2>My Projects</h2>
            </div>
            <div class="projects-grid">
                <div class="project-card">
                    <div class="project-img">
                        <img src="https://images.unsplash.com/photo-1551650975-87deedd944c3?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Student Registration App">
                    </div>
                    <div class="project-content">
                        <h3 class="project-title">Student Registration App</h3>
                        <div class="project-tech">
                            <span class="tech-tag">Flutter</span>
                            <span class="tech-tag">Django</span>
                            <span class="tech-tag">Mobile App</span>
                        </div>
                        <p class="project-desc">A college project to register student's credentials to a document using Flutter and Django framework.</p>
                        <div class="project-links">
                            <a href="#" class="project-link"><i class="fas fa-external-link-alt"></i> Live Demo</a>
                            <a href="#" class="project-link"><i class="fab fa-github"></i> Code</a>
                        </div>
                    </div>
                </div>
                <div class="project-card">
                    <div class="project-img">
                        <img src="https://images.unsplash.com/photo-1584473457406-6240486418e9?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="Mahibari App">
                    </div>
                    <div class="project-content">
                        <h3 class="project-title">Mahibari App</h3>
                        <div class="project-tech">
                            <span class="tech-tag">Flutter</span>
                            <span class="tech-tag">Django</span>
                            <span class="tech-tag">Mobile App</span>
                            <span class="tech-tag">Bilingual</span>
                        </div>
                        <p class="project-desc">An application to register and predict the upcoming period cycle using both Nepali and English language/date using Flutter and Django framework.</p>
                        <div class="project-links">
                            <a href="#" class="project-link"><i class="fas fa-external-link-alt"></i> Live Demo</a>
                            <a href="#" class="project-link"><i class="fab fa-github"></i> Code</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Achievements Section -->
    <section id="achievements" class="achievements">
        <div class="container">
            <div class="section-title">
                <h2>My Achievements</h2>
            </div>
            <div class="achievements-grid">
                <div class="achievement-card">
                    <div class="achievement-icon">
                        <i class="fas fa-award"></i>
                    </div>
                    <h3 class="achievement-title">AAA Scholarship</h3>
                    <p class="achievement-desc">I was honored to receive the prestigious AAA Scholarship during my studies at Itahari International College, recognizing my academic excellence and commitment to learning. This scholarship not only supported my education but also motivated me to continue pursuing academic growth and contributing to the academic community.</p>
                </div>
                <div class="achievement-card">
                    <div class="achievement-icon">
                        <i class="fas fa-graduation-cap"></i>
                    </div>
                    <h3 class="achievement-title">Post Graduate Scholarship</h3>
                    <p class="achievement-desc">I have been awarded a prestigious postgraduate scholarship in recognition of my academic achievements and dedication to continuous learning. This scholarship has enabled me to further pursue advanced studies, allowing me to deepen my expertise and contribute to the academic field.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="contact">
        <div class="container">
            <div class="section-title">
                <h2>Contact Me</h2>
            </div>
            <div class="contact-container">
                <div class="contact-info">
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-map-marker-alt"></i>
                        </div>
                        <div class="contact-text">
                            <h3>Location</h3>
                            <p>Sunsari, Itahari</p>
                        </div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-phone-alt"></i>
                        </div>
                        <div class="contact-text">
                            <h3>Phone</h3>
                            <a href="tel:9862358756">9862358756</a>
                        </div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-envelope"></i>
                        </div>
                        <div class="contact-text">
                            <h3>Email</h3>
                            <a href="mailto:sarikadahal2003@gmail.com">sarikadahal2003@gmail.com</a>
                        </div>
                    </div>
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-user-tie"></i>
                        </div>
                        <div class="contact-text">
                            <h3>Reference</h3>
                            <p>Santosh Parajuli - Head of Academics</p>
                            <p>Itahari International College</p>
                            <a href="tel:+9779849853141">+977 9849853141</a>
                            <a href="mailto:Santosh.parajuli@iic.edu.np">Santosh.parajuli@iic.edu.np</a>
                        </div>
                    </div>
                </div>
                <div class="contact-form">
                    <form id="contactForm">
                        <div class="form-group">
                            <label for="name">Name</label>
                            <input type="text" id="name" class="form-control" required>
                        </div>
                        <div class="form-group">
                            <label for="email">Email</label>
                            <input type="email" id="email" class="form-control" required>
                        </div>
                        <div class="form-group">
                            <label for="subject">Subject</label>
                            <input type="text" id="subject" class="form-control" required>
                        </div>
                        <div class="form-group">
                            <label for="message">Message</label>
                            <textarea id="message" class="form-control" required></textarea>
                        </div>
                        <button type="submit" class="submit-btn">Send Message</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="social-links">
                <a href="#" class="social-link"><i class="fab fa-linkedin-in"></i></a>
                <a href="#" class="social-link"><i class="fab fa-github"></i></a>
                <a href="#" class="social-link"><i class="fab fa-twitter"></i></a>
                <a href="#" class="social-link"><i class="fab fa-facebook-f"></i></a>
            </div>
            <p class="copyright">&copy; 2024 Sarika Dahal. All Rights Reserved.</p>
        </div>
    </footer>

    <script>
        // Mobile Menu Toggle
        const menuToggle = document.querySelector('.menu-toggle');
        const navMenu = document.getElementById('nav-menu');

        menuToggle.addEventListener('click', () => {
            navMenu.classList.toggle('active');
        });

        // Close mobile menu when clicking on a link
        document.querySelectorAll('#nav-menu a').forEach(link => {
            link.addEventListener('click', () => {
                navMenu.classList.remove('active');
            });
        });

        // Header scroll effect
        window.addEventListener('scroll', () => {
            const header = document.getElementById('header');
            if (window.scrollY > 100) {
                header.classList.add('scrolled');
            } else {
                header.classList.remove('scrolled');
            }
        });

        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                const targetElement = document.querySelector(targetId);
                
                if (targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                }
            });
        });

        // Form submission
        const contactForm = document.getElementById('contactForm');
        
        contactForm.addEventListener('submit', function(e) {
            e.preventDefault();
            
            // Get form values
            const name = document.getElementById('name').value;
            const email = document.getElementById('email').value;
            const subject = document.getElementById('subject').value;
            const message = document.getElementById('message').value;
            
            // Here you would typically send the form data to a server
            // For this example, we'll just log it and show an alert
            console.log({ name, email, subject, message });
            
            alert('Thank you for your message! I will get back to you soon.');
            contactForm.reset();
        });

        // Animate skill bars on scroll
        function animateSkills() {
            const skillBars = document.querySelectorAll('.skill-progress');
            
            skillBars.forEach(bar => {
                const width = bar.style.width;
                bar.style.width
