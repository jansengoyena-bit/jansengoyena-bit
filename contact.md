---
layout: page
title: Contact Us
---

<section class="relative min-h-screen flex items-center justify-center py-24">
    <div class="absolute inset-0 z-0">
        <img src="espaciomanila.jpg" alt="Espacio Manila Background" class="w-full h-full object-cover">
        <div class="absolute inset-0 bg-white/20 backdrop-blur-[3px]"></div>
    </div>

    <div class="max-w-4xl w-full mx-auto px-8 relative z-10">
        
        <div class="bg-[#FDFBF7] shadow-[0_35px_60px_-15px_rgba(1,31,63,0.3)] rounded-2xl overflow-hidden reveal">
            
            <div class="pt-16 pb-8 px-12 text-center border-b border-[#011F3F]/5">
                <img src="image_09a5d7.png" alt="Espacio Manila Logo" class="h-14 w-auto mx-auto mb-8 opacity-90">
                <h1 class="text-3xl md:text-5xl text-[#011F3F] font-bold serif tracking-tight uppercase leading-none">
                    Let's Start the <br><span class="italic text-[#C5A059] font-medium">Conversation</span>
                </h1>
                <div class="max-w-md mx-auto mt-6">
                    <p class="text-[#011F3F]/50 text-[10px] md:text-[11px] uppercase tracking-[0.4em] leading-relaxed font-black">
                        To inquire about our spaces and services, get in touch with us using the form below.
                    </p>
                </div>
            </div>

            <div class="p-8 md:p-14 bg-white">
                <form action="https://formspree.io/f/your-id" method="POST" class="space-y-6">
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                        <div class="space-y-2 group">
                            <label class="text-[10px] uppercase tracking-widest font-black text-[#011F3F]/40 ml-1 group-focus-within:text-[#C5A059] transition">First Name</label>
                            <input type="text" name="first_name" required placeholder="Jansen" 
                                class="w-full bg-[#FDFBF7] border-b-2 border-[#011F3F]/10 px-0 py-3 text-[#011F3F] placeholder:text-gray-300 focus:outline-none focus:border-[#C5A059] transition-all duration-300 text-sm font-medium">
                        </div>
                        
                        <div class="space-y-2 group">
                            <label class="text-[10px] uppercase tracking-widest font-black text-[#011F3F]/40 ml-1 group-focus-within:text-[#C5A059] transition">Last Name</label>
                            <input type="text" name="last_name" required placeholder="Goyena" 
                                class="w-full bg-[#FDFBF7] border-b-2 border-[#011F3F]/10 px-0 py-3 text-[#011F3F] placeholder:text-gray-300 focus:outline-none focus:border-[#C5A059] transition-all duration-300 text-sm font-medium">
                        </div>
                    </div>

                    <div class="space-y-2 group">
                        <label class="text-[10px] uppercase tracking-widest font-black text-[#011F3F]/40 ml-1 group-focus-within:text-[#C5A059] transition">Business Email</label>
                        <input type="email" name="email" required placeholder="email@company.com" 
                            class="w-full bg-[#FDFBF7] border-b-2 border-[#011F3F]/10 px-0 py-3 text-[#011F3F] placeholder:text-gray-300 focus:outline-none focus:border-[#C5A059] transition-all duration-300 text-sm font-medium">
                    </div>

                    <div class="space-y-2 group">
                        <label class="text-[10px] uppercase tracking-widest font-black text-[#011F3F]/40 ml-1 group-focus-within:text-[#C5A059] transition">Contact Number</label>
                        <input type="tel" name="phone" placeholder="+63 XXX XXX XXXX" 
                            class="w-full bg-[#FDFBF7] border-b-2 border-[#011F3F]/10 px-0 py-3 text-[#011F3F] placeholder:text-gray-300 focus:outline-none focus:border-[#C5A059] transition-all duration-300 text-sm font-medium">
                    </div>

                    <div class="space-y-2 relative group">
                        <label class="text-[10px] uppercase tracking-widest font-black text-[#011F3F]/40 ml-1 group-focus-within:text-[#C5A059] transition">Nature of Inquiry</label>
                        <select name="subject" 
                            class="w-full bg-[#FDFBF7] border-b-2 border-[#011F3F]/10 px-0 py-3 text-[#011F3F] focus:outline-none focus:border-[#C5A059] transition-all duration-300 text-sm appearance-none cursor-pointer font-medium">
                            <option>What can we help you with?</option>
                            <option>Virtual Office Solutions</option>
                            <option>Tax & Accounting Compliance</option>
                            <option>Legal Counsel & Retainers</option>
                            <option>SEC / BIR Company Registration</option>
                        </select>
                        <div class="absolute right-2 top-[42px] pointer-events-none">
                            <i class="fa-solid fa-chevron-down text-[#C5A059] text-[10px]"></i>
                        </div>
                    </div>

                    <button type="submit" 
                        class="w-full bg-[#011F3F] text-[#FDFBF7] font-black uppercase tracking-[0.4em] py-5 mt-6 hover:bg-[#C5A059] transition-all duration-500 text-sm group flex items-center justify-center gap-3 shadow-lg hover:shadow-gold/20">
                        Transmit Inquiry
                        <i class="fa-solid fa-chevron-right text-[10px] group-hover:translate-x-1 transition-transform"></i>
                    </button>
                </form>
            </div>
        </div>
    </div>
</section>