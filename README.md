<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Programa Oficial AntoPuntos: Reconocimiento Exclusivo al Amor y la Conexión</title>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700&family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        /* Base Styles */
        body {
            font-family: 'Poppins', sans-serif;
            line-height: 1.7;
            margin: 0;
            padding: 0;
            background-color: #fce4ec; /* Soft pink background */
            color: #333;
            overflow-x: hidden; /* Prevent horizontal scroll */
        }

        /* Container */
        .container {
            max-width: 1000px;
            margin: 40px auto; /* Increased top/bottom margin */
            padding: 20px;
            background-color: #fff;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.15); /* Stronger shadow */
            transform: translateY(20px); /* Slight lift on load */
            opacity: 0; /* Hidden initially */
            animation: fadeIn 1s forwards ease-out;
        }

        @keyframes fadeIn {
            to {
                transform: translateY(0);
                opacity: 1;
            }
        }

        /* Header Section */
        header {
            text-align: center;
            padding: 50px 20px; /* More padding */
            background: linear-gradient(135deg, #ff6f91 0%, #a218f7 100%); /* Slightly more serious gradient */
            color: #fff;
            border-radius: 18px 18px 0 0; /* Rounded top corners */
            margin-bottom: 40px; /* More margin */
            position: relative;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2); /* Shadow for header */
        }

        header::before { /* Decorative overlay */
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(255, 255, 255, 0.1);
            clip-path: circle(15% at 5% 10%) circle(10% at 90% 80%) circle(8% at 30% 95%); /* More abstract shapes */
        }

        header h1 {
            font-family: 'Playfair Display', serif;
            font-size: 4.2em; /* Slightly adjusted for longer title */
            margin-bottom: 15px;
            letter-spacing: 1.5px; /* More spacing */
            text-shadow: 3px 3px 6px rgba(0, 0, 0, 0.3); /* Stronger shadow for text */
            position: relative;
            z-index: 1;
        }

        header p {
            font-size: 1.3em; /* Larger intro text */
            font-weight: 300;
            max-width: 750px;
            margin: 0 auto;
            position: relative;
            z-index: 1;
        }

        /* Section Headings */
        section {
            margin-bottom: 60px; /* More space between sections */
            padding: 0 20px;
        }

        section h2 {
            font-family: 'Playfair Display', serif;
            color: #b70043; /* Darker, more serious pink */
            font-size: 2.8em; /* Adjusted for longer titles */
            text-align: center;
            margin-bottom: 40px;
            position: relative;
        }

        section h2::after {
            content: '';
            display: block;
            width: 120px; /* Wider line */
            height: 5px; /* Thicker line */
            background-color: #e91e63; /* Solid pink for seriousness */
            margin: 15px auto 0;
            border-radius: 5px;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.15);
        }

        /* Introduction Text for sections */
        .section-intro-text {
            text-align: center;
            font-size: 1.15em;
            color: #555;
            max-width: 800px;
            margin: 0 auto 50px; /* More bottom margin */
        }

        /* Points Grid */
        .point-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); /* Larger minimum width */
            gap: 35px; /* More gap */
            margin-top: 40px;
        }

        .point-card {
            background-color: #fff0f5; /* Very light pink */
            border-radius: 18px; /* More rounded corners */
            padding: 30px; /* More padding */
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1); /* Stronger shadow */
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            text-align: center;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            align-items: center;
            border: 2px solid #ffccd2; /* More prominent border */
        }

        .point-card:hover {
            transform: translateY(-10px) scale(1.03); /* More pronounced lift */
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
        }

        .point-card h3 {
            color: #a00030; /* Darker red-pink */
            font-size: 1.7em; /* Adjusted for longer titles */
            margin-bottom: 12px;
            font-weight: 600;
            display: flex;
            align-items: center;
            justify-content: center;
            border-bottom: 1px solid #ffdde1; /* Subtle line under title */
            padding-bottom: 10px;
            width: 100%;
        }

        .point-card h3 i {
            margin-right: 12px; /* More space for icon */
            color: #e91e63;
            font-size: 1.3em;
        }

        .point-card p {
            font-size: 1.05em; /* Slightly larger text */
            color: #555;
            flex-grow: 1;
            margin-bottom: 25px; /* More bottom margin */
        }

        .point-value {
            background-color: #e91e63; /* Solid pink for points for seriousness */
            color: #fff; /* White text on points */
            font-weight: 700;
            font-size: 1.3em;
            padding: 10px 25px;
            border-radius: 30px;
            box-shadow: 0 3px 8px rgba(0, 0, 0, 0.2); /* Stronger shadow for points */
            display: inline-block;
        }

        /* Info Blocks (Registration / Rewards) */
        .info-block {
            background-color: #ffeff3; /* Lighter, more solid pink */
            padding: 40px;
            border-radius: 18px;
            margin-top: 50px;
            text-align: center;
            box-shadow: inset 0 4px 10px rgba(0, 0, 0, 0.1);
            border: 1px solid #ffccd2;
        }

        .info-block h3 {
            font-family: 'Playfair Display', serif;
            color: #b70043;
            font-size: 2.4em;
            margin-bottom: 25px;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        .info-block h3 i {
            margin-right: 18px;
            color: #e91e63;
            font-size: 1.2em;
        }

        .info-block p {
            font-size: 1.15em;
            color: #444;
            margin-bottom: 25px;
        }

        .info-block ul {
            list-style: none;
            padding: 0;
            margin: 30px 0;
            display: inline-block;
            text-align: left;
            width: 100%; /* Ensure list takes full width for alignment */
        }

        .info-block ul li {
            background-color: #fff;
            margin-bottom: 15px;
            padding: 18px 30px;
            border-radius: 12px;
            box-shadow: 0 3px 10px rgba(0,0,0,0.08);
            font-weight: 500;
            color: #666;
            transition: background-color 0.3s ease, transform 0.2s ease;
            display: flex;
            align-items: center;
            font-size: 1.05em;
            border: 1px solid #eee;
        }

        .info-block ul li i {
            margin-right: 12px;
            color: #e91e63;
            font-size: 1.1em;
        }

        .info-block ul li:hover {
            background-color: #fff8fb;
            transform: translateX(5px);
        }

        .key-pillars {
            font-weight: 600;
            margin-top: 25px;
            color: #777;
            font-size: 1.1em;
        }

        /* Footer */
        footer {
            text-align: center;
            margin-top: 70px;
            padding: 40px 20px;
            border-top: 2px solid #e91e63;
            color: #666;
            font-size: 1em;
            background-color: #f8bbd0;
            border-radius: 0 0 20px 20px;
            box-shadow: 0 -5px 15px rgba(0, 0, 0, 0.08);
            font-weight: 500;
        }

        footer p {
            margin: 8px 0;
        }

        .enrollment-section {
            background-color: #ffdde1; /* Soft contrasting color */
            padding: 30px;
            border-radius: 15px;
            margin-top: 50px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            text-align: center;
            color: #333;
        }

        .enrollment-section h3 {
            font-family: 'Playfair Display', serif;
            color: #a00030;
            font-size: 2.2em;
            margin-bottom: 20px;
        }

        .enrollment-section p {
            font-size: 1.1em;
            margin-bottom: 15px;
        }

        .enrollment-section .phone-number {
            font-size: 1.5em;
            font-weight: 700;
            color: #e91e63;
            display: block;
            margin-top: 20px;
        }

        /* Responsive Adjustments */
        @media (max-width: 768px) {
            .container {
                margin: 20px auto;
                padding: 10px;
            }
            header h1 {
                font-size: 2.8em;
            }
            header p {
                font-size: 1.1em;
            }
            section h2 {
                font-size: 2.2em;
            }
            .section-intro-text {
                font-size: 1em;
                margin-bottom: 30px;
            }
            .point-grid {
                grid-template-columns: 1fr;
            }
            .point-card {
                padding: 20px;
            }
            .point-card h3 {
                font-size: 1.5em;
            }
            .point-card p {
                font-size: 0.95em;
            }
            .point-value {
                font-size: 1.1em;
                padding: 8px 20px;
            }
            .info-block {
                padding: 25px;
            }
            .info-block h3 {
                font-size: 2em;
            }
            .info-block p {
                font-size: 1em;
            }
            .info-block ul li {
                padding: 12px 20px;
                font-size: 0.95em;
            }
            footer {
                padding: 20px 10px;
                font-size: 0.85em;
            }
            .enrollment-section h3 {
                font-size: 1.8em;
            }
            .enrollment-section .phone-number {
                font-size: 1.3em;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>Programa Oficial AntoPuntos</h1>
            <p><strong>Reconocimiento Exclusivo al Amor y la Conexión</strong></p>
            <p>Este sistema ha sido diseñado meticulosamente para celebrar y recompensar cada uno de tus gestos. ¡Con **AntoPuntos**, tu dedicación se transformará en beneficios tangibles y experiencias exclusivas para ti!</p>
        </header>

        <section>
            <h2>I. Sistema de Acumulación de AntoPuntos</h2>
            <p class="section-intro-text">
                Cada acción que realices contribuirá directamente a tu saldo de **AntoPuntos**. Estos puntos son el reflejo y reconocimiento de tu valiosa contribución a nuestra felicidad y bienestar mutuo.
            </p>

            <div class="point-grid">
                <div class="point-card">
                    <h3><i class="fas fa-hand-holding-heart"></i> Muestras de Afecto Espontáneo</h3>
                    <p>Un beso o abrazo inesperado, un mensaje de cariño no solicitado, o una expresión verbal sincera de amor y aprecio.</p>
                    <span class="point-value">5 Puntos</span>
                </div>
                <div class="point-card">
                    <h3><i class="fas fa-lightbulb"></i> Actos de Consideración y Detalle</h3>
                    <p>Preparar mi bebida favorita sin que lo pida, dejar notas reflexivas, recordar y preguntar por un evento importante, o un cumplido específico y auténtico.</p>
                    <span class="point-value">10 Puntos</span>
                </div>
                <div class="point-card">
                    <h3><i class="fas fa-ear-listen"></i> Soporte Emocional Activo</h3>
                    <p>Escuchar con plena atención y empatía mis preocupaciones, ofrecer soluciones o consuelo, brindar ánimo ante desafíos, o expresar defensa y apoyo público.</p>
                    <span class="point-value">15 Puntos</span>
                </div>
                <div class="point-card">
                    <h3><i class="fas fa-calendar-check"></i> Inversión en Tiempo de Calidad</h3>
                    <p>Proponer y organizar una actividad o cita exclusiva, o dedicar tiempo sin distracciones a intereses compartidos.</p>
                    <span class="point-value">20 Puntos</span>
                </div>
                <div class="point-card">
                    <h3><i class="fas fa-concierge-bell"></i> Gestos de Servicio Desinteresado</h3>
                    <p>Ofrecer un masaje relajante, preparar su comida predilecta, realizar una tarea doméstica que no le agrada, o cuidar de su bienestar en momentos de necesidad.</p>
                    <span class="point-value">25 Puntos</span>
                </div>
                <div class="point-card">
                    <h3><i class="fas fa-gifts"></i> Sorpresas y Celebraciones Significativas</h3>
                    <p>Organizar una pequeña conmemoración por un logro o fecha especial, o una sorpresa inesperada que genere alegría.</p>
                    <span class="point-value">30 Puntos</span>
                </div>
                <div class="point-card">
                    <h3><i class="fas fa-fire-alt"></i> Demostraciones de Pasión e Iniciativa</h3>
                    <p>Tomar la iniciativa en momentos de intimidad, planificar una experiencia romántica especial (como una escapada o velada), o expresar admiración profunda por sus cualidades y talentos.</p>
                    <span class="point-value">40 Puntos</span>
                </div>
            </div>
        </section>

        <section>
            <h2>II. Beneficios Inmediatos por Inscripción</h2>
            <div class="info-block">
                <h3>¡Acceso Instantáneo al Ser Parte de AntoPuntos!</h3>
                <p>Por el solo hecho de tu inscripción en el programa **AntoPuntos**, recibirás acceso instantáneo y exclusivo a:</p>
                <ul>
                    <li><i class="fas fa-headset"></i> <strong>Atención y Cobertura 24/7:</strong> Soporte dedicado y continuo en todas las áreas que necesites.</li>
                    <li><i class="fas fa-lightbulb"></i> <strong>Asesorías Especializadas:</strong> Acceso a orientación en temas **Legales, de Salud, Finanzas, Estilo de Vida y Entretenimiento**.</li>
                    <li><i class="fas fa-concierge-bell"></i> <strong>Servicios Exclusivos:</strong> Incluyen **Personal Shopper** y **Traslados** coordinados para tu comodidad.</li>
                </ul>
                <p class="key-pillars">Es importante destacar que estos beneficios inmediatos también se extienden a **tu familia directa**, reafirmando nuestro compromiso con su bienestar integral.</p>
            </div>
        </section>

        <section>
            <h2>III. Catálogo de Beneficios Exclusivos por Canje de AntoPuntos</h2>
            <p class="section-intro-text">
                Al acumular tus **AntoPuntos**, podrás acceder a una selección premium de beneficios y experiencias diseñadas y pensadas exclusivamente para ti, para proporcionarte momentos de gran satisfacción y disfrute personal y compartido.
            </p>
            <div class="info-block">
                <h3>¡Tus Puntos, Tus Recompensas!</h3>
                <ul>
                    <li><i class="fas fa-film"></i> <strong>50 Puntos: "Noche Cinematográfica a Tu Elección"</strong>
                        <p>Selecciona la película y los acompañamientos (snacks, bebidas); me encargaré de crear el ambiente perfecto para tu disfrute.</p>
                    </li>
                    <li><i class="fas fa-spa"></i> <strong>100 Puntos: "Sesión de Masaje Personalizada"</strong>
                        <p>Una sesión de masaje de 30 minutos, con aceites aromáticos y música relajante, brindada por mí con dedicación y profesionalismo.</p>
                    </li>
                    <li><i class="fas fa-utensils"></i> <strong>150 Puntos: "Experiencia Culinaria a Medida"</strong>
                        <p>Indica tu platillo favorito y lo prepararé con esmero, incluyendo entrada y postre, para una velada gastronómica íntima en casa.</p>
                    </li>
                    <li><i class="fas fa-broom"></i> <strong>200 Puntos: "Jornada de Liberación de Tareas"</strong>
                        <p>Asumiré todas las responsabilidades domésticas por un día completo, permitiéndote un descanso total o la dedicación exclusiva a tus pasatiempos.</p>
                    </li>
                    <li><i class="fas fa-hiking"></i> <strong>250 Puntos: "Aventura o Actividad Seleccionada por Ti"</strong>
                        <p>Planificaremos y realizaremos una actividad de tu elección (senderismo, visita cultural, evento deportivo, etc.). Yo gestionaré la logística y los costos asociados.</p>
                    </li>
                    <li><i class="fas fa-moon"></i> <strong>300 Puntos: "Velada de Pasión Exclusiva"</strong>
                        <p>Una noche dedicada íntegramente a la intimidad, la conexión profunda y el romance, en un ambiente cuidadosamente diseñado para la ocasión y sin interrupciones.</p>
                    </li>
                    <li><i class="fas fa-plane"></i> <strong>400 Puntos: "Escapada Romántica (Corta Duración)"</strong>
                        <p>Una noche en un destino cercano de tu agrado (playa, montaña, ciudad). Me encargaré de todos los detalles de reserva y planificación para tu máximo disfrute.</p>
                    </li>
                    <li><i class="fas fa-crown"></i> <strong>500 Puntos: "Cumplimiento de un Deseo Especial"</strong>
                        <p>Podrás solicitar un deseo personal (razonable y que contribuya positivamente a nuestra relación), abarcando desde un obsequio único hasta una experiencia largamente soñada.</p>
                    </li>
                </ul>
            </div>
        </section>

        <section>
            <h2>IV. Procedimiento de Registro y Monitoreo de Puntos</h2>
            <div class="info-block">
                <h3>Registro: Un Proceso Sencillo y Transparente</h3>
                <p>La administración de tus **AntoPuntos** será gestionada directamente por mí, **Antonieta Torrejon**, garantizando un seguimiento claro y justo de cada contribución. Valoraré y consideraré tu registro personal como referencia complementaria.</p>
                <ul>
                    <li><i class="fas fa-clipboard-check"></i> <strong>Registro Manual:</strong> Te sugiero utilizar una libreta dedicada o un documento digital para documentar la fecha, el gesto realizado y los puntos obtenidos.</li>
                    <li><i class="fas fa-mobile-alt"></i> <strong>Plataforma Digital (Próximamente):</strong> Anticipamos el lanzamiento de una aplicación móvil específica para facilitar el registro, monitoreo y canje de tus puntos, optimizando tu experiencia en el programa.</li>
                </ul>
                <p class="key-pillars">La **lealtad**, honestidad, confianza y el compromiso mutuo son pilares fundamentales para el éxito y la alegría de este programa.</p>
            </div>
        </section>

        <section class="enrollment-section">
            <h3>Proceso de Inscripción:</h3>
            <p>Para formalizar tu inscripción en el programa **AntoPuntos**, por favor, indícanos brevemente por qué deseas ser parte de esta exclusiva iniciativa.</p>
            <p>Posteriormente, solicita una entrevista personal y envía la frase **"Estoy de Acuerdo"** a mi número de contacto:</p>
            <span class="phone-number">+56996262764</span>
        </section>

        <footer>
            <p>Este Programa de Reconocimiento es una iniciativa seria y comprometida para nutrir y fortalecer nuestra relación día a día, construyendo un futuro lleno de momentos inolvidables.</p>
            <p>Con el mayor compromiso y afecto,</p>
            <p><strong>Antonieta Torrejon</strong></p>
            <p>&copy; 2025 AntoPuntos. Todos los derechos reservados. Programa de Fidelización Interna de Pareja.</p>
        </footer>
    </div>
</body>
</html>
