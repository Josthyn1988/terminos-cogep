<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculadora de Términos Procesales COGEP - Mejorada</title>
    
    <!-- PWA Meta Tags -->
    <meta name="theme-color" content="#1e3a8a">
    <meta name="mobile-web-app-capable" content="yes">
    <meta name="apple-mobile-web-app-capable" content="yes">
    <meta name="apple-mobile-web-app-status-bar-style" content="default">
    <meta name="apple-mobile-web-app-title" content="Calculadora COGEP">
    <meta name="description" content="Calculadora de términos procesales del COGEP con funcionalidades avanzadas">
    
    <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/css/all.min.css">
    
    <style>
        :root {
            --primary-blue: #1e3a8a;
            --secondary-blue: #3b82f6;
            --accent-blue: #60a5fa;
            --dark-gray: #1f2937;
            --light-gray: #f8fafc;
            --animation-duration: 0.3s;
        }
        
        /* Animaciones mejoradas */
        @keyframes slideInFromTop {
            from {
                opacity: 0;
                transform: translateY(-30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        @keyframes slideInFromBottom {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        @keyframes fadeIn {
            from {
                opacity: 0;
            }
            to {
                opacity: 1;
            }
        }
        
        @keyframes scaleIn {
            from {
                opacity: 0;
                transform: scale(0.95);
            }
            to {
                opacity: 1;
                transform: scale(1);
            }
        }
        
        @keyframes pulse {
            0%, 100% {
                transform: scale(1);
            }
            50% {
                transform: scale(1.05);
            }
        }
        
        .animate-slide-in-top {
            animation: slideInFromTop var(--animation-duration) ease-out;
        }
        
        .animate-slide-in-bottom {
            animation: slideInFromBottom var(--animation-duration) ease-out;
        }
        
        .animate-fade-in {
            animation: fadeIn var(--animation-duration) ease-in;
        }
        
        .animate-scale-in {
            animation: scaleIn var(--animation-duration) ease-out;
        }
        
        .animate-pulse {
            animation: pulse 2s cubic-bezier(0.4, 0, 0.6, 1) infinite;
        }
        
        .professional-gradient {
            background: linear-gradient(135deg, var(--primary-blue) 0%, var(--secondary-blue) 100%);
        }
        
        .shadow-professional {
            box-shadow: 0 4px 20px rgba(30, 58, 138, 0.12);
        }
        
        .text-primary-blue { color: var(--primary-blue); }
        .bg-primary-blue { background-color: var(--primary-blue); }
        .border-primary-blue { border-color: var(--primary-blue); }
        
        .result-card {
            background: linear-gradient(135deg, #f0f9ff 0%, #e0f2fe 100%);
            border-left: 4px solid var(--primary-blue);
        }
        
        .admin-panel {
            background: linear-gradient(135deg, #fef3e2 0%, #fde68a 100%);
            border-left: 4px solid #d97706;
        }
        
        .holiday-item {
            transition: all var(--animation-duration) ease;
        }
        
        .holiday-item:hover {
            background-color: var(--light-gray);
            transform: translateX(4px);
        }
        
        .btn-primary {
            background-color: var(--primary-blue);
            color: white;
            transition: all var(--animation-duration) ease;
        }
        
        .btn-primary:hover {
            background-color: var(--secondary-blue);
            transform: translateY(-2px);
            box-shadow: 0 4px 12px rgba(30, 58, 138, 0.3);
        }
        
        .btn-primary:active {
            transform: translateY(-1px);
        }
        
        .input-focus:focus {
            border-color: var(--secondary-blue);
            box-shadow: 0 0 0 3px rgba(59, 130, 246, 0.1);
            transform: scale(1.02);
            transition: all var(--animation-duration) ease;
        }

        /* Tooltips mejorados */
        .tooltip {
            position: relative;
            display: inline-block;
        }

        .tooltip .tooltiptext {
            visibility: hidden;
            width: 300px;
            background-color: #1f2937;
            color: #fff;
            text-align: left;
            border-radius: 6px;
            padding: 8px 12px;
            position: absolute;
            z-index: 1000;
            bottom: 125%;
            left: 50%;
            margin-left: -150px;
            opacity: 0;
            transition: opacity var(--animation-duration);
            font-size: 12px;
            line-height: 1.4;
        }

        .tooltip .tooltiptext::after {
            content: "";
            position: absolute;
            top: 100%;
            left: 50%;
            margin-left: -5px;
            border-width: 5px;
            border-style: solid;
            border-color: #1f2937 transparent transparent transparent;
        }

        .tooltip:hover .tooltiptext {
            visibility: visible;
            opacity: 1;
        }

        .legal-reference {
            background: linear-gradient(135deg, #fef7cd 0%, #fbbf24 20%);
            border: 1px solid #f59e0b;
            border-radius: 6px;
            padding: 8px 12px;
            margin: 8px 0;
            font-size: 13px;
            transition: all var(--animation-duration) ease;
        }

        .legal-reference:hover {
            transform: translateX(2px);
            box-shadow: 0 2px 8px rgba(245, 158, 11, 0.2);
        }

        /* Estilos para el calendario mejorado */
        .calendario-dia {
            width: 40px;
            height: 40px;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 6px;
            font-size: 14px;
            font-weight: 500;
            transition: all 0.2s ease;
            position: relative;
            cursor: pointer;
        }

        .dia-habil {
            background-color: #f8fafc;
            border: 1px solid #e2e8f0;
            color: #1f2937;
        }

        .dia-no-habil {
            background-color: #fee2e2;
            border: 1px solid #fca5a5;
            color: #991b1b;
        }

        .dia-inicio {
            background-color: var(--primary-blue) !important;
            color: white !important;
            font-weight: bold;
            box-shadow: 0 2px 8px rgba(30, 58, 138, 0.3);
            transform: scale(1.1);
        }

        .dia-vencimiento {
            background-color: #dc2626 !important;
            color: white !important;
            font-weight: bold;
            box-shadow: 0 2px 8px rgba(220, 38, 38, 0.3);
            transform: scale(1.1);
        }

        .dia-actual {
            background-color: #059669 !important;
            color: white !important;
            font-weight: bold;
            box-shadow: 0 2px 8px rgba(5, 150, 105, 0.3);
            transform: scale(1.05);
        }

        .dia-en-termino {
            background-color: #fef3c7;
            border: 1px solid #f59e0b;
            color: #92400e;
        }

        .calendario-mes {
            margin-bottom: 24px;
        }

        .calendario-header {
            background: linear-gradient(135deg, var(--primary-blue), var(--secondary-blue));
            color: white;
            padding: 12px;
            border-radius: 8px 8px 0 0;
            text-align: center;
            font-weight: bold;
            font-size: 16px;
        }

        .calendario-grid {
            display: grid;
            grid-template-columns: repeat(7, 1fr);
            gap: 4px;
            padding: 16px;
            background: white;
            border: 1px solid #e2e8f0;
            border-top: none;
            border-radius: 0 0 8px 8px;
        }

        .calendario-dia-nombre {
            text-align: center;
            font-weight: 600;
            color: #6b7280;
            padding: 8px 0;
            font-size: 12px;
            background-color: #f9fafb;
            border-radius: 4px;
        }

        .citacion-prensa-option {
            background: linear-gradient(135deg, #fff7ed 0%, #fed7aa 100%);
            border: 1px solid #fb923c;
            border-radius: 8px;
            padding: 16px;
            margin-top: 16px;
        }

        .leyenda-item {
            display: flex;
            align-items: center;
            gap: 8px;
            font-size: 13px;
        }

        .leyenda-cuadro {
            width: 24px;
            height: 24px;
            border-radius: 4px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            font-size: 12px;
        }

        /* Optimización móvil mejorada */
        @media (max-width: 768px) {
            .container {
                padding: 0.5rem;
            }
            
            .calendario-dia {
                width: 32px;
                height: 32px;
                font-size: 12px;
            }
            
            .calendario-grid {
                gap: 2px;
                padding: 12px;
            }
            
            .tooltip .tooltiptext {
                width: 250px;
                margin-left: -125px;
                font-size: 11px;
            }
            
            .professional-gradient .container {
                padding: 1rem;
            }
            
            .professional-gradient h1 {
                font-size: 1.5rem;
            }
            
            .grid.lg\\:grid-cols-3 {
                grid-template-columns: 1fr;
                gap: 1rem;
            }
            
            .grid.lg\\:grid-cols-2 {
                grid-template-columns: 1fr;
                gap: 1rem;
            }
            
            .btn-primary {
                padding: 0.75rem 1rem;
                font-size: 14px;
            }
            
            .space-y-4 > * + * {
                margin-top: 1rem;
            }
        }

        @media (max-width: 640px) {
            .calendario-dia {
                width: 28px;
                height: 28px;
                font-size: 11px;
            }
            
            .professional-gradient h1 {
                font-size: 1.25rem;
            }
            
            .professional-gradient p {
                font-size: 0.875rem;
            }
            
            .shadow-professional {
                box-shadow: 0 2px 10px rgba(30, 58, 138, 0.08);
            }
        }

        /* Estilos específicos para PDF */
        @media print {
            body { 
                font-size: 11px; 
                background: white !important;
            }
            .no-print { display: none !important; }
            .shadow-professional { box-shadow: none; }
            .professional-gradient { background: var(--primary-blue) !important; }
            .container { max-width: none; margin: 0; padding: 20px; }
            .calendario-mes { break-inside: avoid; }
            .grid { display: block; }
            .lg\\:grid-cols-3 > div:first-child { margin-bottom: 20px; }
            .lg\\:grid-cols-2 > div { margin-bottom: 20px; }
            .space-y-8 > * { margin-bottom: 15px !important; }
            .mt-8 { margin-top: 15px !important; }
            .py-8 { padding-top: 15px !important; padding-bottom: 15px !important; }
            .tooltip .tooltiptext { display: none; }
            .animate-slide-in-top,
            .animate-slide-in-bottom,
            .animate-fade-in,
            .animate-scale-in {
                animation: none;
            }
        }
    
        /* Estilos para modo oscuro */
        .dark-mode {
            background-color: #0f172a;
            color: #e5e7eb;
        }
        .dark-mode .bg-white {
            background-color: #1f2937;
            color: #e5e7eb;
        }
        .dark-mode .result-card {
            background: linear-gradient(135deg, #1e293b 0%, #374151 100%);
            border-left-color: var(--secondary-blue);
        }
        .dark-mode .admin-panel {
            background: linear-gradient(135deg, #4b5563 0%, #6b7280 100%);
            border-left-color: #f59e0b;
            color: #e5e7eb;
        }
        .dark-mode .bg-gray-50 { background-color: #1f2937; }
        .dark-mode .text-gray-700 { color: #d1d5db; }
        .dark-mode .text-gray-500 { color: #9ca3af; }
        .dark-mode input, .dark-mode select, .dark-mode textarea {
            background-color: #374151;
            color: #f9fafb;
            border-color: #4b5563;
        }
        .dark-mode .btn-primary {
            background-color: #2563eb;
            color: #f9fafb;
        }
        .dark-mode .btn-primary:hover {
            background-color: #3b82f6;
        }

        /* PWA Install Button */
        .install-button {
            position: fixed;
            bottom: 20px;
            right: 20px;
            z-index: 1000;
            display: none;
        }

        /* Loading spinner */
        .loading-spinner {
            border: 3px solid #f3f3f3;
            border-top: 3px solid var(--primary-blue);
            border-radius: 50%;
            width: 30px;
            height: 30px;
            animation: spin 1s linear infinite;
        }

        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        /* Notificación toast */
        .toast {
            position: fixed;
            top: 20px;
            right: 20px;
            background-color: #4ade80;
            color: white;
            padding: 12px 24px;
            border-radius: 8px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
            z-index: 1000;
            transform: translateX(100%);
            transition: transform var(--animation-duration) ease;
        }

        .toast.show {
            transform: translateX(0);
        }

        .toast.error {
            background-color: #ef4444;
        }

        /* Conexión offline */
        .offline-indicator {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            background-color: #f59e0b;
            color: white;
            text-align: center;
            padding: 8px;
            font-size: 14px;
            z-index: 1001;
            display: none;
        }
    </style>
</head>
<body class="bg-gray-50 min-h-screen">
    <!-- Indicador de conexión offline -->
    <div id="offlineIndicator" class="offline-indicator">
        <i class="fas fa-wifi-slash mr-2"></i>
        Modo sin conexión - Algunas funciones pueden estar limitadas
    </div>

    <!-- Header -->
    <header class="professional-gradient text-white shadow-lg animate-slide-in-top">
        <div class="container mx-auto px-6 py-4">
            <div class="flex items-center justify-between">
                <div class="flex items-center space-x-4">
                    <div class="bg-white p-3 rounded-full">
                        <i class="fas fa-balance-scale text-primary-blue text-2xl"></i>
                    </div>
                    <div>
                        <h1 class="text-2xl font-bold">Calculadora de Términos Procesales</h1>
                        <p class="text-blue-100">Consejo de la Judicatura - COGEP con Referencias Legales</p>
                    </div>
                </div>
                
                <div class="text-right flex items-center space-x-4">
                    <div>
                        <p class="text-sm opacity-90">Desarrollado por</p>
                        <p class="font-semibold">Ab. Josthyn Noboa</p>
                        <p class="text-xs text-blue-200">Secretario Judicial</p>
                    </div>
                    <button id="darkModeToggle" onclick="toggleDarkMode()" class="bg-white p-2 rounded-full text-primary-blue no-print transition-all duration-300 hover:scale-110" title="Alternar modo oscuro">
                        <i class="fas fa-moon"></i>
                    </button>
                </div>
            </div>
        </div>
    </header>

    <div class="container mx-auto px-6 py-8">
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-8">
            <!-- Datos del Proceso -->
            <div class="lg:col-span-2 animate-slide-in-bottom">
                <div class="bg-white rounded-lg shadow-professional p-6">
                    <h2 class="text-xl font-bold text-primary-blue mb-6 flex items-center">
                        <i class="fas fa-clipboard-list mr-3"></i>
                        Datos del Proceso
                    </h2>
                    
                    <div class="space-y-4">
                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-2">Tipo de Procedimiento:</label>
                            <select id="tipoTramite" class="w-full p-3 border border-gray-300 rounded-lg input-focus transition-all duration-300" onchange="mostrarReferenciaLegal()" aria-describedby="tipoTramiteError" aria-invalid="false">
                                <!-- Procedimientos principales -->
                                <optgroup label="Procedimientos Principales">
                                    <option value="ordinario" data-articulo="Art. 291">📋 Procedimiento Ordinario (30 días) - Art. 291 COGEP</option>
                                    <option value="sumario" data-articulo="Art. 333">⚡ Procedimiento Sumario (15 días) - Art. 333 COGEP</option>
                                    <option value="monitorio" data-articulo="Art. 358">💰 Procedimiento Monitorio (15 días) - Art. 358 COGEP</option>
                                    <option value="ejecutivo" data-articulo="Art. 351">⚖️ Procedimiento Ejecutivo (15 días) - Art. 351 COGEP</option>
                                </optgroup>

                                <!-- Términos de contestación específicos -->
                                <optgroup label="Términos de Contestación">
                                    <option value="contestacion_ordinario" data-articulo="Art. 291">📝 Contestación Ordinario (30 días) - Art. 291 COGEP</option>
                                    <option value="contestacion_sumario" data-articulo="Art. 333">📝 Contestación Sumario (15 días) - Art. 333 COGEP</option>
                                    <option value="contestacion_sumario_ninez" data-articulo="Art. 333">👶 Contestación Sumario Niñez/Adolescencia (10 días) - Art. 333 COGEP</option>
                                    <option value="contestacion_ejecutivo" data-articulo="Art. 351">📝 Contestación Ejecutivo (15 días) - Art. 351 COGEP</option>
                                </optgroup>

                                <!-- Audiencias -->
                                <optgroup label="Audiencias y Convocatorias">
                                    <option value="audiencia_preliminar" data-articulo="Art. 292">🎯 Audiencia Preliminar (10-20 días) - Art. 292 COGEP</option>
                                    <option value="audiencia_juicio" data-articulo="Art. 297">⚡ Audiencia de Juicio (máx. 30 días) - Art. 297 COGEP</option>
                                    <option value="audiencia_unica_sumario" data-articulo="Art. 333">🎯 Audiencia Única Sumario (máx. 30 días) - Art. 333 COGEP</option>
                                    <option value="audiencia_unica_sumario_ninez" data-articulo="Art. 333">👶 Audiencia Única Sumario Niñez (máx. 20 días) - Art. 333 COGEP</option>
                                    <option value="audiencia_ejecutivo" data-articulo="Art. 354">⚖️ Audiencia Única Ejecutivo (máx. 20 días) - Art. 354 COGEP</option>
                                </optgroup>

                                <!-- Recursos procesales -->
                                <optgroup label="Recursos Procesales">
                                    <option value="apelacion" data-articulo="Art. 257">📤 Recurso de Apelación (10 días) - Art. 257 COGEP</option>
                                    <option value="apelacion_ninez" data-articulo="Art. 257">👶 Apelación Niñez/Adolescencia (5 días) - Art. 257 COGEP</option>
                                    <option value="casacion" data-articulo="Art. 266">🏛️ Recurso de Casación (30 días) - Art. 266 COGEP</option>
                                    <option value="hecho" data-articulo="Art. 280">📋 Recurso de Hecho (3 días) - Art. 280 COGEP</option>
                                    <option value="aclaracion_ampliacion" data-articulo="Art. 274">❓ Aclaración/Ampliación (3 días) - Art. 274 COGEP</option>
                                </optgroup>

                                <!-- Procedimientos especiales -->
                                <optgroup label="Procedimientos Especiales">
                                    <option value="contencioso_administrativo_subjetiva" data-articulo="Art. 306.1">🏛️ Contencioso Administrativo Subjetiva (90 días) - Art. 306.1 COGEP</option>
                                    <option value="contencioso_administrativo_objetiva" data-articulo="Art. 306.2">🏛️ Contencioso Administrativo Objetiva (3 años) - Art. 306.2 COGEP</option>
                                    <option value="contencioso_tributario" data-articulo="Art. 306.5">💰 Contencioso Tributario (60 días) - Art. 306.5 COGEP</option>
                                    <option value="mandamiento_ejecucion" data-articulo="Art. 372">⚡ Mandamiento de Ejecución (5 días) - Art. 372 COGEP</option>
                                </optgroup>

                                <!-- Otros términos relevantes -->
                                <optgroup label="Otros Términos">
                                    <option value="abandono" data-articulo="Art. 245">⏰ Abandono del Proceso (6 meses) - Art. 245 COGEP</option>
                                    <option value="oposicion_concurso" data-articulo="Art. 425">💼 Oposición a Concurso (10 días) - Art. 425 COGEP</option>
                                    <option value="informe_auditor" data-articulo="Art. 420">📊 Informe de Auditor (10 días) - Art. 420 COGEP</option>
                                </optgroup>
                            </select>
                            <div id="referenciaLegalDiv" class="legal-reference hidden">
                                <i class="fas fa-book-open text-yellow-600 mr-2"></i>
                                <span id="referenciaLegalTexto"></span>
                            </div>
                            <p id="tipoTramiteError" class="text-xs text-red-600 mt-1 hidden" aria-live="assertive"></p>
                        </div>
                        
                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-2">Fecha de Inicio del Término:</label>
                            <input type="date" id="fechaInicio" class="w-full p-3 border border-gray-300 rounded-lg input-focus transition-all duration-300" aria-describedby="fechaInicioError" aria-invalid="false">
                            <p id="fechaInicioError" class="text-xs text-red-600 mt-1 hidden" aria-live="assertive"></p>
                        </div>

                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-2">Nombre del demandado:</label>
                            <input type="text" id="nombreDemandado" placeholder="Ingresa el nombre del demandado" class="w-full p-3 border border-gray-300 rounded-lg input-focus transition-all duration-300">
                        </div>
                        
                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-2">Tipo de Cálculo:</label>
                            <div class="flex space-x-4">
                                <label class="flex items-center tooltip">
                                    <input type="radio" name="tipoCalculo" value="habil" checked class="mr-2 text-primary-blue">
                                    <span class="text-sm">Días hábiles únicamente</span>
                                    <span class="tooltiptext">Excluye fines de semana, feriados y vacancias judiciales</span>
                                </label>
                                <label class="flex items-center tooltip">
                                    <input type="radio" name="tipoCalculo" value="continuo" class="mr-2 text-primary-blue">
                                    <span class="text-sm">Días continuos</span>
                                    <span class="tooltiptext">Incluye todos los días, solo aplicable en casos específicos como abandono</span>
                                </label>
                            </div>
                        </div>

                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-2">Región judicial para vacancia:</label>
                            <select id="regionVacanciaSelect" class="w-full p-3 border border-gray-300 rounded-lg input-focus transition-all duration-300">
                                <option value="sierra">Sierra y Amazonía (1-15 agosto)</option>
                                <option value="costa">Costa e Insular (17-31 marzo)</option>
                            </select>
                        </div>

                        <div class="citacion-prensa-option">
                            <label class="flex items-start cursor-pointer tooltip">
                                <input type="checkbox" id="citacionPrensa" class="mt-1 mr-3 text-orange-600">
                                <div>
                                    <span class="font-semibold text-orange-800">Agregar período adicional por Citación por Prensa</span>
                                    <p class="text-sm text-orange-700 mt-1">
                                        Añade 20 días adicionales al término. "Transcurridos veinte días desde la última publicación o transmisión del mensaje radial comenzará el término para contestar la demanda."
                                    </p>
                                </div>
                                <span class="tooltiptext">Según Art. 60 COGEP, aplicable cuando no se puede ubicar al demandado</span>
                            </label>
                        </div>
                        
                        <button onclick="calcularTermino()" class="w-full btn-primary py-3 px-6 rounded-lg font-semibold transition-all duration-300 flex items-center justify-center">
                            <i class="fas fa-calculator mr-2"></i>
                            Calcular Término
                        </button>
                    </div>
                </div>

                <!-- Panel Administrativo -->
                <div class="bg-white rounded-lg shadow-professional p-6 mt-8 no-print">
                    <h2 class="text-xl font-bold text-primary-blue mb-6 flex items-center">
                        <i class="fas fa-user-shield mr-3"></i>
                        Panel Administrativo
                    </h2>
                    
                    <div id="adminLogin" class="space-y-4">
                        <div>
                            <label class="block text-sm font-medium text-gray-700 mb-2">Acceso de Secretario:</label>
                            <input type="password" id="adminPassword" placeholder="Ingrese contraseña" class="w-full p-3 border border-gray-300 rounded-lg input-focus">
                        </div>
                        <button onclick="verificarAcceso()" class="btn-primary py-2 px-4 rounded-lg font-semibold">
                            <i class="fas fa-unlock mr-2"></i>
                            Acceder
                        </button>
                    </div>
                    
                    <div id="adminPanel" class="hidden space-y-4">
                        <div class="admin-panel rounded-lg p-4">
                            <h4 class="font-semibold text-orange-800 mb-3">Modificación de Fechas</h4>
                            <div class="space-y-3">
                                <div>
                                    <label class="block text-sm font-medium text-gray-700 mb-1">Nueva fecha de vencimiento:</label>
                                    <input type="date" id="nuevaFecha" class="w-full p-2 border border-gray-300 rounded input-focus">
                                </div>
                                <div>
                                    <label class="block text-sm font-medium text-gray-700 mb-1">Justificación del cambio:</label>
                                    <textarea id="justificacion" placeholder="Indique el motivo del cambio..." class="w-full p-2 border border-gray-300 rounded input-focus h-20"></textarea>
                                </div>
                                <button onclick="modificarFecha()" class="bg-orange-600 text-white py-2 px-4 rounded font-semibold hover:bg-orange-700 transition-all duration-300">
                                    <i class="fas fa-edit mr-2"></i>
                                    Aplicar Modificación
                                </button>
                            </div>
                        </div>
                        
                        <div id="historialCambios" class="mt-4">
                            <h4 class="font-semibold text-gray-800 mb-2">Historial de Modificaciones</h4>
                            <div id="listaHistorial" class="space-y-2 max-h-32 overflow-y-auto">
                                <p class="text-sm text-gray-500">No hay modificaciones registradas</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Resultados -->
            <div class="animate-scale-in">
                <div class="bg-white rounded-lg shadow-professional p-6">
                    <h2 class="text-xl font-bold text-primary-blue mb-6 flex items-center">
                        <i class="fas fa-chart-line mr-3"></i>
                        Resultados
                    </h2>
                    
                    <div id="resultado" class="space-y-4">
                        <div class="text-center text-gray-500 py-8">
                            <i class="fas fa-hourglass-half text-4xl mb-4 text-gray-400 animate-pulse"></i>
                            <p>Ingrese los datos y presione calcular para obtener los resultados</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <div class="grid grid-cols-1 lg:grid-cols-2 gap-8 mt-8">
            <!-- Días No Hábiles Considerados -->
            <div class="bg-white rounded-lg shadow-professional p-6 animate-fade-in">
                <h3 class="text-lg font-bold text-primary-blue mb-4 flex items-center">
                    <i class="fas fa-calendar-times mr-3 text-red-500"></i>
                    Días No Hábiles Considerados
                </h3>
                <div class="space-y-3">
                    <div class="flex items-center text-sm">
                        <i class="fas fa-times-circle text-red-500 mr-3"></i>
                        <span>Sábados y domingos</span>
                    </div>
                    <div class="flex items-center text-sm">
                        <i class="fas fa-times-circle text-red-500 mr-3"></i>
                        <span>Feriados nacionales</span>
                    </div>
                    <div id="vacanciaInfoList" class="space-y-1">
                    </div>
                </div>
            </div>

            <!-- Próximos Feriados -->
            <div class="bg-white rounded-lg shadow-professional p-6 animate-fade-in">
                <h3 class="text-lg font-bold text-primary-blue mb-4 flex items-center">
                    <i class="fas fa-calendar-alt mr-3 text-green-500"></i>
                    Próximos Feriados
                </h3>
                <div id="proximosFeriados" class="space-y-2 max-h-48 overflow-y-auto">
                </div>
            </div>
        </div>

        <!-- Referencias Normativas del COGEP Ampliadas -->
        <div class="bg-white rounded-lg shadow-professional p-6 mt-8 animate-slide-in-bottom">
            <h3 class="text-lg font-bold text-primary-blue mb-4 flex items-center">
                <i class="fas fa-book-open mr-3"></i>
                Referencias Normativas del COGEP
            </h3>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4 text-sm">
                <div class="bg-blue-50 p-4 rounded-lg border-l-4 border-blue-500 hover:shadow-lg transition-all duration-300">
                    <h4 class="font-semibold text-primary-blue mb-2">
                        <a href="https://www.telecomunicaciones.gob.ec/wp-content/uploads/2018/09/Codigo-Orgánico-General-de-Procesos.pdf" target="_blank" class="underline hover:text-blue-800">Art. 291 - Procedimiento Ordinario</a>
                    </h4>
                    <p class="text-gray-700">Contestación: 30 días desde la última citación</p>
                </div>
                <div class="bg-green-50 p-4 rounded-lg border-l-4 border-green-500 hover:shadow-lg transition-all duration-300">
                    <h4 class="font-semibold text-primary-blue mb-2">
                        <a href="https://www.telecomunicaciones.gob.ec/wp-content/uploads/2018/09/Codigo-Orgánico-General-de-Procesos.pdf" target="_blank" class="underline hover:text-blue-800">Art. 333 - Procedimiento Sumario</a>
                    </h4>
                    <p class="text-gray-700">Contestación: 15 días (10 días en niñez/adolescencia)</p>
                </div>
                <div class="bg-yellow-50 p-4 rounded-lg border-l-4 border-yellow-500 hover:shadow-lg transition-all duration-300">
                    <h4 class="font-semibold text-primary-blue mb-2">
                        <a href="https://www.telecomunicaciones.gob.ec/wp-content/uploads/2018/09/Codigo-Orgánico-General-de-Procesos.pdf" target="_blank" class="underline hover:text-blue-800">Art. 257 - Apelación</a>
                    </h4>
                    <p class="text-gray-700">10 días (5 días en niñez/adolescencia)</p>
                </div>
                <div class="bg-red-50 p-4 rounded-lg border-l-4 border-red-500 hover:shadow-lg transition-all duration-300">
                    <h4 class="font-semibold text-primary-blue mb-2">
                        <a href="https://www.telecomunicaciones.gob.ec/wp-content/uploads/2018/09/Codigo-Orgánico-General-de-Procesos.pdf" target="_blank" class="underline hover:text-blue-800">Art. 266 - Casación</a>
                    </h4>
                    <p class="text-gray-700">30 días posteriores a la ejecutoria</p>
                </div>
                <div class="bg-purple-50 p-4 rounded-lg border-l-4 border-purple-500 hover:shadow-lg transition-all duration-300">
                    <h4 class="font-semibold text-primary-blue mb-2">
                        <a href="https://www.telecomunicaciones.gob.ec/wp-content/uploads/2018/09/Codigo-Orgánico-General-de-Procesos.pdf" target="_blank" class="underline hover:text-blue-800">Art. 245 - Abandono</a>
                    </h4>
                    <p class="text-gray-700">6 meses desde la última providencia útil</p>
                </div>
                <div class="bg-orange-50 p-4 rounded-lg border-l-4 border-orange-500 hover:shadow-lg transition-all duration-300">
                    <h4 class="font-semibold text-primary-blue mb-2">
                        <a href="https://www.telecomunicaciones.gob.ec/wp-content/uploads/2018/09/Codigo-Orgánico-General-de-Procesos.pdf" target="_blank" class="underline hover:text-blue-800">Art. 306 - Contencioso</a>
                    </h4>
                    <p class="text-gray-700">Administrativo: 90 días / Tributario: 60 días</p>
                </div>
            </div>
        </div>

        <!-- Calendario del Periodo Calculado -->
        <div class="bg-white rounded-lg shadow-professional p-6 mt-8 animate-scale-in">
            <h3 class="text-lg font-bold text-primary-blue mb-4 flex items-center">
                <i class="fas fa-calendar mr-3"></i>
                Calendario del Período Calculado
                <button id="exportCalendarBtn" onclick="exportarEventoCalendario()" class="ml-auto btn-primary py-2 px-4 rounded-lg text-sm no-print hidden">
                    <i class="fas fa-calendar-plus mr-2"></i>
                    Exportar Evento
                </button>
            </h3>
            
            <div id="calendarioVisual" class="text-center text-gray-500 py-8">
                <i class="fas fa-calendar-week text-4xl mb-4 text-gray-400 animate-pulse"></i>
                <p>El calendario se mostrará después de realizar el cálculo</p>
            </div>

            <div id="leyendaCalendario" class="hidden mt-6">
                <h4 class="font-semibold text-gray-800 mb-3">Leyenda del Calendario:</h4>
                <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-5 gap-4">
                    <div class="leyenda-item">
                        <div class="leyenda-cuadro dia-habil">1</div>
                        <span>Día hábil</span>
                    </div>
                    <div class="leyenda-item">
                        <div class="leyenda-cuadro dia-no-habil">N</div>
                        <span>Día no hábil</span>
                    </div>
                    <div class="leyenda-item">
                        <div class="leyenda-cuadro dia-actual">H</div>
                        <span>Fecha actual</span>
                    </div>
                    <div class="leyenda-item">
                        <div class="leyenda-cuadro dia-inicio">I</div>
                        <span>Inicio término</span>
                    </div>
                    <div class="leyenda-item">
                        <div class="leyenda-cuadro dia-vencimiento">V</div>
                        <span>Vencimiento</span>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Footer -->
    <footer class="bg-gray-800 text-white py-6 mt-12">
        <div class="container mx-auto px-6 text-center">
            <p class="text-sm">
                Desarrollado por el <strong>Ab. Josthyn Noboa</strong> – Secretario Judicial
            </p>
            <p class="text-xs text-gray-400 mt-2">
                Actualizado con COGEP 2025 | Con Referencias Legales Específicas
            </p>
            <div class="flex justify-center space-x-4 mt-4">
                <i class="fas fa-gavel text-yellow-400"></i>
                <i class="fas fa-balance-scale text-yellow-400"></i>
                <i class="fas fa-university text-yellow-400"></i>
            </div>
        </div>
    </footer>

    <!-- PWA Install Button -->
    <button id="installButton" class="install-button btn-primary py-3 px-6 rounded-full shadow-lg">
        <i class="fas fa-download mr-2"></i>
        Instalar App
    </button>

    <script>
        // Definición completa de feriados nacionales por año
        const feriados = {
            2025: [
                {fecha: "2025-01-01", nombre: "Año Nuevo"},
                {fecha: "2025-03-03", nombre: "Carnaval (Lunes)"},
                {fecha: "2025-03-04", nombre: "Carnaval (Martes)"},
                {fecha: "2025-04-18", nombre: "Viernes Santo"},
                {fecha: "2025-05-02", nombre: "Día del Trabajo (trasladado)"},
                {fecha: "2025-05-23", nombre: "Batalla de Pichincha (trasladado)"},
                {fecha: "2025-08-11", nombre: "Primer Grito de Independencia (trasladado)"},
                {fecha: "2025-10-10", nombre: "Independencia de Guayaquil (trasladado)"},
                {fecha: "2025-11-04", nombre: "Día de los Difuntos (trasladado)"},
                {fecha: "2025-11-03", nombre: "Independencia de Cuenca"},
                {fecha: "2025-12-25", nombre: "Navidad"}
            ],
            2026: [
                {fecha: "2026-01-01", nombre: "Año Nuevo"},
                {fecha: "2026-02-16", nombre: "Carnaval (Lunes)"},
                {fecha: "2026-02-17", nombre: "Carnaval (Martes)"},
                {fecha: "2026-04-03", nombre: "Viernes Santo"},
                {fecha: "2026-05-01", nombre: "Día del Trabajo"},
                {fecha: "2026-05-24", nombre: "Batalla de Pichincha"},
                {fecha: "2026-08-10", nombre: "Primer Grito de Independencia"},
                {fecha: "2026-10-09", nombre: "Independencia de Guayaquil"},
                {fecha: "2026-11-02", nombre: "Día de los Difuntos"},
                {fecha: "2026-11-03", nombre: "Independencia de Cuenca"},
                {fecha: "2026-12-25", nombre: "Navidad"}
            ],
            2027: [
                {fecha: "2027-01-01", nombre: "Año Nuevo"},
                {fecha: "2027-02-08", nombre: "Carnaval (Lunes)"},
                {fecha: "2027-02-09", nombre: "Carnaval (Martes)"},
                {fecha: "2027-03-26", nombre: "Viernes Santo"},
                {fecha: "2027-05-01", nombre: "Día del Trabajo"},
                {fecha: "2027-05-24", nombre: "Batalla de Pichincha"},
                {fecha: "2027-08-10", nombre: "Primer Grito de Independencia"},
                {fecha: "2027-10-09", nombre: "Independencia de Guayaquil"},
                {fecha: "2027-11-02", nombre: "Día de los Difuntos"},
                {fecha: "2027-11-03", nombre: "Independencia de Cuenca"},
                {fecha: "2027-12-25", nombre: "Navidad"}
            ],
            2028: [
                {fecha: "2028-01-01", nombre: "Año Nuevo"},
                {fecha: "2028-02-28", nombre: "Carnaval (Lunes)"},
                {fecha: "2028-02-29", nombre: "Carnaval (Martes)"},
                {fecha: "2028-04-14", nombre: "Viernes Santo"},
                {fecha: "2028-05-01", nombre: "Día del Trabajo"},
                {fecha: "2028-05-24", nombre: "Batalla de Pichincha"},
                {fecha: "2028-08-10", nombre: "Primer Grito de Independencia"},
                {fecha: "2028-10-09", nombre: "Independencia de Guayaquil"},
                {fecha: "2028-11-02", nombre: "Día de los Difuntos"},
                {fecha: "2028-11-03", nombre: "Independencia de Cuenca"},
                {fecha: "2028-12-25", nombre: "Navidad"}
            ]
        };

        // Períodos de vacancia judicial
        const vacanciasGenerales = [
            {start: '-12-23', end: '-12-31', nombre: 'Receso de Fin de Año'},
            {start: '-01-01', end: '-01-06', nombre: 'Receso de Año Nuevo'}
        ];

        const vacanciasRegional = {
            sierra: [ { start: '-08-01', end: '-08-15', nombre: 'Vacancia Judicial Sierra y Amazonía' } ],
            costa:  [ { start: '-03-17', end: '-03-31', nombre: 'Vacancia Judicial Costa e Insular' } ]
        };

        let regionVacancia = 'sierra';

        // Configuraciones mejoradas con referencias legales específicas
        const configuracionesCOGEP = {
            // Procedimientos principales
            'ordinario': {
                dias: 30, 
                nombre: 'Procedimiento Ordinario - Contestación',
                articulo: 'Art. 291',
                referencia: 'La o el demandado tendrá treinta días para presentar su contestación a la demanda. Este término se contará desde que se practicó la última citación.',
                tipoCalculo: 'habil'
            },
            'sumario': {
                dias: 15, 
                nombre: 'Procedimiento Sumario - Contestación',
                articulo: 'Art. 333',
                referencia: 'Para contestar la demanda y la reconvención se tendrá un término de quince días.',
                tipoCalculo: 'habil'
            },
            'monitorio': {
                dias: 15, 
                nombre: 'Procedimiento Monitorio - Pago',
                articulo: 'Art. 358',
                referencia: 'La o el juzgador, una vez que declare admisible la demanda, concederá el término de quince días para el pago.',
                tipoCalculo: 'habil'
            },
            'ejecutivo': {
                dias: 15, 
                nombre: 'Procedimiento Ejecutivo - Contestación',
                articulo: 'Art. 351',
                referencia: 'El demandado contestará la demanda en el término de quince días.',
                tipoCalculo: 'habil'
            },
            'contestacion_ordinario': {
                dias: 30, 
                nombre: 'Contestación en Procedimiento Ordinario',
                articulo: 'Art. 291',
                referencia: 'Término para contestar demanda en procedimiento ordinario: treinta días desde la última citación.',
                tipoCalculo: 'habil'
            },
            'contestacion_sumario': {
                dias: 15, 
                nombre: 'Contestación en Procedimiento Sumario',
                articulo: 'Art. 333',
                referencia: 'Para contestar la demanda se tendrá un término de quince días.',
                tipoCalculo: 'habil'
            },
            'contestacion_sumario_ninez': {
                dias: 10, 
                nombre: 'Contestación Sumario - Niñez y Adolescencia',
                articulo: 'Art. 333',
                referencia: 'En materia de niñez y adolescencia el término será de diez días.',
                tipoCalculo: 'habil'
            },
            'contestacion_ejecutivo': {
                dias: 15, 
                nombre: 'Contestación en Procedimiento Ejecutivo',
                articulo: 'Art. 351',
                referencia: 'El demandado contestará la demanda en el término de quince días.',
                tipoCalculo: 'habil'
            },
            'audiencia_preliminar': {
                dias: 20, 
                nombre: 'Audiencia Preliminar (máximo)',
                articulo: 'Art. 292',
                referencia: 'La audiencia preliminar deberá realizarse en un término no menor a diez ni mayor a veinte días.',
                tipoCalculo: 'habil'
            },
            'audiencia_juicio': {
                dias: 30, 
                nombre: 'Audiencia de Juicio (máximo)',
                articulo: 'Art. 297',
                referencia: 'La audiencia de juicio se realizará en el término máximo de treinta días contados a partir de la culminación de la audiencia preliminar.',
                tipoCalculo: 'habil'
            },
            'audiencia_unica_sumario': {
                dias: 30, 
                nombre: 'Audiencia Única en Sumario (máximo)',
                articulo: 'Art. 333',
                referencia: 'La audiencia única se realizará en el término máximo de treinta días a partir de la contestación a la demanda.',
                tipoCalculo: 'habil'
            },
            'audiencia_unica_sumario_ninez': {
                dias: 20, 
                nombre: 'Audiencia Única Sumario - Niñez (máximo)',
                articulo: 'Art. 333',
                referencia: 'En materia de niñez y adolescencia, la audiencia única se realizará en el término máximo de veinte días.',
                tipoCalculo: 'habil'
            },
            'audiencia_ejecutivo': {
                dias: 20, 
                nombre: 'Audiencia Única en Ejecutivo (máximo)',
                articulo: 'Art. 354',
                referencia: 'La audiencia única deberá realizarse en el término máximo de veinte días contados a partir de la fecha en que concluyó el término.',
                tipoCalculo: 'habil'
            },
            'apelacion': {
                dias: 10, 
                nombre: 'Recurso de Apelación',
                articulo: 'Art. 257',
                referencia: 'El recurso de apelación se presentará por escrito dentro del término de diez días contados a partir de la notificación.',
                tipoCalculo: 'habil'
            },
            'apelacion_ninez': {
                dias: 5, 
                nombre: 'Apelación - Niñez y Adolescencia',
                articulo: 'Art. 257',
                referencia: 'En materia de la niñez y adolescencia, el término será de cinco días.',
                tipoCalculo: 'habil'
            },
            'casacion': {
                dias: 30, 
                nombre: 'Recurso de Casación',
                articulo: 'Art. 266',
                referencia: 'El recurso de casación se interpondrá dentro del término de treinta días posteriores a la ejecutoria del auto o sentencia.',
                tipoCalculo: 'habil'
            },
            'hecho': {
                dias: 3, 
                nombre: 'Recurso de Hecho',
                articulo: 'Art. 280',
                referencia: 'Dentro del término de tres días siguientes al de la notificación de la providencia denegatoria.',
                tipoCalculo: 'habil'
            },
            'aclaracion_ampliacion': {
                dias: 3, 
                nombre: 'Aclaración o Ampliación',
                articulo: 'Art. 274',
                referencia: 'La petición de aclaración o ampliación se solicitará dentro de tres días de notificada la providencia.',
                tipoCalculo: 'habil'
            },
            'contencioso_administrativo_subjetiva': {
                dias: 90, 
                nombre: 'Contencioso Administrativo - Acción Subjetiva',
                articulo: 'Art. 306.1',
                referencia: 'En los casos en que se interponga una acción subjetiva, el término será de noventa días.',
                tipoCalculo: 'habil'
            },
            'contencioso_administrativo_objetiva': {
                dias: 1095, 
                nombre: 'Contencioso Administrativo - Acción Objetiva',
                articulo: 'Art. 306.2',
                referencia: 'En los casos de acción objetiva o de anulación por exceso de poder, el plazo será de tres años.',
                tipoCalculo: 'continuo'
            },
            'contencioso_tributario': {
                dias: 60, 
                nombre: 'Contencioso Tributario',
                articulo: 'Art. 306.5',
                referencia: 'En las acciones contencioso tributarias, el término para demandar será de sesenta días.',
                tipoCalculo: 'habil'
            },
            'mandamiento_ejecucion': {
                dias: 5, 
                nombre: 'Mandamiento de Ejecución',
                articulo: 'Art. 372',
                referencia: 'El mandamiento de ejecución deberá cumplirse en el término de cinco días.',
                tipoCalculo: 'habil'
            },
            'abandono': {
                dias: 180, 
                nombre: 'Abandono del Proceso',
                articulo: 'Art. 245',
                referencia: 'Seis meses desde la última providencia útil, según Art. 33 del Código Civil (días continuos).',
                tipoCalculo: 'continuo'
            },
            'oposicion_concurso': {
                dias: 10, 
                nombre: 'Oposición a Concurso',
                articulo: 'Art. 425',
                referencia: 'Los acreedores podrán formular oposición al concurso dentro del término de diez días.',
                tipoCalculo: 'habil'
            },
            'informe_auditor': {
                dias: 10, 
                nombre: 'Informe de Auditor',
                articulo: 'Art. 420',
                referencia: 'El informe del auditor debe ser presentado en el término máximo de diez días.',
                tipoCalculo: 'habil'
            }
        };

        // Variables globales
        let historialModificaciones = [];
        let fechaOriginalCalculada = null;
        let fechaModificada = null;
        let datosUltimoCalculo = null;
        let deferredPrompt;

        // PWA Service Worker Registration
        if ('serviceWorker' in navigator) {
            navigator.serviceWorker.register(createServiceWorker())
                .then(registration => {
                    console.log('Service Worker registrado');
                    showToast('Aplicación lista para usar offline', 'success');
                })
                .catch(error => {
                    console.log('Error al registrar Service Worker:', error);
                });
        }

        function createServiceWorker() {
            const swCode = `
                const CACHE_NAME = 'cogep-calculator-v1';
                const urlsToCache = [
                    '/',
                    'https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css',
                    'https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/css/all.min.css'
                ];

                self.addEventListener('install', event => {
                    event.waitUntil(
                        caches.open(CACHE_NAME)
                            .then(cache => cache.addAll(urlsToCache))
                    );
                });

                self.addEventListener('fetch', event => {
                    event.respondWith(
                        caches.match(event.request)
                            .then(response => {
                                return response || fetch(event.request);
                            })
                    );
                });
            `;
            
            const blob = new Blob([swCode], { type: 'application/javascript' });
            return URL.createObjectURL(blob);
        }

        // PWA Install Prompt
        window.addEventListener('beforeinstallprompt', (e) => {
            e.preventDefault();
            deferredPrompt = e;
            document.getElementById('installButton').style.display = 'block';
        });

        document.getElementById('installButton').addEventListener('click', async () => {
            if (deferredPrompt) {
                deferredPrompt.prompt();
                const { outcome } = await deferredPrompt.userChoice;
                if (outcome === 'accepted') {
                    showToast('Aplicación instalada correctamente', 'success');
                    document.getElementById('installButton').style.display = 'none';
                }
                deferredPrompt = null;
            }
        });

        // Detección de conexión offline/online
        window.addEventListener('online', () => {
            document.getElementById('offlineIndicator').style.display = 'none';
            showToast('Conexión restaurada', 'success');
        });

        window.addEventListener('offline', () => {
            document.getElementById('offlineIndicator').style.display = 'block';
            showToast('Modo sin conexión activado', 'warning');
        });

        function showToast(message, type = 'success') {
            const toast = document.createElement('div');
            toast.className = `toast ${type === 'error' ? 'error' : ''}`;
            toast.innerHTML = `
                <i class="fas fa-${type === 'error' ? 'exclamation-triangle' : type === 'warning' ? 'exclamation-circle' : 'check-circle'} mr-2"></i>
                ${message}
            `;
            
            document.body.appendChild(toast);
            
            setTimeout(() => {
                toast.classList.add('show');
            }, 100);
            
            setTimeout(() => {
                toast.classList.remove('show');
                setTimeout(() => {
                    document.body.removeChild(toast);
                }, 300);
            }, 3000);
        }

        function actualizarVacanciaInfo() {
            const contenedor = document.getElementById('vacanciaInfoList');
            if (!contenedor) return;
            
            contenedor.innerHTML = '';
            
            // Receso general
            const recesoDiv = document.createElement('div');
            recesoDiv.className = 'flex items-center text-sm';
            recesoDiv.innerHTML = '<i class="fas fa-times-circle text-red-500 mr-3"></i><span>Receso de fin de año (23 dic - 6 ene)</span>';
            contenedor.appendChild(recesoDiv);
            
            // Vacancia regional
            const regionalDiv = document.createElement('div');
            regionalDiv.className = 'flex items-center text-sm';
            let textoVacancia = regionVacancia === 'costa' ? 
                'Vacancia judicial Costa e Insular (17-31 marzo)' : 
                'Vacancia judicial Sierra y Amazonía (1-15 agosto)';
            regionalDiv.innerHTML = '<i class="fas fa-times-circle text-red-500 mr-3"></i><span>' + textoVacancia + '</span>';
            contenedor.appendChild(regionalDiv);
        }

        function mostrarReferenciaLegal() {
            const tipoTramite = document.getElementById('tipoTramite').value;
            const config = configuracionesCOGEP[tipoTramite];
            const divReferencia = document.getElementById('referenciaLegalDiv');
            const textoReferencia = document.getElementById('referenciaLegalTexto');
            
            if (config && config.referencia) {
                textoReferencia.innerHTML = `<strong>${config.articulo}:</strong> ${config.referencia}`;
                divReferencia.classList.remove('hidden');
                setTimeout(() => {
                    divReferencia.classList.add('animate-fade-in');
                }, 10);
            } else {
                divReferencia.classList.add('hidden');
            }
        }

        function esFeriado(date) {
            const año = date.getFullYear();
            const fechaStr = date.toISOString().slice(0, 10);
            return feriados[año]?.some(f => f.fecha === fechaStr);
        }

        function enVacanciaJudicial(date) {
            const mes = ("0" + (date.getMonth() + 1)).slice(-2);
            const dia = ("0" + date.getDate()).slice(-2);
            const fechaTag = `-${mes}-${dia}`;
            
            const enGeneral = vacanciasGenerales.some(periodo => fechaTag >= periodo.start && fechaTag <= periodo.end);
            if (enGeneral) return true;
            
            const listaRegional = vacanciasRegional[regionVacancia] || [];
            return listaRegional.some(periodo => fechaTag >= periodo.start && fechaTag <= periodo.end);
        }

        function esFinDeSemana(date) {
            const dia = date.getDay();
            return dia === 0 || dia === 6;
        }

        function esDiaHabil(date) {
            return !esFinDeSemana(date) && !esFeriado(date) && !enVacanciaJudicial(date);
        }

        function formatearFecha(date) {
            const opciones = { 
                weekday: 'long', 
                year: 'numeric', 
                month: 'long', 
                day: 'numeric' 
            };
            return date.toLocaleDateString('es-EC', opciones);
        }

        function calcularTermino() {
            // Mostrar indicador de carga
            const botonCalcular = document.querySelector('button[onclick="calcularTermino()"]');
            const textoOriginal = botonCalcular.innerHTML;
            botonCalcular.innerHTML = '<div class="loading-spinner mx-auto"></div>';
            botonCalcular.disabled = true;
            
            setTimeout(() => {
                realizarCalculo();
                botonCalcular.innerHTML = textoOriginal;
                botonCalcular.disabled = false;
            }, 500);
        }

        function realizarCalculo() {
            // Referencias a los campos y mensajes de error
            const fechaInicioInput = document.getElementById('fechaInicio');
            const tipoTramiteSelect = document.getElementById('tipoTramite');
            const fechaInicioError = document.getElementById('fechaInicioError');
            const tipoTramiteError = document.getElementById('tipoTramiteError');

            // Limpiar mensajes de error anteriores
            if (fechaInicioError) {
                fechaInicioError.textContent = '';
                fechaInicioError.classList.add('hidden');
            }
            if (fechaInicioInput) {
                fechaInicioInput.setAttribute('aria-invalid', 'false');
            }
            if (tipoTramiteError) {
                tipoTramiteError.textContent = '';
                tipoTramiteError.classList.add('hidden');
            }
            if (tipoTramiteSelect) {
                tipoTramiteSelect.setAttribute('aria-invalid', 'false');
            }

            const fechaInicioStr = fechaInicioInput ? fechaInicioInput.value : '';
            if (!fechaInicioStr) {
                // Mostrar mensaje de error específico y marcar como inválido
                if (fechaInicioError) {
                    fechaInicioError.textContent = 'Seleccione una fecha de inicio válida.';
                    fechaInicioError.classList.remove('hidden');
                }
                if (fechaInicioInput) {
                    fechaInicioInput.setAttribute('aria-invalid', 'true');
                }
                showToast('Por favor, seleccione una fecha de inicio', 'error');
                return;
            }

            const fechaInicio = new Date(fechaInicioStr + 'T00:00:00');
            const tipoTramite = tipoTramiteSelect ? tipoTramiteSelect.value : '';
            const tipoCalculo = document.querySelector('input[name="tipoCalculo"]:checked').value;
            const citacionPrensa = document.getElementById('citacionPrensa').checked;

            const config = configuracionesCOGEP[tipoTramite];
            if (!config) {
                // Mostrar mensaje de error específico y marcar como inválido
                if (tipoTramiteError) {
                    tipoTramiteError.textContent = 'Seleccione un tipo de trámite válido.';
                    tipoTramiteError.classList.remove('hidden');
                }
                if (tipoTramiteSelect) {
                    tipoTramiteSelect.setAttribute('aria-invalid', 'true');
                }
                showToast('Por favor, seleccione un tipo de trámite', 'error');
                return;
            }

            let diasTotal = config.dias;
            let nombreCompleto = config.nombre;
            
            if (citacionPrensa) {
                diasTotal += 20;
                nombreCompleto += ' + Citación por Prensa (20 días)';
            }

            let fechaActual = new Date(fechaInicio);
            let diasContados = 0;
            let diasTranscurridos = 0;
            let diasNoHabiles = 0;

            const calculoEfectivo = config.tipoCalculo === 'continuo' ? 'continuo' : tipoCalculo;

            while (diasContados < diasTotal) {
                fechaActual.setDate(fechaActual.getDate() + 1);
                diasTranscurridos++;

                if (calculoEfectivo === 'habil') {
                    if (esDiaHabil(fechaActual)) {
                        diasContados++;
                    } else {
                        diasNoHabiles++;
                    }
                } else {
                    diasContados++;
                }
            }

            const fechaVencimiento = new Date(fechaActual);
            fechaOriginalCalculada = new Date(fechaVencimiento);
            
            const hoy = new Date();
            hoy.setHours(0, 0, 0, 0);
            fechaVencimiento.setHours(0, 0, 0, 0);

            const estaVencido = fechaVencimiento < hoy;
            const diasRestantes = Math.ceil((fechaVencimiento - hoy) / (1000 * 60 * 60 * 24));

            datosUltimoCalculo = {
                fechaInicio,
                fechaVencimiento: fechaModificada || fechaVencimiento,
                fechaOriginal: fechaOriginalCalculada,
                diasTermino: diasTotal,
                diasTranscurridos,
                diasNoHabiles,
                estaVencido,
                diasRestantes,
                tipoTramite: nombreCompleto,
                tipoCodigo: tipoTramite,
                config,
                calculoEfectivo,
                citacionPrensa
            };

            mostrarResultado(datosUltimoCalculo);
            mostrarCalendarioMejorado(fechaInicio, fechaModificada || fechaVencimiento);
            
            // Mostrar botón de exportar calendario
            document.getElementById('exportCalendarBtn').classList.remove('hidden');
            
            showToast('Cálculo completado correctamente', 'success');
        }

        function mostrarResultado(datos) {
            const fechaFinal = fechaModificada || datos.fechaVencimiento;
            const hoy = new Date();
            hoy.setHours(0, 0, 0, 0);
            fechaFinal.setHours(0, 0, 0, 0);
            
            const estaVencidoFinal = fechaFinal < hoy;
            const diasRestantesFinal = Math.ceil((fechaFinal - hoy) / (1000 * 60 * 60 * 24));

            const estado = estaVencidoFinal ? 
                '<div class="bg-red-50 border border-red-200 rounded-lg p-4 animate-scale-in"><div class="flex items-center"><i class="fas fa-exclamation-triangle text-red-500 mr-2"></i><span class="font-semibold text-red-700">TÉRMINO VENCIDO</span></div></div>' :
                '<div class="bg-green-50 border border-green-200 rounded-lg p-4 animate-scale-in"><div class="flex items-center"><i class="fas fa-check-circle text-green-500 mr-2"></i><span class="font-semibold text-green-700">TÉRMINO VIGENTE</span></div></div>';

            let infoEspecial = '';
            if (datos.config.tipoCalculo === 'continuo') {
                infoEspecial = '<div class="bg-orange-50 border border-orange-200 rounded-lg p-3 mt-2 animate-fade-in"><div class="flex items-center text-sm"><i class="fas fa-info-circle text-orange-500 mr-2"></i><span class="text-orange-700">Cálculo en días continuos según normativa</span></div></div>';
            }

            if (datos.citacionPrensa) {
                infoEspecial += '<div class="bg-blue-50 border border-blue-200 rounded-lg p-3 mt-2 animate-fade-in"><div class="flex items-center text-sm"><i class="fas fa-newspaper text-blue-500 mr-2"></i><span class="text-blue-700">Incluye 20 días adicionales por Citación por Prensa</span></div></div>';
            }

            // Referencia legal específica
            if (datos.config.articulo && datos.config.referencia) {
                infoEspecial += `<div class="bg-yellow-50 border border-yellow-200 rounded-lg p-3 mt-2 animate-fade-in">
                    <div class="flex items-center text-sm">
                        <i class="fas fa-book-open text-yellow-600 mr-2"></i>
                        <span class="text-yellow-800 font-medium">${datos.config.articulo} COGEP</span>
                    </div>
                    <p class="text-xs text-yellow-700 mt-1">${datos.config.referencia}</p>
                </div>`;
            }

            let modificacionInfo = '';
            if (fechaModificada) {
                modificacionInfo = `
                    <div class="bg-purple-50 border border-purple-200 rounded-lg p-3 mt-2 animate-fade-in">
                        <div class="flex items-center text-sm">
                            <i class="fas fa-edit text-purple-600 mr-2"></i>
                            <span class="text-purple-800 font-medium">Fecha modificada por secretario</span>
                        </div>
                        <p class="text-xs text-purple-700 mt-1">Original: ${formatearFecha(datos.fechaOriginal)}</p>
                    </div>
                `;
            }

            document.getElementById('resultado').innerHTML = `
                ${estado}
                ${infoEspecial}
                ${modificacionInfo}
                <div class="result-card rounded-lg p-4 mt-4 animate-slide-in-bottom">
                    <h4 class="font-bold text-primary-blue mb-3">Fecha de vencimiento:</h4>
                    <p class="text-lg font-semibold">${formatearFecha(fechaFinal)}</p>
                    <p class="text-sm text-gray-600 mt-1">${fechaFinal.toLocaleDateString('es-EC')}</p>
                </div>
                <div class="space-y-2 mt-4 animate-fade-in">
                    <div class="flex justify-between py-2 border-b border-gray-200">
                        <span class="text-sm font-medium">Procedimiento:</span>
                        <span class="text-sm">${datos.tipoTramite}</span>
                    </div>
                    <div class="flex justify-between py-2 border-b border-gray-200">
                        <span class="text-sm font-medium">Base legal:</span>
                        <span class="text-sm">${datos.config.articulo} COGEP</span>
                    </div>
                    <div class="flex justify-between py-2 border-b border-gray-200">
                        <span class="text-sm font-medium">Días del término:</span>
                        <span class="text-sm">${datos.diasTermino} ${datos.config.tipoCalculo === 'continuo' ? 'días continuos' : 'días'}</span>
                    </div>
                    <div class="flex justify-between py-2 border-b border-gray-200">
                        <span class="text-sm font-medium">Días transcurridos:</span>
                        <span class="text-sm">${datos.diasTranscurridos} días</span>
                    </div>
                    <div class="flex justify-between py-2 border-b border-gray-200">
                        <span class="text-sm font-medium">Días no hábiles:</span>
                        <span class="text-sm">${datos.diasNoHabiles} días</span>
                    </div>
                    <div class="flex justify-between py-2">
                        <span class="text-sm font-medium">Estado:</span>
                        <span class="text-sm ${estaVencidoFinal ? 'text-red-600' : 'text-green-600'}">
                            ${estaVencidoFinal ? 
                                `Vencido hace ${Math.abs(diasRestantesFinal)} días` : 
                                `Vigente por ${diasRestantesFinal} días más`}
                        </span>
                    </div>
                </div>
            `;

            // Añadir sección de notas y razón automática
            const contenedorResultado = document.getElementById('resultado');
            const extraSection = document.createElement('div');
            extraSection.classList.add('mt-4', 'animate-slide-in-bottom');
            extraSection.innerHTML = `
                <div>
                    <h4 class="font-bold text-primary-blue mb-2">Agregar Nota:</h4>
                    <textarea id="noteInput" class="w-full p-2 border border-gray-300 rounded input-focus h-20" placeholder="Escriba aquí sus notas adicionales..."></textarea>
                    <button onclick="guardarNota()" class="mt-2 btn-primary py-2 px-4 rounded-lg no-print transition-all duration-300">
                        <i class="fas fa-save mr-2"></i>Guardar Nota
                    </button>
                    <div id="notaGuardada" class="text-xs text-green-600 mt-2"></div>
                </div>
                <div class="mt-4">
                    <h4 class="font-bold text-primary-blue mb-2">Razón automática:</h4>
                    <textarea id="razonTexto" class="w-full p-2 border border-gray-300 rounded input-focus h-32" readonly></textarea>
                    <div class="flex gap-2 mt-2">
                        <button onclick="copiarRazon()" class="bg-gray-600 text-white py-2 px-4 rounded-lg font-semibold no-print transition-all duration-300 hover:bg-gray-700">
                            <i class="fas fa-copy mr-2"></i>Copiar Razón
                        </button>
                        <button onclick="window.print()" class="bg-gray-300 text-gray-800 py-2 px-4 rounded-lg font-semibold no-print transition-all duration-300 hover:bg-gray-400">
                            <i class="fas fa-file-pdf mr-2"></i>Exportar a PDF
                        </button>
                    </div>
                </div>
            `;
            contenedorResultado.appendChild(extraSection);
            
            // Generar razón automática
            const razonElem = document.getElementById('razonTexto');
            if (razonElem) {
                razonElem.value = generarRazon(datos);
            }
        }

        function mostrarCalendarioMejorado(fechaInicio, fechaFin) {
            const hoy = new Date();
            hoy.setHours(0, 0, 0, 0);
            fechaInicio.setHours(0, 0, 0, 0);
            fechaFin.setHours(0, 0, 0, 0);

            const mesInicio = new Date(fechaInicio);
            mesInicio.setDate(1);
            const mesFin = new Date(fechaFin);
            mesFin.setDate(1);

            let calendarioHTML = '';
            let fechaActual = new Date(mesInicio);

            while (fechaActual <= mesFin) {
                calendarioHTML += generarCalendarioMes(fechaActual, fechaInicio, fechaFin, hoy);
                fechaActual.setMonth(fechaActual.getMonth() + 1);
            }

            const calendarioVisual = document.getElementById('calendarioVisual');
            calendarioVisual.innerHTML = calendarioHTML;
            calendarioVisual.classList.add('animate-fade-in');
            document.getElementById('leyendaCalendario').classList.remove('hidden');
        }

        function generarCalendarioMes(fecha, fechaInicio, fechaFin, hoy) {
            const año = fecha.getFullYear();
            const mes = fecha.getMonth();
            const nombreMes = fecha.toLocaleDateString('es-EC', { month: 'long', year: 'numeric' });
            
            const primerDia = new Date(año, mes, 1);
            const ultimoDia = new Date(año, mes + 1, 0);
            const diaInicioSemana = primerDia.getDay();

            let html = `
                <div class="calendario-mes animate-scale-in">
                    <div class="calendario-header">
                        ${nombreMes.charAt(0).toUpperCase() + nombreMes.slice(1)}
                    </div>
                    <div class="calendario-grid">
                        <div class="calendario-dia-nombre">Dom</div>
                        <div class="calendario-dia-nombre">Lun</div>
                        <div class="calendario-dia-nombre">Mar</div>
                        <div class="calendario-dia-nombre">Mié</div>
                        <div class="calendario-dia-nombre">Jue</div>
                        <div class="calendario-dia-nombre">Vie</div>
                        <div class="calendario-dia-nombre">Sáb</div>
            `;

            for (let i = 0; i < diaInicioSemana; i++) {
                html += '<div class="calendario-dia"></div>';
            }

            for (let dia = 1; dia <= ultimoDia.getDate(); dia++) {
                const fechaDia = new Date(año, mes, dia);
                let clases = 'calendario-dia ';
                let contenido = dia;

                if (fechaDia.toDateString() === hoy.toDateString()) {
                    clases += 'dia-actual';
                    contenido = 'H';
                } else if (fechaDia.toDateString() === fechaInicio.toDateString()) {
                    clases += 'dia-inicio';
                    contenido = 'I';
                } else if (fechaDia.toDateString() === fechaFin.toDateString()) {
                    clases += 'dia-vencimiento';
                    contenido = 'V';
                } else if (fechaDia >= fechaInicio && fechaDia <= fechaFin) {
                    if (esDiaHabil(fechaDia)) {
                        clases += 'dia-en-termino';
                    } else {
                        clases += 'dia-no-habil';
                    }
                } else if (esDiaHabil(fechaDia)) {
                    clases += 'dia-habil';
                } else {
                    clases += 'dia-no-habil';
                }

                html += `<div class="${clases}" title="${obtenerTituloFecha(fechaDia, fechaInicio, fechaFin, hoy)}" aria-label="${obtenerTituloFecha(fechaDia, fechaInicio, fechaFin, hoy)}">${contenido}</div>`;
            }

            html += '</div></div>';
            return html;
        }

        function obtenerTituloFecha(fecha, fechaInicio, fechaFin, hoy) {
            let titulo = formatearFecha(fecha);
            
            if (fecha.toDateString() === hoy.toDateString()) {
                titulo += ' - Fecha actual';
            } else if (fecha.toDateString() === fechaInicio.toDateString()) {
                titulo += ' - Inicio del término';
            } else if (fecha.toDateString() === fechaFin.toDateString()) {
                titulo += ' - Fecha de vencimiento';
            } else if (!esDiaHabil(fecha)) {
                if (esFinDeSemana(fecha)) {
                    titulo += ' - Fin de semana';
                } else if (esFeriado(fecha)) {
                    const feriado = feriados[fecha.getFullYear()]?.find(f => f.fecha === fecha.toISOString().slice(0, 10));
                    titulo += ` - Feriado: ${feriado?.nombre || 'Feriado nacional'}`;
                } else if (enVacanciaJudicial(fecha)) {
                    titulo += ' - Vacancia judicial';
                }
            } else if (fecha >= fechaInicio && fecha <= fechaFin) {
                titulo += ' - Día dentro del término';
            } else {
                titulo += ' - Día hábil';
            }
            
            return titulo;
        }

        function verificarAcceso() {
            const password = document.getElementById('adminPassword').value;
            if (password === 'secretario2025') {
                document.getElementById('adminLogin').classList.add('hidden');
                document.getElementById('adminPanel').classList.remove('hidden');
                document.getElementById('adminPanel').classList.add('animate-fade-in');
                showToast('Acceso administrativo concedido', 'success');
            } else {
                showToast('Contraseña incorrecta', 'error');
                document.getElementById('adminPassword').focus();
            }
        }

        function modificarFecha() {
            const nuevaFecha = document.getElementById('nuevaFecha').value;
            const justificacion = document.getElementById('justificacion').value;
            
            if (!nuevaFecha || !justificacion) {
                showToast('Por favor, complete todos los campos', 'error');
                return;
            }
            
            if (!fechaOriginalCalculada) {
                showToast('Primero debe realizar un cálculo', 'error');
                return;
            }
            
            fechaModificada = new Date(nuevaFecha + 'T00:00:00');
            
            const modificacion = {
                fecha: new Date(),
                fechaOriginal: new Date(fechaOriginalCalculada),
                fechaNueva: new Date(fechaModificada),
                justificacion: justificacion
            };
            
            historialModificaciones.push(modificacion);
            actualizarHistorial();
            calcularTermino();
            
            document.getElementById('nuevaFecha').value = '';
            document.getElementById('justificacion').value = '';
            
            showToast('Fecha modificada exitosamente', 'success');
        }

        function actualizarHistorial() {
            const lista = document.getElementById('listaHistorial');
            if (historialModificaciones.length === 0) {
                lista.innerHTML = '<p class="text-sm text-gray-500">No hay modificaciones registradas</p>';
                return;
            }
            
            lista.innerHTML = historialModificaciones.map(mod => `
                <div class="bg-gray-50 p-3 rounded border text-xs animate-fade-in">
                    <div class="font-medium">${mod.fecha.toLocaleString('es-EC')}</div>
                    <div>Original: ${mod.fechaOriginal.toLocaleDateString('es-EC')}</div>
                    <div>Nueva: ${mod.fechaNueva.toLocaleDateString('es-EC')}</div>
                    <div class="text-gray-600 mt-1">${mod.justificacion}</div>
                </div>
            `).reverse().join('');
        }

        function cargarProximosFeriados() {
            const hoy = new Date();
            const proximosFeriados = [];
            
            for (let año = hoy.getFullYear(); año <= hoy.getFullYear() + 1; año++) {
                if (feriados[año]) {
                    feriados[año].forEach(feriado => {
                        const fechaFeriado = new Date(feriado.fecha + 'T00:00:00');
                        if (fechaFeriado >= hoy && proximosFeriados.length < 10) {
                            proximosFeriados.push({
                                fecha: fechaFeriado,
                                nombre: feriado.nombre
                            });
                        }
                    });
                }
            }

            const contenedor = document.getElementById('proximosFeriados');
            if (proximosFeriados.length > 0) {
                contenedor.innerHTML = proximosFeriados.map((feriado, index) => `
                    <div class="holiday-item flex items-center justify-between p-3 border rounded-lg animate-fade-in" style="animation-delay: ${index * 0.1}s;">
                        <div>
                            <p class="font-medium text-sm">${feriado.nombre}</p>
                            <p class="text-xs text-gray-500">${formatearFecha(feriado.fecha)}</p>
                        </div>
                        <i class="fas fa-calendar-day text-yellow-500"></i>
                    </div>
                `).join('');
            } else {
                contenedor.innerHTML = '<p class="text-center text-gray-500 py-4">No hay feriados próximos</p>';
            }
        }

        function guardarNota() {
            const noteInput = document.getElementById('noteInput');
            const notaGuardada = document.getElementById('notaGuardada');
            if (!noteInput) return;
            const nota = noteInput.value.trim();
            if (nota) {
                const clave = 'nota_' + new Date().getTime();
                localStorage.setItem(clave, nota);
                if (notaGuardada) {
                    notaGuardada.textContent = 'Nota guardada correctamente';
                    setTimeout(() => {
                        notaGuardada.textContent = '';
                    }, 3000);
                }
                noteInput.value = '';
                showToast('Nota guardada correctamente', 'success');
            } else {
                showToast('Por favor, escriba una nota antes de guardar', 'error');
            }
        }

        function toggleDarkMode() {
            document.body.classList.toggle('dark-mode');
            const isDark = document.body.classList.contains('dark-mode');
            localStorage.setItem('darkMode', isDark ? '1' : '0');
            
            const icon = document.querySelector('#darkModeToggle i');
            icon.className = isDark ? 'fas fa-sun' : 'fas fa-moon';
            
            showToast(`Modo ${isDark ? 'oscuro' : 'claro'} activado`, 'success');
        }

        function generarRazon(datos) {
            const nombre = document.getElementById('nombreDemandado')?.value || '______________________';
            let tiempoTexto = '';
            
            try {
                let fechaFinal = fechaModificada ? new Date(fechaModificada) : new Date(datos.fechaVencimiento);
                fechaFinal.setHours(0,0,0,0);
                const hoy = new Date();
                hoy.setHours(0,0,0,0);
                const diasDif = Math.ceil((fechaFinal - hoy) / (1000 * 60 * 60 * 24));
                
                if (diasDif < 0) {
                    tiempoTexto = `${Math.abs(diasDif)} día${Math.abs(diasDif) === 1 ? '' : 's'} desde el vencimiento del término legal`;
                } else if (diasDif === 0) {
                    tiempoTexto = 'el término vence hoy';
                } else {
                    tiempoTexto = `${diasDif} día${diasDif === 1 ? '' : 's'} para que venza el término legal`;
                }
            } catch (e) {
                tiempoTexto = '';
            }
            
            const fechaFinal = fechaModificada ? new Date(fechaModificada) : new Date(datos.fechaVencimiento);
            fechaFinal.setHours(0, 0, 0, 0);
            const fechaFinalTexto = fechaFinal.toLocaleDateString('es-EC', { weekday: 'long', day: 'numeric', month: 'long', year: 'numeric' });
            
            let lineaFecha;
            const hoyRef = new Date();
            hoyRef.setHours(0, 0, 0, 0);
            const diasRestCalc = Math.ceil((fechaFinal - hoyRef) / (1000 * 60 * 60 * 24));
            
            if (diasRestCalc > 0) {
                lineaFecha = `3. La fecha en la que vence el término es el ${fechaFinalTexto} (${datos.config.articulo} COGEP)`;
            } else {
                lineaFecha = `3. La fecha en la que venció el término fue el ${fechaFinalTexto} (${datos.config.articulo} COGEP)`;
            }
            
            return `RAZÓN.- En cumplimiento de la providencia inmediata anterior, se informa lo siguiente:\n1. Respecto al término legal para contestar la demanda. El demandado Sr. ${nombre} no ha contestado la demanda ni ha presentado excepciones dentro del término de ley.\n2. Respecto al término para contestar o para presentar el recurso, han transcurrido ${tiempoTexto}.\n${lineaFecha}\nParticular que certifico para los fines de ley.`;
        }

        function copiarRazon() {
            const razonElem = document.getElementById('razonTexto');
            if (!razonElem) return;
            
            navigator.clipboard.writeText(razonElem.value).then(() => {
                showToast('Razón copiada al portapapeles', 'success');
            }).catch(() => {
                // Fallback para navegadores más antiguos
                razonElem.select();
                document.execCommand('copy');
                showToast('Razón copiada al portapapeles', 'success');
            });
        }

        // Función para exportar evento al calendario
        function exportarEventoCalendario() {
            if (!datosUltimoCalculo) {
                showToast('Debe realizar un cálculo primero', 'error');
                return;
            }

            const fechaVenc = fechaModificada || datosUltimoCalculo.fechaVencimiento;
            const nombre = document.getElementById('nombreDemandado')?.value || 'Demandado';
            
            const evento = {
                title: `Vencimiento: ${datosUltimoCalculo.config.nombre}`,
                start: fechaVenc,
                description: `Demandado: ${nombre}\nProcedimiento: ${datosUltimoCalculo.tipoTramite}\nBase legal: ${datosUltimoCalculo.config.articulo} COGEP\nFecha de inicio: ${datosUltimoCalculo.fechaInicio.toLocaleDateString('es-EC')}`
            };

            const icsContent = generarICS(evento);
            descargarArchivo(icsContent, `vencimiento_${fechaVenc.toISOString().slice(0, 10)}.ics`, 'text/calendar');
            showToast('Evento exportado al calendario', 'success');
        }

        function generarICS(evento) {
            const formatearFechaICS = (fecha) => {
                return fecha.toISOString().replace(/[-:]/g, '').split('.')[0] + 'Z';
            };

            const fechaInicio = new Date(evento.start);
            fechaInicio.setHours(9, 0, 0, 0); // 9:00 AM

            const fechaFin = new Date(fechaInicio);
            fechaFin.setHours(10, 0, 0, 0); // 10:00 AM

            const ahora = new Date();

            return [
                'BEGIN:VCALENDAR',
                'VERSION:2.0',
                'PRODID:-//Calculadora COGEP//ES',
                'BEGIN:VEVENT',
                `UID:${ahora.getTime()}@cogep-calculator.com`,
                `DTSTAMP:${formatearFechaICS(ahora)}`,
                `DTSTART:${formatearFechaICS(fechaInicio)}`,
                `DTEND:${formatearFechaICS(fechaFin)}`,
                `SUMMARY:${evento.title}`,
                `DESCRIPTION:${evento.description.replace(/\n/g, '\\n')}`,
                'BEGIN:VALARM',
                'TRIGGER:-P1D',
                'DESCRIPTION:Recordatorio: Vencimiento de término procesal mañana',
                'ACTION:DISPLAY',
                'END:VALARM',
                'BEGIN:VALARM',
                'TRIGGER:-PT2H',
                'DESCRIPTION:Recordatorio: Vencimiento de término procesal en 2 horas',
                'ACTION:DISPLAY',
                'END:VALARM',
                'END:VEVENT',
                'END:VCALENDAR'
            ].join('\r\n');
        }

        function descargarArchivo(contenido, nombreArchivo, tipoMime) {
            const blob = new Blob([contenido], { type: tipoMime });
            const url = URL.createObjectURL(blob);
            const a = document.createElement('a');
            a.href = url;
            a.download = nombreArchivo;
            document.body.appendChild(a);
            a.click();
            document.body.removeChild(a);
            URL.revokeObjectURL(url);
        }

        // Inicialización mejorada
        document.addEventListener('DOMContentLoaded', function() {
            // Aplicar tema guardado
            const darkPref = localStorage.getItem('darkMode');
            if (darkPref === '1') {
                document.body.classList.add('dark-mode');
                const icon = document.querySelector('#darkModeToggle i');
                if (icon) icon.className = 'fas fa-sun';
            }
            
            // Configurar fecha inicial
            const hoy = new Date();
            const fechaInput = document.getElementById('fechaInicio');
            if (fechaInput) {
                fechaInput.value = hoy.toISOString().slice(0, 10);
            }
            
            // Cargar datos iniciales
            cargarProximosFeriados();
            mostrarReferenciaLegal();

            // Configurar evento de cambio de región
            const regionVacSelect = document.getElementById('regionVacanciaSelect');
            if (regionVacSelect) {
                regionVacSelect.value = regionVacancia;
                actualizarVacanciaInfo();
                regionVacSelect.addEventListener('change', function() {
                    regionVacancia = this.value;
                    actualizarVacanciaInfo();
                    const resultadoElem = document.getElementById('resultado');
                    if (resultadoElem && resultadoElem.innerHTML.trim() !== '' && resultadoElem.innerText.indexOf('Ingrese los datos') === -1) {
                        calcularTermino();
                    }
                });
            } else {
                actualizarVacanciaInfo();
            }

            // Configurar atajos de teclado
            document.addEventListener('keydown', function(e) {
                if (e.ctrlKey || e.metaKey) {
                    switch(e.key) {
                        case 'Enter':
                            e.preventDefault();
                            calcularTermino();
                            break;
                        case 'p':
                            e.preventDefault();
                            window.print();
                            break;
                    }
                }
            });

            // Mostrar mensaje de bienvenida
            setTimeout(() => {
                showToast('Calculadora COGEP cargada correctamente', 'success');
            }, 1000);
        });
    </script>
</body>
</html>
