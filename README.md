# Hotel-Casa-Colonial
Infografia de Hotel Casa Colonial San Antonio del Tachira
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Infografía: Hotel Casa Colonial, San Antonio del Táchira</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;700;900&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
        }
        .chart-container {
            position: relative;
            width: 100%;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
            height: 350px;
            max-height: 45vh;
        }
        @media (max-width: 768px) {
            .chart-container {
                height: 300px;
                max-height: 50vh;
            }
        }
        .background-slider {
            background-size: cover;
            background-position: center;
            transition: background-image 1.5s ease-in-out;
        }
    </style>
</head>
<body class="text-gray-800">

    <!-- Contenedor para la imagen de fondo con capa semitransparente -->
    <div id="background-slider" class="fixed inset-0 z-0 bg-cover bg-center background-slider">
        <div class="absolute inset-0 bg-black opacity-30"></div>
    </div>

    <!-- El contenido principal de la infografía flotará sobre el fondo -->
    <div class="relative z-10 container mx-auto p-4 md:p-8">

        <header class="text-center mb-12">
            <h1 class="text-4xl md:text-6xl font-black text-white mb-2">Hotel Casa Colonial</h1>
            <p class="text-xl md:text-2xl text-[#F5DEB3]">Su Refugio Estratégico en San Antonio del Táchira</p>
        </header>

        <main class="space-y-8">
            
            <section class="bg-white rounded-2xl shadow-2xl p-6 md:p-8 grid grid-cols-1 md:grid-cols-2 gap-8 items-center">
                <div class="md:col-span-1">
                    <h2 class="text-3xl font-bold text-[#5C4033] mb-4">Calidad Validada por Cientos de Viajeros</h2>
                    <p class="text-lg mb-4">La experiencia en Casa Colonial no solo es una promesa, es un hecho respaldado por cientos de reseñas. Con una calificación promedio sobresaliente, el hotel se consolida como una de las opciones más confiables y recomendadas de la región.</p>
                    <div class="flex items-center justify-center md:justify-start space-x-4">
                        <span class="text-7xl font-black text-[#8B4513]">8.4</span>
                        <span class="text-xl font-bold text-gray-600">/ 10<br>Muy Bueno</span>
                    </div>
                     <p class="text-sm text-gray-500 mt-2 text-center md:text-left">*Basado en más de 650 opiniones en plataformas líderes.</p>
                </div>
                <div class="md:col-span-1">
                    <div class="chart-container h-[300px] md:h-[350px]">
                        <canvas id="guestRatingChart"></canvas>
                    </div>
                </div>
            </section>

            <section class="bg-white rounded-2xl shadow-2xl p-6 md:p-8">
                <h2 class="text-3xl font-bold text-[#5C4033] mb-2 text-center">Ubicación Central para el Viajero</h2>
                <p class="text-lg text-center max-w-3xl mx-auto mb-10">La ubicación del Hotel Casa Colonial es inmejorable, posicionándolo como el punto de partida perfecto para diligencias, turismo y tránsito internacional. Todo lo que necesita está a solo unos pasos de distancia.</p>
                <div class="relative flex flex-col items-center">
                    <div class="bg-[#8B4513] text-white p-4 rounded-xl shadow-lg z-10">
                        <h3 class="font-bold text-xl">📍 Hotel Casa Colonial</h3>
                    </div>
                    <div class="w-full grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8 mt-16">
                        <div class="text-center p-4 bg-[#F5DEB3] rounded-lg">
                            <span class="text-4xl">🏛️</span>
                            <h4 class="font-bold mt-2">Plaza Bolívar y Catedral</h4>
                            <p class="text-2xl font-bold text-[#8B4513]">1 Cuadra</p>
                        </div>
                        <div class="text-center p-4 bg-[#F5DEB3] rounded-lg">
                            <span class="text-4xl">🛂</span>
                            <h4 class="font-bold mt-2">Oficina del SAIME</h4>
                            <p class="text-2xl font-bold text-[#8B4513]">4 Cuadras</p>
                        </div>
                        <div class="text-center p-4 bg-[#F5DEB3] rounded-lg">
                             <span class="text-4xl">🌉</span>
                            <h4 class="font-bold mt-2">Puente Internacional</h4>
                            <p class="text-2xl font-bold text-[#8B4513]">7 Cuadras</p>
                        </div>
                        <div class="text-center p-4 bg-[#F5DEB3] rounded-lg">
                            <span class="text-4xl">✈️</span>
                            <h4 class="font-bold mt-2">Aeropuerto J.V. Gómez</h4>
                            <p class="text-2xl font-bold text-[#8B4513]">~8 Minutos</p>
                        </div>
                    </div>
                </div>
            </section>
            
            <section class="grid grid-cols-1 lg:grid-cols-5 gap-8">
                <div class="lg:col-span-3 bg-white rounded-2xl shadow-2xl p-6 md:p-8">
                    <h2 class="text-3xl font-bold text-[#5C4033] mb-4">Alojamiento y Precios Competitivos</h2>
                    <p class="text-lg mb-6">El hotel ofrece una excelente relación calidad-precio con habitaciones para cada necesidad, desde viajeros solos hasta familias numerosas. Los precios asequibles no comprometen la comodidad ni la calidad del servicio.</p>
                    <div class="chart-container h-[400px]">
                        <canvas id="roomPricesChart"></canvas>
                    </div>
                </div>
                <div class="lg:col-span-2 bg-white rounded-2xl shadow-2xl p-6 md:p-8">
                    <h2 class="text-3xl font-bold text-[#5C4033] mb-4">Servicios que Marcan la Diferencia</h2>
                    <p class="text-lg mb-6">Más allá de lo básico, Casa Colonial ofrece comodidades pensadas para la tranquilidad y conveniencia total del huésped.</p>
                    <ul class="space-y-4">
                        <li class="flex items-center text-lg"><span class="text-3xl mr-4">🔌</span> Planta Eléctrica de Respaldo</li>
                        <li class="flex items-center text-lg"><span class="text-3xl mr-4">📶</span> Wi-Fi Gratuito en todo el hotel</li>
                        <li class="flex items-center text-lg"><span class="text-3xl mr-4">❄️</span> Aire Acondicionado individual por habitación</li>
                        <li class="flex items-center text-lg"><span class="text-3xl mr-4">🔒</span> Seguridad y Vigilancia 24/7</li>
                        <li class="flex items-center text-lg"><span class="text-3xl mr-4">🐾</span> Admite Mascotas (sin restricciones)</li>
                        <li class="flex items-center text-lg"><span class="text-3xl mr-4">🏍️</span> Parking Techado para Motos</li>
                        <li class="flex items-center text-lg"><span class="text-3xl mr-4">🧼</span> Protocolos de Higiene Rigurosos</li>
                    </ul>
                </div>
            </section>
            
            <section class="bg-white rounded-2xl shadow-2xl p-6 md:p-8">
                <h2 class="text-3xl font-bold text-[#5C4033] mb-6 text-center">La Voz de Nuestros Huéspedes</h2>
                 <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                    <blockquote class="bg-[#F5DEB3] p-6 rounded-lg">
                        <p class="text-lg italic">"La atención increíble del personal, nos sentimos en casa. Muy bien ubicado y con sitios de comida a domicilio exquisitos cerca."</p>
                        <footer class="mt-4 font-bold">- Huésped de Booking.com</footer>
                    </blockquote>
                    <blockquote class="bg-[#F5DEB3] p-6 rounded-lg">
                        <p class="text-lg italic">"La relación precio-calidad es muy buena. Todo súper limpio, el aire acondicionado perfecto y la atención del personal es súper querida."</p>
                        <footer class="mt-4 font-bold">- Huésped de Booking.com</footer>
                    </blockquote>
                    <blockquote class="bg-[#F5DEB3] p-6 rounded-lg">
                        <p class="text-lg italic">"Excelente ubicación, cerca al SAIME para los que necesitamos hacer trámites. Un ambiente muy familiar y seguro. Recomendado."</p>
                        <footer class="mt-4 font-bold">- Huésped de Trivago</footer>
                    </blockquote>
                    <blockquote class="bg-[#F5DEB3] p-6 rounded-lg">
                        <p class="text-lg italic">"Un lugar de paso, estratégico por su ubicación."</p>
                        <footer class="mt-4 font-bold">- Elena (Airbnb)</footer>
                    </blockquote>
                    <blockquote class="bg-[#F5DEB3] p-6 rounded-lg">
                        <p class="text-lg italic">"Super amable el personal. De fácil acceso. Recomendadísimo."</p>
                        <footer class="mt-4 font-bold">- Emily (Airbnb)</footer>
                    </blockquote>
                    <blockquote class="bg-[#F5DEB3] p-6 rounded-lg">
                        <p class="text-lg italic">"Excelente estadía , todo fue tal cuál lo ofrecido. La atención, y calidad humana es impresionantemente buena y de calidad, sin duda alguna recomiendo esta opción de hospedaje. Muchas gracias por tanta atención, y excelencia!"</p>
                        <footer class="mt-4 font-bold">- Carlos (Airbnb)</footer>
                    </blockquote>
                     <blockquote class="bg-[#F5DEB3] p-6 rounded-lg">
                        <p class="text-lg italic">"Vacaciones · Viajero solitario."</p>
                        <footer class="mt-4 font-bold">- Amador Tovar (Google Maps)</footer>
                    </blockquote>
                    <blockquote class="bg-[#F5DEB3] p-6 rounded-lg">
                        <p class="text-lg italic">"Excelente ubicación. Personal muy gentil."</p>
                        <footer class="mt-4 font-bold">- Ely Gonzalez (Google Maps)</footer>
                    </blockquote>
                    <blockquote class="bg-[#F5DEB3] p-6 rounded-lg">
                        <p class="text-lg italic">"Por su relación precio calidad y su ubicación céntrica lo recomiendo."</p>
                        <footer class="mt-4 font-bold">- Antonio Ovalles (Google Maps)</footer>
                    </blockquote>
                    <blockquote class="bg-[#F5DEB3] p-6 rounded-lg">
                        <p class="text-lg italic">"Es un hotel pequeño pero muy familiar ya acogedor, con hermosos pasillos decorados muy lindos haciéndolo sentir a uno en casa, la habitación es limpia y cómoda, sábanas limpias y bonitas, TV, ac excelente, lo mejor de todo es la atención de las chicas de recepción, soñé espléndidas te ayudan con tu equipaje y te dan la bienvenida con una sonrisa, acompañada de un cafecito o té que endulzan el corazón, muy bien ubicado cerca de la avenida principal y el saine, los recomendamos ampliamente! Forman un muy buen equipo, sigan adelante, nos vamos mañana complacidos por haber descansado en sus lindas instalaciones!"</p>
                        <footer class="mt-4 font-bold">- carlos (Google Maps)</footer>
                    </blockquote>
                </div>
                 <div class="mt-8">
                     <h3 class="text-2xl font-bold text-center text-[#5C4033] mb-4">Consistencia en Calificaciones</h3>
                     <p class="text-lg text-center max-w-3xl mx-auto mb-6">El alto nivel de satisfacción se mantiene consistente a través de diferentes plataformas de reserva, incluyendo Booking.com, Trivago, **151 evaluaciones de Airbnb**, **263 valoraciones de 10/10 en Google Maps** y otras, demostrando un compromiso sólido con la calidad del servicio a lo largo del tiempo.</p>
                    <div class="chart-container h-[400px]">
                        <canvas id="reviewPlatformChart"></canvas>
                    </div>
                </div>
            </section>
        </main>
        
        <footer class="text-center mt-12 py-6 border-t border-[#8B4513] text-white">
            <p class="text-lg">¿Listo para una estancia cómoda y conveniente?</p>
            <p class="text-[#F5DEB3] text-xl font-bold mt-1">Contacta al Hotel Casa Colonial: WhatsApp +58 276 7712679</p>
             <div class="mt-4 text-xs text-[#D2B48C]">
                <p>Infografía generada con datos del informe público del Hotel Casa Colonial.</p>
                <!-- 
                    Palette: Colonial Browns.
                    Narrative Plan: Introduction (Hook with rating) -> Location Advantage -> Room Offerings -> Key Services -> Guest Testimonials -> Conclusion/CTA.
                    Visualization Choices:
                    - Guest Rating: Goal: Inform. Viz: Donut Chart (Chart.js). Justification: Visually appealing way to show a single, key proportion.
                    - Location Proximity: Goal: Organize. Viz: HTML/CSS Flow Diagram. Justification: Clear, structured way to show relationships without maps/SVG.
                    - Room Prices: Goal: Compare. Viz: Horizontal Bar Chart (Chart.js). Justification: Best for comparing values across distinct categories (rooms).
                    - Amenities: Goal: Organize. Viz: Icon List (HTML/CSS Pictograph). Justification: Scannable and visually engaging way to list features.
                    - Review Platforms: Goal: Compare. Viz: Bar Chart (Chart.js). Justification: Compares ratings across platforms while showing the volume of reviews for context.
                    Confirmation: NO SVG was used. NO Mermaid JS was used. All charts are rendered on Canvas by Chart.js. All diagrams are structured HTML/CSS with Tailwind.
                -->
            </div>
        </footer>

    </div>

    <script>
        const colonialBrowns = {
            primaryDark: '#5C4033',
            secondaryDark: '#8B4513',
            accentMedium: '#A0522D',
            lightNeutral: '#D2B48C',
            veryLightNeutral: '#F5DEB3'
        };

        const defaultChartOptions = {
            maintainAspectRatio: false,
            plugins: {
                legend: {
                    labels: {
                        color: colonialBrowns.primaryDark,
                        font: {
                            size: 14
                        }
                    }
                },
                tooltip: {
                    callbacks: {
                        title: function(tooltipItems) {
                            const item = tooltipItems[0];
                            let label = item.chart.data.labels[item.dataIndex];
                            if (Array.isArray(label)) {
                                return label.join(' ');
                            }
                            return label;
                        }
                    }
                }
            }
        };
        
        function wrapLabel(str, maxWidth = 16) {
            if (str.length <= maxWidth) return str;
            let wrapped = [];
            let words = str.split(' ');
            let currentLine = '';
            for (let word of words) {
                if ((currentLine + ' ' + word).trim().length > maxWidth) {
                    wrapped.push(currentLine.trim());
                    currentLine = word;
                } else {
                    currentLine = (currentLine + ' ' + word).trim();
                }
            }
            if (currentLine) {
                wrapped.push(currentLine.trim());
            }
            return wrapped;
        }


        new Chart(document.getElementById('guestRatingChart'), {
            type: 'doughnut',
            data: {
                labels: ['Calificación', 'Restante para 10'],
                datasets: [{
                    label: 'Calificación de Huéspedes',
                    data: [8.4, 1.6],
                    backgroundColor: [colonialBrowns.secondaryDark, colonialBrowns.veryLightNeutral],
                    borderColor: [colonialBrowns.secondaryDark, colonialBrowns.veryLightNeutral],
                    borderWidth: 1,
                    cutout: '70%'
                }]
            },
            options: {
                ...defaultChartOptions,
                 plugins: {
                    ...defaultChartOptions.plugins,
                    legend: { display: false },
                    tooltip: { enabled: false }
                }
            }
        });

        const roomLabels = [
            'Matrimonial Sencilla',
            'Matrimonial Superior',
            'Triple (3p)',
            'Familiar Sencilla (3-4p)',
            'Familiar Grande (5p)'
        ].map(label => wrapLabel(label));

        new Chart(document.getElementById('roomPricesChart'), {
            type: 'bar',
            data: {
                labels: roomLabels,
                datasets: [{
                    label: 'Precio por Noche (USD)',
                    data: [20, 25, 25, 30, 35],
                    backgroundColor: colonialBrowns.accentMedium,
                    borderColor: colonialBrowns.secondaryDark,
                    borderWidth: 2,
                    borderRadius: 5
                }]
            },
            options: {
                ...defaultChartOptions,
                indexAxis: 'y',
                scales: {
                    x: {
                        beginAtZero: true,
                        grid: {
                            color: '#e0e0e0'
                        },
                         ticks: {
                            color: colonialBrowns.primaryDark,
                             callback: function(value) {
                                return '$' + value;
                            }
                        }
                    },
                    y: {
                        grid: {
                            display: false
                        },
                        ticks: {
                           color: colonialBrowns.primaryDark
                        }
                    }
                },
                plugins: {
                    ...defaultChartOptions.plugins,
                    legend: {
                        display: false
                    }
                }
            }
        });

        new Chart(document.getElementById('reviewPlatformChart'), {
            type: 'bar',
            data: {
                labels: [wrapLabel('Trivago (General)'), wrapLabel('Booking.com (Consolidado)'), wrapLabel('Airbnb (General)'), wrapLabel('Google Maps (General)'), wrapLabel('Booking.com (Reciente)')],
                datasets: [{
                    label: 'Calificación Promedio',
                    data: [8.4, 8.4, 9.2, 10.0, 9.4],
                    backgroundColor: [colonialBrowns.lightNeutral, colonialBrowns.lightNeutral, colonialBrowns.lightNeutral, colonialBrowns.lightNeutral, colonialBrowns.lightNeutral],
                    borderColor: [colonialBrowns.secondaryDark, colonialBrowns.secondaryDark, colonialBrowns.secondaryDark, colonialBrowns.secondaryDark, colonialBrowns.secondaryDark],
                    yAxisID: 'y'
                }, {
                    label: 'Número de Reseñas',
                    data: [657, 450, 151, 263, 20],
                    backgroundColor: [colonialBrowns.primaryDark, colonialBrowns.primaryDark, colonialBrowns.primaryDark, colonialBrowns.primaryDark, colonialBrowns.primaryDark],
                    borderColor: [colonialBrowns.primaryDark, colonialBrowns.primaryDark, colonialBrowns.primaryDark, colonialBrowns.primaryDark, colonialBrowns.primaryDark],
                    yAxisID: 'y1'
                }]
            },
            options: {
                ...defaultChartOptions,
                scales: {
                    x: {
                        ticks: { color: colonialBrowns.primaryDark }
                    },
                    y: {
                        type: 'linear',
                        display: true,
                        position: 'left',
                        title: {
                            display: true,
                            text: 'Calificación (0-10)',
                            color: colonialBrowns.primaryDark
                        },
                        max: 10,
                        min: 0
                    },
                    y1: {
                        type: 'linear',
                        display: true,
                        position: 'right',
                        title: {
                            display: true,
                            text: 'Número de Reseñas',
                            color: colonialBrowns.primaryDark
                        },
                        grid: {
                            drawOnChartArea: false
                        }
                    }
                }
            }
        });

        const backgroundImages = [
            "https://placehold.co/1920x1080/5C4033/F5DEB3?text=Fachada+Hotel",
            "https://placehold.co/1920x1080/8B4513/F5DEB3?text=Recepción",
            "https://placehold.co/1920x1080/A0522D/F5DEB3?text=Sala+Estar",
            "https://placehold.co/1920x1080/D2B48C/5C4033?text=Pasillo+Interior"
        ];
        let currentImageIndex = 0;
        const backgroundSlider = document.getElementById('background-slider');

        function changeBackgroundImage() {
            currentImageIndex = (currentImageIndex + 1) % backgroundImages.length;
            backgroundSlider.style.backgroundImage = `url('${backgroundImages[currentImageIndex]}')`;
        }

        // Set initial background image
        backgroundSlider.style.backgroundImage = `url('${backgroundImages[currentImageIndex]}')`;

        // Change image every 7 seconds
        setInterval(changeBackgroundImage, 7000); 
    </script>
</body>
</html>
