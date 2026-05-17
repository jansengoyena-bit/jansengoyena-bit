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

    .input-box { margin-bottom: 30px; }
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

    /* Multi-Quote Cart UI Additions */
    .cart-item {
        display: flex;
        justify-content: space-between;
        align-items: center;
        background: rgba(1, 31, 63, 0.03);
        border: 1px solid rgba(1, 31, 63, 0.08);
        padding: 14px 16px;
        border-radius: 4px;
        margin-bottom: 10px;
        font-size: 13px;
        animation: fadeIn 0.3s ease-out forwards;
    }
    .cart-item button {
        background: none;
        border: none;
        color: #dc3545;
        cursor: pointer;
        font-weight: bold;
        font-size: 18px;
        padding: 0 5px;
        transition: transform 0.2s;
    }
    .cart-item button:hover {
        transform: scale(1.2);
    }
    .btn-gold {
        background: #C5A059;
        color: white;
        border: none;
        padding: 16px;
        width: 100%;
        font-weight: 700;
        text-transform: uppercase;
        letter-spacing: 2px;
        cursor: pointer;
        transition: background 0.3s, transform 0.1s;
        font-size: 11px;
        margin-bottom: 35px;
    }
    .btn-gold:hover {
        background: #011F3F;
    }
    .btn-gold:active {
        transform: scale(0.99);
    }

    /* Success state transition animation */
    .animate-fade-in {
        animation: fadeIn 0.6s ease-out forwards;
    }
    @keyframes fadeIn {
        from { opacity: 0; transform: translateY(10px); }
        to { opacity: 1; transform: translateY(0); }
    }

    @media (max-width: 1024px) {
        .calculator-side { flex: 1; width: 100%; }
        .sticky-card { position: relative; top: 0; }
    }

    .premium-preview-box {
        height: 140px; 
        margin: 0; 
        background-color: rgba(1, 31, 63, 0.02); 
        color: rgba(1, 31, 63, 0.65); 
        border: 1px dashed rgba(1, 31, 63, 0.2); 
        font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif; 
        font-size: 10px;          
        letter-spacing: 0.5px;   
        line-height: 1.7;        
        padding: 14px;
        overflow-y: auto;
        white-space: pre-wrap;
        cursor: default;
        border-radius: 4px;
    }

    /* Process Flow Styles for Onboarding Steps */
    .onboarding-steps {
        max-width: 480px;
        margin: 35px auto;
        text-align: left;
    }
    .step-item {
        display: flex;
        align-items: flex-start;
        gap: 16px;
        padding: 16px 0;
        border-bottom: 1px dashed rgba(1, 31, 63, 0.08);
    }
    .step-item:last-child {
        border-bottom: none;
    }
    .step-badge {
        background: #011F3F;
        color: #C5A059;
        font-size: 11px;
        font-weight: bold;
        width: 24px;
        height: 24px;
        display: flex;
        align-items: center;
        justify-content: center;
        border-radius: 50%;
        flex-shrink: 0;
        margin-top: 1px;
    }
    .step-text {
        font-size: 13px;
        color: #011F3F;
        line-height: 1.5;
        font-weight: 400;
    }
</style>

