# minhee
<!DOCTYPE html>
<html lang="ko" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ARCHI-TECHTE / 건축설계 포트폴리오</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Google Fonts: Playfair Display (Heading), Inter (Body) -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=Playfair+Display:ital,wght@0,400;0,600;0,700;1,400&display=swap" rel="stylesheet">
    <!-- Font Awesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <!-- Custom Style Config -->
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                        serif: ['Playfair Display', 'serif'],
                    },
                    colors: {
                        arch: {
                            950: '#0a0a0a',
                            900: '#121212',
                            800: '#1c1c1c',
                            700: '#2d2d2d',
                            400: '#a3a3a3',
                            300: '#d4d4d4',
                            100: '#f5f5f5',
                            gold: '#c5a880',
                            goldHover: '#b3956d'
                        }
                    }
                }
            }
        }
    </script>
    
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #0a0a0a;
            color: #f5f5f5;
        }
        /* Custom scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #0a0a0a;
        }
        ::-webkit-scrollbar-thumb {
            background: #2d2d2d;
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #c5a880;
        }
        /* Grid blueprint pattern background */
        .bg-blueprint {
            background-size: 40px 40px;
            background-image: linear-gradient(to right, rgba(197, 168, 128, 0.05) 1px, transparent 1px),
                              linear-gradient(to bottom, rgba(197, 168, 128, 0.05) 1px, transparent 1px);
        }
    </style>
</head>
<body class="overflow-x-hidden">

<!-- Navigation -->
<nav class="fixed top-0 left-0 w-full z-50 bg-arch-950/80 backdrop-blur-md border-b border-arch-800/50 transition-all duration-300" id="navbar">
    <div class="max-w-7xl mx-auto px-6 h-20 flex items-center justify-between">
        <!-- Logo -->
        <a href="#" class="flex items-center space-x-3 group">
            <div class="relative w-10 h-10 border border-arch-gold flex items-center justify-center overflow-hidden transition-all duration-300 group-hover:bg-arch-gold">
                <span class="font-serif text-lg font-bold tracking-widest text-white transition-colors duration-300 group-hover:text-arch-950">K</span>
                <!-- Abstract geometric overlay -->
                <div class="absolute inset-0 border-t border-r border-transparent group-hover:border-arch-950 transition-all duration-300"></div>
            </div>
            <div class="flex flex-col">
                <span class="font-serif text-lg font-bold tracking-wider text-white">KIM WOO JIN</span>
                <span class="text-[10px] tracking-[0.3em] text-arch-gold">ARCHITECT</span>
            </div>
        </a>

        <!-- Desktop Menu -->
        <div class="hidden md:flex items-center space-x-10 text-sm font-medium tracking-widest text-arch-300">
            <a href="#about" class="hover:text-arch-gold transition-colors duration-300">ABOUT</a>
            <a href="#philosophy" class="hover:text-arch-gold transition-colors duration-300">PHILOSOPHY</a>
            <a href="#blueprint" class="hover:text-arch-gold transition-colors duration-300">EXPERIENCE</a>
            <a href="#portfolio" class="hover:text-arch-gold transition-colors duration-300">PORTFOLIO</a>
            <a href="#contact" class="px-5 py-2.5 border border-arch-gold text-arch-gold hover:bg-arch-gold hover:text-arch-950 transition-all duration-300 rounded-sm">CONTACT</a>
        </div>

        <!-- Mobile Menu Toggle Button -->
        <button class="md:hidden text-arch-100 hover:text-arch-gold transition-colors duration-300 focus:outline-none" id="mobile-menu-btn" aria-label="메뉴 열기">
            <i class="fa-solid fa-bars-staggered text-2xl"></i>
        </button>
    </div>

    <!-- Mobile Drawer Menu -->
    <div id="mobile-drawer" class="fixed top-0 right-0 h-screen w-80 bg-arch-900 border-l border-arch-800 p-8 transform translate-x-full transition-transform duration-300 ease-in-out z-50 shadow-2xl">
        <div class="flex justify-end mb-12">
            <button id="close-drawer-btn" class="text-arch-400 hover:text-arch-gold text-2xl" aria-label="메뉴 닫기">
                <i class="fa-solid fa-xmark"></i>
            </button>
        </div>
        <div class="flex flex-col space-y-8 text-lg font-medium tracking-widest">
            <a href="#about" class="mobile-link hover:text-arch-gold transition-colors">ABOUT</a>
            <a href="#philosophy" class="mobile-link hover:text-arch-gold transition-colors">PHILOSOPHY</a>
            <a href="#blueprint" class="mobile-link hover:text-arch-gold transition-colors">EXPERIENCE</a>
            <a href="#portfolio" class="mobile-link hover:text-arch-gold transition-colors">PORTFOLIO</a>
            <a href="#contact" class="mobile-link inline-block text-center py-3 border border-arch-gold text-arch-gold hover:bg-arch-gold hover:text-arch-950 transition-colors">CONTACT</a>
        </div>
    </div>
</nav>

<!-- Hero Section -->
<section class="relative min-h-screen flex items-center justify-center pt-20 overflow-hidden" id="hero">
    <!-- Background Image with Overlay -->
    <div class="absolute inset-0 bg-[url('https://images.unsplash.com/photo-1600585154340-be6161a56a0c?q=80&w=2070')] bg-cover bg-center opacity-30"></div>
    <div class="absolute inset-0 bg-gradient-to-t from-arch-950 via-arch-950/80 to-transparent"></div>
    <div class="absolute inset-0 bg-blueprint"></div>

    <!-- Decorative Structural Lines -->
    <div class="absolute left-[10%] top-0 h-full w-[1px] bg-arch-gold/10 hidden md:block"></div>
    <div class="absolute right-[10%] top-0 h-full w-[1px] bg-arch-gold/10 hidden md:block"></div>
    <div class="absolute left-0 top-[30%] w-full h-[1px] bg-arch-gold/10 hidden md:block"></div>

    <!-- Hero Content -->
    <div class="relative max-w-7xl mx-auto px-6 w-full z-10 grid grid-cols-1 lg:grid-cols-12 gap-12 items-center py-12">
        <div class="lg:col-span-8 flex flex-col space-y-6">
            <div class="inline-flex items-center space-x-3 text-arch-gold font-medium tracking-[0.3em] text-xs md:text-sm">
                <span class="w-8 h-[1px] bg-arch-gold"></span>
                <span>KIM WOO JIN ARCHITECTS</span>
            </div>
            
            <h1 class="font-serif text-4xl sm:text-5xl md:text-7xl lg:text-8xl font-bold leading-tight text-white tracking-tight">
                Structuring <br>
                <span class="text-transparent bg-clip-text bg-gradient-to-r from-white via-arch-300 to-arch-gold">Space & Light</span>
            </h1>
            
            <p class="text-arch-400 text-sm md:text-lg max-w-xl font-light leading-relaxed">
                공간은 인간의 삶을 담는 그릇이며, 빛은 그 공간에 생명을 불어넣는 조각가입니다. 지속 가능한 친환경 설계와 시대를 초월하는 미니멀리즘을 조화롭게 구현합니다.
            </p>
            
            <div class="pt-4 flex flex-wrap gap-4">
                <a href="#portfolio" class="px-8 py-4 bg-arch-gold hover:bg-arch-goldHover text-arch-950 text-sm font-semibold tracking-widest rounded-sm transition-all duration-300 flex items-center space-x-3">
                    <span>PORTFOLIO</span>
                    <i class="fa-solid fa-arrow-right"></i>
                </a>
                <a href="#blueprint" class="px-8 py-4 border border-arch-700 hover:border-arch-gold text-white hover:text-arch-gold text-sm font-semibold tracking-widest rounded-sm transition-all duration-300">
                    BLUEPRINT VIEW
                </a>
            </div>
        </div>

        <!-- Architectural Stats Info Card -->
        <div class="lg:col-span-4 bg-arch-900/40 border border-arch-800 p-8 rounded-lg backdrop-blur-md relative overflow-hidden group">
            <div class="absolute -right-12 -bottom-12 w-48 h-48 border border-arch-gold/10 rounded-full group-hover:scale-110 transition-transform duration-500"></div>
            <h3 class="font-serif text-xl font-bold mb-6 text-white border-b border-arch-800 pb-4">핵심 디자인 지표</h3>
            
            <div class="space-y-6">
                <div>
                    <div class="flex justify-between text-xs text-arch-400 mb-2 tracking-wider">
                        <span>SUSTAINABILITY (친환경성)</span>
                        <span>95%</span>
                    </div>
                    <div class="h-1 bg-arch-800 rounded-full overflow-hidden">
                        <div class="h-full bg-arch-gold rounded-full" style="width: 95%"></div>
                    </div>
                </div>
                <div>
                    <div class="flex justify-between text-xs text-arch-400 mb-2 tracking-wider">
                        <span>NATURAL LIGHTING (자연 채광 극대화)</span>
                        <span>90%</span>
                    </div>
                    <div class="h-1 bg-arch-800 rounded-full overflow-hidden">
                        <div class="h-full bg-arch-gold rounded-full" style="width: 90%"></div>
                    </div>
                </div>
                <div>
                    <div class="flex justify-between text-xs text-arch-400 mb-2 tracking-wider">
                        <span>STRUCTURAL INTEGRITY (구조적 영속성)</span>
                        <span>100%</span>
                    </div>
                    <div class="h-1 bg-arch-800 rounded-full overflow-hidden">
                        <div class="h-full bg-arch-gold rounded-full" style="width: 100%"></div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Scroll Down Indicator -->
    <div class="absolute bottom-8 left-1/2 -translate-x-1/2 flex flex-col items-center space-y-2 text-xs tracking-widest text-arch-400">
        <span class="animate-bounce"><i class="fa-solid fa-chevron-down text-arch-gold text-sm"></i></span>
        <span>SCROLL DOWN</span>
    </div>
