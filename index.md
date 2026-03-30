---
layout: page
title: Home | Espacio Manila
---

<style>
    /* Professional Animation Core */
    .reveal-up { opacity: 0; transform: translateY(40px); transition: all 1.2s cubic-bezier(0.22, 1, 0.36, 1); }
    .reveal-left { opacity: 0; transform: translateX(-40px); transition: all 1.2s cubic-bezier(0.22, 1, 0.36, 1); }
    .reveal-right { opacity: 0; transform: translateX(40px); transition: all 1.2s cubic-bezier(0.22, 1, 0.36, 1); }
    .active { opacity: 1 !important; transform: translate(0,0) !important; }

    .gold-accent-line { width: 60px; height: 4px; background: #C5A059; margin-bottom: 2rem; }
    
    /* Footer visibility insurance */
    footer { position: relative; z-index: 50; display: block !important; }
</style>

<main class="bg-[#FDFBF7] text-[#011F3F]">

    <section class="relative min-h-[80vh] flex items-center pt-12 pb-20 overflow-hidden bg-[#FDFBF7]">
    
        <div class="absolute top-0 left-10 text-[15rem] font-serif font-black text-[#011F3F]/5 select-none -z-10 uppercase">
            Espacio
        </div>
    
        <div class="max-w-7xl mx-auto px-8 grid grid-cols-1 lg:grid-cols-12 gap-16 items-center">
            
            <div class="lg:col-span-7 reveal-left">
                <div class="flex items-center gap-4 mb-8">
                    <div class="h-[1px] w-12 bg-[#C5A059]"></div>
                    <span class="text-[10px] uppercase tracking-[0.5em] font-black text-[#011F3F]/60">Established 2026</span>
                </div>
    
                <h1 class="text-5xl md:text-7xl font-serif leading-[1.05] mb-8 text-[#011F3F]">
                    Virtual <span class="text-[#C5A059]">Infrastructure</span> <br>
                    for the Modern Elite.
                </h1>
                
                <p class="text-[19px] text-[#2D3748] leading-relaxed mb-12 max-w-xl">
                    We bridge the gap between your ambition and Philippine regulatory reality. 
                    Prestigious addresses, seamless compliance, and total peace of mind.
                </p>
    
                <div class="flex flex-wrap gap-6">
                    <a href="#quote" class="bg-[#011F3F] text-white px-12 py-5 text-[10px] font-black uppercase tracking-[0.3em] hover:bg-[#C5A059] transition-all shadow-2xl">
                        Get a Quote
                    </a>
                    <div class="flex items-center gap-3 px-6 py-5 border border-[#011F3F]/10 rounded-sm">
                        <span class="w-2 h-2 rounded-full bg-green-500 animate-pulse"></span>
                        <span class="text-[10px] font-black uppercase tracking-widest">Consultants Online</span>
                    </div>
                </div>
            </div>
    
            <div class="lg:col-span-5 reveal-right relative">
                <div class="aspect-[4/5] bg-[#011F3F] rounded-sm overflow-hidden shadow-2xl relative z-10">
                    <img src="https://images.unsplash.com/photo-1497366754035-f200968a6e72?auto=format&fit=crop&q=80" 
                         alt="Executive Office" 
                         class="w-full h-full object-cover grayscale hover:grayscale-0 transition-all duration-1000">
                </div>
                <div class="absolute -top-10 -right-10 w-40 h-40 border-t-2 border-r-2 border-[#C5A059]/30 -z-0"></div>
            </div>
    
        </div>
    </section>
    <section class="py-24 bg-white">
        <div class="max-w-7xl mx-auto px-8">
            <div class="text-center mb-20 reveal-up">
                <h2 class="text-3xl md:text-5xl font-serif mb-6">Our Core Services</h2>
                <div class="gold-accent-line mx-auto"></div>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-10">
                <div class="reveal-up p-10 border border-[#011F3F]/5 bg-[#FDFBF7] hover:border-[#C5A059] transition-all group">
                    <i class="fa-solid fa-map-location-dot text-3xl text-[#C5A059] mb-6"></i>
                    <h3 class="text-xl font-serif mb-4">Virtual Office Address</h3>
                    <p class="text-sm text-[#2D3748] leading-relaxed">Gain a prestigious business address in a prime location without the overhead costs of physical office space.</p>
                </div>
                <div class="reveal-up p-10 border border-[#011F3F]/5 bg-[#FDFBF7] hover:border-[#C5A059] transition-all" style="transition-delay: 100ms;">
                    <i class="fa-solid fa-file-signature text-3xl text-[#C5A059] mb-6"></i>
                    <h3 class="text-xl font-serif mb-4">Business Registration</h3>
                    <p class="text-sm text-[#2D3748] leading-relaxed">Seamlessly navigate the complexities of SEC and DTI, ensuring total compliance and peace of mind.</p>
                </div>
                <div class="reveal-up p-10 border border-[#011F3F]/5 bg-[#FDFBF7] hover:border-[#C5A059] transition-all" style="transition-delay: 200ms;">
                    <i class="fa-solid fa-calculator text-3xl text-[#C5A059] mb-6"></i>
                    <h3 class="text-xl font-serif mb-4">Tax Compliance</h3>
                    <p class="text-sm text-[#2D3748] leading-relaxed">Our expert team handles your tax requirements, from registration and bookkeeping to filing and reporting.</p>
                </div>
                <div class="reveal-up p-10 border border-[#011F3F]/5 bg-[#FDFBF7] hover:border-[#C5A059] transition-all">
                    <i class="fa-solid fa-users-rectangle text-3xl text-[#C5A059] mb-6"></i>
                    <h3 class="text-xl font-serif mb-4">Meeting Room Access</h3>
                    <p class="text-sm text-[#2D3748] leading-relaxed">Host important presentations and client signings in our modern, fully-equipped meeting rooms.</p>
                </div>
                <div class="reveal-up p-10 border border-[#011F3F]/5 bg-[#FDFBF7] hover:border-[#C5A059] transition-all md:col-span-2 lg:col-span-2" style="transition-delay: 300ms;">
                    <i class="fa-solid fa-briefcase text-3xl text-[#C5A059] mb-6"></i>
                    <h3 class="text-xl font-serif mb-4">Additional Solutions</h3>
                    <p class="text-sm text-[#2D3748] leading-relaxed">Benefit from payroll management, comprehensive bookkeeping, and administrative support tailored for growth.</p>
                </div>
            </div>
        </div>
    </section>

    <section class="py-24 bg-[#011F3F] text-[#FDFBF7]">
        <div class="max-w-7xl mx-auto px-8 grid grid-cols-1 lg:grid-cols-2 gap-20 items-center">
            <div class="reveal-left">
                <h2 class="text-4xl font-serif mb-12 italic text-[#C5A059]">Why Choose Espacio Manila?</h2>
                <div class="space-y-8">
                    <div class="flex gap-6">
                        <span class="text-[#C5A059] font-black text-xl">01</span>
                        <div>
                            <h4 class="font-bold uppercase tracking-widest text-sm mb-2">Convenience</h4>
                            <p class="text-[#FDFBF7]/60 text-sm">All your business needs met under one professional roof.</p>
                        </div>
                    </div>
                    <div class="flex gap-6">
                        <span class="text-[#C5A059] font-black text-xl">02</span>
                        <div>
                            <h4 class="font-bold uppercase tracking-widest text-sm mb-2">Affordability</h4>
                            <p class="text-[#FDFBF7]/60 text-sm">Save on expensive traditional office overheads instantly.</p>
                        </div>
                    </div>
                    <div class="flex gap-6">
                        <span class="text-[#C5A059] font-black text-xl">03</span>
                        <div>
                            <h4 class="font-bold uppercase tracking-widest text-sm mb-2">Expertise</h4>
                            <p class="text-[#FDFBF7]/60 text-sm">Guidance from professionals across all aspects of setup.</p>
                        </div>
                    </div>
                </div>
            </div>
            <div class="reveal-right bg-white/5 p-12 border border-white/10">
                <p class="text-2xl font-serif leading-relaxed italic mb-8">
                    "Ready to Level Up Your Business?"
                </p>
                <p class="text-[#FDFBF7]/70 mb-10">Let us help you determine the best solution for your unique business needs. Start your journey with us today.</p>
                <a href="/contact" class="inline-block bg-[#C5A059] text-[#011F3F] px-12 py-5 font-black uppercase tracking-[0.3em] text-[10px] hover:bg-white transition-all">Inquire Now</a>
            </div>
        </div>
    </section>

</main>

<script>
    // The Animation Engine
    const observer = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
            if (entry.isIntersecting) {
                entry.target.classList.add('active');
            }
        });
    }, { threshold: 0.15 });

    document.querySelectorAll('.reveal-up, .reveal-left, .reveal-right').forEach((el) => {
        observer.observe(el);
    });
</script>