<div id="espacio-nexus">

    <div style="max-width: 650px; margin: 0 auto; padding: 40px 24px 0 24px; text-align: left;">
        <h3 style="color: #011F3F; font-family: serif; font-size: 1rem; margin: 0 0 10px 0; font-weight: bold; text-transform: uppercase; letter-spacing: 0.5px;">
            Espacio Manila Service Quote
        </h3>
    </div>

    <div style="max-width: 650px; margin: 0 auto; padding: 40px 24px 60px 24px;">
        
        <div id="calculator-workflow">
            <div class="input-box">
                <span class="label-meta">Services Offered</span>
                <select id="vo_choice" onchange="updateSubServices()" class="dropdown-ui">
                    <option value="">-- SELECT A CATEGORY --</option>
                    <option value="ACCOUNTING_SYS">COMPLIANCE SERVICES</option>
                    <option value="AFS">AUDITED FINANCIAL STATEMENTS PRICING</option>
                    <option value="BOOKKEEPING_TAX">BOOKKEEPING AND TAX FILING PRICING</option>
                    <option value="END_TO_END">END TO END ACCOUNTING SERVICES</option>
                </select>
            </div>

            <div class="input-box" style="margin-bottom: 20px;">
                <span class="label-meta">Service Tier / Scope</span>
                <select id="bookkeeping_choice" class="dropdown-ui">
                    <option value="placeholder_fallback">Please select a main category first</option>
                </select>
            </div>

            <button type="button" onclick="addItemToQuote()" class="btn-gold">
                + Add Selection to Quote List
            </button>

            <div id="quote-summary-area" style="margin-bottom: 35px; display: none;">
                <span class="label-meta">Your Selected Quotation Bundle</span>
                <div id="cart-items-container"></div>
            </div>

            <div style="background: #011F3F; color: white; padding: 25px 35px; border-radius: 4px; border-left: 5px solid #C5A059; display: flex; justify-content: space-between; align-items: center; margin-bottom: 50px; box-shadow: 0 10px 30px rgba(1, 31, 63, 0.15);">
                <div>
                    <p style="font-size: 10px; color: #C5A059; font-weight: bold; text-transform: uppercase; letter-spacing: 1px; margin: 0;">Combined Estimated Total</p>
                </div>
                <div>
                    <div id="out_total" style="font-size: 2.5rem; color: #C5A059; font-family: serif; font-weight: bold;">₱0</div>
                </div>
            </div>

            <div style="margin-top: 40px;">
                <span class="label-meta">Secure Your Quotation</span>
                <h2 style="font-family: serif; font-size: 2rem; margin-top: 5px; margin-bottom: 25px; color: #011F3F;">Get a Price Quote</h2>
                
                <form id="nexus-quote-form" style="display: flex; flex-direction: column; gap: 15px;">
                    <div style="display: flex; gap: 15px;">
                        <input type="text" name="entry.440124246" placeholder="First Name" class="form-input" style="flex: 1; margin: 0;" required>
                        <input type="text" name="entry.1440295803" placeholder="Last Name" class="form-input" style="flex: 1; margin: 0;" required>
                    </div>
                    
                    <input type="email" name="entry.1510499110" placeholder="Business Email Address" class="form-input" style="margin: 0;" required>
                    <input type="tel" name="entry.84122293" placeholder="Contact Number (+63 XXX XXX XXXX)" class="form-input" style="margin: 0;">
                    
                    <span class="label-meta" style="margin-top: 10px;">Specific Requirements or Notes</span>
                    <textarea id="user_custom_notes" placeholder="Tell us more about your business needs, custom requests, or timeline milestones here..." class="form-input" style="height: 120px; margin: 0;"></textarea>

                    <span class="label-meta" style="margin-top: 10px;">Selected Services Preview</span>
                    <div id="hidden_notes_compiled" class="premium-preview-box">Your selected bundle layout will appear here automatically...</div>
                    
                    <input type="hidden" name="entry.386645384" id="form_payload_services">
                    <input type="hidden" name="entry.153965477" id="form_payload_notes">
                    <input type="hidden" name="entry.1247618226" id="hidden_total" value="₱0">
                    <input type="hidden" name="entry.1885822597" id="hidden_category" value="Multi-Quote Bundle">
                    
                    <button type="submit" id="submit-btn" style="width: 100%; background: #011F3F; color: white; border: none; padding: 20px; font-weight: 900; text-transform: uppercase; letter-spacing: 2px; cursor: pointer; transition: background 0.3s; margin-top: 15px;" onmouseover="this.style.background='#C5A059'" onmouseout="this.style.background='#011F3F'">
                        <span id="btn-text">Submit Bundle Request</span>
                    </button>
                </form>
            </div>
        </div>

        <div id="success-notification" style="display: none; padding: 40px 10px; text-align: center;" class="animate-fade-in">
            <div style="color: #C5A059; font-size: 40px; margin-bottom: 20px;"><i class="fa-solid fa-circle-check"></i></div>
            <h2 style="font-family: serif; font-size: 1.8rem; color: #011F3F; margin-bottom: 12px; line-height: 1.3; max-width: 550px; margin-left: auto; margin-right: auto;">
                We already accept your inquiry/quotation request. We will respond to you shortly.
            </h2>
            
            <div class="onboarding-steps">
                <span class="label-meta" style="margin-bottom: 20px; text-align: center;">Next Execution Steps</span>
                
                <div class="step-item">
                    <div class="step-badge">1</div>
                    <div class="step-text">Our sales representative will contact you to discuss your needs.</div>
                </div>
                <div class="step-item">
                    <div class="step-badge">2</div>
                    <div class="step-text">Send final quotation for signature.</div>
                </div>
                <div class="step-item">
                    <div class="step-badge">3</div>
                    <div class="step-text">Pay the downpayment.</div>
                </div>
                <div class="step-item">
                    <div class="step-badge">4</div>
                    <div class="step-text">Start the engagement.</div>
                </div>
            </div>

            <button onclick="location.reload()" style="background: none; border: none; border-bottom: 1px solid #C5A059; color: #C5A059; font-size: 10px; letter-spacing: 2px; text-transform: uppercase; cursor: pointer; padding-bottom: 4px; margin-top: 20px;">
                Calculate another scope
            </button>
        </div>

        <div style="margin-top: 40px; padding-top: 20px; border-top: 1px solid rgba(1, 31, 63, 0.1);">
            <p style="font-family: 'Inter', -apple-system, sans-serif; font-size: 11px; line-height: 1.6; color: #011F3F; opacity: 0.5; font-style: italic; text-align: justify; margin: 0;">
                <strong>Disclaimer:</strong> The rates listed are starting rates and may vary depending on the complexity and scope of the project. Final pricing will be determined after assessing the specific requirements and details of your project. Additional charges may apply for specialized services, revisions, or unforeseen factors. Please contact us for a detailed quote tailored to your needs.
            </p>
        </div>

    </div>
