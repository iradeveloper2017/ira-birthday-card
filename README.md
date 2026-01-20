<!DOCTYPE html>
<html dir="rtl" lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ira - Birthday Dua</title>
    <style>
        /* Custom Fonts */
        @import url('https://fonts.googleapis.com/css2?family=Amiri:wght@400;700&family=Noto+Naskh+Arabic:wght@400;500;600&family=Poppins:wght@300;400;500;600&display=swap');
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(45deg, #0c3b5c 0%, #1a7a8c 100%);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
            overflow-x: hidden;
        }
        
        /* Main Card Container */
        .birthday-card {
            width: 100%;
            max-width: 500px;
            background: #ffffff;
            border-radius: 25px;
            position: relative;
            overflow: hidden;
            box-shadow: 
                0 25px 50px -12px rgba(0, 0, 0, 0.25),
                0 0 0 2px #fff,
                0 0 0 4px #0c3b5c;
        }
        
        /* Header with Islamic Pattern */
        .card-header {
            background: linear-gradient(135deg, #0c3b5c 0%, #1a7a8c 100%);
            padding: 40px 30px 30px;
            text-align: center;
            position: relative;
            border-bottom: 8px solid #d4af37;
        }
        
        .arabic-pattern {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: 
                radial-gradient(circle at 25% 25%, rgba(212, 175, 55, 0.1) 2px, transparent 2px),
                radial-gradient(circle at 75% 75%, rgba(212, 175, 55, 0.1) 2px, transparent 2px);
            background-size: 30px 30px;
            opacity: 0.3;
        }
        
        /* Name Circle */
        .name-circle {
            width: 120px;
            height: 120px;
            background: linear-gradient(135deg, #d4af37 0%, #ffd700 100%);
            border-radius: 50%;
            margin: 0 auto 25px;
            display: flex;
            align-items: center;
            justify-content: center;
            border: 5px solid white;
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
            position: relative;
            z-index: 2;
        }
        
        .name-text {
            font-family: 'Amiri', serif;
            font-size: 2.8em;
            font-weight: bold;
            color: #0c3b5c;
            text-shadow: 2px 2px 4px rgba(255, 255, 255, 0.5);
        }
        
        /* Title Styling */
        .birthday-title {
            font-family: 'Noto Naskh Arabic', serif;
            font-size: 3em;
            color: white;
            margin-bottom: 10px;
            text-shadow: 3px 3px 6px rgba(0, 0, 0, 0.3);
            letter-spacing: 2px;
        }
        
        .subtitle {
            color: #d4af37;
            font-size: 1.2em;
            font-weight: 500;
            margin-top: 5px;
        }
        
        /* Main Content */
        .card-content {
            padding: 35px 30px;
            background: #f9f7f2;
            min-height: 400px;
            position: relative;
        }
        
        /* Date Badge */
        .date-badge {
            background: linear-gradient(45deg, #d4af37, #ffd700);
            color: #0c3b5c;
            padding: 12px 35px;
            border-radius: 0 25px 25px 0;
            display: inline-block;
            font-weight: bold;
            font-size: 1.3em;
            margin: -55px 0 35px -30px;
            box-shadow: 5px 5px 15px rgba(0, 0, 0, 0.1);
            position: relative;
            z-index: 3;
        }
        
        /* Dua Box */
        .dua-box {
            background: white;
            border-radius: 20px;
            padding: 25px;
            margin-bottom: 30px;
            border-right: 8px solid #0c3b5c;
            box-shadow: 0 8px 20px rgba(12, 59, 92, 0.1);
            position: relative;
            overflow: hidden;
        }
        
        .dua-box:before {
            content: '';
            position: absolute;
            top: 0;
            right: 0;
            width: 60px;
            height: 60px;
            background: linear-gradient(135deg, transparent 50%, rgba(212, 175, 55, 0.1) 50%);
        }
        
        .dua-arabic {
            font-family: 'Noto Naskh Arabic', serif;
            font-size: 1.8em;
            color: #0c3b5c;
            line-height: 1.8;
            margin-bottom: 15px;
            text-align: center;
        }
        
        .dua-meaning {
            color: #2c3e50;
            font-size: 1.1em;
            line-height: 1.6;
            border-top: 2px dashed #e0e0e0;
            padding-top: 15px;
            margin-top: 15px;
        }
        
        /* Blessings Grid */
        .blessings-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 15px;
            margin: 25px 0;
        }
        
        .blessing-card {
            background: white;
            padding: 20px 15px;
            border-radius: 15px;
            text-align: center;
            transition: all 0.3s ease;
            cursor: pointer;
            border: 2px solid transparent;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }
        
        .blessing-card:hover {
            transform: translateY(-5px);
            border-color: #d4af37;
            box-shadow: 0 10px 25px rgba(212, 175, 55, 0.2);
        }
        
        .blessing-icon {
            font-size: 2em;
            margin-bottom: 10px;
            color: #0c3b5c;
        }
        
        .blessing-text {
            color: #2c3e50;
            font-size: 0.95em;
            font-weight: 500;
        }
        
        /* Interactive Button */
        .dua-button {
            background: linear-gradient(45deg, #0c3b5c, #1a7a8c);
            color: white;
            border: none;
            padding: 16px 40px;
            border-radius: 50px;
            font-size: 1.1em;
            font-weight: 600;
            cursor: pointer;
            display: block;
            margin: 30px auto;
            transition: all 0.3s ease;
            box-shadow: 0 10px 20px rgba(12, 59, 92, 0.3);
            position: relative;
            overflow: hidden;
        }
        
        .dua-button:before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
            transition: 0.5s;
        }
        
        .dua-button:hover:before {
            left: 100%;
        }
        
        .dua-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 15px 30px rgba(12, 59, 92, 0.4);
        }
        
        /* Special Message */
        .special-message {
            background: linear-gradient(135deg, #fff8e1, #fff);
            border-radius: 15px;
            padding: 25px;
            margin-top: 25px;
            border-left: 5px solid #d4af37;
            display: none;
            animation: fadeInUp 0.5s ease;
        }
        
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
        
        .message-title {
            color: #0c3b5c;
            font-size: 1.4em;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        /* Footer */
        .card-footer {
            background: #0c3b5c;
            padding: 25px 30px;
            text-align: center;
            border-top: 5px solid #d4af37;
        }
        
        .signature {
            font-family: 'Amiri', serif;
            font-size: 1.4em;
            color: #d4af37;
            margin-bottom: 10px;
            letter-spacing: 2px;
        }
        
        .handmade-note {
            color: rgba(255, 255, 255, 0.8);
            font-size: 0.9em;
            font-style: italic;
            margin-top: 10px;
        }
        
        /* Decorative Elements */
        .corner-decoration {
            position: absolute;
            width: 60px;
            height: 60px;
            opacity: 0.1;
        }
        
        .corner-1 {
            top: 20px;
            left: 20px;
            border-top: 3px solid #0c3b5c;
            border-left: 3px solid #0c3b5c;
        }
        
        .corner-2 {
            bottom: 20px;
            right: 20px;
            border-bottom: 3px solid #0c3b5c;
            border-right: 3px solid #0c3b5c;
        }
        
        /* Floating Hearts Animation */
        .floating-hearts {
            position: absolute;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
            pointer-events: none;
            z-index: 1;
        }
        
        .floating-heart {
            position: absolute;
            color: #ff6b8b;
            opacity: 0;
            animation: float 8s linear infinite;
        }
        
        @keyframes float {
            0% {
                transform: translateY(100vh) rotate(0deg);
                opacity: 0;
            }
            10% {
                opacity: 1;
            }
            90% {
                opacity: 1;
            }
            100% {
                transform: translateY(-100px) rotate(360deg);
                opacity: 0;
            }
        }
        
        /* Mobile Responsive */
        @media (max-width: 600px) {
            .birthday-card {
                max-width: 95%;
                border-radius: 20px;
            }
            
            .card-header {
                padding: 30px 20px 25px;
            }
            
            .name-circle {
                width: 100px;
                height: 100px;
            }
            
            .name-text {
                font-size: 2.2em;
            }
            
            .birthday-title {
                font-size: 2.3em;
            }
            
            .card-content {
                padding: 25px 20px;
            }
            
            .blessings-grid {
                grid-template-columns: 1fr;
            }
            
            .dua-arabic {
                font-size: 1.5em;
            }
        }
        
        /* Touch Feedback */
        .touch-feedback {
            position: absolute;
            border-radius: 50%;
            background: rgba(212, 175, 55, 0.3);
            transform: scale(0);
            animation: ripple 0.6s linear;
            pointer-events: none;
        }
        
        @keyframes ripple {
            to {
                transform: scale(4);
                opacity: 0;
            }
        }
    </style>
</head>
<body>
    <div class="birthday-card">
        <div class="floating-hearts" id="heartsContainer"></div>
        
        <!-- Header Section -->
        <div class="card-header">
            <div class="arabic-pattern"></div>
            <div class="name-circle">
                <div class="name-text" id="nameText">Ira</div>
            </div>
            <h1 class="birthday-title">عيد ميلاد سعيد</h1>
            <div class="subtitle">May Allah's Blessings Be Upon You</div>
        </div>
        
        <!-- Content Section -->
        <div class="card-content">
            <div class="corner-decoration corner-1"></div>
            <div class="corner-decoration corner-2"></div>
            
            <div class="date-badge">🌙 19th Date - Special Blessings</div>
            
            <div class="dua-box">
                <div class="dua-arabic">
                    جَعَلَكَ اللَّهُ مِنَ الْمُفْلِحِينَ وَرَزَقَكَ الْعِلْمَ النَّافِعَ
                </div>
                <div class="dua-meaning">
                    আল্লাহ তায়ালা আপনাকে সফলদের অন্তর্ভুক্ত করুন এবং উপকারী জ্ঞান দান করুন। আপনার প্রতিটি দিন যেন হয় বরকতময়, প্রতিটি পদক্ষেপ হোক সফলতার দিকে।
                </div>
            </div>
            
            <div class="blessings-grid">
                <div class="blessing-card" data-blessing="1">
                    <div class="blessing-icon">🕌</div>
                    <div class="blessing-text">Strong Iman & Taqwa</div>
                </div>
                <div class="blessing-card" data-blessing="2">
                    <div class="blessing-icon">❤️</div>
                    <div class="blessing-text">Health & Happiness</div>
                </div>
                <div class="blessing-card" data-blessing="3">
                    <div class="blessing-icon">📚</div>
                    <div class="blessing-text">Useful Knowledge</div>
                </div>
                <div class="blessing-card" data-blessing="4">
                    <div class="blessing-icon">🤲</div>
                    <div class="blessing-text">Halal Rizq</div>
                </div>
            </div>
            
            <button class="dua-button" id="showMessageBtn">
                ✨ Click for Special Dua ✨
            </button>
            
            <div class="special-message" id="specialMessage">
                <div class="message-title">
                    <span>🌟</span> Personal Dua for Ira
                </div>
                <p style="line-height: 1.7; color: #2c3e50; margin-bottom: 15px;">
                    "হে আল্লাহ, Ira-এর জীবনকে রহমত ও বরকত দ্বারা পূর্ণ করুন। 
                    তাকে উত্তম স্বাস্থ্য, প্রশান্তিপূর্ণ মন, এবং সফলতা দান করুন। 
                    তার পরিবার ও প্রিয়জনদের সাথে সুখ-শান্তিতে জীবন কাটুক।"
                </p>
                <div style="text-align: left; padding: 15px; background: rgba(212, 175, 55, 0.1); border-radius: 10px;">
                    <div style="font-family: 'Noto Naskh Arabic', serif; font-size: 1.2em; color: #0c3b5c; margin-bottom: 5px;">
                        بِسْمِ اللَّهِ الرَّحْمَنِ الرَّحِيمِ
                    </div>
                    <div style="color: #666; font-size: 0.9em;">
                        Every step blessed with His mercy
                    </div>
                </div>
            </div>
        </div>
        
        <!-- Footer Section -->
        <div class="card-footer">
            <div class="signature">With Duas & Prayers</div>
            <div style="color: white; font-size: 1.1em; margin-bottom: 8px;">Wish by Hasan</div>
            <div class="handmade-note">
                Handcrafted with care • Coded with intention
            </div>
            <div style="color: rgba(255, 255, 255, 0.6); font-size: 0.8em; margin-top: 15px;">
                This digital gift is made especially for Ira
            </div>
        </div>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const nameText = document.getElementById('nameText');
            const showMessageBtn = document.getElementById('showMessageBtn');
            const specialMessage = document.getElementById('specialMessage');
            const heartsContainer = document.getElementById('heartsContainer');
            const blessingCards = document.querySelectorAll('.blessing-card');
            
            // Personalize with name
            const userName = 'Ira';
            nameText.textContent = userName;
            
            // Create floating hearts
            function createHearts() {
                const heartEmojis = ['💝', '💖', '✨', '🌟', '🕌', '🤲'];
                
                for (let i = 0; i < 15; i++) {
                    const heart = document.createElement('div');
                    heart.className = 'floating-heart';
                    heart.textContent = heartEmojis[Math.floor(Math.random() * heartEmojis.length)];
                    heart.style.left = Math.random() * 100 + '%';
                    heart.style.fontSize = (Math.random() * 20 + 15) + 'px';
                    heart.style.animationDelay = (Math.random() * 5) + 's';
                    heart.style.animationDuration = (Math.random() * 4 + 6) + 's';
                    
                    heartsContainer.appendChild(heart);
                    
                    // Cleanup
                    setTimeout(() => {
                        heart.remove();
                    }, 10000);
                }
            }
            
            // Start heart animation
            createHearts();
            setInterval(createHearts, 2000);
            
            // Show special message
            showMessageBtn.addEventListener('click', function(e) {
                // Ripple effect
                createRipple(e);
                
                // Toggle message
                if (specialMessage.style.display === 'block') {
                    specialMessage.style.display = 'none';
                    showMessageBtn.innerHTML = '✨ Click for Special Dua ✨';
                } else {
                    specialMessage.style.display = 'block';
                    showMessageBtn.innerHTML = '👇 Hide Dua';
                    
                    // Update message with name
                    const messageParagraph = specialMessage.querySelector('p');
                    if (messageParagraph) {
                        messageParagraph.innerHTML = messageParagraph.innerHTML
                            .replace(/Ira/g, `<strong>${userName}</strong>`);
                    }
                }
                
                // Haptic feedback for mobile
                if (navigator.vibrate) {
                    navigator.vibrate(30);
                }
            });
            
            // Blessing cards interaction
            blessingCards.forEach(card => {
                card.addEventListener('click', function(e) {
                    createRipple(e);
                    
                    // Add visual feedback
                    this.style.transform = 'scale(0.95)';
                    this.style.boxShadow = '0 3px 10px rgba(212, 175, 55, 0.4)';
                    
                    // Show blessing message
                    const blessings = {
                        1: "May your faith grow stronger every day",
                        2: "Health and happiness always be with you",
                        3: "Wisdom and knowledge guide your path",
                        4: "Halal provisions come to you easily"
                    };
                    
                    const blessingNum = this.getAttribute('data-blessing');
                    const originalText = this.querySelector('.blessing-text').textContent;
                    
                    this.querySelector('.blessing-text').textContent = blessings[blessingNum];
                    this.style.background = 'linear-gradient(135deg, #fff8e1, #fff)';
                    
                    // Reset after 2 seconds
                    setTimeout(() => {
                        this.style.transform = '';
                        this.style.boxShadow = '';
                        this.style.background = '';
                        this.querySelector('.blessing-text').textContent = originalText;
                    }, 2000);
                });
            });
            
            // Ripple effect function
            function createRipple(event) {
                const btn = event.currentTarget;
                const circle = document.createElement("span");
                const diameter = Math.max(btn.clientWidth, btn.clientHeight);
                const radius = diameter / 2;
                
                circle.style.width = circle.style.height = `${diameter}px`;
                circle.style.left = `${event.clientX - btn.getBoundingClientRect().left - radius}px`;
                circle.style.top = `${event.clientY - btn.getBoundingClientRect().top - radius}px`;
                circle.className = "touch-feedback";
                
                const ripple = btn.querySelector(".touch-feedback");
                if (ripple) {
                    ripple.remove();
                }
                
                btn.appendChild(circle);
                
                setTimeout(() => {
                    circle.remove();
                }, 600);
            }
            
            // Check if today is 19th
            const today = new Date();
            const dateBadge = document.querySelector('.date-badge');
            
            if (today.getDate() === 19) {
                dateBadge.innerHTML = '🎉 Today is 19th! Special Birthday Blessings! 🎉';
                dateBadge.style.background = 'linear-gradient(45deg, #ff6b6b, #ffd700)';
                dateBadge.style.animation = 'pulse 2s infinite';
                
                // Add pulse animation
                const style = document.createElement('style');
                style.textContent = `
                    @keyframes pulse {
                        0% { transform: translateX(-30px) scale(1); }
                        50% { transform: translateX(-30px) scale(1.05); }
                        100% { transform: translateX(-30px) scale(1); }
                    }
                `;
                document.head.appendChild(style);
            }
            
            // Add touch events for mobile
            showMessageBtn.addEventListener('touchstart', function() {
                this.style.transform = 'scale(0.97)';
            });
            
            showMessageBtn.addEventListener('touchend', function() {
                this.style.transform = '';
            });
            
            // Auto-show message on page load after 3 seconds
            setTimeout(() => {
                if (specialMessage.style.display !== 'block') {
                    showMessageBtn.click();
                    setTimeout(() => {
                        showMessageBtn.click();
                    }, 5000);
                }
            }, 3000);
        });
    </script>
</body>
</html>