</section>

<!-- About Section & Stats -->
<section id="about" class="py-24 border-t border-arch-900 bg-arch-950 relative">
    <div class="max-w-7xl mx-auto px-6">
        <div class="grid grid-cols-1 lg:grid-cols-12 gap-16 items-center">
            
            <!-- Architect Portrait / Image Collage -->
            <div class="lg:col-span-5 relative">
                <!-- Outer structural frame -->
                <div class="absolute -top-4 -left-4 w-full h-full border border-arch-gold/30 rounded-sm z-0"></div>
                <!-- Main Portrait (Beautiful minimalist architectural building/office mockup) -->
                <div class="relative z-10 overflow-hidden bg-arch-900 border border-arch-800 rounded-sm">
                    <img src="https://images.unsplash.com/photo-1577415124269-fc1140a69e91?q=80&w=1964" alt="Architect Portrait" class="w-full h-[450px] object-cover filter grayscale hover:grayscale-0 transition-all duration-700">
                </div>
                <!-- Mini overlay stat box -->
                <div class="absolute bottom-6 -right-6 bg-arch-gold text-arch-950 p-6 rounded-sm z-20 shadow-xl max-w-xs">
                    <p class="font-serif text-2xl font-bold leading-tight">"공간을 짓는다는 것은 가치관을 설계하는 것과 같습니다."</p>
                </div>
            </div>

            <!-- Intro text and key stats -->
            <div class="lg:col-span-7 flex flex-col justify-center space-y-8">
                <div class="space-y-3">
                    <span class="text-arch-gold text-xs font-bold tracking-[0.3em]">ABOUT ME</span>
                    <h2 class="font-serif text-3xl md:text-5xl font-bold text-white">김우진 / Lead Architect</h2>
                </div>
                
                <p class="text-arch-400 font-light leading-relaxed">
                    대한민국 서울을 기반으로 활동 중인 건축가 김우진입니다. 한예종 건축학과를 최우수 졸업하고 글로벌 탑티어 건축사무소 OMA와 켄고 쿠마 사무소에서 오랜 실무 경험을 다졌습니다. 
                </p>
                <p class="text-arch-400 font-light leading-relaxed">
                    우리의 공간 설계는 단순한 형태 구상을 뛰어넘어, 그 공간을 누릴 사람들의 고유한 동선과 대지가 품고 있는 역사적, 자연적 컨텍스트를 치밀하게 조율하는 과정입니다. 거주성과 조형미의 경계에서 시대를 아우르는 지속 가능한 현대식 구조물을 제안합니다.
                </p>

                <!-- Key Stat Metrics Grid -->
                <div class="grid grid-cols-2 md:grid-cols-4 gap-6 pt-6 border-t border-arch-800">
                    <div class="text-center md:text-left">
                        <span class="block font-serif text-3xl md:text-4xl font-bold text-arch-gold">12+</span>
                        <span class="text-xs text-arch-400 tracking-wider">경력 연수 (Years)</span>
                    </div>
                    <div class="text-center md:text-left">
                        <span class="block font-serif text-3xl md:text-4xl font-bold text-arch-gold">45+</span>
                        <span class="text-xs text-arch-400 tracking-wider">완공 프로젝트 (Projects)</span>
                    </div>
                    <div class="text-center md:text-left">
                        <span class="block font-serif text-3xl md:text-4xl font-bold text-arch-gold">8+</span>
                        <span class="text-xs text-arch-400 tracking-wider">디자인 어워드 수상</span>
                    </div>
                    <div class="text-center md:text-left">
                        <span class="block font-serif text-3xl md:text-4xl font-bold text-arch-gold">100%</span>
                        <span class="text-xs text-arch-400 tracking-wider">친환경 자재 지향</span>
                    </div>
                </div>
            </div>

        </div>
    </div>
</section>

<!-- Design Philosophy Section -->
<section id="philosophy" class="py-24 bg-arch-900 border-y border-arch-800/80">
    <div class="max-w-7xl mx-auto px-6">
        <div class="text-center max-w-3xl mx-auto mb-16 space-y-4">
            <span class="text-arch-gold text-xs font-bold tracking-[0.3em]">OUR MANIFESTO</span>
            <h2 class="font-serif text-3xl md:text-5xl font-bold text-white">건축 디자인 철학</h2>
            <p class="text-arch-400 font-light text-sm md:text-base">형태는 쓰임새를 따르고, 쓰임새는 자연의 품격을 담아야 합니다. 3가지 가치 핵심을 타협 없이 고수합니다.</p>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
            <!-- Philosophy Card 1 -->
            <div class="p-8 bg-arch-950 border border-arch-800 rounded-sm hover:border-arch-gold/50 transition-all duration-300 flex flex-col space-y-5 group">
                <div class="w-12 h-12 rounded-sm bg-arch-900 flex items-center justify-center border border-arch-800 group-hover:bg-arch-gold group-hover:border-arch-gold transition-all duration-300">
                    <i class="fa-solid fa-compass-drafting text-arch-gold group-hover:text-arch-950 transition-colors duration-300 text-xl"></i>
                </div>
                <h3 class="font-serif text-xl font-bold text-white tracking-wide">01. 형태와 공간의 긴장감</h3>
                <p class="text-arch-400 font-light text-sm leading-relaxed">
                    불필요한 장식을 완전히 걷어내어 극단적인 여백의 미를 구현하며, 엄격한 비례와 매스(Mass) 설계를 통해 구조적 긴장감과 아름다움을 창조합니다.
                </p>
            </div>

            <!-- Philosophy Card 2 -->
            <div class="p-8 bg-arch-950 border border-arch-800 rounded-sm hover:border-arch-gold/50 transition-all duration-300 flex flex-col space-y-5 group">
                <div class="w-12 h-12 rounded-sm bg-arch-900 flex items-center justify-center border border-arch-800 group-hover:bg-arch-gold group-hover:border-arch-gold transition-all duration-300">
                    <i class="fa-solid fa-sun text-arch-gold group-hover:text-arch-950 transition-colors duration-300 text-xl"></i>
                </div>
                <h3 class="font-serif text-xl font-bold text-white tracking-wide">02. 빛과 대기의 영속적인 변화</h3>
                <p class="text-arch-400 font-light text-sm leading-relaxed">
                    시간대에 따라 무작위적으로 침투하는 자연 채광과 그림자 패턴을 인테리어 핵심 요소로 설계하여, 하루 중 단 한순간도 같지 않은 역동적인 내부 무드를 자아냅니다.
                </p>
            </div>

            <!-- Philosophy Card 3 -->
            <div class="p-8 bg-arch-950 border border-arch-800 rounded-sm hover:border-arch-gold/50 transition-all duration-300 flex flex-col space-y-5 group">
                <div class="w-12 h-12 rounded-sm bg-arch-900 flex items-center justify-center border border-arch-800 group-hover:bg-arch-gold group-hover:border-arch-gold transition-all duration-300">
                    <i class="fa-solid fa-leaf text-arch-gold group-hover:text-arch-950 transition-colors duration-300 text-xl"></i>
                </div>
                <h3 class="font-serif text-xl font-bold text-white tracking-wide">03. 대지 순환과 친환경적 배려</h3>
                <p class="text-arch-400 font-light text-sm leading-relaxed">
                    건물이 자리 잡은 지형의 바람길과 고저차를 훼손하지 않는 자연 합일의 평면도를 완성하고 고단열, 친환경 천연 마감 소재를 최우선으로 선별합니다.
                </p>
            </div>
        </div>
    </div>
