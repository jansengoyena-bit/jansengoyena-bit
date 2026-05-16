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

    <div style="max-width: 650px; margin: 0 auto; padding: 40px 24px 0 24px; text-align: left;">
      
        <h3 style="color: #011F3F; font-family: serif; font-size: 1rem; margin: 0 0 10px 0; font-weight: bold; text-transform: uppercase; letter-spacing: 0.5px;">
            Espacio Manila Service Quote
        </h3>
       
    </div>

    <div style="max-width: 650px; margin: 0 auto; padding: 40px 24px 60px 24px;">
        
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

        <div class="input-box" style="margin-bottom: 30px;">
            <span class="label-meta">Service Tier / Scope</span>
            <select id="bookkeeping_choice" onchange="calculateQuote()" class="dropdown-ui">
                <option value="0">Please select a main category first</option>
            </select>
        </div>

        <div style="background: #011F3F; color: white; padding: 25px 35px; border-radius: 4px; border-left: 5px solid #C5A059; display: flex; justify-content: space-between; align-items: center; margin-bottom: 50px; box-shadow: 0 10px 30px rgba(1, 31, 63, 0.15);">
            <div>
                <p style="font-size: 10px; color: #C5A059; font-weight: bold; text-transform: uppercase; letter-spacing: 1px; margin: 0;">Estimated Total</p>
            </div>
            <div>
                <div id="out_total" style="font-size: 2.5rem; color: #C5A059; font-family: serif; font-weight: bold;">₱0</div>
            </div>
        </div>

        <div style="margin-top: 40px;">
            <span class="label-meta">Secure Your Quotation</span>
            <h2 style="font-family: serif; font-size: 2rem; margin-top: 5px; margin-bottom: 25px; color: #011F3F;">Get a Price Quote</h2>
            
            <form action="https://formspree.io/f/your-id" method="POST">
                <input type="text" name="name" placeholder="Full Name" class="form-input" required>
                <input type="email" name="email" placeholder="Email Address" class="form-input" required>
                <input type="text" name="company" placeholder="Company Name (Optional)" class="form-input">
                <textarea name="message" placeholder="Specific requirements or questions..." class="form-input" style="height: 120px;"></textarea>
                
                <input type="hidden" name="estimated_total" id="hidden_total" value="₱0">
                
                <button type="submit" style="width: 100%; background: #011F3F; color: white; border: none; padding: 20px; font-weight: 900; text-transform: uppercase; letter-spacing: 2px; cursor: pointer; transition: background 0.3s;" onmouseover="this.style.background='#C5A059'" onmouseout="this.style.background='#011F3F'">
                    Submit Request
                </button>
            </form>
        </div>

        <div style="margin-top: 40px; padding-top: 20px; border-top: 1px solid rgba(1, 31, 63, 0.1);">
            <p style="font-family: 'Inter', -apple-system, sans-serif; font-size: 11px; line-height: 1.6; color: #011F3F; opacity: 0.5; font-style: italic; text-align: justify; margin: 0;">
                <strong>Disclaimer:</strong> The rates listed are starting rates and may vary depending on the complexity and scope of the project. Final pricing will be determined after assessing the specific requirements and details of your project. Additional charges may apply for specialized services, revisions, or unforeseen factors. Please contact us for a detailed quote tailored to your needs.
            </p>
        </div>

    </div>
</div>

