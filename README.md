<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Digital Studio Marketplace - Professional Design & Development Services</title>
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
            background-color: #f8f9fa;
        }

        /* Navbar Styling */
        navbar {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 1rem 0;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .navbar-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: bold;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .logo-icon {
            width: 40px;
            height: 40px;
            background: rgba(255, 255, 255, 0.2);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
        }

        .navbar-buttons {
            display: flex;
            gap: 15px;
            align-items: center;
        }

        .language-btn, .signup-btn {
            padding: 0.6rem 1.2rem;
            border: 2px solid white;
            background: transparent;
            color: white;
            cursor: pointer;
            border-radius: 25px;
            font-size: 0.95rem;
            transition: all 0.3s ease;
        }

        .language-btn:hover {
            background: rgba(255, 255, 255, 0.2);
        }

        .signup-btn {
            background: white;
            color: #667eea;
            border-color: white;
            font-weight: 600;
        }

        .signup-btn:hover {
            background: #f0f0f0;
            transform: translateY(-2px);
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 100px 20px;
            text-align: center;
        }

        .hero-content {
            max-width: 1200px;
            margin: 0 auto;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            font-weight: 700;
            line-height: 1.2;
        }

        .hero p {
            font-size: 1.3rem;
            margin-bottom: 2rem;
            opacity: 0.95;
            max-width: 700px;
            margin-left: auto;
            margin-right: auto;
        }

        .cta-button {
            display: inline-block;
            background: white;
            color: #667eea;
            padding: 1rem 2.5rem;
            border: none;
            border-radius: 50px;
            font-size: 1.1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
        }

        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 20px rgba(0, 0, 0, 0.3);
        }

        /* Categories Section */
        .categories-section {
            max-width: 1200px;
            margin: 80px auto;
            padding: 0 20px;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            color: #333;
            margin-bottom: 3rem;
            font-weight: 700;
        }

        .categories-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }

        .category-card {
            background: white;
            border-radius: 15px;
            padding: 30px;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
            transition: all 0.3s ease;
            cursor: pointer;
        }

        .category-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(102, 126, 234, 0.2);
        }

        .category-icon {
            font-size: 3.5rem;
            margin-bottom: 15px;
        }

        .category-card h3 {
            font-size: 1.3rem;
            color: #333;
            margin-bottom: 0.5rem;
        }

        .category-card p {
            color: #666;
            font-size: 0.95rem;
        }

        /* Simulation Section */
        .simulation-section {
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            padding: 80px 20px;
            margin: 80px 0;
        }

        .simulation-container {
            max-width: 1200px;
            margin: 0 auto;
        }

        .simulation-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 40px;
            align-items: start;
        }

        .simulation-form {
            background: white;
            padding: 40px;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }

        .simulation-form h2 {
            font-size: 2rem;
            color: #333;
            margin-bottom: 2rem;
            font-weight: 700;
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            color: #333;
            font-weight: 600;
            font-size: 0.95rem;
        }

        .form-group input {
            width: 100%;
            padding: 0.8rem;
            border: 2px solid #e0e0e0;
            border-radius: 8px;
            font-size: 1rem;
            transition: border-color 0.3s ease;
        }

        .form-group input:focus {
            outline: none;
            border-color: #667eea;
            box-shadow: 0 0 0 3px rgba(102, 126, 234, 0.1);
        }

        .input-suffix {
            color: #666;
            font-size: 0.85rem;
            margin-top: 0.3rem;
        }

        .simulate-btn {
            width: 100%;
            padding: 1rem;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            border: none;
            border-radius: 8px;
            font-size: 1.1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            margin-top: 1rem;
        }

        .simulate-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 20px rgba(102, 126, 234, 0.3);
        }

        .simulate-btn:active {
            transform: translateY(0);
        }

        /* Results Section */
        .results-display {
            background: white;
            padding: 40px;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            display: none;
        }

        .results-display.active {
            display: block;
        }

        .results-display h2 {
            font-size: 2rem;
            color: #333;
            margin-bottom: 2rem;
            font-weight: 700;
        }

        .results-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
            margin-bottom: 2rem;
        }

        .result-card {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 25px;
            border-radius: 10px;
        }

        .result-label {
            font-size: 0.9rem;
            opacity: 0.9;
            margin-bottom: 0.5rem;
        }

        .result-value {
            font-size: 2rem;
            font-weight: 700;
        }

        .chart-container {
            margin-top: 2rem;
            position: relative;
            height: 300px;
            background: #f8f9fa;
            border-radius: 10px;
            padding: 20px;
        }

        canvas {
            max-width: 100%;
        }

        /* Footer */
        footer {
            background: #2c3e50;
            color: #ecf0f1;
            padding: 60px 20px 20px;
            margin-top: 80px;
        }

        .footer-container {
            max-width: 1200px;
            margin: 0 auto;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 2rem;
        }

        .footer-section h3 {
            font-size: 1.2rem;
            margin-bottom: 1rem;
            color: white;
            font-weight: 700;
        }

        .footer-section p {
            color: #bdc3c7;
            font-size: 0.95rem;
            line-height: 1.8;
        }

        .footer-section ul {
            list-style: none;
        }

        .footer-section ul li {
            margin-bottom: 0.8rem;
        }

        .footer-section ul li a {
            color: #bdc3c7;
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .footer-section ul li a:hover {
            color: #667eea;
        }

        .footer-bottom {
            border-top: 1px solid #34495e;
            padding-top: 2rem;
            text-align: center;
            color: #95a5a6;
            font-size: 0.9rem;
        }

        .footer-bottom p {
            margin-bottom: 0.5rem;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.5rem;
            }

            .hero p {
                font-size: 1rem;
            }

            .section-title {
                font-size: 2rem;
            }

            .categories-grid {
                grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
                gap: 20px;
            }

            .simulation-content {
                grid-template-columns: 1fr;
            }

            .results-grid {
                grid-template-columns: 1fr;
            }

            .navbar-buttons {
                gap: 10px;
            }

            .language-btn, .signup-btn {
                padding: 0.5rem 1rem;
                font-size: 0.85rem;
            }
        }

        @media (max-width: 480px) {
            .hero {
                padding: 50px 20px;
            }

            .hero h1 {
                font-size: 1.8rem;
            }

            .section-title {
                font-size: 1.5rem;
            }

            .simulation-form {
                padding: 20px;
            }

            .navbar-container {
                flex-direction: column;
                gap: 15px;
            }
        }

        /* Loading and error states */
        .error-message {
            color: #e74c3c;
            font-size: 0.9rem;
            margin-top: 0.5rem;
            display: none;
        }

        .error-message.show {
            display: block;
        }
    </style>
