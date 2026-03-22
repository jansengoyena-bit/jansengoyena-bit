---
layout: page
title: Professional Suite & Quotation
---

<style>
    #espacio-nexus {
        background-color: #FDFBF7;
        color: #011F3F;
        font-family: 'Inter', -apple-system, sans-serif;
    }
    .hero-section {
        position: relative;
        padding: 100px 20px;
        background: #011F3F;
        text-align: center;
        overflow: hidden;
    }
    .hero-image {
        position: absolute;
        inset: 0;
        background-image: url('espaciomanila.jpg');
        background-size: cover;
        background-position: center;
        opacity: 0.25;
        z-index: 1;
    }
    .hero-overlay {
        position: absolute;
        inset: 0;
        background: linear-gradient(to bottom, #011F3F, transparent, #011F3F);
        z-index: 2;
    }
    .hero-text { position: relative; z-index: 3; }
    
    .content-grid {
        max-width: 1200px;
        margin: 0 auto;
        padding: 60px 24px;
        display: flex;
        flex-wrap: wrap;
        gap: 50px;
    }
    .selection-side { flex: 1; min-width: 320px; }
    .calculator-side { flex: 0 0 400px; }

    .input-box { margin-bottom: 40px; }
    .label-meta {
        font-size: 10px;
        text-transform: uppercase;
        letter-spacing: 3px;
        color: #C5A059;
        font-weight: 900;
        margin-bottom: 12px;
        display: block;
    }
    .dropdown-ui, .form-input {
        width: 100%;
        padding: 16px;
        border: 1px solid rgba(1, 31, 63, 0.1);
        background: white;
        color: #011F3F;
        font-size: 14px;
        margin-bottom: 15px;
    }

    .sticky-card {
        background: #011F3F;
        color: white;
        padding: 45px;
        border-radius: 4px;
        position: sticky;
        top: 20px;
        box-shadow: 0 30px 60px rgba(0,0,0,0.2);
        border-top: 5px solid #C5A059;
    }
    .price-large {
        font-size: 3.5rem;
        color: #C5A059;
        font-family: serif;
        margin: 10px 0;
    }

    .form-section {
        margin-top: 60px;
        padding-top: 60px;
        border-top: 1px solid rgba(1, 31, 63, 0.1);
    }

    @media (max-width: 1024px) {
        .calculator-side { flex: 1; width: 100%; }
        .sticky-card { position: relative; top: 0; }
    }
</style>

<div id="espacio-nexus">

    <div class="hero-section">
        <div class="hero-image"></div>
        <div class="hero-overlay"></div>
        <div class="hero-text">
            <span style="color: #C5A059; text-transform: uppercase; letter-spacing: 5px; font-size: 10px; font-weight: bold;">Full Service Portfolio</span>
            <h1 style="color: white; font-family: serif; font-size: 3.5rem; margin: 15px 0; text-transform: uppercase;">Tailor Your <span style="font-style: italic; color: #C5A059;">Suite</span></h1>
        </div>
    </div>

    <div class="content-grid">
        
        <div class="selection-side">
            <div class="input-box">
                <span class="label-meta">01. Virtual Office & Address</span>
                <select id="vo_choice" onchange="calculateQuote()" class="dropdown-ui">
                    <option value="0">Not Required</option>
                    <option value="1500">Makati (Kamagong) — ₱1,500/mo</option>
                    <option value="2500">BGC (High Street) — ₱2,500/mo</option>
                    <option value="5000">Corporate HQ — ₱5,000/mo</option>
                </select>
            </div>

            <div class="input-box">
                <span class="label-meta">02. Bookkeeping & Tax Filing (Monthly)</span>
                <select id="bookkeeping_choice" onchange="calculateQuote()" class="dropdown-ui">
                    <option value="0">None</option>
                    <option value="3500">Micro (Up to 20 Trans.) — ₱3,500/mo</option>
                    <option value="7500">Small (Up to 50 Trans.) — ₱7,500/mo</option>
                    <option value="15000">Medium (Up to 100 Trans.) — ₱15,000/mo</option>
                </select>
            </div>

            <div class="input-box">
                <span class="label-meta">03. End-to-End Accounting (Monthly)</span>
                <select id="ete_choice" onchange="calculateQuote()" class="dropdown-ui">
                    <option value="0">None</option>
                    <option value="25000">Startup Suite — ₱25,000/mo</option>
                    <option value="50000">SME Suite — ₱50,000/mo</option>
                </select>
            </div>

            <div class="input-box">
                <span class="label-meta">04. Audited Financial Statements (Annual)</span>
                <select id="afs_choice" onchange="calculateQuote()" class="dropdown-ui">
                    <option value="0">None</option>
                    <option value="20000">Basic Audit — ₱20,000</option>
                    <option value="45000">Standard Audit — ₱45,000</option>
                    <option value="85000">Complex Corporate — ₱85,000</option>
                </select>
            </div>

            <div class="form-section">
                <span class="label-meta">05. Secure Your Quotation</span>
                <h2 style="font-family: serif; font-size: 2rem; margin-bottom: 25px;">Get a Price Quote</h2>
                
                <form action="https://formspree.io/f/your-id" method="POST">
                    <input type="text" name="name" placeholder="Full Name" class="form-input" required>
                    <input type="email" name="email" placeholder="Email Address" class="form-input" required>
                    <input type="text" name="company" placeholder="Company Name (Optional)" class="form-input">
                    <textarea name="message" placeholder="Specific requirements or questions..." class="form-input" style="height: 120px;"></textarea>
                    
                    <input type="hidden" name="estimated_monthly" id="hidden_monthly" value="₱0">
                    <input type="hidden" name="estimated_setup" id="hidden_setup" value="₱0">
                    <input type="hidden" name="estimated_total" id="hidden_total" value="₱0">
                    
                    <button type="submit" style="width: 100%; background: #011F3F; color: white; border: none; padding: 20px; font-weight: 900; text-transform: uppercase; letter-spacing: 2px; cursor: pointer;">
                        Submit Request
                    </button>
                </form>
            </div>
        </div>

        <div class="calculator-side">
            <div class="sticky-card">
                <p style="color: #C5A059; font-size: 10px; font-weight: bold; letter-spacing: 3px; text-transform: uppercase; margin-bottom: 25px;">Live Estimate</p>
                
                <div style="display: flex; justify-content: space-between; margin-bottom: 12px; opacity: 0.5; font-size: 12px; text-transform: uppercase;">
                    <span>Monthly Retainer</span>
                    <span id="out_monthly">₱0</span>
                </div>
                
                <div style="display: flex; justify-content: space-between; margin-bottom: 30px; opacity: 0.5; font-size: 12px; text-transform: uppercase;">
                    <span>Setup/Annual Fees</span>
                    <span id="out_setup">₱0</span>
                </div>

                <div style="border-top: 1px solid rgba(255,255,255,0.1); padding-top: 25px;">
                    <p style="font-size: 10px; color: #C5A059; font-weight: bold; text-transform: uppercase;">Estimated Total</p>
                    <div id="out_total" class="price-large">₱0</div>
                </div>
                
                <p style="font-size: 11px; opacity: 0.6; line-height: 1.4; margin-top: 20px;">
                    Use the form on the left to lock in this estimate and receive a formal proposal via email.
                </p>
            </div>
        </div>
    </div>
</div>

<script>
    function calculateQuote() {
        const vo = parseInt(document.getElementById('vo_choice').value) || 0;
        const bookkeeping = parseInt(document.getElementById('bookkeeping_choice').value) || 0;
        const ete = parseInt(document.getElementById('ete_choice').value) || 0;
        const monthly = vo + bookkeeping + ete;

        const afs = parseInt(document.getElementById('afs_choice').value) || 0;
        
        // Setup logic
        const setup = afs; 

        // Update UI
        const monthlyStr = '₱' + monthly.toLocaleString();
        const setupStr = '₱' + setup.toLocaleString();
        const totalStr = '₱' + (monthly + setup).toLocaleString();

        document.getElementById('out_monthly').innerText = monthlyStr;
        document.getElementById('out_setup').innerText = setupStr;
        document.getElementById('out_total').innerText = totalStr;

        // Update Hidden Form Fields
        document.getElementById('hidden_monthly').value = monthlyStr;
        document.getElementById('hidden_setup').value = setupStr;
        document.getElementById('hidden_total').value = totalStr;
    }
    window.onload = calculateQuote;
</script>