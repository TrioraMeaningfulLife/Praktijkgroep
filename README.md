<!DOCTYPE html>
<html lang="nl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Restaurant, serre en buitendienst - Triora</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap');
        
        :root {
            --triora-blue: #003255;
            --triora-orange: #E66E19;
            --triora-green: #82BC00;
            --triora-light-blue: #F0F4F7;
            --triora-grey: #64748b;
        }

        body {
            font-family: 'Inter', sans-serif;
            background-color: #fcfcfc;
            color: var(--triora-blue);
        }

        .section-tab {
            border-bottom: 3px solid transparent;
            color: var(--triora-blue);
            transition: all 0.3s ease;
        }

        .section-tab.active {
            border-bottom-color: var(--triora-orange);
            color: var(--triora-orange);
            font-weight: 700;
        }

        .category-header {
            border-left: 4px solid var(--triora-blue);
        }

        .bg-triora-blue { background-color: var(--triora-blue); }
        .text-triora-blue { color: var(--triora-blue); }
        .border-triora-blue { border-color: var(--triora-blue); }
        
        .bg-triora-orange { background-color: var(--triora-orange); }
        .text-triora-orange { color: var(--triora-orange); }
        
        .bg-triora-green { background-color: var(--triora-green); }
        .text-triora-green { color: var(--triora-green); }

        .card-shadow {
            box-shadow: 0 4px 20px rgba(0, 50, 85, 0.08);
        }

        .animate-fade-in {
            animation: fadeIn 0.4s ease-out forwards;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body class="p-4 md:p-8">
    <div class="max-w-4xl mx-auto">
        <!-- Header -->
        <header class="text-center mb-10 border-b border-slate-100 pb-8">
            <div class="mb-4 inline-block px-4 py-1 rounded border border-triora-blue text-triora-blue font-bold tracking-widest text-xs uppercase">
                Triora - Parnassia Groep
            </div>
            <!-- Gevraagde Titel -->
            <h1 class="text-3xl md:text-5xl font-extrabold text-triora-blue mb-2">Restaurant, serre en buitendienst</h1>
            <p class="text-lg text-slate-500 font-medium italic">Praktijkgroep 2 - Dagelijkse werkzaamheden</p>
            
            <div class="mt-8 flex justify-center gap-3 flex-wrap">
                <span class="bg-triora-blue text-white px-4 py-1.5 rounded-full text-xs font-bold uppercase tracking-wider shadow-sm"><i class="fas fa-utensils mr-2"></i>Restaurant</span>
                <span class="bg-triora-green text-white px-4 py-1.5 rounded-full text-xs font-bold uppercase tracking-wider shadow-sm"><i class="fas fa-sun mr-2"></i>Serre & Buiten</span>
                <span class="bg-triora-orange text-white px-4 py-1.5 rounded-full text-xs font-bold uppercase tracking-wider shadow-sm"><i class="fas fa-check-double mr-2"></i>HACCP</span>
            </div>
        </header>

        <!-- Navigation Tabs -->
        <div class="flex flex-wrap justify-center gap-4 md:gap-8 mb-10 border-b border-slate-200" id="tab-container">
            <button onclick="showSection('ontbijt')" class="section-tab active px-2 py-4 text-sm uppercase tracking-widest font-bold focus:outline-none">
                Ontbijt
            </button>
            <button onclick="showSection('lunch')" class="section-tab px-2 py-4 text-sm uppercase tracking-widest font-bold focus:outline-none">
                Lunch
            </button>
            <button onclick="showSection('diner')" class="section-tab px-2 py-4 text-sm uppercase tracking-widest font-bold focus:outline-none">
                Diner
            </button>
            <button onclick="showSection('buiten')" class="section-tab px-2 py-4 text-sm uppercase tracking-widest font-bold focus:outline-none">
                Buitendienst
            </button>
            <button onclick="showSection('maandag')" class="section-tab px-2 py-4 text-sm uppercase tracking-widest font-bold focus:outline-none">
                Maandag
            </button>
        </div>

        <!-- Content Sections -->
        <div id="content-area" class="min-h-[400px]">
            
            <!-- Ontbijt Section -->
            <div id="ontbijt" class="content-section animate-fade-in">
                <div class="grid md:grid-cols-2 gap-8">
                    <div class="bg-white p-8 rounded-2xl card-shadow border-t-4 border-triora-blue">
                        <h3 class="category-header text-lg font-bold text-triora-blue mb-6 pl-4 uppercase tracking-wider">Vóór het ontbijt <span class="text-triora-orange ml-2">07:45</span></h3>
                        <ul class="space-y-4">
                            <li class="flex items-start font-medium text-triora-blue"><i class="fas fa-check-circle text-triora-green mt-1 mr-4"></i> Zuivel en vleeswaren op de tafels zetten.</li>
                            <li class="flex items-start text-slate-500 text-sm italic"><i class="fas fa-info-circle mt-1 mr-4"></i> Controleer de serre op netheid.</li>
                        </ul>
                    </div>
                    <div class="bg-white p-8 rounded-2xl card-shadow border-t-4 border-slate-200">
                        <h3 class="category-header text-lg font-bold text-triora-blue mb-6 pl-4 uppercase tracking-wider">Na het ontbijt</h3>
                        <ul class="space-y-4 text-slate-600">
                            <li class="flex items-start"><i class="fas fa-sink text-triora-blue mt-1 mr-4 opacity-70"></i> Spoelkeuken: restjes weggooien en afwassen.</li>
                            <li class="flex items-start"><i class="fas fa-snowflake text-triora-blue mt-1 mr-4 opacity-70"></i> Gekoelde producten direct terugzetten.</li>
                            <li class="flex items-start"><i class="fas fa-broom text-triora-blue mt-1 mr-4 opacity-70"></i> Tafels schoonmaken en opdekken voor lunch.</li>
                            <li class="flex items-start"><i class="fas fa-utensils text-triora-blue mt-1 mr-4 opacity-70"></i> Servetten en bestek klaarleggen.</li>
                        </ul>
                    </div>
                </div>
            </div>

            <!-- Lunch Section -->
            <div id="lunch" class="content-section hidden animate-fade-in">
                <div class="grid md:grid-cols-2 gap-8">
                    <div class="bg-white p-8 rounded-2xl card-shadow border-t-4 border-triora-blue">
                        <h3 class="category-header text-lg font-bold text-triora-blue mb-6 pl-4 uppercase tracking-wider">Vóór de lunch <span class="text-triora-orange ml-2">12:00</span></h3>
                        <ul class="space-y-4">
                            <li class="flex items-start font-medium text-triora-blue"><i class="fas fa-check-circle text-triora-green mt-1 mr-4"></i> Zuivel en vleeswaren op de tafels zetten.</li>
                        </ul>
                    </div>
                    <div class="bg-white p-8 rounded-2xl card-shadow border-t-4 border-slate-200">
                        <h3 class="category-header text-lg font-bold text-triora-blue mb-6 pl-4 uppercase tracking-wider">Na de lunch</h3>
                        <ul class="space-y-4 text-slate-600">
                            <li class="flex items-start"><i class="fas fa-sink text-triora-blue mt-1 mr-4 opacity-70"></i> Spoelkeuken netjes achterlaten na afwas.</li>
                            <li class="flex items-start"><i class="fas fa-tint text-triora-blue mt-1 mr-4 opacity-70"></i> Waterkannen vullen en koud zetten voor diner.</li>
                            <li class="flex items-start"><i class="fas fa-snowflake text-triora-blue mt-1 mr-4 opacity-70"></i> Gekoelde producten direct terugzetten.</li>
                            <li class="flex items-start"><i class="fas fa-broom text-triora-blue mt-1 mr-4 opacity-70"></i> Tafels schoonmaken en opdekken voor diner.</li>
                        </ul>
                    </div>
                </div>
            </div>

            <!-- Diner Section -->
            <div id="diner" class="content-section hidden animate-fade-in">
                <div class="grid md:grid-cols-2 gap-8">
                    <div class="bg-white p-8 rounded-2xl card-shadow border-t-4 border-triora-blue">
                        <h3 class="category-header text-lg font-bold text-triora-blue mb-6 pl-4 uppercase tracking-wider">Vóór het diner <span class="text-triora-orange ml-2">17:20</span></h3>
                        <ul class="space-y-4">
                            <li class="flex items-start font-medium text-triora-blue"><i class="fas fa-wine-glass text-triora-green mt-1 mr-4"></i> Waterkannen, vla, peper en zout op tafel.</li>
                        </ul>
                    </div>
                    <div class="bg-white p-8 rounded-2xl card-shadow border-t-4 border-triora-orange">
                        <h3 class="category-header text-lg font-bold text-triora-orange mb-6 pl-4 uppercase tracking-wider border-triora-orange">Einde Dag & Sluiting</h3>
                        <ul class="space-y-4 text-slate-600">
                            <li class="flex items-start font-bold text-triora-blue"><i class="fas fa-clipboard-check text-triora-orange mt-1 mr-4"></i> HACCP-controle zuivel, fris & vleeswaren.</li>
                            <li class="flex items-start"><i class="fas fa-broom text-triora-blue mt-1 mr-4 opacity-70"></i> Vloer (incl. serre) stofzuigen en dweilen.</li>
                            <li class="flex items-start"><i class="fas fa-trash-alt text-triora-blue mt-1 mr-4 opacity-70"></i> Vuilnisbakken legen en nieuwe zakken.</li>
                            <li class="flex items-start"><i class="fas fa-table text-triora-blue mt-1 mr-4 opacity-70"></i> Tafels opdekken voor ontbijt (incl. zoet beleg).</li>
                            <li class="flex items-start"><i class="fas fa-spray-can text-triora-blue mt-1 mr-4 opacity-70"></i> Buitenzijde koelkast en handvat reinigen.</li>
                        </ul>
                    </div>
                </div>
            </div>

            <!-- Buitendienst Section -->
            <div id="buiten" class="content-section hidden animate-fade-in">
                <div class="bg-white p-8 rounded-2xl card-shadow border-t-4 border-triora-green">
                    <h3 class="category-header text-xl font-bold text-triora-green mb-8 pl-4 uppercase tracking-widest border-triora-green">Terreinonderhoud</h3>
                    <div class="grid md:grid-cols-2 gap-12">
                        <div>
                            <h4 class="font-bold text-triora-blue mb-4 flex items-center tracking-wide uppercase text-xs">
                                <span class="w-8 h-8 rounded-full bg-triora-green text-white flex items-center justify-center mr-3">1</span> 
                                Netheid Omgeving
                            </h4>
                            <ul class="space-y-4 text-slate-600 ml-1">
                                <li class="flex items-start"><i class="fas fa-broom text-triora-green mt-1 mr-4"></i> Terras (bij de serre) vegen en meubilair ordenen.</li>
                                <li class="flex items-start"><i class="fas fa-trash text-triora-green mt-1 mr-4"></i> Zwerfvuil rondom gebouw & parkeerplaatsen.</li>
                                <li class="flex items-start"><i class="fas fa-dumpster text-triora-green mt-1 mr-4"></i> Buiten vuilnisbakken legen.</li>
                            </ul>
                        </div>
                        <div>
                            <h4 class="font-bold text-triora-blue mb-4 flex items-center tracking-wide uppercase text-xs">
                                <span class="w-8 h-8 rounded-full bg-triora-blue text-white flex items-center justify-center mr-3">2</span> 
                                Containers & Seizoen
                            </h4>
                            <ul class="space-y-4 text-slate-600 ml-1">
                                <li class="flex items-start"><i class="fas fa-snowflake text-triora-blue mt-1 mr-4 opacity-70"></i> Bladeren/sneeuw vrijmaken bij entree.</li>
                                <li class="flex items-start font-semibold"><i class="fas fa-truck text-triora-orange mt-1 mr-4"></i> Ma-avond: Grijze containers voorzetten.</li>
                                <li class="flex items-start font-semibold"><i class="fas fa-truck text-triora-blue mt-1 mr-4"></i> Di-avond: Blauwe containers voorzetten.</li>
                                <li class="flex items-start"><i class="fas fa-undo text-slate-400 mt-1 mr-4"></i> Lege containers direct terugzetten na lediging.</li>
                            </ul>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Maandag Section -->
            <div id="maandag" class="content-section hidden animate-fade-in">
                <div class="bg-triora-light-blue p-10 rounded-2xl border border-slate-200">
                    <div class="flex items-center mb-8">
                        <div class="bg-triora-blue text-white p-4 rounded-xl mr-6 shadow-lg">
                            <i class="fas fa-calendar-check fa-2x"></i>
                        </div>
                        <div>
                            <h3 class="text-2xl font-bold text-triora-blue">Schoonmaakfocus Maandag</h3>
                            <p class="text-slate-500 font-medium">Extra hygiëne voor restaurant en serre</p>
                        </div>
                    </div>
                    <div class="grid md:grid-cols-3 gap-6">
                        <div class="bg-white p-6 rounded-xl shadow-sm text-center border-b-4 border-triora-blue">
                            <i class="fas fa-tray text-triora-blue text-3xl mb-4"></i>
                            <p class="font-bold text-triora-blue mb-2 uppercase text-xs tracking-wider">Dienbladen</p>
                            <p class="text-sm text-slate-500">Alle dienbladen met zoet beleg grondig afwassen.</p>
                        </div>
                        <div class="bg-white p-6 rounded-xl shadow-sm text-center border-b-4 border-triora-blue">
                            <i class="fas fa-box-open text-triora-blue text-3xl mb-4"></i>
                            <p class="font-bold text-triora-blue mb-2 uppercase text-xs tracking-wider">Plastic Bakken</p>
                            <p class="text-sm text-slate-500">Alle belegbakken volledig reinigen in de spoelkeuken.</p>
                        </div>
                        <div class="bg-white p-6 rounded-xl shadow-sm text-center border-b-4 border-triora-orange">
                            <i class="fas fa-soap text-triora-orange text-3xl mb-4"></i>
                            <p class="font-bold text-triora-orange mb-2 uppercase text-xs tracking-wider">Grote Koelkast</p>
                            <p class="text-sm text-slate-500">Binnenkant volledig soppen en controleren.</p>
                        </div>
                    </div>
                </div>
            </div>

        </div>

        <!-- Footer -->
        <footer class="mt-16 text-center">
            <div class="p-8 bg-white border border-slate-200 rounded-2xl card-shadow inline-block w-full">
                <div class="flex flex-col md:flex-row items-center justify-center gap-4">
                    <i class="fas fa-handshake text-triora-orange text-2xl"></i>
                    <p class="text-triora-blue text-lg">
                        <strong>Samenwerking:</strong> Breng je eigen servies weg en help de spoelkeuken schoon te houden.
                    </p>
                </div>
            </div>
            <p class="mt-8 text-slate-400 text-xs uppercase tracking-widest font-bold">
                Triora &copy; 2025 | Meaningfull Life
        </footer>
    </div>

    <script>
        function showSection(id) {
            document.querySelectorAll('.content-section').forEach(section => {
                section.classList.add('hidden');
            });
            
            const target = document.getElementById(id);
            target.classList.remove('hidden');
            
            document.querySelectorAll('.section-tab').forEach(tab => {
                tab.classList.remove('active');
            });
            event.currentTarget.classList.add('active');
        }
    </script>
</body>
</html>
