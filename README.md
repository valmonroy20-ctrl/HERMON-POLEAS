<!DOCTYPE html>
<html lang="es" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hermon | Poleas de Aluminio - Ingeniería que no para.</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- FontAwesome & Lucide Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts: Montserrat -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,300;0,400;0,600;0,700;0,800;0,900;1,700&display=swap" rel="stylesheet">

    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        brand: {
                            orange: '#FF6A00',
                            dark: '#141414',
                            steel: '#333333',
                            mid: '#6D6D6D',
                            light: '#A7A7A7',
                            white: '#FFFFFF'
                        }
                    },
                    fontFamily: {
                        sans: ['Montserrat', 'sans-serif'],
                    }
                }
            }
        }
    </script>

    <style>
        body {
            font-family: 'Montserrat', sans-serif;
            background-color: #141414;
            color: #FFFFFF;
        }

        /* Estilos visuales del manual de marca */
        .brand-grid-pattern {
            background-image: radial-gradient(rgba(255, 106, 0, 0.12) 1px, transparent 1px);
            background-size: 24px 24px;
        }

        .stripes-accent {
            background: repeating-linear-gradient(
                -45deg,
                #FF6A00,
                #FF6A00 8px,
                transparent 8px,
                transparent 16px
            );
        }

        .industrial-border {
            border-left: 4px solid #FF6A00;
        }

        .clip-slant {
            clip-path: polygon(0 0, 100% 0, 100% 88%, 0 100%);
        }

        .clip-slant-reverse {
            clip-path: polygon(0 12%, 100% 0, 100% 100%, 0 100%);
        }

        .orange-glow {
            box-shadow: 0 0 25px rgba(255, 106, 0, 0.25);
        }

        /* Reemplazo seguro de alerta */
        #notification-toast {
            transition: transform 0.3s ease-in-out, opacity 0.3s ease-in-out;
        }
    </style>
