---
layout: page
title: About Espacio Manila
---

<style>
    #about-espacio {
        background-color: #FDFBF7;
        color: #001529;
        font-family: 'Inter', sans-serif;
        overflow-x: hidden;
    }
    .hero-about {
        background-color: #001529;
        padding: 100px 24px;
        position: relative;
        text-align: center;
    }
    .stat-grid {
        max-width: 1100px;
        margin: -40px auto 0;
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
        gap: 15px;
        padding: 0 24px;
        position: relative;
        z-index: 10;
    }
    .stat-card {
        background: white;
        padding: 30px 15px;
        text-align: center;
        box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        border-bottom: 4px solid #99793D;
    }
    .stat-main-text {
        font-size: 1.1rem;
        font-weight: 800;
        color: #001529;
        text-transform: uppercase;
    }
    .stat-label {
        font-size: 11px;
        text-transform: uppercase;
        letter-spacing: 2px;
        color: #000000 !important;
        font-weight: 900;
        display: block;
        margin-top: 8px;
    }

    /* ORIGINAL ANIMATIONS RESTORED */
    .reveal-left { opacity: 0; transform: translateX(-50px); transition: all 1.2s ease-out; }
    .reveal-right { opacity: 0; transform: translateX(50px); transition: all 1.2s ease-out; }
    .reveal-up { opacity: 0; transform: translateY(30px); transition: all 1.2s ease-out; }
    .active { opacity: 1 !important; transform: translate(0,0) !important; }

    .content-section { max-width: 1000px; margin: 100px auto; padding: 0 24px; }
    
    /* HIGH-READABILITY MAIN COPY SYSTEM */
    .content-section p {
        font-size: 19px;
        line-height: 1.8;
    }

    /* PURE TEXT SLIDER ARCHITECTURE (Replicated from Homepage) */
    .slider-viewport {
        position: relative;
        overflow: hidden;
        width: 100%;
        max-width: 1200px !important; 
        margin: 0 auto;
    }
    .slider-track {
        display: flex;
        transition: transform 0.6s cubic-bezier(0.25, 1, 0.5, 1);
        width: 100%;
    }
    .value-card-wrapper {
        flex: 0 0 100%;
        width: 100%;
        box-sizing: border-box;
        padding: 0 20px; 
    }
    .value-card {
        background: transparent !important;
        padding: 40px 0 !important;
        border: none !important;
        box-shadow: none !important;
        height: 100%;
    }

    /* FORCED SPECIFICITY TYPOGRAPHY SCHEME FOR VALUES */
    .value-title {
        font-size: 32px !important;
        font-weight: 900 !important;
        text-transform: uppercase !important;
        letter-spacing: 0.15em !important;
        margin-bottom: 1.5rem !important;
        line-height: 1.2 !important;
    }
    .value-description {
        font-size: 20px !important;
        line-height: 1.8 !important;
        color: #2D3748 !important;
        font-weight: 300 !important;
    }

    /* Responsive Desktop Scaling Rules */
    @media (min-width: 768px) {
        .value-title {
            font-size: 30px !important; 
        }
        .value-description {
            font-size: 30px !important; 
        }
    }
    
    /* Slider Controls Layout styling */
    .slider-dot {
        width: 10px;
        height: 10px;
        border-radius: 50%;
        background-color: rgba(1, 21, 41, 0.15);
        transition: all 0.3s ease;
        border: none;
        padding: 0;
        cursor: pointer;
    }
    .slider-dot.dot-active {
        background-color: #99793D;
        width: 36px;
        border-radius: 5px;
    }
</style>

