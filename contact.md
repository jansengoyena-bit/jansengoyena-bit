---
layout: page
title: Home | Espacio Manila
---

<style>
    /* 1. Animation Core - Smooth & Professional */
    .reveal-up { opacity: 0; transform: translateY(30px); transition: all 1.2s cubic-bezier(0.22, 1, 0.36, 1); }
    .reveal-left { opacity: 0; transform: translateX(-40px); transition: all 1.2s cubic-bezier(0.22, 1, 0.36, 1); }
    .reveal-right { opacity: 0; transform: translateX(40px); transition: all 1.2s cubic-bezier(0.22, 1, 0.36, 1); }
    .active { opacity: 1 !important; transform: translate(0,0) !important; }

    /* 2. Layout Fix: Prevents footer from being "sucked up" */
    #espacio-main-content {
        min-height: 80vh;
        display: block;
        position: relative;
        background-color: #FDFBF7;
    }

    /* 3. High-Contrast Footer Overrides */
    footer {
        background-color: #011F3F !important;
        position: relative;
        z-index: 50;
        display: block !important;
        clear: both;
    }

    footer h4, footer .footer-title { color: #C5A059 !important; font-weight: 900 !important; }
    footer p, footer a, footer li, footer span { color: #FDFBF7 !important; opacity: 1 !important; }
    footer i { color: #C5A059 !important; }

    .gold-line { width: 50px; height: 3px; background: #C5A059; margin: 1.5rem 0; }
</style>

<div id="espacio-main-content">

    <section class="relative pt-16 pb-24 overflow-hidden">
        <div class="absolute top-0 left-0 text-[12vw] font-serif font-black text-[#011F3F]/5 pointer-events-none -z-10 uppercase select-none">
            Espacio
        </div>

        <div class="max-w-7xl mx-auto px-8 grid grid-cols-1 lg:grid-cols-12 gap-16 items-center">
            
            <div class="lg:col-span-7 reveal-left">
                <span class="text-[11px] uppercase tracking-[0.5em] font-black text-[#C5A059] mb-4 block">Complete Virtual Solutions</span>
                <h1 class="text-5xl md:text-7xl font-serif leading-tight mb-6 text-[#011F3F]">
                    Welcome to <br>
                    <span class="text-[#011F3F]">Espacio</span> <span class="text-[#C5A059] italic">Manila</span>
                </h1>
                <div class="gold-line"></div>
                <p class="text-[19px] text-[#2D3748] leading-relaxed mb-10 max-w-xl font-medium">
                    Empowering Entrepreneurs to Thrive. We provide everything you need to manage your business effectively—from prestigious addresses to total regulatory compliance.
                </p>
                <div class="flex flex-wrap gap-5">
                    <a href="#quote" class="bg-[#011F3F] text-white px-10 py-4 text-[10px] font-black uppercase tracking-[0.3em] hover:bg-[#C5A059] transition-all shadow-xl">Get a Quote</a>
                    <a href="/contact" class="border-2 border-[#011F3F] text-[#011F3F] px-10 py-4 text-[10px] font-black uppercase tracking-[0.3em] hover:bg-[#011F3F] hover:text-white transition-all">Inquire Now</a>
                </div>
            </div>

            <div class="lg:col-span-5 reveal-right relative">
                <div class="aspect-[4/5] bg-[#011F3F] rounded-sm overflow-hidden shadow-2xl relative z-10">
                    <img src="https://images.unsplash.com/photo-1497366754035-f200968a6e72?auto=format&fit=crop&q=80" alt="Executive Office" class="w-full h-full object-cover grayscale hover:grayscale-0 transition-all duration-1000">
                </div>
                <div class="absolute -top-6 -right-6 w-32 h-32 border-t-4 border-r-4 border-[#C5A059]/30 -z-0"></div>
            </div>
        </div>
    </section>

    <section class="py-24 bg-white">
        <div class="max-w-7xl mx-auto px-8">
            <h2 class="text-3xl font-serif text-[#011F3F] mb-16 reveal-up">Our Core Services</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-12">
                
                <div class="reveal-up group">
                    <h3 class="font-black uppercase tracking-widest text-[12px] text-[#C5A059] mb-4">01. Virtual Office</h3>
                    <p class="text-sm text-[#2D3748] leading-relaxed">Gain a prestigious business address in a prime location without the overhead costs of physical office space.</p>
                </div>

                <div class="reveal-up" style="transition-delay: 150ms;">
                    <h3 class="font-black uppercase tracking-widest text-[12px] text-[#C5A059] mb-4">02. Registration</h3>
                    <p class="text-sm text-[#2D3748] leading-relaxed">Seamlessly navigate the complexities of SEC and DTI, ensuring compliance and peace of mind.</p>
                </div>

                <div class="reveal-up" style="transition-delay: 300ms;">
                    <h3 class="font-black uppercase tracking-widest text-[12px] text-[#C5A059] mb-4">03. Tax Compliance</h3>
                    <p class="text-sm text-[#2D3748] leading-relaxed">Our expert team handles your tax registration, filing, and reporting with architectural precision.</p>
                </div>

            </div>
        </div>
    </section>

</div> <script>
    const observer = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
            if (entry.isIntersecting) {
                entry.target.classList.add('active');
            }
        });
    }, { threshold: 0.1 });

    document.querySelectorAll('.reveal-up, .reveal-left, .reveal-right').forEach((el) => {
        observer.observe(el);
    });
</script>