</section>

<!-- Interactive Blueprint Layer Explorer (WOW FACTOR) -->
<section id="blueprint" class="py-24 bg-arch-950 relative overflow-hidden">
    <!-- Grid blueprint pattern overlay background -->
    <div class="absolute inset-0 bg-blueprint opacity-60"></div>
    
    <div class="max-w-7xl mx-auto px-6 relative z-10">
        <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 items-center">
            
            <!-- Left Info Panel -->
            <div class="lg:col-span-4 flex flex-col justify-center space-y-6">
                <div>
                    <span class="text-arch-gold text-xs font-bold tracking-[0.3em]">INTERACTIVE SIMULATION</span>
                    <h2 class="font-serif text-3xl md:text-4xl font-bold text-white mt-2">상호작용형 설계도 분석기</h2>
                </div>
                <p class="text-arch-400 text-sm font-light leading-relaxed">
                    우리가 설계하는 주거용 단독주택 'House of Void'의 실측 도면층입니다. 오른쪽 스위치를 클릭해 설계의 층별 레이어(구조벽, 가구, 조명, 기류 배정)를 중첩시켜 설계 과정을 간접 체험해 보세요.
                </p>

                <!-- Toggle Controls -->
                <div class="space-y-4 pt-4 border-t border-arch-800">
                    <!-- Switch 1: Wall & Structure -->
                    <div class="flex items-center justify-between p-3 bg-arch-900/60 rounded-md border border-arch-800">
                        <div class="flex items-center space-x-3">
                            <i class="fa-solid fa-layer-group text-slate-400"></i>
                            <span class="text-xs font-semibold tracking-wider text-white">01. 벽체 및 중심 뼈대 (Structure)</span>
                        </div>
                        <button onclick="toggleBlueprintLayer('wall-layer')" id="btn-wall-layer" class="w-12 h-6 rounded-full bg-arch-gold transition-colors duration-300 focus:outline-none relative">
                            <div class="w-5 h-5 rounded-full bg-arch-950 absolute top-[2px] right-[2px] transition-all duration-300" id="dot-wall-layer"></div>
                        </button>
                    </div>

                    <!-- Switch 2: Furniture Layout -->
                    <div class="flex items-center justify-between p-3 bg-arch-900/60 rounded-md border border-arch-800">
                        <div class="flex items-center space-x-3">
                            <i class="fa-solid fa-couch text-amber-500"></i>
                            <span class="text-xs font-semibold tracking-wider text-white">02. 가구 배치안 (Furniture)</span>
                        </div>
                        <button onclick="toggleBlueprintLayer('furniture-layer')" id="btn-furniture-layer" class="w-12 h-6 rounded-full bg-arch-gold transition-colors duration-300 focus:outline-none relative">
                            <div class="w-5 h-5 rounded-full bg-arch-950 absolute top-[2px] right-[2px] transition-all duration-300" id="dot-furniture-layer"></div>
                        </button>
                    </div>

                    <!-- Switch 3: Lighting & Electrical -->
                    <div class="flex items-center justify-between p-3 bg-arch-900/60 rounded-md border border-arch-800">
                        <div class="flex items-center space-x-3">
                            <i class="fa-solid fa-lightbulb text-yellow-400 animate-pulse"></i>
                            <span class="text-xs font-semibold tracking-wider text-white">03. 조명 & 전기 도면 (Lighting)</span>
                        </div>
                        <button onclick="toggleBlueprintLayer('lighting-layer')" id="btn-lighting-layer" class="w-12 h-6 rounded-full bg-arch-gold transition-colors duration-300 focus:outline-none relative">
                            <div class="w-5 h-5 rounded-full bg-arch-950 absolute top-[2px] right-[2px] transition-all duration-300" id="dot-lighting-layer"></div>
                        </button>
                    </div>

                    <!-- Switch 4: Circulation & Green Paths -->
                    <div class="flex items-center justify-between p-3 bg-arch-900/60 rounded-md border border-arch-800">
                        <div class="flex items-center space-x-3">
                            <i class="fa-solid fa-wind text-teal-400"></i>
                            <span class="text-xs font-semibold tracking-wider text-white">04. 바람길 & 친환경 요소 (Eco Paths)</span>
                        </div>
                        <button onclick="toggleBlueprintLayer('eco-layer')" id="btn-eco-layer" class="w-12 h-6 rounded-full bg-arch-gold transition-colors duration-300 focus:outline-none relative">
                            <div class="w-5 h-5 rounded-full bg-arch-950 absolute top-[2px] right-[2px] transition-all duration-300" id="dot-eco-layer"></div>
                        </button>
                    </div>
                </div>
            </div>

            <!-- Right Interactive SVG Box -->
            <div class="lg:col-span-8 bg-arch-900/80 border border-arch-800/80 rounded-lg p-6 flex items-center justify-center relative min-h-[450px]">
                <div class="absolute top-4 left-4 text-[10px] tracking-widest text-arch-gold font-mono uppercase">PROJECT: HOUSE OF VOID / FLOOR PLAN</div>
                
                <!-- The Live SVG Rendered Area -->
                <svg viewBox="0 0 800 500" class="w-full h-auto max-w-2xl" id="blueprint-svg">
                    <!-- Base grid layout -->
                    <rect width="800" height="500" fill="transparent"/>
                    
                    <!-- 1. WALL & STRUCTURE LAYER -->
                    <g id="wall-layer" class="transition-opacity duration-300 opacity-100">
                        <!-- Structural outer boundaries -->
                        <rect x="100" y="100" width="600" height="300" fill="none" stroke="#ffffff" stroke-width="4" stroke-dasharray="5 2" opacity="0.4"/>
                        <!-- Inner partition heavy walls -->
                        <line x1="250" y1="100" x2="250" y2="280" stroke="#f5f5f5" stroke-width="6"/>
                        <line x1="250" y1="340" x2="250" y2="400" stroke="#f5f5f5" stroke-width="6"/>
                        <line x1="480" y1="100" x2="480" y2="250" stroke="#f5f5f5" stroke-width="6"/>
                        <line x1="480" y1="250" x2="700" y2="250" stroke="#f5f5f5" stroke-width="6"/>
                        
                        <!-- Column structures -->
                        <rect x="90" y="90" width="20" height="20" fill="#c5a880"/>
                        <rect x="690" y="90" width="20" height="20" fill="#c5a880"/>
                        <rect x="90" y="390" width="20" height="20" fill="#c5a880"/>
                        <rect x="690" y="390" width="20" height="20" fill="#c5a880"/>
                        <rect x="240" y="270" width="20" height="20" fill="#c5a880"/>
                        <rect x="470" y="240" width="20" height="20" fill="#c5a880"/>
                    </g>

                    <!-- 2. FURNITURE LAYER -->
                    <g id="furniture-layer" class="transition-opacity duration-300 opacity-100">
                        <!-- Master Living Bed -->
                        <rect x="130" y="150" width="80" height="90" fill="none" stroke="#d97706" stroke-width="2" rx="4"/>
                        <rect x="140" y="160" width="30" height="20" fill="none" stroke="#d97706" stroke-width="1.5" rx="2"/>
                        <rect x="180" y="160" width="30" height="20" fill="none" stroke="#d97706" stroke-width="1.5" rx="2"/>
                        <path d="M 130 200 L 210 200" stroke="#d97706" stroke-width="1.5"/>
                        <text x="145" y="235" fill="#d97706" font-size="10" font-family="sans-serif">MASTER BED</text>
                        
                        <!-- Dining Table & Chairs -->
                        <rect x="300" y="160" width="120" height="60" fill="none" stroke="#d97706" stroke-width="2" rx="2"/>
                        <!-- Chairs -->
                        <circle cx="330" cy="145" r="8" fill="none" stroke="#d97706" stroke-width="1.5"/>
                        <circle cx="390" cy="145" r="8" fill="none" stroke="#d97706" stroke-width="1.5"/>
                        <circle cx="330" cy="235" r="8" fill="none" stroke="#d97706" stroke-width="1.5"/>
                        <circle cx="390" cy="235" r="8" fill="none" stroke="#d97706" stroke-width="1.5"/>
                        <text x="325" y="195" fill="#d97706" font-size="11" font-family="sans-serif">DINING TABLE</text>

                        <!-- Large Sofa Area -->
                        <path d="M 520 150 L 660 150 L 660 210" fill="none" stroke="#d97706" stroke-width="2"/>
                        <rect x="530" y="160" width="110" height="30" fill="none" stroke="#d97706" stroke-width="1"/>
                        <text x="560" y="140" fill="#d97706" font-size="10" font-family="sans-serif">LIVING SOFA</text>
                    </g>

                    <!-- 3. LIGHTING LAYER -->
                    <g id="lighting-layer" class="transition-opacity duration-300 opacity-100">
                        <!-- Spotlights and ceiling electrical wire paths -->
                        <!-- Dining Pendant Lights -->
                        <circle cx="330" cy="190" r="5" fill="#eab308"/>
                        <circle cx="390" cy="190" r="5" fill="#eab308"/>
                        <!-- Light halo rings -->
                        <circle cx="330" cy="190" r="25" fill="none" stroke="#eab308" stroke-width="1" stroke-dasharray="3 3"/>
                        <circle cx="390" cy="190" r="25" fill="none" stroke="#eab308" stroke-width="1" stroke-dasharray="3 3"/>

                        <!-- Spotlights -->
                        <circle cx="170" cy="130" r="4" fill="#eab308"/>
                        <circle cx="590" cy="120" r="4" fill="#eab308"/>
                        <circle cx="590" cy="300" r="4" fill="#eab308"/>
                        
                        <!-- Curved wire path representations -->
                        <path d="M 170 130 Q 250 150 330 190" fill="none" stroke="#eab308" stroke-width="1.5" stroke-dasharray="4 4"/>
                        <path d="M 390 190 Q 490 155 590 120" fill="none" stroke="#eab308" stroke-width="1.5" stroke-dasharray="4 4"/>
                        <path d="M 590 120 L 590 300" fill="none" stroke="#eab308" stroke-width="1.5" stroke-dasharray="4 4"/>
                    </g>

                    <!-- 4. ECO PATHS & AIRFLOW LAYER -->
                    <g id="eco-layer" class="transition-opacity duration-300 opacity-100">
                        <!-- Blue Arrows representing Cool Summer Airflow Path -->
                        <path d="M 100 320 Q 200 320 250 310" fill="none" stroke="#2dd4bf" stroke-width="3" marker-end="url(#arrow)" stroke-dasharray="5 5" class="animate-[dash_2s_linear_infinite]"/>
                        <path d="M 250 310 Q 300 300 480 320" fill="none" stroke="#2dd4bf" stroke-width="3" stroke-dasharray="5 5"/>
                        <path d="M 480 320 Q 590 330 700 320" fill="none" stroke="#2dd4bf" stroke-width="3" stroke-dasharray="5 5"/>
                        <text x="110" y="345" fill="#2dd4bf" font-size="10" font-family="sans-serif">◀ SUMMER WINDWAY</text>

                        <!-- Indoor pocket gardens/eco voids -->
                        <rect x="280" y="290" width="160" height="70" fill="none" stroke="#2dd4bf" stroke-width="2" rx="15" stroke-dasharray="4 4"/>
                        <text x="315" y="330" fill="#2dd4bf" font-size="11" font-family="sans-serif">ECO COURTYARD</text>
                        <!-- Small green plants (Abstract SVG) -->
                        <path d="M 295 340 Q 300 320 310 335 Q 320 325 315 340 Z" fill="#2dd4bf"/>
                        <path d="M 415 340 Q 420 320 430 335 Q 440 325 435 340 Z" fill="#2dd4bf"/>
                    </g>
                    
                    <!-- SVG marker definition for wind directions -->
                    <defs>
                        <marker id="arrow" viewBox="0 0 10 10" refX="5" refY="5" markerWidth="6" markerHeight="6" orient="auto-start-reverse">
                            <path d="M 0 0 L 10 5 L 0 10 z" fill="#2dd4bf" />
                        </marker>
                    </defs>
                </svg>
            </div>

        </div>
    </div>
