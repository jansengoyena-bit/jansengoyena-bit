---
layout: page
title: Home | Espacio Manila
---

<section class="relative min-h-[90vh] flex items-center bg-[#FDFBF7] overflow-hidden py-20">
    <div class="max-w-7xl mx-auto px-8 grid grid-cols-1 lg:grid-cols-2 gap-16 items-center">

        <div class="space-y-8 animate-fade-in">
            <h2 class="text-[10px] uppercase tracking-[0.5em] text-[#C5A059] font-black">Financial Intelligence</h2>
            <h1 class="text-4xl md:text-6xl text-[#011F3F] font-bold serif leading-tight">
                Strategic <span class="italic text-[#C5A059] font-medium">Financial</span> Leadership for Growth.
            </h1>
            <p class="text-lg text-[#011F3F]/70 leading-relaxed max-w-lg font-medium">
                We help clients execute their vision through growth and profitability. Boutique accounting, business consulting, and sophisticated financial strategies.
            </p>
            <div class="pt-4">
                <div class="flex items-center gap-4 text-[#011F3F]/40">
                    <div class="h-[1px] w-12 bg-[#C5A059]"></div>
                    <span class="text-[9px] uppercase tracking-widest font-bold">The Architect's Protocol</span>
                </div>
            </div>
        </div>

        <div class="relative">
            <div class="bg-white p-8 md:p-10 shadow-[0_35px_60px_-15px_rgba(1,31,63,0.1)] rounded-2xl border border-[#011F3F]/5">
                
                <div id="form-container">
                    <h3 class="text-xl text-[#011F3F] serif mb-8 uppercase tracking-tight">Secure Your <span class="text-[#C5A059]">Consultation</span></h3>
                    
                    <form id="nexus-contact-form" class="space-y-5">
                        <div class="grid grid-cols-2 gap-4">
                            <div class="space-y-1">
                                <label class="text-[9px] uppercase tracking-widest font-black text-[#011F3F]/40 ml-1">First Name</label>
                                <input type="text" name="entry.539737381" required class="w-full bg-[#FDFBF7] border-b border-[#011F3F]/10 px-0 py-2 text-[#011F3F] focus:outline-none focus:border-[#C5A059] transition-all text-sm font-medium" />
                            </div>
                            <div class="space-y-1">
                                <label class="text-[9px] uppercase tracking-widest font-black text-[#011F3F]/40 ml-1">Last Name</label>
                                <input type="text" name="entry.772958265" required class="w-full bg-[#FDFBF7] border-b border-[#011F3F]/10 px-0 py-2 text-[#011F3F] focus:outline-none focus:border-[#C5A059] transition-all text-sm font-medium" />
                            </div>
                        </div>

                        <div class="space-y-1">
                            <label class="text-[9px] uppercase tracking-widest font-black text-[#011F3F]/40 ml-1">Business Email</label>
                            <input type="email" name="entry.1928928074" required class="w-full bg-[#FDFBF7] border-b border-[#011F3F]/10 px-0 py-2 text-[#011F3F] focus:outline-none focus:border-[#C5A059] transition-all text-sm font-medium" />
                        </div>

                        <div class="space-y-1 group">
                            <label class="text-[9px] uppercase tracking-widest font-black text-[#011F3F]/40 ml-1">Nature of Inquiry</label>
                            <textarea 
                                name="entry.2087135975" 
                                required 
                                rows="3" 
                                placeholder="How can we assist your growth?" 
                                class="w-full bg-[#FDFBF7] border-b border-[#011F3F]/10 px-0 py-2 text-[#011F3F] focus:outline-none focus:border-[#C5A059] transition-all text-sm font-medium resize-none"
                            ></textarea>
                        </div>
                        <button type="submit" id="submit-btn" class="w-full bg-[#011F3F] text-[#FDFBF7] font-black uppercase tracking-[0.4em] py-4 mt-4 hover:bg-[#C5A059] transition-all duration-500 text-[10px] flex items-center justify-center gap-3">
                            <span id="btn-text">Transmit Inquiry</span>
                        </button>
                    </form>

                    <div id="success-notification" class="hidden text-center py-10 animate-fade-in">
                        <i class="fa-solid fa-circle-check text-[#C5A059] text-4xl mb-4"></i>
                        <h2 class="serif text-xl text-[#011F3F]">Transmission Received</h2>
                        <p class="text-[9px] uppercase tracking-[0.3em] text-[#011F3F]/50 mt-2">The Architect will review your data shortly.</p>
                    </div>
                </div>

            </div>
            <div class="absolute -bottom-6 -right-6 w-32 h-32 bg-[#C5A059]/10 rounded-full blur-2xl -z-10"></div>
        </div>
    </div>
</section>

<script>
    const GOOGLE_FORM_ACTION = "https://docs.google.com/forms/d/e/1FAIpQLSfbokdyYUv_OhY-pXKoj4ZbVaPDij4iZ5QK077CgYraUdVBIQ/formResponse";
    const contactForm = document.getElementById('nexus-contact-form');
    const successNotif = document.getElementById('success-notification');
    const submitBtn = document.getElementById('submit-btn');
    const btnText = document.getElementById('btn-text');

    contactForm.addEventListener('submit', function(e) {
        e.preventDefault();
        btnText.innerText = "Transmitting...";
        submitBtn.disabled = true;

        const formData = new FormData(contactForm);

        fetch(GOOGLE_FORM_ACTION, {
            method: 'POST',
            mode: 'no-cors',
            body: formData
        })
        .then(() => {
            contactForm.classList.add('hidden');
            successNotif.classList.remove('hidden');
        })
        .catch(err => {
            alert("Connection error. Please try again.");
            btnText.innerText = "Transmit Inquiry";
            submitBtn.disabled = false;
        });
    });
</script>

<style>
   #success-notification.hidden {
        display: none !important;
    }

    /* 3. Ensure the Form actually hides when the Success Message appears */
    #nexus-contact-form.hidden {
        display: none !important;
    }

    /* 4. Smooth Animation for the Success Message */
    .animate-fade-in {
        animation: fadeIn 0.6s ease-out forwards;
    }
    @keyframes fadeIn {
        from { opacity: 0; transform: translateY(10px); }
        to { opacity: 1; transform: translateY(0); }
    }
</style>