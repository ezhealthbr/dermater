<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dermater® Brand Book Interativo</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600;700&family=Open+Sans:wght@400;600&display=swap" rel="stylesheet">
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <style>
        body {
            font-family: 'Open Sans', sans-serif;
            background-color: #FFFFFF; /* Branco Neve */
        }
        h1, h2, h3, .font-montserrat {
            font-family: 'Montserrat', sans-serif;
        }
        .dermater-logo-font-derma {
            font-family: 'Montserrat', sans-serif;
            font-weight: 500; /* Medium */
        }
        .dermater-logo-font-ter {
            font-family: 'Montserrat', sans-serif;
            font-weight: 700; /* Bold */
        }
        .bg-azul-dermater { background-color: #356064; }
        .text-azul-dermater { color: #356064; }
        .border-azul-dermater { border-color: #356064; }
        .bg-cinza-azulado { background-color: #D9E1E2; }
        .text-cinza-azulado { color: #D9E1E2; }
        .bg-azul-tecnico { background-color: #4F99C0; }
        .text-azul-tecnico { color: #4F99C0; }
        .bg-verde-calmante { background-color: #95BFB9; }
        .text-verde-calmante { color: #95BFB9; }
        .bg-verde-natural { background-color: #7CA89A; }
        .text-verde-natural { color: #7CA89A; }
        .bg-dourado-neutro { background-color: #C1B29F; }
        .text-dourado-neutro { color: #C1B29F; }
        .border-dourado-neutro { border-color: #C1B29F; }
        .content-section { display: none; }
        .content-section.active { display: block; }
        .nav-link {
            display: block;
            padding: 0.75rem 1.5rem;
            margin-bottom: 0.5rem;
            border-radius: 0.375rem;
            transition: background-color 0.2s ease-in-out, color 0.2s ease-in-out;
        }
        .nav-link:hover {
            background-color: #e9f0f1; /* Tom mais claro do Cinza Azulado */
            color: #356064; /* Azul Dermater */
        }
        .nav-link.active {
            background-color: #356064; /* Azul Dermater */
            color: #FFFFFF; /* Branco Neve */
            font-weight: 600;
        }
        .chart-container {
            position: relative;
            width: 100%;
            max-width: 400px; /* Max width for pie chart */
            margin-left: auto;
            margin-right: auto;
            height: 300px; /* Base height */
            max-height: 350px;
        }
        @media (min-width: 768px) {
            .chart-container {
                height: 350px;
            }
        }
        .color-swatch {
            width: 100px;
            height: 100px;
            border: 1px solid #D9E1E2; /* Cinza Azulado Claro */
        }
        .font-sample {
            border: 1px solid #D9E1E2;
            padding: 1rem;
            margin-top: 0.5rem;
            border-radius: 0.25rem;
            background-color: #f8f9fa;
        }
        .accordion-button {
            background-color: #f0f4f5; /* Light gray-blue for inactive */
            color: #356064;
            font-weight: 600;
        }
        .accordion-button.active, .accordion-button:hover {
            background-color: #4F99C0; /* Azul Técnico for active/hover */
            color: #FFFFFF;
        }
        .accordion-content {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.3s ease-out;
            background-color: #FFFFFF;
            border: 1px solid #D9E1E2;
            border-top: none;
        }
        .logo-with-r {
            position: relative;
            display: inline-block;
        }
        .logo-r-symbol {
            position: absolute;
            top: -0.5em; /* Adjust as needed */
            right: -1.2em; /* Adjust as needed */
            font-size: 0.4em; /* Adjust relative to logo size */
            vertical-align: super;
        }
    </style>
</head>
<body class="bg-branco-neve text-gray-800 flex min-h-screen">

    <aside class="w-64 bg-white shadow-lg p-6 space-y-2 fixed top-0 left-0 h-full overflow-y-auto">
        <div class="text-center mb-8">
            <h1 class="text-2xl font-montserrat font-bold text-azul-dermater">Dermater®</h1>
            <p class="text-sm text-gray-600 font-montserrat">Brand Book</p>
            <p class="text-xs text-gray-500 font-montserrat">Versão 2.0 2025</p>
        </div>
        <nav>
            <a href="#essencia" class="nav-link active">1. Essência da Marca</a>
            <a href="#logotipo" class="nav-link">2. Logotipo</a>
            <a href="#paleta-cores" class="nav-link">3. Paleta de Cores</a>
            <a href="#tipografia" class="nav-link">4. Tipografia</a>
            <a href="#aplicacoes" class="nav-link">5. Aplicações da Marca</a>
            <a href="#usos-premium" class="nav-link">6. Usos Dourado/Verde</a>
            <a href="#hierarquia-visual" class="nav-link">7. Hierarquia Visual</a>
            <a href="#versoes-logo" class="nav-link">8. Versões do Logotipo</a>
            <a href="#regras-uso" class="nav-link">9. Regras de Uso</a>
            <a href="#mockups" class="nav-link">10. Mockups (Sugestão)</a>
            <a href="#conclusao" class="nav-link">11. Conclusão</a>
        </nav>
    </aside>

    <main class="ml-64 flex-1 p-8 md:p-12 overflow-y-auto">
        
        <section id="essencia" class="content-section active">
            <h2 class="text-3xl font-montserrat font-bold text-azul-dermater mb-6">1. Essência da Marca</h2>
            <p class="mb-6 text-gray-700">Esta seção define o núcleo da identidade Dermater. O posicionamento, tom de comunicação e pilares visuais são fundamentais para guiar todas as expressões da marca, assegurando consistência e alinhamento com seus valores de sofisticação, ciência e alta performance.</p>
            
            <div class="bg-cinza-azulado p-6 rounded-lg shadow mb-6">
                <h3 class="text-xl font-montserrat font-semibold text-azul-dermater mb-3">Origem do Nome</h3>
                <p class="text-gray-700">O nome "Dermater" deriva da junção das palavras "Dermatologia" e "Terapia", refletindo a expertise científica no cuidado com a pele e a abordagem de tratamento e bem-estar que a marca oferece.</p>
            </div>

            <div class="bg-cinza-azulado p-6 rounded-lg shadow mb-6">
                <h3 class="text-xl font-montserrat font-semibold text-azul-dermater mb-3">Posicionamento</h3>
                <p class="text-gray-700">Dermocosmético premium, científico e de alta performance, com apelo clínico, mas sensorialmente sofisticado.</p>
            </div>

            <div class="bg-cinza-azulado p-6 rounded-lg shadow mb-6">
                <h3 class="text-xl font-montserrat font-semibold text-azul-dermater mb-3">Tom da Comunicação</h3>
                <p class="text-gray-700">Preciso, confiável, técnico, minimalista e elegante.</p>
            </div>

            <div class="bg-cinza-azulado p-6 rounded-lg shadow mb-6">
                <h3 class="text-xl font-montserrat font-semibold text-azul-dermater mb-3">Slogan</h3>
                <p class="text-gray-700 font-bold">“Dermater. Ciência que transforma sua pele.”</p>
            </div>

            <div class="bg-cinza-azulado p-6 rounded-lg shadow mb-6">
                <h3 class="text-xl font-montserrat font-semibold text-azul-dermater mb-3">Tagline</h3>
                <p class="text-gray-700 font-bold">“Dermocosméticos de alta performance, com respaldo científico.”</p>
            </div>

            <div class="bg-cinza-azulado p-6 rounded-lg shadow">
                <h3 class="text-xl font-montserrat font-semibold text-azul-dermater mb-3">Pilares Visuais</h3>
                <ul class="list-disc list-inside text-gray-700 space-y-1">
                    <li>Dermatologia avançada</li>
                    <li>Tecnologia de resultados</li>
                    <li>Beleza natural e cuidado com a pele</li>
                    <li>Design limpo, sofisticado e atemporal</li>
                </ul>
            </div>
        </section>

        <section id="logotipo" class="content-section">
            <h2 class="text-3xl font-montserrat font-bold text-azul-dermater mb-6">2. Logotipo</h2>
            <p class="mb-6 text-gray-700">O logotipo Dermater é a assinatura visual principal da marca. Sua construção tipográfica foi cuidadosamente pensada para comunicar os valores centrais da marca: a fusão entre ciência dermatológica e a força de resultados confiáveis. Abaixo, detalhamos sua estrutura e o significado por trás de sua composição.</p>

            <div class="bg-cinza-azulado p-6 rounded-lg shadow mb-6 text-center">
                <h3 class="text-xl font-montserrat font-semibold text-azul-dermater mb-4">Construção Tipográfica</h3>
                <div class="text-5xl md:text-7xl text-azul-dermater my-8 logo-with-r">
                    <span class="dermater-logo-font-derma">DERMA</span><span class="dermater-logo-font-ter">TER</span><span class="logo-r-symbol">®</span>
                </div>
                <p class="text-gray-700 mt-4"><span class="font-semibold">DERMA</span> → Montserrat Medium (500)</p>
                <p class="text-gray-700"><span class="font-semibold">TER</span> → Montserrat Bold (700)</p>
            </div>

            <div class="bg-cinza-azulado p-6 rounded-lg shadow">
                <h3 class="text-xl font-montserrat font-semibold text-azul-dermater mb-3">Tradução da Composição</h3>
                <ul class="list-disc list-inside text-gray-700 space-y-1">
                    <li><span class="font-semibold">Leveza e precisão</span> na parte científica (“DERMA”)</li>
                    <li><span class="font-semibold">Força, confiança e estabilidade</span> na assinatura da marca (“TER”)</li>
                </ul>
            </div>
        </section>

        <section id="paleta-cores" class="content-section">
            <h2 class="text-3xl font-montserrat font-bold text-azul-dermater mb-6">3. Paleta de Cores Oficial</h2>
            <p class="mb-6 text-gray-700">A paleta de cores Dermater foi selecionada para transmitir sofisticação, confiança e uma conexão com a ciência e a natureza. Cada cor tem uma função específica, contribuindo para uma identidade visual coesa e elegante. Utilize esta seção para consultar os códigos HEX e entender o papel de cada tom.</p>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 mb-8">
                <div class="bg-white p-4 rounded-lg shadow border border-cinza-azulado">
                    <div class="color-swatch bg-azul-dermater rounded-md mx-auto mb-3"></div>
                    <h4 class="font-montserrat font-semibold text-azul-dermater text-center">Azul Profundo Dermater</h4>
                    <p class="text-xs text-gray-600 text-center mb-1">#356064</p>
                    <p class="text-xs text-gray-500 text-center mb-2">Principal (logo, títulos)</p>
                    <button class="copy-hex-btn w-full bg-azul-tecnico text-white text-xs py-1 px-2 rounded hover:bg-azul-dermater transition-colors" data-hex="#356064">Copiar HEX</button>
                </div>
                <div class="bg-white p-4 rounded-lg shadow border border-cinza-azulado">
                    <div class="color-swatch bg-white rounded-md mx-auto mb-3"></div>
                    <h4 class="font-montserrat font-semibold text-azul-dermater text-center">Branco Neve</h4>
                    <p class="text-xs text-gray-600 text-center mb-1">#FFFFFF</p>
                    <p class="text-xs text-gray-500 text-center mb-2">Fundo primário, pureza</p>
                    <button class="copy-hex-btn w-full bg-azul-tecnico text-white text-xs py-1 px-2 rounded hover:bg-azul-dermater transition-colors" data-hex="#FFFFFF">Copiar HEX</button>
                </div>
                <div class="bg-white p-4 rounded-lg shadow border border-cinza-azulado">
                    <div class="color-swatch bg-cinza-azulado rounded-md mx-auto mb-3"></div>
                    <h4 class="font-montserrat font-semibold text-azul-dermater text-center">Cinza Azulado Claro</h4>
                    <p class="text-xs text-gray-600 text-center mb-1">#D9E1E2</p>
                    <p class="text-xs text-gray-500 text-center mb-2">Fundo secundário, cards</p>
                    <button class="copy-hex-btn w-full bg-azul-tecnico text-white text-xs py-1 px-2 rounded hover:bg-azul-dermater transition-colors" data-hex="#D9E1E2">Copiar HEX</button>
                </div>
                <div class="bg-white p-4 rounded-lg shadow border border-cinza-azulado">
                    <div class="color-swatch bg-azul-tecnico rounded-md mx-auto mb-3"></div>
                    <h4 class="font-montserrat font-semibold text-azul-dermater text-center">Azul Claro Técnico</h4>
                    <p class="text-xs text-gray-600 text-center mb-1">#4F99C0</p>
                    <p class="text-xs text-gray-500 text-center mb-2">Detalhes técnicos, ícones</p>
                    <button class="copy-hex-btn w-full bg-azul-tecnico text-white text-xs py-1 px-2 rounded hover:bg-azul-dermater transition-colors" data-hex="#4F99C0">Copiar HEX</button>
                </div>
                <div class="bg-white p-4 rounded-lg shadow border border-cinza-azulado">
                    <div class="color-swatch bg-verde-calmante rounded-md mx-auto mb-3"></div>
                    <h4 class="font-montserrat font-semibold text-azul-dermater text-center">Verde Calmante</h4>
                    <p class="text-xs text-gray-600 text-center mb-1">#95BFB9</p>
                    <p class="text-xs text-gray-500 text-center mb-2">Bem-estar, naturalidade</p>
                    <button class="copy-hex-btn w-full bg-azul-tecnico text-white text-xs py-1 px-2 rounded hover:bg-azul-dermater transition-colors" data-hex="#95BFB9">Copiar HEX</button>
                </div>
                <div class="bg-white p-4 rounded-lg shadow border border-cinza-azulado">
                    <div class="color-swatch bg-verde-natural rounded-md mx-auto mb-3"></div>
                    <h4 class="font-montserrat font-semibold text-azul-dermater text-center">Verde Natural Premium</h4>
                    <p class="text-xs text-gray-600 text-center mb-1">#7CA89A</p>
                    <p class="text-xs text-gray-500 text-center mb-2">Destaques orgânicos</p>
                    <button class="copy-hex-btn w-full bg-azul-tecnico text-white text-xs py-1 px-2 rounded hover:bg-azul-dermater transition-colors" data-hex="#7CA89A">Copiar HEX</button>
                </div>
                 <div class="bg-white p-4 rounded-lg shadow border border-cinza-azulado md:col-span-1 lg:col-span-1">
                    <div class="color-swatch bg-dourado-neutro rounded-md mx-auto mb-3"></div>
                    <h4 class="font-montserrat font-semibold text-azul-dermater text-center">Dourado Neutro</h4>
                    <p class="text-xs text-gray-600 text-center mb-1">#C1B29F</p>
                    <p class="text-xs text-gray-500 text-center mb-2">Detalhes premium sutis</p>
                    <button class="copy-hex-btn w-full bg-azul-tecnico text-white text-xs py-1 px-2 rounded hover:bg-azul-dermater transition-colors" data-hex="#C1B29F">Copiar HEX</button>
                </div>
            </div>
            
            <h3 class="text-xl font-montserrat font-semibold text-azul-dermater mb-4 text-center">Distribuição Conceitual da Paleta</h3>
            <div class="chart-container mb-6">
                <canvas id="colorPaletteChart"></canvas>
            </div>
            <p class="text-sm text-gray-600 text-center">Este gráfico ilustra uma divisão conceitual da paleta, por exemplo, entre cores estruturais/principais e cores de acento/funcionais, para demonstrar o equilíbrio da paleta.</p>
            <div id="copy-feedback" class="fixed bottom-5 right-5 bg-azul-dermater text-white px-4 py-2 rounded-md shadow-lg transition-opacity duration-300 opacity-0">Código copiado!</div>


        </section>

        <section id="tipografia" class="content-section">
            <h2 class="text-3xl font-montserrat font-bold text-azul-dermater mb-6">4. Tipografia Oficial</h2>
            <p class="mb-6 text-gray-700">A tipografia Dermater é composta pelas fontes Montserrat e Open Sans, escolhidas por sua elegância, legibilidade e versatilidade. Elas trabalham em conjunto para criar uma hierarquia visual clara e comunicar a mensagem da marca com precisão e sofisticação. Explore abaixo os usos específicos e pesos de cada fonte.</p>

            <div class="space-y-6">
                <div>
                    <h3 class="text-xl font-montserrat font-semibold text-azul-tecnico mb-2">Logo</h3>
                    <p><span class="font-semibold">Fonte:</span> Montserrat | <span class="font-semibold">Peso:</span> Medium (500) + Bold (700)</p>
                    <p><span class="font-semibold">Característica:</span> Geométrica, elegante, moderna</p>
                    <div class="font-sample">
                        <span class="dermater-logo-font-derma">DERMA</span><span class="dermater-logo-font-ter">TER</span><span class="logo-r-symbol text-azul-dermater" style="font-size: 0.4em;">®</span>
                    </div>
                </div>
                <div>
                    <h3 class="text-xl font-montserrat font-semibold text-azul-tecnico mb-2">Títulos Principais</h3>
                    <p><span class="font-semibold">Fonte:</span> Montserrat | <span class="font-semibold">Peso:</span> Bold (700)</p>
                    <p><span class="font-semibold">Característica:</span> Força, clareza visual, contraste técnico</p>
                    <div class="font-sample">
                        <h1 class="font-montserrat font-bold text-2xl">Este é um Título Principal</h1>
                    </div>
                </div>
                <div>
                    <h3 class="text-xl font-montserrat font-semibold text-azul-tecnico mb-2">Subtítulos</h3>
                    <p><span class="font-semibold">Fonte:</span> Montserrat | <span class="font-semibold">Peso:</span> Medium (500)</p>
                    <p><span class="font-semibold">Característica:</span> Leve, limpo, equilibrado</p>
                    <div class="font-sample">
                        <h2 class="font-montserrat font-medium text-xl">Este é um Subtítulo</h2>
                    </div>
                </div>
                <div>
                    <h3 class="text-xl font-montserrat font-semibold text-azul-tecnico mb-2">Texto Corrido</h3>
                    <p><span class="font-semibold">Fonte:</span> Open Sans | <span class="font-semibold">Peso:</span> Regular (400)</p>
                    <p><span class="font-semibold">Característica:</span> Legibilidade superior, neutra e versátil</p>
                    <div class="font-sample">
                        <p class="text-base">Este é um exemplo de texto corrido, utilizado para parágrafos e descrições mais longas, garantindo uma leitura agradável.</p>
                    </div>
                </div>
                <div>
                    <h3 class="text-xl font-montserrat font-semibold text-azul-tecnico mb-2">Destaques Técnicos</h3>
                    <p><span class="font-semibold">Fonte:</span> Open Sans | <span class="font-semibold">Peso:</span> Semibold (600)</p>
                    <p><span class="font-semibold">Característica:</span> Ênfase em bullet points, boxes ou callouts</p>
                    <div class="font-sample">
                        <p class="font-semibold text-base">Informação técnica importante ou um callout relevante.</p>
                    </div>
                </div>
            </div>
        </section>

        <section id="aplicacoes" class="content-section">
            <h2 class="text-3xl font-montserrat font-bold text-azul-dermater mb-6">5. Aplicações da Marca</h2>
            <p class="mb-6 text-gray-700">Esta seção detalha como a identidade visual Dermater deve ser aplicada em diferentes contextos, desde embalagens de produtos até materiais digitais e científicos. O objetivo é manter a consistência e o reconhecimento da marca em todos os pontos de contato. Clique nos itens abaixo para expandir e ver as diretrizes específicas.</p>

            <div class="space-y-4" id="accordionContainer">
                <div>
                    <button class="accordion-button w-full text-left p-4 rounded-t-md focus:outline-none transition-colors duration-300 ease-in-out">
                        ✔️ Embalagens de Produto
                    </button>
                    <div class="accordion-content p-4 rounded-b-md">
                        <ul class="list-disc list-inside space-y-2 text-gray-700">
                            <li>Fundo branco predominante.</li>
                            <li>Logotipo em <span class="text-azul-dermater font-semibold">Azul Dermater (#356064)</span> ou em <span class="text-dourado-neutro font-semibold">dourado discreto (#C1B29F)</span> em versões premium.</li>
                            <li>Uso de linhas finas ou divisores em dourado, verde natural ou cinza azulado.</li>
                            <li>Elementos técnicos (como ativos ou benefícios) destacados em <span class="text-azul-tecnico font-semibold">Azul Técnico (#4F99C0)</span>.</li>
                        </ul>
                    </div>
                </div>
                <div>
                    <button class="accordion-button w-full text-left p-4 focus:outline-none transition-colors duration-300 ease-in-out">
                        ✔️ E-commerce e Materiais Digitais
                    </button>
                    <div class="accordion-content p-4">
                        <ul class="list-disc list-inside space-y-2 text-gray-700">
                            <li>Fundo claro predominante.</li>
                            <li>Botões e call-to-actions (CTAs) em <span class="text-azul-tecnico font-semibold">Azul Técnico</span> ou <span class="text-verde-natural font-semibold">Verde Natural</span>.</li>
                            <li>Área de conteúdo técnico em fundo <span class="text-cinza-azulado">Cinza Azulado Claro</span>, para gerar contraste suave.</li>
                        </ul>
                    </div>
                </div>
                <div>
                    <button class="accordion-button w-full text-left p-4 rounded-b-md focus:outline-none transition-colors duration-300 ease-in-out">
                        ✔️ Material Técnico e Científico
                    </button>
                    <div class="accordion-content p-4">
                        <ul class="list-disc list-inside space-y-2 text-gray-700">
                            <li>Cabeçalhos fortes em <span class="font-montserrat font-bold text-azul-dermater">Montserrat Bold na cor Azul Dermater</span>.</li>
                            <li>Texto corrido em Open Sans Regular em preto ou cinza escuro.</li>
                            <li>Caixas de destaques técnicos em <span class="text-cinza-azulado">Cinza Azulado Claro</span> ou <span class="text-verde-calmante">Verde Calmante</span>.</li>
                        </ul>
                    </div>
                </div>
            </div>
        </section>

        <section id="usos-premium" class="content-section">
            <h2 class="text-3xl font-montserrat font-bold text-azul-dermater mb-6">6. Usos do Dourado e Verde Premium</h2>
            <p class="mb-6 text-gray-700">O Dourado Neutro e o Verde Natural Premium são cores de destaque que adicionam um toque de sofisticação e conexão com a naturalidade, respectivamente. Seu uso deve ser sutil e estratégico para reforçar a percepção premium da marca. Veja abaixo as orientações específicas para a aplicação destes tons.</p>
            <div class="overflow-x-auto">
                <table class="min-w-full bg-white border border-cinza-azulado rounded-lg shadow">
                    <thead class="bg-cinza-azulado">
                        <tr>
                            <th class="font-montserrat text-left font-semibold text-azul-dermater p-3">Elemento</th>
                            <th class="font-montserrat text-left font-semibold text-azul-dermater p-3">Cor Aplicada</th>
                            <th class="font-montserrat text-left font-semibold text-azul-dermater p-3">Função</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr class="border-b border-cinza-azulado">
                            <td class="p-3 text-gray-700">Selos de qualidade</td>
                            <td class="p-3 text-dourado-neutro font-semibold">Dourado (#C1B29F)</td>
                            <td class="p-3 text-gray-700">Reforçar percepção premium, sem ostentação</td>
                        </tr>
                        <tr class="border-b border-cinza-azulado">
                            <td class="p-3 text-gray-700">Bordas de rótulos</td>
                            <td class="p-3 text-dourado-neutro font-semibold">Dourado discreto</td>
                            <td class="p-3 text-gray-700">Refinamento elegante</td>
                        </tr>
                        <tr class="border-b border-cinza-azulado">
                            <td class="p-3 text-gray-700">Callouts de naturalidade</td>
                            <td class="p-3 text-verde-natural font-semibold">Verde Natural (#7CA89A)</td>
                            <td class="p-3 text-gray-700">Ênfase na conexão com ingredientes naturais</td>
                        </tr>
                        <tr>
                            <td class="p-3 text-gray-700">Elementos de UX</td>
                            <td class="p-3"><span class="text-verde-natural font-semibold">Verde</span> ou <span class="text-azul-tecnico font-semibold">Azul Técnico</span></td>
                            <td class="p-3 text-gray-700">Guiar interações digitais com leveza e sofisticação</td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </section>

        <section id="hierarquia-visual" class="content-section">
            <h2 class="text-3xl font-montserrat font-bold text-azul-dermater mb-6">7. Hierarquia Visual (Exemplo)</h2>
            <p class="mb-6 text-gray-700">Uma hierarquia visual clara é crucial para a legibilidade e o impacto da comunicação. Esta seção demonstra um exemplo de como os diferentes níveis de texto devem ser formatados, combinando as fontes e cores da marca para criar uma estrutura coesa e fácil de seguir. Observe como cada elemento contribui para a organização da informação.</p>
            <div class="space-y-4">
                <div class="p-4 border border-cinza-azulado rounded-lg bg-white">
                    <p class="text-xs text-gray-500 mb-1">H1 - Título de Seção</p>
                    <h1 class="font-montserrat font-bold text-3xl text-azul-dermater">Título de Seção Principal</h1>
                </div>
                <div class="p-4 border border-cinza-azulado rounded-lg bg-white">
                    <p class="text-xs text-gray-500 mb-1">H2 - Subtítulo</p>
                    <h2 class="font-montserrat font-medium text-2xl text-azul-tecnico">Subtítulo Importante</h2>
                </div>
                <div class="p-4 border border-cinza-azulado rounded-lg bg-white">
                    <p class="text-xs text-gray-500 mb-1">Body - Texto Principal</p>
                    <p class="text-base text-gray-800" style="color: #222222;">Este é o texto principal para parágrafos de conteúdo. Ele utiliza Open Sans Regular para máxima legibilidade e conforto visual, mantendo um tom neutro e profissional.</p>
                </div>
                <div class="p-4 border border-cinza-azulado rounded-lg bg-white">
                    <p class="text-xs text-gray-500 mb-1">Callout - Destaque Técnico</p>
                    <p class="font-opensans font-semibold text-base text-verde-natural">Callout: Destaque para informações sobre ingredientes naturais ou benefícios específicos.</p>
                </div>
                <div class="p-4 border border-cinza-azulado rounded-lg bg-white">
                    <p class="text-xs text-gray-500 mb-1">Detalhe - Linhas, Divisores, Selos</p>
                    <div class="h-px bg-dourado-neutro my-2 w-1/2"></div>
                    <p class="font-montserrat text-sm text-dourado-neutro">Selo de Qualidade | Linha Fina</p>
                </div>
            </div>
        </section>

        <section id="versoes-logo" class="content-section">
            <h2 class="text-3xl font-montserrat font-bold text-azul-dermater mb-6">8. Versões do Logotipo</h2>
            <p class="mb-6 text-gray-700">Para garantir a flexibilidade e a correta aplicação do logotipo Dermater em diversas mídias e fundos, diferentes versões foram criadas. É essencial escolher a versão mais adequada para manter a legibilidade e o impacto visual da marca. Abaixo apresentamos as principais variações e suas recomendações de uso.</p>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                <div class="p-6 border border-cinza-azulado rounded-lg text-center bg-white">
                    <h3 class="font-montserrat font-semibold text-azul-dermater mb-3">Principal</h3>
                    <div class="text-5xl text-azul-dermater my-4 logo-with-r">
                        <span class="dermater-logo-font-derma">DERMA</span><span class="dermater-logo-font-ter">TER</span><span class="logo-r-symbol">®</span>
                    </div>
                    <p class="text-sm text-gray-600">Azul Dermater sobre fundo branco.</p>
                </div>
                <div class="p-6 border border-cinza-azulado rounded-lg text-center bg-azul-dermater">
                    <h3 class="font-montserrat font-semibold text-white mb-3">Secundária</h3>
                     <div class="text-5xl text-white my-4 logo-with-r">
                        <span class="dermater-logo-font-derma">DERMA</span><span class="dermater-logo-font-ter">TER</span><span class="logo-r-symbol">®</span>
                    </div>
                    <p class="text-sm text-cinza-azulado">Branco sobre fundo Azul Dermater.</p>
                </div>
                <div class="p-6 border border-cinza-azulado rounded-lg text-center bg-white">
                    <h3 class="font-montserrat font-semibold text-azul-dermater mb-3">Premium (Opção 1)</h3>
                    <div class="text-5xl text-dourado-neutro my-4 logo-with-r">
                        <span class="dermater-logo-font-derma">DERMA</span><span class="dermater-logo-font-ter">TER</span><span class="logo-r-symbol">®</span>
                    </div>
                    <p class="text-sm text-gray-600">Dourado sobre fundo branco.</p>
                </div>
                <div class="p-6 border border-cinza-azulado rounded-lg text-center bg-gray-900">
                    <h3 class="font-montserrat font-semibold text-white mb-3">Premium (Opção 2)</h3>
                     <div class="text-5xl text-dourado-neutro my-4 logo-with-r">
                        <span class="dermater-logo-font-derma">DERMA</span><span class="dermater-logo-font-ter">TER</span><span class="logo-r-symbol">®</span>
                    </div>
                    <p class="text-sm text-cinza-azulado">Dourado sobre fundo preto.</p>
                </div>
                 <div class="p-6 border border-cinza-azulado rounded-lg text-center bg-white">
                    <h3 class="font-montserrat font-semibold text-azul-dermater mb-3">Monocromática (Preto)</h3>
                    <div class="text-5xl text-black my-4 logo-with-r">
                        <span class="dermater-logo-font-derma">DERMA</span><span class="dermater-logo-font-ter">TER</span><span class="logo-r-symbol">®</span>
                    </div>
                    <p class="text-sm text-gray-600">Preto 100% sobre fundo claro.</p>
                </div>
                <div class="p-6 border border-cinza-azulado rounded-lg text-center bg-black">
                    <h3 class="font-montserrat font-semibold text-white mb-3">Monocromática (Branco)</h3>
                     <div class="text-5xl text-white my-4 logo-with-r">
                        <span class="dermater-logo-font-derma">DERMA</span><span class="dermater-logo-font-ter">TER</span><span class="logo-r-symbol">®</span>
                    </div>
                    <p class="text-sm text-cinza-azulado">Branco puro sobre fundo escuro.</p>
                </div>
            </div>
        </section>

        <section id="regras-uso" class="content-section">
            <h2 class="text-3xl font-montserrat font-bold text-azul-dermater mb-6">9. Regras de Uso</h2>
            <p class="mb-6 text-gray-700">Para manter a integridade e o reconhecimento da marca Dermater, é vital seguir algumas regras básicas de aplicação do logotipo. Estas diretrizes garantem que o logotipo seja sempre apresentado de forma clara, legível e impactante. Consulte as permissões e restrições abaixo para um uso correto.</p>
            <div class="space-y-4">
                <div class="bg-cinza-azulado p-6 rounded-lg shadow">
                    <h3 class="text-lg font-montserrat font-semibold text-azul-dermater mb-2">Fundo do Logotipo</h3>
                    <p class="text-green-600 flex items-center mb-1"><span class="text-2xl mr-2">✅</span> Permitido: Sempre sobre fundo branco ou fundos claros da paleta que garantam contraste.</p>
                    <p class="text-red-600 flex items-center"><span class="text-2xl mr-2">❌</span> Não permitido: Sobre fundos poluídos, com texturas complexas ou cores que comprometam a legibilidade.</p>
                </div>
                <div class="bg-cinza-azulado p-6 rounded-lg shadow">
                    <h3 class="text-lg font-montserrat font-semibold text-azul-dermater mb-2">Legibilidade</h3>
                    <p class="text-green-600 flex items-center mb-1"><span class="text-2xl mr-2">✅</span> Permitido: Garantir contraste suficiente entre o logotipo e o fundo.</p>
                    <p class="text-red-600 flex items-center"><span class="text-2xl mr-2">❌</span> Não permitido: Aplicar sobre fundos com baixo contraste ou que dificultem a leitura.</p>
                </div>
                <div class="bg-cinza-azulado p-6 rounded-lg shadow">
                    <h3 class="text-lg font-montserrat font-semibold text-azul-dermater mb-2">Espaçamento Mínimo (Área de Proteção)</h3>
                    <p class="text-green-600 flex items-center mb-1"><span class="text-2xl mr-2">✅</span> Permitido: Manter uma margem de respiro ao redor do logotipo, no mínimo equivalente à altura da letra "D" maiúscula do logo.</p>
                    <p class="text-red-600 flex items-center"><span class="text-2xl mr-2">❌</span> Não permitido: Aproximação excessiva de outros elementos gráficos, textos ou bordas da peça.</p>
                </div>
                 <div class="bg-cinza-azulado p-6 rounded-lg shadow">
                    <h3 class="text-lg font-montserrat font-semibold text-azul-dermater mb-2">Integridade do Logotipo</h3>
                    <p class="text-green-600 flex items-center mb-1"><span class="text-2xl mr-2">✅</span> Permitido: Usar as versões oficiais do logotipo sem alterações.</p>
                    <p class="text-red-600 flex items-center"><span class="text-2xl mr-2">❌</span> Não permitido: Distorcer, rotacionar, adicionar efeitos, mudar cores fora da paleta ou alterar a proporção dos elementos do logotipo.</p>
                </div>
            </div>
        </section>

        <section id="mockups" class="content-section">
            <h2 class="text-3xl font-montserrat font-bold text-azul-dermater mb-6">10. Mockups (Sugestão Visual)</h2>
            <p class="mb-6 text-gray-700">Esta seção oferece sugestões de como a identidade visual Dermater pode ser traduzida em aplicações práticas, como embalagens, plataformas de e-commerce e materiais científicos. Estas são diretrizes para inspirar a criação de peças que reflitam a sofisticação e o rigor científico da marca.</p>
            
            <div class="bg-cinza-azulado p-6 rounded-lg shadow space-y-4 text-gray-700">
                <h3 class="text-xl font-montserrat font-semibold text-azul-dermater mb-3">Aplicações Recomendadas:</h3>
                
                <div class="pb-4 mb-4">
                    <h4 class="font-montserrat font-semibold text-lg text-azul-tecnico mb-2">Embalagens de Produto:</h4>
                    <ul class="list-disc list-inside space-y-1 ml-4">
                        <li>Design clean com fundo branco predominante.</li>
                        <li>Logotipo em Azul Dermater (#356064) ou em dourado discreto (#C1B29F) para versões premium.</li>
                        <li>Uso de linhas finas ou divisores em dourado, verde natural ou cinza azulado para detalhes.</li>
                        <li>Elementos técnicos (como ativos ou benefícios) destacados em Azul Técnico (#4F99C0) para clareza.</li>
                    </ul>
                </div>

                <div class="pb-4 mb-4">
                    <h4 class="font-montserrat font-semibold text-lg text-azul-tecnico mb-2">E-commerce e Materiais Digitais:</h4>
                    <ul class="list-disc list-inside space-y-1 ml-4">
                        <li>Interface com grid claro e amplo uso de espaço em branco para respiro visual.</li>
                        <li>Botões e Call-to-Actions (CTAs) em Azul Técnico ou Verde Natural para guiar o usuário.</li>
                        <li>Área de conteúdo técnico em fundo Cinza Azulado Claro (#D9E1E2) para gerar contraste suave e destacar informações importantes.</li>
                    </ul>
                </div>

                <div>
                    <h4 class="font-montserrat font-semibold text-lg text-azul-tecnico mb-2">Material Técnico e Científico:</h4>
                    <ul class="list-disc list-inside space-y-1 ml-4">
                        <li>Cabeçalhos fortes em Montserrat Bold (700) na cor Azul Dermater.</li>
                        <li>Texto corrido em Open Sans Regular (400) em preto ou cinza escuro para máxima legibilidade.</li>
                        <li>Caixas de destaques técnicos em Cinza Azulado Claro ou Verde Calmante para organizar e realçar informações.</li>
                    </ul>
                </div>
            </div>
        </section>
        
        <section id="conclusao" class="content-section">
            <h2 class="text-3xl font-montserrat font-bold text-azul-dermater mb-6">11. Conclusão</h2>
            <p class="mb-6 text-gray-700">A identidade visual Dermater, conforme detalhada neste Brand Book, foi concebida para comunicar os valores essenciais da marca: ciência, performance, sofisticação e cuidado. Ao seguir estas diretrizes, garantimos uma apresentação coesa e impactante em todos os pontos de contato.</p>
            
            <div class="bg-cinza-azulado p-6 rounded-lg shadow">
                <h3 class="text-xl font-montserrat font-semibold text-azul-dermater mb-3">A Identidade Visual Proposta Entrega:</h3>
                <ul class="list-disc list-inside text-gray-700 space-y-1">
                    <li>Sofisticação sem ostentação.</li>
                    <li>Aspecto técnico com leveza e credibilidade.</li>
                    <li>Coerência com marcas internacionais de alta performance dermatológica.</li>
                    <li>Flexibilidade total para produtos, digital e materiais científicos.</li>
                </ul>
                <p class="mt-4 text-gray-700">A aplicação consistente destes elementos é fundamental para construir e fortalecer a percepção da marca Dermater no mercado.</p>
            </div>
        </section>

    </main>

    <script>
        document.addEventListener('DOMContentLoaded', function () {
            const navLinks = document.querySelectorAll('.nav-link');
            const contentSections = document.querySelectorAll('.content-section');
            const copyButtons = document.querySelectorAll('.copy-hex-btn');
            const copyFeedbackEl = document.getElementById('copy-feedback');

            function showSection(hash) {
                contentSections.forEach(section => {
                    if ('#' + section.id === hash) {
                        section.classList.add('active');
                    } else {
                        section.classList.remove('active');
                    }
                });
                navLinks.forEach(link => {
                    if (link.getAttribute('href') === hash) {
                        link.classList.add('active');
                    } else {
                        link.classList.remove('active');
                    }
                });
                 // Scroll to top of main content area
                document.querySelector('main').scrollTop = 0;
            }

            navLinks.forEach(link => {
                link.addEventListener('click', function (e) {
                    e.preventDefault();
                    const targetHash = this.getAttribute('href');
                    history.pushState(null, null, targetHash); // Update URL hash
                    showSection(targetHash);
                });
            });
            
            // Handle initial load based on hash or default to first section
            let initialHash = window.location.hash;
            if (!initialHash || !document.querySelector(initialHash)) {
                initialHash = navLinks[0].getAttribute('href');
            }
            showSection(initialHash);

            // Handle back/forward browser navigation
            window.addEventListener('popstate', function() {
                showSection(window.location.hash || navLinks[0].getAttribute('href'));
            });


            copyButtons.forEach(button => {
                button.addEventListener('click', function() {
                    const hexToCopy = this.dataset.hex;
                    navigator.clipboard.writeText(hexToCopy).then(() => {
                        copyFeedbackEl.classList.remove('opacity-0');
                        copyFeedbackEl.classList.add('opacity-100');
                        setTimeout(() => {
                            copyFeedbackEl.classList.remove('opacity-100');
                            copyFeedbackEl.classList.add('opacity-0');
                        }, 2000);
                    }).catch(err => {
                        console.error('Erro ao copiar HEX: ', err);
                        // Fallback for older browsers or if clipboard API fails
                        try {
                            const textArea = document.createElement("textarea");
                            textArea.value = hexToCopy;
                            textArea.style.position = "fixed"; //avoid scrolling to bottom
                            document.body.appendChild(textArea);
                            textArea.focus();
                            textArea.select();
                            document.execCommand('copy');
                            document.body.removeChild(textArea);
                            
                            copyFeedbackEl.textContent = 'Copiado (fallback)!';
                            copyFeedbackEl.classList.remove('opacity-0');
                            copyFeedbackEl.classList.add('opacity-100');
                            setTimeout(() => {
                                copyFeedbackEl.classList.remove('opacity-100');
                                copyFeedbackEl.classList.add('opacity-0');
                                copyFeedbackEl.textContent = 'Código copiado!'; // Reset message
                            }, 2000);

                        } catch (e) {
                            copyFeedbackEl.textContent = 'Falha ao copiar!';
                            copyFeedbackEl.style.backgroundColor = '#E53E3E'; // Red for error
                            copyFeedbackEl.classList.remove('opacity-0');
                            copyFeedbackEl.classList.add('opacity-100');
                             setTimeout(() => {
                                copyFeedbackEl.classList.remove('opacity-100');
                                copyFeedbackEl.classList.add('opacity-0');
                                copyFeedbackEl.textContent = 'Código copiado!'; // Reset message
                                copyFeedbackEl.style.backgroundColor = '#356064'; // Reset color
                            }, 2000);
                        }
                    });
                });
            });

            // Accordion for "Aplicações da Marca"
            const accordionButtons = document.querySelectorAll('.accordion-button');
            accordionButtons.forEach(button => {
                button.addEventListener('click', () => {
                    const content = button.nextElementSibling;
                    const isActive = button.classList.contains('active');

                    // Close all other accordions first
                    const container = button.closest('.space-y-4');
                    if (container) {
                        container.querySelectorAll('.accordion-button.active').forEach(activeButton => {
                            if (activeButton !== button) {
                                activeButton.classList.remove('active');
                                const activeContent = activeButton.nextElementSibling;
                                activeContent.style.maxHeight = null;
                                activeContent.classList.remove('p-4');
                                activeContent.classList.add('p-0');
                            }
                        });
                    }

                    if (isActive) {
                        // If currently active, close it
                        button.classList.remove('active');
                        content.style.maxHeight = null;
                        content.classList.remove('p-4');
                        content.classList.add('p-0');
                    } else {
                        // If not active, open it
                        button.classList.add('active');
                        // Apply padding first to ensure scrollHeight includes it
                        content.classList.remove('p-0');
                        content.classList.add('p-4');
                        content.style.maxHeight = content.scrollHeight + "px";
                    }
                });
                // Initial state setup for content-sections
                const content = button.nextElementSibling;
                if (!button.classList.contains('active')) {
                    content.classList.add('p-0');
                } else {
                     // Ensure initial active state opens correctly with padding
                     content.classList.add('p-4');
                     content.style.maxHeight = content.scrollHeight + "px";
                }
            });
            
            // Color Palette Chart
            const ctx = document.getElementById('colorPaletteChart').getContext('2d');
            new Chart(ctx, {
                type: 'pie',
                data: {
                    labels: ['Cores Principais/Estruturais', 'Cores de Detalhe/Acento', 'Cores Funcionais/Técnicas'],
                    datasets: [{
                        label: 'Distribuição Conceitual da Paleta',
                        data: [2, 3, 2], // Ex: Azul Dermater, Branco (Principais); Cinza Azulado, Dourado, Verde Calmante (Detalhe); Azul Técnico, Verde Natural (Funcional)
                        backgroundColor: [
                            '#356064', // Azul Dermater
                            '#D9E1E2', // Cinza Azulado
                            '#4F99C0', // Azul Técnico
                            // '#95BFB9', // Verde Calmante (Could be added if data array increased)
                            // '#7CA89A', // Verde Natural
                            // '#C1B29F'  // Dourado Neutro
                        ],
                        borderColor: [
                            '#FFFFFF',
                            '#FFFFFF',
                            '#FFFFFF'
                        ],
                        borderWidth: 2
                    }]
                },
                options: {
                    responsive: true,
                    maintainAspectRatio: false,
                    plugins: {
                        legend: {
                            position: 'bottom',
                            labels: {
                                color: '#333', // Darker text for legend
                                font: {
                                    family: "'Open Sans', sans-serif",
                                    size: 12
                                }
                            }
                        },
                        tooltip: {
                            callbacks: {
                                label: function(context) {
                                    let label = context.label || '';
                                    if (label) {
                                        label += ': ';
                                    }
                                    if (context.parsed !== null) {
                                        label += context.parsed;
                                    }
                                    return label + ' cores';
                                }
                            },
                            bodyFont: {
                                family: "'Open Sans', sans-serif"
                            },
                            titleFont: {
                                family: "'Montserrat', sans-serif"
                            }
                        }
                    }
                }
            });

        });
    </script>
</body>
</html>