</section>

<!-- Portfolio Section -->
<section id="portfolio" class="py-24 bg-arch-900 border-t border-arch-800">
    <div class="max-w-7xl mx-auto px-6">
        
        <!-- Header Info -->
        <div class="flex flex-col md:flex-row md:items-end justify-between mb-16 space-y-4 md:space-y-0">
            <div class="space-y-3">
                <span class="text-arch-gold text-xs font-bold tracking-[0.3em]">PORTFOLIO</span>
                <h2 class="font-serif text-3xl md:text-5xl font-bold text-white">완공 프로젝트 아카이브</h2>
            </div>
            
            <!-- Filter Tabs -->
            <div class="flex flex-wrap gap-2 text-xs md:text-sm font-semibold tracking-widest border border-arch-800 p-1.5 rounded-md bg-arch-950/60">
                <button onclick="filterPortfolio('all')" id="filter-all" class="portfolio-filter-btn px-4 py-2 bg-arch-gold text-arch-950 rounded-sm transition-all duration-300">ALL</button>
                <button onclick="filterPortfolio('residential')" id="filter-residential" class="portfolio-filter-btn px-4 py-2 hover:text-arch-gold rounded-sm transition-all duration-300">RESIDENTIAL</button>
                <button onclick="filterPortfolio('commercial')" id="filter-commercial" class="portfolio-filter-btn px-4 py-2 hover:text-arch-gold rounded-sm transition-all duration-300">COMMERCIAL</button>
                <button onclick="filterPortfolio('public')" id="filter-public" class="portfolio-filter-btn px-4 py-2 hover:text-arch-gold rounded-sm transition-all duration-300">PUBLIC</button>
                <button onclick="filterPortfolio('concept')" id="filter-concept" class="portfolio-filter-btn px-4 py-2 hover:text-arch-gold rounded-sm transition-all duration-300">CONCEPT</button>
            </div>
        </div>

        <!-- Portfolio Cards Grid -->
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8" id="portfolio-container">
            
            <!-- Project Card 1: Residential -->
            <div class="project-card group bg-arch-950 border border-arch-800/80 rounded-md overflow-hidden relative transition-all duration-500 hover:-translate-y-2 hover:border-arch-gold/50 cursor-pointer" data-category="residential" onclick="openProjectModal('void-house')">
                <div class="relative overflow-hidden h-72">
                    <img src="https://images.unsplash.com/photo-1600596542815-ffad4c1539a9?q=80&w=2075" alt="House of Void" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110">
                    <div class="absolute inset-0 bg-gradient-to-t from-arch-950/90 via-transparent to-transparent opacity-80"></div>
                    <span class="absolute top-4 left-4 text-[10px] tracking-widest font-bold px-3 py-1 border border-arch-gold bg-arch-950 text-arch-gold rounded-full uppercase">Residential</span>
                </div>
                <div class="p-6 space-y-3">
                    <h3 class="font-serif text-xl font-bold text-white group-hover:text-arch-gold transition-colors">House of Void (보이드 하우스)</h3>
                    <p class="text-arch-400 font-light text-xs leading-relaxed line-clamp-2">중앙 보이드 안마당을 거쳐 자연광을 무제한으로 유입시키는 단독 단층 모던 주택입니다.</p>
                    <div class="flex justify-between items-center text-[11px] text-arch-gold font-semibold pt-4 border-t border-arch-900 uppercase tracking-widest">
                        <span>SEOUL, KOREA</span>
                        <span>View Details <i class="fa-solid fa-arrow-right ml-1"></i></span>
                    </div>
                </div>
            </div>

            <!-- Project Card 2: Commercial -->
            <div class="project-card group bg-arch-950 border border-arch-800/80 rounded-md overflow-hidden relative transition-all duration-500 hover:-translate-y-2 hover:border-arch-gold/50 cursor-pointer" data-category="commercial" onclick="openProjectModal('cube-tower')">
                <div class="relative overflow-hidden h-72">
                    <img src="https://images.unsplash.com/photo-1486406146926-c627a92ad1ab?q=80&w=2070" alt="Cube Tower" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110">
                    <div class="absolute inset-0 bg-gradient-to-t from-arch-950/90 via-transparent to-transparent opacity-80"></div>
                    <span class="absolute top-4 left-4 text-[10px] tracking-widest font-bold px-3 py-1 border border-arch-gold bg-arch-950 text-arch-gold rounded-full uppercase">Commercial</span>
                </div>
                <div class="p-6 space-y-3">
                    <h3 class="font-serif text-xl font-bold text-white group-hover:text-arch-gold transition-colors">Cubic Dynamic Tower (큐브 다이나믹 타워)</h3>
                    <p class="text-arch-400 font-light text-xs leading-relaxed line-clamp-2">각 층의 박스가 유기적으로 회전하는 듯한 외관의 스마트 오피스 복합 타워입니다.</p>
                    <div class="flex justify-between items-center text-[11px] text-arch-gold font-semibold pt-4 border-t border-arch-900 uppercase tracking-widest">
                        <span>BUSAN, KOREA</span>
                        <span>View Details <i class="fa-solid fa-arrow-right ml-1"></i></span>
                    </div>
                </div>
            </div>

            <!-- Project Card 3: Public -->
            <div class="project-card group bg-arch-950 border border-arch-800/80 rounded-md overflow-hidden relative transition-all duration-500 hover:-translate-y-2 hover:border-arch-gold/50 cursor-pointer" data-category="public" onclick="openProjectModal('public-library')">
                <div class="relative overflow-hidden h-72">
                    <img src="https://images.unsplash.com/photo-1507842217343-583bb7270b66?q=80&w=2070" alt="Forest Library" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110">
                    <div class="absolute inset-0 bg-gradient-to-t from-arch-950/90 via-transparent to-transparent opacity-80"></div>
                    <span class="absolute top-4 left-4 text-[10px] tracking-widest font-bold px-3 py-1 border border-arch-gold bg-arch-950 text-arch-gold rounded-full uppercase">Public</span>
                </div>
                <div class="p-6 space-y-3">
                    <h3 class="font-serif text-xl font-bold text-white group-hover:text-arch-gold transition-colors">The Forest Pavilion Library (숲의 파빌리온 도서관)</h3>
                    <p class="text-arch-400 font-light text-xs leading-relaxed line-clamp-2">투명 유리 필로티 구조를 채택해 주변 원시 산림 경관과 유기적 동조를 이루는 공공 도서관입니다.</p>
                    <div class="flex justify-between items-center text-[11px] text-arch-gold font-semibold pt-4 border-t border-arch-900 uppercase tracking-widest">
                        <span>GANGWON, KOREA</span>
                        <span>View Details <i class="fa-solid fa-arrow-right ml-1"></i></span>
                    </div>
                </div>
            </div>

            <!-- Project Card 4: Concept -->
            <div class="project-card group bg-arch-950 border border-arch-800/80 rounded-md overflow-hidden relative transition-all duration-500 hover:-translate-y-2 hover:border-arch-gold/50 cursor-pointer" data-category="concept" onclick="openProjectModal('cloud-concept')">
                <div class="relative overflow-hidden h-72">
                    <img src="https://images.unsplash.com/photo-1506973035872-a4ec16b8e8d9?q=80&w=2070" alt="Floating Cloud" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110">
                    <div class="absolute inset-0 bg-gradient-to-t from-arch-950/90 via-transparent to-transparent opacity-80"></div>
                    <span class="absolute top-4 left-4 text-[10px] tracking-widest font-bold px-3 py-1 border border-arch-gold bg-arch-950 text-arch-gold rounded-full uppercase">Concept</span>
                </div>
                <div class="p-6 space-y-3">
                    <h3 class="font-serif text-xl font-bold text-white group-hover:text-arch-gold transition-colors">Floating Eco-Cloud (플로팅 아일랜드 2050)</h3>
                    <p class="text-arch-400 font-light text-xs leading-relaxed line-clamp-2">기후 이상 변화에 대응하기 위해 구상된 자가 발전식 해상 하이브리드 거주용 건축 컨셉입니다.</p>
                    <div class="flex justify-between items-center text-[11px] text-arch-gold font-semibold pt-4 border-t border-arch-900 uppercase tracking-widest">
                        <span>SEA PREVIEW CONCEPT</span>
                        <span>View Details <i class="fa-solid fa-arrow-right ml-1"></i></span>
                    </div>
                </div>
            </div>

            <!-- Project Card 5: Residential -->
            <div class="project-card group bg-arch-950 border border-arch-800/80 rounded-md overflow-hidden relative transition-all duration-500 hover:-translate-y-2 hover:border-arch-gold/50 cursor-pointer" data-category="residential" onclick="openProjectModal('cliff-villa')">
                <div class="relative overflow-hidden h-72">
                    <img src="https://images.unsplash.com/photo-1613490493576-7fde63acd811?q=80&w=2071" alt="Cliff Edge Villa" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110">
                    <div class="absolute inset-0 bg-gradient-to-t from-arch-950/90 via-transparent to-transparent opacity-80"></div>
                    <span class="absolute top-4 left-4 text-[10px] tracking-widest font-bold px-3 py-1 border border-arch-gold bg-arch-950 text-arch-gold rounded-full uppercase">Residential</span>
                </div>
                <div class="p-6 space-y-3">
                    <h3 class="font-serif text-xl font-bold text-white group-hover:text-arch-gold transition-colors">Cliffside Horizon Villa (해안 절벽 뷰 주택)</h3>
                    <p class="text-arch-400 font-light text-xs leading-relaxed line-clamp-2">수평선과 일치하도록 정밀 설계된 인피니티 풀을 갖춘 럭셔리 휴양형 모던 주거 공간입니다.</p>
                    <div class="flex justify-between items-center text-[11px] text-arch-gold font-semibold pt-4 border-t border-arch-900 uppercase tracking-widest">
                        <span>JEJU, KOREA</span>
                        <span>View Details <i class="fa-solid fa-arrow-right ml-1"></i></span>
                    </div>
                </div>
            </div>

            <!-- Project Card 6: Commercial -->
            <div class="project-card group bg-arch-950 border border-arch-800/80 rounded-md overflow-hidden relative transition-all duration-500 hover:-translate-y-2 hover:border-arch-gold/50 cursor-pointer" data-category="commercial" onclick="openProjectModal('atrium-mall')">
                <div class="relative overflow-hidden h-72">
                    <img src="https://images.unsplash.com/photo-1519567241046-7f570eee3ce6?q=80&w=2070" alt="Atrium Mall" class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110">
                    <div class="absolute inset-0 bg-gradient-to-t from-arch-950/90 via-transparent to-transparent opacity-80"></div>
                    <span class="absolute top-4 left-4 text-[10px] tracking-widest font-bold px-3 py-1 border border-arch-gold bg-arch-950 text-arch-gold rounded-full uppercase">Commercial</span>
                </div>
                <div class="p-6 space-y-3">
                    <h3 class="font-serif text-xl font-bold text-white group-hover:text-arch-gold transition-colors">Hyper-Atrium Complex (하이퍼 아뜨리움 몰)</h3>
                    <p class="text-arch-400 font-light text-xs leading-relaxed line-clamp-2">중정 천장을 뒤덮은 대형 유리 캐노피를 통해 기상 조건에 구애받지 않고 자연 채광을 선사합니다.</p>
                    <div class="flex justify-between items-center text-[11px] text-arch-gold font-semibold pt-4 border-t border-arch-900 uppercase tracking-widest">
                        <span>INCHEON, KOREA</span>
                        <span>View Details <i class="fa-solid fa-arrow-right ml-1"></i></span>
                    </div>
                </div>
            </div>

        </div>
    </div>
