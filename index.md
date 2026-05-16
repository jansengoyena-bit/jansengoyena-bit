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
    .service-card-wrapper {
        flex: 0 0 100%;
        width: 100%;
        box-sizing: border-box;
        padding: 0 20px; /* Kept side padding for mobile screen safety */
    }
    .service-card {
        background: transparent !important; /* Removed white card block */
        padding: 40px 0 !important; /* Shifted focus entirely to layout breathing room */
        border: none !important; /* Stripped container outline constraints */
        box-shadow: none !important; /* Stripped background elevation tracking */
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
    .slider-dot {
        width: 10px;
        height: 10px;
        border-radius: 50%;
        background-color: rgba(1, 31, 63, 0.15);
        transition: all 0.3s ease;
        border: none;
        padding: 0;
        cursor: pointer;
    }
    .slider-dot.dot-active {
        background-color: #C5A059;
        width: 36px;
        border-radius: 5px;
    }
    .slider-nav-btn {
        background: transparent; /* Changed button wrappers to blend transparently */
        color: #011F3F;
        border: 1px solid rgba(1, 31, 63, 0.1);
        width: 56px;
        height: 56px;
        display: flex;
        align-items: center;
        justify-content: center;
        cursor: pointer;
        transition: all 0.3s ease;
    }
    .slider-nav-btn:hover {
        background: #011F3F;
        color: white;
        border-color: #011F3F;
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

                <div class="flex items-center justify-between max-w-md mx-auto mt-12">
                    <button class="slider-nav-btn" onclick="moveSlide(-1)" aria-label="Previous slide">
                        <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><polyline points="15 18 9 12 15 6"></polyline></svg>
                    </button>
                    
                    <div class="flex gap-3.5" id="sliderDotsContainer">
                        </div>
                    
                    <button class="slider-nav-btn" onclick="moveSlide(1)" aria-label="Next slide">
                        <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><polyline points="9 18 15 12 9 6"></polyline></svg>
                    </button>
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
</script>