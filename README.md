# seosem-website
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>WebAudit Pro | Free SEO & SEM Analysis</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #4361ee;
            --secondary: #3a0ca3;
            --accent: #4cc9f0;
            --light: #f8f9fa;
            --dark: #212529;
            --success: #4bb543;
            --warning: #ff9e00;
            --danger: #e63946;
            --gray: #6c757d;
            --light-gray: #e9ecef;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            line-height: 1.6;
            color: var(--dark);
            background-color: #f5f7ff;
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }
        
        /* Header Styles */
        header {
            background-color: white;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem 0;
        }
        
        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--primary);
            display: flex;
            align-items: center;
        }
        
        .logo i {
            margin-right: 10px;
            color: var(--accent);
        }
        
        .nav-links {
            display: flex;
            list-style: none;
        }
        
        .nav-links li {
            margin-left: 2rem;
        }
        
        .nav-links a {
            text-decoration: none;
            color: var(--dark);
            font-weight: 500;
            transition: color 0.3s;
        }
        
        .nav-links a:hover {
            color: var(--primary);
        }
        
        .btn {
            display: inline-block;
            padding: 0.8rem 1.5rem;
            background-color: var(--primary);
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-weight: 600;
            text-decoration: none;
            transition: all 0.3s;
        }
        
        .btn:hover {
            background-color: var(--secondary);
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }
        
        .btn-outline {
            background-color: transparent;
            border: 2px solid var(--primary);
            color: var(--primary);
        }
        
        .btn-outline:hover {
            background-color: var(--primary);
            color: white;
        }
        
        /* Hero Section */
        .hero {
            padding: 5rem 0;
            background: linear-gradient(135deg, #4361ee 0%, #3a0ca3 100%);
            color: white;
            text-align: center;
        }
        
        .hero h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
        }
        
        .hero p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 2rem;
            opacity: 0.9;
        }
        
        .hero-btns {
            display: flex;
            justify-content: center;
            gap: 1rem;
            margin-top: 2rem;
        }
        
        .hero-btns .btn {
            background-color: white;
            color: var(--primary);
        }
        
        .hero-btns .btn:hover {
            background-color: var(--light-gray);
        }
        
        /* Tabs Section */
        .tabs-section {
            padding: 4rem 0;
            background-color: white;
        }
        
        .tabs-header {
            text-align: center;
            margin-bottom: 3rem;
        }
        
        .tabs-header h2 {
            font-size: 2.5rem;
            color: var(--secondary);
            margin-bottom: 1rem;
        }
        
        .tabs-header p {
            color: var(--gray);
            max-width: 700px;
            margin: 0 auto;
        }
        
        .tabs {
            display: flex;
            justify-content: center;
            margin-bottom: 2rem;
            border-bottom: 1px solid var(--light-gray);
        }
        
        .tab-btn {
            padding: 1rem 2rem;
            background: none;
            border: none;
            font-size: 1.1rem;
            font-weight: 600;
            color: var(--gray);
            cursor: pointer;
            position: relative;
            transition: all 0.3s;
        }
        
        .tab-btn.active {
            color: var(--primary);
        }
        
        .tab-btn.active::after {
            content: '';
            position: absolute;
            bottom: -1px;
            left: 0;
            width: 100%;
            height: 3px;
            background-color: var(--primary);
        }
        
        .tab-content {
            display: none;
        }
        
        .tab-content.active {
            display: block;
            animation: fadeIn 0.5s ease;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        
        /* Comparison Section */
        .comparison {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 2rem;
            margin-bottom: 3rem;
        }
        
        .comparison-card {
            background-color: var(--light);
            border-radius: 10px;
            padding: 2rem;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
        }
        
        .comparison-card h3 {
            color: var(--secondary);
            margin-bottom: 1.5rem;
            padding-bottom: 0.5rem;
            border-bottom: 2px solid var(--accent);
        }
        
        .comparison-list {
            list-style: none;
        }
        
        .comparison-list li {
            margin-bottom: 1rem;
            padding-left: 1.5rem;
            position: relative;
        }
        
        .comparison-list li:before {
            content: '•';
            position: absolute;
            left: 0;
            color: var(--primary);
            font-weight: bold;
        }
        
        /* Features Section */
        .features {
            margin: 3rem 0;
        }
        
        .features h3 {
            color: var(--secondary);
            margin-bottom: 1.5rem;
            text-align: center;
        }
        
        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5rem;
        }
        
        .feature-card {
            background-color: white;
            border-radius: 10px;
            padding: 1.5rem;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            text-align: center;
            transition: transform 0.3s;
        }
        
        .feature-card:hover {
            transform: translateY(-5px);
        }
        
        .feature-icon {
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 1rem;
        }
        
        .feature-card h4 {
            margin-bottom: 0.5rem;
            color: var(--secondary);
        }
        
        /* Process Section */
        .process {
            background-color: var(--light);
            padding: 4rem 0;
        }
        
        .process h2 {
            text-align: center;
            color: var(--secondary);
            margin-bottom: 3rem;
        }
        
        .process-steps {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
        }
        
        .step {
            text-align: center;
            padding: 2rem 1rem;
        }
        
        .step-number {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 60px;
            height: 60px;
            background-color: var(--primary);
            color: white;
            border-radius: 50%;
            font-size: 1.5rem;
            font-weight: bold;
            margin-bottom: 1.5rem;
        }
        
        .step h3 {
            color: var(--secondary);
            margin-bottom: 1rem;
        }
        
        /* CTA Section */
        .cta {
            padding: 5rem 0;
            background: linear-gradient(135deg, #3a0ca3 0%, #4361ee 100%);
            color: white;
            text-align: center;
        }
        
        .cta h2 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
        }
        
        .cta p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 2rem;
            opacity: 0.9;
        }
        
        .cta-form {
            max-width: 500px;
            margin: 0 auto;
        }
        
        .form-group {
            margin-bottom: 1.5rem;
            text-align: left;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 500;
        }
        
        .form-control {
            width: 100%;
            padding: 0.8rem 1rem;
            border: none;
            border-radius: 5px;
            font-size: 1rem;
        }
        
        /* Footer */
        footer {
            background-color: var(--dark);
            color: white;
            padding: 3rem 0 1.5rem;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
            margin-bottom: 2rem;
        }
        
        .footer-column h3 {
            color: var(--accent);
            margin-bottom: 1.5rem;
            font-size: 1.2rem;
        }
        
        .footer-links {
            list-style: none;
        }
        
        .footer-links li {
            margin-bottom: 0.8rem;
        }
        
        .footer-links a {
            color: var(--light-gray);
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-links a:hover {
            color: var(--accent);
        }
        
        .copyright {
            text-align: center;
            padding-top: 1.5rem;
            border-top: 1px solid rgba(255,255,255,0.1);
            color: var(--gray);
            font-size: 0.9rem;
        }
        
        /* Responsive Styles */
        @media (max-width: 768px) {
            .navbar {
                flex-direction: column;
            }
            
            .nav-links {
                margin-top: 1rem;
            }
            
            .nav-links li {
                margin-left: 1rem;
                margin-right: 1rem;
            }
            
            .hero h1 {
                font-size: 2.2rem;
            }
            
            .comparison {
                grid-template-columns: 1fr;
            }
            
            .tabs {
                flex-direction: column;
            }
            
            .tab-btn {
                width: 100%;
                text-align: center;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <nav class="navbar">
                <div class="logo">
                    <i class="fas fa-chart-line"></i>
                    WebAudit Pro
                </div>
                <ul class="nav-links">
                    <li><a href="#home">Home</a></li>
                    <li><a href="#features">Features</a></li>
                    <li><a href="#seo">SEO Audit</a></li>
                    <li><a href="#sem">SEM Audit</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
                <a href="#audit" class="btn">Get Free Audit</a>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container">
            <h1>Free Professional Website Audit</h1>
            <p>Get comprehensive SEO and SEM analysis to improve your website's performance and drive more traffic to your business.</p>
            <div class="hero-btns">
                <a href="#seo" class="btn">SEO Audit</a>
                <a href="#sem" class="btn">SEM Audit</a>
            </div>
        </div>
    </section>

    <!-- Tabs Section -->
    <section class="tabs-section" id="features">
        <div class="container">
            <div class="tabs-header">
                <h2>Comprehensive Website Analysis</h2>
                <p>Our free audit tools provide detailed insights into your website's SEO and SEM performance</p>
            </div>
            
            <div class="tabs">
                <button class="tab-btn active" data-tab="seo">SEO Technical Audit</button>
                <button class="tab-btn" data-tab="sem">SEM Performance Audit</button>
            </div>
            
            <!-- SEO Tab Content -->
            <div class="tab-content active" id="seo-content">
                <h3>How do search engines work?</h3>
                
                <div class="process">
                    <div class="process-steps">
                        <div class="step">
                            <div class="step-number">1</div>
                            <h3>Crawling</h3>
                            <p>Search engines send out the spider to <strong>crawl</strong> your website</p>
                        </div>
                        <div class="step">
                            <div class="step-number">2</div>
                            <h3>Indexing</h3>
                            <p>Search engine determine whether the pages will be indexed into their database according to <strong>performance and content quality</strong></p>
                        </div>
                        <div class="step">
                            <div class="step-number">3</div>
                            <h3>Ranking</h3>
                            <p>Search engines assign a page rank according to various factors related to content relevant and website authority</p>
                        </div>
                    </div>
                </div>
                
                <div class="features">
                    <h3>What will be included in the SEO Technical Audit?</h3>
                    <div class="features-grid">
                        <div class="feature-card">
                            <div class="feature-icon">
                                <i class="fas fa-spider"></i>
                            </div>
                            <h4>Crawl Analysis</h4>
                            <p>Crawling entrance, link issues, site structure</p>
                        </div>
                        <div class="feature-card">
                            <div class="feature-icon">
                                <i class="fas fa-database"></i>
                            </div>
                            <h4>Index Evaluation</h4>
                            <p>Loading speed, content uniqueness, technical performance</p>
                        </div>
                        <div class="feature-card">
                            <div class="feature-icon">
                                <i class="fas fa-trophy"></i>
                            </div>
                            <h4>Rank Assessment</h4>
                            <p>Domain authority, security, on-page elements, mobile friendliness</p>
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- SEM Tab Content -->
            <div class="tab-content" id="sem-content">
                <h3>How AdWords Performance Audit System Help You in Your Business?</h3>
                
                <div class="comparison">
                    <div class="comparison-card">
                        <h3>Before: Optimization is complicated and time-consuming</h3>
                        <ul class="comparison-list">
                            <li>Poor visualization of account health status</li>
                            <li>Optimization is arbitrary without clear direction</li>
                            <li>Hard to measure your optimized results</li>
                        </ul>
                    </div>
                    <div class="comparison-card">
                        <h3>Now: Real-time Analysis with YouFind Analytics</h3>
                        <ul class="comparison-list">
                            <li>Comparing through benchmarking</li>
                            <li>Best practices optimization</li>
                            <li>Provide insightful/actionable recommendations</li>
                        </ul>
                    </div>
                </div>
                
                <div class="features">
                    <h3>What will be included in the AdWords Performance Audit?</h3>
                    <div class="features-grid">
                        <div class="feature-card">
                            <div class="feature-icon">
                                <i class="fas fa-chart-bar"></i>
                            </div>
                            <h4>Google Ads Performance Grade</h4>
                            <p>Comprehensive scoring of your ad account performance</p>
                        </div>
                        <div class="feature-card">
                            <div class="feature-icon">
                                <i class="fas fa-cogs"></i>
                            </div>
                            <h4>Account Performance</h4>
                            <p>Active campaigns, ad groups, keywords, and more</p>
                        </div>
                        <div class="feature-card">
                            <div class="feature-icon">
                                <i class="fas fa-key"></i>
                            </div>
                            <h4>Keywords Performance</h4>
                            <p>Quality score analysis and performance summary</p>
                        </div>
                        <div class="feature-card">
                            <div class="feature-icon">
                                <i class="fas fa-piggy-bank"></i>
                            </div>
                            <h4>Cost & Conversion Analysis</h4>
                            <p>Potential cost savings, CTR, conversion rates, and more</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- CTA Section -->
    <section class="cta" id="audit">
        <div class="container">
            <h2>Get Your Free Website Audit Now</h2>
            <p>Submit your website URL and email to receive a comprehensive SEO and SEM analysis report</p>
            
            <form class="cta-form">
                <div class="form-group">
                    <label for="website">Website URL</label>
                    <input type="url" id="website" class="form-control" placeholder="https://example.com" required>
                </div>
                <div class="form-group">
                    <label for="email">Email Address</label>
                    <input type="email" id="email" class="form-control" placeholder="your@email.com" required>
                </div>
                <div class="form-group">
                    <label for="audit-type">Audit Type</label>
                    <select id="audit-type" class="form-control">
                        <option value="seo">SEO Technical Audit</option>
                        <option value="sem">SEM Performance Audit</option>
                        <option value="both">Both SEO & SEM Audit</option>
                    </select>
                </div>
                <button type="submit" class="btn" style="background-color: white; color: var(--primary); width: 100%;">Get Free Audit Report</button>
            </form>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>WebAudit Pro</h3>
                    <p>Providing professional website analysis tools to help businesses improve their online presence.</p>
                </div>
                <div class="footer-column">
                    <h3>Quick Links</h3>
                    <ul class="footer-links">
                        <li><a href="#home">Home</a></li>
                        <li><a href="#features">Features</a></li>
                        <li><a href="#seo">SEO Audit</a></li>
                        <li><a href="#sem">SEM Audit</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Services</h3>
                    <ul class="footer-links">
                        <li><a href="#">Free Website Audit</a></li>
                        <li><a href="#">SEO Consulting</a></li>
                        <li><a href="#">SEM Management</a></li>
                        <li><a href="#">Performance Tracking</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Contact Us</h3>
                    <ul class="footer-links">
                        <li><a href="mailto:info@webauditpro.com">info@webauditpro.com</a></li>
                        <li><a href="#">Support Center</a></li>
                        <li><a href="#">Live Chat</a></li>
                    </ul>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2023 WebAudit Pro. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <script>
        // Tab functionality
        document.addEventListener('DOMContentLoaded', function() {
            const tabBtns = document.querySelectorAll('.tab-btn');
            const tabContents = document.querySelectorAll('.tab-content');
            
            tabBtns.forEach(btn => {
                btn.addEventListener('click', () => {
                    // Remove active class from all buttons and contents
                    tabBtns.forEach(b => b.classList.remove('active'));
                    tabContents.forEach(c => c.classList.remove('active'));
                    
                    // Add active class to clicked button
                    btn.classList.add('active');
                    
                    // Show corresponding content
                    const tabId = btn.getAttribute('data-tab') + '-content';
                    document.getElementById(tabId).classList.add('active');
                });
            });
            
            // Form submission
            const form = document.querySelector('.cta-form');
            form.addEventListener('submit', function(e) {
                e.preventDefault();
                alert('Thank you for your request! Your free audit report will be sent to your email shortly.');
                form.reset();
            });
        });
    </script>
</body>
</html>