</section>

<!-- Project Detail Modal -->
<div id="project-modal" class="fixed inset-0 bg-arch-950/95 z-50 flex items-center justify-center p-4 md:p-8 hidden opacity-0 transition-opacity duration-300 overflow-y-auto">
    <div class="bg-arch-900 border border-arch-800 rounded-lg max-w-4xl w-full max-h-[90vh] overflow-y-auto relative p-6 md:p-10 text-arch-100" id="modal-content">
        <!-- Close Button -->
        <button onclick="closeProjectModal()" class="absolute top-4 right-4 text-arch-400 hover:text-arch-gold text-2xl" aria-label="상세 닫기">
            <i class="fa-solid fa-xmark"></i>
        </button>

        <div class="grid grid-cols-1 md:grid-cols-2 gap-8 pt-4">
            <!-- Modal Slider Image -->
            <div>
                <img id="modal-img" src="" alt="Project Image" class="w-full h-80 md:h-[450px] object-cover rounded-md border border-arch-800">
                
                <!-- Quick Architectural Specs -->
                <div class="mt-6 grid grid-cols-2 gap-4 text-xs font-mono uppercase bg-arch-950/80 border border-arch-800 p-4 rounded-md">
                    <div>
                        <span class="block text-arch-400">LOCATION</span>
                        <span id="modal-spec-location" class="text-white font-semibold"></span>
                    </div>
                    <div>
                        <span class="block text-arch-400">TOTAL AREA</span>
                        <span id="modal-spec-area" class="text-white font-semibold"></span>
                    </div>
                    <div>
                        <span class="block text-arch-400">COMPLETION YEAR</span>
                        <span id="modal-spec-year" class="text-white font-semibold"></span>
                    </div>
                    <div>
                        <span class="block text-arch-400">PROJECT TYPE</span>
                        <span id="modal-spec-type" class="text-white font-semibold text-arch-gold"></span>
                    </div>
                </div>
            </div>

            <!-- Modal Written Specs -->
            <div class="flex flex-col justify-between space-y-6">
                <div class="space-y-4">
                    <span id="modal-category" class="text-xs text-arch-gold tracking-[0.3em] font-bold uppercase"></span>
                    <h3 id="modal-title" class="font-serif text-2xl md:text-4xl font-bold text-white leading-tight"></h3>
                    <div class="w-12 h-[2px] bg-arch-gold"></div>
                    <p id="modal-desc" class="text-arch-400 font-light text-sm leading-relaxed"></p>
                </div>

                <div class="space-y-4 pt-6 border-t border-arch-800">
                    <h4 class="font-serif text-lg font-bold text-white">설계적 핵심 주안점 (Architectural Strategy)</h4>
                    <p id="modal-strategy" class="text-arch-400 font-light text-xs leading-relaxed"></p>
                </div>
                
                <div class="pt-4">
                    <button onclick="closeProjectModal()" class="w-full md:w-auto px-6 py-3 border border-arch-gold text-arch-gold hover:bg-arch-gold hover:text-arch-950 transition-all font-semibold text-xs tracking-widest rounded-sm">
                        CLOSE DETAILED VIEW
                    </button>
                </div>
            </div>
        </div>
    </div>
