```html
<!DOCTYPE html>
<html lang="pt-BR" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>RAULS | Assista na Netflix</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        netflix: {
                            red: '#E50914',
                            redHover: '#B81D24',
                            dark: '#141414',
                            cardBg: '#181818',
                            gray: '#2F2F2F',
                            lightGray: '#8C8C8C',
                        }
                    },
                    fontFamily: {
                        sans: ['Helvetica Neue', 'Segoe UI', 'Roboto', 'Arial', 'sans-serif'],
                    }
                }
            }
        }
    </script>
    <!-- FontAwesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        body {
            background-color: #141414;
            color: #FFFFFF;
            font-family: 'Helvetica Neue', Helvetica, Arial, sans-serif;
            overflow-x: hidden;
        }

        /* Netflix Hero Vignette Gradient */
        .hero-vignette {
            background: linear-gradient(
                180deg, 
                rgba(20, 20, 20, 0.5) 0%, 
                rgba(20, 20, 20, 0.2) 40%, 
                rgba(20, 20, 20, 0.8) 80%, 
                #141414 100%
            ),
            linear-gradient(
                90deg,
                rgba(20, 20, 20, 0.9) 0%,
                rgba(20, 20, 20, 0.5) 50%,
                rgba(20, 20, 20, 0.9) 100%
            );
        }

        .netflix-red-glow {
            box-shadow: 0 0 25px rgba(229, 9, 20, 0.4);
        }

        .plan-card.selected {
            border-color: #E50914;
            background-color: rgba(229, 9, 20, 0.08);
            transform: translateY(-4px);
        }

        /* Subtle Poster Lighting Simulation */
        .poster-overlay {
            background: radial-gradient(circle at 30% 40%, rgba(229, 9, 20, 0.25) 0%, rgba(10, 25, 50, 0.6) 60%, rgba(20, 20, 20, 0.95) 100%);
        }

        /* Custom Modal Transition */
        .modal-fade {
            transition: opacity 0.3s ease, transform 0.3s ease;
        }
    </style>
</head>
<body class="min-h-screen flex flex-col justify-between antialiased selection:bg-netflix-red selection:text-white">

    <!-- 1. CABEÇALHO (HEADER) -->
    <header class="fixed top-0 left-0 w-full z-40 transition-all duration-500 bg-gradient-to-b from-black/90 via-black/50 to-transparent" id="navbar">
        <div class="max-w-7xl mx-auto px-4 sm:px-8 h-20 flex items-center justify-between">
            <!-- Logo Netflix -->
            <a href="#" class="flex items-center" aria-label="Netflix Home">
                <svg class="h-7 sm:h-9 fill-netflix-red" viewBox="0 0 111 30" xmlns="http://www.w3.org/2000/svg">
                    <path d="M105.062 14.28L111 30H101.938L98.882 21.365L95.733 30H86.848L92.83 14.28L87.11 0H96.082L98.882 8.016L101.766 0H110.651L105.062 14.28ZM74.419 30V0H83.218V30H74.419ZM58.74 30V0H72.846V7.121H67.539V11.531H72.23V18.528H67.539V30H58.74ZM40.916 30V0H49.715V22.879H56.559V30H40.916ZM26.255 18.528H31.03V30H22.231V0H36.337V7.121H31.03V11.531H35.721V18.528H26.255ZM10.222 30V11.531H4.915V30H0V0H13.687V7.121H8.38V11.531H15.137V30H10.222Z"/>
                </svg>
            </a>

            <!-- Botão Entrar -->
            <button id="btnOpenLogin" class="bg-netflix-red hover:bg-netflix-redHover text-white text-sm sm:text-base font-semibold px-4 py-1.5 sm:px-5 sm:py-2 rounded transition-colors duration-200 shadow-md">
                Entrar
            </button>
        </div>
    </header>

    <!-- 2. HERO SECTION (DESTAQUE PRINCIPAL) -->
    <section class="relative min-h-screen flex items-center justify-start pt-24 pb-16 overflow-hidden">
        <!-- Background Poster Image with Cinematic Lighting & Overlays -->
        <div class="absolute inset-0 -z-10 bg-black">
            <!-- Simulated Dramatically Lit Background Graphic -->
            <div class="absolute inset-0 bg-cover bg-center filter brightness-90 saturate-120 scale-105 transition-transform duration-10000 transform hover:scale-100" 
                 style="background-image: url('https://images.unsplash.com/photo-1550745165-9bc0b252726f?auto=format&fit=crop&w=1920&q=80');">
            </div>
            
            <!-- Dark Cyberpunk/Crime Neon Lighting Overlays -->
            <div class="absolute inset-0 poster-overlay"></div>
            
            <!-- Laptop & Bike Silhouette Elements (Artistic Vibe) -->
            <div class="absolute inset-0 opacity-40 mix-blend-screen bg-gradient-to-r from-red-900/30 via-slate-900/80 to-blue-900/40"></div>
            
            <!-- Vignette Gradients for Text Contrast -->
            <div class="absolute inset-0 hero-vignette"></div>
        </div>

        <div class="max-w-7xl mx-auto px-4 sm:px-8 w-full z-10 pt-12">
            <div class="max-w-2xl space-y-6">
                
                <!-- Netflix Original Badge -->
                <div class="flex items-center gap-2">
                    <span class="text-netflix-red font-black tracking-widest text-lg sm:text-xl flex items-center gap-1">
                        <svg class="w-5 h-5 fill-current" viewBox="0 0 24 24"><path d="M5.398 0v24h4.195V10.29l5.01 13.71h4.002V0h-4.196v13.63L9.4 0H5.398z"/></svg>
                        SÉRIE
                    </span>
                    <span class="text-xs uppercase tracking-widest text-slate-300 border border-slate-600 px-2 py-0.5 rounded bg-black/40">ORIGINAL NETFLIX</span>
                </div>

                <!-- Title (H1) -->
                <h1 class="text-6xl sm:text-8xl lg:text-9xl font-black tracking-tighter text-white drop-shadow-2xl font-sans uppercase" style="text-shadow: 0 5px 30px rgba(229, 9, 20, 0.5), 0 0 10px rgba(0,0,0,0.8);">
                    RAULS
                </h1>

                <!-- Tags / Metadata -->
                <div class="flex flex-wrap items-center gap-3 text-sm text-slate-300 font-medium">
                    <span class="text-emerald-400 font-bold">98% relevante</span>
                    <span class="border border-slate-500 px-1.5 py-0.5 text-xs rounded">18+</span>
                    <span>1 Temporada</span>
                    <span class="border border-slate-400/50 px-2 py-0.5 text-xs rounded-sm">4K Ultra HD</span>
                    <span class="text-slate-400">Drama Criminal • Suspense • Tech</span>
                </div>

                <!-- Subtitle / Hook Line -->
                <p class="text-lg sm:text-xl text-slate-200 font-normal leading-relaxed drop-shadow-md max-w-xl">
                    O crime se reinventou na velocidade da fibra óptica. Ostentação, códigos e consequências irreversíveis.
                </p>

                <!-- CTA (Chamada para Ação) -->
                <div class="pt-4 flex flex-wrap items-center gap-4">
                    <button id="btnWatchNow" class="bg-netflix-red hover:bg-netflix-redHover text-white px-8 py-3.5 rounded font-bold text-lg sm:text-xl flex items-center gap-3 transition-all transform hover:scale-105 netflix-red-glow shadow-xl">
                        <i class="fa-solid fa-play text-xl"></i>
                        <span>Assista agora</span>
                    </button>

                    <button id="btnMoreInfo" class="bg-slate-500/40 hover:bg-slate-500/60 text-white px-7 py-3.5 rounded font-bold text-lg flex items-center gap-3 backdrop-blur-sm transition-all">
                        <i class="fa-solid fa-circle-info text-xl"></i>
                        <span>Mais informações</span>
                    </button>
                </div>
            </div>
        </div>
    </section>

    <!-- 3. SEÇÃO DE SINOPSE (SOBRE A SÉRIE) -->
    <section id="synopsis" class="py-20 bg-gradient-to-b from-netflix-dark via-[#111111] to-netflix-dark relative border-t border-slate-800/60">
        <div class="max-w-5xl mx-auto px-4 sm:px-8">
            <div class="grid grid-cols-1 md:grid-cols-12 gap-8 items-center">
                
                <div class="md:col-span-8 space-y-6">
                    <div class="inline-block border-l-4 border-netflix-red pl-4">
                        <h2 class="text-2xl sm:text-4xl font-extrabold tracking-tight text-white">
                            O que está por trás da tela?
                        </h2>
                    </div>

                    <p class="text-lg sm:text-xl text-slate-300 leading-relaxed font-light">
                        Acompanhe a ascensão e queda de jovens que encontraram no ambiente digital um atalho perigoso para o sucesso. Entre ostentação e golpes, descubra até onde a busca por dinheiro fácil pode levar. <span class="text-white font-semibold">"RAULS"</span> mergulha fundo na cultura e nos riscos da vida online no Brasil.
                    </p>

                    <!-- Features/Bullet Badges -->
                    <div class="grid grid-cols-2 sm:grid-cols-3 gap-4 pt-4 border-t border-slate-800">
                        <div class="flex items-center gap-3 text-slate-300">
                            <i class="fa-solid fa-shield-halved text-netflix-red text-xl"></i>
                            <span class="text-sm font-medium">Cybercrime Brasil</span>
                        </div>
                        <div class="flex items-center gap-3 text-slate-300">
                            <i class="fa-solid fa-sack-dollar text-netflix-red text-xl"></i>
                            <span class="text-sm font-medium">Vida de Luxo</span>
                        </div>
                        <div class="flex items-center gap-3 text-slate-300">
                            <i class="fa-solid fa-user-ninja text-netflix-red text-xl"></i>
                            <span class="text-sm font-medium">Investigação</span>
                        </div>
                    </div>
                </div>

                <!-- Visual Card/Thumb Preview -->
                <div class="md:col-span-4 relative group rounded-xl overflow-hidden border border-slate-800 shadow-2xl bg-netflix-cardBg">
                    <img src="https://images.unsplash.com/photo-1526374965328-7f61d4dc18c5?auto=format&fit=crop&w=600&q=80" alt="RAULS Poster Detail" class="w-full h-80 object-cover group-hover:scale-105 transition-transform duration-500 filter brightness-90">
                    <div class="absolute inset-0 bg-gradient-to-t from-black via-transparent to-transparent"></div>
                    <div class="absolute bottom-4 left-4 right-4 text-center">
                        <span class="text-xs uppercase tracking-widest text-netflix-red font-bold">Lançamento Exclusivo</span>
                        <p class="text-sm font-bold text-white mt-1">Disponível em todos os seus aparelhos</p>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- 4. SEÇÃO DE PLANOS (TABELA / CARDS DE PREÇOS) -->
    <section id="plans" class="py-20 bg-netflix-dark relative">
        <div class="max-w-7xl mx-auto px-4 sm:px-8">
            
            <div class="text-center max-w-3xl mx-auto mb-16 space-y-3">
                <span class="text-netflix-red font-bold text-sm tracking-widest uppercase">Sem Fidelidade • Cancele quando quiser</span>
                <h2 class="text-3xl sm:text-5xl font-black text-white tracking-tight">
                    Escolha o seu plano e comece a assistir
                </h2>
                <p class="text-slate-400 text-base sm:text-lg">
                    Assista a <span class="text-white font-semibold">RAULS</span> e a milhares de outros títulos no seu celular, tablet, TV ou computador.
                </p>
            </div>

            <!-- Cards de Planos Responsivos -->
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8 items-stretch">
                
                <!-- Plano 1: Padrão com anúncios -->
                <div data-plan="padrao-anuncios" class="plan-card cursor-pointer bg-netflix-cardBg border-2 border-slate-800 rounded-2xl p-8 flex flex-col justify-between transition-all duration-300 hover:border-slate-600">
                    <div>
                        <div class="flex justify-between items-center mb-4">
                            <h3 class="text-xl font-bold text-white">Padrão com anúncios</h3>
                            <span class="text-xs bg-slate-800 text-slate-300 px-2.5 py-1 rounded-full font-medium">Econômico</span>
                        </div>
                        <div class="mb-6">
                            <span class="text-3xl font-black text-white">R$ 20,90</span>
                            <span class="text-slate-400 text-sm">/mês</span>
                        </div>

                        <ul class="space-y-4 text-sm text-slate-300 mb-8 border-t border-slate-800 pt-6">
                            <li class="flex items-center gap-3">
                                <i class="fa-solid fa-check text-emerald-500"></i>
                                <span>Qualidade <strong>Full HD (1080p)</strong></span>
                            </li>
                            <li class="flex items-center gap-3">
                                <i class="fa-solid fa-circle-info text-amber-400"></i>
                                <span>Com alguns intervalos comerciais</span>
                            </li>
                            <li class="flex items-center gap-3">
                                <i class="fa-solid fa-tv text-slate-400"></i>
                                <span>Assista em <strong>2 aparelhos</strong> simultâneos</span>
                            </li>
                            <li class="flex items-center gap-3">
                                <i class="fa-solid fa-mobile-button text-slate-400"></i>
                                <span>Disponível em TV, computador, celular e tablet</span>
                            </li>
                        </ul>
                    </div>

                    <button class="select-plan-btn w-full py-3 rounded-lg border border-slate-600 hover:border-white font-bold text-sm text-white transition-all">
                        Selecionar Plano
                    </button>
                </div>

                <!-- Plano 2: Padrão (Destaque Popular) -->
                <div data-plan="padrao" class="plan-card selected relative cursor-pointer bg-netflix-cardBg border-2 border-netflix-red rounded-2xl p-8 flex flex-col justify-between transition-all duration-300 shadow-2xl">
                    <div class="absolute -top-3.5 left-1/2 -translate-x-1/2 bg-netflix-red text-white text-xs font-bold uppercase tracking-wider px-4 py-1 rounded-full shadow-lg">
                        Mais Popular
                    </div>

                    <div>
                        <div class="flex justify-between items-center mb-4 mt-2">
                            <h3 class="text-2xl font-bold text-white">Padrão</h3>
                            <span class="text-xs bg-netflix-red/20 text-netflix-red px-2.5 py-1 rounded-full font-bold">Sem Anúncios</span>
                        </div>
                        <div class="mb-6">
                            <span class="text-4xl font-black text-white">R$ 44,90</span>
                            <span class="text-slate-400 text-sm">/mês</span>
                        </div>

                        <ul class="space-y-4 text-sm text-slate-200 mb-8 border-t border-slate-800 pt-6">
                            <li class="flex items-center gap-3">
                                <i class="fa-solid fa-check text-emerald-500 text-base"></i>
                                <span>Qualidade <strong>Full HD (1080p)</strong></span>
                            </li>
                            <li class="flex items-center gap-3">
                                <i class="fa-solid fa-check text-emerald-500 text-base"></i>
                                <span><strong>Sem anúncios</strong> ou interrupções</span>
                            </li>
                            <li class="flex items-center gap-3">
                                <i class="fa-solid fa-tv text-slate-300"></i>
                                <span>Assista em <strong>2 aparelhos</strong> simultâneos</span>
                            </li>
                            <li class="flex items-center gap-3">
                                <i class="fa-solid fa-download text-slate-300"></i>
                                <span>Download para assistir offline</span>
                            </li>
                        </ul>
                    </div>

                    <button class="select-plan-btn w-full py-3.5 rounded-lg bg-netflix-red hover:bg-netflix-redHover font-bold text-sm text-white transition-all shadow-md">
                        Plano Selecionado
                    </button>
                </div>

                <!-- Plano 3: Premium -->
                <div data-plan="premium" class="plan-card cursor-pointer bg-netflix-cardBg border-2 border-slate-800 rounded-2xl p-8 flex flex-col justify-between transition-all duration-300 hover:border-slate-600">
                    <div>
                        <div class="flex justify-between items-center mb-4">
                            <h3 class="text-xl font-bold text-white">Premium</h3>
                            <span class="text-xs bg-amber-500/20 text-amber-400 px-2.5 py-1 rounded-full font-bold">4K + HDR</span>
                        </div>
                        <div class="mb-6">
                            <span class="text-3xl font-black text-white">R$ 59,90</span>
                            <span class="text-slate-400 text-sm">/mês</span>
                        </div>

                        <ul class="space-y-4 text-sm text-slate-300 mb-8 border-t border-slate-800 pt-6">
                            <li class="flex items-center gap-3">
                                <i class="fa-solid fa-check text-emerald-500"></i>
                                <span>Qualidade <strong>4K Ultra HD + HDR</strong></span>
                            </li>
                            <li class="flex items-center gap-3">
                                <i class="fa-solid fa-check text-emerald-500"></i>
                                <span><strong>Sem anúncios</strong></span>
                            </li>
                            <li class="flex items-center gap-3">
                                <i class="fa-solid fa-volume-high text-amber-400"></i>
                                <span><strong>Áudio espacial</strong> (Imersivo)</span>
                            </li>
                            <li class="flex items-center gap-3">
                                <i class="fa-solid fa-tv text-slate-400"></i>
                                <span>Assista em <strong>4 aparelhos</strong> simultâneos</span>
                            </li>
                        </ul>
                    </div>

                    <button class="select-plan-btn w-full py-3 rounded-lg border border-slate-600 hover:border-white font-bold text-sm text-white transition-all">
                        Selecionar Plano
                    </button>
                </div>

            </div>
            
            <!-- Bottom CTA -->
            <div class="mt-12 text-center">
                <button id="btnSubscribeSelected" class="bg-netflix-red hover:bg-netflix-redHover text-white px-10 py-4 rounded-lg font-extrabold text-lg transition-all netflix-red-glow flex items-center justify-center gap-3 mx-auto">
                    <i class="fa-brands 
