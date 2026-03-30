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
    
    .gold-accent { color: #C5A059; }
    .bg-navy { background-color: #011F3F; }
    
    .service-card {
        background: white;
        padding: 40px;
        border: 1px solid rgba(1, 31, 63, 0.05);
        transition: all 0.5s ease;
    }
    .service-card:hover {
        border-color: #C5A059;
        transform: translateY(-5px);
    }

    /* 3. Footer Visibility Insurance */
    footer {
        position: relative;
        z-index: 50;
        background-color: #011F3F !important;
        display: block !important;
    }
    footer * { color: #FDFBF7 !important; }
</style>

<div id="espacio-landing">

       <section class="relative pt-12 pb-20 lg:min-h-[85vh] flex items-center bg-[#FDFBF7]">
        <div class="absolute top-0 left-0 w-full h-full pointer-events-none -z-10 overflow-hidden">
            <span class="absolute top-10 left-10 text-[12vw] font-serif font-black opacity-[0.03] uppercase text-navy">Espacio</span>
        </div>
    
        <div class="max-w-7xl mx-auto px-8 grid grid-cols-1 lg:grid-cols-12 gap-16 items-center">
            <div class="lg:col-span-7 reveal-left">
                <span class="text-[11px] uppercase tracking-[0.4em] font-black text-[#C5A059] mb-6 block">Your Complete Business Infrastructure</span>
                <h1 class="text-4xl md:text-6xl font-serif leading-tight mb-8 text-[#011F3F]">
                    Welcome to <br />Espacio <span class="italic text-[#C5A059]">Manila</span>
                </h1>
                <h2 class="text-xl font-bold mb-6 text-[#011F3F]">Empowering Entrepreneurs to Thrive</h2>
                <p class="text-[19px] text-[#2D3748] leading-relaxed mb-10 max-w-xl">
                    Are you an entrepreneur looking for a professional and seamless way to establish and grow your business? 
                    Look no further than <b>Espacio Manila</b>. We provide everything you need to manage your business effectively, from virtual addresses to full regulatory compliance.
                </p>
                <div class="flex flex-wrap gap-4">
                    <a href="#quote" class="bg-[#011F3F] text-white px-10 py-4 text-[10px] font-black uppercase tracking-[0.3em] hover:bg-[#C5A059] transition-all shadow-lg">Get a Quote</a>
                    <a href="#inquiry" class="border-2 border-[#011F3F] text-[#011F3F] px-10 py-4 text-[10px] font-black uppercase tracking-[0.3em] hover:bg-[#011F3F] hover:text-white transition-all">Inquire Now</a>
                </div>
            </div>
    
            <div class="lg:col-span-5 reveal-right">
                <div class="relative">
                    <div class="aspect-[4/5] bg-[#011F3F] rounded-sm overflow-hidden shadow-[0_20px_50px_rgba(1,31,63,0.3)] border-b-8 border-r-8 border-[#C5A059]/10">
                        <img src="https://images.unsplash.com/photo-1497366216548-37526070297c?auto=format&fit=crop&q=80&w=1200" 
                             alt="Modern Professional Office" 
                             class="w-full h-full object-cover transition-transform duration-700 hover:scale-110" />
                    </div>
                    
                    
                    
                    <div class="absolute -top-6 -right-6 w-32 h-32 border-t-4 border-l-4 border-[#C5A059]/30 -z-10"></div>
                </div>
            </div>
        </div>
    </section>
    <section class="py-24 bg-white">
        <div class="max-w-7xl mx-auto px-8">
            <div class="reveal-up mb-16 text-center">
                <h2 class="text-3xl md:text-5xl font-serif mb-4">Our Core Services</h2>
                <div class="w-20 h-1 bg-navy mx-auto"></div>
            </div>
    
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <div class="service-card reveal-up">
                    <h3 class="font-black uppercase tracking-widest text-xs gold-accent mb-4">Virtual Office Address</h3>
                    <p class="text-sm leading-relaxed text-[#2D3748]">Gain a prestigious business address in a prime location without the overhead costs of physical office space.</p>
                </div>
                <div class="service-card reveal-up" style="transition-delay: 100ms;">
                    <h3 class="font-black uppercase tracking-widest text-xs gold-accent mb-4">Business Registration</h3>
                    <p class="text-sm leading-relaxed text-[#2D3748]">Seamlessly navigate the complexities of business registration, ensuring compliance and peace of mind.</p>
                </div>
                <div class="service-card reveal-up" style="transition-delay: 200ms;">
                    <h3 class="font-black uppercase tracking-widest text-xs gold-accent mb-4">Tax Compliance</h3>
                    <p class="text-sm leading-relaxed text-[#2D3748]">Our expert team takes care of your tax compliance requirements, from registration to filing and reporting.</p>
                </div>
                <div class="service-card reveal-up">
                    <h3 class="font-black uppercase tracking-widest text-xs gold-accent mb-4">Meeting Room Access</h3>
                    <p class="text-sm leading-relaxed text-[#2D3748]">Host important meetings and presentations in our modern and equipped meeting rooms.</p>
                </div>
                <div class="service-card reveal-up lg:col-span-2" style="transition-delay: 100ms;">
                    <h3 class="font-black uppercase tracking-widest text-xs gold-accent mb-4">Additional Solutions</h3>
                    <p class="text-sm leading-relaxed text-[#2D3748]">Benefit from other essential services, including payroll, bookkeeping, and other administrative support to streamline your operations.</p>
                </div>
            </div>
        </div>
    </section>
    <section class="py-24 bg-navy text-[#FDFBF7]">
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
                        <a href="/quote" class="block w-full text-center bg-[#C5A059] text-navy py-5 font-black uppercase tracking-[0.3em] text-[10px] hover:bg-white transition-all">Get a Quote</a>
                        
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
    const observer = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
            if (entry.isIntersecting) entry.target.classList.add('active');
        });
    }, { threshold: 0.1 });

    document.querySelectorAll('.reveal-up, .reveal-left, .reveal-right').forEach((el) => {
        observer.observe(el);
    });
</script>