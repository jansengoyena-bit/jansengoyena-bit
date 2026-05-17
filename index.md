---
layout: page
title: Home | Espacio Manila
---

<style>
    /* 1. Animation Core */
    .reveal-up { opacity: 0; transform: translateY(30px); transition: all 1.2s cubic-bezier(0.22, 1, 0.36, 1); }
    .reveal-left { opacity: 0; transform: translateX(-40px); transition: all 1.2s cubic-bezier(0.22, 1, 0.36, 1); }
    .reveal-right { opacity: 0; transform: translateX(40px); transition: all 1.2s cubic-bezier(0.22, 1, 0.36, 1); }
    .active { opacity: 1 !important; transform: translate(0,0) !important; }

    /* 2. Layout Structure */
    #espacio-landing {
        background-color: #FDFBF7;
        color: #011F3F;
        overflow-x: hidden;
    }
    
    .gold-accent { color: #C5A059 !important; }
    .bg-navy { background-color: #011F3F; }
    
    /* 3. Pure Text Slider Styles (Borders, Cards, and Highlights Removed) */
    .slider-viewport, .review-viewport {
        position: relative;
        overflow: hidden;
        width: 100%;
        max-width: 1200px !important; 
        margin: 0 auto;
    }
    .slider-track, .review-track {
        display: flex;
        transition: transform 0.6s cubic-bezier(0.25, 1, 0.5, 1);
        width: 100%;
    }
    .service-card-wrapper, .review-card-wrapper {
        flex: 0 0 100%;
        width: 100%;
        box-sizing: border-box;
        padding: 0 20px; 
    }
    .service-card, .review-card {
        background: transparent !important; 
        padding: 40px 0 !important; 
        border: none !important; 
        box-shadow: none !important; 
        height: 100%;
    }

    /* Forced High-Specificity Typography Rules */
    .slider-title {
        font-size: 32px !important;
        font-weight: 900 !important;
        text-transform: uppercase !important;
        letter-spacing: 0.15em !important;
        margin-bottom: 1.5rem !important;
        line-height: 1.2 !important;
    }
    .slider-description {
        font-size: 20px !important;
        line-height: 1.8 !important;
        color: #2D3748 !important;
        font-weight: 300 !important;
    }

    /* Media queries to guarantee responsive display scales */
    @media (min-width: 768px) {
        .slider-title {
            font-size: 30px !important; 
        }
        .slider-description {
            font-size: 30px !important; 
        }
    }
    
    /* Navigation Indicators */
    .slider-dot, .review-dot {
        width: 10px;
        height: 10px;
        border-radius: 50%;
        background-color: rgba(1, 31, 63, 0.13);
        transition: all 0.3s ease;
        border: none;
        padding: 0;
        cursor: pointer;
    }
    .slider-dot.dot-active, .review-dot.dot-active {
        background-color: #C5A059;
        width: 36px;
        border-radius: 5px;
    }

    /* 4. Footer Visibility Insurance */
    footer {
        position: relative;
        z-index: 50;
        background-color: #011F3F !important;
        display: block !important;
    }
    footer * { color: #FDFBF7 !important; }
</style>

<div id="espacio-landing">

    <section class="relative pt-12 pb-20 lg:min-h-[85vh] flex items-center">
        <div class="absolute top-0 left-0 w-full h-full pointer-events-none -z-10 overflow-hidden">
            <span class="absolute top-10 left-10 text-[12vw] font-serif font-black opacity-[0.03] uppercase">Espacio</span>
        </div>

        <div class="max-w-7xl mx-auto px-8 grid grid-cols-1 lg:grid-cols-12 gap-16 items-center">
            <div class="lg:col-span-7 reveal-left">
                <span class="text-[11px] uppercase tracking-[0.4em] font-black gold-accent mb-6 block">Your Complete Virtual Office Solution</span>
                <h1 class="text-4xl md:text-6xl font-serif leading-tight mb-8">
                    Welcome to <br>Espacio <span class="italic gold-accent">Manila</span>
                </h1>
                <h2 class="text-xl font-bold mb-6">Empowering Entrepreneurs to Thrive</h2>
                <p class="text-[17px] text-[#2D3748] leading-relaxed mb-10 max-w-xl">
                    Are you an entrepreneur looking for a professional and seamless way to establish and grow your business? 
                    Look no further than <b>Espacio Manila</b>, your all-in-one virtual office solution. 
                    We provide everything you need to manage your business effectively, from virtual addresses to regulatory compliance.
                </p>
                <div class="flex flex-wrap gap-4">
                    <a href="/services" class="bg-[#011F3F] text-white px-10 py-4 text-[10px] font-black uppercase tracking-[0.3em] hover:bg-[#C5A059] transition-all">Get a Quote</a>
                    <a href="/contact" class="border-2 border-[#011F3F] text-[#011F3F] px-10 py-4 text-[10px] font-black uppercase tracking-[0.3em] hover:bg-[#011F3F] hover:text-white transition-all">Inquire Now</a>
                </div>
            </div>

            <div class="lg:col-span-5 reveal-right">
                <div class="relative">
                    <div class="aspect-[4/5] bg-navy rounded-sm overflow-hidden shadow-2xl">
                        <img src="https://images.unsplash.com/photo-1497366216548-37526070297c?auto=format&fit=crop&q=80&w=1200" alt="Professional Office" class="w-full h-full object-cover">
                    </div>
                    <div class="absolute -bottom-6 -right-6 w-32 h-32 border-b-4 border-r-4 border-[#C5A059]/30 -z-10"></div>
                </div>
            </div>
        </div>
    </section>

    <section class="py-28 bg-white">
        <div class="max-w-7xl mx-auto px-8">
            <div class="reveal-up mb-16 text-center">
                <h2 class="text-4xl md:text-6xl font-serif mb-5">Our Core Services</h2>
                <div class="w-28 h-1.5 bg-navy mx-auto"></div>
            </div>

            <div class="reveal-up relative max-w-7xl mx-auto">
                
                <div class="slider-viewport" id="servicesSlider">
                    <div class="slider-track" id="sliderTrack">
                        
                        <div class="service-card-wrapper">
                            <div class="service-card text-center">
                                <h3 class="slider-title gold-accent">Virtual Office Address</h3>
                                <p class="slider-description max-w-4xl mx-auto">Gain a prestigious business address in a prime location without the overhead costs of physical office space.</p>
                            </div>
                        </div>
                        
                        <div class="service-card-wrapper">
                            <div class="service-card text-center">
                                <h3 class="slider-title gold-accent">Business Registration</h3>
                                <p class="slider-description max-w-4xl mx-auto">Seamlessly navigate the complexities of business registration, ensuring compliance and peace of mind.</p>
                            </div>
                        </div>
                        
                        <div class="service-card-wrapper">
                            <div class="service-card text-center">
                                <h3 class="slider-title gold-accent">Tax Compliance</h3>
                                <p class="slider-description max-w-4xl mx-auto">Our expert team takes care of your tax compliance requirements, from registration to filing and reporting.</p>
                            </div>
                        </div>
                        
                        <div class="service-card-wrapper">
                            <div class="service-card text-center">
                                <h3 class="slider-title gold-accent">Meeting Room Access</h3>
                                <p class="slider-description max-w-4xl mx-auto">Host important meetings and presentations in our modern and equipped meeting rooms.</p>
                            </div>
                        </div>
                        
                        <div class="service-card-wrapper">
                            <div class="service-card text-center">
                                <h3 class="slider-title gold-accent">Additional Solutions</h3>
                                <p class="slider-description max-w-4xl mx-auto">Benefit from other essential services, including payroll, bookkeeping, and other administrative support to streamline your operations.</p>
                            </div>
                        </div>

                    </div>
                </div>

                <div class="flex items-center justify-center max-w-md mx-auto mt-12">
                    <div class="flex gap-3.5" id="sliderDotsContainer"></div>
                </div>

            </div>
        </div>
    </section>

    <section class="py-24 bg-gradient-to-b from-[#011F3F] to-[#001529] text-[#FDFBF7]">
  
        <div class="max-w-7xl mx-auto px-8">
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-20 items-start">
                <div class="reveal-left">
                    <h2 class="text-3xl md:text-5xl font-serif mb-12">Why Choose <br><span class="gold-accent">Espacio Manila?</span></h2>
                    <ul class="space-y-8">
                        <li class="flex gap-6">
                            <span class="gold-accent font-black">01</span>
                            <div>
                                <h4 class="font-bold uppercase tracking-widest text-sm mb-1">Convenience</h4>
                                <p class="text-[#FDFBF7]/60 text-sm">Get all your business needs met under one roof.</p>
                            </div>
                        </li>
                        <li class="flex gap-6">
                            <span class="gold-accent font-black">02</span>
                            <div>
                                <h4 class="font-bold uppercase tracking-widest text-sm mb-1">Affordability</h4>
                                <p class="text-[#FDFBF7]/60 text-sm">Save money on expensive office space and operational costs.</p>
                            </div>
                        </li>
                        <li class="flex gap-6">
                            <span class="gold-accent font-black">03</span>
                            <div>
                                <h4 class="font-bold uppercase tracking-widest text-sm mb-1">Professionalism</h4>
                                <p class="text-[#FDFBF7]/60 text-sm">Enhance your brand image with a prestigious address.</p>
                            </div>
                        </li>
                        <li class="flex gap-6">
                            <span class="gold-accent font-black">04</span>
                            <div>
                                <h4 class="font-bold uppercase tracking-widest text-sm mb-1">Expertise</h4>
                                <p class="text-[#FDFBF7]/60 text-sm">Our team will guide you through all aspects of management.</p>
                            </div>
                        </li>
                        <li class="flex gap-6">
                            <span class="gold-accent font-black">05</span>
                            <div>
                                <h4 class="font-bold uppercase tracking-widest text-sm mb-1">Scalability</h4>
                                <p class="text-[#FDFBF7]/60 text-sm">Adapt our services to meet your evolving business needs.</p>
                            </div>
                        </li>
                    </ul>
                </div>

                <div class="reveal-right bg-white/5 p-12 border border-white/10 rounded-sm">
                    <h3 class="text-2xl font-serif mb-6 italic gold-accent">Ready to Level Up Your Business?</h3>
                    <p class="text-sm mb-10 leading-relaxed text-[#FDFBF7]/80">
                        Let us help you determine the best solution for your unique business needs. Start your entrepreneurial journey with Espacio Manila today.
                    </p>
                    <div id="quote" class="space-y-6">
                        <h4 class="font-bold uppercase tracking-widest text-[11px] mb-2">Get a Custom Quote</h4>
                        <a href="/services" class="block w-full text-center bg-[#C5A059] text-navy py-5 font-black uppercase tracking-[0.3em] text-[10px] hover:bg-white transition-all">Get a Quote</a>
                        
                        <div id="inquiry" class="pt-8 border-t border-white/10">
                            <h4 class="font-bold uppercase tracking-widest text-[11px] mb-4">Have a Question?</h4>
                            <a href="/contact" class="block w-full text-center border border-white text-white py-5 font-black uppercase tracking-[0.3em] text-[10px] hover:bg-white hover:text-navy transition-all">Inquire Now</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section class="py-24 bg-[#F9F6F0] border-t border-b border-navy/5">
        <div class="max-w-4xl mx-auto px-8 text-center">
            <div class="reveal-up mb-12">
                <h2 class="text-4xl md:text-5xl font-serif text-[#011F3F] tracking-tight">What Our Clients Say About Us</h2>
            </div>

            <div class="reveal-up review-viewport" id="reviewsSlider">
                <div class="review-track" id="reviewTrack">
                    
                    <div class="review-card-wrapper">
                        <div class="review-card flex flex-col items-center">
                            <div class="w-20 h-20 rounded-full overflow-hidden mb-8 border-2 border-[#C5A059] shadow-md">
                                <img src="https://images.unsplash.com/photo-1534528741775-53994a69daeb?auto=format&fit=crop&q=80&w=200" alt="Client Avatar" class="w-full h-full object-cover">
                            </div>
                            <blockquote class="font-serif text-lg md:text-xl text-[#011F3F] leading-relaxed italic max-w-2xl mb-6">
                                "Espacio Manila helped me out of a very sticky business registration bottleneck created by the neglect of a former consulting group. I have nothing but the highest praise for this team and the people working there. My ongoing experience is just as positive."
                            </blockquote>
                            <cite class="text-xs uppercase tracking-[0.25em] font-black gold-accent not-italic">— Maria Santos, TechFoundry Inc.</cite>
                        </div>
                    </div>

                    <div class="review-card-wrapper">
                        <div class="review-card flex flex-col items-center">
                            <div class="w-20 h-20 rounded-full overflow-hidden mb-8 border-2 border-[#C5A059] shadow-md">
                                <img src="https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?auto=format&fit=crop&q=80&w=200" alt="Client Avatar" class="w-full h-full object-cover">
                            </div>
                            <blockquote class="font-serif text-lg md:text-xl text-[#011F3F] leading-relaxed italic max-w-2xl mb-6">
                                "Having a prestigious business address in a prime location without overhead costs transformed our brand presence overnight. Their handling of our tax compliance requirements is flawless, efficient, and gives us true peace of mind."
                            </blockquote>
                            <cite class="text-xs uppercase tracking-[0.25em] font-black gold-accent not-italic">— Shane Miller, Global Trade Solutions</cite>
                        </div>
                    </div>

                    <div class="review-card-wrapper">
                        <div class="review-card flex flex-col items-center">
                            <div class="w-20 h-20 rounded-full overflow-hidden mb-8 border-2 border-[#C5A059] shadow-md">
                                <img src="https://images.unsplash.com/photo-1494790108377-be9c29b29330?auto=format&fit=crop&q=80&w=200" alt="Client Avatar" class="w-full h-full object-cover">
                            </div>
                            <blockquote class="font-serif text-lg md:text-xl text-[#011F3F] leading-relaxed italic max-w-2xl mb-6">
                                "Their end-to-end support framework across payroll management, corporate filings, and modern physical meeting rooms allowed us to launch operations safely and cleanly in record time. Phenomenal value architectural setup."
                            </blockquote>
                            <cite class="text-xs uppercase tracking-[0.25em] font-black gold-accent not-italic">— Anna Lim, Creative Hive Studios</cite>
                        </div>
                    </div>

                    <div class="review-card-wrapper">
                        <div class="review-card flex flex-col items-center">
                            <div class="w-20 h-20 rounded-full overflow-hidden mb-8 border-2 border-[#C5A059] shadow-md">
                                <img src="https://images.unsplash.com/photo-1500648767791-00dcc994a43e?auto=format&fit=crop&q=80&w=200" alt="Client Avatar" class="w-full h-full object-cover">
                            </div>
                            <blockquote class="font-serif text-lg md:text-xl text-[#011F3F] leading-relaxed italic max-w-2xl mb-6">
                                "As a foreign business owner breaking into the regional marketplace, handling statutory declarations can feel like a minefield. Espacio Manila handled everything transparently, removing a tremendous amount of structural weight off our backs."
                            </blockquote>
                            <cite class="text-xs uppercase tracking-[0.25em] font-black gold-accent not-italic">— David Vance, NexaCore Logistics</cite>
                        </div>
                    </div>

                    <div class="review-card-wrapper">
                        <div class="review-card flex flex-col items-center">
                            <div class="w-20 h-20 rounded-full overflow-hidden mb-8 border-2 border-[#C5A059] shadow-md">
                                <img src="https://images.unsplash.com/photo-1580489944761-15a19d654956?auto=format&fit=crop&q=80&w=200" alt="Client Avatar" class="w-full h-full object-cover">
                            </div>
                            <blockquote class="font-serif text-lg md:text-xl text-[#011F3F] leading-relaxed italic max-w-2xl mb-6">
                                "The sheer flexibility of accessing high-end, professionally styled meeting boardrooms exactly when we need to sign physical asset deeds or host stakeholders is incomparable. Best strategic choice we made this fiscal year."
                            </blockquote>
                            <cite class="text-xs uppercase tracking-[0.25em] font-black gold-accent not-italic">— Elena Rostova, Vertex Capital Partners</cite>
                        </div>
                    </div>

                    <div class="review-card-wrapper">
                        <div class="review-card flex flex-col items-center">
                            <div class="w-20 h-20 rounded-full overflow-hidden mb-8 border-2 border-[#C5A059] shadow-md">
                                <img src="https://images.unsplash.com/photo-1472099645785-5658abf4ff4e?auto=format&fit=crop&q=80&w=200" alt="Client Avatar" class="w-full h-full object-cover">
                            </div>
                            <blockquote class="font-serif text-lg md:text-xl text-[#011F3F] leading-relaxed italic max-w-2xl mb-6">
                                "Their administrative ecosystem is smooth and tightly integrated. Mail handling alerts arrive cleanly without lagging, and bookkeeping logs are structured with accurate microservice precision. Highly recommended for remote-first squads."
                            </blockquote>
                            <cite class="text-xs uppercase tracking-[0.25em] font-black gold-accent not-italic">— Jonathan Mercer, CloudSync Software</cite>
                        </div>
                    </div>

                    <div class="review-card-wrapper">
                        <div class="review-card flex flex-col items-center">
                            <div class="w-20 h-20 rounded-full overflow-hidden mb-8 border-2 border-[#C5A059] shadow-md">
                                <img src="https://images.unsplash.com/photo-1544005313-94ddf0286df2?auto=format&fit=crop&q=80&w=200" alt="Client Avatar" class="w-full h-full object-cover">
                            </div>
                            <blockquote class="font-serif text-lg md:text-xl text-[#011F3F] leading-relaxed italic max-w-2xl mb-6">
                                "Navigating bureaucratic filings for agricultural and manufacturing startups is complex. Their expert consultation framework streamlined our local compliance paths elegantly, leaving us entirely free to optimize production scales."
                            </blockquote>
                            <cite class="text-xs uppercase tracking-[0.25em] font-black gold-accent not-italic">— Clara Valenzuela, TerraGrow Agribusiness</cite>
                        </div>
                    </div>

                </div>
            </div>

            <div class="flex justify-center flex-wrap max-w-lg mx-auto gap-3 mt-8" id="reviewDotsContainer"></div>
        </div>
    </section>

</div>

<script>
    // Intersection Observer architecture
    const observer = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
            if (entry.isIntersecting) entry.target.classList.add('active');
        });
    }, { threshold: 0.1 });

    document.querySelectorAll('.reveal-up, .reveal-left, .reveal-right').forEach((el) => {
        observer.observe(el);
    });

    // Carousel Text Slider Engine Core Parameters
    let currentSlide = 0;
    const track = document.getElementById('sliderTrack');
    const slides = document.querySelectorAll('.service-card-wrapper');
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
            dot.setAttribute('aria-label', `Maps to slide ${i + 1}`);
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

    const sliderViewport = document.getElementById('servicesSlider');
    
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


    // Independent Client Reviews Slider Engine Block
    let currentReview = 0;
    const reviewTrack = document.getElementById('reviewTrack');
    const reviewSlides = document.querySelectorAll('.review-card-wrapper');
    const totalReviews = reviewSlides.length;
    const reviewDotsContainer = document.getElementById('reviewDotsContainer');
    let reviewAutoInterval;

    let reviewTouchStartX = 0;
    let reviewTouchEndX = 0;

    function buildReviewDots() {
        reviewDotsContainer.innerHTML = '';
        for (let i = 0; i < totalReviews; i++) {
            const dot = document.createElement('button');
            dot.className = `review-dot ${i === 0 ? 'dot-active' : ''}`;
            dot.setAttribute('aria-label', `Go to review ${i + 1}`);
            dot.addEventListener('click', () => {
                goToReview(i);
                restartReviewAutoSlide();
            });
            reviewDotsContainer.appendChild(dot);
        }
    }

    function updateReviewPosition() {
        reviewTrack.style.transform = `translateX(-${currentReview * 100}%)`;
        const dots = document.querySelectorAll('.review-dot');
        dots.forEach((dot, idx) => {
            if (idx === currentReview) {
                dot.classList.add('dot-active');
            } else {
                dot.classList.remove('dot-active');
            }
        });
    }

    function goToReview(index) {
        currentReview = index;
        updateReviewPosition();
    }

    function moveReview(direction) {
        currentReview += direction;
        if (currentReview >= totalReviews) {
            currentReview = 0;
        } else if (currentReview < 0) {
            currentReview = totalReviews - 1;
        }
        updateReviewPosition();
    }

    function startReviewAutoSlide() {
        reviewAutoInterval = setInterval(() => {
            moveReview(1);
        }, 6000); // Transitions automatically every 6 seconds
    }

    function restartReviewAutoSlide() {
        clearInterval(reviewAutoInterval);
        startReviewAutoSlide();
    }

    const reviewsSliderViewport = document.getElementById('reviewsSlider');

    reviewsSliderViewport.addEventListener('touchstart', (e) => {
        reviewTouchStartX = e.changedTouches[0].screenX;
        clearInterval(reviewAutoInterval);
    }, { passive: true });

    reviewsSliderViewport.addEventListener('touchend', (e) => {
        reviewTouchEndX = e.changedTouches[0].screenX;
        const threshold = 40;
        if (reviewTouchStartX - reviewTouchEndX > threshold) {
            moveReview(1);
        } else if (reviewTouchEndX - reviewTouchStartX > threshold) {
            moveReview(-1);
        }
        startReviewAutoSlide();
    }, { passive: true });

    buildReviewDots();
    startReviewAutoSlide();
</script>