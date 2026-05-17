---
layout: page
title: Virtual Office Solutions | Espacio Manila
---

<style>
    /* 1. Core Structural Animations */
    .reveal-up { opacity: 0; transform: translateY(40px); transition: all 1.2s cubic-bezier(0.215, 0.610, 0.355, 1); }
    .reveal-left { opacity: 0; transform: translateX(-40px); transition: all 1.2s cubic-bezier(0.215, 0.610, 0.355, 1); }
    .reveal-right { opacity: 0; transform: translateX(40px); transition: all 1.2s cubic-bezier(0.215, 0.610, 0.355, 1); }
    .active { opacity: 1 !important; transform: translate(0,0) !important; }

    /* 2. Architectural Minimalist Canvas */
    #espacio-virtual-office {
        background-color: #FDFBF7;
        color: #011F3F;
        font-family: 'Inter', sans-serif;
        overflow-x: hidden;
    }
    
    .gold-accent { color: #C5A059 !important; }
    
    /* 3. Pure Text Architecture Carousel Engine */
    .slider-viewport {
        position: relative;
        overflow: hidden;
        width: 100%;
        max-width: 1200px;
        margin: 0 auto;
    }
    .slider-track {
        display: flex;
        transition: transform 0.7s cubic-bezier(0.25, 1, 0.5, 1);
        width: 100%;
    }
    .package-slide-wrapper {
        flex: 0 0 100%;
        width: 100%;
        box-sizing: border-box;
        padding: 0 24px;
    }
    .package-slide {
        background: transparent !important;
        border: none !important;
        box-shadow: none !important;
        padding: 40px 0 !important;
    }

    /* Typographic Hierarchy */
    .package-headline {
        font-size: 32px !important;
        font-weight: 900 !important;
        text-transform: uppercase !important;
        letter-spacing: 0.15em !important;
        margin-bottom: 1.5rem !important;
        line-height: 1.2 !important;
    }
    .package-details-list {
        font-size: 18px !important;
        line-height: 2 !important;
        color: #2D3748 !important;
        font-weight: 300 !important;
    }

    @media (min-width: 768px) {
        .package-headline { font-size: 20px !important; }
        .package-details-list { font-size: 20px !important; }
    }

    /* Carousel Nav Components */
    .slider-dot {
        width: 10px;
        height: 10px;
        border-radius: 50%;
        background-color: rgba(1, 31, 63, 0.15);
        transition: all 0.3s ease;
        border: none;
        padding: 0;
        cursor: pointer;
    }
    .slider-dot.dot-active {
        background-color: #C5A059;
        width: 36px;
        border-radius: 5px;
    }
    .slider-nav-btn {
        background: transparent;
        color: #011F3F;
        border: 1px solid rgba(1, 31, 63, 0.1);
        width: 56px;
        height: 56px;
        display: flex;
        align-items: center;
        justify-content: center;
        cursor: pointer;
        transition: all 0.3s ease;
    }
    .slider-nav-btn:hover {
        background: #011F3F;
        color: white;
        border-color: #011F3F;
    }

    /* 4. Elegant Minimalist FAQ Typography System */
    .faq-trigger {
        width: 100%;
        text-align: left;
        padding: 28px 0;
        background: transparent;
        border: none;
        outline: none;
        display: flex;
        justify-content: space-between;
        align-items: center;
        cursor: pointer;
        font-family: serif;
        font-size: 18px;
        color: #011F3F;
        transition: color 0.3s ease;
    }
    .faq-trigger:hover { color: #C5A059; }
    .faq-icon {
        font-size: 14px;
        font-weight: 300;
        transition: transform 0.4s cubic-bezier(0.22, 1, 0.36, 1);
        color: #C5A059;
    }
    .faq-content {
        max-height: 0;
        overflow: hidden;
        transition: max-height 0.5s cubic-bezier(0.22, 1, 0.36, 1);
    }
    .faq-text {
        padding-bottom: 28px;
        font-size: 15px;
        line-height: 1.8;
        color: #2D3748;
        font-weight: 300;
    }

    /* Office Showcase Layout Rules */
    .office-viewer-frame {
        position: relative;
        width: 100%;
        aspect-ratio: 16 / 10;
        overflow: hidden;
        background-color: #011F3F;
    }
    .office-img-node {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        object-fit: cover;
        opacity: 0;
        transition: opacity 1s cubic-bezier(0.4, 0, 0.2, 1);
    }
    .office-img-node.img-visible {
        opacity: 0.85;
    }

    /* Photo indicator dots with internal tracking states */
    .photo-dots-indicator {
        position: absolute;
        bottom: 16px;
        right: 16px;
        display: flex;
        gap: 6px;
        z-index: 20;
        background: rgba(1, 31, 63, 0.4);
        padding: 6px 10px;
        border-radius: 20px;
        backdrop-filter: blur(4px);
    }
    .photo-dot {
        width: 6px;
        height: 6px;
        border-radius: 50%;
        background: rgba(255, 255, 255, 0.4);
        transition: all 0.3s ease;
    }
    .photo-dot.active-photo-dot {
        background: #C5A059;
        transform: scale(1.25);
    }

    /* Numbered Customer Review Tracker Dots */
    .review-dot-numbered {
        width: 28px;
        height: 28px;
        border-radius: 50%;
        background-color: transparent;
        border: 1px solid rgba(1, 31, 63, 0.15);
        color: #011F3F;
        font-size: 11px;
        font-weight: 600;
        display: flex;
        align-items: center;
        justify-content: center;
        transition: all 0.3s ease;
        cursor: pointer;
    }
    .review-dot-numbered.dot-active {
        background-color: #C5A059;
        border-color: #C5A059;
        color: #011F3F;
        transform: scale(1.1);
    }
</style>

<div id="espacio-virtual-office">

    <section class="relative pt-20 pb-32 lg:min-h-[85vh] flex items-center">
        <div class="max-w-7xl mx-auto px-8 w-full grid grid-cols-1 lg:grid-cols-12 gap-16 items-center">
            
            <div class="lg:col-span-7 reveal-left">
                <span class="text-[10px] uppercase tracking-[0.5em] font-black gold-accent mb-6 block">Strategic Infrastructure</span>
                <h1 class="text-4xl md:text-7xl font-serif font-light leading-[1.1] mb-8 text-[#011F3F]">
                    Virtual Office <br><span class="italic font-normal gold-accent">Frameworks</span>
                </h1>
                <p class="text-[18px] text-[#2D3748] font-light leading-relaxed mb-12 max-w-xl">
                    Establish an immediate corporate footprint in prime business centers. We offer high-tier corporate addresses paired with essential compliance architecture to streamline your regulatory presence seamlessly.
                </p>
                <div class="flex flex-wrap gap-6">
                    <a href="/contact" class="bg-[#011F3F] text-white px-12 py-5 text-[10px] font-black uppercase tracking-[0.3em] hover:bg-[#C5A059] transition-all duration-300 shadow-sm">Initialize Setup</a>
                </div>
            </div>

            <div class="hidden lg:block lg:col-span-5 reveal-right">
                <div class="relative p-4">
                    <div class="aspect-[4/5] bg-[#011F3F] overflow-hidden shadow-[0_30px_70px_rgba(1,31,63,0.06)]">
                        <img src="https://images.unsplash.com/photo-1497366216548-37526070297c?auto=format&fit=crop&q=80&w=1200" alt="Corporate Business Core Address Infrastructure" class="w-full h-full object-cover filter grayscale contrast-125 mix-blend-luminosity">
                    </div>
                    <div class="absolute -bottom-2 -right-2 w-40 h-40 border-b border-r border-[#C5A059]/30 -z-10"></div>
                </div>
            </div>

        </div>
    </section>

    <section class="py-28 bg-[#FBF9F4] border-t border-[#011F3F]/5">
        <div class="max-w-7xl mx-auto px-8">
            
            <div class="reveal-up mb-20 text-center">
                <span class="text-[10px] uppercase tracking-[0.4em] text-[#011F3F]/50 block mb-3">Prestigious Legal Anchors</span>
                <h2 class="text-3xl md:text-5xl font-serif font-light text-[#011F3F]">Our Premium Locations</h2>
                <div class="w-20 h-[1px] bg-[#011F3F]/20 mx-auto mt-5"></div>
            </div>

            <div class="grid grid-cols-1 lg:grid-cols-3 gap-10 items-stretch">
                
                <div class="reveal-up flex flex-col bg-white border border-navy/5 shadow-sm rounded-sm overflow-hidden" data-location-card="makati">
                    <div class="office-viewer-frame" id="makatiViewer">
                        <img src="https://images.unsplash.com/photo-1497366216548-37526070297c?auto=format&fit=crop&q=80&w=800" alt="Makati Boardroom Option" class="office-img-node img-visible filter grayscale contrast-110">
                        <img src="https://images.unsplash.com/photo-1497215728101-856f4ea42174?auto=format&fit=crop&q=80&w=800" alt="Makati Open Desk Framework" class="office-img-node filter grayscale contrast-110">
                        <img src="https://images.unsplash.com/photo-1497366811353-6870744d04b2?auto=format&fit=crop&q=80&w=800" alt="Makati Executive Layout" class="office-img-node filter grayscale contrast-110">
                        <img src="https://images.unsplash.com/photo-1517502884422-41eaead166d4?auto=format&fit=crop&q=80&w=800" alt="Makati Shared Lounge Area" class="office-img-node filter grayscale contrast-110">
                        
                        <div class="photo-dots-indicator" id="makatiPhotoDots"></div>
                    </div>
                    <div class="p-8 flex-grow flex flex-col justify-between">
                        <div>
                            <span class="text-[10px] uppercase tracking-[0.25em] text-[#C5A059] font-bold block mb-2">Central Business District</span>
                            <h3 class="text-2xl font-serif font-normal text-[#011F3F] mb-4">Makati City</h3>
                            <p class="text-sm font-light text-[#2D3748] leading-relaxed mb-6">
                                Establish prominence in the financial core of the Philippines. Perfect for institutional credibility, corporate filings, and high-stakes investor board meetings.
                            </p>
                        </div>
                        <div class="pt-4 border-t border-navy/5 flex items-center justify-between text-xs font-medium text-[#011F3F]">
                            <span>Hours: 8:00 AM – 5:00 PM</span>
                            <span class="gold-accent uppercase tracking-widest text-[10px] font-bold">Active Branch</span>
                        </div>
                    </div>
                </div>

                <div class="reveal-up flex flex-col bg-white border border-navy/5 shadow-sm rounded-sm overflow-hidden" data-location-card="ortigas">
                    <div class="office-viewer-frame" id="ortigasViewer">
                        <img src="https://images.unsplash.com/photo-1497215728101-856f4ea42174?auto=format&fit=crop&q=80&w=800" alt="Ortigas Facility Lounge" class="office-img-node img-visible filter grayscale contrast-110">
                        <img src="https://images.unsplash.com/photo-1497366811353-6870744d04b2?auto=format&fit=crop&q=80&w=800" alt="Ortigas Dedicated Conference Setup" class="office-img-node filter grayscale contrast-110">
                        <img src="https://images.unsplash.com/photo-1416339306562-f3d12fefd36f?auto=format&fit=crop&q=80&w=800" alt="Ortigas Minimal Private Suite" class="office-img-node filter grayscale contrast-110">
                        <img src="https://images.unsplash.com/photo-1497366216548-37526070297c?auto=format&fit=crop&q=80&w=800" alt="Ortigas Shared Workspace Wing" class="office-img-node filter grayscale contrast-110">
                        
                        <div class="photo-dots-indicator" id="ortigasPhotoDots"></div>
                    </div>
                    <div class="p-8 flex-grow flex flex-col justify-between">
                        <div>
                            <span class="text-[10px] uppercase tracking-[0.25em] text-[#C5A059] font-bold block mb-2">Strategic Tech & Commerce</span>
                            <h3 class="text-2xl font-serif font-normal text-[#011F3F] mb-4">Ortigas Center</h3>
                            <p class="text-sm font-light text-[#2D3748] leading-relaxed mb-6">
                                Positioned perfectly at the geographic intersection of metro commercial routes. High-tier building infrastructure optimizing access for distributed digital teams.
                            </p>
                        </div>
                        <div class="pt-4 border-t border-navy/5 flex items-center justify-between text-xs font-medium text-[#011F3F]">
                            <span>Hours: 8:00 AM – 5:00 PM</span>
                            <span class="gold-accent uppercase tracking-widest text-[10px] font-bold">Active Branch</span>
                        </div>
                    </div>
                </div>

                <div class="reveal-up flex flex-col bg-transparent border-2 border-dashed border-[#011F3F]/10 rounded-sm relative overflow-hidden group">
                    <div class="absolute inset-0 bg-[#011F3F]/5 pointer-events-none"></div>
                    <div class="p-10 my-auto text-center flex flex-col items-center justify-center">
                        <div class="w-16 h-16 rounded-full bg-[#011F3F]/5 flex items-center justify-center mb-6 text-[#C5A059]">
                            <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><circle cx="12" cy="12" r="10"></circle><polyline points="12 6 12 12 16 14"></polyline></svg>
                        </div>
                        <span class="text-[10px] uppercase tracking-[0.3em] gold-accent font-bold block mb-2">Expansion Horizon</span>
                        <h3 class="text-3xl font-serif font-light text-[#011F3F] mb-4">Quezon City</h3>
                        <p class="text-sm font-light text-[#2D3748]/70 leading-relaxed max-w-xs mb-6">
                            Unlocking premium operational legal frameworks soon in the north cluster's most expansive innovation district.
                        </p>
                        <span class="inline-block px-4 py-2 border border-[#011F3F]/20 text-[9px] uppercase tracking-[0.25em] font-bold text-[#011F3F]/60">Opening Soon</span>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <section class="py-32 bg-white">
        <div class="max-w-7xl mx-auto px-8">
            
            <div class="reveal-up mb-24 text-center">
                <span class="text-[20px] uppercase tracking-[0.4em] text-[#011F3F]/40 block mb-3">Operational Offerings</span>
                <h2 class="text-2xl md:text-2xl font-serif font-light text-[#011F3F]">Package Deployments</h2>
                <div class="w-16 h-[1px] bg-[#011F3F]/20 mx-auto mt-6"></div>
            </div>

            <div class="reveal-up relative">
                <div class="slider-viewport" id="officeSlider">
                    <div class="slider-track" id="officeTrack">
                        
                        <div class="package-slide-wrapper">
                            <div class="package-slide text-center">
                                <h3 class="package-headline gold-accent">Virtual Office Base Address</h3>
                                <div class="package-details-list max-w-4xl mx-auto font-light">
                                    Use of premium address for business registration purposes <br>
                                    Mandatory matching integration with monthly corporate accounting architecture <br>
                                    Comprehensive handling frameworks for statutory compliance documentation
                                </div>
                            </div>
                        </div>
                        
                        <div class="package-slide-wrapper">
                            <div class="package-slide text-center">
                                <h3 class="package-headline gold-accent">Address Migration Solutions</h3>
                                <div class="package-details-list max-w-4xl mx-auto font-light">
                                    Complete corporate address change and relocation paperwork management <br>
                                    Seamless transition handling from historical virtual or physical providers <br>
                                    Official agency updates to securely re-baseline municipal and state profiles
                                </div>
                            </div>
                        </div>
                        
                        <div class="package-slide-wrapper">
                            <div class="package-slide text-center">
                                <h3 class="package-headline gold-accent">Conference Room Allocations</h3>
                                <div class="package-details-list max-w-4xl mx-auto font-light">
                                    Access to secure, modern on-demand boardroom facilities <br>
                                    Equipped with baseline corporate communication tools and high-speed networks <br>
                                    Strategic 24-hour advance reservation framework matching operational timelines
                                </div>
                            </div>
                        </div>

                    </div>
                </div>

                <div class="flex items-center justify-between max-w-md mx-auto mt-16">
                    <button class="slider-nav-btn" onclick="moveOfficeSlide(-1)" aria-label="Previous operational segment">
                        <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><polyline points="15 18 9 12 15 6"></polyline></svg>
                    </button>
                    
                    <div class="flex gap-3.5" id="officeDotsContainer"></div>
                    
                    <button class="slider-nav-btn" onclick="moveOfficeSlide(1)" aria-label="Next operational segment">
                        <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><polyline points="9 18 15 12 9 6"></polyline></svg>
                    </button>
                </div>

            </div>
        </div>
    </section>

    <section class="py-32 bg-white border-t border-[#011F3F]/10">
        <div class="max-w-4xl mx-auto px-8 reveal-up">
            
            <div class="mb-16">
                <span class="text-[10px] uppercase tracking-[0.4em] text-[#011F3F]/40 block mb-3">Information Bureau</span>
                <h2 class="text-3xl md:text-4xl font-serif font-light text-[#011F3F]">Frequently Asked Questions</h2>
            </div>

            <div class="divide-y divide-[#011F3F]/10">
                
                <div>
                    <button class="faq-trigger" onclick="toggleFaq(this)">
                        <span>What packages for virtual offices does our company offer?</span>
                        <span class="faq-icon">&#43;</span>
                    </button>
                    <div class="faq-content">
                        <div class="faq-text">
                            We offer virtual office packages with a mandatory subscription to monthly bookkeeping and tax filing services, as well as configurations bundling a Virtual Office + Change of Business Address for clients looking to update existing setups or switch providers.
                        </div>
                    </div>
                </div>

                <div>
                    <button class="faq-trigger" onclick="toggleFaq(this)">
                        <span>What documents must I supply in order to use the virtual office package?</span>
                        <span class="faq-icon">&#43;</span>
                    </button>
                    <div class="faq-content">
                        <div class="faq-text">
                            Prerequisites depend on registration status. Generally, active entities must supply current corporate documentation, identity validations, and financial baseline files to align with our mandatory compliance tracking.
                        </div>
                    </div>
                </div>

                <div>
                    <button class="faq-trigger" onclick="toggleFaq(this)">
                        <span>Do you take in clients from abroad that require a virtual address in the Philippines?</span>
                        <span class="faq-icon">&#43;</span>
                    </button>
                    <div class="faq-content">
                        <div class="faq-text">
                            Yes, international entities seeking an established legal presence and compliance framework in the Philippines are supported, provided registration and tax accounting integrations are maintained.
                        </div>
                    </div>
                </div>

                <div>
                    <button class="faq-trigger" onclick="toggleFaq(this)">
                        <span>The DTI or SEC are still processing my company name. Can I still submit a virtual office application?</span>
                        <span class="faq-icon">&#43;</span>
                    </button>
                    <div class="faq-content">
                        <div class="faq-text">
                            Yes, as long as the business could provide the updated documents and must avail our monthly bookkeeping and tax filing service.
                        </div>
                    </div>
                </div>

                <div>
                    <button class="faq-trigger" onclick="toggleFaq(this)">
                        <span>How long does it take if I want to avail a Virtual Office? Could it take a day or less?</span>
                        <span class="faq-icon">&#43;</span>
                    </button>
                    <div class="faq-content">
                        <div class="faq-text">
                            Since most of the services required for processing virtual office are already available here in-house, the processing time would be reduced up to 1 business day depending on the processing speed of the documents that would be reviewed and the availability of concerned employees.
                        </div>
                    </div>
                </div>

                <div>
                    <button class="faq-trigger" onclick="toggleFaq(this)">
                        <span>Is it possible for me to switch to a shared co-working space in the future if I avail the Virtual Office?</span>
                        <span class="faq-icon">&#43;</span>
                    </button>
                    <div class="faq-content">
                        <div class="faq-text">
                            It is possible to switch as long as the necessary payment and documents would be provided.
                        </div>
                    </div>
                </div>

                <div>
                    <button class="faq-trigger" onclick="toggleFaq(this)">
                        <span>Do mail and call handling come with a virtual office package?</span>
                        <span class="faq-icon">&#43;</span>
                    </button>
                    <div class="faq-content">
                        <div class="faq-text">
                            No, the Virtual Office package only covers the use of virtual address for the business and does not include mail and call handling.
                        </div>
                    </div>
                </div>

                <div>
                    <button class="faq-trigger" onclick="toggleFaq(this)">
                        <span>Do I have access to additional services if I have a virtual office?</span>
                        <span class="faq-icon">&#43;</span>
                    </button>
                    <div class="faq-content">
                        <div class="faq-text">
                            No, the virtual office package is only limited to use of virtual address for business purposes and does not include additional services.
                        </div>
                    </div>
                </div>

                <div>
                    <button class="faq-trigger" onclick="toggleFaq(this)">
                        <span>When may I reserve a conference room?</span>
                        <span class="faq-icon">&#43;</span>
                    </button>
                    <div class="faq-content">
                        <div class="faq-text">
                            The conference room is available during weekdays and must be reserved one (1) day before.
                        </div>
                    </div>
                </div>

                <div>
                    <button class="faq-trigger" onclick="toggleFaq(this)">
                        <span>Can I visit and make use of the facilities whenever I want if I purchase a Virtual Office package?</span>
                        <span class="faq-icon">&#43;</span>
                    </button>
                    <div class="faq-content">
                        <div class="faq-text">
                            No, virtual space is only limited to the company using our virtual address and does not include any of our facilities. Should the client be interested in accessing our facilities, a dedicated desk package is also being offered.
                        </div>
                    </div>
                </div>

                <div>
                    <button class="faq-trigger" onclick="toggleFaq(this)">
                        <span>Where are our operational locations and what are its business hours?</span>
                        <span class="faq-icon">&#43;</span>
                    </button>
                    <div class="faq-content">
                        <div class="faq-text">
                            We have two (2) locations for virtual office: Makati City and Ortigas Center. Both offices operate under the same business hours, from 8:00 AM to 5:00 PM.
                        </div>
                    </div>
                </div>

                <div>
                    <button class="faq-trigger" onclick="toggleFaq(this)">
                        <span>What methods of payment are available for my bundle of virtual offices?</span>
                        <span class="faq-icon">&#43;</span>
                    </button>
                    <div class="faq-content">
                        <div class="faq-text">
                            You can settle your virtual office bundle payment through bank transfer to BPI account number xxxxxxx or via GCash to 09xxxxxxx. Please reference your invoice number for easy tracking.
                        </div>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <section class="py-32 bg-[#011F3F] text-[#FDFBF7]">
        <div class="max-w-7xl mx-auto px-8">
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-24 items-start">
                
                <div class="reveal-left">
                    <span class="text-[10px] uppercase tracking-[0.5em] text-[#C5A059] block mb-4 font-black">Prerequisites</span>
                    <h2 class="text-3xl md:text-5xl font-serif font-light mb-16 leading-tight">Integration <br><span class="gold-accent italic">Parameters</span></h2>
                    
                    <ul class="space-y-12">
                        <li class="flex gap-8">
                            <span class="gold-accent font-light text-xl tracking-widest border-b border-[#C5A059]/20 h-8">01</span>
                            <div>
                                <h4 class="font-bold uppercase tracking-[0.2em] text-xs mb-2 text-white">Compliance Bundle</h4>
                                <p class="text-[#FDFBF7]/60 font-light text-sm leading-relaxed">All active spatial addresses require integration into internal monthly bookkeeping and tax filing deployment tracks.</p>
                            </div>
                        </li>
                        <li class="flex gap-8">
                            <span class="gold-accent font-light text-xl tracking-widest border-b border-[#C5A059]/20 h-8">02</span>
                            <div>
                                <h4 class="font-bold uppercase tracking-[0.2em] text-xs mb-2 text-white">Documentation Lifecycle</h4>
                                <p class="text-[#FDFBF7]/60 font-light text-sm leading-relaxed">Applications are subject to standard document verification loops; initialization completes within an agile 1-business-day response envelope.</p>
                            </div>
                        </li>
                        <li class="flex gap-8">
                            <span class="gold-accent font-light text-xl tracking-widest border-b border-[#C5A059]/20 h-8">03</span>
                            <div>
                                <h4 class="font-bold uppercase tracking-[0.2em] text-xs mb-2 text-white">Physical Scope</h4>
                                <p class="text-[#FDFBF7]/60 font-light text-sm leading-relaxed">Virtual options provide digital legal presence and regulatory registration anchors; dedicated workstation access requires desk-package tier mapping.</p>
                            </div>
                        </li>
                    </ul>
                </div>

                <div class="reveal-right bg-white/[0.02] p-12 md:p-16 border border-white/10 backdrop-blur-sm shadow-2xl mt-4">
                    <h3 class="text-2xl font-serif mb-6 italic gold-accent font-light">Initiate Corporate Registration</h3>
                    <p class="text-sm font-light mb-12 leading-relaxed text-[#FDFBF7]/70">
                        Map your virtual office requirements to our strategic regulatory legal footprints in premium metropolitan zones. Let's align your infrastructure setup today.
                    </p>
                    <div class="space-y-6">
                        <a href="/contact" class="block w-full text-center bg-[#C5A059] text-[#011F3F] py-5 font-black uppercase tracking-[0.3em] text-[10px] hover:bg-white transition-all duration-300">Request Configuration</a>
                    </div>
                </div>
                
            </div>
        </div>
    </section>

</div>

<script>
    // Universal Animation Observer Hook
    const globalObserver = new IntersectionObserver((entries) => {
        entries.forEach(entry => {
            if (entry.isIntersecting) entry.target.classList.add('active');
        });
    }, { threshold: 0.05 });

    document.querySelectorAll('.reveal-up, .reveal-left, .reveal-right').forEach((el) => {
        globalObserver.observe(el);
    });

    // Carousel Slider Logical Parameters Engine
    let activeOfficeIndex = 0;
    const officeTrack = document.getElementById('officeTrack');
    const officeSlides = document.querySelectorAll('.package-slide-wrapper');
    const maximumSlides = officeSlides.length;
    const officeDotsContainer = document.getElementById('officeDotsContainer');
    let autoMoveTimer;
    
    let swipeStartCoordinateX = 0;
    let swipeEndCoordinateX = 0;

    function renderNavigationDots() {
        officeDotsContainer.innerHTML = '';
        for (let i = 0; i < maximumSlides; i++) {
            const individualDot = document.createElement('button');
            individualDot.className = `slider-dot ${i === 0 ? 'dot-active' : ''}`;
            individualDot.setAttribute('aria-label', `Go to operational segment slide ${i + 1}`);
            individualDot.addEventListener('click', () => {
                transitionToSpecificSlide(i);
                refreshAutoMoveTimer();
            });
            officeDotsContainer.appendChild(individualDot);
        }
    }

    function recomputeTrackTranslation() {
        officeTrack.style.transform = `translateX(-${activeOfficeIndex * 100}%)`;
        
        const allDots = document.querySelectorAll('.slider-dot');
        allDots.forEach((dotInstance, indexMark) => {
            if (indexMark === activeOfficeIndex) {
                dotInstance.classList.add('dot-active');
            } else {
                dotInstance.classList.remove('dot-active');
            }
        });
    }

    function transitionToSpecificSlide(targetIndex) {
        activeOfficeIndex = targetIndex;
        recomputeTrackTranslation();
    }

    function moveOfficeSlide(offsetDirection) {
        activeOfficeIndex += offsetDirection;
        if (activeOfficeIndex >= maximumSlides) {
            activeOfficeIndex = 0;
        } else if (activeOfficeIndex < 0) {
            activeOfficeIndex = maximumSlides - 1;
        }
        recomputeTrackTranslation();
    }

    function launchAutoMoveSequence() {
        autoMoveTimer = setInterval(() => {
            moveOfficeSlide(1);
        }, 6000); 
    }

    function refreshAutoMoveTimer() {
        clearInterval(autoMoveTimer);
        launchAutoMoveSequence();
    }

    const interactionViewport = document.getElementById('officeSlider');
    
    interactionViewport.addEventListener('touchstart', (eventContext) => {
        swipeStartCoordinateX = eventContext.changedTouches[0].screenX;
        clearInterval(autoMoveTimer);
    }, { passive: true });

    interactionViewport.addEventListener('touchend', (eventContext) => {
        swipeEndCoordinateX = eventContext.changedTouches[0].screenX;
        processTouchSwipeTrajectory();
        launchAutoMoveSequence();
    }, { passive: true });

    function processTouchSwipeTrajectory() {
        const structuralSwipeThreshold = 50;
        if (swipeStartCoordinateX - swipeEndCoordinateX > structuralSwipeThreshold) {
            moveOfficeSlide(1);
        } else if (swipeEndCoordinateX - swipeStartCoordinateX > structuralSwipeThreshold) {
            moveOfficeSlide(-1);
        }
    }

    // Modern Minimalist Accordion Execution Function
    function toggleFaq(buttonElement) {
        const icon = buttonElement.querySelector('.faq-icon');
        const contentPanel = buttonElement.nextElementSibling;
        
        if (contentPanel.style.maxHeight && contentPanel.style.maxHeight !== '0px') {
            contentPanel.style.maxHeight = '0px';
            icon.innerHTML = '&#43;';
        } else {
            document.querySelectorAll('.faq-content').forEach(panel => panel.style.maxHeight = '0px');
            document.querySelectorAll('.faq-icon').forEach(ico => ico.innerHTML = '&#43;');
            
            contentPanel.style.maxHeight = contentPanel.scrollHeight + 'px';
            icon.innerHTML = '&#8722;';
        }
    }

    // Office Image Slide-Fade Loop Engine with Explicit Indicators
    function setupOfficeImageSliders() {
        const viewports = ['makati', 'ortigas'];
        
        viewports.forEach(location => {
            const container = document.getElementById(`${location}Viewer`);
            const indicatorContainer = document.getElementById(`${location}PhotoDots`);
            if (!container || !indicatorContainer) return;
            
            const images = container.querySelectorAll('.office-img-node');
            const totalPhotos = images.length;
            
            indicatorContainer.innerHTML = '';
            for (let i = 0; i < totalPhotos; i++) {
                const dot = document.createElement('span');
                dot.className = `photo-dot ${i === 0 ? 'active-photo-dot' : ''}`;
                indicatorContainer.appendChild(dot);
            }
            
            const photoDotsNodes = indicatorContainer.querySelectorAll('.photo-dot');
            let idx = 0;
            
            setInterval(() => {
                images[idx].classList.remove('img-visible');
                photoDotsNodes[idx].classList.remove('active-photo-dot');
                
                idx = (idx + 1) % totalPhotos;
                
                images[idx].classList.add('img-visible');
                photoDotsNodes[idx].classList.add('active-photo-dot');
            }, 4500);
        });
    }

    // Fix factual discrepancy in location text from source raw template file
    document.querySelectorAll('.faq-text').forEach(faq => {
        if(faq.innerText.includes('Makati City and Muntinlupa City')) {
            faq.innerText = faq.innerText.replace('Muntinlupa City', 'Ortigas Center');
        }
    });

    renderNavigationDots();
    launchAutoMoveSequence();
    setupOfficeImageSliders();
</script>