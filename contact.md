---
layout: page
title: Contact Us | Espacio Manila
---

<main>
    <section class="relative min-h-screen flex items-center justify-center py-24 bg-[#FDFBF7]">
        <div class="max-w-4xl w-full mx-auto px-8 relative z-10">
            <div class="bg-white shadow-[0_35px_60px_-15px_rgba(1,31,63,0.1)] rounded-2xl overflow-hidden">

                <div id="form-container" class="p-8 md:p-14">
                    <div class="text-center mb-12">
                        <h1 class="text-2xl md:text-4xl text-[#011F3F] font-bold serif uppercase tracking-tight">
                            Let's Start the <span class="italic text-[#C5A059] font-medium">Conversation</span>
                        </h1>
                    </div>

                    <form id="nexus-contact-form" class="space-y-6">
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                            <div class="space-y-2 group">
                                <label class="text-[10px] uppercase tracking-widest font-black text-[#011F3F]/40 ml-1">First Name</label>
                                <input type="text" name="entry.539737381" required placeholder="Jansen" class="w-full bg-[#FDFBF7] border-b-2 border-[#011F3F]/10 px-0 py-3 text-[#011F3F] focus:outline-none focus:border-[#C5A059] transition-all text-sm font-medium" />
                            </div>
                            
                            <div class="space-y-2 group">
                                <label class="text-[10px] uppercase tracking-widest font-black text-[#011F3F]/40 ml-1">Last Name</label>
                                <input type="text" name="entry.772958265" required placeholder="Goyena" class="w-full bg-[#FDFBF7] border-b-2 border-[#011F3F]/10 px-0 py-3 text-[#011F3F] focus:outline-none focus:border-[#C5A059] transition-all text-sm font-medium" />
                            </div>
                        </div>

                        <div class="space-y-2 group">
                            <label class="text-[10px] uppercase tracking-widest font-black text-[#011F3F]/40 ml-1">Business Email</label>
                            <input type="email" name="entry.1928928074" required placeholder="email@company.com" class="w-full bg-[#FDFBF7] border-b-2 border-[#011F3F]/10 px-0 py-3 text-[#011F3F] focus:outline-none focus:border-[#C5A059] transition-all text-sm font-medium" />
                        </div>

                        <div class="space-y-2 group">
                            <label class="text-[10px] uppercase tracking-widest font-black text-[#011F3F]/40 ml-1">Contact Number</label>
                            <input type="tel" name="entry.512370401" placeholder="+63 XXX XXX XXXX" class="w-full bg-[#FDFBF7] border-b-2 border-[#011F3F]/10 px-0 py-3 text-[#011F3F] focus:outline-none focus:border-[#C5A059] transition-all text-sm font-medium" />
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

                        <button type="submit" id="submit-btn" class="w-full bg-[#011F3F] text-[#FDFBF7] font-black uppercase tracking-[0.4em] py-5 mt-6 hover:bg-[#C5A059] transition-all duration-500 text-sm flex items-center justify-center gap-3 shadow-lg">
                            <span id="btn-text">Transmit Inquiry</span>
                            <i class="fa-solid fa-chevron-right text-[10px]"></i>
                        </button>
                    </form>

                    <div id="success-notification" class="hidden text-center py-10 animate-fade-in">
                        <i class="fa-solid fa-circle-check text-[#C5A059] text-5xl mb-6"></i>
                        <h2 class="serif text-3xl text-[#011F3F]">Transmission Received</h2>
                        <p class="text-[10px] uppercase tracking-[0.4em] text-[#011F3F]/50 mt-4">The Architect will contact you shortly.</p>
                        <button onclick="location.reload()" class="mt-8 text-[9px] uppercase tracking-widest text-[#C5A059] border-b border-[#C5A059] pb-1">Send another inquiry</button>
                    </div>

                </div>
            </div>
        </div>
    </section>
</main>

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
        submitBtn.style.opacity = "0.7";

        const formData = new FormData(contactForm);

        fetch(GOOGLE_FORM_ACTION, {
            method: 'POST',
            mode: 'no-cors',
            body: formData
        })
        .then(() => {
            contactForm.classList.add('hidden');
            successNotif.classList.remove('hidden');
            successNotif.scrollIntoView({ behavior: 'smooth', block: 'center' });
        })
        .catch(err => {
            console.error(err);
            alert("Transmission error. Please check your connection.");
            btnText.innerText = "Try Again";
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