<script>
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
            { text: "BIR Closure + Notarial/Transport", price: 10000 + 2000 },
            { text: "BIR Computerized Accounting Software Accreditation", price: 50000 },
            { text: "BIR Registration Amendment", price: 5000 },
            { text: "BIR Registration (Notarial + Transport)", price: 8500 },
            { text: "BIR Registration NON VAT to VAT (Notarial + Transport)", price: 8500 },
            { text: "BIR Registration Renewal (Notarial + Transport)", price: 0 },
            { text: "BIR Registration (New, Renewal, Updating) + Notarial/Transport", price: 0 },
            { text: "BIR Updating/Amendment of Line of Business", price: 0 },
            { text: "BMBE Registration - Renewal", price: 0 },
            { text: "Books of Accounts Registration", price: 0 },
            { text: "BPLO Change of Address", price: 0 },
            { text: "Business Permit Amendment", price: 0 },
            { text: "Business Permit Closure", price: 0 },
            { text: "Business Permit Closure + Notarial/Transport", price: 0 },
            { text: "Business Permit - New/Renewal (Notarial + Transport)", price: 0 },
            { text: "Business Permit Registration (New, Renewal, Updating) + Notarial/Transport", price: 0 },
            { text: "Closing of BIR Open Cases per Tax Return", price: 0 },
            { text: "Company Valuation", price: 0 },
            { text: "Copyright Registration", price: 0 },
            { text: "Corporate Secretarial Services", price: 0 },
            { text: "DTI Change of Business Address", price: 0 },
            { text: "DTI Change of Territorial Scope", price: 0 },
            { text: "DTI Closure", price: 0 },
            { text: "DTI Closure + Notarial/Transport", price: 0 },
            { text: "DTI Registration", price: 0 },
            { text: "eFAST Account", price: 0 },
            { text: "eFPS Registration", price: 0 },
            { text: "ESales Registration", price: 0 },
            { text: "ESecure (1 - 5 Incorporators)", price: 0 },
            { text: "ESecure (6 - 10 Incorporators)", price: 0 },
            { text: "ESecure (11 - 15 Incorporators)", price: 0 },
            { text: "FDA CPR", price: 0 },
            { text: "FDA Certificate of Product Notification", price: 0 },
            { text: "FDA LTO", price: 0 },
            { text: "FDA LTO Renewal", price: 0 },
            { text: "Filing of Form of Appointment for OPC (FAO)", price: 0 },
            { text: "GIS", price: 0 },
            { text: "HALAL Certification", price: 0 },
            { text: "Income Payee's Sworn Declaration of Gross Sales", price: 0 },
            { text: "Leasing Information Sheet Preparation", price: 0 },
            { text: "Legal Retainer", price: 0 },
            { text: "LGU Updating of Line of Business", price: 0 },
            { text: "Lifting of Suspended SEC registration", price: 0 },
            { text: "Looseleaf Permit Application", price: 0 },
            { text: "Memorandum Circular No. 28 (MC 28)", price: 0 },
            { text: "Nominee Director Services", price: 0 },
            { text: "Pag-IBIG Employer Registration", price: 0 },
            { text: "Patent Registration", price: 0 },
            { text: "Payroll Management (Per Employee, Per Month)", price: 0 },
            { text: "PCAB Registration (A/AA/AAA/AAAA)", price: 0 },
            { text: "PCAB Registration (B, C)", price: 0 },
            { text: "PCAB Registration (D)", price: 0 },
            { text: "PCAB Registration (E)", price: 0 },
            { text: "PCAB Pakyaw", price: 0 },
            { text: "Permit to Use Application for POS", price: 0 },
            { text: "PEZA Registration", price: 0 },
            { text: "PHILGEPS Platinum Membership", price: 0 },
            { text: "PHILGEPS Red Membership", price: 0 },
            { text: "PhilHealth Employer Registration", price: 0 },
            { text: "POS Registration", price: 0 },
            { text: "Processing of BIR from NON-VAT to VAT Registration (Notarial/Transport)", price: 0 },
            { text: "Processing of Certificate of Registration (BIR 2303)", price: 0 },
            { text: "Professional Tax Receipt / Occupational Tax Receipt", price: 0 },
            { text: "RDO Transfer", price: 0 },
            { text: "Resident Agent Services", price: 0 },
            { text: "SEC Amendment (Change of Address)", price: 0 },
            { text: "SEC Amendment (Change of Fiscal Year)", price: 0 },
            { text: "SEC Amendment (Change of Tradename)", price: 0 },
            { text: "SEC Amendment (Change of Treasurer)", price: 0 },
            { text: "SEC Amendment (Increase of Capital Share)", price: 0 },
            { text: "SEC Amendment Update of Purpose", price: 0 },
            { text: "SEC Assessment of Open Cases", price: 0 },
            { text: "SEC assistance filing AFS, ITR and GIS", price: 0 },
            { text: "SEC Closure + Notarial/Transport", price: 0 },
            { text: "SEC Registration", price: 0 },
            { text: "Secretary's Certificate", price: 0 },
            { text: "SSS Employer Registration", price: 0 },
            { text: "SSS, Pag-IBIG, PhilHealth Closure", price: 0 },
            { text: "Submission of Inventory List", price: 0 },
            { text: "Sworn Declaration + Notarial/Transport", price: 0 },
            { text: "Tax Audit Assistance - LOA (Letter of Authority) + 1%", price: 0 },
            { text: "Tax Clearance for Biding + Notarial/Transport", price: 0 },
            { text: "Tax Clearance for Verification + Notarial/Transport", price: 0 },
            { text: "Tax Clearance + Notarial/Transport", price: 0 },
            { text: "Tax Exemption Services", price: 0 },
            { text: "Tax Return Amendment (Per Tax Return)", price: 0 },
            { text: "TIN ID / TIN Preparation (Notarial + Transport)", price: 0 },
            { text: "TIN Update Information", price: 0 },
            { text: "Trademark Registration", price: 0 },
            { text: "Transfer of stocks/shares per Transaction/Change of Incorporators", price: 0 },
            { text: "Treasurer Services", price: 0 },
            { text: "Virtual Office Subscription + Notarial Registration", price: 0 },
            { text: "CPA BOA Accreditation Processing Fee", price: 0 }
        ],
        "AFS": [
            { text: "No Operations", price: 3500 },
            { text: "Php 0 - 5M Gross Sales/Assets/Expenses", price: 15000 },
            { text: "Php 5M - 10M Gross Sales/Assets/Expenses", price: 25000 },
            { text: "Php 10M – 20M Gross Sales/Assets/Expenses", price: 35000 },
            { text: "Php 20M – 30M Gross Sales/Assets/Expenses", price: 50000 },
            { text: "Php 30M – 40M Gross Sales/Assets/Expenses", price: 0 },
            { text: "Php 40M – 50M Gross Sales/Assets/Expenses", price: 0 },
            { text: "Php 50M – 60M Gross Sales/Assets/Expenses", price: 0 },
            { text: "Php 60M – 70M Gross Sales/Assets/Expenses", price: 0 },
            { text: "Php 70M – 80M Gross Sales/Assets/Expenses", price: 0 },
            { text: "Php 80M – 90M Gross Sales/Assets/Expenses", price: 0 },
            { text: "Php 90M – 100M Gross Sales/Assets/Expenses", price: 0 }
        ],
        "BOOKKEEPING_TAX": [
        { "text": "NON-VAT less than 1M Gross Sales/Revenues", "price": 0 },
        { "text": "NON-VAT Php 1M - 2M Gross Sales/Revenue", "price": 0 },
        { "text": "NON-VAT Php 2M - 3M Gross Sales/Revenues", "price": 0 },
        { "text": "Php 3M to 10M Gross Sales/Revenues", "price": 0 },
        { "text": "Php 10M – 20M Gross Sales/Revenues", "price": 0 },
        { "text": "Php 20M – 30M Gross Sales/Revenues", "price": 0 },
        { "text": "Php 30M – 40M Gross Sales/Revenues", "price": 0 },
        { "text": "Php 40M – 50M Gross Sales/Revenues", "price": 0 },
        { "text": "Php 50M – 60M Gross Sales/Revenues", "price": 0 },
        { "text": "Php 60M – 70M Gross Sales/Revenues", "price": 0 },
        { "text": "Php 70M – 80M Gross Sales/Revenues", "price": 0 },
        { "text": "Php 80M – 90M Gross Sales/Revenues", "price": 0 },
        { "text": "Php 100M & Above Gross Sales/Revenue", "price": 0 }
        ],
        "END_TO_END": [
        { "text": "NON-VAT less than 1M Gross Sales/Revenues", "price": 0 },
        { "text": "NON-VAT Php 1M - 2M Gross Sales/Revenues", "price": 0 },
        { "text": "NON-VAT Php 2M - 3M Gross Sales/Revenues", "price": 0 },
        { "text": "Php 3M - 5M Gross Sales/Revenues", "price": 0 },
        { "text": "Php 5M - 10M Gross Sales/Revenues", "price": 0 },
        { "text": "Php 10M – 20M Gross Sales/Revenues", "price": 0 },
        { "text": "Php 20M – 30M Gross Sales/Revenues", "price": 0 },
        { "text": "Php 30M – 40M Gross Sales/Revenues", "price": 0 },
        { "text": "Php 40M – 50M Gross Sales/Revenues", "price": 0 },
        { "text": "Php 50M – 60M Gross Sales/Revenues", "price": 0 },
        { "text": "Php 60M – 70M Gross Sales/Revenues", "price": 0 },
        { "text": "Php 70M – 80M Gross Sales/Revenues", "price": 0 },
        { "text": "Php 80M – 90M Gross Sales/Revenues", "price": 0 }
        ]
    };

    function updateSubServices() {
        const parentSelect = document.getElementById('vo_choice');
        const childSelect = document.getElementById('bookkeeping_choice');
        const selectedCategory = parentSelect.value;

        childSelect.innerHTML = '';

        if (!selectedCategory || !serviceData[selectedCategory]) {
            childSelect.innerHTML = '<option value="0">Please select a main category first</option>';
            calculateQuote();
            return;
        }

        serviceData[selectedCategory].forEach((service) => {
            const option = document.createElement('option');
            option.value = service.price;
            option.text = `${service.text} (+₱${service.price.toLocaleString()})`;
            childSelect.appendChild(option);
        });

        calculateQuote();
    }

    function calculateQuote() {
        const childSelect = document.getElementById('bookkeeping_choice');
        const selectedOption = childSelect.options[childSelect.selectedIndex];

        let total = 0;

        if (selectedOption && selectedOption.value !== "0") {
            total = parseInt(selectedOption.value) || 0;
        }

        const totalStr = '₱' + total.toLocaleString();

        // Update UI Text
        document.getElementById('out_total').innerText = totalStr;

        // Update Hidden Form Field for submission
        document.getElementById('hidden_total').value = totalStr;
    }

    window.onload = function() {
        updateSubServices();
    };
</script>