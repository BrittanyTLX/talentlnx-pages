<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The TalentLNX Journey to ARETÉ</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700;900&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f8fafc;
        }
        .chart-container {
            position: relative;
            width: 100%;
            max-width: 500px;
            margin-left: auto;
            margin-right: auto;
            height: 350px;
            max-height: 450px;
        }
        @media (min-width: 768px) {
            .chart-container {
                height: 400px;
            }
        }
        .stat-card {
            background-color: white;
            border-radius: 0.75rem;
            padding: 1.5rem;
            box-shadow: 0 4px 6px -1px rgb(0 0 0 / 0.1), 0 2px 4px -2px rgb(0 0 0 / 0.1);
            text-align: center;
        }
        .lifecycle-step {
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
            padding: 1rem;
            background-color: white;
            border-radius: 0.5rem;
            box-shadow: 0 1px 3px 0 rgb(0 0 0 / 0.1), 0 1px 2px -1px rgb(0 0 0 / 0.1);
            border-left: 4px solid;
            transition: transform 0.2s ease-in-out, box-shadow 0.2s ease-in-out;
        }
        .lifecycle-step:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 15px -3px rgb(0 0 0 / 0.1), 0 4px 6px -2px rgb(0 0 0 / 0.1);
        }
        .lifecycle-number {
            font-size: 1.5rem;
            font-weight: 900;
            width: 50px;
            height: 50px;
            border-radius: 9999px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            margin-bottom: 0.75rem;
        }
        .gemini-input {
            width: 100%;
            padding: 0.75rem;
            border: 1px solid #d1d5db;
            border-radius: 0.5rem;
            margin-bottom: 1rem;
        }
        .gemini-button {
            width: 100%;
            padding: 0.75rem;
            border-radius: 0.5rem;
            background-color: #073B4C;
            color: white;
            font-weight: bold;
            transition: background-color 0.2s;
        }
        .gemini-button:hover {
            background-color: #118AB2;
        }
        .gemini-output {
            width: 100%;
            min-height: 150px;
            padding: 0.75rem;
            border: 1px solid #e5e7eb;
            border-radius: 0.5rem;
            background-color: #f9fafb;
            white-space: pre-wrap;
            word-wrap: break-word;
        }
    </style>
