<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Noble Consultant | Elite Enterprise & Digital Growth Strategy</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- FontAwesome Icons CDN -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts Inter & Plus Jakarta Sans -->
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800&family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        brand: {
                            coral: '#E8532B',       // Matches 'C' in logo
                            coralHover: '#D0421B',
                            lightCoral: '#FFF2EE',
                            dark: '#0D0D0E',        // Deep obsidian black
                            charcoal: '#18181B',    // Card background black
                            surface: '#242428',     // Secondary surface dark
                            cream: '#FAF8F5',       
                            muted: '#A1A1AA'
                        }
                    },
                    fontFamily: {
                        sans: ['Plus Jakarta Sans', 'Inter', 'sans-serif'],
                    },
                    maxWidth: {
                        '8xl': '1360px',
                        '9xl': '1440px'
                    }
                }
            }
        }
    </script>
    <style>
        body {
            font-family: 'Plus Jakarta Sans', sans-serif;
            background-color: #0D0D0E;
            color: #F4F4F5;
            overflow-x: hidden;
        }
        .nc-gradient-text {
            background: linear-gradient(135deg, #FFFFFF 30%, #E8532B 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        .nc-coral-gradient {
            background: linear-gradient(135deg, #E8532B 0%, #FF734C 100%);
        }
        .nc-glass {
            background: rgba(24, 24, 27, 0.85);
            backdrop-filter: blur(16px);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        .nc-glow {
            box-shadow: 0 12px 35px -10px rgba(232, 83, 43, 0.35);
        }
        .custom-scrollbar::-webkit-scrollbar {
            width: 8px;
        }
        .custom-scrollbar::-webkit-scrollbar-track {
            background: #0D0D0E;
        }
        .custom-scrollbar::-webkit-scrollbar-thumb {
            background: #242428;
            border-radius: 4px;
        }
        .custom-scrollbar::-webkit-scrollbar-thumb:hover {
            background: #E8532B;
        }
    </style>
</head>
<body class="custom-scrollbar min-h-screen flex flex-col justify-between selection:bg-brand-coral selection:text-white">

    <!-- NAVIGATION BAR -->
    <header class="sticky top-0 z-50 nc-glass border-b border-white/10 transition-all duration-300" id="mainHeader">
        <div class="max-w-8xl mx-auto px-4 sm:px-6 lg:px-12 h-20 sm:h-24 flex items-center justify-between">
            <!-- Brand Logo -->
            <a href="#" onclick="navigateTo('home'); return false;" class="flex items-center gap-3 group">
                <div class="relative w-11 h-11 sm:w-12 sm:h-12 bg-black rounded-xl border border-white/20 p-1.5 flex flex-col justify-center items-center shadow-lg group-hover:border-brand-coral transition-colors shrink-0">
                    <div class="flex items-center leading-none text-xl sm:text-2xl font-extrabold tracking-tighter">
                        <span class="text-white">N</span>
                        <span class="text-brand-coral">C</span>
                    </div>
                    <span class="text-[7px] sm:text-[8px] text-white/70 font-semibold tracking-widest mt-0.5">NOBLE</span>
                </div>
                <div class="flex flex-col">
                    <span class="text-base sm:text-xl font-bold tracking-tight text-white group-hover:text-brand-coral transition-colors leading-tight">NOBLE CONSULTANT</span>
                    <span class="text-[10px] sm:text-xs tracking-widest text-brand-coral uppercase font-semibold">Strategy & Enterprise Growth</span>
                </div>
            </a>

            <!-- Desktop Nav Links -->
            <nav class="hidden lg:flex items-center space-x-1 xl:space-x-3">
                <button onclick="navigateTo('home')" class="nav-link px-4 py-2.5 text-sm xl:text-base font-semibold text-white hover:text-brand-coral transition-colors rounded-xl hover:bg-white/5 active-nav" data-page="home">Home</button>
                <button onclick="navigateTo('about')" class="nav-link px-4 py-2.5 text-sm xl:text-base font-semibold text-white/80 hover:text-brand-coral transition-colors rounded-xl hover:bg-white/5" data-page="about">About Us</button>
                <button onclick="navigateTo('services')" class="nav-link px-4 py-2.5 text-sm xl:text-base font-semibold text-white/80 hover:text-brand-coral transition-colors rounded-xl hover:bg-white/5" data-page="services">Capabilities</button>
                <button onclick="navigateTo('projects')" class="nav-link px-4 py-2.5 text-sm xl:text-base font-semibold text-white/80 hover:text-brand-coral transition-colors rounded-xl hover:bg-white/5" data-page="projects">Case Studies</button>
                <button onclick="navigateTo('testimonials')" class="nav-link px-4 py-2.5 text-sm xl:text-base font-semibold text-white/80 hover:text-brand-coral transition-colors rounded-xl hover:bg-white/5" data-page="testimonials">Reviews</button>
                <button onclick="navigateTo('pricing')" class="nav-link px-4 py-2.5 text-sm xl:text-base font-semibold text-white/80 hover:text-brand-coral transition-colors rounded-xl hover:bg-white/5" data-page="pricing">Pricing</button>
            </nav>

            <!-- CTA Header Button -->
            <div class="hidden lg:flex items-center gap-4">
                <button onclick="navigateTo('contact')" class="nc-coral-gradient text-white px-6 py-3 rounded-xl font-bold text-sm xl:text-base hover:scale-[1.02] transition-all nc-glow flex items-center gap-2">
                    <span>Get Consultation</span>
                    <i class="fa-solid fa-arrow-right text-xs"></i>
                </button>
            </div>

            <!-- Mobile Hamburger Button -->
            <div class="lg:hidden flex items-center">
                <button id="mobileMenuBtn" onclick="toggleMobileMenu()" class="p-2.5 rounded-xl text-white/80 hover:text-white hover:bg-white/10 focus:outline-none">
                    <i class="fa-solid fa-bars text-2xl" id="menuIcon"></i>
                </button>
            </div>
        </div>

        <!-- Mobile Drawer Menu -->
        <div id="mobileMenu" class="hidden lg:hidden nc-glass border-b border-white/10 px-6 pt-3 pb-8 space-y-3">
            <button onclick="navigateTo('home'); toggleMobileMenu();" class="block w-full text-left px-4 py-3 text-base font-semibold text-white hover:bg-white/5 rounded-xl">Home</button>
            <button onclick="navigateTo('about'); toggleMobileMenu();" class="block w-full text-left px-4 py-3 text-base font-semibold text-white/80 hover:bg-white/5 rounded-xl">About Us</button>
            <button onclick="navigateTo('services'); toggleMobileMenu();" class="block w-full text-left px-4 py-3 text-base font-semibold text-white/80 hover:bg-white/5 rounded-xl">Capabilities</button>
            <button onclick="navigateTo('projects'); toggleMobileMenu();" class="block w-full text-left px-4 py-3 text-base font-semibold text-white/80 hover:bg-white/5 rounded-xl">Case Studies</button>
            <button onclick="navigateTo('testimonials'); toggleMobileMenu();" class="block w-full text-left px-4 py-3 text-base font-semibold text-white/80 hover:bg-white/5 rounded-xl">Reviews & Wall of Love</button>
            <button onclick="navigateTo('pricing'); toggleMobileMenu();" class="block w-full text-left px-4 py-3 text-base font-semibold text-white/80 hover:bg-white/5 rounded-xl">Pricing Packages</button>
            <button onclick="navigateTo('contact'); toggleMobileMenu();" class="mt-4 w-full nc-coral-gradient text-white py-3.5 rounded-xl font-bold text-center block">Contact Noble Consultant</button>
        </div>
    </header>

    <main id="appContent" class="flex-grow">
        <!-- ========================================================================= -->
        <!-- PAGE 1: HOME PAGE -->
        <!-- ========================================================================= -->
        <section id="page-home" class="page-view block">
            <!-- Hero Section with Desktop Wide Layout -->
            <div class="relative overflow-hidden py-12 lg:py-24 px-4 sm:px-6 lg:px-12 max-w-8xl mx-auto">
                <!-- Background Ambient Lights -->
                <div class="absolute top-1/3 left-1/2 -translate-x-1/2 -translate-y-1/2 w-[700px] h-[700px] bg-brand-coral/15 rounded-full blur-[160px] pointer-events-none"></div>

                <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 xl:gap-16 items-center">
                    <!-- Left Hero Text -->
                    <div class="lg:col-span-7 space-y-6 lg:space-y-8 text-center lg:text-left">
                        <div class="inline-flex items-center gap-2 px-4 py-2 rounded-full bg-brand-coral/10 border border-brand-coral/30 text-brand-coral text-xs sm:text-sm font-bold tracking-wide uppercase">
                            <i class="fa-solid fa-gem text-xs"></i>
                            <span>Noble Business Strategy & Advisory</span>
                        </div>
                        
                        <h1 class="text-4xl sm:text-5xl lg:text-6xl xl:text-7xl font-extrabold tracking-tight text-white leading-[1.12]">
                            Accelerating Enterprise <span class="nc-gradient-text">Revenue & Sustainable Growth</span>
                        </h1>
                        
                        <p class="text-base sm:text-xl text-zinc-300 max-w-3xl mx-auto lg:mx-0 leading-relaxed font-normal">
                            Welcome to <strong class="text-white font-semibold">Noble Consultant</strong>. We partner with founders, executives, and scaling brands to optimize operations, implement modern growth systems, and elevate market influence.
                        </p>

                        <div class="flex flex-col sm:flex-row items-center justify-center lg:justify-start gap-4 pt-4">
                            <button onclick="navigateTo('contact')" class="w-full sm:w-auto nc-coral-gradient text-white px-8 py-4 sm:py-5 rounded-2xl font-bold text-base sm:text-lg hover:scale-[1.02] transition-all nc-glow flex items-center justify-center gap-3">
                                <span>Book Strategic Consultation</span>
                                <i class="fa-solid fa-calendar-check"></i>
                            </button>
                            <button onclick="navigateTo('projects')" class="w-full sm:w-auto bg-brand-surface hover:bg-white/10 text-white border border-white/10 px-8 py-4 sm:py-5 rounded-2xl font-semibold text-base sm:text-lg transition-all flex items-center justify-center gap-3">
                                <i class="fa-solid fa-chart-line text-brand-coral"></i>
                                <span>View Case Studies</span>
                            </button>
                        </div>

                        <!-- Mini Social Proof Metric Bar -->
                        <div class="pt-8 sm:pt-10 border-t border-white/10 grid grid-cols-3 gap-6 text-center lg:text-left">
                            <div>
                                <p class="text-2xl sm:text-4xl font-extrabold text-white">98%</p>
                                <p class="text-xs sm:text-sm text-zinc-400 mt-1 font-medium">Client Retention</p>
                            </div>
                            <div>
                                <p class="text-2xl sm:text-4xl font-extrabold text-brand-coral">$45M+</p>
                                <p class="text-xs sm:text-sm text-zinc-400 mt-1 font-medium">Value Generated</p>
                            </div>
                            <div>
                                <p class="text-2xl sm:text-4xl font-extrabold text-white">120+</p>
                                <p class="text-xs sm:text-sm text-zinc-400 mt-1 font-medium">Projects Delivered</p>
                            </div>
                        </div>
                    </div>

                    <!-- Right Hero Image - User Portrait Container -->
                    <div class="lg:col-span-5 relative flex justify-center">
                        <div class="relative w-full max-w-lg lg:max-w-none">
                            <!-- Background Glow Frame -->
                            <div class="absolute inset-0 bg-gradient-to-tr from-brand-coral via-orange-500 to-amber-500 rounded-3xl transform rotate-2 scale-95 opacity-70 blur-md"></div>
                            
                            <!-- Main Portrait Container -->
                            <div class="relative bg-brand-charcoal border border-white/20 rounded-3xl overflow-hidden shadow-2xl">
                                <img src="image_0b0f18.jpg" alt="Noble Consultant Advisor" class="w-full h-auto object-cover max-h-[620px] w-full filter brightness-105 contrast-105" onerror="this.onerror=null; this.src='https://placehold.co/700x850/18181b/ffffff?text=Noble+Consultant+Advisor'">
                                
                                <!-- Floating Badge Top -->
                                <div class="absolute top-5 right-5 nc-glass px-4 py-2.5 rounded-2xl flex items-center gap-3 border border-brand-coral/40">
                                    <div class="w-3 h-3 rounded-full bg-emerald-500 animate-pulse"></div>
                                    <div class="text-left">
                                        <p class="text-[10px] text-zinc-400 uppercase font-bold tracking-wider">Status</p>
                                        <p class="text-xs font-bold text-white">Accepting Q4 Clients</p>
                                    </div>
                                </div>

                                <!-- Floating Overlay Badge Bottom -->
                                <div class="absolute bottom-5 left-5 right-5 nc-glass p-4 sm:p-5 rounded-2xl border border-white/20">
                                    <div class="flex items-center justify-between">
                                        <div>
                                            <h4 class="text-sm sm:text-base font-bold text-white">Lead Strategic Consultant</h4>
                                            <p class="text-xs sm:text-sm text-brand-coral font-semibold">Noble Consultant Advisory</p>
                                        </div>
                                        <div class="flex text-amber-400 text-xs sm:text-sm gap-1">
                                            <i class="fa-solid fa-star"></i>
                                            <i class="fa-solid fa-star"></i>
                                            <i class="fa-solid fa-star"></i>
                                            <i class="fa-solid fa-star"></i>
                                            <i class="fa-solid fa-star"></i>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Trust Brands Banner -->
            <div class="py-12 bg-brand-charcoal/70 border-y border-white/5 my-12">
                <div class="max-w-8xl mx-auto px-4 sm:px-6 lg:px-12 text-center">
                    <p class="text-xs sm:text-sm font-bold text-zinc-400 uppercase tracking-widest mb-8">Trusted by Innovative Founders & Enterprise Operations Worldwide</p>
                    <div class="grid grid-cols-2 sm:grid-cols-3 lg:grid-cols-5 gap-8 items-center opacity-80 hover:opacity-100 transition-opacity">
                        <div class="text-base sm:text-xl font-extrabold tracking-wider text-zinc-300 flex items-center justify-center"><i class="fa-solid fa-building text-brand-coral mr-2"></i>APEX HOLDINGS</div>
                        <div class="text-base sm:text-xl font-extrabold tracking-wider text-zinc-300 flex items-center justify-center"><i class="fa-solid fa-chart-pie text-brand-coral mr-2"></i>VENTURE MATRIX</div>
                        <div class="text-base sm:text-xl font-extrabold tracking-wider text-zinc-300 flex items-center justify-center"><i class="fa-solid fa-shield-halved text-brand-coral mr-2"></i>NEXUS CAPITAL</div>
                        <div class="text-base sm:text-xl font-extrabold tracking-wider text-zinc-300 flex items-center justify-center"><i class="fa-solid fa-rocket text-brand-coral mr-2"></i>ELEVATE TECH</div>
                        <div class="text-base sm:text-xl font-extrabold tracking-wider text-zinc-300 flex items-center justify-center col-span-2 sm:col-span-1"><i class="fa-solid fa-globe text-brand-coral mr-2"></i>HORIZON CORP</div>
                    </div>
                </div>
            </div>

            <!-- CORE SERVICES PREVIEW -->
            <div class="py-20 max-w-8xl mx-auto px-4 sm:px-6 lg:px-12">
                <div class="text-center max-w-3xl mx-auto mb-16">
                    <span class="text-brand-coral font-bold text-sm sm:text-base tracking-widest uppercase">High Impact Capabilities</span>
                    <h2 class="text-3xl sm:text-5xl font-extrabold text-white mt-3">Tailored Consultancy for Scale</h2>
                    <p class="text-zinc-400 mt-4 text-base sm:text-lg">We diagnose structural bottlenecks, design actionable roadmaps, and implement bulletproof digital and operational systems.</p>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 sm:gap-10">
                    <!-- Service Card 1 -->
                    <div class="bg-brand-charcoal p-8 sm:p-10 rounded-3xl border border-white/10 hover:border-brand-coral/60 transition-all group hover:-translate-y-1.5 flex flex-col justify-between">
                        <div>
                            <div class="w-16 h-16 rounded-2xl bg-brand-coral/10 border border-brand-coral/30 flex items-center justify-center text-brand-coral text-3xl mb-8 group-hover:bg-brand-coral group-hover:text-white transition-all">
                                <i class="fa-solid fa-lightbulb"></i>
                            </div>
                            <h3 class="text-2xl font-bold text-white mb-4">Corporate Growth Strategy</h3>
                            <p class="text-zinc-400 text-base leading-relaxed mb-8">Comprehensive market positioning, scaling strategy, and business model optimization for high-growth firms.</p>
                        </div>
                        <button onclick="navigateTo('services')" class="text-brand-coral font-bold text-base inline-flex items-center gap-2 group-hover:translate-x-1 transition-transform">
                            Explore Capabilities <i class="fa-solid fa-chevron-right text-xs"></i>
                        </button>
                    </div>

                    <!-- Service Card 2 -->
                    <div class="bg-brand-charcoal p-8 sm:p-10 rounded-3xl border border-white/10 hover:border-brand-coral/60 transition-all group hover:-translate-y-1.5 flex flex-col justify-between">
                        <div>
                            <div class="w-16 h-16 rounded-2xl bg-brand-coral/10 border border-brand-coral/30 flex items-center justify-center text-brand-coral text-3xl mb-8 group-hover:bg-brand-coral group-hover:text-white transition-all">
                                <i class="fa-solid fa-laptop-code"></i>
                            </div>
                            <h3 class="text-2xl font-bold text-white mb-4">Digital Transformation</h3>
                            <p class="text-zinc-400 text-base leading-relaxed mb-8">Modernizing software stacks, automation workflows, and customer experience funnels for high conversions.</p>
                        </div>
                        <button onclick="navigateTo('services')" class="text-brand-coral font-bold text-base inline-flex items-center gap-2 group-hover:translate-x-1 transition-transform">
                            Explore Capabilities <i class="fa-solid fa-chevron-right text-xs"></i>
                        </button>
                    </div>

                    <!-- Service Card 3 -->
                    <div class="bg-brand-charcoal p-8 sm:p-10 rounded-3xl border border-white/10 hover:border-brand-coral/60 transition-all group hover:-translate-y-1.5 flex flex-col justify-between">
                        <div>
                            <div class="w-16 h-16 rounded-2xl bg-brand-coral/10 border border-brand-coral/30 flex items-center justify-center text-brand-coral text-3xl mb-8 group-hover:bg-brand-coral group-hover:text-white transition-all">
                                <i class="fa-solid fa-sliders"></i>
                            </div>
                            <h3 class="text-2xl font-bold text-white mb-4">Operations & Revenue Ops</h3>
                            <p class="text-zinc-400 text-base leading-relaxed mb-8">Eliminating process friction, aligning marketing with sales, and building repeatable revenue channels.</p>
                        </div>
                        <button onclick="navigateTo('services')" class="text-brand-coral font-bold text-base inline-flex items-center gap-2 group-hover:translate-x-1 transition-transform">
                            Explore Capabilities <i class="fa-solid fa-chevron-right text-xs"></i>
                        </button>
                    </div>
                </div>
            </div>

            <!-- FEATURED TESTIMONIAL PREVIEW -->
            <div class="py-20 bg-brand-surface/40 border-y border-white/5">
                <div class="max-w-8xl mx-auto px-4 sm:px-6 lg:px-12">
                    <div class="flex flex-col md:flex-row justify-between items-start md:items-end mb-14 gap-4">
                        <div>
                            <span class="text-brand-coral font-bold text-sm sm:text-base tracking-widest uppercase">Verified Client Reviews</span>
                            <h2 class="text-3xl sm:text-4xl font-extrabold text-white mt-2">What Executive Leaders Say</h2>
                        </div>
                        <button onclick="navigateTo('testimonials')" class="text-brand-coral hover:text-white font-bold text-base flex items-center gap-2 group">
                            <span>View All Verified Reviews</span>
                            <i class="fa-solid fa-arrow-right group-hover:translate-x-1 transition-transform"></i>
                        </button>
                    </div>

                    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8" id="homeReviewsContainer">
                        <!-- Populated via JS dynamically -->
                    </div>
                </div>
            </div>
        </section>

        <!-- ========================================================================= -->
        <!-- PAGE 2: ABOUT US -->
        <!-- ========================================================================= -->
        <section id="page-about" class="page-view hidden">
            <div class="py-20 max-w-8xl mx-auto px-4 sm:px-6 lg:px-12">
                <!-- Page Title Header -->
                <div class="text-center max-w-4xl mx-auto mb-20">
                    <span class="text-brand-coral font-bold text-sm sm:text-base tracking-widest uppercase">About Noble Consultant</span>
                    <h1 class="text-4xl sm:text-5xl lg:text-6xl font-extrabold text-white mt-3">Precision Strategy for Ambitious Leaders</h1>
                    <p class="text-zinc-400 mt-4 text-base sm:text-xl leading-relaxed">Built on principles of transparency, analytical rigor, and sustainable enterprise scale.</p>
                </div>

                <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 lg:gap-16 items-center mb-24">
                    <!-- Photo Left -->
                    <div class="lg:col-span-5 flex justify-center">
                        <div class="relative w-full max-w-md rounded-3xl overflow-hidden border-2 border-brand-coral/40 shadow-2xl bg-brand-charcoal">
                            <img src="image_0b0f18.jpg" alt="Noble Consultant Founder" class="w-full h-auto object-cover" onerror="this.onerror=null; this.src='https://placehold.co/700x850/18181b/ffffff?text=Noble+Consultant+Advisor'">
                            <div class="p-6 bg-brand-charcoal border-t border-white/10 text-center">
                                <h3 class="text-xl font-bold text-white">Founder & Chief Consultant</h3>
                                <p class="text-sm text-brand-coral font-semibold">Noble Consultant Advisory</p>
                            </div>
                        </div>
                    </div>

                    <!-- Story Right -->
                    <div class="lg:col-span-7 space-y-6 sm:space-y-8">
                        <h2 class="text-3xl sm:text-4xl font-extrabold text-white">Empowering Enterprise Scale Through Principled Advisory</h2>
                        <p class="text-zinc-300 text-base sm:text-lg leading-relaxed">At <strong class="text-white">Noble Consultant</strong>, we believe every enterprise possesses untapped potential that can be unlocked through structured planning, optimized workflows, and modern execution.</p>
                        <p class="text-zinc-400 text-base sm:text-lg leading-relaxed">We step into your organization not as external vendors, but as strategic partners deeply committed to measurable ROI. Our holistic approach bridges high-level executive strategy with hands-on implementation.</p>
                        
                        <div class="grid grid-cols-1 sm:grid-cols-2 gap-6 pt-4">
                            <div class="p-6 rounded-2xl bg-brand-charcoal border border-white/10">
                                <i class="fa-solid fa-bullseye text-brand-coral text-3xl mb-3"></i>
                                <h4 class="font-bold text-white text-lg">Our Mission</h4>
                                <p class="text-sm text-zinc-400 mt-2 leading-relaxed">To deliver clear, actionable, and scalable business advisory that drives repeatable revenue growth.</p>
                            </div>
                            <div class="p-6 rounded-2xl bg-brand-charcoal border border-white/10">
                                <i class="fa-solid fa-eye text-brand-coral text-3xl mb-3"></i>
                                <h4 class="font-bold text-white text-lg">Our Vision</h4>
                                <p class="text-sm text-zinc-400 mt-2 leading-relaxed">To be the most trusted strategic advisory firm for forward-thinking enterprises and scaling founders.</p>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Core Values -->
                <div class="py-16 bg-brand-charcoal rounded-3xl p-8 sm:p-14 border border-white/10">
                    <h3 class="text-3xl font-extrabold text-white text-center mb-12">Our Core Principles</h3>
                    <div class="grid grid-cols-1 md:grid-cols-3 gap-10">
                        <div class="text-center space-y-4">
                            <div class="w-14 h-14 rounded-full bg-brand-coral/20 text-brand-coral flex items-center justify-center mx-auto text-2xl font-bold">1</div>
                            <h4 class="text-xl font-bold text-white">Uncompromising Integrity</h4>
                            <p class="text-sm text-zinc-400 leading-relaxed">Direct recommendations with zero fluff. Honest, transparent advice centered strictly around your ROI.</p>
                        </div>
                        <div class="text-center space-y-4">
                            <div class="w-14 h-14 rounded-full bg-brand-coral/20 text-brand-coral flex items-center justify-center mx-auto text-2xl font-bold">2</div>
                            <h4 class="text-xl font-bold text-white">Data-Driven Execution</h4>
                            <p class="text-sm text-zinc-400 leading-relaxed">Every strategic roadmap is grounded in rigorous financial analytics and realistic market benchmarks.</p>
                        </div>
                        <div class="text-center space-y-4">
                            <div class="w-14 h-14 rounded-full bg-brand-coral/20 text-brand-coral flex items-center justify-center mx-auto text-2xl font-bold">3</div>
                            <h4 class="text-xl font-bold text-white">Long-term Partnership</h4>
                            <p class="text-sm text-zinc-400 leading-relaxed">We stay aligned during implementation to ensure your teams maintain long-term momentum.</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- ========================================================================= -->
        <!-- PAGE 3: SERVICES -->
        <!-- ========================================================================= -->
        <section id="page-services" class="page-view hidden">
            <div class="py-20 max-w-8xl mx-auto px-4 sm:px-6 lg:px-12">
                <div class="text-center max-w-4xl mx-auto mb-20">
                    <span class="text-brand-coral font-bold text-sm sm:text-base tracking-widest uppercase">Consulting Capabilities</span>
                    <h1 class="text-4xl sm:text-5xl lg:text-6xl font-extrabold text-white mt-3">Services Built for Enterprise Scale</h1>
                    <p class="text-zinc-400 mt-4 text-base sm:text-xl">Explore our modular consultancy offerings designed for scaling startups, corporate modernization, and revenue operational efficiency.</p>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 sm:gap-10">
                    <!-- Service 1 -->
                    <div class="bg-brand-charcoal rounded-3xl p-8 sm:p-10 border border-white/10 hover:border-brand-coral transition-all flex flex-col justify-between">
                        <div>
                            <div class="w-14 h-14 rounded-2xl bg-brand-coral/10 text-brand-coral flex items-center justify-center text-2xl mb-8">
                                <i class="fa-solid fa-chess"></i>
                            </div>
                            <h3 class="text-2xl font-bold text-white mb-4">Executive Advisory</h3>
                            <p class="text-zinc-400 text-base leading-relaxed mb-8">Strategic alignment for founders and leadership teams. Quarterly planning, market entry analysis, and unit-economics optimization.</p>
                            <ul class="space-y-3 text-sm text-zinc-300 mb-8">
                                <li class="flex items-center gap-3"><i class="fa-solid fa-check text-brand-coral"></i> Go-to-Market Strategy</li>
                                <li class="flex items-center gap-3"><i class="fa-solid fa-check text-brand-coral"></i> Business Model Innovation</li>
                                <li class="flex items-center gap-3"><i class="fa-solid fa-check text-brand-coral"></i> Unit Economics & Pricing</li>
                            </ul>
                        </div>
                        <button onclick="navigateTo('contact')" class="w-full py-4 rounded-2xl bg-white/5 hover:bg-brand-coral text-white font-bold text-base transition-colors">Inquire Service</button>
                    </div>

                    <!-- Service 2 -->
                    <div class="bg-brand-charcoal rounded-3xl p-8 sm:p-10 border border-white/10 hover:border-brand-coral transition-all flex flex-col justify-between">
                        <div>
                            <div class="w-14 h-14 rounded-2xl bg-brand-coral/10 text-brand-coral flex items-center justify-center text-2xl mb-8">
                                <i class="fa-solid fa-network-wired"></i>
                            </div>
                            <h3 class="text-2xl font-bold text-white mb-4">Digital Systems & Automation</h3>
                            <p class="text-zinc-400 text-base leading-relaxed mb-8">Streamline customer acquisition and back-office operations with custom software integrations, CRM workflows, and automation.</p>
                            <ul class="space-y-3 text-sm text-zinc-300 mb-8">
                                <li class="flex items-center gap-3"><i class="fa-solid fa-check text-brand-coral"></i> CRM & Sales Pipeline Setup</li>
                                <li class="flex items-center gap-3"><i class="fa-solid fa-check text-brand-coral"></i> Workflow Automation</li>
                                <li class="flex items-center gap-3"><i class="fa-solid fa-check text-brand-coral"></i> Customer Journey Engineering</li>
                            </ul>
                        </div>
                        <button onclick="navigateTo('contact')" class="w-full py-4 rounded-2xl bg-white/5 hover:bg-brand-coral text-white font-bold text-base transition-colors">Inquire Service</button>
                    </div>

                    <!-- Service 3 -->
                    <div class="bg-brand-charcoal rounded-3xl p-8 sm:p-10 border border-white/10 hover:border-brand-coral transition-all flex flex-col justify-between">
                        <div>
                            <div class="w-14 h-14 rounded-2xl bg-brand-coral/10 text-brand-coral flex items-center justify-center text-2xl mb-8">
                                <i class="fa-solid fa-bullhorn"></i>
                            </div>
                            <h3 class="text-2xl font-bold text-white mb-4">Brand Positioning</h3>
                            <p class="text-zinc-400 text-base leading-relaxed mb-8">Elevate your brand image to command premium market pricing. Messaging alignment, corporate identity, and collateral strategy.</p>
                            <ul class="space-y-3 text-sm text-zinc-300 mb-8">
                                <li class="flex items-center gap-3"><i class="fa-solid fa-check text-brand-coral"></i> Brand Architecture</li>
                                <li class="flex items-center gap-3"><i class="fa-solid fa-check text-brand-coral"></i> Value Proposition Refining</li>
                                <li class="flex items-center gap-3"><i class="fa-solid fa-check text-brand-coral"></i> Pitch Deck & Collateral Strategy</li>
                            </ul>
                        </div>
                        <button onclick="navigateTo('contact')" class="w-full py-4 rounded-2xl bg-white/5 hover:bg-brand-coral text-white font-bold text-base transition-colors">Inquire Service</button>
                    </div>
                </div>

                <!-- Interactive Quote Calculator Section -->
                <div class="mt-24 p-8 sm:p-12 rounded-3xl bg-gradient-to-r from-brand-charcoal to-brand-surface border border-white/10">
                    <div class="max-w-3xl mx-auto text-center">
                        <h3 class="text-3xl font-extrabold text-white mb-3">Instant Engagement Estimator</h3>
                        <p class="text-sm text-zinc-400 mb-10">Select your primary consulting objectives to estimate scope and investment.</p>

                        <div class="space-y-6 text-left">
                            <div>
                                <label class="block text-xs font-bold text-zinc-300 uppercase tracking-wider mb-2">Primary Objective:</label>
                                <select id="calcObjective" onchange="calculateEstimate()" class="w-full bg-brand-dark border border-white/20 rounded-2xl p-4 text-white text-base focus:border-brand-coral focus:outline-none">
                                    <option value="3000">Strategy Roadmap & Business Audit ($3,000)</option>
                                    <option value="5500">Digital Systems & Automation Buildout ($5,500)</option>
                                    <option value="8000">Full Enterprise Transformation ($8,000)</option>
                                </select>
                            </div>

                            <div>
                                <label class="block text-xs font-bold text-zinc-300 uppercase tracking-wider mb-2">Estimated Timeline / Duration:</label>
                                <select id="calcDuration" onchange="calculateEstimate()" class="w-full bg-brand-dark border border-white/20 rounded-2xl p-4 text-white text-base focus:border-brand-coral focus:outline-none">
                                    <option value="1">1 Month Sprint (Standard)</option>
                                    <option value="1.8">3 Months Deep Advisory (10% Savings)</option>
                                    <option value="3">6 Months Enterprise Retainer (15% Savings)</option>
                                </select>
                            </div>

                            <div class="pt-8 border-t border-white/10 flex flex-col sm:flex-row items-center justify-between gap-6">
                                <div>
                                    <p class="text-xs text-zinc-400 uppercase font-bold tracking-wider">Estimated Engagement Investment:</p>
                                    <p class="text-4xl font-extrabold text-brand-coral mt-1" id="calcTotal">$3,000 USD</p>
                                </div>
                                <button onclick="navigateTo('contact')" class="w-full sm:w-auto nc-coral-gradient text-white px-8 py-4 rounded-2xl text-base font-bold shadow-lg hover:scale-105 transition-transform">
                                    Lock In Estimate
                                </button>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- ========================================================================= -->
        <!-- PAGE 4: PROJECTS / CASE STUDIES -->
        <!-- ========================================================================= -->
        <section id="page-projects" class="page-view hidden">
            <div class="py-20 max-w-8xl mx-auto px-4 sm:px-6 lg:px-12">
                <div class="text-center max-w-4xl mx-auto mb-20">
                    <span class="text-brand-coral font-bold text-sm sm:text-base tracking-widest uppercase">Proven Outcomes</span>
                    <h1 class="text-4xl sm:text-5xl lg:text-6xl font-extrabold text-white mt-3">Case Studies & Impact</h1>
                    <p class="text-zinc-400 mt-4 text-base sm:text-xl">A selection of recent enterprise engagements facilitated by Noble Consultant.</p>
                </div>

                <div class="grid grid-cols-1 lg:grid-cols-2 gap-10">
                    <!-- Case Study 1 -->
                    <div class="bg-brand-charcoal rounded-3xl overflow-hidden border border-white/10 hover:border-brand-coral transition-all">
                        <div class="p-8 sm:p-12">
                            <span class="px-4 py-1.5 rounded-full bg-brand-coral/10 text-brand-coral text-xs font-bold uppercase tracking-wider">SaaS & FinTech</span>
                            <h3 class="text-3xl font-extrabold text-white mt-5">Scalable B2B Funnel Redesign</h3>
                            <p class="text-zinc-400 text-base mt-4 leading-relaxed">Streamlined corporate client onboarding and sales collateral for a financial technology provider.</p>
                            <div class="mt-8 pt-8 border-t border-white/10 grid grid-cols-3 gap-4 text-center">
                                <div>
                                    <p class="text-2xl sm:text-3xl font-extrabold text-brand-coral">+140%</p>
                                    <p class="text-xs text-zinc-400 mt-1">Conversion Growth</p>
                                </div>
                                <div>
                                    <p class="text-2xl sm:text-3xl font-extrabold text-white">14 Days</p>
                                    <p class="text-xs text-zinc-400 mt-1">Sales Cycle Reduced</p>
                                </div>
                                <div>
                                    <p class="text-2xl sm:text-3xl font-extrabold text-brand-coral">$2.4M</p>
                                    <p class="text-xs text-zinc-400 mt-1">Pipeline Added</p>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- Case Study 2 -->
                    <div class="bg-brand-charcoal rounded-3xl overflow-hidden border border-white/10 hover:border-brand-coral transition-all">
                        <div class="p-8 sm:p-12">
                            <span class="px-4 py-1.5 rounded-full bg-brand-coral/10 text-brand-coral text-xs font-bold uppercase tracking-wider">Retail & Commerce</span>
                            <h3 class="text-3xl font-extrabold text-white mt-5">Omnichannel Revenue Strategy</h3>
                            <p class="text-zinc-400 text-base mt-4 leading-relaxed">Unified regional retail operations with automated inventory and multi-location digital marketing campaigns.</p>
                            <div class="mt-8 pt-8 border-t border-white/10 grid grid-cols-3 gap-4 text-center">
                                <div>
                                    <p class="text-2xl sm:text-3xl font-extrabold text-brand-coral">3.2x</p>
                                    <p class="text-xs text-zinc-400 mt-1">ROI Achieved</p>
                                </div>
                                <div>
                                    <p class="text-2xl sm:text-3xl font-extrabold text-white">35%</p>
                                    <p class="text-xs text-zinc-400 mt-1">Cost Savings</p>
                                </div>
                                <div>
                                    <p class="text-2xl sm:text-3xl font-extrabold text-brand-coral">100k+</p>
                                    <p class="text-xs text-zinc-400 mt-1">New Customers</p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- ========================================================================= -->
        <!-- PAGE 5: TESTIMONIALS / REVIEWS -->
        <!-- ========================================================================= -->
        <section id="page-testimonials" class="page-view hidden">
            <div class="py-20 max-w-8xl mx-auto px-4 sm:px-6 lg:px-12">
                <div class="text-center max-w-4xl mx-auto mb-20">
                    <span class="text-brand-coral font-bold text-sm sm:text-base tracking-widest uppercase">Client Testimonials</span>
                    <h1 class="text-4xl sm:text-5xl lg:text-6xl font-extrabold text-white mt-3">Wall of Trust & Reviews</h1>
                    <p class="text-zinc-400 mt-4 text-base sm:text-xl">Read full accounts from business owners, managing directors, and partners who work with Noble Consultant.</p>
                </div>

                <!-- 6 Full Testimonials Desktop Grid -->
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8" id="fullReviewsContainer">
                    <!-- Javascript populates 6 distinct client reviews -->
                </div>
            </div>
        </section>

        <!-- ========================================================================= -->
        <!-- PAGE 6: PRICING -->
        <!-- ========================================================================= -->
        <section id="page-pricing" class="page-view hidden">
            <div class="py-20 max-w-8xl mx-auto px-4 sm:px-6 lg:px-12">
                <div class="text-center max-w-4xl mx-auto mb-20">
                    <span class="text-brand-coral font-bold text-sm sm:text-base tracking-widest uppercase">Transparent Pricing</span>
                    <h1 class="text-4xl sm:text-5xl lg:text-6xl font-extrabold text-white mt-3">Consultancy Engagement Tiers</h1>
                    <p class="text-zinc-400 mt-4 text-base sm:text-xl">Select the scope that matches your business maturity and growth objectives.</p>
                </div>

                <div class="grid grid-cols-1 lg:grid-cols-3 gap-8 lg:gap-10">
                    <!-- Tier 1 -->
                    <div class="bg-brand-charcoal p-8 sm:p-10 rounded-3xl border border-white/10 flex flex-col justify-between">
                        <div>
                            <span class="text-zinc-400 font-bold text-xs uppercase tracking-wider">Advisory Sprint</span>
                            <h3 class="text-3xl font-extrabold text-white mt-3">Strategic Audit</h3>
                            <p class="text-zinc-400 text-sm mt-2">Ideal for diagnosing business operational flaws.</p>
                            <div class="my-8">
                                <span class="text-5xl font-extrabold text-white">$2,500</span>
                                <span class="text-zinc-400 text-base"> / engagement</span>
                            </div>
                            <ul class="space-y-4 text-base text-zinc-300">
                                <li class="flex items-center gap-3"><i class="fa-solid fa-check text-brand-coral"></i> Full Process & Growth Audit</li>
                                <li class="flex items-center gap-3"><i class="fa-solid fa-check text-brand-coral"></i> Executive Strategy Blueprint</li>
                                <li class="flex items-center gap-3"><i class="fa-solid fa-check text-brand-coral"></i> 2x Live Advisory Workshops</li>
                            </ul>
                        </div>
                        <button onclick="navigateTo('contact')" class="mt-10 w-full py-4 rounded-2xl bg-white/10 hover:bg-brand-coral text-white font-bold text-base transition-colors">Select Tier</button>
                    </div>

                    <!-- Tier 2 - Featured -->
                    <div class="bg-brand-surface p-8 sm:p-10 rounded-3xl border-2 border-brand-coral relative flex flex-col justify-between nc-glow">
                        <div class="absolute -top-4 left-1/2 -translate-x-1/2 bg-brand-coral text-white text-xs font-extrabold uppercase px-5 py-1.5 rounded-full tracking-wider">
                            Most Popular Choice
                        </div>
                        <div>
                            <span class="text-brand-coral font-bold text-xs uppercase tracking-wider">Growth Acceleration</span>
                            <h3 class="text-3xl font-extrabold text-white mt-3">Noble System Implement</h3>
                            <p class="text-zinc-400 text-sm mt-2">Complete system restructuring & digital transformation.</p>
                            <div class="my-8">
                                <span class="text-5xl font-extrabold text-white">$5,800</span>
                                <span class="text-zinc-400 text-base"> / month</span>
                            </div>
                            <ul class="space-y-4 text-base text-zinc-300">
                                <li class="flex items-center gap-3"><i class="fa-solid fa-check text-brand-coral"></i> Everything in Audit Tier</li>
                                <li class="flex items-center gap-3"><i class="fa-solid fa-check text-brand-coral"></i> CRM & Tech Stack Re-building</li>
                                <li class="flex items-center gap-3"><i class="fa-solid fa-check text-brand-coral"></i> Dedicated Lead Strategic Consultant</li>
                                <li class="flex items-center gap-3"><i class="fa-solid fa-check text-brand-coral"></i> Weekly Operations Reviews</li>
                            </ul>
                        </div>
                        <button onclick="navigateTo('contact')" class="mt-10 w-full py-4 rounded-2xl nc-coral-gradient text-white font-bold text-base shadow-lg hover:scale-[1.02] transition-all">Partner With Us</button>
                    </div>

                    <!-- Tier 3 -->
                    <div class="bg-brand-charcoal p-8 sm:p-10 rounded-3xl border border-white/10 flex flex-col justify-between">
                        <div>
                            <span class="text-zinc-400 font-bold text-xs uppercase tracking-wider">Enterprise Advisory</span>
                            <h3 class="text-3xl font-extrabold text-white mt-3">Retainer Partner</h3>
                            <p class="text-zinc-400 text-sm mt-2">Continuous executive advisory and fractional CSO.</p>
                            <div class="my-8">
                                <span class="text-5xl font-extrabold text-white">Custom</span>
                            </div>
                            <ul class="space-y-4 text-base text-zinc-300">
                                <li class="flex items-center gap-3"><i class="fa-solid fa-check text-brand-coral"></i> Board-level Advisory</li>
                                <li class="flex items-center gap-3"><i class="fa-solid fa-check text-brand-coral"></i> Direct SLA & On-demand Calls</li>
                                <li class="flex items-center gap-3"><i class="fa-solid fa-check text-brand-coral"></i> Custom Systems Engineering</li>
                            </ul>
                        </div>
                        <button onclick="navigateTo('contact')" class="mt-10 w-full py-4 rounded-2xl bg-white/10 hover:bg-brand-coral text-white font-bold text-base transition-colors">Inquire Enterprise</button>
                    </div>
                </div>
            </div>
        </section>

        <!-- ========================================================================= -->
        <!-- PAGE 7: CONTACT -->
        <!-- ========================================================================= -->
        <section id="page-contact" class="page-view hidden">
            <div class="py-20 max-w-8xl mx-auto px-4 sm:px-6 lg:px-12">
                <div class="text-center max-w-4xl mx-auto mb-20">
                    <span class="text-brand-coral font-bold text-sm sm:text-base tracking-widest uppercase">Start The Conversation</span>
                    <h1 class="text-4xl sm:text-5xl lg:text-6xl font-extrabold text-white mt-3">Connect With Noble Consultant</h1>
                    <p class="text-zinc-400 mt-4 text-base sm:text-xl">Schedule your initial consultation or send us your strategic inquiry.</p>
                </div>

                <div class="grid grid-cols-1 lg:grid-cols-12 gap-12">
                    <!-- Contact Form Left -->
                    <div class="lg:col-span-7 bg-brand-charcoal p-8 sm:p-12 rounded-3xl border border-white/10">
                        <form id="contactForm" onsubmit="handleFormSubmit(event)" class="space-y-6">
                            <div class="grid grid-cols-1 sm:grid-cols-2 gap-6">
                                <div>
                                    <label class="block text-xs font-bold text-zinc-300 uppercase tracking-wider mb-2">Full Name *</label>
                                    <input type="text" required placeholder="e.g. David Miller" class="w-full bg-brand-dark border border-white/15 rounded-2xl p-4 text-white text-base focus:border-brand-coral focus:outline-none">
                                </div>
                                <div>
                                    <label class="block text-xs font-bold text-zinc-300 uppercase tracking-wider mb-2">Work Email *</label>
                                    <input type="email" required placeholder="david@company.com" class="w-full bg-brand-dark border border-white/15 rounded-2xl p-4 text-white text-base focus:border-brand-coral focus:outline-none">
                                </div>
                            </div>

                            <div class="grid grid-cols-1 sm:grid-cols-2 gap-6">
                                <div>
                                    <label class="block text-xs font-bold text-zinc-300 uppercase tracking-wider mb-2">Company / Organization</label>
                                    <input type="text" placeholder="Your Business Name" class="w-full bg-brand-dark border border-white/15 rounded-2xl p-4 text-white text-base focus:border-brand-coral focus:outline-none">
                                </div>
                                <div>
                                    <label class="block text-xs font-bold text-zinc-300 uppercase tracking-wider mb-2">Primary Interest</label>
                                    <select class="w-full bg-brand-dark border border-white/15 rounded-2xl p-4 text-white text-base focus:border-brand-coral focus:outline-none">
                                        <option>Growth Strategy</option>
                                        <option>Digital Automation</option>
                                        <option>Brand Alignment</option>
                                        <option>General Advisory</option>
                                    </select>
                                </div>
                            </div>

                            <div>
                                <label class="block text-xs font-bold text-zinc-300 uppercase tracking-wider mb-2">Project Details & Goals *</label>
                                <textarea rows="5" required placeholder="Tell us briefly about your current operations and goals..." class="w-full bg-brand-dark border border-white/15 rounded-2xl p-4 text-white text-base focus:border-brand-coral focus:outline-none"></textarea>
                            </div>

                            <button type="submit" class="w-full nc-coral-gradient text-white py-5 rounded-2xl font-bold text-lg hover:opacity-95 transition-all shadow-xl">
                                Send Strategic Inquiry
                            </button>
                        </form>
                    </div>

                    <!-- Contact Details Right -->
                    <div class="lg:col-span-5 space-y-8">
                        <div class="bg-brand-charcoal p-8 sm:p-10 rounded-3xl border border-white/10 space-y-8">
                            <h3 class="text-2xl font-bold text-white">Direct Office Contacts</h3>
                            
                            <div class="flex items-start gap-5">
                                <div class="w-12 h-12 rounded-2xl bg-brand-coral/10 text-brand-coral flex items-center justify-center text-xl shrink-0">
                                    <i class="fa-solid fa-envelope"></i>
                                </div>
                                <div>
                                    <p class="text-xs text-zinc-400 font-bold uppercase tracking-wider">Official Email</p>
                                    <p class="text-base sm:text-lg font-semibold text-white mt-1">contact@nobleconsultant.com</p>
                                </div>
                            </div>

                            <div class="flex items-start gap-5">
                                <div class="w-12 h-12 rounded-2xl bg-brand-coral/10 text-brand-coral flex items-center justify-center text-xl shrink-0">
                                    <i class="fa-solid fa-phone"></i>
                                </div>
                                <div>
                                    <p class="text-xs text-zinc-400 font-bold uppercase tracking-wider">Direct Advisory Line</p>
                                    <p class="text-base sm:text-lg font-semibold text-white mt-1">+1 (800) 555-NOBLE</p>
                                </div>
                            </div>

                            <div class="flex items-start gap-5">
                                <div class="w-12 h-12 rounded-2xl bg-brand-coral/10 text-brand-coral flex items-center justify-center text-xl shrink-0">
                                    <i class="fa-solid fa-location-dot"></i>
                                </div>
                                <div>
                                    <p class="text-xs text-zinc-400 font-bold uppercase tracking-wider">Headquarters</p>
                                    <p class="text-base sm:text-lg font-semibold text-white mt-1">Financial District, Strategy Hub</p>
                                </div>
                            </div>
                        </div>

                        <!-- Founder Callout Card -->
                        <div class="bg-gradient-to-br from-brand-charcoal to-brand-surface p-8 rounded-3xl border border-brand-coral/40 flex items-center gap-5">
                            <img src="image_0b0f18.jpg" alt="Noble Consultant Founder" class="w-20 h-20 rounded-2xl object-cover border border-white/20 shrink-0" onerror="this.onerror=null; this.src='https://placehold.co/100x100/18181b/ffffff?text=Noble'">
                            <div>
                                <h4 class="text-base sm:text-lg font-bold text-white">Direct Advisory Guarantee</h4>
                                <p class="text-xs sm:text-sm text-zinc-400 mt-1">All incoming inquiries are reviewed personally by our lead advisory team within 24 hours.</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <!-- FOOTER -->
    <footer class="bg-brand-charcoal border-t border-white/10 pt-20 pb-12 mt-20">
        <div class="max-w-8xl mx-auto px-4 sm:px-6 lg:px-12">
            <div class="grid grid-cols-1 md:grid-cols-12 gap-10 pb-16 border-b border-white/10">
                <!-- Brand Info -->
                <div class="md:col-span-5 space-y-5">
                    <div class="flex items-center gap-3">
                        <div class="w-11 h-11 bg-black rounded-xl border border-white/20 p-1 flex flex-col justify-center items-center">
                            <div class="flex items-center text-xl font-extrabold leading-none">
                                <span class="text-white">N</span>
                                <span class="text-brand-coral">C</span>
                            </div>
                            <span class="text-[7px] text-white/70 font-semibold tracking-widest">NOBLE</span>
                        </div>
                        <span class="text-xl font-bold text-white">NOBLE CONSULTANT</span>
                    </div>
                    <p class="text-sm text-zinc-400 leading-relaxed max-w-md">
                        High-stakes strategy, digital transformation, and growth advisory engineered for scaling business enterprises worldwide.
                    </p>
                </div>

                <!-- Navigation Quicklinks -->
                <div class="md:col-span-3 space-y-4">
                    <p class="text-xs font-bold uppercase text-white tracking-widest">Navigation</p>
                    <ul class="space-y-3 text-sm text-zinc-400">
                        <li><a href="#" onclick="navigateTo('home'); return false;" class="hover:text-brand-coral transition-colors">Home</a></li>
                        <li><a href="#" onclick="navigateTo('about'); return false;" class="hover:text-brand-coral transition-colors">About Us</a></li>
                        <li><a href="#" onclick="navigateTo('services'); return false;" class="hover:text-brand-coral transition-colors">Capabilities</a></li>
                        <li><a href="#" onclick="navigateTo('projects'); return false;" class="hover:text-brand-coral transition-colors">Case Studies</a></li>
                        <li><a href="#" onclick="navigateTo('testimonials'); return false;" class="hover:text-brand-coral transition-colors">Client Reviews</a></li>
                        <li><a href="#" onclick="navigateTo('pricing'); return false;" class="hover:text-brand-coral transition-colors">Pricing Tiers</a></li>
                    </ul>
                </div>

                <!-- Socials & Legal -->
                <div class="md:col-span-4 space-y-4">
                    <p class="text-xs font-bold uppercase text-white tracking-widest">Connect With Us</p>
                    <div class="flex gap-4">
                        <a href="#" class="w-11 h-11 rounded-2xl bg-white/5 hover:bg-brand-coral text-white flex items-center justify-center transition-colors text-lg"><i class="fa-brands fa-linkedin-in"></i></a>
                        <a href="#" class="w-11 h-11 rounded-2xl bg-white/5 hover:bg-brand-coral text-white flex items-center justify-center transition-colors text-lg"><i class="fa-brands fa-x-twitter"></i></a>
                        <a href="#" class="w-11 h-11 rounded-2xl bg-white/5 hover:bg-brand-coral text-white flex items-center justify-center transition-colors text-lg"><i class="fa-brands fa-facebook-f"></i></a>
                    </div>
                </div>
            </div>

            <div class="pt-8 flex flex-col sm:flex-row justify-between items-center text-xs sm:text-sm text-zinc-500 gap-4">
                <p>&copy; 2026 Noble Consultant. All Rights Reserved.</p>
                <div class="flex gap-8">
                    <a href="#" class="hover:text-zinc-300 transition-colors">Privacy Policy</a>
                    <a href="#" class="hover:text-zinc-300 transition-colors">Terms of Service</a>
                </div>
            </div>
        </div>
    </footer>

    <!-- SCRIPT LOGIC -->
    <script>
        // Client reviews dataset
        const clientReviews = [
            {
                name: "Marcus Vance",
                role: "Chief Executive Officer",
                company: "Vance Logistics Group",
                avatar: "https://images.unsplash.com/photo-1534528741775-53994a69daeb?w=150&auto=format&fit=crop&q=80",
                stars: 5,
                text: "Noble Consultant transformed our entire client acquisition pipeline. The strategy provided gave us total clarity on unit economics and elevated our ROI by over 140% in under six months!"
            },
            {
                name: "Elena Rostova",
                role: "Operations Director",
                company: "Apex Global FinTech",
                avatar: "https://images.unsplash.com/photo-1580489944761-15a19d654956?w=150&auto=format&fit=crop&q=80",
                stars: 5,
                text: "Working directly with the Noble Consultant team felt like unlocking a cheat code for our growth. Their operational automation setup saved us over 30 hours per week across our teams."
            },
            {
                name: "Dr. Samuel O'Connor",
                role: "Managing Partner",
                company: "O'Connor Capital",
                avatar: "https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?w=150&auto=format&fit=crop&q=80",
                stars: 5,
                text: "The brand repositioning and executive advisory delivered by Noble Consultant allowed us to command premium retainer rates with enterprise clients. Absolutely top-tier service!"
            },
            {
                name: "Sophia Martinez",
                role: "Founder & Product Lead",
                company: "Luminary Health",
                avatar: "https://images.unsplash.com/photo-1573496359142-b8d87734a5a2?w=150&auto=format&fit=crop&q=80",
                stars: 5,
                text: "Noble Consultant's structured approach restored our leadership team's alignment. They don't just supply theories; they guide execution step-by-step."
            },
            {
                name: "David Chen",
                role: "VP of Business Development",
                company: "Krypton Systems",
                avatar: "https://images.unsplash.com/photo-1500648767791-00dcc994a43e?w=150&auto=format&fit=crop&q=80",
                stars: 5,
                text: "Exceptional advisory. Their deep knowledge of sales operations and modern digital funnels resulted in our highest quarterly performance in company history."
            },
            {
                name: "Amara Nwosu",
                role: "Head of Marketing",
                company: "Aura Commerce",
                avatar: "https://images.unsplash.com/photo-1531746020798-e6953c6e8e04?w=150&auto=format&fit=crop&q=80",
                stars: 5,
                text: "The level of professionalism and integrity from Noble Consultant is unmatched. The customized growth roadmap exceeded every metric we set."
            }
        ];

        // Multi-page Router Function
        function navigateTo(pageId) {
            const pages = document.querySelectorAll('.page-view');
            pages.forEach(page => page.classList.add('hidden'));

            const targetPage = document.getElementById(`page-${pageId}`);
            if(targetPage) {
                targetPage.classList.remove('hidden');
            }

            const navLinks = document.querySelectorAll('.nav-link');
            navLinks.forEach(link => {
                if(link.getAttribute('data-page') === pageId) {
                    link.classList.add('text-brand-coral', 'bg-white/5');
                    link.classList.remove('text-white/80');
                } else {
                    link.classList.remove('text-brand-coral', 'bg-white/5');
                    link.classList.add('text-white/80');
                }
            });

            window.scrollTo({ top: 0, behavior: 'smooth' });
        }

        // Toggle Mobile Navigation Drawer
        function toggleMobileMenu() {
            const menu = document.getElementById('mobileMenu');
            menu.classList.toggle('hidden');
        }

        // Render Reviews HTML Template
        function renderReviews() {
            const homeContainer = document.getElementById('homeReviewsContainer');
            const fullContainer = document.getElementById('fullReviewsContainer');

            let html = '';
            clientReviews.forEach(review => {
                let starsHtml = '<i class="fa-solid fa-star text-amber-400 text-xs"></i>'.repeat(review.stars);

                html += `
                    <div class="bg-brand-charcoal p-8 rounded-3xl border border-white/10 hover:border-brand-coral/40 transition-all flex flex-col justify-between">
                        <div>
                            <div class="flex items-center gap-1 mb-5">
                                ${starsHtml}
                            </div>
                            <p class="text-zinc-300 text-base leading-relaxed italic mb-8">"${review.text}"</p>
                        </div>
                        <div class="flex items-center gap-4 pt-5 border-t border-white/10">
                            <img src="${review.avatar}" alt="${review.name}" class="w-12 h-12 rounded-full object-cover border border-brand-coral/40">
                            <div>
                                <h4 class="text-base font-bold text-white">${review.name}</h4>
                                <p class="text-xs text-brand-coral font-semibold">${review.role}</p>
                                <p class="text-xs text-zinc-400">${review.company}</p>
                            </div>
                        </div>
                    </div>
                `;
            });

            if(homeContainer) {
                homeContainer.innerHTML = clientReviews.slice(0, 3).map(review => {
                    let starsHtml = '<i class="fa-solid fa-star text-amber-400 text-xs"></i>'.repeat(review.stars);
                    return `
                        <div class="bg-brand-charcoal p-8 rounded-3xl border border-white/10 flex flex-col justify-between">
                            <div>
                                <div class="flex items-center gap-1 mb-4">${starsHtml}</div>
                                <p class="text-zinc-300 text-sm leading-relaxed mb-6">"${review.text}"</p>
                            </div>
                            <div class="flex items-center gap-4 pt-4 border-t border-white/10">
                                <img src="${review.avatar}" alt="${review.name}" class="w-11 h-11 rounded-full object-cover">
                                <div>
                                    <h4 class="text-sm font-bold text-white">${review.name}</h4>
                                    <p class="text-xs text-brand-coral font-semibold">${review.company}</p>
                                </div>
                            </div>
                        </div>
                    `;
                }).join('');
            }

            if(fullContainer) fullContainer.innerHTML = html;
        }

        // Calculation logic for interactive quote tool
        function calculateEstimate() {
            const baseObj = parseFloat(document.getElementById('calcObjective').value);
            const durationMultiplier = parseFloat(document.getElementById('calcDuration').value);
            const total = Math.round(baseObj * durationMultiplier);
            document.getElementById('calcTotal').innerText = `$${total.toLocaleString()} USD`;
        }

        // Custom notification for contact form submit
        function handleFormSubmit(e) {
            e.preventDefault();
            const messageBox = document.createElement('div');
            messageBox.className = "fixed bottom-8 right-8 bg-brand-coral text-white px-8 py-5 rounded-2xl shadow-2xl z-50 flex items-center gap-4 animate-bounce";
            messageBox.innerHTML = `
                <i class="fa-solid fa-paper-plane text-2xl"></i>
                <div>
                    <h5 class="font-bold text-base">Inquiry Received!</h5>
                    <p class="text-xs">Noble Consultant team will reach out within 24 hours.</p>
                </div>
            `;
            document.body.appendChild(messageBox);
            setTimeout(() => {
                messageBox.remove();
                document.getElementById('contactForm').reset();
            }, 4000);
        }

        // Initialize on load
        window.onload = function() {
            renderReviews();
        };
    </script>
</body>
</html>