</head>
<body class="antialiased selection:bg-brand-orange selection:text-black">

    <!-- NOTIFICACIÓN / TOAST CUSTOM -->
    <div id="notification-toast" class="fixed bottom-5 right-5 z-50 transform translate-y-20 opacity-0 pointer-events-none bg-brand-steel border-l-4 border-brand-orange text-white p-4 rounded shadow-2xl flex items-center gap-3 max-w-md">
        <i class="fa-solid fa-circle-check text-brand-orange text-xl"></i>
        <div>
            <p id="toast-title" class="font-bold text-sm">Mensaje Enviado</p>
            <p id="toast-desc" class="text-xs text-brand-light">Un asesor técnico se pondrá en contacto en breve.</p>
        </div>
    </div>

    <!-- NAVBAR SUPERIOR -->
    <header class="fixed top-0 left-0 w-full z-40 bg-brand-dark/95 backdrop-blur-md border-b border-brand-steel">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-20 flex items-center justify-between">
            
            <!-- LOGOTIPO HERMON -->
            <a href="#" class="flex items-center gap-3 group">
                <div class="w-10 h-10 bg-brand-orange flex items-center justify-center font-black text-black text-2xl tracking-tighter transform -skew-x-12 group-hover:bg-white transition-colors">
                    H
                </div>
                <div>
                    <span class="block font-black text-xl tracking-wider text-white leading-none">HERMON</span>
                    <span class="block text-[10px] tracking-[0.25em] text-brand-light font-bold mt-1">POLEAS DE ALUMINIO</span>
                </div>
            </a>

            <!-- NAVEGACIÓN DESKTOP -->
            <nav class="hidden md:flex items-center space-x-8 text-xs font-bold uppercase tracking-wider">
                <a href="#inicio" class="text-white hover:text-brand-orange transition-colors">Inicio</a>
                <a href="#nosotros" class="text-brand-light hover:text-brand-orange transition-colors">Quiénes Somos</a>
                <a href="#ventajas" class="text-brand-light hover:text-brand-orange transition-colors">Calidad y Matrices</a>
                <a href="#productos" class="text-brand-light hover:text-brand-orange transition-colors">Catálogo</a>
                <a href="#cotizar" class="text-brand-light hover:text-brand-orange transition-colors">Cotización</a>
            </nav>

            <!-- BOTÓN CONTACTO -->
            <div class="hidden md:flex items-center gap-4">
                <a href="#cotizar" class="px-5 py-2.5 bg-brand-orange text-black font-extrabold text-xs tracking-wider uppercase transform hover:-translate-y-0.5 transition-all shadow-md hover:bg-white">
                    Solicitar Cotización <i class="fa-solid fa-arrow-right ml-1"></i>
                </a>
            </div>

            <!-- BOTÓN MENÚ MÓVIL -->
            <button id="mobile-menu-btn" class="md:hidden text-white text-2xl focus:outline-none" aria-label="Abrir Menú">
                <i class="fa-solid fa-bars"></i>
            </button>
        </div>

        <!-- MENÚ MÓVIL DESPLEGABLE -->
        <div id="mobile-menu" class="hidden md:hidden bg-brand-dark border-b border-brand-steel px-6 py-6 space-y-4">
            <a href="#inicio" class="mobile-link block text-sm font-bold uppercase text-white hover:text-brand-orange">Inicio</a>
            <a href="#nosotros" class="mobile-link block text-sm font-bold uppercase text-brand-light hover:text-brand-orange">Quiénes Somos</a>
            <a href="#ventajas" class="mobile-link block text-sm font-bold uppercase text-brand-light hover:text-brand-orange">Calidad y Matrices</a>
            <a href="#productos" class="mobile-link block text-sm font-bold uppercase text-brand-light hover:text-brand-orange">Catálogo</a>
            <a href="#cotizar" class="mobile-link block text-sm font-bold uppercase text-brand-light hover:text-brand-orange">Cotización</a>
            <a href="#cotizar" class="mobile-link inline-block w-full text-center px-5 py-3 bg-brand-orange text-black font-extrabold text-xs uppercase tracking-wider">
                Solicitar Cotización
            </a>
        </div>
    </header>

    <!-- MAIN HERO SECTION -->
    <section id="inicio" class="relative pt-32 pb-20 md:pt-40 md:pb-32 bg-brand-dark overflow-hidden border-b border-brand-steel">
        <!-- Fondo Decorativo -->
        <div class="absolute inset-0 brand-grid-pattern opacity-40"></div>
        <div class="absolute -right-20 top-1/4 w-96 h-96 bg-brand-orange/10 rounded-full blur-3xl pointer-events-none"></div>

        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative z-10">
            <div class="grid md:grid-cols-12 gap-12 items-center">
                
                <!-- Columna Izquierda: Texto Hero -->
                <div class="md:col-span-7 space-y-6">
                    <div class="inline-flex items-center gap-2 px-3 py-1 bg-brand-steel/60 border border-brand-orange/40 rounded-sm">
                        <span class="w-2 h-2 bg-brand-orange rounded-full animate-pulse"></span>
                        <span class="text-xs font-bold uppercase tracking-widest text-brand-orange">Fabrica e Ingeniería B2B</span>
                    </div>

                    <h1 class="text-4xl sm:text-5xl lg:text-6xl font-black uppercase tracking-tight text-white leading-tight">
                        Calidad que impulsa <br>
                        <span class="text-transparent bg-clip-text bg-gradient-to-r from-brand-orange via-white to-brand-orange">
                            Tu Producción.
                        </span>
                    </h1>

                    <p class="text-brand-light text-base sm:text-lg max-w-xl font-normal leading-relaxed">
                        Fabricamos poleas de aluminio de alta aleación con tecnología de matrices de precisión. La solución confiable para industrias que no aceptan paros imprevistos.
                    </p>

                    <!-- Barras de Acento Diagonales (Elemento Gráfico Manual) -->
                    <div class="flex items-center gap-2 py-2">
                        <div class="w-12 h-2 stripes-accent"></div>
                        <span class="text-xs font-bold uppercase text-brand-light tracking-widest">INGENIERÍA QUE NO PARA.</span>
                    </div>

                    <div class="flex flex-wrap gap-4 pt-4">
                        <a href="#cotizar" class="px-8 py-4 bg-brand-orange text-black font-extrabold text-sm uppercase tracking-wider transform hover:scale-105 transition-all orange-glow flex items-center gap-3">
                            <span>Solicitar Cotización</span>
                            <i class="fa-solid fa-calculator"></i>
                        </a>
                        <a href="#nosotros" class="px-8 py-4 bg-brand-steel text-white font-extrabold text-sm uppercase tracking-wider hover:bg-brand-orange hover:text-black transition-all border border-brand-mid/30">
                            Conocer Nuestra Historia
                        </a>
                    </div>

                    <!-- Métricas / Indicadores -->
                    <div class="grid grid-cols-3 gap-6 pt-8 border-t border-brand-steel/80">
                        <div>
                            <span class="block text-2xl lg:text-3xl font-black text-brand-orange">100%</span>
                            <span class="text-[11px] uppercase font-bold text-brand-light">Cumplimiento en Entregas</span>
                        </div>
                        <div>
                            <span class="block text-2xl lg:text-3xl font-black text-white">Alta</span>
                            <span class="text-[11px] uppercase font-bold text-brand-light">Aleación de Aluminio</span>
                        </div>
                        <div>
                            <span class="block text-2xl lg:text-3xl font-black text-brand-orange">0%</span>
                            <span class="text-[11px] uppercase font-bold text-brand-light">Margen de Tolerancia</span>
                        </div>
                    </div>
                </div>

                <!-- Columna Derecha: Render o Arte de Producto -->
                <div class="md:col-span-5 relative">
                    <div class="relative mx-auto max-w-md lg:max-w-none">
                        <!-- Marco Fotográfico Industrial -->
                        <div class="relative bg-gradient-to-b from-brand-steel to-brand-dark p-3 rounded-lg border border-brand-orange/30 orange-glow">
                            <!-- SVG Renderizado de Polea de Aluminio Industrial -->
                            <div class="w-full h-80 sm:h-96 bg-black/80 rounded flex items-center justify-center p-6 relative overflow-hidden">
                                <div class="absolute inset-0 bg-brand-orange/5 radial-gradient"></div>
                                
                                <!-- Diagrama Gráfico Ilustrativo de Polea -->
                                <svg class="w-full h-full text-brand-orange animate-spin-slow" style="animation-duration: 40s;" viewBox="0 0 200 200" fill="none" xmlns="http://www.w3.org/2000/svg">
                                    <!-- Polea exterior -->
                                    <circle cx="100" cy="100" r="90" stroke="#333333" stroke-width="12"/>
                                    <circle cx="100" cy="100" r="82" stroke="#FF6A00" stroke-width="3" stroke-dasharray="8 4"/>
                                    <!-- Canales V -->
                                    <circle cx="100" cy="100" r="70" stroke="#A7A7A7" stroke-width="6"/>
                                    <!-- Brazos / Estructura -->
                                    <circle cx="100" cy="100" r="45" stroke="#FF6A00" stroke-width="8"/>
                                    <line x1="100" y1="10" x2="100" y2="190" stroke="#6D6D6D" stroke-width="6"/>
                                    <line x1="10" y1="100" x2="190" y2="100" stroke="#6D6D6D" stroke-width="6"/>
                                    <line x1="36" y1="36" x2="164" y2="164" stroke="#6D6D6D" stroke-width="4"/>
                                    <line x1="164" y1="36" x2="36" y2="164" stroke="#6D6D6D" stroke-width="4"/>
                                    <!-- Centro del eje -->
                                    <circle cx="100" cy="100" r="22" fill="#141414" stroke="#FF6A00" stroke-width="4"/>
                                    <rect x="94" y="82" width="12" height="10" fill="#FF6A00"/>
                                </svg>

                                <!-- Etiqueta Flotante sobre la Foto -->
                                <div class="absolute bottom-4 left-4 right-4 bg-brand-dark/90 backdrop-blur p-3 border-l-2 border-brand-orange flex justify-between items-center">
                                    <div>
                                        <p class="text-xs font-extrabold uppercase text-white">Polea Industrial de Aluminio</p>
                                        <p class="text-[10px] text-brand-light">Maquinado con Matrices de Alta Precisión</p>
                                    </div>
                                    <span class="text-xs font-black text-brand-orange bg-brand-steel px-2 py-1">CERTIFICADA</span>
                                </div>
                            </div>
                        </div>

                        <!-- Detalle decorativo gráfico de esquinas -->
                        <div class="absolute -top-3 -left-3 w-6 h-6 border-t-2 border-l-2 border-brand-orange"></div>
                        <div class="absolute -bottom-3 -right-3 w-6 h-6 border-b-2 border-r-2 border-brand-orange"></div>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- SECCIÓN: QUIÉNES SOMOS (HISTORIA GENERACIONAL & VALORES) -->
    <section id="nosotros" class="py-24 bg-brand-dark relative border-b border-brand-steel">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid lg:grid-cols-12 gap-12 items-center">
                
                <!-- Columna Visual e Histórica -->
                <div class="lg:col-span-5 space-y-6">
                    <div class="bg-brand-steel p-8 border border-brand-mid/20 relative">
                        <div class="w-12 h-1 bg-brand-orange mb-6"></div>
                        <h3 class="text-2xl font-black uppercase text-white tracking-wider mb-2">Tradición e Innovación</h3>
                        <p class="text-xs font-bold text-brand-orange tracking-widest uppercase mb-4">Herencia que Construye Futuro</p>
                        
                        <p class="text-brand-light text-sm leading-relaxed mb-6">
                            Desde nuestros primeros talleres hasta la planta de producción industrial moderna, la filosofía Hermon no ha cambiado: el compromiso absoluto con el trabajo bien hecho y el respeto hacia el cliente.
                        </p>

                        <div class="p-4 bg-brand-dark border-l-4 border-brand-orange">
                            <p class="text-xs italic text-brand-light">
                                "Aprendimos que una polea no es solo metal procesado; es la confianza de una fábrica entera que depende de que nuestro producto jamás se detenga."
                            </p>
                            <span class="block text-[11px] font-bold text-white uppercase mt-2">— Dirección General Hermon</span>
                        </div>
                    </div>
                </div>

                <!-- Columna Contenido Principal -->
                <div class="lg:col-span-7 space-y-6">
                    <div class="inline-block text-xs font-extrabold uppercase tracking-widest text-brand-orange border-b-2 border-brand-orange pb-1">
                        NUESTRA HISTORIA Y VALORES
                    </div>

                    <h2 class="text-3xl sm:text-4xl font-black uppercase text-white tracking-tight leading-tight">
                        Una Empresa Familiar <br>
                        <span class="text-brand-orange">De Generación en Generación</span>
                    </h2>

                    <div class="space-y-4 text-brand-light text-sm sm:text-base leading-relaxed">
                        <p>
                            En <strong class="text-white">HERMON</strong>, la pasión por la ingeniería de transmisión no se improvisa: se hereda. A lo largo de las décadas, hemos evolucionado de generación en generación, perfeccionando nuestros procesos de fundición y mecanizado para convertirnos en el referente indiscutible de poleas de aluminio.
                        </p>
                        <p>
                            Mantenemos intactos los valores fundacionales con los que nacimos: <strong class="text-white">cercanía real con el cliente, palabra de honor en cada trato y una lealtad inquebrantable</strong>. Entendemos las necesidades operativas de la industria porque llevamos el trabajo metalmecánico en las venas.
                        </p>
                    </div>

                    <!-- Pilares Clave Exigidos -->
                    <div class="grid sm:grid-cols-2 gap-4 pt-4">
                        <div class="p-4 bg-brand-steel/40 border border-brand-steel hover:border-brand-orange transition-colors">
                            <div class="flex items-center gap-3 mb-2">
                                <i class="fa-solid fa-handshake text-brand-orange text-lg"></i>
                                <h4 class="font-extrabold text-sm uppercase text-white">Lealtad & Conexión</h4>
                            </div>
                            <p class="text-xs text-brand-light">
                                Trato directo y sincero. Construimos relaciones B2B duraderas donde el cliente siempre cuenta con respaldo directo de fábrica.
                            </p>
                        </div>

                        <div class="p-4 bg-brand-steel/40 border border-brand-steel hover:border-brand-orange transition-colors">
                            <div class="flex items-center gap-3 mb-2">
                                <i class="fa-solid fa-clock text-brand-orange text-lg"></i>
                                <h4 class="font-extrabold text-sm uppercase text-white">Entregas a Tiempo</h4>
                            </div>
                            <p class="text-xs text-brand-light">
                                Cumplimos rigurosamente con las fechas comprometidas. Sabes exactamente cuándo llegará tu pedido a planta.
                            </p>
                        </div>
                    </div>

                </div>

            </div>
        </div>
    </section>

    <!-- SECCIÓN: CALIDAD Y FABRICACIÓN CON MATRICES (PUNTO CLAVE) -->
    <section id="ventajas" class="py-24 bg-brand-steel/20 relative border-b border-brand-steel">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            
            <div class="text-center max-w-3xl mx-auto mb-16">
                <span class="text-xs font-extrabold text-brand-orange uppercase tracking-widest block mb-2">Ingeniería de Tolerancia Cero</span>
                <h2 class="text-3xl sm:text-4xl font-black uppercase text-white tracking-tight">
                    Fabricación con Matrices y Aluminio Seleccionado
                </h2>
                <div class="w-16 h-1 bg-brand-orange mx-auto my-4"></div>
                <p class="text-brand-light text-sm sm:text-base">
                    No utilizamos aluminio genérico ni procesos improvisados. Cada polea nace de matrices de precisión diseñadas para garantizar la máxima durabilidad y balance estructural.
                </p>
            </div>

            <!-- Grid de Características de Calidad -->
            <div class="grid md:grid-cols-3 gap-8">
                
                <!-- Tarjeta 1: Matrices Propias -->
                <div class="bg-brand-dark p-8 border border-brand-steel relative group hover:border-brand-orange transition-all">
                    <div class="w-12 h-12 bg-brand-steel flex items-center justify-center text-brand-orange text-xl font-bold mb-6 group-hover:bg-brand-orange group-hover:text-black transition-colors">
                        <i class="fa-solid fa-cubes-stacked"></i>
                    </div>
                    <h3 class="text-xl font-black uppercase text-white mb-3">Fabricación con Matrices</h3>
                    <p class="text-brand-light text-xs sm:text-sm leading-relaxed mb-4">
                        Desarrollamos e iteramos nuestras propias matrices de moldeado industrial. Esto asegura homogeneidad en el metal, consistencia en la densidad del producto y dimensiones idénticas pieza tras pieza.
                    </p>
                    <ul class="text-xs text-brand-light space-y-2 border-t border-brand-steel pt-4">
                        <li class="flex items-center gap-2"><i class="fa-solid fa-check text-brand-orange"></i> Estructura interna sin porosidades</li>
                        <li class="flex items-center gap-2"><i class="fa-solid fa-check text-brand-orange"></i> Balance dinámico optimizado</li>
                    </ul>
                </div>

                <!-- Tarjeta 2: Aluminio de Primera Calidad -->
                <div class="bg-brand-dark p-8 border border-brand-steel relative group hover:border-brand-orange transition-all">
                    <div class="w-12 h-12 bg-brand-steel flex items-center justify-center text-brand-orange text-xl font-bold mb-6 group-hover:bg-brand-orange group-hover:text-black transition-colors">
                        <i class="fa-solid fa-shield-halved"></i>
                    </div>
                    <h3 class="text-xl font-black uppercase text-white mb-3">Aluminio de Alta Aleación</h3>
                    <p class="text-brand-light text-xs sm:text-sm leading-relaxed mb-4">
                        Seleccionamos aleaciones lingote de primer uso con resistencia superior a la fatiga, fricción y cambios térmicos. Ligereza estructural que reduce el desgaste sobre rodamientos y motores.
                    </p>
                    <ul class="text-xs text-brand-light space-y-2 border-t border-brand-steel pt-4">
                        <li class="flex items-center gap-2"><i class="fa-solid fa-check text-brand-orange"></i> Mayor disipación de calor</li>
                        <li class="flex items-center gap-2"><i class="fa-solid fa-check text-brand-orange"></i> Resistencia contra corrosión</li>
                    </ul>
                </div>

                <!-- Tarjeta 3: Puntualidad y Cumplimiento -->
                <div class="bg-brand-dark p-8 border border-brand-steel relative group hover:border-brand-orange transition-all">
                    <div class="w-12 h-12 bg-brand-steel flex items-center justify-center text-brand-orange text-xl font-bold mb-6 group-hover:bg-brand-orange group-hover:text-black transition-colors">
                        <i class="fa-solid fa-truck-fast"></i>
                    </div>
                    <h3 class="text-xl font-black uppercase text-white mb-3">Tiempos de Entrega Reales</h3>
                    <p class="text-brand-light text-xs sm:text-sm leading-relaxed mb-4">
                        Sabemos que un retraso detiene líneas operativas enteras. Nos comprometemos únicamente con plazos de entrega que CUMPLIMOS al 100%, con logística y seguimiento directo.
                    </p>
                    <ul class="text-xs text-brand-light space-y-2 border-t border-brand-steel pt-4">
                        <li class="flex items-center gap-2"><i class="fa-solid fa-check text-brand-orange"></i> Compromiso Paro Cero</li>
                        <li class="flex items-center gap-2"><i class="fa-solid fa-check text-brand-orange"></i> Despachos programados</li>
                    </ul>
                </div>

            </div>

            <!-- Banner Promesa Hermon -->
            <div class="mt-16 bg-gradient-to-r from-brand-steel via-brand-dark to-brand-steel p-8 border-l-4 border-brand-orange flex flex-col md:flex-row items-center justify-between gap-6">
                <div>
                    <h4 class="text-lg font-black uppercase text-white">¿Requieres poleas a la medida o fabricaciones especiales?</h4>
                    <p class="text-xs text-brand-light mt-1">Diseñamos y ajustamos canales, bocinas y diámetros según las especificaciones de tu maquinaria.</p>
                </div>
                <a href="#cotizar" class="px-6 py-3 bg-brand-orange text-black font-extrabold text-xs uppercase tracking-wider whitespace-nowrap hover:bg-white transition-colors">
                    Consultar con Ingeniería
                </a>
            </div>

        </div>
    </section>

    <!-- SECCIÓN: CATÁLOGO DE PRODUCTOS -->
    <section id="productos" class="py-24 bg-brand-dark border-b border-brand-steel">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            
            <div class="flex flex-col md:flex-row md:items-end justify-between mb-12">
                <div>
                    <span class="text-xs font-extrabold text-brand-orange uppercase tracking-widest block">Línea de Producción</span>
                    <h2 class="text-3xl sm:text-4xl font-black uppercase text-white tracking-tight">
                        Catálogo de Poleas Industriales
                    </h2>
                </div>
                <div class="mt-4 md:mt-0">
                    <p class="text-xs text-brand-light font-bold">Todas las piezas cuentan con acabados mecanizados CNC de alta precisión.</p>
                </div>
            </div>

            <!-- Grid de Productos -->
            <div class="grid sm:grid-cols-2 lg:grid-cols-4 gap-6">
                
                <!-- Producto 1 -->
                <div class="bg-brand-steel/30 border border-brand-steel hover:border-brand-orange transition-all group overflow-hidden">
                    <div class="h-48 bg-black/60 flex items-center justify-center p-4 relative">
                        <!-- Icono / Gráfico Ilustrativo -->
                        <i class="fa-solid fa-gear text-6xl text-brand-orange group-hover:scale-110 transition-transform"></i>
                        <span class="absolute top-3 left-3 bg-brand-orange text-black font-black text-[10px] px-2 py-0.5 uppercase">Canal V</span>
                    </div>
                    <div class="p-5">
                        <h3 class="font-extrabold uppercase text-white text-base">Polea Tipo V (A, B, C)</h3>
                        <p class="text-xs text-brand-light mt-1 mb-4">Disponible de 1 a 6 ranuras. Para motores eléctricos y transmisión de potencia continua.</p>
                        <div class="flex justify-between items-center text-xs border-t border-brand-steel pt-3">
                            <span class="text-brand-light font-bold">Aluminio Reforzado</span>
                            <a href="#cotizar" class="text-brand-orange font-bold uppercase hover:underline">Cotizar <i class="fa-solid fa-angle-right"></i></a>
                        </div>
                    </div>
                </div>

                <!-- Producto 2 -->
                <div class="bg-brand-steel/30 border border-brand-steel hover:border-brand-orange transition-all group overflow-hidden">
                    <div class="h-48 bg-black/60 flex items-center justify-center p-4 relative">
                        <i class="fa-solid fa-dharmachakra text-6xl text-brand-light group-hover:text-brand-orange group-hover:scale-110 transition-all"></i>
                        <span class="absolute top-3 left-3 bg-brand-steel text-white font-black text-[10px] px-2 py-0.5 uppercase">Escalonada</span>
                    </div>
                    <div class="p-5">
                        <h3 class="font-extrabold uppercase text-white text-base">Polea Escalonada</h3>
                        <p class="text-xs text-brand-light mt-1 mb-4">Para cambio progresivo de velocidades en taladros, tornos y maquinaria de taller.</p>
                        <div class="flex justify-between items-center text-xs border-t border-brand-steel pt-3">
                            <span class="text-brand-light font-bold">Varias Etapas</span>
                            <a href="#cotizar" class="text-brand-orange font-bold uppercase hover:underline">Cotizar <i class="fa-solid fa-angle-right"></i></a>
                        </div>
                    </div>
                </div>

                <!-- Producto 3 -->
                <div class="bg-brand-steel/30 border border-brand-steel hover:border-brand-orange transition-all group overflow-hidden">
                    <div class="h-48 bg-black/60 flex items-center justify-center p-4 relative">
                        <i class="fa-solid fa-compact-disc text-6xl text-brand-orange group-hover:scale-110 transition-transform"></i>
                        <span class="absolute top-3 left-3 bg-brand-orange text-black font-black text-[10px] px-2 py-0.5 uppercase">Sincrónica</span>
                    </div>
                    <div class="p-5">
                        <h3 class="font-extrabold uppercase text-white text-base">Poleas Sincrónicas (Dentadas)</h3>
                        <p class="text-xs text-brand-light mt-1 mb-4">Cero deslizamiento. Para sistemas de automatización, robótica y control preciso.</p>
                        <div class="flex justify-between items-center text-xs border-t border-brand-steel pt-3">
                            <span class="text-brand-light font-bold">Paso HTD / XL</span>
                            <a href="#cotizar" class="text-brand-orange font-bold uppercase hover:underline">Cotizar <i class="fa-solid fa-angle-right"></i></a>
                        </div>
                    </div>
                </div>

                <!-- Producto 4 -->
                <div class="bg-brand-steel/30 border border-brand-steel hover:border-brand-orange transition-all group overflow-hidden">
                    <div class="h-48 bg-black/60 flex items-center justify-center p-4 relative">
                        <i class="fa-solid fa-industry text-6xl text-brand-light group-hover:text-brand-orange group-hover:scale-110 transition-all"></i>
                        <span class="absolute top-3 left-3 bg-brand-steel text-white font-black text-[10px] px-2 py-0.5 uppercase">Especial</span>
                    </div>
                    <div class="p-5">
                        <h3 class="font-extrabold uppercase text-white text-base">Poleas Especiales B2B</h3>
                        <p class="text-xs text-brand-light mt-1 mb-4">Fabricación según plano técnico, bocina cónica, cuñeros especiales y sobredimensiones.</p>
                        <div class="flex justify-between items-center text-xs border-t border-brand-steel pt-3">
                            <span class="text-brand-light font-bold">A la Medida</span>
                            <a href="#cotizar" class="text-brand-orange font-bold uppercase hover:underline">Cotizar <i class="fa-solid fa-angle-right"></i></a>
                        </div>
                    </div>
                </div>

            </div>

        </div>
    </section>

    <!-- SECCIÓN DE RESPALDO Y TESTIMONIO (ESTILO MANUAL) -->
    <section class="py-20 bg-brand-steel/10 border-b border-brand-steel">
        <div class="max-w-5xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <i class="fa-solid fa-quote-left text-4xl text-brand-orange mb-6 block"></i>
            <p class="text-xl sm:text-2xl font-extrabold uppercase text-white leading-relaxed tracking-wide mb-6">
                "Nuestros paros no planificados se redujeron radicalmente desde que estandarizamos con las poleas de aluminio Hermon. Calidad de aluminio real y tiempos de entrega que sí respetan."
            </p>
            <div class="inline-block border-t border-brand-orange pt-3">
                <p class="text-xs font-black uppercase text-brand-orange">Jefe de Mantenimiento Industrial</p>
                <p class="text-[11px] text-brand-light uppercase">Planta de Manufactura - CDMX</p>
            </div>
        </div>
    </section>

    <!-- SECCIÓN: FORMULARIO DE COTIZACIÓN Y SOLICITUD DE ASESORÍA -->
    <section id="cotizar" class="py-24 bg-brand-dark relative">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid lg:grid-cols-12 gap-12">
                
                <!-- Información de Contacto Directo -->
                <div class="lg:col-span-5 space-y-8">
                    <div>
                        <span class="text-xs font-extrabold text-brand-orange uppercase tracking-widest block mb-1">ATENCIÓN INMEDIATA B2B</span>
                        <h2 class="text-3xl font-black uppercase text-white">Solicita una Cotización o Asesoría Técnica</h2>
                        <div class="w-12 h-1 bg-brand-orange my-4"></div>
                        <p class="text-brand-light text-sm">
                            Atendemos solicitudes de plantas, talleres mecánicos, distribuidores y proyectos especiales. Garantizamos respuesta en tiempo récord.
                        </p>
                    </div>

                    <div class="space-y-4 text-sm">
                        <div class="flex items-start gap-4 p-4 bg-brand-steel/30 border border-brand-steel">
                            <i class="fa-solid fa-envelope text-brand-orange text-xl mt-1"></i>
                            <div>
                                <strong class="block text-white uppercase text-xs">Correo Directo</strong>
                                <span class="text-brand-light">contacto@hermon.com</span>
                            </div>
                        </div>

                        <div class="flex items-start gap-4 p-4 bg-brand-steel/30 border border-brand-steel">
                            <i class="fa-solid fa-globe text-brand-orange text-xl mt-1"></i>
                            <div>
                                <strong class="block text-white uppercase text-xs">Sitio Web Oficial</strong>
                                <span class="text-brand-light">hermon.com</span>
                            </div>
                        </div>

                        <div class="flex items-start gap-4 p-4 bg-brand-steel/30 border border-brand-steel">
                            <i class="fa-solid fa-truck-ramp-box text-brand-orange text-xl mt-1"></i>
                            <div>
                                <strong class="block text-white uppercase text-xs">Envíos & Logística</strong>
                                <span class="text-brand-light">Cobertura y entrega garantizada a nivel nacional</span>
                            </div>
                        </div>
                    </div>

                    <!-- Cuadro de Compromiso Hermon -->
                    <div class="p-6 bg-brand-steel border-l-4 border-brand-orange">
                        <h4 class="font-extrabold text-xs uppercase text-white mb-2">Compromiso Paro Cero</h4>
                        <p class="text-xs text-brand-light">
                            Si confirmas una fecha de entrega con nuestro equipo, esa fecha se cumple. La puntualidad forma parte de nuestro ADN familiar.
                        </p>
                    </div>
                </div>

                <!-- Formulario Interactivo -->
                <div class="lg:col-span-7 bg-brand-steel/20 p-8 sm:p-10 border border-brand-steel relative">
                    <h3 class="text-xl font-black uppercase text-white mb-6">Cotizador de Poleas y Pedidos</h3>
                    
                    <form id="quote-form" class="space-y-4">
                        <div class="grid sm:grid-cols-2 gap-4">
                            <div>
                                <label class="block text-[11px] font-bold uppercase text-brand-light mb-1">Nombre Completo *</label>
                                <input type="text" required placeholder="Ej. Ing. Carlos Mendoza" class="w-full bg-brand-dark border border-brand-steel px-4 py-3 text-sm text-white focus:outline-none focus:border-brand-orange">
                            </div>
                            <div>
                                <label class="block text-[11px] font-bold uppercase text-brand-light mb-1">Empresa / Taller *</label>
                                <input type="text" required placeholder="Nombre de la empresa" class="w-full bg-brand-dark border border-brand-steel px-4 py-3 text-sm text-white focus:outline-none focus:border-brand-orange">
                            </div>
                        </div>

                        <div class="grid sm:grid-cols-2 gap-4">
                            <div>
                                <label class="block text-[11px] font-bold uppercase text-brand-light mb-1">Correo Electrónico *</label>
                                <input type="email" required placeholder="correo@empresa.com" class="w-full bg-brand-dark border border-brand-steel px-4 py-3 text-sm text-white focus:outline-none focus:border-brand-orange">
                            </div>
                            <div>
                                <label class="block text-[11px] font-bold uppercase text-brand-light mb-1">Teléfono / WhatsApp *</label>
                                <input type="tel" required placeholder="10 dígitos" class="w-full bg-brand-dark border border-brand-steel px-4 py-3 text-sm text-white focus:outline-none focus:border-brand-orange">
                            </div>
                        </div>

                        <div class="grid sm:grid-cols-2 gap-4">
                            <div>
                                <label class="block text-[11px] font-bold uppercase text-brand-light mb-1">Tipo de Polea</label>
                                <select class="w-full bg-brand-dark border border-brand-steel px-4 py-3 text-sm text-white focus:outline-none focus:border-brand-orange">
                                    <option value="v">Polea Tipo V (Standard)</option>
                                    <option value="escalonada">Polea Escalonada</option>
                                    <option value="sincronica">Polea Sincrónica / Dentada</option>
                                    <option value="medida">Fabricación Especial con Matrices</option>
                                </select>
                            </div>
                            <div>
                                <label class="block text-[11px] font-bold uppercase text-brand-light mb-1">Cantidad Estimada</label>
                                <input type="number" min="1" value="10" class="w-full bg-brand-dark border border-brand-steel px-4 py-3 text-sm text-white focus:outline-none focus:border-brand-orange">
                            </div>
                        </div>

                        <div>
                            <label class="block text-[11px] font-bold uppercase text-brand-light mb-1">Especificaciones Técnicas / Mensaje</label>
                            <textarea rows="4" placeholder="Indica diámetros, número de canales, cuñeros o requerimientos especiales..." class="w-full bg-brand-dark border border-brand-steel px-4 py-3 text-sm text-white focus:outline-none focus:border-brand-orange"></textarea>
                        </div>

                        <button type="submit" class="w-full py-4 bg-brand-orange text-black font-extrabold text-sm uppercase tracking-wider hover:bg-white transition-all shadow-lg">
                            Enviar Solicitud de Cotización <i class="fa-solid fa-paper-plane ml-2"></i>
                        </button>

                        <p class="text-[10px] text-brand-light text-center">
                            Tus datos están protegidos. Respuesta garantizada en menos de 24 horas hábiles.
                        </p>
                    </form>
                </div>

            </div>
        </div>
    </section>

    <!-- FOOTER OFICIAL -->
    <footer class="bg-black border-t border-brand-steel py-12 text-brand-light text-xs">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex flex-col md:flex-row justify-between items-center gap-6">
                
                <!-- Logo & Tagline -->
                <div class="flex items-center gap-3">
                    <div class="w-8 h-8 bg-brand-orange flex items-center justify-center font-black text-black text-xl tracking-tighter">
                        H
                    </div>
                    <div>
                        <span class="block font-black text-white text-base tracking-wider">HERMON</span>
                        <span class="block text-[9px] uppercase tracking-widest text-brand-orange font-bold">INGENIERÍA QUE NO PARA.</span>
                    </div>
                </div>

                <!-- Copyright -->
                <div class="text-center md:text-right space-y-1">
                    <p>© 2025 HERMON POLEAS DE ALUMINIO. Todos los derechos reservados.</p>
                    <p class="text-[10px] text-brand-mid">Especialistas en fabricación de poleas de alta aleación con matrices industriales.</p>
                </div>

            </div>
        </div>
    </footer>

    <!-- LÓGICA JAVASCRIPT -->
    <script>
        // Menú Móvil
        const mobileBtn = document.getElementById('mobile-menu-btn');
        const mobileMenu = document.getElementById('mobile-menu');
        const mobileLinks = document.querySelectorAll('.mobile-link');

        mobileBtn.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });

        mobileLinks.forEach(link => {
            link.addEventListener('click', () => {
                mobileMenu.classList.add('hidden');
            });
        });

        // Manejo del Formulario de Cotización con Notificación Custom
        const quoteForm = document.getElementById('quote-form');
        const toast = document.getElementById('notification-toast');
        const toastTitle = document.getElementById('toast-title');
        const toastDesc = document.getElementById('toast-desc');

        function showToast(title, desc) {
            toastTitle.textContent = title;
            toastDesc.textContent = desc;
            toast.classList.remove('translate-y-20', 'opacity-0', 'pointer-events-none');
            
            setTimeout(() => {
                toast.classList.add('translate-y-20', 'opacity-0', 'pointer-events-none');
            }, 4500);
        }

        quoteForm.addEventListener('submit', (e) => {
            e.preventDefault();
            showToast('¡Cotización Recibida!', 'Nos pondremos en contacto con usted a la brevedad posible para enviarle la propuesta técnica.');
            quoteForm.reset();
        });
    </script>
</body>
</html>

