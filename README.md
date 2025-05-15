<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cyrus Kuiyaki | Criminology Expert & Consultant</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&family=Playfair+Display:wght@700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #2c3e50;
            --secondary: #e74c3c;
            --accent: #3498db;
            --light: #ecf0f1;
            --dark: #1a252f;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Poppins', sans-serif;
            line-height: 1.6;
            color: #333;
            background-color: #f9f9f9;
            overflow-x: hidden;
        }
        
        header {
            background: linear-gradient(135deg, var(--primary), var(--dark));
            color: white;
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
        }
        
        header.scrolled {
            padding: 0.5rem 0;
            background: rgba(44, 62, 80, 0.95);
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-family: 'Playfair Display', serif;
            font-size: 1.8rem;
            font-weight: 700;
            color: white;
            text-decoration: none;
            display: flex;
            align-items: center;
        }
        
        .logo span {
            color: var(--secondary);
        }
        
        .nav-links {
            display: flex;
            list-style: none;
        }
        
        .nav-links li {
            margin-left: 2rem;
        }
        
        .nav-links a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
            position: relative;
        }
        
        .nav-links a:hover {
            color: var(--accent);
        }
        
        .nav-links a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            background: var(--accent);
            bottom: -5px;
            left: 0;
            transition: width 0.3s;
        }
        
        .nav-links a:hover::after {
            width: 100%;
        }
        
        .hamburger {
            display: none;
            cursor: pointer;
        }
        
        .hero {
            height: 100vh;
            background: url('https://images.unsplash.com/photo-1587825140708-dfaf72ae4b04?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80') no-repeat center center/cover;
            display: flex;
            align-items: center;
            position: relative;
            color: white;
        }
        
        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.6);
        }
        
        .hero-content {
            position: relative;
            z-index: 1;
            max-width: 800px;
            animation: fadeInUp 1s ease;
        }
        
        .hero h1 {
            font-family: 'Playfair Display', serif;
            font-size: 3.5rem;
            margin-bottom: 1rem;
            line-height: 1.2;
        }
        
        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
        }
        
        .btn {
            display: inline-block;
            background: var(--accent);
            color: white;
            padding: 0.8rem 1.8rem;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s;
            border: none;
            cursor: pointer;
        }
        
        .btn:hover {
            background: #2980b9;
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }
        
        .btn-outline {
            background: transparent;
            border: 2px solid white;
            margin-left: 1rem;
        }
        
        .btn-outline:hover {
            background: white;
            color: var(--primary);
        }
        
        section {
            padding: 5rem 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 3rem;
        }
        
        .section-title h2 {
            font-family: 'Playfair Display', serif;
            font-size: 2.5rem;
            color: var(--primary);
            position: relative;
            display: inline-block;
        }
        
        .section-title h2::after {
            content: '';
            position: absolute;
            width: 50%;
            height: 3px;
            background: var(--secondary);
            bottom: -10px;
            left: 25%;
        }
        
        .about {
            background: white;
        }
        
        .about-content {
            display: flex;
            align-items: center;
            gap: 3rem;
        }
        
        .about-img {
            flex: 1;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 20px 30px rgba(0,0,0,0.1);
            animation: fadeInLeft 1s ease;
        }
        
        .about-img img {
            width: 100%;
            height: auto;
            display: block;
            transition: transform 0.5s;
        }
        
        .about-img:hover img {
            transform: scale(1.05);
        }
        
        .about-text {
            flex: 1;
            animation: fadeInRight 1s ease;
        }
        
        .about-text h3 {
            font-size: 2rem;
            margin-bottom: 1.5rem;
            color: var(--primary);
        }
        
        .about-text p {
            margin-bottom: 1.5rem;
        }
        
        .services {
            background: var(--light);
        }
        
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .service-card {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: all 0.3s;
            text-align: center;
            padding: 2rem;
            transform: translateY(0);
        }
        
        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.15);
        }
        
        .service-icon {
            font-size: 3rem;
            color: var(--accent);
            margin-bottom: 1.5rem;
        }
        
        .service-card h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: var(--primary);
        }
        
        .experience {
            background: white;
        }
        
        .timeline {
            position: relative;
            max-width: 800px;
            margin: 0 auto;
            padding: 2rem 0;
        }
        
        .timeline::before {
            content: '';
            position: absolute;
            width: 2px;
            background: var(--accent);
            top: 0;
            bottom: 0;
            left: 50%;
            margin-left: -1px;
        }
        
        .timeline-item {
            padding: 1rem 2rem;
            position: relative;
            width: 50%;
            box-sizing: border-box;
            margin-bottom: 2rem;
            opacity: 0;
            transform: translateY(20px);
            transition: all 0.5s ease;
        }
        
        .timeline-item.visible {
            opacity: 1;
            transform: translateY(0);
        }
        
        .timeline-item:nth-child(odd) {
            left: 0;
            text-align: right;
            padding-right: 3rem;
        }
        
        .timeline-item:nth-child(even) {
            left: 50%;
            padding-left: 3rem;
        }
        
        .timeline-content {
            background: var(--light);
            padding: 1.5rem;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            position: relative;
        }
        
        .timeline-content::after {
            content: '';
            position: absolute;
            width: 15px;
            height: 15px;
            background: var(--accent);
            border-radius: 50%;
            top: 20px;
        }
        
        .timeline-item:nth-child(odd) .timeline-content::after {
            right: -37px;
        }
        
        .timeline-item:nth-child(even) .timeline-content::after {
            left: -37px;
        }
        
        .timeline-date {
            font-weight: 600;
            color: var(--secondary);
            margin-bottom: 0.5rem;
        }
        
        .contact {
            background: linear-gradient(135deg, var(--primary), var(--dark));
            color: white;
        }
        
        .contact .section-title h2 {
            color: white;
        }
        
        .contact .section-title h2::after {
            background: var(--accent);
        }
        
        .contact-container {
            display: flex;
            gap: 3rem;
        }
        
        .contact-info {
            flex: 1;
            animation: fadeInLeft 1s ease;
        }
        
        .contact-info h3 {
            font-size: 1.8rem;
            margin-bottom: 1.5rem;
        }
        
        .contact-details {
            margin-bottom: 2rem;
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            margin-bottom: 1rem;
        }
        
        .contact-icon {
            font-size: 1.5rem;
            margin-right: 1rem;
            color: var(--accent);
        }
        
        .contact-form {
            flex: 1;
            animation: fadeInRight 1s ease;
        }
        
        .form-group {
            margin-bottom: 1.5rem;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 500;
        }
        
        .form-control {
            width: 100%;
            padding: 0.8rem 1rem;
            border-radius: 5px;
            border: none;
            font-family: 'Poppins', sans-serif;
            background: rgba(255,255,255,0.1);
            color: white;
            transition: all 0.3s;
        }
        
        .form-control:focus {
            outline: none;
            background: rgba(255,255,255,0.2);
        }
        
        textarea.form-control {
            min-height: 150px;
            resize: vertical;
        }
        
        .form-control::placeholder {
            color: rgba(255,255,255,0.7);
        }
        
        footer {
            background: var(--dark);
            color: white;
            text-align: center;
            padding: 2rem 0;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            margin-bottom: 1.5rem;
        }
        
        .social-links a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: rgba(255,255,255,0.1);
            color: white;
            margin: 0 0.5rem;
            transition: all 0.3s;
        }
        
        .social-links a:hover {
            background: var(--accent);
            transform: translateY(-3px);
        }
        
        .copyright {
            font-size: 0.9rem;
            opacity: 0.8;
        }
        
        /* Animations */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        @keyframes fadeInLeft {
            from {
                opacity: 0;
                transform: translateX(-20px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }
        
        @keyframes fadeInRight {
            from {
                opacity: 0;
                transform: translateX(20px);
            }
            to {
                opacity: 1;
                transform: translateX(0);
            }
        }
        
        /* Interactive Elements */
        .lawyer-network {
            background: var(--light);
            padding: 3rem;
            border-radius: 10px;
            margin-top: 3rem;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        
        .lawyer-network::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('https://images.unsplash.com/photo-1589829545856-d10d557cf95f?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80') no-repeat center center/cover;
            opacity: 0.1;
            z-index: 0;
        }
        
        .lawyer-network-content {
            position: relative;
            z-index: 1;
        }
        
        .lawyer-network h3 {
            font-size: 2rem;
            margin-bottom: 1rem;
            color: var(--primary);
        }
        
        .lawyer-network p {
            margin-bottom: 2rem;
            max-width: 700px;
            margin-left: auto;
            margin-right: auto;
        }
        
        .testimonials {
            padding: 5rem 0;
            background: white;
        }
        
        .testimonial-slider {
            max-width: 800px;
            margin: 0 auto;
            position: relative;
            overflow: hidden;
        }
        
        .testimonial-slide {
            padding: 2rem;
            text-align: center;
            display: none;
            animation: fadeIn 0.5s ease;
        }
        
        .testimonial-slide.active {
            display: block;
        }
        
        .testimonial-text {
            font-style: italic;
            margin-bottom: 1.5rem;
            position: relative;
        }
        
        .testimonial-text::before,
        .testimonial-text::after {
            content: '"';
            font-size: 2rem;
            color: var(--accent);
            opacity: 0.5;
        }
        
        .testimonial-author {
            font-weight: 600;
            color: var(--primary);
        }
        
        .slider-nav {
            display: flex;
            justify-content: center;
            margin-top: 1.5rem;
        }
        
        .slider-dot {
            width: 12px;
            height: 12px;
            border-radius: 50%;
            background: #ccc;
            margin: 0 5px;
            cursor: pointer;
            transition: all 0.3s;
        }
        
        .slider-dot.active {
            background: var(--accent);
            transform: scale(1.2);
        }
        
        @keyframes fadeIn {
            from {
                opacity: 0;
            }
            to {
                opacity: 1;
            }
        }
        
        /* Responsive Styles */
        @media (max-width: 992px) {
            .about-content {
                flex-direction: column;
            }
            
            .contact-container {
                flex-direction: column;
            }
            
            .timeline::before {
                left: 31px;
            }
            
            .timeline-item {
                width: 100%;
                padding-left: 70px;
                padding-right: 25px;
                text-align: left;
            }
            
            .timeline-item:nth-child(even) {
                left: 0;
            }
            
            .timeline-item:nth-child(odd) .timeline-content::after,
            .timeline-item:nth-child(even) .timeline-content::after {
                left: 15px;
            }
        }
        
        @media (max-width: 768px) {
            .nav-links {
                position: fixed;
                top: 70px;
                left: -100%;
                width: 100%;
                height: calc(100vh - 70px);
                background: var(--primary);
                flex-direction: column;
                align-items: center;
                justify-content: center;
                transition: all 0.5s ease;
            }
            
            .nav-links.active {
                left: 0;
            }
            
            .nav-links li {
                margin: 1.5rem 0;
            }
            
            .hamburger {
                display: block;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .section-title h2 {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <header id="header">
        <div class="container">
            <nav>
                <a href="#" class="logo">Cyrus <span>Kuiyaki</span></a>
                <ul class="nav-links" id="navLinks">
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#services">Services</a></li>
                    <li><a href="#experience">Experience</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
                <div class="hamburger" id="hamburger">
                    <i class="fas fa-bars"></i>
                </div>
            </nav>
        </div>
    </header>

    <section class="hero" id="home">
        <div class="container">
            <div class="hero-content">
                <h1>Criminology Expert & Consultant</h1>
                <p>With years of experience in criminology, probation services, and legal networking, I provide comprehensive solutions to complex criminal justice challenges in Kenya.</p>
                <a href="#contact" class="btn">Get in Touch</a>
                <a href="#services" class="btn btn-outline">Our Services</a>
            </div>
        </div>
    </section>

    <section class="about" id="about">
        <div class="container">
            <div class="section-title">
                <h2>About Me</h2>
            </div>
            <div class="about-content">
                <div class="about-img">
                    <img src="https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=687&q=80" alt="Cyrus Kuiyaki">
                </div>
                <div class="about-text">
                    <h3>Cyrus Kuiyaki</h3>
                    <p>I am a dedicated criminology professional with extensive experience in both public service and private consultancy. My career has been focused on creating safer communities through evidence-based practices and innovative solutions.</p>
                    <p>As a former probation officer and Nairobi County Council employee, I bring unique insights into the Kenyan criminal justice system. My work bridges the gap between theory and practice, ensuring practical solutions to complex problems.</p>
                    <p>Beyond my professional qualifications, I am committed to mentoring young criminology professionals and advocating for justice system reforms that prioritize rehabilitation and community safety.</p>
                    <a href="#experience" class="btn">View My Experience</a>
                </div>
            </div>
        </div>
    </section>

    <section class="services" id="services">
        <div class="container">
            <div class="section-title">
                <h2>My Services</h2>
            </div>
            <div class="services-grid">
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-gavel"></i>
                    </div>
                    <h3>Criminal Case Analysis</h3>
                    <p>Comprehensive analysis of criminal cases using criminological theories and forensic evidence to build strong legal strategies.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-user-shield"></i>
                    </div>
                    <h3>Probation Consultancy</h3>
                    <p>Expert advice on probation matters, rehabilitation programs, and offender management based on years of hands-on experience.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-handshake"></i>
                    </div>
                    <h3>Legal Networking</h3>
                    <p>Connecting clients with specialized lawyers for various legal needs, ensuring you get the right representation for your case.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-chart-line"></i>
                    </div>
                    <h3>Crime Prevention Strategies</h3>
                    <p>Developing customized crime prevention plans for communities, businesses, and institutions based on criminological research.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-balance-scale"></i>
                    </div>
                    <h3>Expert Witness</h3>
                    <p>Serving as an expert witness in court cases, providing professional opinions on criminological matters and offender behavior.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-book"></i>
                    </div>
                    <h3>Training & Workshops</h3>
                    <p>Conducting training sessions for law enforcement, community groups, and organizations on various criminology topics.</p>
                </div>
            </div>
            
            <div class="lawyer-network">
                <div class="lawyer-network-content">
                    <h3>Legal Network Access</h3>
                    <p>With my extensive network in the Kenyan legal community, I can connect you with specialized lawyers across various practice areas including criminal defense, family law, civil litigation, and more. Whether you need representation or legal advice, I can help you find the right professional for your specific needs.</p>
                    <a href="#contact" class="btn">Request Legal Connection</a>
                </div>
            </div>
        </div>
    </section>

    <section class="experience" id="experience">
        <div class="container">
            <div class="section-title">
                <h2>Professional Experience</h2>
            </div>
            <div class="timeline">
                <div class="timeline-item">
                    <div class="timeline-content">
                        <div class="timeline-date">2018 - Present</div>
                        <h3>Independent Criminology Consultant</h3>
                        <p>Providing expert criminology consultation services to law firms, NGOs, and government agencies. Specializing in criminal behavior analysis, crime prevention strategies, and rehabilitation program development.</p>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="timeline-content">
                        <div class="timeline-date">2015 - 2018</div>
                        <h3>Probation Officer</h3>
                        <p>Served as a probation officer in Nairobi, managing caseloads of offenders, preparing pre-sentence reports, and monitoring compliance with court orders. Developed rehabilitation programs that reduced recidivism rates.</p>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="timeline-content">
                        <div class="timeline-date">2010 - 2015</div>
                        <h3>Nairobi County Council</h3>
                        <p>Worked with the Nairobi County Council on community safety initiatives and urban crime prevention strategies. Collaborated with local law enforcement to implement evidence-based crime reduction programs.</p>
                    </div>
                </div>
                <div class="timeline-item">
                    <div class="timeline-content">
                        <div class="timeline-date">2006 - 2010</div>
                        <h3>Research Assistant - University of Nairobi</h3>
                        <p>Conducted criminological research focusing on urban crime patterns and youth delinquency. Assisted in publishing several papers that informed national crime prevention policies.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section class="testimonials">
        <div class="container">
            <div class="section-title">
                <h2>Client Testimonials</h2>
            </div>
            <div class="testimonial-slider">
                <div class="testimonial-slide active">
                    <div class="testimonial-text">
                        Cyrus provided invaluable insights into our criminal case that helped shape our legal strategy. His expertise in offender behavior analysis was crucial to our successful defense.
                    </div>
                    <div class="testimonial-author">- James Mwangi, Business Owner</div>
                </div>
                <div class="testimonial-slide">
                    <div class="testimonial-text">
                        As a community leader, I've worked with Cyrus on several crime prevention initiatives. His practical approach and deep understanding of criminology have made our neighborhood safer.
                    </div>
                    <div class="testimonial-author">- Sarah Atieno, Community Organizer</div>
                </div>
                <div class="testimonial-slide">
                    <div class="testimonial-text">
                        The probation program Cyrus designed for our organization has shown remarkable results in reducing repeat offenses among youth offenders. His expertise is unmatched.
                    </div>
                    <div class="testimonial-author">- David Ochieng, NGO Director</div>
                </div>
                <div class="slider-nav">
                    <div class="slider-dot active" data-slide="0"></div>
                    <div class="slider-dot" data-slide="1"></div>
                    <div class="slider-dot" data-slide="2"></div>
                </div>
            </div>
        </div>
    </section>

    <section class="contact" id="contact">
        <div class="container">
            <div class="section-title">
                <h2>Contact Me</h2>
            </div>
            <div class="contact-container">
                <div class="contact-info">
                    <h3>Get In Touch</h3>
                    <p>Feel free to reach out for consultations, speaking engagements, or to discuss how I can assist with your criminology or legal needs.</p>
                    <div class="contact-details">
                        <div class="contact-item">
                            <div class="contact-icon">
                                <i class="fas fa-phone"></i>
                            </div>
                            <div>0700 695 101</div>
                        </div>
                        <div class="contact-item">
                            <div class="contact-icon">
                                <i class="fas fa-envelope"></i>
                            </div>
                            <div>cyrus.kuiyaki@example.com</div>
                        </div>
                        <div class="contact-item">
                            <div class="contact-icon">
                                <i class="fas fa-map-marker-alt"></i>
                            </div>
                            <div>Nairobi, Kenya</div>
                        </div>
                    </div>
                    <h3>Office Hours</h3>
                    <p>Monday - Friday: 9:00 AM - 5:00 PM</p>
                    <p>Saturday: 10:00 AM - 2:00 PM</p>
                    <p>Emergency consultations available outside hours</p>
                </div>
                <div class="contact-form">
                    <form id="contactForm">
                        <div class="form-group">
                            <label for="name">Your Name</label>
                            <input type="text" id="name" class="form-control" placeholder="Enter your name" required>
                        </div>
                        <div class="form-group">
                            <label for="email">Email Address</label>
                            <input type="email" id="email" class="form-control" placeholder="Enter your email" required>
                        </div>
                        <div class="form-group">
                            <label for="phone">Phone Number</label>
                            <input type="tel" id="phone" class="form-control" placeholder="Enter your phone number">
                        </div>
                        <div class="form-group">
                            <label for="service">Service Needed</label>
                            <select id="service" class="form-control">
                                <option value="">Select a service</option>
                                <option value="case-analysis">Criminal Case Analysis</option>
                                <option value="probation">Probation Consultancy</option>
                                <option value="legal-network">Legal Network Connection</option>
                                <option value="crime-prevention">Crime Prevention Strategy</option>
                                <option value="expert-witness">Expert Witness Services</option>
                                <option value="training">Training & Workshops</option>
                                <option value="other">Other</option>
                            </select>
                        </div>
                        <div class="form-group">
                            <label for="message">Your Message</label>
                            <textarea id="message" class="form-control" placeholder="Enter your message" required></textarea>
                        </div>
                        <button type="submit" class="btn">Send Message</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <div class="social-links">
                <a href="#"><i class="fab fa-facebook-f"></i></a>
                <a href="#"><i class="fab fa-twitter"></i></a>
                <a href="#"><i class="fab fa-linkedin-in"></i></a>
                <a href="#"><i class="fab fa-instagram"></i></a>
            </div>
            <div class="copyright">
                &copy; 2023 Cyrus Kuiyaki. All Rights Reserved.
            </div>
        </div>
    </footer>

    <script>
        // Mobile Navigation
        const hamburger = document.getElementById('hamburger');
        const navLinks = document.getElementById('navLinks');
        
        hamburger.addEventListener('click', () => {
            navLinks.classList.toggle('active');
        });
        
        // Smooth Scrolling
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                if (navLinks.classList.contains('active')) {
                    navLinks.classList.remove('active');
                }
                
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
        
        // Header Scroll Effect
        window.addEventListener('scroll', () => {
            const header = document.getElementById('header');
            if (window.scrollY > 50) {
                header.classList.add('scrolled');
            } else {
                header.classList.remove('scrolled');
            }
        });
        
        // Timeline Animation
        const timelineItems = document.querySelectorAll('.timeline-item');
        
        function checkTimeline() {
            const triggerBottom = window.innerHeight / 5 * 4;
            
            timelineItems.forEach(item => {
                const itemTop = item.getBoundingClientRect().top;
                
                if (itemTop < triggerBottom) {
                    item.classList.add('visible');
                }
            });
        }
        
        window.addEventListener('scroll', checkTimeline);
        checkTimeline(); // Check on load
        
        // Testimonial Slider
        const slides = document.querySelectorAll('.testimonial-slide');
        const dots = document.querySelectorAll('.slider-dot');
        let currentSlide = 0;
        
        function showSlide(n) {
            slides.forEach(slide => slide.classList.remove('active'));
            dots.forEach(dot => dot.classList.remove('active'));
            
            currentSlide = (n + slides.length) % slides.length;
            slides[currentSlide].classList.add('active');
            dots[currentSlide].classList.add('active');
        }
        
        dots.forEach((dot, index) => {
            dot.addEventListener('click', () => {
                showSlide(index);
            });
        });
        
        // Auto slide change
        setInterval(() => {
            showSlide(currentSlide + 1);
        }, 5000);
        
        // Form Submission
        const contactForm = document.getElementById('contactForm');
        
        contactForm.addEventListener('submit', (e) => {
            e.preventDefault();
            
            // Here you would typically send the form data to a server
            alert('Thank you for your message! Cyrus will get back to you soon.');
            contactForm.reset();
        });
    </script>
</body>
</html>
