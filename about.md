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

    /* Animation Classes */
    .reveal-left { opacity: 0; transform: translateX(-50px); transition: all 1.2s ease-out; }
    .reveal-right { opacity: 0; transform: translateX(50px); transition: all 1.2s ease-out; }
    .reveal-up { opacity: 0; transform: translateY(30px); transition: all 1.2s ease-out; }
    .active { opacity: 1 !important; transform: translate(0,0) !important; }

    .content-section { max-width: 1000px; margin: 100px auto; padding: 0 24px; }
    
    .value-card {
        background: white;
        padding: 40px;
        border-left: 4px solid #99793D;
        box-shadow: 0 5px 15px rgba(0,0,0,0.05);
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
            <p style="font-size: 18px; color: #2D3748; line-height: 1.8;">
                To provide the highest level of professional accounting, legal, and business registration services. We aim to empower entrepreneurs by removing the friction of compliance, allowing them to focus on innovation and sustainable growth.
            </p>
        </div>
        <div class="reveal-right">
            <h2 style="font-family: serif; font-size: 2rem; color: #001529; border-bottom: 3px solid #99793D; display: inline-block; margin-bottom: 20px;">Our Vision</h2>
            <p style="font-size: 18px; color: #2D3748; line-height: 1.8;">
                To be the premier business infrastructure provider in the Philippines, recognized for our uncompromising integrity, technical precision, and our ability to turn complex regulatory landscapes into seamless operational pathways.
            </p>
        </div>
    </section>

    <section class="content-section" style="margin-top: 0;">
        <h2 class="reveal-up text-center" style="font-family: serif; font-size: 2.5rem; margin-bottom: 50px;">Core Values</h2>
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
            <div class="value-card reveal-up" style="transition-delay: 100ms;">
                <h3 style="font-weight: 900; color: #000; text-transform: uppercase; letter-spacing: 1px; margin-bottom: 15px;">Integrity</h3>
                <p style="font-size: 15px; color: #4A5568;">We uphold the highest ethical standards, ensuring every filing and statement reflects the absolute truth of your business standing.</p>
            </div>
            <div class="value-card reveal-up" style="transition-delay: 200ms;">
                <h3 style="font-weight: 900; color: #000; text-transform: uppercase; letter-spacing: 1px; margin-bottom: 15px;">Precision</h3>
                <p style="font-size: 15px; color: #4A5568;">In the world of taxation and law, details are everything. We execute every task with architectural accuracy.</p>
            </div>
            <div class="value-card reveal-up" style="transition-delay: 300ms;">
                <h3 style="font-weight: 900; color: #000; text-transform: uppercase; letter-spacing: 1px; margin-bottom: 15px;">Commitment</h3>
                <p style="font-size: 15px; color: #4A5568;">Your success is our success. We remain committed to your long-term legacy as your strategic business ally.</p>
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
</script>