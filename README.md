<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Abidkhanktk - Frontend Developer</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #0f172a 0%, #1e293b 100%);
            color: #f8fafc;
            line-height: 1.6;
            min-height: 100vh;
            padding: 20px;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        /* Header Section */
        .header {
            text-align: center;
            margin-bottom: 40px;
            padding: 40px 20px;
            background: rgba(15, 23, 42, 0.8);
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
            border: 1px solid #334155;
        }
        
        .greeting {
            font-size: 2.5rem;
            margin-bottom: 10px;
            background: linear-gradient(90deg, #60a5fa, #3b82f6);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            font-weight: 700;
        }
        
        .title {
            font-size: 1.8rem;
            color: #cbd5e1;
            margin-bottom: 20px;
            font-weight: 500;
        }
        
        .location {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            background: rgba(30, 41, 59, 0.7);
            padding: 8px 16px;
            border-radius: 50px;
            font-size: 1rem;
            color: #94a3b8;
            margin-bottom: 30px;
        }
        
        .location i {
            color: #3b82f6;
        }
        
        /* Profile Views */
        .profile-views {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
            margin-top: 20px;
            font-size: 0.9rem;
            color: #94a3b8;
        }
        
        /* Hero Image */
        .hero-image {
            width: 100%;
            max-width: 600px;
            margin: 30px auto;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.4);
        }
        
        .hero-image img {
            width: 100%;
            height: auto;
            display: block;
        }
        
        /* Fun Fact */
        .fun-fact {
            background: rgba(30, 41, 59, 0.7);
            padding: 20px;
            border-radius: 15px;
            margin: 30px 0;
            border-left: 5px solid #3b82f6;
            display: flex;
            align-items: flex-start;
            gap: 15px;
        }
        
        .fun-fact i {
            color: #fbbf24;
            font-size: 1.5rem;
            margin-top: 2px;
        }
        
        /* Skills Section */
        .section-title {
            font-size: 2rem;
            margin: 40px 0 20px;
            color: #f1f5f9;
            text-align: center;
            position: relative;
        }
        
        .section-title:after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 4px;
            background: linear-gradient(90deg, #60a5fa, #3b82f6);
            border-radius: 2px;
        }
        
        .skills-container {
            background: rgba(15, 23, 42, 0.8);
            border-radius: 20px;
            padding: 30px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
            border: 1px solid #334155;
            margin-bottom: 40px;
        }
        
        .tools-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(120px, 1fr));
            gap: 25px;
            margin-top: 20px;
        }
        
        .tool-card {
            background: rgba(30, 41, 59, 0.7);
            border-radius: 15px;
            padding: 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            text-align: center;
            transition: all 0.3s ease;
            border: 1px solid #475569;
        }
        
        .tool-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 25px rgba(59, 130, 246, 0.2);
            border-color: #3b82f6;
        }
        
        .tool-card img {
            width: 50px;
            height: 50px;
            margin-bottom: 15px;
            object-fit: contain;
        }
        
        .tool-card span {
            color: #cbd5e1;
            font-size: 0.9rem;
            font-weight: 500;
        }
        
        /* Stats Section */
        .stats-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 30px;
        }
        
        .stat-card {
            background: rgba(15, 23, 42, 0.8);
            border-radius: 15px;
            padding: 25px;
            text-align: center;
            border: 1px solid #334155;
            transition: all 0.3s ease;
        }
        
        .stat-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
        }
        
        .stat-card i {
            font-size: 2.5rem;
            margin-bottom: 15px;
            color: #60a5fa;
        }
        
        .stat-number {
            font-size: 2.2rem;
            font-weight: 700;
            color: #f1f5f9;
            margin-bottom: 5px;
        }
        
        .stat-label {
            color: #94a3b8;
            font-size: 1rem;
        }
        
        /* Footer */
        .footer {
            text-align: center;
            margin-top: 50px;
            padding-top: 30px;
            border-top: 1px solid #334155;
            color: #94a3b8;
            font-size: 0.9rem;
        }
        
        /* Responsive Design */
        @media (max-width: 768px) {
            .greeting {
                font-size: 2rem;
            }
            
            .title {
                font-size: 1.4rem;
            }
            
            .tools-grid {
                grid-template-columns: repeat(auto-fill, minmax(100px, 1fr));
                gap: 15px;
            }
            
            .tool-card {
                padding: 15px;
            }
            
            .tool-card img {
                width: 40px;
                height: 40px;
            }
        }
        
        @media (max-width: 480px) {
            .container {
                padding: 10px;
            }
            
            .header {
                padding: 30px 15px;
            }
            
            .tools-grid {
                grid-template-columns: repeat(3, 1fr);
            }
            
            .stats-container {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header Section -->
        <header class="header">
            <h1 class="greeting">Hi 👋, I'm Abidkhanktk</h1>
            <h2 class="title">A passionate frontend developer from Pakistan</h2>
            
            <div class="location">
                <i class="fas fa-map-marker-alt"></i>
                <span>Pakistan</span>
            </div>
            
            <div class="profile-views">
                <i class="far fa-eye"></i>
                <span><strong>Profile views:</strong> 1,245</span>
            </div>
        </header>
        
        <!-- Hero Image -->
        <div class="hero-image">
            <img src="https://media.giphy.com/media/qgQUggAC3Pfv687qPC/giphy.gif" alt="Coding animation">
        </div>
        
        <!-- Fun Fact -->
        <div class="fun-fact">
            <i class="fas fa-lightbulb"></i>
            <div>
                <h3>Fun Fact</h3>
                <p>I believe that humor makes coding more enjoyable! I love solving complex problems with simple, elegant solutions and always try to keep a positive attitude while debugging. 😄</p>
            </div>
        </div>
        
        <!-- Skills Section -->
        <h2 class="section-title">Languages & Tools</h2>
        
        <div class="skills-container">
            <p style="text-align: center; color: #cbd5e1; margin-bottom: 20px;">Here are the technologies I work with:</p>
            
            <div class="tools-grid">
                <!-- HTML5 -->
                <a href="https://www.w3.org/html/" target="_blank" rel="noreferrer" class="tool-card">
                    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original-wordmark.svg" alt="HTML5">
                    <span>HTML5</span>
                </a>
                
                <!-- CSS3 -->
                <a href="https://www.w3schools.com/css/" target="_blank" rel="noreferrer" class="tool-card">
                    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original-wordmark.svg" alt="CSS3">
                    <span>CSS3</span>
                </a>
                
                <!-- JavaScript -->
                <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript" target="_blank" rel="noreferrer" class="tool-card">
                    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-original.svg" alt="JavaScript">
                    <span>JavaScript</span>
                </a>
                
                <!-- React -->
                <a href="https://reactjs.org/" target="_blank" rel="noreferrer" class="tool-card">
                    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/react/react-original-wordmark.svg" alt="React">
                    <span>React</span>
                </a>
                
                <!-- Next.js -->
                <a href="https://nextjs.org/" target="_blank" rel="noreferrer" class="tool-card">
                    <img src="https://cdn.worldvectorlogo.com/logos/nextjs-2.svg" alt="Next.js">
                    <span>Next.js</span>
                </a>
                
                <!-- Node.js -->
                <a href="https://nodejs.org" target="_blank" rel="noreferrer" class="tool-card">
                    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nodejs/nodejs-original-wordmark.svg" alt="Node.js">
                    <span>Node.js</span>
                </a>
                
                <!-- MongoDB -->
                <a href="https://www.mongodb.com/" target="_blank" rel="noreferrer" class="tool-card">
                    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mongodb/mongodb-original-wordmark.svg" alt="MongoDB">
                    <span>MongoDB</span>
                </a>
                
                <!-- MySQL -->
                <a href="https://www.mysql.com/" target="_blank" rel="noreferrer" class="tool-card">
                    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mysql/mysql-original-wordmark.svg" alt="MySQL">
                    <span>MySQL</span>
                </a>
                
                <!-- PHP -->
                <a href="https://www.php.net" target="_blank" rel="noreferrer" class="tool-card">
                    <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/php/php-original.svg" alt="PHP">
                    <span>PHP</span>
                </a>
            </div>
        </div>
        
        <!-- Stats Section -->
        <h2 class="section-title">My GitHub Stats</h2>
        
        <div class="stats-container">
            <div class="stat-card">
                <i class="fas fa-code-branch"></i>
                <div class="stat-number">42</div>
                <div class="stat-label">Repositories</div>
            </div>
            
            <div class="stat-card">
                <i class="fas fa-star"></i>
                <div class="stat-number">128</div>
                <div class="stat-label">Stars Earned</div>
            </div>
            
            <div class="stat-card">
                <i class="fas fa-users"></i>
                <div class="stat-number">18</div>
                <div class="stat-label">Contributions</div>
            </div>
            
            <div class="stat-card">
                <i class="fas fa-calendar-alt"></i>
                <div class="stat-number">365</div>
                <div class="stat-label">Days Active</div>
            </div>
        </div>
        
        <!-- Footer -->
        <footer class="footer">
            <p>© 2023 Abidkhanktk. All rights reserved.</p>
            <p style="margin-top: 10px;">
                <i class="fas fa-envelope"></i> abidkhanktk@example.com | 
                <i class="fab fa-twitter"></i> @abidkhanktk | 
                <i class="fab fa-linkedin"></i> abidkhanktk
            </p>
        </footer>
    </div>

    <script>
        // Simple view counter animation
        document.addEventListener('DOMContentLoaded', function() {
            const viewCountElement = document.querySelector('.profile-views span');
            let views = 1245;
            
            // Simulate increasing views
            setInterval(() => {
                views += Math.floor(Math.random() * 3);
                viewCountElement.innerHTML = `<strong>Profile views:</strong> ${views.toLocaleString()}`;
            }, 10000);
            
            // Add hover effects to tool cards
            const toolCards = document.querySelectorAll('.tool-card');
            toolCards.forEach(card => {
                card.addEventListener('mouseenter', function() {
                    const icon = this.querySelector('img');
                    icon.style.transform = 'scale(1.1)';
                    icon.style.transition = 'transform 0.3s ease';
                });
                
                card.addEventListener('mouseleave', function() {
                    const icon = this.querySelector('img');
                    icon.style.transform = 'scale(1)';
                });
            });
        });
    </script>
</body>
</html>