</div>

<!-- Timeline of Achievements -->
<section class="py-24 bg-arch-950 border-t border-arch-900 relative">
    <div class="max-w-7xl mx-auto px-6">
        <div class="text-center max-w-3xl mx-auto mb-16 space-y-4">
            <span class="text-arch-gold text-xs font-bold tracking-[0.3em]">CHRONICLE</span>
            <h2 class="font-serif text-3xl md:text-5xl font-bold text-white">커리어 히스토리 & 수상</h2>
            <p class="text-arch-400 font-light text-sm md:text-base">어떤 발자취로 공간 혁신을 일구어 왔는지 소개합니다.</p>
        </div>

        <div class="max-w-4xl mx-auto relative border-l border-arch-800 pl-6 md:pl-12 space-y-12">
            <!-- Timeline Item 1 -->
            <div class="relative">
                <!-- Timeline Dot Indicator -->
                <div class="absolute -left-[31px] md:-left-[55px] top-1.5 w-4 h-4 rounded-full bg-arch-gold border-4 border-arch-950"></div>
                <div class="flex flex-col md:flex-row md:items-center justify-between mb-2">
                    <span class="text-xs font-mono font-bold text-arch-gold tracking-widest">2024 - 현재</span>
                    <h3 class="font-serif text-lg md:text-xl font-bold text-white md:order-first">KIM WOO JIN ARCHITECTS 설립 및 파트너십 대표</h3>
                </div>
                <p class="text-arch-400 text-xs md:text-sm font-light leading-relaxed">
                    자체 건축설계 디자인 사무소를 출범하여, 환경과의 공생을 기저에 둔 현대적 단독주택 및 중소형 사옥 건축을 주도하고 있습니다. 한국 젊은 건축가 포럼 정회원으로 위촉되었습니다.
                </p>
            </div>

            <!-- Timeline Item 2 -->
            <div class="relative">
                <!-- Timeline Dot Indicator -->
                <div class="absolute -left-[31px] md:-left-[55px] top-1.5 w-4 h-4 rounded-full bg-arch-700 border-4 border-arch-950"></div>
                <div class="flex flex-col md:flex-row md:items-center justify-between mb-2">
                    <span class="text-xs font-mono font-bold text-arch-gold tracking-widest">2021 - 2023</span>
                    <h3 class="font-serif text-lg md:text-xl font-bold text-white md:order-first">대한민국 우수 젊은건축가상 대상 (Grand Prize)</h3>
                </div>
                <p class="text-arch-400 text-xs md:text-sm font-light leading-relaxed">
                    강원도 홍천의 친환경 도서관 'Forest Pavilion' 설계를 통해 국토교통부 주관 '올해의 젊은 건축가 상' 대상을 거머쥐며 설계 역량과 지속 가능성 디자인 가치를 증명받았습니다.
                </p>
            </div>

            <!-- Timeline Item 3 -->
            <div class="relative">
                <!-- Timeline Dot Indicator -->
                <div class="absolute -left-[31px] md:-left-[55px] top-1.5 w-4 h-4 rounded-full bg-arch-700 border-4 border-arch-950"></div>
                <div class="flex flex-col md:flex-row md:items-center justify-between mb-2">
                    <span class="text-xs font-mono font-bold text-arch-gold tracking-widest">2016 - 2020</span>
                    <h3 class="font-serif text-lg md:text-xl font-bold text-white md:order-first">Kengo Kuma & Associates (Tokyo) 시니어 디자이너</h3>
                </div>
                <p class="text-arch-400 text-xs md:text-sm font-light leading-relaxed">
                    도쿄의 본사에서 근무하며 동양적인 미니멀리즘과 자연 목조 주거 디자인을 전문으로 연구하고 아시아 전역의 하이엔드 복합 리조트 프로젝트를 리드 설계자로 기획했습니다.
                </p>
            </div>

            <!-- Timeline Item 4 -->
            <div class="relative">
                <!-- Timeline Dot Indicator -->
                <div class="absolute -left-[31px] md:-left-[55px] top-1.5 w-4 h-4 rounded-full bg-arch-700 border-4 border-arch-950"></div>
                <div class="flex flex-col md:flex-row md:items-center justify-between mb-2">
                    <span class="text-xs font-mono font-bold text-arch-gold tracking-widest">2015</span>
                    <h3 class="font-serif text-lg md:text-xl font-bold text-white md:order-first">한국예술종합학교 미술원 건축학과 최우수 졸업</h3>
                </div>
                <p class="text-arch-400 text-xs md:text-sm font-light leading-relaxed">
                    한예종 졸업전에서 '공중 정원 도시 2030'을 제안하며 학부 최우수작품상 수상 및 한국건축가협회 학생 본상을 거머쥐었습니다.
                </p>
            </div>
        </div>
    </div>
</section>