</head>
<body>
    <!-- Navbar -->
    <navbar>
        <div class="navbar-container">
            <div class="logo">
                <div class="logo-icon">🎨</div>
                <span>Digital Studio</span>
            </div>
            <div class="navbar-buttons">
                <button class="language-btn">🌐 English</button>
                <button class="signup-btn">Sign Up</button>
            </div>
        </div>
    </navbar>

    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-content">
            <h1>Transform Your Digital Vision Into Reality</h1>
            <p>Connect with talented designers, developers, and creative professionals. Launch, scale, and manage your digital projects with our marketplace ecosystem.</p>
            <button class="cta-button" id="scrollToSimulation">Start Simulation</button>
        </div>
    </section>

    <!-- Categories Section -->
    <section class="categories-section">
        <h2 class="section-title">Browse Our Categories</h2>
        <div class="categories-grid">
            <div class="category-card">
                <div class="category-icon">🎨</div>
                <h3>Logo Design</h3>
                <p>Professional brand identity creation</p>
            </div>
            <div class="category-card">
                <div class="category-icon">🌐</div>
                <h3>Web Development</h3>
                <p>Custom website and web app development</p>
            </div>
            <div class="category-card">
                <div class="category-icon">📱</div>
                <h3>Mobile Apps</h3>
                <p>iOS and Android application development</p>
            </div>
            <div class="category-card">
                <div class="category-icon">📊</div>
                <h3>UI/UX Design</h3>
                <p>User interface and experience design</p>
            </div>
            <div class="category-card">
                <div class="category-icon">🎬</div>
                <h3>Video Production</h3>
                <p>Professional video creation and editing</p>
            </div>
            <div class="category-card">
                <div class="category-icon">✍️</div>
                <h3>Content Writing</h3>
                <p>SEO-optimized content creation</p>
            </div>
            <div class="category-card">
                <div class="category-icon">🎙️</div>
                <h3>Audio Production</h3>
                <p>Professional voiceover and music production</p>
            </div>
            <div class="category-card">
                <div class="category-icon">📈</div>
                <h3>Digital Marketing</h3>
                <p>Social media and SEO marketing services</p>
            </div>
            <div class="category-card">
                <div class="category-icon">🎮</div>
                <h3>Game Development</h3>
                <p>2D and 3D game creation</p>
            </div>
            <div class="category-card">
                <div class="category-icon">🖼️</div>
                <h3>Graphic Design</h3>
                <p>Print and digital graphic design</p>
            </div>
            <div class="category-card">
                <div class="category-icon">💻</div>
                <h3>Software Development</h3>
                <p>Full-stack application development</p>
            </div>
            <div class="category-card">
                <div class="category-icon">🔧</div>
                <h3>Technical Support</h3>
                <p>Maintenance and support services</p>
            </div>
        </div>
    </section>

    <!-- Simulation Section -->
    <section class="simulation-section" id="simulationSection">
        <div class="simulation-container">
            <h2 class="section-title">Revenue Calculator</h2>
            <div class="simulation-content">
                <div class="simulation-form">
                    <h2>Calculate Your Earnings</h2>
                    <form id="simulationForm">
                        <div class="form-group">
                            <label for="productPrice">Product/Service Price</label>
                            <input type="number" id="productPrice" name="productPrice" placeholder="Enter price in USD" min="0" step="0.01" required>
                            <div class="input-suffix">Minimum: $10 | Maximum: $50,000</div>
                        </div>
                        <div class="form-group">
                            <label for="monthlySales">Monthly Sales (Number of Orders)</label>
                            <input type="number" id="monthlySales" name="monthlySales" placeholder="Enter number of orders" min="0" step="1" required>
                            <div class="input-suffix">Estimated based on market data</div>
                        </div>
                        <div class="form-group">
                            <label for="commissionFee">Commission Fee (%)</label>
                            <input type="number" id="commissionFee" name="commissionFee" placeholder="Enter commission percentage" min="0" max="100" step="0.1" value="20" required>
                            <div class="input-suffix">Standard: 15-25% | Platform fee: 5% + Payment: 2.9%</div>
                        </div>
                        <button type="submit" class="simulate-btn">Calculate Revenue</button>
                        <div class="error-message" id="errorMessage"></div>
                    </form>
                </div>

                <div class="results-display" id="resultsDisplay">
                    <h2>Your Revenue Projection</h2>
                    <div class="results-grid">
                        <div class="result-card">
                            <div class="result-label">Monthly Revenue</div>
                            <div class="result-value" id="monthlyRevenue">$0.00</div>
                        </div>
                        <div class="result-card">
                            <div class="result-label">Yearly Revenue</div>
                            <div class="result-value" id="yearlyRevenue">$0.00</div>
                        </div>
                    </div>
                    <div class="chart-container">
                        <canvas id="revenueChart"></canvas>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="footer-container">
            <div class="footer-content">
                <div class="footer-section">
                    <h3>About Us</h3>
                    <p>Digital Studio Marketplace is a leading platform connecting businesses with talented creative professionals worldwide. We empower creators and entrepreneurs to build amazing digital products.</p>
                </div>
                <div class="footer-section">
                    <h3>Quick Links</h3>
                    <ul>
                        <li><a href="#categories">Browse Categories</a></li>
                        <li><a href="#simulation">Revenue Calculator</a></li>
                        <li><a href="#pricing">Pricing Plans</a></li>
                        <li><a href="#blog">Blog & Resources</a></li>
                    </ul>
                </div>
                <div class="footer-section">
                    <h3>Contact</h3>
                    <ul>
                        <li><a href="mailto:support@digitalstudio.com">support@digitalstudio.com</a></li>
                        <li><a href="tel:+1234567890">+1 (234) 567-890</a></li>
                        <li><a href="#">Address: 123 Creative Lane, Tech City, TC 12345</a></li>
                    </ul>
                </div>
                <div class="footer-section">
                    <h3>Follow Us</h3>
                    <ul>
                        <li><a href="#">Facebook</a></li>
                        <li><a href="#">Twitter</a></li>
                        <li><a href="#">Instagram</a></li>
                        <li><a href="#">LinkedIn</a></li>
                    </ul>
                </div>
            </div>
            <div class="footer-bottom">
                <p>&copy; 2026 Digital Studio Marketplace. All rights reserved.</p>
                <p>Privacy Policy | Terms of Service | Cookie Policy</p>
            </div>
        </div>
    </footer>

    <script>
        // Form submission and calculations
        const form = document.getElementById('simulationForm');
        const resultsDisplay = document.getElementById('resultsDisplay');
        const errorMessage = document.getElementById('errorMessage');
        let chart = null;

        form.addEventListener('submit', function(e) {
            e.preventDefault();
            
            // Clear previous error message
            errorMessage.classList.remove('show');
            errorMessage.textContent = '';

            // Get form values
            const productPrice = parseFloat(document.getElementById('productPrice').value);
            const monthlySales = parseInt(document.getElementById('monthlySales').value);
            const commissionFee = parseFloat(document.getElementById('commissionFee').value);

            // Validation
            if (productPrice < 10 || productPrice > 50000) {
                showError('Product price must be between $10 and $50,000');
                return;
            }

            if (monthlySales < 0) {
                showError('Monthly sales cannot be negative');
                return;
            }

            if (commissionFee < 0 || commissionFee > 100) {
                showError('Commission fee must be between 0% and 100%');
                return;
            }

            // Calculate revenue
            const monthlyGrossRevenue = productPrice * monthlySales;
            const monthlyCommission = monthlyGrossRevenue * (commissionFee / 100);
            const monthlyNetRevenue = monthlyGrossRevenue - monthlyCommission;
            const yearlyNetRevenue = monthlyNetRevenue * 12;

            // Display results
            document.getElementById('monthlyRevenue').textContent = formatCurrency(monthlyNetRevenue);
            document.getElementById('yearlyRevenue').textContent = formatCurrency(yearlyNetRevenue);

            // Show results
            resultsDisplay.classList.add('active');

            // Draw chart
            drawRevenueChart(monthlyNetRevenue);

            // Scroll to results
            resultsDisplay.scrollIntoView({ behavior: 'smooth', block: 'nearest' });
        });

        function showError(message) {
            errorMessage.textContent = message;
            errorMessage.classList.add('show');
        }

        function formatCurrency(amount) {
            return new Intl.NumberFormat('en-US', {
                style: 'currency',
                currency: 'USD',
                minimumFractionDigits: 2,
                maximumFractionDigits: 2
            }).format(amount);
        }

        function drawRevenueChart(monthlyRevenue) {
            const canvas = document.getElementById('revenueChart');
            const ctx = canvas.getContext('2d');

            // Clear previous chart
            if (chart) {
                chart.destroy();
            }

            // Generate 12-month data
            const months = ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul', 'Aug', 'Sep', 'Oct', 'Nov', 'Dec'];
            const data = months.map(month => monthlyRevenue);

            // Create simple bar chart using canvas
            const chartHeight = canvas.height;
            const chartWidth = canvas.width;
            const barWidth = chartWidth / (months.length * 1.5);
            const barSpacing = barWidth * 0.5;
            const maxValue = Math.max(...data) * 1.2;
            const scaleY = (chartHeight * 0.8) / maxValue;

            // Clear canvas
            ctx.clearRect(0, 0, chartWidth, chartHeight);

            // Draw grid
            ctx.strokeStyle = '#e0e0e0';
            ctx.lineWidth = 1;
            for (let i = 0; i <= 5; i++) {
                const y = (chartHeight * 0.9) - (i * (chartHeight * 0.18));
                ctx.beginPath();
                ctx.moveTo(0, y);
                ctx.lineTo(chartWidth, y);
                ctx.stroke();
            }

            // Draw bars
            ctx.fillStyle = '#667eea';
            data.forEach((value, index) => {
                const x = (index * (barWidth + barSpacing)) + barSpacing;
                const height = value * scaleY;
                const y = (chartHeight * 0.9) - height;
                
                ctx.fillRect(x, y, barWidth, height);
            });

            // Draw labels
            ctx.fillStyle = '#333';
            ctx.font = '12px Arial';
            ctx.textAlign = 'center';
            months.forEach((month, index) => {
                const x = (index * (barWidth + barSpacing)) + barSpacing + (barWidth / 2);
                ctx.fillText(month, x, chartHeight - 10);
            });

            // Draw Y-axis labels
            ctx.textAlign = 'right';
            for (let i = 0; i <= 5; i++) {
                const value = (i * maxValue) / 5;
                const y = (chartHeight * 0.9) - (i * (chartHeight * 0.18));
                ctx.fillText(formatCurrency(value), 40, y + 5);
            }
        }

        // Smooth scroll to simulation section
        document.getElementById('scrollToSimulation').addEventListener('click', function() {
            document.getElementById('simulationSection').scrollIntoView({ behavior: 'smooth' });
        });

        // Sign up button functionality
        document.querySelector('.signup-btn').addEventListener('click', function() {
            alert('Sign up feature coming soon!');
        });

        // Language button functionality
        document.querySelector('.language-btn').addEventListener('click', function() {
            alert('Multi-language support coming soon!');
        });

        // Category card click functionality
        document.querySelectorAll('.category-card').forEach(card => {
            card.addEventListener('click', function() {
                const categoryName = this.querySelector('h3').textContent;
                alert(`You selected: ${categoryName}\n\nRedirecting to category page...`);
            });
        });

        // Resize canvas on window resize
        window.addEventListener('resize', function() {
            const canvas = document.getElementById('revenueChart');
            if (canvas && resultsDisplay.classList.contains('active')) {
                // Adjust canvas size
                const container = canvas.parentElement;
                canvas.width = container.clientWidth - 40;
                canvas.height = 300;
            }
        });

        // Initialize canvas size
        window.addEventListener('load', function() {
            const canvas = document.getElementById('revenueChart');
            const container = canvas.parentElement;
            canvas.width = container.clientWidth - 40;
            canvas.height = 300;
        });
    </script>
</body>
</html>