</div>

<script>
    const GOOGLE_FORM_ACTION = "https://docs.google.com/forms/d/e/1FAIpQLScNHfbmuT9fKoUltEznVK9KaoPfTNUZ7hSC4ZuSyVbeHaAPbQ/formResponse";
    const serviceData = {
        "ACCOUNTING_SYS": [
            { text: "Accounting System Implementation Support", price: 50000 },
            { text: "Annual Inventory List", price: 5000 },
            { text: "Annual ITR Preparation - NON-VAT", price: 3000 },
            { text: "Annual ITR Preparation - VAT", price: 5000 },
            { text: "Assessment of BIR Open Cases (includes SPA, Notarial, Transport)", price: 5000 },
            { text: "Authority to Print", price: 5000 },
            { text: "BIR 2316 (per employee)", price: 1000 },
            { text: "BMBE Registration", price: 7000 },
            { text: "BIR Change of Address/RDO Transfer", price: 10000 },
            { text: "BIR Change of Name and Address", price: 10000 },
            { text: "BIR Change of Tradename", price: 5000 },
            { text: "BIR Closure", price: 10000 },
            { text: "BIR Closure + Notarial/Transport", price: 12000, breakdown: "₱12,000" },
            { text: "BIR Computerized Accounting Software Accreditation", price: 50000 },
            { text: "BIR Registration Amendment", price: 5000 },
            { text: "BIR Registration (Notarial + Transport)", price: 8500 },
            { text: "BIR Registration NON VAT to VAT (Notarial + Transport)", price: 8500 },
            { text: "BIR Registration Renewal (Notarial + Transport)", price: 8500 },
            { text: "BIR Registration (New, Renewal, Updating) + Notarial/Transport", price: 8500 },
            { text: "BIR Updating/Amendment of Line of Business", price: 7000 },
            { text: "BMBE Registration - Renewal", price: 7000 },
            { text: "Books of Accounts Registration", price: 5000 },
            { text: "BPLO Change of Address", price: 1000 },
            { text: "Business Permit Amendment", price: 5000 },
            { text: "Business Permit Closure", price: 1000 },
            { text: "Business Permit Closure + Notarial/Transport", price: 12000, breakdown: "₱10,000 + ₱2,000" },
            { text: "Business Permit - New/Renewal (Notarial + Transport)", price: 12000, breakdown: "₱10,000 + ₱2,000" },
            { text: "Business Permit Registration (New, Renewal, Updating) + Notarial/Transport", price: 8500, breakdown: "₱7,000 + ₱1,500" },
            { text: "Closing of BIR Open Cases per Tax Return", price: 500 },
            { text: "Company Valuation", price: 150000 },
            { text: "Copyright Registration", price: 50000 },
            { text: "Corporate Secretarial Services", price: 7000 },
            { text: "DTI Change of Business Address", price: 5000 },
            { text: "DTI Change of Territorial Scope", price: 5000 },
            { text: "DTI Closure", price: 10000 },
            { text: "DTI Closure + Notarial/Transport", price: 12000, breakdown: "₱10,000 + ₱2,000" },
            { text: "DTI Registration", price: 1500 },
            { text: "eFAST Account", price: 10000 },
            { text: "eFPS Registration", price: 5000 },
            { text: "ESales Registration", price: 20000 },
            { text: "ESecure (1 - 5 Incorporators)", price: 5000 },
            { text: "ESecure (6 - 10 Incorporators)", price: 8000 },
            { text: "ESecure (11 - 15 Incorporators)", price: 10000 },
            { text: "FDA CPR", price: 45000 },
            { text: "FDA Certificate of Product Notification", price: 45000 },
            { text: "FDA LTO", price: 60000 },
            { text: "FDA LTO Renewal", price: 60000 },
            { text: "Filing of Form of Appointment for OPC (FAO)", price: 5000 },
            { text: "GIS", price: 5000 },
            { text: "HALAL Certification", price: 35000 },
            { text: "Income Payee's Sworn Declaration of Gross Sales", price: 5000 },
            { text: "Leasing Information Sheet Preparation", price: 5000 },
            { text: "Legal Retainer", price: 10000 },
            { text: "LGU Updating of Line of Business", price: 7000 },
            { text: "Lifting of Suspended SEC registration", price: 20000 },
            { text: "Looseleaf Permit Application", price: 5000 },
            { text: "Memorandum Circular No. 28 (MC 28)", price: 10000 },
            { text: "Nominee Director Services", price: 10000 },
            { text: "Pag-IBIG Employer Registration", price: 7000 },
            { text: "Patent Registration", price: 50000 },
            { text: "Payroll Management (Per Employee, Per Month)", price: 1500 },
            { text: "PCAB Registration (A/AA/AAA/AAAA)", price: 35000 },
            { text: "PCAB Registration (B, C)", price: 35000 },
            { text: "PCAB Registration (D)", price: 25000 },
            { text: "PCAB Registration (E)", price: 20000 },
            { text: "PCAB Pakyaw", price: 15000 },
            { text: "Permit to Use Application for POS", price: 20000 },
            { text: "PEZA Registration", price: 100000 },
            { text: "PHILGEPS Platinum Membership", price: 10000 },
            { text: "PHILGEPS Red Membership", price: 5000 },
            { text: "PhilHealth Employer Registration", price: 7000 },
            { text: "POS Registration", price: 10000 },
            { text: "Processing of BIR from NON-VAT to VAT Registration (Notarial/Transport)", price: 8500 },
            { text: "Processing of Certificate of Registration (BIR 2303)", price: 3000 },
            { text: "Professional Tax Receipt / Occupational Tax Receipt", price: 3500 },
            { text: "RDO Transfer", price: 10000 },
            { text: "Resident Agent Services", price: 10000 },
            { text: "SEC Amendment (Change of Address)", price: 20000 },
            { text: "SEC Amendment (Change of Fiscal Year)", price: 20000 },
            { text: "SEC Amendment (Change of Tradename)", price: 20000 },
            { text: "SEC Amendment (Change of Treasurer)", price: 20000 },
            { text: "SEC Amendment (Increase of Capital Share)", price: 50000 },
            { text: "SEC Amendment Update of Purpose", price: 20000 },
            { text: "SEC Assessment of Open Cases", price: 5000 },
            { text: "SEC assistance filing AFS, ITR and GIS", price: 5000 },
            { text: "SEC Closure + Notarial/Transport", price: 27000, breakdown: "₱25,000 + ₱2,000" },
            { text: "SEC Registration", price: 10000 },
            { text: "Secretary's Certificate", price: 3000 },
            { text: "SSS Employer Registration", price: 7000 },
            { text: "SSS, Pag-IBIG, PhilHealth Closure", price: 25000 },
            { text: "Submission of Inventory List", price: 5000 },
            { text: "Sworn Declaration + Notarial/Transport", price: 6500 },
            { text: "Tax Audit Assistance - LOA (Letter of Authority) + 1%", price: 100000 },
            { text: "Tax Clearance for Biding + Notarial/Transport", price: 7000, breakdown: "₱5,000 + ₱2,000" },
            { text: "Tax Clearance for Verification + Notarial/Transport", price: 7000, breakdown: "₱5,000 + ₱2,000" },
            { text: "Tax Clearance + Notarial/Transport", price: 7000, breakdown: "₱5,000 + ₱2,000" },
            { text: "Tax Exemption Services", price: 10000 },
            { text: "Tax Return Amendment (Per Tax Return)", price: 2000 },
            { text: "TIN ID / TIN Preparation (Notarial + Transport)", price: 4500 },
            { text: "TIN Update Information", price: 3000 },
            { text: "Trademark Registration", price: 30000 },
            { text: "Transfer of stocks/shares per Transaction/Change of Incorporators", price: 30000 },
            { text: "Treasurer Services", price: 10000 },
            { text: "Virtual Office Subscription + Notarial Registration", price: 7000, breakdown: "₱5,000 + ₱2,000" },
            { text: "CPA BOA Accreditation Processing Fee", price: 100000 }
        ],
        "AFS": [
            { text: "No Operations", price: 3500 },
            { text: "Php 0 - 5M Gross Sales/Assets/Expenses", price: 10000 },
            { text: "Php 5M - 10M Gross Sales/Assets/Expenses", price: 15000 },
            { text: "Php 10M – 20M Gross Sales/Assets/Expenses", price: 20000 },
            { text: "Php 20M – 30M Gross Sales/Assets/Expenses", price: 30000 },
            { text: "Php 30M – 40M Gross Sales/Assets/Expenses", price: 50000 },
            { text: "Php 40M – 50M Gross Sales/Assets/Expenses", price: 60000 },
            { text: "Php 50M – 60M Gross Sales/Assets/Expenses", price: 70000 },
            { text: "Php 60M – 70M Gross Sales/Assets/Expenses", price: 80000 },
            { text: "Php 70M – 80M Gross Sales/Assets/Expenses", price: 90000 },
            { text: "Php 80M – 90M Gross Sales/Assets/Expenses", price: 100000 },
            { text: "Php 90M – 100M Gross Sales/Assets/Expenses", price: 110000 }
        ],
        "BOOKKEEPING_TAX": [
            { "text": "NON-VAT less than 1M Gross Sales/Revenues", "price": 1500 },
            { "text": "NON-VAT Php 1M - 2M Gross Sales/Revenue", "price": 3000 },
            { "text": "NON-VAT Php 2M - 3M Gross Sales/Revenues", "price": 5000 },
            { "text": "Php 3M to 10M Gross Sales/Revenues", "price": 6000 },
            { "text": "Php 10M – 20M Gross Sales/Revenues", "price": 8500 },
            { "text": "Php 20M – 30M Gross Sales/Revenues", "price": 11000 },
            { "text": "Php 30M – 40M Gross Sales/Revenues", "price": 13500 },
            { "text": "Php 40M – 50M Gross Sales/Revenues", "price": 16000 },
            { "text": "Php 50M – 60M Gross Sales/Revenues", "price": 18500 },
            { "text": "Php 60M – 70M Gross Sales/Revenues", "price": 21000 },
            { "text": "Php 70M – 80M Gross Sales/Revenues", "price": 23000 },
            { "text": "Php 80M – 90M Gross Sales/Revenues", "price": 26000 },
            { "text": "Php 100M & Above Gross Sales/Revenue", "price": 30000 }
        ],
        "END_TO_END": [
            { "text": "NON-VAT less than 1M Gross Sales/Revenues", "price": 3500 },
            { "text": "NON-VAT Php 1M - 2M Gross Sales/Revenues", "price": 5000 },
            { "text": "NON-VAT Php 2M - 3M Gross Sales/Revenues", "price": 7000 },
            { "text": "Php 3M - 5M Gross Sales/Revenues", "price": 8000 },
            { "text": "Php 5M - 10M Gross Sales/Revenues", "price": 9000 },
            { "text": "Php 10M – 20M Gross Sales/Revenues", "price": 10500 },
            { "text": "Php 20M – 30M Gross Sales/Revenues", "price": 13000 },
            { "text": "Php 30M – 40M Gross Sales/Revenues", "price": 15500 },
            { "text": "Php 40M – 50M Gross Sales/Revenues", "price": 18000 },
            { "text": "Php 50M – 60M Gross Sales/Revenues", "price": 20500 },
            { "text": "Php 60M – 70M Gross Sales/Revenues", "price": 23000 },
            { "text": "Php 70M – 80M Gross Sales/Revenues", "price": 25500 },
            { "text": "Php 80M – 90M Gross Sales/Revenues", "price": 28000 }
        ]
    };

    let quoteCart = [];

    function updateSubServices() {
        const parentSelect = document.getElementById('vo_choice');
        const childSelect = document.getElementById('bookkeeping_choice');
        const selectedCategory = parentSelect.value;

        childSelect.innerHTML = '';

        if (!selectedCategory || !serviceData[selectedCategory]) {
            childSelect.innerHTML = '<option value="placeholder_fallback">Please select a main category first</option>';
            return;
        }

        serviceData[selectedCategory].forEach((service, index) => {
            const option = document.createElement('option');
            option.value = index;
            
            if (service.breakdown) {
                option.text = `${service.text} (+${service.breakdown})`;
            } else {
                option.text = `${service.text} (+₱${service.price.toLocaleString()})`;
            }
            
            childSelect.appendChild(option);
        });
    }

    function addItemToQuote() {
        const parentSelect = document.getElementById('vo_choice');
        const childSelect = document.getElementById('bookkeeping_choice');
        
        if (!parentSelect.value || childSelect.value === "placeholder_fallback" || childSelect.selectedIndex === -1) {
            alert("Please pick both a Category and a specific Scope before adding.");
            return;
        }

        const categoryKey = parentSelect.value;
        const categoryText = parentSelect.options[parentSelect.selectedIndex].text;
        const itemIndex = parseInt(childSelect.value);
        const selectedItemRaw = serviceData[categoryKey][itemIndex];

        const isDuplicate = quoteCart.some(item => item.text === selectedItemRaw.text && item.category === categoryText);
        if (isDuplicate) {
            alert("This service has already been added to your quotation list.");
            return;
        }

        quoteCart.push({
            category: categoryText,
            text: selectedItemRaw.text,
            price: selectedItemRaw.price
        });

        renderCart();
    }

    function removeItemFromQuote(index) {
        quoteCart.splice(index, 1);
        renderCart();
    }

    function renderCart() {
        const container = document.getElementById('cart-items-container');
        const summaryArea = document.getElementById('quote-summary-area');
        
        container.innerHTML = '';
        
        if (quoteCart.length === 0) {
            summaryArea.style.display = 'none';
            updateTotals(0);
            return;
        }

        summaryArea.style.display = 'block';
        let rollingSum = 0;

        quoteCart.forEach((item, index) => {
            rollingSum += item.price;
            
            const itemRow = document.createElement('div');
            itemRow.className = 'cart-item';
            itemRow.innerHTML = `
                <div>
                    <strong style="color: #C5A059; font-size: 10px; display:block; text-transform: uppercase; letter-spacing: 1px;">${item.category}</strong>
                    <span style="color: #011F3F; font-weight: 500;">${item.text}</span>
                </div>
                <div style="display: flex; align-items: center; gap: 15px;">
                    <span style="font-weight: bold; color: #011F3F;">₱${item.price.toLocaleString()}</span>
                    <button type="button" onclick="removeItemFromQuote(${index})">&times;</button>
                </div>
            `;
            container.appendChild(itemRow);
        });

        updateTotals(rollingSum);
    }

    function updateTotals(totalAmount) {
        const totalStr = '₱' + totalAmount.toLocaleString();
        
        document.getElementById('out_total').innerText = totalStr;
        document.getElementById('hidden_total').value = totalStr;

        if (quoteCart.length > 0) {
            let manifestationString = "=== SELECTED SERVICES BUNDLE ===\n";
            quoteCart.forEach((item, i) => {
                manifestationString += `${i+1}. [${item.category}] ${item.text} - ₱${item.price.toLocaleString()}\n`;
            });
            manifestationString += `\nCombined Estimate: ${totalStr}\n================================`;
            
            document.getElementById('hidden_notes_compiled').innerText = manifestationString;
        } else {
            document.getElementById('hidden_notes_compiled').innerText = "Selected services bundle manifest will automatically compile here...";
        }
    }

    document.getElementById('nexus-quote-form').addEventListener('submit', function(e) {
        e.preventDefault();
        
        if (quoteCart.length === 0) {
            alert("Your quotation bundle is empty. Please add at least one service before submitting.");
            return;
        }
        
        const quoteForm = document.getElementById('nexus-quote-form');
        const submitBtn = document.getElementById('submit-btn');
        const btnText = document.getElementById('btn-text');
        const workflowArea = document.getElementById('calculator-workflow');
        const successNotif = document.getElementById('success-notification');

        btnText.innerText = "Transmitting Bundle...";
        submitBtn.disabled = true;
        submitBtn.style.opacity = "0.7";

        document.getElementById('form_payload_services').value = document.getElementById('hidden_notes_compiled').innerText;
        document.getElementById('form_payload_notes').value = document.getElementById('user_custom_notes').value;

        const formData = new FormData(quoteForm);

        fetch(GOOGLE_FORM_ACTION, {
            method: 'POST',
            mode: 'no-cors',
            body: formData
        })
        .then(() => {
            workflowArea.style.display = 'none';
            successNotif.style.display = 'block';
            successNotif.scrollIntoView({ behavior: 'smooth', block: 'center' });
        })
        .catch(err => {
            console.error(err);
            alert("Transmission error. Please check your connection.");
            btnText.innerText = "Try Again";
            submitBtn.disabled = false;
            submitBtn.style.opacity = "1";
        });
    });

    window.onload = function() {
        updateSubServices();
    };
</script>