<div id="about-espacio">

    <header class="hero-about">
        <div style="position: relative; z-index: 5;">
            <span style="color: #F1D592; text-transform: uppercase; letter-spacing: 5px; font-size: 12px; font-weight: 900;">Strategic Business Infrastructure</span>
            <h1 style="color: white; font-family: serif; font-size: clamp(2rem, 5vw, 4rem); margin: 20px 0; text-transform: uppercase;">
                Espacio <span style="color: #99793D;">Manila</span>
            </h1>
        </div>
    </header>

    <div class="stat-grid">
        <div class="stat-card">
            <span class="stat-main-text">CPA Professional</span>
            <span class="stat-label">Certified Experts</span>
        </div>
        <div class="stat-card">
            <span class="stat-main-text">SEC Accredited</span>
            <span class="stat-label">Government Link</span>
        </div>
        <div class="stat-card">
            <span class="stat-main-text">BIR Registered</span>
            <span class="stat-label">Tax Compliance</span>
        </div>
        <div class="stat-card">
            <span class="stat-main-text">Public Accounts</span>
            <span class="stat-label">Certified Firm</span>
        </div>
    </div>

    <section class="content-section grid grid-cols-1 md:grid-cols-2 gap-12">
        <div class="reveal-left">
            <h2 style="font-family: serif; font-size: 2rem; color: #001529; border-bottom: 3px solid #99793D; display: inline-block; margin-bottom: 20px;">Our Mission</h2>
            <p style="color: #2D3748;">
                To provide the highest level of professional accounting, legal, and business registration services. We aim to empower entrepreneurs by removing the friction of compliance, allowing them to focus on innovation and sustainable growth.
            </p>
        </div>
        <div class="reveal-right">
            <h2 style="font-family: serif; font-size: 2rem; color: #001529; border-bottom: 3px solid #99793D; display: inline-block; margin-bottom: 20px;">Our Vision</h2>
            <p style="color: #2D3748;">
                To be the premier business infrastructure provider in the Philippines, recognized for our uncompromising integrity, technical precision, and our ability to turn complex regulatory landscapes into seamless operational pathways.
            </p>
        </div>
    </section>

    <section class="content-section" style="margin-top: 0;">
        <h2 class="reveal-up text-center" style="font-family: serif; font-size: 2.5rem; margin-bottom: 50px;">Core Values</h2>
        
        <div class="reveal-up relative max-w-7xl mx-auto">
            
            <div class="slider-viewport" id="valuesSlider">
                <div class="slider-track" id="sliderTrack">
                    
                    <div class="value-card-wrapper">
                        <div class="value-card text-center">
                            <h3 class="value-title" style="color: #99793D !important;">Integrity</h3>
                            <p class="value-description max-w-4xl mx-auto">We uphold the highest ethical standards, ensuring every filing and statement reflects the absolute truth of your business standing.</p>
                        </div>
                    </div>
                    
                    <div class="value-card-wrapper">
                        <div class="value-card text-center">
                            <h3 class="value-title" style="color: #99793D !important;">Precision</h3>
                            <p class="value-description max-w-4xl mx-auto">In the world of taxation and law, details are everything. We execute every task with architectural accuracy.</p>
                        </div>
                    </div>
                    
                    <div class="value-card-wrapper">
                        <div class="value-card text-center">
                            <h3 class="value-title" style="color: #99793D !important;">Commitment</h3>
                            <p class="value-description max-w-4xl mx-auto">Your success is our success. We remain committed to your long-term legacy as your strategic business ally.</p>
                        </div>
                    </div>
                    
                </div>
            </div>

            <div class="flex items-center justify-center max-w-md mx-auto mt-12">
                <div class="flex gap-3.5" id="sliderDotsContainer"></div>
            </div>

        </div>
    </section>

    <div style="margin: 100px 0; text-align: center;" class="reveal-up">
        <a href="/contact" style="background: #001529; color: #FFFFFF; padding: 22px 50px; text-decoration: none; font-weight: 900; text-transform: uppercase; letter-spacing: 3px; display: inline-block; border: 2px solid #99793D;">
            Partner With Us
        </a>
    </div>

</div>

<script>
    // Intersection Observer architecture
    const observer = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
            if (entry.isIntersecting) {
                entry.target.classList.add('active');
            }
        });
    }, { threshold: 0.1 });

    document.querySelectorAll('.reveal-left, .reveal-right, .reveal-up').forEach((el) => {
        observer.observe(el);
    });

    // Carousel Value Text Slider Engine Parameters
    let currentSlide = 0;
    const track = document.getElementById('sliderTrack');
    const slides = document.querySelectorAll('.value-card-wrapper');
    const totalSlides = slides.length;
    const dotsContainer = document.getElementById('sliderDotsContainer');
    let autoSlideInterval;
    
    let touchStartX = 0;
    let touchEndX = 0;

    function buildDots() {
        dotsContainer.innerHTML = '';
        for (let i = 0; i < totalSlides; i++) {
            const dot = document.createElement('button');
            dot.className = `slider-dot ${i === 0 ? 'dot-active' : ''}`;
            dot.setAttribute('aria-label', `Maps to value slide ${i + 1}`);
            dot.addEventListener('click', () => {
                goToSlide(i);
                restartAutoSlide();
            });
            dotsContainer.appendChild(dot);
        }
    }

    function updateSliderPosition() {
        track.style.transform = `translateX(-${currentSlide * 100}%)`;
        
        const dots = document.querySelectorAll('.slider-dot');
        dots.forEach((dot, idx) => {
            if (idx === currentSlide) {
                dot.classList.add('dot-active');
            } else {
                dot.classList.remove('dot-active');
            }
        });
    }

    function goToSlide(index) {
        currentSlide = index;
        updateSliderPosition();
    }

    function moveSlide(direction) {
        currentSlide += direction;
        if (currentSlide >= totalSlides) {
            currentSlide = 0;
        } else if (currentSlide < 0) {
            currentSlide = totalSlides - 1;
        }
        updateSliderPosition();
    }

    function startAutoSlide() {
        autoSlideInterval = setInterval(() => {
            moveSlide(1);
        }, 5000);
    }

    function restartAutoSlide() {
        clearInterval(autoSlideInterval);
        startAutoSlide();
    }

    const sliderViewport = document.getElementById('valuesSlider');
    
    sliderViewport.addEventListener('touchstart', (e) => {
        touchStartX = e.changedTouches[0].screenX;
        clearInterval(autoSlideInterval);
    }, { passive: true });

    sliderViewport.addEventListener('touchend', (e) => {
        touchEndX = e.changedTouches[0].screenX;
        handleSwipeGesture();
        startAutoSlide();
    }, { passive: true });

    function handleSwipeGesture() {
        const threshold = 40;
        if (touchStartX - touchEndX > threshold) {
            moveSlide(1);
        } else if (touchEndX - touchStartX > threshold) {
            moveSlide(-1);
        }
    }

    buildDots();
    startAutoSlide();
</script>