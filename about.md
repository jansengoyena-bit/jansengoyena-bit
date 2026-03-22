---
layout: page
title: About Espacio Manila
---

<style>
    #about-nexus {
        background-color: #FAFAFA;
        color: #011F3F;
        font-family: 'Inter', sans-serif;
    }
    .hero-about {
        background-color: #011F3F;
        padding: 120px 24px;
        position: relative;
        overflow: hidden;
        text-align: center;
    }
    .hero-accent {
        position: absolute;
        right: -5%;
        top: 0;
        width: 35%;
        height: 100%;
        background: #C5A059;
        opacity: 0.1;
        transform: skewX(15deg);
    }
    .stat-grid {
        max-width: 1100px;
        margin: -60px auto 0;
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
        gap: 20px;
        padding: 0 24px;
        position: relative;
        z-index: 10;
    }
    .stat-card {
        background: white;
        padding: 40px 20px;
        text-align: center;
        box-shadow: 0 15px 35px rgba(1, 31, 63, 0.1);
        border-top: 5px solid #C5A059;
    }
    .stat-number {
        font-size: 2.8rem;
        font-weight: 800;
        color: #011F3F;
        display: block;
        font-family: serif;
    }
    .stat-label {
        font-size: 10px;
        text-transform: uppercase;
        letter-spacing: 3px;
        color: #C5A059;
        font-weight: 900;
        margin-top: 10px;
        display: block;
    }
    .content-section {
        max-width: 850px;
        margin: 100px auto;
        padding: 0 24px;
        line-height: 1.9;
    }
    .nexus-pullquote {
        font-size: 1.6rem;
        font-family: serif;
        font-style: italic;
        border-left: 6px solid #C5A059;
        padding: 20px 0 20px 40px;
        margin: 50px 0;
        color: #011F3F;
        background: rgba(197, 160, 89, 0.05);
    }
</style>

<div id="about-nexus">

    <header class="hero-about">
        <div class="hero-accent"></div>
        <div style="position: relative; z-index: 5;">
            <span style="color: #C5A059; text-transform: uppercase; letter-spacing: 6px; font-size: 11px; font-weight: bold;">The Nexus of Enterprise</span>
            <h1 style="color: white; font-family: serif; font-size: clamp(2.5rem, 5vw, 4.5rem); margin: 25px 0; text-transform: uppercase;">Defining <span style="color: #C5A059;">The Architect</span></h1>
            <p style="color: rgba(255,255,255,0.6); max-width: 650px; margin: 0 auto; font-size: 15px; font-weight: 300;">Espacio Manila provides high-tier accounting, legal, and business registration infrastructure for the modern Philippine market.</p>
        </div>
    </header>

    <div class="stat-grid">
        <div class="stat-card">
            <span class="stat-number">10+</span>
            <span class="stat-label">Years of Mastery</span>
        </div>
        <div class="stat-card">
            <span class="stat-number">500+</span>
            <span class="stat-label">Clients Governed</span>
        </div>
        <div class="stat-card">
            <span class="stat-number">CPAs</span>
            <span class="stat-label">Precision Team</span>
        </div>
        <div class="stat-card">
            <span class="stat-number">Lawyers</span>
            <span class="stat-label">Legal Authority</span>
        </div>
    </div>

    <article class="content-section">
        <h2 style="font-family: serif; font-size: 2.5rem; margin-bottom: 25px; color: #011F3F;">The Espacio Manila Standard</h2>
        <div style="height: 5px; width: 80px; background: #C5A059; margin-bottom: 50px;"></div>
        
        <p>Espacio Manila is a collective of elite CPAs and Lawyers dedicated to providing the technical architecture required for business success. We serve as the bridge between international ambition and local regulatory compliance, offering a seamless interface for freelancers, SMEs, and global corporations.</p>

        <blockquote class="nexus-pullquote">
            "We provide the foundation. You build the legacy. Outsource your complexities to the experts."
        </blockquote>

        <p>From the initial SEC incorporation and BIR registration to ongoing monthly tax compliance and audited financial statements, our suite is designed for total operational efficiency. We ensure your employees are paid accurately and your books remain irreproachable, allowing you to focus entirely on growth.</p>
        
        <div style="margin-top: 80px; text-align: center;">
            <a href="/services" style="background: #011F3F; color: #C5A059; padding: 22px 50px; text-decoration: none; font-weight: 900; text-transform: uppercase; letter-spacing: 3px; display: inline-block; border: 1px solid #C5A059;">
                Explore The Suite
            </a>
        </div>
    </article>

</div>