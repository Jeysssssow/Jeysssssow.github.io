<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>St. Jammie Movement - LGBTQ+ Rights in Kenya</title>
    <style>
        :root {
            --primary: #9c27b0;
            --secondary: #7b1fa2;
            --accent: #ff9800;
            --light: #f5f5f5;
            --dark: #333;
            --text: #424242;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            line-height: 1.6;
            color: var(--text);
            background-color: var(--light);
        }
        
        header {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            padding: 2rem 0;
            text-align: center;
        }
        
        .logo {
            font-size: 2.5rem;
            font-weight: bold;
            margin-bottom: 1rem;
        }
        
        .tagline {
            font-size: 1.2rem;
            margin-bottom: 2rem;
        }
        
        nav {
            background-color: var(--secondary);
            padding: 1rem;
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        nav ul {
            display: flex;
            justify-content: center;
            list-style: none;
            flex-wrap: wrap;
        }
        
        nav li {
            margin: 0 1rem;
        }
        
        nav a {
            color: white;
            text-decoration: none;
            font-weight: bold;
            padding: 0.5rem 1rem;
            border-radius: 4px;
            transition: background-color 0.3s;
        }
        
        nav a:hover {
            background-color: rgba(255, 255, 255, 0.2);
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem;
        }
        
        section {
            margin-bottom: 3rem;
            padding: 2rem;
            background-color: white;
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }
        
        h1, h2, h3 {
            color: var(--primary);
            margin-bottom: 1rem;
        }
        
        h1 {
            font-size: 2.5rem;
            border-bottom: 3px solid var(--accent);
            padding-bottom: 0.5rem;
            display: inline-block;
        }
        
        h2 {
            font-size: 2rem;
        }
        
        h3 {
            font-size: 1.5rem;
            color: var(--secondary);
        }
        
        .btn {
            display: inline-block;
            background-color: var(--accent);
            color: white;
            padding: 0.8rem 1.5rem;
            border-radius: 4px;
            text-decoration: none;
            font-weight: bold;
            margin: 1rem 0;
            transition: transform 0.3s, box-shadow 0.3s;
            cursor: pointer;
            border: none;
        }
        
        .btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }
        
        .impact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin: 2rem 0;
        }
        
        .impact-card {
            background-color: var(--light);
            padding: 1.5rem;
            border-radius: 8px;
            border-top: 4px solid var(--primary);
        }
        
        .testimonial {
            font-style: italic;
            padding: 1.5rem;
            background-color: rgba(156, 39, 176, 0.1);
            border-left: 4px solid var(--primary);
            margin: 1.5rem 0;
        }
        
        .donation-options {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            margin: 2rem 0;
        }
        
        .donation-option {
            flex: 1;
            min-width: 200px;
            padding: 1.5rem;
            background-color: var(--light);
            border-radius: 8px;
            text-align: center;
        }
        
        .donation-amount {
            font-size: 1.5rem;
            font-weight: bold;
            color: var(--primary);
        }
        
        footer {
            background-color: var(--dark);
            color: white;
            text-align: center;
            padding: 2rem;
            margin-top: 2rem;
        }
        
        .social-links {
            margin: 1rem 0;
        }
        
        .social-links a {
            color: white;
            margin: 0 0.5rem;
            font-size: 1.5rem;
        }

        /* Modal Styles */
        .modal {
            display: none;
            position: fixed;
            z-index: 1000;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            overflow: auto;
            background-color: rgba(0,0,0,0.4);
        }

        .modal-content {
            background-color: #fefefe;
            margin: 10% auto;
            padding: 2rem;
            border-radius: 8px;
            box-shadow: 0 4px 20px rgba(0,0,0,0.2);
            width: 80%;
            max-width: 600px;
            animation: modalopen 0.4s;
        }

        @keyframes modalopen {
            from {opacity: 0; transform: translateY(-50px);}
            to {opacity: 1; transform: translateY(0);}
        }

        .close {
            color: #aaa;
            float: right;
            font-size: 28px;
            font-weight: bold;
            cursor: pointer;
        }

        .close:hover {
            color: var(--primary);
        }

        .payment-method {
            margin: 1.5rem 0;
            padding: 1rem;
            border: 1px solid #ddd;
            border-radius: 5px;
        }

        .payment-method h4 {
            margin-top: 0;
            color: var(--secondary);
        }

        .payment-details {
            margin: 0.5rem 0;
            padding: 0.5rem;
            background-color: rgba(156, 39, 176, 0.05);
            border-radius: 4px;
        }

        .copy-btn {
            background-color: var(--primary);
            color: white;
            border: none;
            padding: 0.3rem 0.6rem;
            border-radius: 3px;
            cursor: pointer;
            margin-left: 0.5rem;
            font-size: 0.8rem;
        }

        .copy-btn:hover {
            background-color: var(--secondary);
        }
        
        @media (max-width: 768px) {
            nav ul {
                flex-direction: column;
                align-items: center;
            }
            
            nav li {
                margin: 0.5rem 0;
            }
            
            .impact-grid {
                grid-template-columns: 1fr;
            }

            .modal-content {
                width: 95%;
                margin: 20% auto;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="logo">St. Jammie Movement</div>
        <div class="tagline">Empowering LGBTQ+ Lives in Kenya</div>
        <button onclick="openModal()" class="btn">Donate Now</button>
    </header>
    
    <nav>
        <ul>
            <li><a href="#home">Home</a></li>
            <li><a href="#impact">Our Impact</a></li>
            <li><a href="#donate">Donate</a></li>
            <li><a href="#support">Get Help</a></li>
            <li><a href="#volunteer">Join Us</a></li>
        </ul>
    </nav>
    
    <div class="container">
        <section id="home">
            <h1>Love Is Human. Fight With Us.</h1>
            <p>For years, Kenya's LGBTQ+ community has faced violence, discrimination, and legal persecution. The St. Jammie Movement is changing that through advocacy, safe spaces, and community empowerment.</p>
            <p>We've helped thousands embrace their true selves - but with your support, we can reach millions.</p>
            <div class="testimonial">
                "Before St. Jammie, I thought I was alone. Now, I know I have a family."<br>
                <strong>- Mwangi, 28, Nairobi</strong>
            </div>
            <button onclick="openModal()" class="btn">Support Our Work</button>
        </section>
        
        <section id="impact">
            <h2>Our Impact</h2>
            <div class="impact-grid">
                <div class="impact-card">
                    <h3>Legal Advocacy</h3>
                    <p>Challenging discriminatory laws and defending LGBTQ+ rights in court. Our 2023 Supreme Court case protected LGBTQ+ organizations' right to associate.</p>
                </div>
                <div class="impact-card">
                    <h3>Safe Housing</h3>
                    <p>Operating emergency shelters in Nairobi, Mombasa & Kisumu for those facing violence or homelessness because of their identity.</p>
                </div>
                <div class="impact-card">
                    <h3>Mental Health</h3>
                    <p>Providing free counseling, support groups, and HIV testing through our network of queer-friendly healthcare providers.</p>
                </div>
                <div class="impact-card">
                    <h3>Visibility</h3>
                    <p>Changing hearts and minds through documentaries, art exhibitions, and community education programs.</p>
                </div>
            </div>
        </section>
        
        <section id="donate">
            <h2>Your Donation Saves Lives</h2>
            <p>Every shilling helps us protect and empower LGBTQ+ Kenyans. Here's what your support can do:</p>
            
            <div class="donation-options">
                <div class="donation-option">
                    <div class="donation-amount">$10</div>
                    <p>A day of meals for someone in crisis</p>
                </div>
                <div class="donation-option">
                    <div class="donation-amount">$50</div>
                    <p>HIV testing for 5 people</p>
                </div>
                <div class="donation-option">
                    <div class="donation-amount">$200</div>
                    <p>A month of rent for a safe house</p>
                </div>
                <div class="donation-option">
                    <div class="donation-amount">$500</div>
                    <p>Legal fees for an LGBTQ+ asylum case</p>
                </div>
            </div>
            
            <button onclick="openModal()" class="btn">Donate Now</button>
        </section>
        
        <section id="support">
            <h2>Get Help</h2>
            <p>Are you LGBTQ+ and in need of support? We're here for you.</p>
            <div class="impact-grid">
                <div class="impact-card">
                    <h3>24/7 Hotline</h3>
                    <p>+254 102 806 956<br>Confidential support anytime</p>
                </div>
                <div class="impact-card">
                    <h3>Email Us</h3>
                    <p>jk3054794@gmail.com<br>Response within 24 hours</p>
                </div>
                <div class="impact-card">
                    <h3>Safe Houses</h3>
                    <p>Locations in Nairobi, Mombasa & Kisumu. Contact us for details.</p>
                </div>
            </div>
        </section>
        
        <section id="volunteer">
            <h2>Join the Movement</h2>
            <p>We need lawyers, counselors, artists, and allies to help us grow.</p>
            <div class="impact-grid">
                <div class="impact-card">
                    <h3>Volunteer</h3>
                    <p>Share your skills and time with our community.</p>
                    <a href="#" class="btn">Sign Up</a>
                </div>
                <div class="impact-card">
                    <h3>Host a Fundraiser</h3>
                    <p>Organize an event to support our work.</p>
                    <a href="#" class="btn">Learn How</a>
                </div>
                <div class="impact-card">
                    <h3>Spread the Word</h3>
                    <p>Follow and share our work on social media.</p>
                    <div class="social-links">
                        <a href="#">FB</a>
                        <a href="#">TW</a>
                        <a href="#">IG</a>
                    </div>
                </div>
            </div>
        </section>
    </div>
    
    <!-- Donation Modal -->
    <div id="donationModal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeModal()">&times;</span>
            <h2>Make a Donation</h2>
            <p>Thank you for supporting the St. Jammie Movement. Please use one of the following payment methods:</p>
            
            <div class="payment-method">
                <h4>Skrill Payment</h4>
                <div class="payment-details">
                    <strong>Email:</strong> jk3054794@gmail.com
                    <button class="copy-btn" onclick="copyToClipboard('jk3054794@gmail.com')">Copy</button>
                </div>
                <p>Send your donation to our Skrill account using the email above.</p>
            </div>
            
            <div class="payment-method">
                <h4>Wise International (M-Pesa)</h4>
                <div class="payment-details">
                    <strong>Name:</strong> James Warigithi Karanja
                </div>
                <div class="payment-details">
                    <strong>Phone:</strong> +254 715 869 346
                    <button class="copy-btn" onclick="copyToClipboard('+254715869346')">Copy</button>
                </div>
                <div class="payment-details">
                    <strong>Country:</strong> Kenya
                </div>
                <div class="payment-details">
                    <strong>Method:</strong> Mpesa Payment
                </div>
                <p>Send your donation via Wise using the details above.</p>
            </div>
            
            <p>After making your donation, please email us at jk3054794@gmail.com with your name and donation amount so we can properly acknowledge your support.</p>
            <button onclick="closeModal()" class="btn">Close</button>
        </div>
    </div>
    
    <footer>
        <div class="logo">St. Jammie Movement</div>
        <p>Building a Kenya where no one has to hide who they are.</p>
        <div class="social-links">
            <a href="#">Facebook</a> | 
            <a href="#">Twitter</a> | 
            <a href="#">Instagram</a>
        </div>
        <p>&copy; 2023 St. Jammie Movement. All rights reserved.</p>
        <p><small>Disclaimer: This is a fictional advocacy website for illustrative purposes.</small></p>
    </footer>

    <script>
        // Modal functions
        function openModal() {
            document.getElementById('donationModal').style.display = 'block';
        }

        function closeModal() {
            document.getElementById('donationModal').style.display = 'none';
        }

        // Close modal when clicking outside of it
        window.onclick = function(event) {
            const modal = document.getElementById('donationModal');
            if (event.target == modal) {
                closeModal();
            }
        }

        // Copy to clipboard function
        function copyToClipboard(text) {
            navigator.clipboard.writeText(text).then(function() {
                alert('Copied to clipboard: ' + text);
            }, function(err) {
                console.error('Could not copy text: ', err);
            });
        }
    </script>
</body>
</html>