</head>
<body class="text-gray-800">

    <!-- Chosen Palette: Energetic & Playful -->
    <!-- Application Structure Plan: The SPA is designed as a narrative journey. It starts with a high-level philosophical hook (ARETÉ), then grounds the user in core principles (5 P's) and market focus (Verticals). It moves to tactical execution, visualizing the sales lifecycle. A new interactive section, "AI-Powered Partner Tools," has been added to provide practical, LLM-driven assistance for outreach and objection handling, directly applying the training concepts. The app concludes with market data to reinforce the 'why' behind the strategy. This flow (Philosophy -> Strategy -> Execution -> AI Tools -> Market Context) was chosen to make the training material digestible and immediately applicable. -->
    <!-- Visualization & Content Choices: 
        - ARETÉ Philosophy -> Goal: Inform -> Viz: Large, bold text. Method: HTML/Tailwind. No SVG/Mermaid.
        - 5 P's Principle -> Goal: Compare/Organize -> Viz: Radar Chart. Method: Chart.js/Canvas. No SVG/Mermaid.
        - Core Verticals -> Goal: Compare/Composition -> Viz: Donut Chart. Method: Chart.js/Canvas. No SVG/Mermaid.
        - Engagement Lifecycle -> Goal: Organize/Process -> Viz: Multi-step styled card flow. Method: HTML/Tailwind. No SVG/Mermaid.
        - AI Outreach Generator -> Goal: Inform/Create -> Interaction: Form input. Justification: Provides a practical tool to apply training on outreach. Method: Gemini API Call. No SVG/Mermaid.
        - AI Role-Play Coach -> Goal: Inform/Organize -> Interaction: Dropdown selection. Justification: Reinforces objection handling training in an interactive way. Method: Gemini API Call. No SVG/Mermaid.
        - Gig Economy Growth -> Goal: Change -> Viz: Line Chart. Method: Chart.js/Canvas. No SVG/Mermaid.
        - Staffing Model Use Cases -> Goal: Compare -> Viz: Horizontal Bar Chart. Method: Chart.js/Canvas. No SVG/Mermaid.
    -->
    <!-- CONFIRMATION: NO SVG graphics used. NO Mermaid JS used. -->

    <header class="bg-[#073B4C] text-white text-center py-16 px-4">
        <h1 class="text-4xl md:text-6xl font-black tracking-tight">The TalentLNX Journey to <span class="text-[#06D6A0]">ARETÉ</span></h1>
        <p class="mt-4 text-lg md:text-xl max-w-3xl mx-auto text-gray-300">An interactive guide to our core philosophy of excellence, the strategic markets we serve, and the proven process that transforms our partners into elite talent advisors.</p>
    </header>

    <main class="container mx-auto p-4 md:p-8">

        <section id="philosophy" class="mb-20">
            <h2 class="text-3xl font-bold text-center mb-4 text-[#073B4C]">Our Foundational Principles</h2>
            <p class="text-center text-gray-600 max-w-3xl mx-auto mb-12">Success at TalentLNX is built on a foundation of strategic preparation and a commitment to excellence. We call this our "ARETÉ" mindset. The "5 P's" framework is how we put that philosophy into practice every day, ensuring every action is thoughtful, informed, and impactful.</p>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-8 items-center">
                <div class="bg-white p-6 rounded-lg shadow-lg">
                    <h3 class="text-2xl font-bold text-center mb-4 text-[#073B4C]">The 5 P's of Peak Performance</h3>
                    <p class="text-center text-gray-600 mb-4">"Proper Preparation Prevents Poor Performance." This radar chart visualizes the five interconnected pillars of readiness. A successful partner demonstrates strength across all areas to deliver consistent, high-quality results.</p>
                    <div class="chart-container">
                        <canvas id="fivePsChart"></canvas>
                    </div>
                </div>
                <div class="bg-white p-6 rounded-lg shadow-lg">
                    <h3 class="text-2xl font-bold text-center mb-4 text-[#073B4C]">Our Core Verticals of Expertise</h3>
                    <p class="text-center text-gray-600 mb-4">We thrive by being specialists, not generalists. Our deep focus on four high-demand, high-impact sectors allows us to provide unparalleled market intelligence and talent access to our clients.</p>
                    <div class="chart-container">
                        <canvas id="verticalsChart"></canvas>
                    </div>
                </div>
            </div>
        </section>

        <section id="lifecycle" class="mb-20">
            <h2 class="text-3xl font-bold text-center mb-4 text-[#073B4C]">The Engagement Lifecycle</h2>
            <p class="text-center text-gray-600 max-w-3xl mx-auto mb-12">Our success follows a systematic, repeatable process that guides every client and candidate interaction from initial contact to long-term partnership. This ensures quality, consistency, and a superior experience for everyone involved.</p>
            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-6">
                <div class="lifecycle-step border-[#FF6B6B]">
                    <div class="lifecycle-number bg-[#FF6B6B]">1</div>
                    <h4 class="font-bold text-lg">Prospecting & Discovery</h4>
                    <p class="text-gray-600 text-sm">Identify high-fit clients using market signals and data. Conduct deep discovery calls to uncover true pain points, not just surface-level needs.</p>
                </div>
                <div class="lifecycle-step border-[#FFD166]">
                    <div class="lifecycle-number bg-[#FFD166]">2</div>
                    <h4 class="font-bold text-lg">Qualification & Intake</h4>
                    <p class="text-gray-600 text-sm">Translate discovery insights into a qualified job order. Define must-haves, confirm budget, and create the blueprint for a successful search.</p>
                </div>
                <div class="lifecycle-step border-[#06D6A0]">
                    <div class="lifecycle-number bg-[#06D6A0]">3</div>
                    <h4 class="font-bold text-lg">Sourcing & Submittal</h4>
                    <p class="text-gray-600 text-sm">Leverage our specialized talent network to find and rigorously screen candidates. Present a curated shortlist of top-tier professionals to the client.</p>
                </div>
                <div class="lifecycle-step border-[#118AB2]">
                    <div class="lifecycle-number bg-[#118AB2]">4</div>
                    <h4 class="font-bold text-lg">Interview & Feedback</h4>
                    <p class="text-gray-600 text-sm">Coordinate the entire interview process, prepare candidates for success, and manage the critical feedback loop to keep momentum.</p>
                </div>
                <div class="lifecycle-step border-[#073B4C] sm:col-span-2 lg:col-span-1 xl:col-span-2">
                    <div class="lifecycle-number bg-[#073B4C]">5</div>
                    <h4 class="font-bold text-lg">Offer & Closing</h4>
                    <p class="text-gray-600 text-sm">Facilitate the offer stage with clarity and confidence, managing negotiations and guiding both client and candidate to a successful close.</p>
                </div>
                 <div class="lifecycle-step border-[#FF6B6B] xl:col-span-2">
                    <div class="lifecycle-number bg-[#FF6B6B]">6</div>
                    <h4 class="font-bold text-lg">Post-Placement & Partnership</h4>
                    <p class="text-gray-600 text-sm">The relationship doesn't end at the hire. We conduct regular check-ins to ensure success, uncover new opportunities, and build lasting loyalty.</p>
                </div>
            </div>
        </section>

        <section id="ai-tools" class="mb-20">
            <h2 class="text-3xl font-bold text-center mb-4 text-[#073B4C]">✨ AI-Powered Partner Tools</h2>
            <p class="text-center text-gray-600 max-w-3xl mx-auto mb-12">Apply your training with practical, AI-driven tools designed to accelerate your workflow and enhance your strategic communication, powered by the Gemini API.</p>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                <div class="bg-white p-6 rounded-lg shadow-lg">
                    <h3 class="text-2xl font-bold text-center mb-4">AI Outreach Message Generator</h3>
                    <p class="text-gray-600 mb-6 text-center">Craft the perfect outreach email. Input a few details about a candidate, and our AI will generate a personalized, value-driven message based on TalentLNX best practices.</p>
                    <input type="text" id="outreachRole" class="gemini-input" placeholder="e.g., Clinical Pharmacist">
                    <input type="text" id="outreachSkill" class="gemini-input" placeholder="e.g., Experience with oncology medication">
                    <input type="text" id="outreachSignal" class="gemini-input" placeholder="e.g., Just earned a new certification">
                    <button id="generateOutreachBtn" class="gemini-button">Generate Message ✨</button>
                    <textarea id="outreachOutput" class="gemini-output mt-4" readonly placeholder="Your generated outreach message will appear here..."></textarea>
                    <button id="copyOutreachBtn" class="w-full mt-2 p-2 text-sm bg-gray-200 text-gray-700 font-semibold rounded-lg hover:bg-gray-300">Copy to Clipboard</button>
                </div>
                <div class="bg-white p-6 rounded-lg shadow-lg">
                    <h3 class="text-2xl font-bold text-center mb-4">Strategic Role-Play Coach</h3>
                    <p class="text-gray-600 mb-6 text-center">Sharpen your objection-handling skills. Select a common client objection, and our AI coach will provide a strategic response aligned with the ARETÉ mindset.</p>
                    <select id="roleplayScenario" class="gemini-input">
                        <option value="price">"Your price is too high."</option>
                        <option value="vendor">"We already have a preferred vendor."</option>
                        <option value="inhouse">"We handle all our recruiting in-house."</option>
                        <option value="not_hiring">"We're not hiring right now."</option>
                    </select>
                    <button id="getCoachingBtn" class="gemini-button">Get Coaching ✨</button>
                    <div id="roleplayOutput" class="gemini-output mt-4 text-left"><p class="text-gray-500">Your AI-powered coaching response will appear here...</p></div>
                </div>
            </div>
        </section>

        <section id="market-insights" class="mb-16">
            <h2 class="text-3xl font-bold text-center mb-4 text-[#073B4C]">Key Market & Performance Insights</h2>
            <p class="text-center text-gray-600 max-w-3xl mx-auto mb-12">Our strategy is informed by real-world data. Understanding these market dynamics and performance drivers is crucial for consulting with clients and delivering effective workforce solutions.</p>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                <div class="bg-white p-6 rounded-lg shadow-lg">
                    <h3 class="text-2xl font-bold text-center mb-4 text-[#073B4C]">Explosive Growth of the Gig Economy</h3>
                    <p class="text-center text-gray-600 mb-4">The shift towards a contingent workforce is a long-term, strategic trend. This data highlights the massive growth in the gig economy, reinforcing the value of flexible staffing solutions for our clients.</p>
                    <div class="chart-container">
                        <canvas id="gigEconomyChart"></canvas>
                    </div>
                </div>
                <div class="bg-white p-6 rounded-lg shadow-lg">
                    <h3 class="text-2xl font-bold text-center mb-4 text-[#073B4C]">Matching Staffing Models to Client Needs</h3>
                    <p class="text-center text-gray-600 mb-4">Different challenges require different solutions. This chart shows common client needs and the most effective TalentLNX staffing model to address them, guiding our consultative approach.</p>
                    <div class="chart-container">
                        <canvas id="staffingModelsChart"></canvas>
                    </div>
                </div>
            </div>
        </section>

    </main>

    <footer class="bg-[#073B4C] text-white text-center py-12 px-4">
        <h2 class="text-2xl font-bold">Become a Strategic Partner</h2>
        <p class="mt-2 max-w-2xl mx-auto text-gray-300">By internalizing these principles and mastering our process, you become more than a vendor; you become an indispensable advisor, driving success for your clients and empowering talent to embrace new possibilities.</p>
    </footer>

    <script>
        const tooltipConfig = {
            plugins: {
                tooltip: {
                    callbacks: {
                        title: function(tooltipItems) {
                            const item = tooltipItems[0];
                            let label = item.chart.data.labels[item.dataIndex];
                            if (Array.isArray(label)) {
                              return label.join(' ');
                            } else {
                              return label;
                            }
                        }
                    }
                }
            }
        };

        const wrapLabel = (label) => {
            const maxLength = 16;
            if (label.length <= maxLength) {
                return label;
            }
            const words = label.split(' ');
            const lines = [];
            let currentLine = '';
            words.forEach(word => {
                if ((currentLine + word).length > maxLength) {
                    lines.push(currentLine.trim());
                    currentLine = '';
                }
                currentLine += word + ' ';
            });
            lines.push(currentLine.trim());
            return lines;
        };

        const fivePsData = {
            labels: [
                ['Profound Market', 'Intelligence'], 
                ['Operational', 'Readiness'], 
                ['Superior Candidate', 'Matching'], 
                ['Proactive', 'Problem-Solving'], 
                ['Professional', 'Polish']
            ],
            datasets: [{
                label: 'ARETÉ Readiness',
                data: [9, 8, 9, 8, 9],
                fill: true,
                backgroundColor: 'rgba(6, 214, 160, 0.2)',
                borderColor: '#06D6A0',
                pointBackgroundColor: '#06D6A0',
                pointBorderColor: '#fff',
                pointHoverBackgroundColor: '#fff',
                pointHoverBorderColor: '#06D6A0'
            }]
        };

        const fivePsCtx = document.getElementById('fivePsChart').getContext('2d');
        new Chart(fivePsCtx, {
            type: 'radar',
            data: fivePsData,
            options: {
                responsive: true,
                maintainAspectRatio: false,
                ...tooltipConfig,
                scales: {
                    r: {
                        angleLines: { color: 'rgba(7, 59, 76, 0.2)' },
                        grid: { color: 'rgba(7, 59, 76, 0.2)' },
                        pointLabels: { font: { size: 12, weight: 'bold' }, color: '#073B4C' },
                        ticks: { backdropColor: 'rgba(255, 255, 255, 0.75)', color: '#073B4C', stepSize: 2 },
                        suggestedMin: 0,
                        suggestedMax: 10
                    }
                },
                plugins: { ...tooltipConfig.plugins, legend: { display: false } }
            }
        });

        const verticalsData = {
            labels: ['Healthcare', 'Specialty Pharmacy', 'Shared Services', 'Call Centers'],
            datasets: [{
                label: 'Core Verticals',
                data: [35, 30, 20, 15],
                backgroundColor: ['#FF6B6B', '#FFD166', '#06D6A0', '#118AB2'],
                borderColor: '#f8fafc',
                borderWidth: 4,
                hoverOffset: 8
            }]
        };

        const verticalsCtx = document.getElementById('verticalsChart').getContext('2d');
        new Chart(verticalsCtx, {
            type: 'doughnut',
            data: verticalsData,
            options: {
                responsive: true,
                maintainAspectRatio: false,
                cutout: '60%',
                ...tooltipConfig,
                plugins: { ...tooltipConfig.plugins, legend: { position: 'bottom' } }
            }
        });

        const gigEconomyData = {
            labels: ['2025', '2027', '2029', '2031', '2033'],
            datasets: [{
                label: 'Gig Economy Market Value ($B)',
                data: [646.77, 919.3, 1305.7, 1854.4, 2100],
                fill: true,
                borderColor: '#118AB2',
                backgroundColor: 'rgba(17, 138, 178, 0.1)',
                tension: 0.4,
                pointBackgroundColor: '#118AB2',
                pointRadius: 5,
                pointHoverRadius: 7
            }]
        };

        const gigEconomyCtx = document.getElementById('gigEconomyChart').getContext('2d');
        new Chart(gigEconomyCtx, {
            type: 'line',
            data: gigEconomyData,
            options: {
                responsive: true,
                maintainAspectRatio: false,
                ...tooltipConfig,
                scales: { y: { beginAtZero: false, ticks: { callback: value => `$${value}B` } } },
                plugins: { ...tooltipConfig.plugins, legend: { display: false } }
            }
        });

        const staffingModelsData = {
            labels: [
                'Cover Short-Term Gaps',
                'Access Niche Expertise',
                'Evaluate Fit (Try/Buy)',
                'Build Core Team'
            ].map(wrapLabel),
            datasets: [{
                label: 'Effectiveness Score',
                data: [9, 7, 8, 9.5],
                backgroundColor: ['#FF6B6B', '#FFD166', '#06D6A0', '#118AB2'],
                borderRadius: 4
            }]
        };

        const staffingModelsCtx = document.getElementById('staffingModelsChart').getContext('2d');
        new Chart(staffingModelsCtx, {
            type: 'bar',
            data: staffingModelsData,
            options: {
                indexAxis: 'y',
                responsive: true,
                maintainAspectRatio: false,
                ...tooltipConfig,
                scales: { x: { beginAtZero: true, suggestedMax: 10, title: { display: true, text: 'Model Suitability' } } },
                plugins: { ...tooltipConfig.plugins, legend: { display: false } }
            }
        });

        const generateOutreachBtn = document.getElementById('generateOutreachBtn');
        const outreachOutput = document.getElementById('outreachOutput');
        const copyOutreachBtn = document.getElementById('copyOutreachBtn');
        const getCoachingBtn = document.getElementById('getCoachingBtn');
        const roleplayOutput = document.getElementById('roleplayOutput');

        const callGemini = async (prompt, outputElement, buttonElement) => {
            outputElement.textContent = 'Generating...';
            buttonElement.disabled = true;
            
            let chatHistory = [{ role: "user", parts: [{ text: prompt }] }];
            const payload = { contents: chatHistory };
            const apiKey = "";
            const apiUrl = `https://generativelanguage.googleapis.com/v1beta/models/gemini-2.5-flash-preview-05-20:generateContent?key=${apiKey}`;

            try {
                const response = await fetch(apiUrl, {
                    method: 'POST',
                    headers: { 'Content-Type': 'application/json' },
                    body: JSON.stringify(payload)
                });
                const result = await response.json();
                if (result.candidates && result.candidates.length > 0 &&
                    result.candidates[0].content && result.candidates[0].content.parts &&
                    result.candidates[0].content.parts.length > 0) {
                    const text = result.candidates[0].content.parts[0].text;
                    if (outputElement.tagName === 'TEXTAREA') {
                        outputElement.value = text;
                    } else {
                        outputElement.innerHTML = text.replace(/\*\*(.*?)\*\*/g, '<strong>$1</strong>').replace(/\n/g, '<br>');
                    }
                } else {
                    outputElement.textContent = 'Sorry, something went wrong. Please try again.';
                }
            } catch (error) {
                outputElement.textContent = 'Error calling the AI. Please check your connection and try again.';
            } finally {
                buttonElement.disabled = false;
            }
        };

        generateOutreachBtn.addEventListener('click', () => {
            const role = document.getElementById('outreachRole').value;
            const skill = document.getElementById('outreachSkill').value;
            const signal = document.getElementById('outreachSignal').value;

            if (!role || !skill || !signal) {
                alert('Please fill in all fields for the outreach message.');
                return;
            }

            const prompt = `
                Act as an expert TalentLNX staffing partner. Write a personalized, concise (3-5 sentences), and value-driven outreach email to a potential candidate.
                Follow these rules from the TalentLNX Outreach Strategy Guide:
                1. Personalize beyond the name. Reference the signal directly.
                2. Keep it tight and respect the reader's time.
                3. Focus on the candidate's career and how this opportunity provides value to them.
                4. End with a simple, clear, and easy-to-answer call to action.
                5. Use a human, confident, and professional tone. Avoid jargon.

                Candidate Details:
                - Role: ${role}
                - Key Skill/Accomplishment: ${skill}
                - Recent Signal: ${signal}

                Generate the email now.
            `;
            callGemini(prompt, outreachOutput, generateOutreachBtn);
        });
        
        copyOutreachBtn.addEventListener('click', () => {
            outreachOutput.select();
            document.execCommand('copy');
            copyOutreachBtn.textContent = 'Copied!';
            setTimeout(() => {
                copyOutreachBtn.textContent = 'Copy to Clipboard';
            }, 2000);
        });

        getCoachingBtn.addEventListener('click', () => {
            const scenario = document.getElementById('roleplayScenario').selectedOptions[0].text;
            
            const prompt = `
                Act as an expert TalentLNX sales coach embodying the ARETÉ, 5 P's, and LGM philosophies.
                A staffing partner is facing the following client objection during a discovery call: "${scenario}"

                Provide a strategic response to handle this objection. Your coaching should include two parts:
                1. **The Response:** The exact phrase the partner should use to respond, framed with empathy and curiosity.
                2. **The Strategy:** A brief explanation of why this response works, linking it back to consultative selling and building long-term partnerships.

                Format the output clearly with "**The Response:**" and "**The Strategy:**" as bolded headers.
            `;
            roleplayOutput.innerHTML = '<p class="text-gray-500">Generating...</p>';
            callGemini(prompt, roleplayOutput, getCoachingBtn);
        });

    </script>

</body>
</html>