<!-- Contact Section -->
<section id="contact" class="py-24 bg-arch-900 border-t border-arch-800">
    <div class="max-w-7xl mx-auto px-6">
        <div class="grid grid-cols-1 lg:grid-cols-12 gap-16">
            
            <!-- Left Contact Info Details -->
            <div class="lg:col-span-5 flex flex-col justify-between space-y-12">
                <div class="space-y-6">
                    <span class="text-arch-gold text-xs font-bold tracking-[0.3em]">TALK TO US</span>
                    <h2 class="font-serif text-3xl md:text-5xl font-bold text-white leading-tight">지속 가능한 <br>미래의 공간을 의뢰하세요</h2>
                    <p class="text-arch-400 text-sm font-light leading-relaxed">
                        신축, 리모델링, 친환경 타운 하우스 단지 설계 및 마스터플랜 컨설팅 제휴에 관한 다양한 아이디어를 적극 환영합니다. 공간에 깊이를 더하는 최상의 파트너가 되어 드립니다.
                    </p>
                </div>

                <!-- Info detail rows -->
                <div class="space-y-6 text-sm">
                    <div class="flex items-center space-x-4">
                        <div class="w-10 h-10 rounded-full border border-arch-800 flex items-center justify-center text-arch-gold">
                            <i class="fa-solid fa-location-dot"></i>
                        </div>
                        <div>
                            <span class="block text-xs text-arch-400">OFFICE LOCATION</span>
                            <span class="text-white font-medium">서울특별시 강남구 테헤란로 123 ARCHI-STUDIO, 5F</span>
                        </div>
                    </div>

                    <div class="flex items-center space-x-4">
                        <div class="w-10 h-10 rounded-full border border-arch-800 flex items-center justify-center text-arch-gold">
                            <i class="fa-solid fa-envelope"></i>
                        </div>
                        <div>
                            <span class="block text-xs text-arch-400">EMAIL ADDRESS</span>
                            <span class="text-white font-medium">contact@wjarchitects.com</span>
                        </div>
                    </div>

                    <div class="flex items-center space-x-4">
                        <div class="w-10 h-10 rounded-full border border-arch-800 flex items-center justify-center text-arch-gold">
                            <i class="fa-solid fa-phone"></i>
                        </div>
                        <div>
                            <span class="block text-xs text-arch-400">PHONE INQUIRY</span>
                            <span class="text-white font-medium">+82 (0)2-1234-5678</span>
                        </div>
                    </div>
                </div>

                <!-- Social Links -->
                <div class="flex space-x-4">
                    <a href="#" class="w-10 h-10 rounded-sm bg-arch-950 border border-arch-800 flex items-center justify-center text-arch-400 hover:text-arch-gold hover:border-arch-gold transition-all duration-300">
                        <i class="fa-brands fa-instagram"></i>
                    </a>
                    <a href="#" class="w-10 h-10 rounded-sm bg-arch-950 border border-arch-800 flex items-center justify-center text-arch-400 hover:text-arch-gold hover:border-arch-gold transition-all duration-300">
                        <i class="fa-brands fa-linkedin-in"></i>
                    </a>
                    <a href="#" class="w-10 h-10 rounded-sm bg-arch-950 border border-arch-800 flex items-center justify-center text-arch-400 hover:text-arch-gold hover:border-arch-gold transition-all duration-300">
                        <i class="fa-brands fa-pinterest"></i>
                    </a>
                    <a href="#" class="w-10 h-10 rounded-sm bg-arch-950 border border-arch-800 flex items-center justify-center text-arch-400 hover:text-arch-gold hover:border-arch-gold transition-all duration-300">
                        <i class="fa-brands fa-youtube"></i>
                    </a>
                </div>
            </div>

            <!-- Right Contact Form -->
            <div class="lg:col-span-7 bg-arch-950 border border-arch-800 p-8 rounded-lg relative overflow-hidden">
                <form id="contact-form" onsubmit="handleContactSubmit(event)" class="space-y-6 relative z-10">
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                        <div class="space-y-2">
                            <label class="text-xs text-arch-400 font-bold uppercase tracking-wider">이름 / 기업명 *</label>
                            <input type="text" required class="w-full bg-arch-900 border border-arch-800 rounded-sm px-4 py-3 text-white focus:outline-none focus:border-arch-gold transition-colors text-sm">
                        </div>
                        <div class="space-y-2">
                            <label class="text-xs text-arch-400 font-bold uppercase tracking-wider">이메일 *</label>
                            <input type="email" required class="w-full bg-arch-900 border border-arch-800 rounded-sm px-4 py-3 text-white focus:outline-none focus:border-arch-gold transition-colors text-sm">
                        </div>
                    </div>

                    <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                        <div class="space-y-2">
                            <label class="text-xs text-arch-400 font-bold uppercase tracking-wider">연락처 *</label>
                            <input type="tel" required placeholder="010-0000-0000" class="w-full bg-arch-900 border border-arch-800 rounded-sm px-4 py-3 text-white focus:outline-none focus:border-arch-gold transition-colors text-sm">
                        </div>
                        <div class="space-y-2">
                            <label class="text-xs text-arch-400 font-bold uppercase tracking-wider">희망 프로젝트 성격</label>
                            <select class="w-full bg-arch-900 border border-arch-800 rounded-sm px-4 py-3 text-white focus:outline-none focus:border-arch-gold transition-colors text-sm">
                                <option class="bg-arch-950">Residential (단독주택/공동주택)</option>
                                <option class="bg-arch-950">Commercial (사옥/식음/빌딩)</option>
                                <option class="bg-arch-950">Public (공공시설/도서관 등)</option>
                                <option class="bg-arch-950">Consulting & Plan (설계 타당성 자문)</option>
                            </select>
                        </div>
                    </div>

                    <div class="space-y-2">
                        <label class="text-xs text-arch-400 font-bold uppercase tracking-wider">프로젝트 설명 및 상세 세부사항 *</label>
                        <textarea required rows="5" placeholder="대지 형태, 대략적인 건축 평수, 원하시는 마감 무드를 작성해 주시면 더욱 정교한 상담이 가능합니다." class="w-full bg-arch-900 border border-arch-800 rounded-sm px-4 py-3 text-white focus:outline-none focus:border-arch-gold transition-colors text-sm"></textarea>
                    </div>

                    <button type="submit" class="w-full py-4 bg-arch-gold hover:bg-arch-goldHover text-arch-950 font-bold text-sm tracking-widest rounded-sm transition-all duration-300 uppercase">
                        설계 프로젝트 의뢰 접수하기
                    </button>
                </form>

                <!-- Custom Success Toast Notification (Hidden by default) -->
                <div id="form-success-alert" class="absolute inset-0 bg-arch-950 z-20 flex flex-col items-center justify-center text-center p-8 hidden flex-col space-y-4">
                    <div class="w-16 h-16 rounded-full border-2 border-arch-gold flex items-center justify-center text-arch-gold text-3xl animate-bounce">
                        <i class="fa-solid fa-check"></i>
                    </div>
                    <h3 class="font-serif text-2xl font-bold text-white">상담 신청이 완벽하게 전송되었습니다</h3>
                    <p class="text-arch-400 text-sm max-w-sm">
                        접수해 주신 설계 개요서(의뢰서)를 바탕으로 심층 타당성을 검토한 후, 48시간 이내에 전담 건축 디자이너가 직접 연락을 드리겠습니다.
                    </p>
                    <button onclick="resetContactForm()" class="px-6 py-2 border border-arch-gold text-arch-gold hover:bg-arch-gold hover:text-arch-950 transition-all text-xs font-bold tracking-widest">
                        다시 작성하기
                    </button>
                </div>
            </div>

        </div>
    </div>
</section>

<!-- Footer -->
<footer class="bg-arch-950 border-t border-arch-900 py-12 text-arch-400 text-xs">
    <div class="max-w-7xl mx-auto px-6 flex flex-col md:flex-row justify-between items-center gap-6">
        <div class="flex items-center space-x-3">
            <span class="font-serif text-base font-bold text-white">KIM WOO JIN ARCHITECTS</span>
            <span class="text-[10px] text-arch-gold">| 사업자등록번호 120-00-00000 | 대표 김우진</span>
        </div>
        <div class="flex space-x-6 text-arch-400">
            <a href="#" class="hover:text-arch-gold transition-colors">이용약관</a>
            <a href="#" class="hover:text-arch-gold transition-colors">개인정보처리방침</a>
            <a href="#" class="hover:text-arch-gold transition-colors">찾아오시는 길</a>
        </div>
        <div>
            <p>&copy; 2026 KIM WOO JIN ARCHITECTS. All rights reserved.</p>
        </div>
    </div>
</footer>

