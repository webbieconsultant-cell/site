<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Noble Consultant | Elite Enterprise Strategy & Digital Transformation</title>
    
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- FontAwesome Icons CDN -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <!-- Google Fonts: Plus Jakarta Sans & Inter -->
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800&family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        brand: {
                            coral: '#E8532B',       // Accent coral matching the 'C' logo
                            coralHover: '#D0421B',
                            coralLight: 'rgba(232, 83, 43, 0.15)',
                            dark: '#0B0C10',        // Obsidian black base
                            surface: '#121318',     // Secondary backdrop
                            card: '#181920',        // Elevated card surface
                            border: '#272935',      // Clean subtle borders
                            muted: '#A1A1AA',
                            cream: '#FAF8F5'
                        }
                    },
                    fontFamily: {
                        sans: ['Plus Jakarta Sans', 'Inter', 'sans-serif'],
                    }
                }
            }
        }
    </script>
    <style>
        body {
            font-family: 'Plus Jakarta Sans', sans-serif;
            background-color: #0B0C10;
            color: #F4F4F5;
            overflow-x: hidden;
        }
        
        .nc-gradient-text {
            background: linear-gradient(135deg, #FFFFFF 20%, #E8532B 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .nc-coral-gradient {
            background: linear-gradient(135deg, #E8532B 0%, #FF6B4A 100%);
        }

        .nc-glass {
            background: rgba(24, 25, 32, 0.85);
            backdrop-filter: blur(16px);
            border: 1px solid rgba(255, 255, 255, 0.08);
        }

        .nc-glow {
            box-shadow: 0 12px 35px -8px rgba(232, 83, 43, 0.35);
        }

        .custom-scrollbar::-webkit-scrollbar {
            width: 8px;
        }
        .custom-scrollbar::-webkit-scrollbar-track {
            background: #0B0C10;
        }
        .custom-scrollbar::-webkit-scrollbar-thumb {
            background: #272935;
            border-radius: 4px;
        }
        .custom-scrollbar::-webkit-scrollbar-thumb:hover {
            background: #E8532B;
        }

        /* Marquee Animation for Client Logos */
        @keyframes marquee {
            0% { transform: translateX(0%); }
            100% { transform: translateX(-50%); }
        }
        .animate-marquee {
            display: flex;
            width: 200%;
            animation: marquee 25s linear infinite;
        }
        .animate-marquee:hover {
            animation-play-state: paused;
        }
    </style>
</head>
<body class="custom-scrollbar min-h-screen flex flex-col justify-between selection:bg-brand-coral selection:text-white">

    <!-- NAVIGATION BAR - FULL WIDTH -->
    <header class="sticky top-0 z-50 nc-glass border-b border-brand-border transition-all duration-300" id="mainHeader">
        <div class="w-full px-6 md:px-12 lg:px-16 xl:px-24 h-20 sm:h-24 flex items-center justify-between">
            <!-- Brand Logo -->
            <a href="#" onclick="navigateTo('home'); return false;" class="flex items-center gap-3.5 group shrink-0">
                <div class="relative w-11 h-11 sm:w-12 sm:h-12 bg-black rounded-xl border border-white/20 p-1.5 flex flex-col justify-center items-center shadow-lg group-hover:border-brand-coral transition-colors">
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
            <nav class="hidden lg:flex items-center space-x-1 xl:space-x-2">
                <button onclick="navigateTo('home')" class="nav-link px-4 py-2.5 text-sm xl:text-base font-semibold text-brand-coral bg-white/5 rounded-xl transition-all" data-page="home">Home</button>
                <button onclick="navigateTo('about')" class="nav-link px-4 py-2.5 text-sm xl:text-base font-semibold text-white/80 hover:text-brand-coral hover:bg-white/5 rounded-xl transition-all" data-page="about">About Us</button>
                <button onclick="navigateTo('services')" class="nav-link px-4 py-2.5 text-sm xl:text-base font-semibold text-white/80 hover:text-brand-coral hover:bg-white/5 rounded-xl transition-all" data-page="services">Capabilities</button>
                <button onclick="navigateTo('projects')" class="nav-link px-4 py-2.5 text-sm xl:text-base font-semibold text-white/80 hover:text-brand-coral hover:bg-white/5 rounded-xl transition-all" data-page="projects">Case Studies</button>
                <button onclick="navigateTo('testimonials')" class="nav-link px-4 py-2.5 text-sm xl:text-base font-semibold text-white/80 hover:text-brand-coral hover:bg-white/5 rounded-xl transition-all" data-page="testimonials">Reviews</button>
                <button onclick="navigateTo('pricing')" class="nav-link px-4 py-2.5 text-sm xl:text-base font-semibold text-white/80 hover:text-brand-coral hover:bg-white/5 rounded-xl transition-all" data-page="pricing">Pricing</button>
            </nav>

            <!-- CTA Header Button -->
            <div class="hidden lg:flex items-center gap-4">
                <button onclick="navigateTo('contact')" class="nc-coral-gradient text-white px-6 py-3 rounded-xl font-bold text-sm xl:text-base hover:scale-[1.02] active:scale-[0.98] transition-all nc-glow flex items-center gap-2">
                    <span>Request a Free Quote</span>
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
        <div id="mobileMenu" class="hidden lg:hidden nc-glass border-b border-brand-border px-6 pt-3 pb-8 space-y-3">
            <button onclick="navigateTo('home'); toggleMobileMenu();" class="block w-full text-left px-4 py-3 text-base font-semibold text-white hover:bg-white/5 rounded-xl">Home</button>
            <button onclick="navigateTo('about'); toggleMobileMenu();" class="block w-full text-left px-4 py-3 text-base font-semibold text-white/80 hover:bg-white/5 rounded-xl">About Us</button>
            <button onclick="navigateTo('services'); toggleMobileMenu();" class="block w-full text-left px-4 py-3 text-base font-semibold text-white/80 hover:bg-white/5 rounded-xl">Capabilities</button>
            <button onclick="navigateTo('projects'); toggleMobileMenu();" class="block w-full text-left px-4 py-3 text-base font-semibold text-white/80 hover:bg-white/5 rounded-xl">Case Studies</button>
            <button onclick="navigateTo('testimonials'); toggleMobileMenu();" class="block w-full text-left px-4 py-3 text-base font-semibold text-white/80 hover:bg-white/5 rounded-xl">Reviews</button>
            <button onclick="navigateTo('pricing'); toggleMobileMenu();" class="block w-full text-left px-4 py-3 text-base font-semibold text-white/80 hover:bg-white/5 rounded-xl">Pricing</button>
            <button onclick="navigateTo('contact'); toggleMobileMenu();" class="mt-4 w-full nc-coral-gradient text-white py-3.5 rounded-xl font-bold text-center block">Request a Free Quote</button>
        </div>
    </header>

    <main id="appContent" class="flex-grow w-full">
        <!-- ========================================================================= -->
        <!-- PAGE 1: HOME PAGE -->
        <!-- ========================================================================= -->
        <section id="page-home" class="page-view block w-full">
            <!-- Full Width Hero Section -->
            <div class="relative overflow-hidden py-12 lg:py-20 px-6 md:px-12 lg:px-16 xl:px-24 w-full">
                <!-- Background Ambient Glows -->
                <div class="absolute top-1/4 left-1/2 -translate-x-1/2 -translate-y-1/2 w-[800px] h-[800px] bg-brand-coral/10 rounded-full blur-[180px] pointer-events-none"></div>

                <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 xl:gap-16 items-center w-full">
                    <!-- Left Hero Text -->
                    <div class="lg:col-span-7 space-y-6 lg:space-y-8 text-center lg:text-left">
                        <div class="inline-flex items-center gap-2 px-4 py-2 rounded-full bg-brand-coralLight border border-brand-coral/30 text-brand-coral text-xs sm:text-sm font-bold tracking-wide uppercase">
                            <i class="fa-solid fa-gem text-xs"></i>
                            <span>Noble Business Advisory & Enterprise Growth</span>
                        </div>
                        
                        <h1 class="text-4xl sm:text-5xl lg:text-6xl xl:text-7xl font-extrabold tracking-tight text-white leading-[1.12]">
                            Accelerating Enterprise <span class="nc-gradient-text">Revenue & Sustainable Scale</span>
                        </h1>
                        
                        <p class="text-base sm:text-xl text-zinc-300 max-w-3xl mx-auto lg:mx-0 leading-relaxed font-normal">
                            Welcome to <strong class="text-white font-semibold">Noble Consultant</strong>. We partner with founders, executives, and scaling brands to optimize operations, deploy high-converting digital systems, and build market leadership.
                        </p>

                        <div class="flex flex-col sm:flex-row items-center justify-center lg:justify-start gap-4 pt-2">
                            <button onclick="navigateTo('contact')" class="w-full sm:w-auto nc-coral-gradient text-white px-8 py-4 sm:py-5 rounded-2xl font-bold text-base sm:text-lg hover:scale-[1.02] active:scale-[0.98] transition-all nc-glow flex items-center justify-center gap-3">
                                <span>Request a Free Quote</span>
                                <i class="fa-solid fa-arrow-right"></i>
                            </button>
                            <button onclick="navigateTo('projects')" class="w-full sm:w-auto bg-brand-card hover:bg-white/10 text-white border border-brand-border px-8 py-4 sm:py-5 rounded-2xl font-semibold text-base sm:text-lg transition-all flex items-center justify-center gap-3">
                                <i class="fa-solid fa-chart-line text-brand-coral"></i>
                                <span>View Case Studies</span>
                            </button>
                        </div>

                        <!-- Mini Social Proof Metric Bar -->
                        <div class="pt-8 sm:pt-10 border-t border-brand-border grid grid-cols-3 gap-6 text-center lg:text-left">
                            <div>
                                <p class="text-2xl sm:text-4xl font-extrabold text-white">98%</p>
                                <p class="text-xs sm:text-sm text-zinc-400 mt-1 font-medium">Client Satisfaction</p>
                            </div>
                            <div>
                                <p class="text-2xl sm:text-4xl font-extrabold text-brand-coral">$45M+</p>
                                <p class="text-xs sm:text-sm text-zinc-400 mt-1 font-medium">Revenue Driven</p>
                            </div>
                            <div>
                                <p class="text-2xl sm:text-4xl font-extrabold text-white">120+</p>
                                <p class="text-xs sm:text-sm text-zinc-400 mt-1 font-medium">Projects Delivered</p>
                            </div>
                        </div>
                    </div>

                    <!-- Right Hero Image - Portrait Container -->
                    <div class="lg:col-span-5 relative flex justify-center">
                        <div class="relative w-full max-w-md lg:max-w-none">
                            <!-- Glowing Frame -->
                            <div class="absolute inset-0 bg-gradient-to-tr from-brand-coral via-orange-500 to-amber-500 rounded-3xl transform rotate-2 scale-95 opacity-60 blur-md"></div>
                            
                            <!-- Main Portrait Box -->
                            <div class="relative bg-brand-card border border-brand-border rounded-3xl overflow-hidden shadow-2xl">
                                <img src="image_0b0f18.jpg" alt="Noble Consultant Advisor" class="w-full h-auto object-cover max-h-[600px] w-full filter brightness-105 contrast-105" onerror="this.onerror=null; this.src='https://placehold.co/700x850/18181b/ffffff?text=Noble+Consultant+Advisor'">
                                
                                <!-- Floating Status Badge -->
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

            <!-- Client Logos Marquee Banner -->
            <div class="py-10 bg-brand-surface border-y border-brand-border overflow-hidden my-8 w-full">
                <div class="w-full px-6 mb-6 text-center">
                    <p class="text-xs sm:text-sm font-bold text-zinc-400 uppercase tracking-widest">Trusted by Growth Leaders & Enterprise Operations Worldwide</p>
                </div>
                <div class="flex overflow-hidden">
                    <div class="animate-marquee items-center justify-around gap-12 opacity-80">
                        <span class="text-lg sm:text-xl font-extrabold text-zinc-300 tracking-wider flex items-center gap-2"><i class="fa-solid fa-building text-brand-coral"></i> APEX HOLDINGS</span>
                        <span class="text-lg sm:text-xl font-extrabold text-zinc-300 tracking-wider flex items-center gap-2"><i class="fa-solid fa-chart-pie text-brand-coral"></i> VENTURE MATRIX</span>
                        <span class="text-lg sm:text-xl font-extrabold text-zinc-300 tracking-wider flex items-center gap-2"><i class="fa-solid fa-shield-halved text-brand-coral"></i> NEXUS CAPITAL</span>
                        <span class="text-lg sm:text-xl font-extrabold text-zinc-300 tracking-wider flex items-center gap-2"><i class="fa-solid fa-rocket text-brand-coral"></i> ELEVATE TECH</span>
                        <span class="text-lg sm:text-xl font-extrabold text-zinc-300 tracking-wider flex items-center gap-2"><i class="fa-solid fa-globe text-brand-coral"></i> HORIZON CORP</span>
                        <span class="text-lg sm:text-xl font-extrabold text-zinc-300 tracking-wider flex items-center gap-2"><i class="fa-solid fa-city text-brand-coral"></i> URBAN PRIME REALTY</span>
                        <!-- Duplicate set for infinite loop -->
                        <span class="text-lg sm:text-xl font-extrabold text-zinc-300 tracking-wider flex items-center gap-2"><i class="fa-solid fa-building text-brand-coral"></i> APEX HOLDINGS</span>
                        <span class="text-lg sm:text-xl font-extrabold text-zinc-300 tracking-wider flex items-center gap-2"><i class="fa-solid fa-chart-pie text-brand-coral"></i> VENTURE MATRIX</span>
                        <span class="text-lg sm:text-xl font-extrabold text-zinc-300 tracking-wider flex items-center gap-2"><i class="fa-solid fa-shield-halved text-brand-coral"></i> NEXUS CAPITAL</span>
                        <span class="text-lg sm:text-xl font-extrabold text-zinc-300 tracking-wider flex items-center gap-2"><i class="fa-solid fa-rocket text-brand-coral"></i> ELEVATE TECH</span>
                        <span class="text-lg sm:text-xl font-extrabold text-zinc-300 tracking-wider flex items-center gap-2"><i class="fa-solid fa-globe text-brand-coral"></i> HORIZON CORP</span>
                        <span class="text-lg sm:text-xl font-extrabold text-zinc-300 tracking-wider flex items-center gap-2"><i class="fa-solid fa-city text-brand-coral"></i> URBAN PRIME REALTY</span>
                    </div>
                </div>
            </div>

            <!-- CORE SERVICES PREVIEW - FULL WIDTH -->
            <div class="py-20 px-6 md:px-12 lg:px-16 xl:px-24 w-full">
                <div class="text-center max-w-3xl mx-auto mb-16">
                    <span class="text-brand-coral font-bold text-xs sm:text-sm tracking-widest uppercase">High Impact Capabilities</span>
                    <h2 class="text-3xl sm:text-5xl font-extrabold text-white mt-3">Tailored Consultancy for Scale</h2>
                    <p class="text-zinc-400 mt-4 text-base sm:text-lg">We diagnose operational bottlenecks, build high-converting web systems, and engineer repeatable revenue pipelines.</p>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 sm:gap-10 w-full">
                    <!-- Service Card 1 -->
                    <div class="bg-brand-card p-8 sm:p-10 rounded-3xl border border-brand-border hover:border-brand-coral/60 transition-all group hover:-translate-y-1.5 flex flex-col justify-between">
                        <div>
                            <div class="w-16 h-16 rounded-2xl bg-brand-coralLight border border-brand-coral/30 flex items-center justify-center text-brand-coral text-3xl mb-8 group-hover:bg-brand-coral group-hover:text-white transition-all">
                                <i class="fa-solid fa-laptop-code"></i>
                            </div>
                            <h3 class="text-2xl font-bold text-white mb-4">Custom Web Development</h3>
                            <p class="text-zinc-400 text-base leading-relaxed mb-8">Ultra-fast, fully responsive web platforms built for maximum conversion, lead generation, and brand dominance.</p>
                        </div>
                        <button onclick="navigateTo('services')" class="text-brand-coral font-bold text-base inline-flex items-center gap-2 group-hover:translate-x-1 transition-transform">
                            Explore Service <i class="fa-solid fa-chevron-right text-xs"></i>
                        </button>
                    </div>

                    <!-- Service Card 2 -->
                    <div class="bg-brand-card p-8 sm:p-10 rounded-3xl border border-brand-border hover:border-brand-coral/60 transition-all group hover:-translate-y-1.5 flex flex-col justify-between">
                        <div>
                            <div class="w-16 h-16 rounded-2xl bg-brand-coralLight border border-brand-coral/30 flex items-center justify-center text-brand-coral text-3xl mb-8 group-hover:bg-brand-coral group-hover:text-white transition-all">
                                <i class="fa-solid fa-chess"></i>
                            </div>
                            <h3 class="text-2xl font-bold text-white mb-4">Product & Business Strategy</h3>
                            <p class="text-zinc-400 text-base leading-relaxed mb-8">Executive advisory, unit economics, market positioning, and roadmap design for ambitious leadership teams.</p>
                        </div>
                        <button onclick="navigateTo('services')" class="text-brand-coral font-bold text-base inline-flex items-center gap-2 group-hover:translate-x-1 transition-transform">
                            Explore Service <i class="fa-solid fa-chevron-right text-xs"></i>
                        </button>
                    </div>

                    <!-- Service Card 3 -->
                    <div class="bg-brand-card p-8 sm:p-10 rounded-3xl border border-brand-border hover:border-brand-coral/60 transition-all group hover:-translate-y-1.5 flex flex-col justify-between">
                        <div>
                            <div class="w-16 h-16 rounded-2xl bg-brand-coralLight border border-brand-coral/30 flex items-center justify-center text-brand-coral text-3xl mb-8 group-hover:bg-brand-coral group-hover:text-white transition-all">
                                <i class="fa-solid fa-city"></i>
                            </div>
                            <h3 class="text-2xl font-bold text-white mb-4">Real Estate Lead Systems</h3>
                            <p class="text-zinc-400 text-base leading-relaxed mb-8">Automated lead qualification and CRM acquisition funnels designed specifically for high-value real estate agencies.</p>
                        </div>
                        <button onclick="navigateTo('services')" class="text-brand-coral font-bold text-base inline-flex items-center gap-2 group-hover:translate-x-1 transition-transform">
                            Explore Service <i class="fa-solid fa-chevron-right text-xs"></i>
                        </button>
                    </div>
                </div>
            </div>

            <!-- FEATURED TESTIMONIAL PREVIEW -->
            <div class="py-20 bg-brand-surface border-y border-brand-border px-6 md:px-12 lg:px-16 xl:px-24 w-full">
                <div class="w-full">
                    <div class="flex flex-col md:flex-row justify-between items-start md:items-end mb-14 gap-4">
                        <div>
                            <span class="text-brand-coral font-bold text-xs sm:text-sm tracking-widest uppercase">Verified Executive Feedback</span>
                            <h2 class="text-3xl sm:text-4xl font-extrabold text-white mt-2">What Client Leaders Say</h2>
                        </div>
                        <button onclick="navigateTo('testimonials')" class="text-brand-coral hover:text-white font-bold text-base flex items-center gap-2 group">
                            <span>View All Wall of Love</span>
                            <i class="fa-solid fa-arrow-right group-hover:translate-x-1 transition-transform"></i>
                        </button>
                    </div>

                    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 w-full" id="homeReviewsContainer">
                        <!-- Populated via JS dynamically -->
                    </div>
                </div>
            </div>

            <!-- CTA Callout Banner -->
            <div class="py-20 px-6 md:px-12 lg:px-16 xl:px-24 w-full">
                <div class="bg-gradient-to-r from-brand-card via-brand-surface to-brand-card rounded-3xl border border-brand-coral/40 p-10 md:p-16 text-center relative overflow-hidden">
                    <div class="relative z-10 max-w-3xl mx-auto space-y-6">
                        <h2 class="text-3xl sm:text-5xl font-extrabold text-white">Ready to Scale Your Enterprise Revenue?</h2>
                        <p class="text-zinc-300 text-base sm:text-lg">Partner with Noble Consultant to build custom web systems, optimize conversions, and dominate your niche.</p>
                        <button onclick="navigateTo('contact')" class="nc-coral-gradient text-white px-10 py-5 rounded-2xl font-bold text-lg hover:scale-105 transition-all shadow-xl nc-glow inline-flex items-center gap-3">
                            <span>Request Your Free Quote</span>
                            <i class="fa-solid fa-paper-plane"></i>
                        </button>
                    </div>
                </div>
            </div>
        </section>

        <!-- ========================================================================= -->
        <!-- PAGE 2: ABOUT US -->
        <!-- ========================================================================= -->
        <section id="page-about" class="page-view hidden w-full">
            <div class="py-16 md:py-20 px-6 md:px-12 lg:px-16 xl:px-24 w-full">
                <!-- Page Title Header -->
                <div class="text-center max-w-4xl mx-auto mb-20">
                    <span class="text-brand-coral font-bold text-xs sm:text-sm tracking-widest uppercase">About Noble Consultant</span>
                    <h1 class="text-4xl sm:text-5xl lg:text-6xl font-extrabold text-white mt-3">Precision Strategy for Ambitious Leaders</h1>
                    <p class="text-zinc-400 mt-4 text-base sm:text-xl leading-relaxed">Built on principles of transparency, analytical rigor, and sustainable enterprise scale.</p>
                </div>

                <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 lg:gap-16 items-center mb-24 w-full">
                    <!-- Photo Left -->
                    <div class="lg:col-span-5 flex justify-center">
                        <div class="relative w-full max-w-md rounded-3xl overflow-hidden border-2 border-brand-coral/40 shadow-2xl bg-brand-card">
                            <img src="image_0b0f18.jpg" alt="Noble Consultant Founder" class="w-full h-auto object-cover" onerror="this.onerror=null; this.src='https://placehold.co/700x850/18181b/ffffff?text=Noble+Consultant+Advisor'">
                            <div class="p-6 bg-brand-card border-t border-brand-border text-center">
                                <h3 class="text-xl font-bold text-white">Lead Growth Consultant</h3>
                                <p class="text-sm text-brand-coral font-semibold">Noble Consultant Advisory</p>
                            </div>
                        </div>
                    </div>

                    <!-- Story Right -->
                    <div class="lg:col-span-7 space-y-6 sm:space-y-8">
                        <h2 class="text-3xl sm:text-4xl font-extrabold text-white">Empowering Enterprise Scale Through Principled Advisory</h2>
                        <p class="text-zinc-300 text-base sm:text-lg leading-relaxed">At <strong class="text-white">Noble Consultant</strong>, we believe every business possesses high growth potential that can be unlocked through structured web systems, automated lead funnels, and optimized operations.</p>
                        <p class="text-zinc-400 text-base sm:text-lg leading-relaxed">We step into your organization not as external vendors, but as strategic partners deeply committed to measurable ROI. Our holistic approach bridges high-level executive strategy with hands-on digital implementation.</p>
                        
                        <div class="grid grid-cols-1 sm:grid-cols-2 gap-6 pt-4">
                            <div class="p-6 rounded-2xl bg-brand-card border border-brand-border">
                                <i class="fa-solid fa-bullseye text-brand-coral text-3xl mb-3"></i>
                                <h4 class="font-bold text-white text-lg">Our Mission</h4>
                                <p class="text-sm text-zinc-400 mt-2 leading-relaxed">To deliver clear, actionable, and scalable business advisory and web systems that drive repeatable revenue growth.</p>
                            </div>
                            <div class="p-6 rounded-2xl bg-brand-card border border-brand-border">
                                <i class="fa-solid fa-eye text-brand-coral text-3xl mb-3"></i>
                                <h4 class="font-bold text-white text-lg">Our Vision</h4>
                                <p class="text-sm text-zinc-400 mt-2 leading-relaxed">To be the premier strategic digital advisory firm for forward-thinking enterprises and scaling founders.</p>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Interactive Core Principles Tabs Section -->
                <div class="py-16 bg-brand-card rounded-3xl p-8 sm:p-14 border border-brand-border mb-20 w-full">
                    <h3 class="text-3xl font-extrabold text-white text-center mb-10">Our Strategic Growth Pillars</h3>
                    
                    <div class="flex justify-center gap-4 mb-8 flex-wrap">
                        <button onclick="switchPillarTab('integrity')" id="pillarBtn-integrity" class="px-6 py-3 rounded-xl font-bold text-sm bg-brand-coral text-white transition-all">Uncompromising Integrity</button>
                        <button onclick="switchPillarTab('data')" id="pillarBtn-data" class="px-6 py-3 rounded-xl font-bold text-sm bg-white/5 text-zinc-300 hover:text-white transition-all">Data-Driven Execution</button>
                        <button onclick="switchPillarTab('partnership')" id="pillarBtn-partnership" class="px-6 py-3 rounded-xl font-bold text-sm bg-white/5 text-zinc-300 hover:text-white transition-all">Long-term Partnership</button>
                    </div>

                    <div id="pillarContent" class="text-center max-w-2xl mx-auto p-6 bg-brand-surface rounded-2xl border border-brand-border">
                        <p class="text-zinc-300 text-base leading-relaxed" id="pillarText">Direct, transparent recommendations with zero fluff. Every piece of advice and system we construct is centered strictly around your measurable return on investment.</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- ========================================================================= -->
        <!-- PAGE 3: SERVICES / CAPABILITIES -->
        <!-- ========================================================================= -->
        <section id="page-services" class="page-view hidden w-full">
            <div class="py-16 md:py-20 px-6 md:px-12 lg:px-16 xl:px-24 w-full">
                <div class="text-center max-w-4xl mx-auto mb-20">
                    <span class="text-brand-coral font-bold text-xs sm:text-sm tracking-widest uppercase">Consulting Capabilities</span>
                    <h1 class="text-4xl sm:text-5xl lg:text-6xl font-extrabold text-white mt-3">Services Built for Enterprise Scale</h1>
                    <p class="text-zinc-400 mt-4 text-base sm:text-xl">Explore our modular consultancy offerings designed for custom web design, product strategy, and automated lead systems.</p>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 sm:gap-10 w-full mb-20">
                    <!-- Service 1 -->
                    <div class="bg-brand-card rounded-3xl p-8 sm:p-10 border border-brand-border hover:border-brand-coral transition-all flex flex-col justify-between">
                        <div>
                            <div class="w-14 h-14 rounded-2xl bg-brand-coralLight text-brand-coral flex items-center justify-center text-2xl mb-8">
                                <i class="fa-solid fa-laptop-code"></i>
                            </div>
                            <h3 class="text-2xl font-bold text-white mb-4">Custom Web Development</h3>
                            <p class="text-zinc-400 text-base leading-relaxed mb-8">Bespoke, lightning-fast web applications designed with modern UI/UX to maximize user engagement and convert visitors into long-term clients.</p>
                            <ul class="space-y-3 text-sm text-zinc-300 mb-8">
                                <li class="flex items-center gap-3"><i class="fa-solid fa-check text-brand-coral"></i> Custom SPA Web Architectures</li>
                                <li class="flex items-center gap-3"><i class="fa-solid fa-check text-brand-coral"></i> Ultra-Fast Desktop & Mobile Load Speeds</li>
                                <li class="flex items-center gap-3"><i class="fa-solid fa-check text-brand-coral"></i> Responsive UI/UX Design Token Systems</li>
                            </ul>
                        </div>
                        <button onclick="navigateTo('contact')" class="w-full py-4 rounded-2xl bg-white/5 hover:bg-brand-coral text-white font-bold text-base transition-colors">Inquire Service</button>
                    </div>

                    <!-- Service 2 -->
                    <div class="bg-brand-card rounded-3xl p-8 sm:p-10 border border-brand-border hover:border-brand-coral transition-all flex flex-col justify-between">
                        <div>
                            <div class="w-14 h-14 rounded-2xl bg-brand-coralLight text-brand-coral flex items-center justify-center text-2xl mb-8">
                                <i class="fa-solid fa-chess"></i>
                            </div>
                            <h3 class="text-2xl font-bold text-white mb-4">Product Strategy & Growth</h3>
                            <p class="text-zinc-400 text-base leading-relaxed mb-8">Executive guidance for business positioning, offer creation, unit economics alignment, and go-to-market scaling roadmaps.</p>
                            <ul class="space-y-3 text-sm text-zinc-300 mb-8">
                                <li class="flex items-center gap-3"><i class="fa-solid fa-check text-brand-coral"></i> Go-to-Market Strategy</li>
                                <li class="flex items-center gap-3"><i class="fa-solid fa-check text-brand-coral"></i> Pricing & Unit Economics Optimization</li>
                                <li class="flex items-center gap-3"><i class="fa-solid fa-check text-brand-coral"></i> Product Positioning & Messaging</li>
                            </ul>
                        </div>
                        <button onclick="navigateTo('contact')" class="w-full py-4 rounded-2xl bg-white/5 hover:bg-brand-coral text-white font-bold text-base transition-colors">Inquire Service</button>
                    </div>

                    <!-- Service 3 -->
                    <div class="bg-brand-card rounded-3xl p-8 sm:p-10 border border-brand-border hover:border-brand-coral transition-all flex flex-col justify-between">
                        <div>
                            <div class="w-14 h-14 rounded-2xl bg-brand-coralLight text-brand-coral flex items-center justify-center text-2xl mb-8">
                                <i class="fa-solid fa-city"></i>
                            </div>
                            <h3 class="text-2xl font-bold text-white mb-4">Real Estate Lead Systems</h3>
                            <p class="text-zinc-400 text-base leading-relaxed mb-8">Specialized digital infrastructure for real estate developers and brokerages to capture, nurture, and convert high-net-worth buyers.</p>
                            <ul class="space-y-3 text-sm text-zinc-300 mb-8">
                                <li class="flex items-center gap-3"><i class="fa-solid fa-check text-brand-coral"></i> Automated Lead Qualification Funnels</li>
                                <li class="flex items-center gap-3"><i class="fa-solid fa-check text-brand-coral"></i> High-Converting Property Dashboards</li>
                                <li class="flex items-center gap-3"><i class="fa-solid fa-check text-brand-coral"></i> CRM Integration & Lead Nurturing</li>
                            </ul>
                        </div>
                        <button onclick="navigateTo('contact')" class="w-full py-4 rounded-2xl bg-white/5 hover:bg-brand-coral text-white font-bold text-base transition-colors">Inquire Service</button>
                    </div>
                </div>

                <!-- Interactive ROI / Project Estimator Tool -->
                <div class="p-8 sm:p-12 rounded-3xl bg-gradient-to-r from-brand-card to-brand-surface border border-brand-border w-full">
                    <div class="max-w-3xl mx-auto text-center">
                        <span class="text-brand-coral font-bold text-xs uppercase tracking-widest">Interactive Calculator</span>
                        <h3 class="text-3xl font-extrabold text-white mt-2 mb-3">Instant Engagement & ROI Estimator</h3>
                        <p class="text-sm text-zinc-400 mb-10">Select your key objectives to calculate scope, timeline, and estimated project return.</p>

                        <div class="space-y-6 text-left">
                            <div>
                                <label class="block text-xs font-bold text-zinc-300 uppercase tracking-wider mb-2">Primary Scope Objective:</label>
                                <select id="calcObjective" onchange="calculateEstimate()" class="w-full bg-brand-dark border border-brand-border rounded-2xl p-4 text-white text-base focus:border-brand-coral focus:outline-none">
                                    <option value="3500">Custom Web Development & Brand Infrastructure ($3,500)</option>
                                    <option value="6000">Product Strategy & Revenue Optimization ($6,000)</option>
                                    <option value="8500">Real Estate Lead System & Automated CRM ($8,500)</option>
                                </select>
                            </div>

                            <div>
                                <label class="block text-xs font-bold text-zinc-300 uppercase tracking-wider mb-2">Advisory Sprint Duration:</label>
                                <select id="calcDuration" onchange="calculateEstimate()" class="w-full bg-brand-dark border border-brand-border rounded-2xl p-4 text-white text-base focus:border-brand-coral focus:outline-none">
                                    <option value="1">1 Month Sprint (Standard)</option>
                                    <option value="1.8">3 Months Growth Retainer (10% Savings)</option>
                                    <option value="3">6 Months Enterprise Partnership (15% Savings)</option>
                                </select>
                            </div>

                            <div class="pt-8 border-t border-brand-border flex flex-col sm:flex-row items-center justify-between gap-6">
                                <div>
                                    <p class="text-xs text-zinc-400 uppercase font-bold tracking-wider">Estimated Total Investment:</p>
                                    <p class="text-4xl font-extrabold text-brand-coral mt-1" id="calcTotal">$3,500 USD</p>
                                </div>
                                <button onclick="navigateTo('contact')" class="w-full sm:w-auto nc-coral-gradient text-white px-8 py-4 rounded-2xl text-base font-bold shadow-lg hover:scale-105 transition-transform">
                                    Request Your Quote
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
        <section id="page-projects" class="page-view hidden w-full">
            <div class="py-16 md:py-20 px-6 md:px-12 lg:px-16 xl:px-24 w-full">
                <div class="text-center max-w-4xl mx-auto mb-16">
                    <span class="text-brand-coral font-bold text-xs sm:text-sm tracking-widest uppercase">Proven Client Outcomes</span>
                    <h1 class="text-4xl sm:text-5xl lg:text-6xl font-extrabold text-white mt-3">Case Studies & Impact</h1>
                    <p class="text-zinc-400 mt-4 text-base sm:text-xl">A selection of enterprise digital systems engineered by Noble Consultant.</p>
                </div>

                <!-- Filter Controls -->
                <div class="flex justify-center gap-3 mb-12 flex-wrap" id="projectFilters">
                    <button onclick="filterProjects('all')" class="filter-btn active-filter px-5 py-2.5 rounded-xl font-bold text-sm bg-brand-coral text-white transition-all" data-filter="all">All Projects</button>
                    <button onclick="filterProjects('web')" class="filter-btn px-5 py-2.5 rounded-xl font-bold text-sm bg-white/5 text-zinc-300 hover:text-white transition-all" data-filter="web">Web Design</button>
                    <button onclick="filterProjects('strategy')" class="filter-btn px-5 py-2.5 rounded-xl font-bold text-sm bg-white/5 text-zinc-300 hover:text-white transition-all" data-filter="strategy">Product Strategy</button>
                    <button onclick="filterProjects('realestate')" class="filter-btn px-5 py-2.5 rounded-xl font-bold text-sm bg-white/5 text-zinc-300 hover:text-white transition-all" data-filter="realestate">Real Estate Gens</button>
                </div>

                <!-- Projects Grid -->
                <div class="grid grid-cols-1 lg:grid-cols-2 gap-8 sm:gap-10 w-full" id="projectsContainer">
                    <!-- Dynamically populated via JS -->
                </div>
            </div>
        </section>

        <!-- ========================================================================= -->
        <!-- PAGE 5: TESTIMONIALS / REVIEWS -->
        <!-- ========================================================================= -->
        <section id="page-testimonials" class="page-view hidden w-full">
            <div class="py-16 md:py-20 px-6 md:px-12 lg:px-16 xl:px-24 w-full">
                <div class="text-center max-w-4xl mx-auto mb-16">
                    <span class="text-brand-coral font-bold text-xs sm:text-sm tracking-widest uppercase">Verified Executive Feedback</span>
                    <h1 class="text-4xl sm:text-5xl lg:text-6xl font-extrabold text-white mt-3">Wall of Trust & Client Reviews</h1>
                    <p class="text-zinc-400 mt-4 text-base sm:text-xl">Read direct accounts from managing directors and founders who trust Noble Consultant.</p>
                    
                    <button onclick="openReviewModal()" class="mt-8 nc-coral-gradient text-white px-8 py-3.5 rounded-2xl font-bold text-base shadow-lg hover:scale-105 transition-transform inline-flex items-center gap-2">
                        <i class="fa-solid fa-pen"></i>
                        <span>Submit Your Review</span>
                    </button>
                </div>

                <!-- 8 Verified Reviews Grid -->
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 w-full" id="fullReviewsContainer">
                    <!-- Javascript populates 8 distinct client reviews -->
                </div>
            </div>
        </section>

        <!-- ========================================================================= -->
        <!-- PAGE 6: PRICING -->
        <!-- ========================================================================= -->
        <section id="page-pricing" class="page-view hidden w-full">
            <div class="py-16 md:py-20 px-6 md:px-12 lg:px-16 xl:px-24 w-full">
                <div class="text-center max-w-4xl mx-auto mb-16">
                    <span class="text-brand-coral font-bold text-xs sm:text-sm tracking-widest uppercase">Transparent Pricing</span>
                    <h1 class="text-4xl sm:text-5xl lg:text-6xl font-extrabold text-white mt-3">Consultancy Engagement Tiers</h1>
                    <p class="text-zinc-400 mt-4 text-base sm:text-xl">Select the scope that matches your enterprise maturity and growth objectives.</p>

                    <!-- Monthly / Annual Retainer Toggle Switch -->
                    <div class="flex items-center justify-center gap-4 mt-10">
                        <span class="text-sm font-bold text-zinc-300" id="monthlyLabel">Monthly Billing</span>
                        <button onclick="togglePricingBilling()" id="pricingToggleBtn" class="w-16 h-9 bg-brand-border rounded-full p-1 relative transition-colors focus:outline-none">
                            <div id="toggleDot" class="w-7 h-7 bg-brand-coral rounded-full shadow-md transform transition-transform"></div>
                        </button>
                        <span class="text-sm font-bold text-zinc-400" id="annualLabel">Annual Retainer <span class="text-xs text-brand-coral font-extrabold">(20% OFF)</span></span>
                    </div>
                </div>

                <div class="grid grid-cols-1 lg:grid-cols-3 gap-8 lg:gap-10 w-full">
                    <!-- Tier 1 -->
                    <div class="bg-brand-card p-8 sm:p-10 rounded-3xl border border-brand-border flex flex-col justify-between">
                        <div>
                            <span class="text-zinc-400 font-bold text-xs uppercase tracking-wider">Starter Launch</span>
                            <h3 class="text-3xl font-extrabold text-white mt-3">Strategic Audit</h3>
                            <p class="text-zinc-400 text-sm mt-2">Ideal for diagnosing web bottlenecks and growth barriers.</p>
                            <div class="my-8">
                                <span class="text-5xl font-extrabold text-white" id="priceTier1">$2,500</span>
                                <span class="text-zinc-400 text-base" id="periodTier1"> / engagement</span>
                            </div>
                            <ul class="space-y-4 text-base text-zinc-300">
                                <li class="flex items-center gap-3"><i class="fa-solid fa-check text-brand-coral"></i> Full Digital Systems Audit</li>
                                <li class="flex items-center gap-3"><i class="fa-solid fa-check text-brand-coral"></i> Executive Strategy Blueprint</li>
                                <li class="flex items-center gap-3"><i class="fa-solid fa-check text-brand-coral"></i> 2x Live Advisory Workshops</li>
                            </ul>
                        </div>
                        <button onclick="navigateTo('contact')" class="mt-10 w-full py-4 rounded-2xl bg-white/10 hover:bg-brand-coral text-white font-bold text-base transition-colors">Request Tier Quote</button>
                    </div>

                    <!-- Tier 2 - Featured -->
                    <div class="bg-brand-surface p-8 sm:p-10 rounded-3xl border-2 border-brand-coral relative flex flex-col justify-between nc-glow">
                        <div class="absolute -top-4 left-1/2 -translate-x-1/2 bg-brand-coral text-white text-xs font-extrabold uppercase px-5 py-1.5 rounded-full tracking-wider">
                            Most Popular Choice
                        </div>
                        <div>
                            <span class="text-brand-coral font-bold text-xs uppercase tracking-wider">Growth Acceleration</span>
                            <h3 class="text-3xl font-extrabold text-white mt-3">Growth Partner</h3>
                            <p class="text-zinc-400 text-sm mt-2">Complete web development & product strategy implementation.</p>
                            <div class="my-8">
                                <span class="text-5xl font-extrabold text-white" id="priceTier2">$5,800</span>
                                <span class="text-zinc-400 text-base" id="periodTier2"> / month</span>
                            </div>
                            <ul class="space-y-4 text-base text-zinc-300">
                                <li class="flex items-center gap-3"><i class="fa-solid fa-check text-brand-coral"></i> Everything in Audit Tier</li>
                                <li class="flex items-center gap-3"><i class="fa-solid fa-check text-brand-coral"></i> Custom SPA Web Design & Build</li>
                                <li class="flex items-center gap-3"><i class="fa-solid fa-check text-brand-coral"></i> Dedicated Lead Strategic Consultant</li>
                                <li class="flex items-center gap-3"><i class="fa-solid fa-check text-brand-coral"></i> Weekly Operations Reviews</li>
                            </ul>
                        </div>
                        <button onclick="navigateTo('contact')" class="mt-10 w-full py-4 rounded-2xl nc-coral-gradient text-white font-bold text-base shadow-lg hover:scale-[1.02] transition-all">Partner With Us</button>
                    </div>

                    <!-- Tier 3 -->
                    <div class="bg-brand-card p-8 sm:p-10 rounded-3xl border border-brand-border flex flex-col justify-between">
                        <div>
                            <span class="text-zinc-400 font-bold text-xs uppercase tracking-wider">Enterprise Scale</span>
                            <h3 class="text-3xl font-extrabold text-white mt-3">Retainer Partner</h3>
                            <p class="text-zinc-400 text-sm mt-2">Continuous executive advisory and real estate lead systems.</p>
                            <div class="my-8">
                                <span class="text-5xl font-extrabold text-white" id="priceTier3">Custom</span>
                            </div>
                            <ul class="space-y-4 text-base text-zinc-300">
                                <li class="flex items-center gap-3"><i class="fa-solid fa-check text-brand-coral"></i> Board-level Digital Advisory</li>
                                <li class="flex items-center gap-3"><i class="fa-solid fa-check text-brand-coral"></i> Real Estate Lead Gen Engine</li>
                                <li class="flex items-center gap-3"><i class="fa-solid fa-check text-brand-coral"></i> Direct SLA & On-demand Priority Calls</li>
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
        <section id="page-contact" class="page-view hidden w-full">
            <div class="py-16 md:py-20 px-6 md:px-12 lg:px-16 xl:px-24 w-full">
                <div class="text-center max-w-4xl mx-auto mb-16">
                    <span class="text-brand-coral font-bold text-xs sm:text-sm tracking-widest uppercase">Start The Conversation</span>
                    <h1 class="text-4xl sm:text-5xl lg:text-6xl font-extrabold text-white mt-3">Request a Free Quote</h1>
                    <p class="text-zinc-400 mt-4 text-base sm:text-xl">Schedule your initial consultation or send us your strategic inquiry.</p>
                </div>

                <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 w-full">
                    <!-- Contact Form Left -->
                    <div class="lg:col-span-7 bg-brand-card p-8 sm:p-12 rounded-3xl border border-brand-border">
                        <form id="contactForm" onsubmit="handleFormSubmit(event)" class="space-y-6">
                            <div class="grid grid-cols-1 sm:grid-cols-2 gap-6">
                                <div>
                                    <label class="block text-xs font-bold text-zinc-300 uppercase tracking-wider mb-2">Full Name *</label>
                                    <input type="text" required placeholder="e.g. David Miller" class="w-full bg-brand-dark border border-brand-border rounded-2xl p-4 text-white text-base focus:border-brand-coral focus:outline-none">
                                </div>
                                <div>
                                    <label class="block text-xs font-bold text-zinc-300 uppercase tracking-wider mb-2">Work Email *</label>
                                    <input type="email" required placeholder="david@company.com" class="w-full bg-brand-dark border border-brand-border rounded-2xl p-4 text-white text-base focus:border-brand-coral focus:outline-none">
                                </div>
                            </div>

                            <div class="grid grid-cols-1 sm:grid-cols-2 gap-6">
                                <div>
                                    <label class="block text-xs font-bold text-zinc-300 uppercase tracking-wider mb-2">Company Name</label>
                                    <input type="text" placeholder="Your Business" class="w-full bg-brand-dark border border-brand-border rounded-2xl p-4 text-white text-base focus:border-brand-coral focus:outline-none">
                                </div>
                                <div>
                                    <label class="block text-xs font-bold text-zinc-300 uppercase tracking-wider mb-2">Primary Interest</label>
                                    <select class="w-full bg-brand-dark border border-brand-border rounded-2xl p-4 text-white text-base focus:border-brand-coral focus:outline-none">
                                        <option>Custom Web Development</option>
                                        <option>Product & Business Strategy</option>
                                        <option>Real Estate Lead Systems</option>
                                        <option>General Strategic Advisory</option>
                                    </select>
                                </div>
                            </div>

                            <!-- Interactive Consultation Time Slot Picker -->
                            <div>
                                <label class="block text-xs font-bold text-zinc-300 uppercase tracking-wider mb-2">Select Preferred Consultation Slot *</label>
                                <div class="grid grid-cols-2 sm:grid-cols-4 gap-3">
                                    <button type="button" onclick="selectSlot(this)" class="slot-btn py-3 px-2 rounded-xl border border-brand-border text-xs font-semibold text-zinc-300 hover:border-brand-coral transition-colors">10:00 AM EST</button>
                                    <button type="button" onclick="selectSlot(this)" class="slot-btn py-3 px-2 rounded-xl border border-brand-border text-xs font-semibold text-zinc-300 hover:border-brand-coral transition-colors">01:30 PM EST</button>
                                    <button type="button" onclick="selectSlot(this)" class="slot-btn py-3 px-2 rounded-xl border border-brand-border text-xs font-semibold text-zinc-300 hover:border-brand-coral transition-colors">03:00 PM EST</button>
                                    <button type="button" onclick="selectSlot(this)" class="slot-btn py-3 px-2 rounded-xl border border-brand-border text-xs font-semibold text-zinc-300 hover:border-brand-coral transition-colors">05:00 PM EST</button>
                                </div>
                            </div>

                            <div>
                                <label class="block text-xs font-bold text-zinc-300 uppercase tracking-wider mb-2">Project Details & Goals *</label>
                                <textarea rows="4" required placeholder="Tell us briefly about your current goals, timeline, and requirements..." class="w-full bg-brand-dark border border-brand-border rounded-2xl p-4 text-white text-base focus:border-brand-coral focus:outline-none"></textarea>
                            </div>

                            <button type="submit" class="w-full nc-coral-gradient text-white py-5 rounded-2xl font-bold text-lg hover:opacity-95 transition-all shadow-xl nc-glow">
                                Send Quote Request
                            </button>
                        </form>
                    </div>

                    <!-- Contact Details Right -->
                    <div class="lg:col-span-5 space-y-8">
                        <div class="bg-brand-card p-8 sm:p-10 rounded-3xl border border-brand-border space-y-8">
                            <h3 class="text-2xl font-bold text-white">Direct Advisory Contacts</h3>
                            
                            <div class="flex items-start gap-5">
                                <div class="w-12 h-12 rounded-2xl bg-brand-coralLight text-brand-coral flex items-center justify-center text-xl shrink-0">
                                    <i class="fa-solid fa-envelope"></i>
                                </div>
                                <div>
                                    <p class="text-xs text-zinc-400 font-bold uppercase tracking-wider">Official Email</p>
                                    <p class="text-base sm:text-lg font-semibold text-white mt-1">contact@nobleconsultant.com</p>
                                </div>
                            </div>

                            <div class="flex items-start gap-5">
                                <div class="w-12 h-12 rounded-2xl bg-brand-coralLight text-brand-coral flex items-center justify-center text-xl shrink-0">
                                    <i class="fa-solid fa-phone"></i>
                                </div>
                                <div>
                                    <p class="text-xs text-zinc-400 font-bold uppercase tracking-wider">Direct Line</p>
                                    <p class="text-base sm:text-lg font-semibold text-white mt-1">+1 (800) 555-NOBLE</p>
                                </div>
                            </div>

                            <div class="flex items-start gap-5">
                                <div class="w-12 h-12 rounded-2xl bg-brand-coralLight text-brand-coral flex items-center justify-center text-xl shrink-0">
                                    <i class="fa-solid fa-location-dot"></i>
                                </div>
                                <div>
                                    <p class="text-xs text-zinc-400 font-bold uppercase tracking-wider">Headquarters</p>
                                    <p class="text-base sm:text-lg font-semibold text-white mt-1">Financial District, Strategy Hub</p>
                                </div>
                            </div>
                        </div>

                        <!-- Founder Callout Card -->
                        <div class="bg-gradient-to-br from-brand-card to-brand-surface p-8 rounded-3xl border border-brand-coral/40 flex items-center gap-5">
                            <img src="image_0b0f18.jpg" alt="Noble Consultant Founder" class="w-20 h-20 rounded-2xl object-cover border border-white/20 shrink-0" onerror="this.onerror=null; this.src='https://placehold.co/100x100/18181b/ffffff?text=Noble'">
                            <div>
                                <h4 class="text-base sm:text-lg font-bold text-white">Direct Advisory Guarantee</h4>
                                <p class="text-xs sm:text-sm text-zinc-400 mt-1">All incoming inquiries are reviewed directly by our lead team within 24 hours.</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <!-- CASE STUDY LIGHTBOX MODAL -->
    <div id="caseStudyModal" class="fixed inset-0 z-50 hidden bg-black/80 backdrop-blur-md flex items-center justify-center p-4 sm:p-6 overflow-y-auto">
        <div class="bg-brand-card border border-brand-border rounded-3xl max-w-3xl w-full p-8 sm:p-12 relative my-8">
            <button onclick="closeModal('caseStudyModal')" class="absolute top-6 right-6 text-zinc-400 hover:text-white text-2xl">
                <i class="fa-solid fa-xmark"></i>
            </button>
            <div id="modalContent">
                <!-- Javascript fills content -->
            </div>
        </div>
    </div>

    <!-- SUBMIT REVIEW MODAL -->
    <div id="reviewModal" class="fixed inset-0 z-50 hidden bg-black/80 backdrop-blur-md flex items-center justify-center p-4 sm:p-6 overflow-y-auto">
        <div class="bg-brand-card border border-brand-border rounded-3xl max-w-xl w-full p-8 sm:p-10 relative">
            <button onclick="closeModal('reviewModal')" class="absolute top-6 right-6 text-zinc-400 hover:text-white text-2xl">
                <i class="fa-solid fa-xmark"></i>
            </button>
            <h3 class="text-2xl font-bold text-white mb-2">Submit Your Review</h3>
            <p class="text-sm text-zinc-400 mb-6">Share your experience working with Noble Consultant.</p>

            <form onsubmit="handleReviewSubmit(event)" class="space-y-4">
                <div>
                    <label class="block text-xs font-bold text-zinc-300 uppercase tracking-wider mb-2">Your Name</label>
                    <input type="text" id="reviewName" required class="w-full bg-brand-dark border border-brand-border rounded-xl p-3 text-white text-sm">
                </div>
                <div>
                    <label class="block text-xs font-bold text-zinc-300 uppercase tracking-wider mb-2">Company & Position</label>
                    <input type="text" id="reviewRole" required placeholder="e.g. CEO at Apex Group" class="w-full bg-brand-dark border border-brand-border rounded-xl p-3 text-white text-sm">
                </div>
                <div>
                    <label class="block text-xs font-bold text-zinc-300 uppercase tracking-wider mb-2">Feedback & Results</label>
                    <textarea id="reviewText" rows="4" required class="w-full bg-brand-dark border border-brand-border rounded-xl p-3 text-white text-sm"></textarea>
                </div>
                <button type="submit" class="w-full nc-coral-gradient text-white py-3.5 rounded-xl font-bold text-base">
                    Publish Feedback
                </button>
            </form>
        </div>
    </div>

    <!-- FOOTER - FULL WIDTH -->
    <footer class="bg-brand-card border-t border-brand-border pt-16 pb-12 w-full">
        <div class="w-full px-6 md:px-12 lg:px-16 xl:px-24">
            <div class="grid grid-cols-1 md:grid-cols-12 gap-10 pb-12 border-b border-brand-border">
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
                        High-stakes enterprise strategy, custom web design, and digital transformation systems engineered for scaling business leadership worldwide.
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
                        <li><a href="#" onclick="navigateTo('testimonials'); return false;" class="hover:text-brand-coral transition-colors">Reviews</a></li>
                        <li><a href="#" onclick="navigateTo('pricing'); return false;" class="hover:text-brand-coral transition-colors">Pricing Tiers</a></li>
                        <li><a href="#" onclick="navigateTo('contact'); return false;" class="hover:text-brand-coral transition-colors">Contact Us</a></li>
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
        // Projects Data with Lightbox Information
        const projectsData = [
            {
                id: 1,
                title: "Scalable B2B Web Platform",
                category: "web",
                categoryLabel: "Web Design",
                summary: "Redesigned corporate client onboarding and responsive web architecture.",
                challenge: "The existing legacy site had slow load times and lacked conversion-optimized design tokens.",
                solution: "Engineered a sleek single-page app architecture with Tailwind CSS and responsive UI components.",
                metrics: [
                    { value: "+140%", label: "Conversion Growth" },
                    { value: "14 Days", label: "Sales Cycle Reduced" },
                    { value: "$2.4M", label: "Pipeline Added" }
                ]
            },
            {
                id: 2,
                title: "Omnichannel Revenue Blueprint",
                category: "strategy",
                categoryLabel: "Product Strategy",
                summary: "Realigned product offering unit economics for a scaling tech enterprise.",
                challenge: "Unclear pricing tiers led to customer churn and low margin realization.",
                solution: "Designed a 3-tier value model and strategic roadmap for long-term retainers.",
                metrics: [
                    { value: "3.2x", label: "ROI Achieved" },
                    { value: "35%", label: "Margin Increase" },
                    { value: "100k+", label: "New Users" }
                ]
            },
            {
                id: 3,
                title: "Real Estate Buyer Qualification Funnel",
                category: "realestate",
                categoryLabel: "Real Estate Lead Gens",
                summary: "Automated lead capture dashboard for luxury property developments.",
                challenge: "Unqualified leads were consuming agent bandwidth without converting.",
                solution: "Built a automated quiz system and CRM lead scoring dashboard.",
                metrics: [
                    { value: "4.8x", label: "Qualified Leads" },
                    { value: "85%", label: "Time Saved" },
                    { value: "$12M+", label: "Property Sales" }
                ]
            },
            {
                id: 4,
                title: "Executive Portfolio & Brand Systems",
                category: "web",
                categoryLabel: "Web Design",
                summary: "Ultra-fast portfolio and messaging framework for high-net-worth founders.",
                challenge: "Inconsistent brand identity across digital platforms.",
                solution: "Implemented an obsidian-themed web app with responsive micro-interactions.",
                metrics: [
                    { value: "99/100", label: "PageSpeed Score" },
                    { value: "+210%", label: "Inquiry Rate" },
                    { value: "100%", label: "Client Retention" }
                ]
            }
        ];

        // 8 Verified Client Reviews Dataset
        const clientReviews = [
            {
                name: "Marcus Vance",
                role: "Chief Executive Officer",
                company: "Vance Logistics Group",
                avatar: "https://images.unsplash.com/photo-1534528741775-53994a69daeb?w=150&auto=format&fit=crop&q=80",
                stars: 5,
                text: "Noble Consultant transformed our entire web platform. The strategy provided total clarity on unit economics and elevated our conversion rates by 140% in under six months!"
            },
            {
                name: "Elena Rostova",
                role: "Operations Director",
                company: "Apex Global FinTech",
                avatar: "https://images.unsplash.com/photo-1580489944761-15a19d654956?w=150&auto=format&fit=crop&q=80",
                stars: 5,
                text: "Working directly with Noble Consultant felt like unlocking a cheat code for enterprise growth. Their automated lead capture systems saved us over 30 hours per week."
            },
            {
                name: "Dr. Samuel O'Connor",
                role: "Managing Partner",
                company: "O'Connor Capital",
                avatar: "https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?w=150&auto=format&fit=crop&q=80",
                stars: 5,
                text: "The brand repositioning and executive advisory delivered by Noble Consultant allowed us to command premium retainer rates with high-value clients."
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
                text: "Exceptional advisory. Their deep knowledge of custom web development and modern digital funnels resulted in our highest quarterly performance in company history."
            },
            {
                name: "Amara Nwosu",
                role: "Head of Marketing",
                company: "Aura Commerce",
                avatar: "https://images.unsplash.com/photo-1531746020798-e6953c6e8e04?w=150&auto=format&fit=crop&q=80",
                stars: 5,
                text: "The level of professionalism and integrity from Noble Consultant is unmatched. The customized web system exceeded every benchmark we established."
            },
            {
                name: "Harrison Forde",
                role: "Managing Director",
                company: "Urban Prime Realty",
                avatar: "https://images.unsplash.com/photo-1472099645785-5658abf4ff4e?w=150&auto=format&fit=crop&q=80",
                stars: 5,
                text: "The Real Estate Lead System built by Noble Consultant revolutionized our property launches. We generated over $12M in closed acquisitions."
            },
            {
                name: "Claire Sterling",
                role: "Chief Operating Officer",
                company: "Sterling Ventures",
                avatar: "https://images.unsplash.com/photo-1544005313-94ddf0286df2?w=150&auto=format&fit=crop&q=80",
                stars: 5,
                text: "From concept to full execution, Noble Consultant delivers unparalleled quality and strategic precision. Highly recommended for any serious business."
            }
        ];

        // Multi-page SPA Router Function
        function navigateTo(pageId) {
            const pages = document.querySelectorAll('.page-view');
            pages.forEach(page => page.classList.add('hidden'));

            const targetPage = document.getElementById(`page-${pageId}`);
            if(targetPage) {
                targetPage.classList.remove('hidden');
            }

            // Update Header Nav States
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

            // Dynamic Document Title
            const titles = {
                home: 'Noble Consultant | Elite Enterprise Strategy & Growth',
                about: 'About Us | Noble Consultant',
                services: 'Capabilities & Services | Noble Consultant',
                projects: 'Case Studies & Client Impact | Noble Consultant',
                testimonials: 'Client Reviews & Wall of Love | Noble Consultant',
                pricing: 'Pricing Tiers & Retainers | Noble Consultant',
                contact: 'Request a Free Quote | Noble Consultant'
            };
            document.title = titles[pageId] || 'Noble Consultant';

            window.scrollTo({ top: 0, behavior: 'smooth' });
        }

        // Mobile Menu Drawer Toggle
        function toggleMobileMenu() {
            const menu = document.getElementById('mobileMenu');
            menu.classList.toggle('hidden');
        }

        // Core Pillars Tab Switcher on About Page
        function switchPillarTab(type) {
            const pillarText = document.getElementById('pillarText');
            const btns = ['integrity', 'data', 'partnership'];
            
            btns.forEach(b => {
                const btn = document.getElementById(`pillarBtn-${b}`);
                if(b === type) {
                    btn.className = "px-6 py-3 rounded-xl font-bold text-sm bg-brand-coral text-white transition-all";
                } else {
                    btn.className = "px-6 py-3 rounded-xl font-bold text-sm bg-white/5 text-zinc-300 hover:text-white transition-all";
                }
            });

            const contentMap = {
                integrity: "Direct, transparent recommendations with zero fluff. Every piece of advice and system we construct is centered strictly around your measurable return on investment.",
                data: "Every web architecture and strategic growth roadmap is grounded in detailed analytics, user research, and financial benchmarks.",
                partnership: "We operate as an extension of your leadership team to ensure long-term implementation success and continued scale."
            };

            if(pillarText) pillarText.innerText = contentMap[type];
        }

        // Render Projects Grid with Filter
        function renderProjects(filter = 'all') {
            const container = document.getElementById('projectsContainer');
            if(!container) return;

            const filtered = filter === 'all' ? projectsData : projectsData.filter(p => p.category === filter);

            container.innerHTML = filtered.map(p => `
                <div class="bg-brand-card rounded-3xl p-8 sm:p-10 border border-brand-border hover:border-brand-coral transition-all flex flex-col justify-between">
                    <div>
                        <span class="px-4 py-1.5 rounded-full bg-brand-coralLight text-brand-coral text-xs font-bold uppercase tracking-wider">${p.categoryLabel}</span>
                        <h3 class="text-2xl font-extrabold text-white mt-5">${p.title}</h3>
                        <p class="text-zinc-400 text-base mt-3 leading-relaxed">${p.summary}</p>
                        
                        <div class="mt-6 pt-6 border-t border-brand-border grid grid-cols-3 gap-2 text-center">
                            ${p.metrics.map(m => `
                                <div>
                                    <p class="text-xl sm:text-2xl font-extrabold text-brand-coral">${m.value}</p>
                                    <p class="text-[10px] sm:text-xs text-zinc-400 mt-0.5">${m.label}</p>
                                </div>
                            `).join('')}
                        </div>
                    </div>

                    <button onclick="openCaseStudyModal(${p.id})" class="mt-8 w-full py-3.5 rounded-2xl bg-white/5 hover:bg-brand-coral text-white font-bold text-sm transition-all flex items-center justify-center gap-2">
                        <span>Read Case Study Details</span>
                        <i class="fa-solid fa-arrow-right text-xs"></i>
                    </button>
                </div>
            `).join('');
        }

        // Filter Projects Click Handler
        function filterProjects(filterKey) {
            const btns = document.querySelectorAll('.filter-btn');
            btns.forEach(btn => {
                if(btn.getAttribute('data-filter') === filterKey) {
                    btn.className = "filter-btn active-filter px-5 py-2.5 rounded-xl font-bold text-sm bg-brand-coral text-white transition-all";
                } else {
                    btn.className = "filter-btn px-5 py-2.5 rounded-xl font-bold text-sm bg-white/5 text-zinc-300 hover:text-white transition-all";
                }
            });
            renderProjects(filterKey);
        }

        // Case Study Modal Handler
        function openCaseStudyModal(id) {
            const project = projectsData.find(p => p.id === id);
            if(!project) return;

            const modalContent = document.getElementById('modalContent');
            modalContent.innerHTML = `
                <span class="px-4 py-1.5 rounded-full bg-brand-coralLight text-brand-coral text-xs font-bold uppercase tracking-wider">${project.categoryLabel}</span>
                <h2 class="text-3xl font-extrabold text-white mt-4">${project.title}</h2>
                
                <div class="space-y-6 mt-6">
                    <div>
                        <h4 class="text-sm font-bold text-brand-coral uppercase tracking-wider">The Challenge</h4>
                        <p class="text-zinc-300 text-base mt-1">${project.challenge}</p>
                    </div>
                    <div>
                        <h4 class="text-sm font-bold text-brand-coral uppercase tracking-wider">Our Solution</h4>
                        <p class="text-zinc-300 text-base mt-1">${project.solution}</p>
                    </div>
                </div>

                <div class="mt-8 p-6 bg-brand-surface rounded-2xl border border-brand-border grid grid-cols-3 gap-4 text-center">
                    ${project.metrics.map(m => `
                        <div>
                            <p class="text-2xl font-extrabold text-brand-coral">${m.value}</p>
                            <p class="text-xs text-zinc-400 mt-1">${m.label}</p>
                        </div>
                    `).join('')}
                </div>

                <button onclick="navigateTo('contact'); closeModal('caseStudyModal');" class="mt-8 w-full nc-coral-gradient text-white py-4 rounded-2xl font-bold text-base shadow-lg">
                    Request Similar Growth Results
                </button>
            `;

            document.getElementById('caseStudyModal').classList.remove('hidden');
        }

        function closeModal(modalId) {
            document.getElementById(modalId).classList.add('hidden');
        }

        // Render Reviews List
        function renderReviews() {
            const homeContainer = document.getElementById('homeReviewsContainer');
            const fullContainer = document.getElementById('fullReviewsContainer');

            let html = '';
            clientReviews.forEach(review => {
                let starsHtml = '<i class="fa-solid fa-star text-amber-400 text-xs"></i>'.repeat(review.stars);

                html += `
                    <div class="bg-brand-card p-8 rounded-3xl border border-brand-border hover:border-brand-coral/40 transition-all flex flex-col justify-between">
                        <div>
                            <div class="flex items-center gap-1 mb-5">
                                ${starsHtml}
                            </div>
                            <p class="text-zinc-300 text-base leading-relaxed italic mb-8">"${review.text}"</p>
                        </div>
                        <div class="flex items-center gap-4 pt-5 border-t border-brand-border">
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
                        <div class="bg-brand-card p-8 rounded-3xl border border-brand-border flex flex-col justify-between">
                            <div>
                                <div class="flex items-center gap-1 mb-4">${starsHtml}</div>
                                <p class="text-zinc-300 text-sm leading-relaxed mb-6">"${review.text}"</p>
                            </div>
                            <div class="flex items-center gap-4 pt-4 border-t border-brand-border">
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

        // Review Submission Modal
        function openReviewModal() {
            document.getElementById('reviewModal').classList.remove('hidden');
        }

        function handleReviewSubmit(e) {
            e.preventDefault();
            const name = document.getElementById('reviewName').value;
            const role = document.getElementById('reviewRole').value;
            const text = document.getElementById('reviewText').value;

            clientReviews.unshift({
                name: name,
                role: role,
                company: "Verified Partner",
                avatar: "https://images.unsplash.com/photo-1535713875002-d1d0cf377fde?w=150&auto=format&fit=crop&q=80",
                stars: 5,
                text: text
            });

            renderReviews();
            closeModal('reviewModal');
            showToast("Feedback Published!", "Thank you for sharing your review with Noble Consultant.");
        }

        // ROI Estimator Calculation Logic
        function calculateEstimate() {
            const baseObj = parseFloat(document.getElementById('calcObjective').value);
            const durationMultiplier = parseFloat(document.getElementById('calcDuration').value);
            const total = Math.round(baseObj * durationMultiplier);
            document.getElementById('calcTotal').innerText = `$${total.toLocaleString()} USD`;
        }

        // Pricing Toggle Switcher Logic
        let isAnnual = false;
        function togglePricingBilling() {
            isAnnual = !isAnnual;
            const dot = document.getElementById('toggleDot');
            const mLabel = document.getElementById('monthlyLabel');
            const aLabel = document.getElementById('annualLabel');

            if(isAnnual) {
                dot.style.transform = 'translateX(28px)';
                mLabel.className = 'text-sm font-bold text-zinc-400';
                aLabel.className = 'text-sm font-bold text-white';

                document.getElementById('priceTier1').innerText = '$2,000';
                document.getElementById('priceTier2').innerText = '$4,640';
            } else {
                dot.style.transform = 'translateX(0px)';
                mLabel.className = 'text-sm font-bold text-white';
                aLabel.className = 'text-sm font-bold text-zinc-400';

                document.getElementById('priceTier1').innerText = '$2,500';
                document.getElementById('priceTier2').innerText = '$5,800';
            }
        }

        // Time slot picker button selector
        function selectSlot(btn) {
            const btns = document.querySelectorAll('.slot-btn');
            btns.forEach(b => {
                b.classList.remove('bg-brand-coral', 'text-white', 'border-brand-coral');
                b.classList.add('border-brand-border', 'text-zinc-300');
            });
            btn.classList.add('bg-brand-coral', 'text-white', 'border-brand-coral');
        }

        // Custom Toast Notification Function
        function showToast(title, desc) {
            const toast = document.createElement('div');
            toast.className = "fixed bottom-8 right-8 bg-brand-coral text-white px-8 py-5 rounded-2xl shadow-2xl z-50 flex items-center gap-4 animate-bounce";
            toast.innerHTML = `
                <i class="fa-solid fa-circle-check text-2xl"></i>
                <div>
                    <h5 class="font-bold text-base">${title}</h5>
                    <p class="text-xs text-white/90">${desc}</p>
                </div>
            `;
            document.body.appendChild(toast);
            setTimeout(() => {
                toast.remove();
            }, 4000);
        }

        // Form Submission Handler
        function handleFormSubmit(e) {
            e.preventDefault();
            showToast("Quote Request Received!", "Noble Consultant team will reach out within 24 hours.");
            document.getElementById('contactForm').reset();
        }

        // Initialize App on Window Load
        window.onload = function() {
            renderProjects('all');
            renderReviews();
        };
    </script>
</body>
</html>
