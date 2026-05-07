# school..
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Green Valley School - Excellence in Education</title>
    
    <style>
        /* ==================== GLOBAL STYLES ==================== */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        /* Define CSS variables for easy color management */
        :root {
            --primary-blue: #2c3e50;
            --light-blue: #3498db;
            --sky-blue: #5dade2;
            --white: #ffffff;
            --light-gray: #ecf0f1;
            --dark-gray: #34495e;
            --accent-green: #27ae60;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: var(--dark-gray);
            background-color: var(--white);
        }

        /* ==================== HEADER & NAVIGATION ==================== */
        header {
            background-color: var(--primary-blue);
            color: var(--white);
            padding: 1rem 0;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }

        .header-container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 2rem;
        }

        .school-name {
            font-size: 1.8rem;
            font-weight: bold;
            letter-spacing: 1px;
        }

        /* Navigation Menu */
        nav ul {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        nav a {
            color: var(--white);
            text-decoration: none;
            font-size: 1rem;
            font-weight: 500;
            transition: color 0.3s ease;
            padding: 0.5rem 1rem;
            border-radius: 4px;
        }

        nav a:hover {
            color: var(--accent-green);
            background-color: rgba(255, 255, 255, 0.1);
            transform: translateY(-2px);
            transition: all 0.3s ease;
        }

        /* Mobile Menu Toggle Button */
        .menu-toggle {
            display: none;
            background: none;
            border: none;
            color: var(--white);
            font-size: 1.5rem;
            cursor: pointer;
        }

        /* ==================== HERO/HOME SECTION ==================== */
        .hero {
            background: linear-gradient(135deg, var(--light-blue) 0%, var(--sky-blue) 100%);
            color: var(--white);
            padding: 4rem 2rem;
            text-align: center;
            min-height: 500px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            background-image: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 600"><defs><pattern id="grid" width="40" height="40" patternUnits="userSpaceOnUse"><path d="M 40 0 L 0 0 0 40" fill="none" stroke="rgba(255,255,255,0.1)" stroke-width="1"/></pattern></defs><rect width="1200" height="600" fill="url(%23grid)"/></svg>');
        }

        .hero-content h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.2);
            animation: slideInDown 0.8s ease;
        }

        .hero-content p {
            font-size: 1.3rem;
            margin-bottom: 2rem;
            animation: slideInUp 0.8s ease;
        }

        .welcome-btn {
            background-color: var(--accent-green);
            color: var(--white);
            padding: 0.8rem 2rem;
            border: none;
            border-radius: 4px;
            font-size: 1rem;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }

        .welcome-btn:hover {
            background-color: #229954;
            transform: scale(1.05);
            box-shadow: 0 6px 8px rgba(0, 0, 0, 0.2);
        }

        .welcome-btn:active {
            transform: scale(0.98);
        }

        /* ==================== SECTION STYLES ==================== */
        section {
            padding: 3rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        section h2 {
            font-size: 2.2rem;
            color: var(--primary-blue);
            margin-bottom: 2rem;
            text-align: center;
            border-bottom: 3px solid var(--light-blue);
            padding-bottom: 1rem;
            display: inline-block;
            width: 100%;
        }

        /* ==================== ABOUT SECTION ==================== */
        .about-content {
            background-color: var(--light-gray);
            padding: 2rem;
            border-radius: 8px;
            border-left: 5px solid var(--light-blue);
            line-height: 1.8;
        }

        .about-content p {
            margin-bottom: 1rem;
            font-size: 1.05rem;
        }

        .about-highlights {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }

        .highlight {
            background-color: var(--white);
            padding: 1.5rem;
            border-radius: 8px;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
            text-align: center;
            transition: all 0.3s ease;
        }

        .highlight:hover {
            transform: translateY(-5px);
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
        }

        .highlight h3 {
            color: var(--light-blue);
            margin-bottom: 0.5rem;
        }

        /* ==================== COURSES SECTION ==================== */
        .courses-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }

        .course-card {
            background-color: var(--white);
            border: 2px solid var(--light-gray);
            border-radius: 8px;
            padding: 2rem;
            text-align: center;
            transition: all 0.3s ease;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
        }

        .course-card:hover {
            border-color: var(--light-blue);
            box-shadow: 0 4px 12px rgba(52, 152, 219, 0.2);
            transform: translateY(-8px);
        }

        .course-icon {
            font-size: 2.5rem;
            margin-bottom: 1rem;
        }

        .course-card h3 {
            color: var(--primary-blue);
            margin-bottom: 0.8rem;
            font-size: 1.3rem;
        }

        .course-card p {
            color: var(--dark-gray);
            line-height: 1.6;
            margin-bottom: 1rem;
        }

        .enroll-btn {
            background-color: var(--light-blue);
            color: var(--white);
            padding: 0.6rem 1.5rem;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-size: 0.95rem;
            font-weight: bold;
            transition: all 0.3s ease;
        }

        .enroll-btn:hover {
            background-color: var(--sky-blue);
            transform: scale(1.05);
        }

        /* ==================== CONTACT SECTION ==================== */
        .contact-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            align-items: start;
        }

        .contact-info {
            background-color: var(--light-gray);
            padding: 2rem;
            border-radius: 8px;
        }

        .contact-info h3 {
            color: var(--primary-blue);
            margin-bottom: 1.5rem;
            font-size: 1.3rem;
        }

        .contact-item {
            margin-bottom: 1.5rem;
            padding-bottom: 1rem;
            border-bottom: 1px solid #bdc3c7;
        }

        .contact-item:last-child {
            border-bottom: none;
        }

        .contact-item strong {
            color: var(--light-blue);
            display: block;
            margin-bottom: 0.3rem;
        }

        /* Contact Form */
        .contact-form {
            background-color: var(--light-gray);
            padding: 2rem;
            border-radius: 8px;
        }

        .contact-form h3 {
            color: var(--primary-blue);
            margin-bottom: 1.5rem;
            font-size: 1.3rem;
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 600;
            color: var(--primary-blue);
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 0.8rem;
            border: 2px solid #bdc3c7;
            border-radius: 4px;
            font-family: inherit;
            font-size: 1rem;
            transition: border-color 0.3s ease;
        }

        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: var(--light-blue);
            box-shadow: 0 0 5px rgba(52, 152, 219, 0.3);
        }

        .form-group textarea {
            resize: vertical;
            min-height: 120px;
        }

        .error-message {
            color: #e74c3c;
            font-size: 0.85rem;
            margin-top: 0.3rem;
            display: none;
        }

        .form-group.error input,
        .form-group.error textarea {
            border-color: #e74c3c;
        }

        .form-group.error .error-message {
            display: block;
        }

        .submit-btn {
            background-color: var(--accent-green);
            color: var(--white);
            padding: 0.8rem 2rem;
            border: none;
            border-radius: 4px;
            font-size: 1rem;
            font-weight: bold;
            cursor: pointer;
            width: 100%;
            transition: all 0.3s ease;
        }

        .submit-btn:hover {
            background-color: #229954;
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }

        .submit-btn:active {
            transform: translateY(0);
        }

        /* ==================== FOOTER ==================== */
        footer {
            background-color: var(--primary-blue);
            color: var(--white);
            text-align: center;
            padding: 2rem;
            margin-top: 3rem;
        }

        footer p {
            margin-bottom: 0.5rem;
        }

        /* ==================== ANIMATIONS ==================== */
        @keyframes slideInDown {
            from {
                opacity: 0;
                transform: translateY(-30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes slideInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* ==================== SUCCESS MESSAGE ==================== */
        .success-message {
            background-color: #d4edda;
            color: #155724;
            padding: 1rem;
            border-radius: 4px;
            margin-bottom: 1rem;
            display: none;
            border: 1px solid #c3e6cb;
        }

        .success-message.show {
            display: block;
            animation: slideInDown 0.5s ease;
        }

        /* ==================== RESPONSIVE DESIGN (MOBILE) ==================== */
        @media (max-width: 768px) {
            /* Header adjustments */
            .header-container {
                padding: 0 1rem;
            }

            .school-name {
                font-size: 1.4rem;
            }

            /* Mobile Menu */
            .menu-toggle {
                display: block;
            }

            nav {
                position: absolute;
                top: 60px;
                left: 0;
                right: 0;
                background-color: var(--primary-blue);
                max-height: 0;
                overflow: hidden;
                transition: max-height 0.3s ease;
            }

            nav.active {
                max-height: 300px;
            }

            nav ul {
                flex-direction: column;
                gap: 0;
                padding: 1rem 0;
            }

            nav a {
                display: block;
                padding: 1rem 2rem;
                border-radius: 0;
            }

            /* Hero section */
            .hero-content h1 {
                font-size: 2rem;
            }

            .hero-content p {
                font-size: 1rem;
            }

            .hero {
                min-height: 350px;
                padding: 2rem 1rem;
            }

            /* Sections */
            section {
                padding: 2rem 1rem;
            }

            section h2 {
                font-size: 1.7rem;
            }

            /* Contact layout */
            .contact-container {
                grid-template-columns: 1fr;
                gap: 2rem;
            }

            /* About highlights */
            .about-highlights {
                grid-template-columns: 1fr;
            }

            /* Courses grid */
            .courses-container {
                grid-template-columns: 1fr;
            }

            /* Welcome message modal */
            .welcome-modal {
                width: 90% !important;
            }
        }

        @media (max-width: 480px) {
            .school-name {
                font-size: 1.2rem;
            }

            .hero-content h1 {
                font-size: 1.5rem;
            }

            .hero-content p {
                font-size: 0.9rem;
            }

            section h2 {
                font-size: 1.4rem;
            }

            nav a {
                padding: 0.8rem 1.5rem;
            }
        }

        /* ==================== MODAL STYLES ==================== */
        .modal {
            display: none;
            position: fixed;
            z-index: 1000;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.4);
            animation: fadeIn 0.3s ease;
        }

        .modal.show {
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .modal-content {
            background-color: var(--white);
            padding: 2rem;
            border-radius: 8px;
            max-width: 500px;
            width: 90%;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.3);
            text-align: center;
            animation: slideInDown 0.3s ease;
        }

        .modal-content h2 {
            color: var(--primary-blue);
            margin-bottom: 1rem;
            font-size: 1.8rem;
        }

        .modal-content p {
            color: var(--dark-gray);
            margin-bottom: 2rem;
            font-size: 1.1rem;
        }

        .close-btn {
            background-color: var(--light-blue);
            color: var(--white);
            padding: 0.6rem 1.5rem;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-size: 1rem;
            font-weight: bold;
            transition: all 0.3s ease;
        }

        .close-btn:hover {
            background-color: var(--sky-blue);
            transform: scale(1.05);
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
            }
            to {
                opacity: 1;
            }
        }
    </style>
</head>
<body>
    <!-- ==================== HEADER & NAVIGATION ==================== -->
    <header>
        <div class="header-container">
            <div class="school-name">🏫 Green Valley School</div>
            <button class="menu-toggle" id="menuToggle">☰</button>
            <nav id="navMenu">
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#courses">Courses</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- ==================== HERO/HOME SECTION ==================== -->
    <section id="home" class="hero">
        <div class="hero-content">
            <h1>Welcome to Green Valley School</h1>
            <p>Excellence in Education • Innovation in Learning • Building Future Leaders</p>
            <button class="welcome-btn" id="welcomeBtn">Learn More</button>
        </div>
    </section>

    <!-- ==================== ABOUT SECTION ==================== -->
    <section id="about">
        <h2>About Our School</h2>
        <div class="about-content">
            <p>
                Green Valley School is a leading educational institution dedicated to providing high-quality education 
                to students from kindergarten through high school. With over 20 years of experience in education, we have 
                established ourselves as a beacon of academic excellence and holistic development.
            </p>
            <p>
                Our mission is to nurture young minds, foster creativity, and prepare students for success in an 
                ever-changing world. We believe in a balanced approach to education that combines traditional academics 
                with modern learning techniques and life skills.
            </p>
        </div>
        
        <div class="about-highlights">
            <div class="highlight">
                <h3>📚 Academic Excellence</h3>
                <p>Rigorous curriculum designed to foster critical thinking and problem-solving skills.</p>
            </div>
            <div class="highlight">
                <h3>👨‍🏫 Expert Faculty</h3>
                <p>Highly qualified teachers with years of experience in their respective fields.</p>
            </div>
            <div class="highlight">
                <h3>🏆 Modern Facilities</h3>
                <p>State-of-the-art classrooms, laboratories, and recreational facilities.</p>
            </div>
            <div class="highlight">
                <h3>🌍 Global Perspective</h3>
                <p>International exchange programs and multicultural learning environment.</p>
            </div>
        </div>
    </section>

    <!-- ==================== COURSES SECTION ==================== -->
    <section id="courses">
        <h2>Our Courses</h2>
        <div class="courses-container">
            <!-- Course Card 1 -->
            <div class="course-card">
                <div class="course-icon">📖</div>
                <h3>English & Literature</h3>
                <p>
                    Develop strong communication and writing skills. Learn classic and contemporary literature, 
                    improve grammar, and build confidence in public speaking.
                </p>
                <button class="enroll-btn">Enroll Now</button>
            </div>

            <!-- Course Card 2 -->
            <div class="course-card">
                <div class="course-icon">🔬</div>
                <h3>Science & Technology</h3>
                <p>
                    Explore the wonders of physics, chemistry, and biology. Engage in hands-on experiments and 
                    learn how science shapes our world.
                </p>
                <button class="enroll-btn">Enroll Now</button>
            </div>

            <!-- Course Card 3 -->
            <div class="course-card">
                <div class="course-icon">🧮</div>
                <h3>Mathematics</h3>
                <p>
                    Master fundamental and advanced mathematical concepts. From algebra to calculus, develop 
                    problem-solving abilities and logical reasoning.
                </p>
                <button class="enroll-btn">Enroll Now</button>
            </div>

            <!-- Course Card 4 -->
            <div class="course-card">
                <div class="course-icon">🎨</div>
                <h3>Arts & Creativity</h3>
                <p>
                    Express yourself through painting, drawing, sculpture, and digital art. Develop creative thinking 
                    and artistic skills in a supportive environment.
                </p>
                <button class="enroll-btn">Enroll Now</button>
            </div>

            <!-- Course Card 5 -->
            <div class="course-card">
                <div class="course-icon">🏃</div>
                <h3>Physical Education</h3>
                <p>
                    Stay fit and healthy through sports and fitness programs. Learn teamwork, discipline, and develop 
                    a lifelong commitment to wellness.
                </p>
                <button class="enroll-btn">Enroll Now</button>
            </div>

            <!-- Course Card 6 -->
            <div class="course-card">
                <div class="course-icon">💻</div>
                <h3>Computer Science</h3>
                <p>
                    Learn programming, web development, and digital literacy. Master modern technology skills essential 
                    for the digital age.
                </p>
                <button class="enroll-btn">Enroll Now</button>
            </div>
        </div>
    </section>

    <!-- ==================== CONTACT SECTION ==================== -->
    <section id="contact">
        <h2>Contact Us</h2>
        <div class="contact-container">
            <!-- Contact Information -->
            <div class="contact-info">
                <h3>Get In Touch</h3>
                <div class="contact-item">
                    <strong>📍 Location:</strong>
                    <p>123 Education Road, Valley City, VC 12345</p>
                </div>
                <div class="contact-item">
                    <strong>📞 Phone:</strong>
                    <p>+1 (555) 123-4567</p>
                </div>
                <div class="contact-item">
                    <strong>📧 Email:</strong>
                    <p>info@greenvalleyschool.edu</p>
                </div>
                <div class="contact-item">
                    <strong>🕒 Office Hours:</strong>
                    <p>Monday - Friday: 8:00 AM - 4:00 PM</p>
                    <p>Saturday: 9:00 AM - 1:00 PM</p>
                </div>
            </div>

            <!-- Contact Form -->
            <div class="contact-form">
                <h3>Send us a Message</h3>
                <div class="success-message" id="successMessage">
                    ✓ Thank you! Your message has been sent successfully. We'll get back to you soon.
                </div>
                <form id="contactForm">
                    <!-- Name Field -->
                    <div class="form-group">
                        <label for="name">Full Name</label>
                        <input type="text" id="name" name="name" placeholder="Enter your full name">
                        <span class="error-message">Please enter your name</span>
                    </div>

                    <!-- Email Field -->
                    <div class="form-group">
                        <label for="email">Email Address</label>
                        <input type="email" id="email" name="email" placeholder="Enter your email">
                        <span class="error-message">Please enter a valid email address</span>
                    </div>

                    <!-- Message Field -->
                    <div class="form-group">
                        <label for="message">Message</label>
                        <textarea id="message" name="message" placeholder="Type your message here..."></textarea>
                        <span class="error-message">Please enter your message</span>
                    </div>

                    <!-- Submit Button -->
                    <button type="submit" class="submit-btn">Send Message</button>
                </form>
            </div>
        </div>
    </section>

    <!-- ==================== WELCOME MODAL ==================== -->
    <div class="modal" id="welcomeModal">
        <div class="modal-content welcome-modal">
            <h2>🎉 Welcome to Green Valley School!</h2>
            <p>
                We're excited to have you here. Green Valley School is committed to providing an exceptional 
                educational experience that prepares students for success. Join us on this amazing journey of 
                learning and growth!
            </p>
            <button class="close-btn" id="closeModal">Close</button>
        </div>
    </div>

    <!-- ==================== FOOTER ==================== -->
    <footer>
        <p>&copy; 2024 Green Valley School. All rights reserved.</p>
        <p>Excellence in Education • Innovation in Learning</p>
    </footer>

    <!-- ==================== JAVASCRIPT ==================== -->
    <script>
        // ==================== MOBILE MENU TOGGLE ====================
        // This JavaScript code handles the responsive mobile menu functionality
        
        const menuToggle = document.getElementById('menuToggle');
        const navMenu = document.getElementById('navMenu');
        
        // Toggle menu when hamburger button is clicked
        menuToggle.addEventListener('click', () => {
            navMenu.classList.toggle('active');
        });
        
        // Close menu when a navigation link is clicked
        const navLinks = navMenu.querySelectorAll('a');
        navLinks.forEach(link => {
            link.addEventListener('click', () => {
                navMenu.classList.remove('active');
            });
        });

        // ==================== WELCOME BUTTON & MODAL ====================
        // This section handles the welcome message modal popup
        
        const welcomeBtn = document.getElementById('welcomeBtn');
        const welcomeModal = document.getElementById('welcomeModal');
        const closeModal = document.getElementById('closeModal');
        
        // Show modal when welcome button is clicked
        welcomeBtn.addEventListener('click', () => {
            welcomeModal.classList.add('show');
        });
        
        // Close modal when close button is clicked
        closeModal.addEventListener('click', () => {
            welcomeModal.classList.remove('show');
        });
        
        // Close modal when clicking outside of it
        window.addEventListener('click', (event) => {
            if (event.target === welcomeModal) {
                welcomeModal.classList.remove('show');
            }
        });

        // ==================== CONTACT FORM VALIDATION ====================
        // This section handles form validation and submission
        
        const contactForm = document.getElementById('contactForm');
        const successMessage = document.getElementById('successMessage');
        const nameInput = document.getElementById('name');
        const emailInput = document.getElementById('email');
        const messageInput = document.getElementById('message');
        
        // Email validation function - checks if email format is valid
        function isValidEmail(email) {
            // Regular expression to check for valid email format
            const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
            return emailRegex.test(email);
        }
        
        // Function to show error for a form field
        function showError(input) {
            const formGroup = input.parentElement;
            formGroup.classList.add('error');
        }
        
        // Function to hide error for a form field
        function hideError(input) {
            const formGroup = input.parentElement;
            formGroup.classList.remove('error');
        }
        
        // Validate form fields when user leaves the field (blur event)
        nameInput.addEventListener('blur', () => {
            if (nameInput.value.trim() === '') {
                showError(nameInput);
            } else {
                hideError(nameInput);
            }
        });
        
        emailInput.addEventListener('blur', () => {
            if (emailInput.value.trim() === '' || !isValidEmail(emailInput.value)) {
                showError(emailInput);
            } else {
                hideError(emailInput);
            }
        });
        
        messageInput.addEventListener('blur', () => {
            if (messageInput.value.trim() === '') {
                showError(messageInput);
            } else {
                hideError(messageInput);
            }
        });
        
        // Handle form submission
        contactForm.addEventListener('submit', (event) => {
            // Prevent default form submission behavior
            event.preventDefault();
            
            // Clear all previous errors
            document.querySelectorAll('.form-group').forEach(group => {
                group.classList.remove('error');
            });
            
            // Validate all fields
            let isValid = true;
            
            // Validate name field
            if (nameInput.value.trim() === '') {
                showError(nameInput);
                isValid = false;
            }
            
            // Validate email field
            if (emailInput.value.trim() === '' || !isValidEmail(emailInput.value)) {
                showError(emailInput);
                isValid = false;
            }
            
            // Validate message field
            if (messageInput.value.trim() === '') {
                showError(messageInput);
                isValid = false;
            }
            
            // If all fields are valid, show success message
            if (isValid) {
                // Show success message with animation
                successMessage.classList.add('show');
                
                // Display alert to user
                alert('Thank you for contacting us!\n\nName: ' + nameInput.value + 
                      '\nEmail: ' + emailInput.value + 
                      '\n\nWe will get back to you soon!');
                
                // Clear form fields
                contactForm.reset();
                
                // Hide success message after 5 seconds
                setTimeout(() => {
                    successMessage.classList.remove('show');
                }, 5000);
            }
        });

        // ==================== SMOOTH SCROLLING ====================
        // This section adds smooth scrolling to navigation links
        
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (event) {
                const href = this.getAttribute('href');
                
                // Only apply smooth scroll for internal links (not just "#")
                if (href !== '#') {
                    event.preventDefault();
                    
                    const target = document.querySelector(href);
                    if (target) {
                        target.scrollIntoView({
                            behavior: 'smooth',
                            block: 'start'
                        });
                    }
                }
            });
        });

        // ==================== COURSE ENROLL BUTTON ====================
        // This section handles course enrollment buttons
        
        const enrollBtns = document.querySelectorAll('.enroll-btn');
        
        // Add click event to all enroll buttons
        enrollBtns.forEach(btn => {
            btn.addEventListener('click', () => {
                alert('Thank you for your interest!\n\nPlease fill out the contact form below to complete your enrollment.');
                
                // Scroll to contact section
                document.getElementById('contact').scrollIntoView({ behavior: 'smooth' });
            });
        });
    </script>
</body>
</html>