<!-- Javascript Logic -->
<script>
    // ----------------------------------------------------
    // PROJECT DATA ARCHIVE (Mock database)
    // ----------------------------------------------------
    const projectsData = {
        'void-house': {
            category: 'Residential',
            title: 'House of Void (보이드 하우스)',
            img: 'https://images.unsplash.com/photo-1600596542815-ffad4c1539a9?q=80&w=2075',
            location: 'Seoul, Korea',
            area: '342 ㎡ (약 103평)',
            year: '2024',
            type: 'Residential (주거)',
            desc: '자연과의 긴밀한 소통과 내향적 프라이버시를 동시에 보호할 수 있도록 사각형 중정(Void Courtyard)을 중심으로 둘러싸는 형태로 설계된 하이엔드 단독 주택입니다.',
            strategy: '바닥부터 거실 천장까지를 전면 관통하는 대지 중심부 중정을 두어, 계절의 변화와 비, 눈 등의 기후 현상을 방 내부에서 오롯이 시각적으로 향유할 수 있도록 유도했습니다. 친환경 천연 단열재 공법을 적용했습니다.'
        },
        'cube-tower': {
            category: 'Commercial',
            title: 'Cubic Dynamic Tower',
            img: 'https://images.unsplash.com/photo-1486406146926-c627a92ad1ab?q=80&w=2070',
            location: 'Busan, Korea',
            area: '12,450 ㎡ (지상 18층)',
            year: '2023',
            type: 'Commercial (상업)',
            desc: '박스형태의 개별 모듈이 불규칙적으로 엇갈려 쌓여 있는 역동적인 조형미를 살린 부산 마린시티 부근의 차세대 크리에이티브 지식산업 오피스 센터입니다.',
            strategy: '어긋나게 돌출된 외관 모듈의 장점을 살려 테라스식 옥상 미니 가든을 전 층에 계단형태로 구현하였으며, 복사열 차단 전면 더블 스킨 커튼월 시스템을 채택해 냉난방 소비 전력을 전년 대비 34% 절감했습니다.'
        },
        'public-library': {
            category: 'Public',
            title: 'The Forest Pavilion Library',
            img: 'https://images.unsplash.com/photo-1507842217343-583bb7270b66?q=80&w=2070',
            location: 'Gangwon, Korea',
            area: '2,100 ㎡',
            year: '2022',
            type: 'Public (공공)',
            desc: '강원도 청정 소나무 숲 군락지에 자연스럽게 내려앉은 듯한 미적 연출을 선보이는 유리 필로티 구조물로 자연 지형 훼손율 5% 미만을 달성한 도서관입니다.',
            strategy: '주요 뼈대를 구조용 집성재 친환경 목재 시스템으로 기획하여 숲속 나무들과 기둥 형태가 연속되게 보조를 맞추었으며, 외부 풍경이 실내 도서 배치선과 평행을 기하도록 세심히 기하학을 정렬시켰습니다.'
        },
        'cloud-concept': {
            category: 'Concept',
            title: 'Floating Eco-Cloud 2050',
            img: 'https://images.unsplash.com/photo-1506973035872-a4ec16b8e8d9?q=80&w=2070',
            location: 'Pacific Ocean',
            area: '65,000 ㎡',
            year: '2050 (Concept)',
            type: 'Hybrid Sea Infrastructure',
            desc: '인공 지능 기후 분석 및 조력 에너지, 수상 태양광 패널을 자체 구비하여 에너지를 100% 자가 수급하는 바다 위의 친환경 소형 하이브리드 인공 섬형 미래 거주 공간 계획안입니다.',
            strategy: '파랑 하중 충격을 효과적으로 회피 분산할 수 있는 3축 육각형 부유체 구조로 안전성을 보증하며, 풍력 유입 터빈과 해양 담수화 공장이 결합된 에스닉하고 친환경적인 첨단 미래지향적 컨셉 프로젝트입니다.'
        },
        'cliff-villa': {
            category: 'Residential',
            title: 'Cliffside Horizon Villa',
            img: 'https://images.unsplash.com/photo-1613490493576-7fde63acd811?q=80&w=2071',
            location: 'Jeju, Korea',
            area: '510 ㎡',
            year: '2023',
            type: 'Residential (휴양/주거)',
            desc: '제주 애월의 현무암 절벽에 안착되어 끝없는 바다 지평선과 유려한 시각적 통합을 노리는 단독 노출콘크리트 하이엔드 풀빌라입니다.',
            strategy: '바다의 파도 소리를 음향 분석하여 실내 중정 설계 시 소리의 반사를 감안해 파도 백색 소음이 최상의 안정감을 주도록 벽 구조의 표면 패턴 조형을 다채롭게 마감해 설계의 소리 감수성을 제고했습니다.'
        },
        'atrium-mall': {
            category: 'Commercial',
            title: 'Hyper-Atrium Mall',
            img: 'https://images.unsplash.com/photo-1519567241046-7f570eee3ce6?q=80&w=2070',
            location: 'Incheon, Korea',
            area: '34,000 ㎡',
            year: '2021',
            type: 'Commercial (쇼핑/복합)',
            desc: '상부 돔에서 스며나오는 태양 일조 광량에 맞춰 실내 LED 라이팅 스펙트럼이 정밀 인공 지능 제어로 동조되는 첨단 미학의 가치를 지닌 복합 엔터테인먼트 쇼핑 시설입니다.',
            strategy: '기둥을 일절 사용하지 않는 무주(無柱) 공법으로 최장 스팬 메가 트러스 시스템을 천장부에 연출하여, 내방하는 쇼핑객들에게 무한한 스케일감과 해방감을 완벽하게 선사합니다.'
        }
    };

    // ----------------------------------------------------
    // PORTFOLIO FILTERING LOGIC
    // ----------------------------------------------------
    function filterPortfolio(category) {
        // Toggle Active Styling on buttons
        const buttons = document.querySelectorAll('.portfolio-filter-btn');
        buttons.forEach(btn => {
            btn.classList.remove('bg-arch-gold', 'text-arch-950');
            btn.classList.add('hover:text-arch-gold', 'text-white');
        });

        const activeBtn = document.getElementById(`filter-${category}`);
        if(activeBtn) {
            activeBtn.classList.remove('hover:text-arch-gold', 'text-white');
            activeBtn.classList.add('bg-arch-gold', 'text-arch-950');
        }

        // Show/Hide project items based on data-category
        const cards = document.querySelectorAll('.project-card');
        cards.forEach(card => {
            const cardCat = card.getAttribute('data-category');
            if (category === 'all' || cardCat === category) {
                card.style.display = 'block';
                // Trigger quick smooth fade-in
                card.style.opacity = '0';
                setTimeout(() => {
                    card.style.opacity = '1';
                }, 50);
            } else {
                card.style.display = 'none';
            }
        });
    }

    // ----------------------------------------------------
    // PROJECT MODAL DYNAMICS
    // ----------------------------------------------------
    function openProjectModal(projectId) {
        const modal = document.getElementById('project-modal');
        const pData = projectsData[projectId];
        if(!pData) return;

        // Populate details
        document.getElementById('modal-img').src = pData.img;
        document.getElementById('modal-category').innerText = pData.category;
        document.getElementById('modal-title').innerText = pData.title;
        document.getElementById('modal-desc').innerText = pData.desc;
        document.getElementById('modal-strategy').innerText = pData.strategy;
        
        // Populate specs
        document.getElementById('modal-spec-location').innerText = pData.location;
        document.getElementById('modal-spec-area').innerText = pData.area;
        document.getElementById('modal-spec-year').innerText = pData.year;
        document.getElementById('modal-spec-type').innerText = pData.type;

        // Show Modal with Fade Effect
        modal.classList.remove('hidden');
        document.body.style.overflow = 'hidden'; // Lock background scroll
        setTimeout(() => {
            modal.classList.remove('opacity-0');
            modal.classList.add('opacity-100');
        }, 10);
    }

    function closeProjectModal() {
        const modal = document.getElementById('project-modal');
        modal.classList.remove('opacity-100');
        modal.classList.add('opacity-0');
        document.body.style.overflow = ''; // Unlock background scroll
        setTimeout(() => {
            modal.classList.add('hidden');
        }, 300);
    }

    // Close modal on outer clicks
    window.addEventListener('click', (e) => {
        const modal = document.getElementById('project-modal');
        if (e.target === modal) {
            closeProjectModal();
        }
    });

    // ----------------------------------------------------
    // INTERACTIVE BLUEPRINT EXPLORER LOGIC
    // ----------------------------------------------------
    function toggleBlueprintLayer(layerId) {
        const layer = document.getElementById(layerId);
        const button = document.getElementById(`btn-${layerId}`);
        const dot = document.getElementById(`dot-${layerId}`);

        if (layer.classList.contains('opacity-100')) {
            // Hide layer
            layer.classList.remove('opacity-100');
            layer.classList.add('opacity-0');
            // Toggle switch design (off state)
            button.classList.remove('bg-arch-gold');
            button.classList.add('bg-arch-800');
            dot.style.right = 'auto';
            dot.style.left = '2px';
        } else {
            // Show layer
            layer.classList.remove('opacity-0');
            layer.classList.add('opacity-100');
            // Toggle switch design (on state)
            button.classList.remove('bg-arch-800');
            button.classList.add('bg-arch-gold');
            dot.style.left = 'auto';
            dot.style.right = '2px';
        }
    }

    // ----------------------------------------------------
    // CONTACT FORM INTERACTION
    // ----------------------------------------------------
    function handleContactSubmit(event) {
        event.preventDefault();
        
        // Simple mock validation & transition to success screen
        const successBox = document.getElementById('form-success-alert');
        successBox.classList.remove('hidden');
        successBox.classList.add('flex');
    }

    function resetContactForm() {
        const form = document.getElementById('contact-form');
        const successBox = document.getElementById('form-success-alert');
        
        form.reset();
        successBox.classList.remove('flex');
        successBox.classList.add('hidden');
    }

    // ----------------------------------------------------
    // MOBILE DRAWER MENU LOGIC
    // ----------------------------------------------------
    const mobileMenuBtn = document.getElementById('mobile-menu-btn');
    const closeDrawerBtn = document.getElementById('close-drawer-btn');
    const mobileDrawer = document.getElementById('mobile-drawer');
    const mobileLinks = document.querySelectorAll('.mobile-link');

    mobileMenuBtn.addEventListener('click', () => {
        mobileDrawer.classList.remove('translate-x-full');
    });

    closeDrawerBtn.addEventListener('click', () => {
        mobileDrawer.classList.add('translate-x-full');
    });

    // Close drawer when clicking any link inside it
    mobileLinks.forEach(link => {
        link.addEventListener('click', () => {
            mobileDrawer.classList.add('translate-x-full');
        });
    });

    // ----------------------------------------------------
    // SCROLL ANIMATIONS / NAVBAR SHRINK
    // ----------------------------------------------------
    window.addEventListener('scroll', () => {
        const navbar = document.getElementById('navbar');
        if (window.scrollY > 80) {
            navbar.classList.remove('h-20');
            navbar.classList.add('h-16', 'bg-arch-950/95', 'shadow-lg');
        } else {
            navbar.classList.remove('h-16', 'bg-arch-950/95', 'shadow-lg');
            navbar.classList.add('h-20');
        }
    });

    // Initialize layout setup on startup
    window.onload = function() {
        // Ensuring layers are fully functional and in default ON state
        console.log("Portfolio Blueprint system initialized.");
    };
</script>

</body>
</html>
