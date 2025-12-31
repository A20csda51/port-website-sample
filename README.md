<!DOCTYPE html>
<html lang="ta">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Outfit2Reel AI | Demo Studio</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;700;900&display=swap');
        body { font-family: 'Inter', sans-serif; background-color: #080808; color: #eee; }
        .purple-glow { box-shadow: 0 0 20px rgba(157, 80, 187, 0.3); }
        .glass-card { background: rgba(255, 255, 255, 0.03); border: 1px solid rgba(255, 255, 255, 0.08); backdrop-filter: blur(10px); }
        .gradient-text { background: linear-gradient(135deg, #a855f7 0%, #ec4899 100%); -webkit-background-clip: text; -webkit-text-fill-color: transparent; }
    </style>
</head>
<body class="overflow-x-hidden">

    <!-- Header -->
    <nav class="p-6 flex justify-between items-center max-w-7xl mx-auto">
        <div class="flex items-center gap-3">
            <div class="w-10 h-10 bg-gradient-to-br from-purple-600 to-pink-600 rounded-xl flex items-center justify-center shadow-lg">
                <i class="fas fa-bolt text-white"></i>
            </div>
            <span class="text-xl font-black tracking-tighter uppercase italic">Outfit2Reel <span class="text-purple-500">AI</span></span>
        </div>
        <div class="hidden md:flex gap-8 text-xs font-bold uppercase tracking-widest text-gray-400">
            <a href="#" class="hover:text-white transition">Showcase</a>
            <a href="#" class="hover:text-white transition">Pricing</a>
            <a href="#" class="hover:text-white transition text-purple-400 underline">Demo Mode</a>
        </div>
    </nav>

    <!-- Hero -->
    <section class="py-16 px-6 text-center max-w-4xl mx-auto">
        <div class="inline-block px-4 py-1 rounded-full border border-purple-500/30 bg-purple-500/10 text-purple-400 text-[10px] font-bold uppercase tracking-widest mb-6">
            Optimized for Sora 2 & Tamil Ads
        </div>
        <h1 class="text-5xl md:text-7xl font-black mb-6 leading-tight uppercase italic">
            Viral Reels in <span class="gradient-text">60 Seconds.</span>
        </h1>
        <p class="text-gray-400 text-lg mb-10 leading-relaxed">
            Upload your dress image. Get a 50-second cinematic script for a female character with high-converting Tamil captions. 
        </p>
    </section>

    <!-- Studio Area -->
    <section class="px-6 pb-20">
        <div class="max-w-6xl mx-auto grid lg:grid-cols-2 gap-10">
            
            <!-- Input Card -->
            <div class="glass-card p-8 rounded-[2rem] space-y-6">
                <div class="flex items-center gap-2 mb-4">
                    <i class="fas fa-wand-sparkles text-purple-500"></i>
                    <h2 class="font-black uppercase italic">The Studio (Demo)</h2>
                </div>

                <!-- Custom Upload -->
                <div id="dropzone" class="aspect-video rounded-3xl border-2 border-dashed border-white/10 flex flex-col items-center justify-center cursor-pointer hover:border-purple-500/50 transition bg-white/5 relative overflow-hidden group">
                    <input type="file" id="imageInput" class="hidden" accept="image/*">
                    <div id="previewWrap" class="absolute inset-0 hidden">
                        <img id="previewImg" src="" class="w-full h-full object-cover">
                    </div>
                    <div id="uploadUI" class="text-center">
                        <div class="w-16 h-16 bg-white/5 rounded-full flex items-center justify-center mx-auto mb-4 group-hover:scale-110 transition">
                            <i class="fas fa-cloud-upload-alt text-gray-400"></i>
                        </div>
                        <p class="text-white font-bold text-sm uppercase">Upload Dress Image</p>
                        <p class="text-gray-500 text-xs mt-1">Select a clear dress/saree photo</p>
                    </div>
                </div>

                <!-- Config -->
                <div class="grid grid-cols-2 gap-4">
                    <div class="space-y-2">
                        <label class="text-[10px] font-black text-gray-500 uppercase">Style</label>
                        <select class="w-full bg-white/5 border border-white/10 rounded-xl px-4 py-3 text-sm text-white outline-none">
                            <option>Tamil Traditional</option>
                            <option>Luxury Boutique</option>
                            <option>Streetwear</option>
                        </select>
                    </div>
                    <div class="space-y-2">
                        <label class="text-[10px] font-black text-gray-500 uppercase">Character</label>
                        <select class="w-full bg-white/5 border border-white/10 rounded-xl px-4 py-3 text-sm text-white outline-none">
                            <option>Female (Lead)</option>
                        </select>
                    </div>
                </div>

                <button id="demoBtn" class="w-full py-5 rounded-2xl bg-white text-black font-black text-lg uppercase italic hover:bg-purple-500 hover:text-white transition transform active:scale-95 shadow-xl shadow-purple-500/10">
                    Generate Demo Script
                </button>
            </div>

            <!-- Output Card -->
            <div class="glass-card p-8 rounded-[2rem] flex flex-col min-h-[450px]">
                <div class="flex justify-between items-center mb-6">
                    <span id="statusLabel" class="text-[10px] font-bold text-gray-500 uppercase tracking-widest">Waiting for input...</span>
                    <button id="copyBtn" class="hidden bg-white/5 px-4 py-2 rounded-xl text-[10px] font-bold uppercase hover:bg-white/10 transition">
                        <i class="fas fa-copy"></i> Copy All
                    </button>
                </div>

                <!-- Result Content -->
                <div id="resultContent" class="flex-1 overflow-y-auto space-y-6 hidden">
                    <div class="animate-in fade-in slide-in-from-bottom-4 duration-700">
                        <h4 class="text-purple-400 font-bold text-xs uppercase mb-2">Sora 2 Cinematic Prompt:</h4>
                        <p id="soraPrompt" class="text-sm text-gray-300 font-mono leading-relaxed bg-black/40 p-4 rounded-xl border border-white/5 italic">
                            <!-- Injected -->
                        </p>
                    </div>
                    <div class="animate-in fade-in slide-in-from-bottom-4 duration-1000">
                        <h4 class="text-pink-400 font-bold text-xs uppercase mb-2">Tamil Sales Script:</h4>
                        <div id="tamilScript" class="text-lg font-bold text-white leading-relaxed p-4 bg-purple-900/10 rounded-xl border border-purple-500/10">
                            <!-- Injected -->
                        </div>
                    </div>
                </div>

                <!-- Placeholder -->
                <div id="placeholder" class="flex-1 flex flex-col items-center justify-center text-center opacity-20">
                    <i class="fas fa-film text-6xl mb-4"></i>
                    <p class="text-sm italic">Your AI-generated marketing content will appear here.</p>
                </div>

                <!-- Mock Loader -->
                <div id="loader" class="hidden flex-1 flex flex-col items-center justify-center text-center">
                    <div class="w-12 h-12 border-4 border-purple-500/20 border-t-purple-500 rounded-full animate-spin mb-4"></div>
                    <p class="text-sm font-black uppercase tracking-widest text-purple-400 animate-pulse">AI Directing Your Reel...</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="py-20 border-t border-white/5 text-center px-6">
        <p class="text-gray-500 font-bold text-[10px] uppercase tracking-widest mb-4">Need a custom AI bot or website integration?</p>
        <p class="text-purple-400 font-black text-lg mb-8 italic">Email us: automation@outfit2reel.ai</p>
        <div class="flex justify-center gap-6 opacity-30">
            <i class="fab fa-instagram"></i>
            <i class="fab fa-twitter"></i>
            <i class="fab fa-linkedin"></i>
        </div>
    </footer>

    <script>
        const imageInput = document.getElementById('imageInput');
        const dropzone = document.getElementById('dropzone');
        const previewWrap = document.getElementById('previewWrap');
        const previewImg = document.getElementById('previewImg');
        const uploadUI = document.getElementById('uploadUI');
        const demoBtn = document.getElementById('demoBtn');
        const loader = document.getElementById('loader');
        const placeholder = document.getElementById('placeholder');
        const resultContent = document.getElementById('resultContent');
        const soraPrompt = document.getElementById('soraPrompt');
        const tamilScript = document.getElementById('tamilScript');
        const statusLabel = document.getElementById('statusLabel');
        const copyBtn = document.getElementById('copyBtn');

        // Image Preview Logic
        dropzone.onclick = () => imageInput.click();
        imageInput.onchange = (e) => {
            const file = e.target.files[0];
            if (file) {
                const reader = new FileReader();
                reader.onload = (ev) => {
                    previewImg.src = ev.target.result;
                    previewWrap.classList.remove('hidden');
                    uploadUI.classList.add('hidden');
                };
                reader.readAsDataURL(file);
            }
        };

        // Mock Generation Logic (No API needed)
        demoBtn.onclick = () => {
            if (!previewImg.src) {
                alert("Mothala Dress Photo upload pannunga!");
                return;
            }

            // Start UI
            placeholder.classList.add('hidden');
            resultContent.classList.add('hidden');
            loader.classList.remove('hidden');
            statusLabel.innerText = "Analyzing Texture...";
            demoBtn.disabled = true;

            // Fake processing delay
            setTimeout(() => {
                loader.classList.add('hidden');
                resultContent.classList.remove('hidden');
                copyBtn.classList.remove('hidden');
                statusLabel.innerText = "Generated (Sora 2 Ready)";
                demoBtn.disabled = false;

                // Set Sample Data
                soraPrompt.innerText = "Cinematic 50s fashion film, Sora 2 rendering. A beautiful female model walking in slow-motion through a luxury South Indian temple-style corridor. The fabric of the outfit flows naturally with air currents. Extreme close-up on the embroidery texture. Soft golden hour lighting hitting the model's face. 8k resolution, hyper-realistic, fashion runway aesthetic.";
                
                tamilScript.innerHTML = "வணக்கம் மக்களே! ✨ <br><br> நீங்க தேடிக்கிட்டு இருந்த அந்த Perfect மார்டன் பாரம்பரிய உடை இதோ! <br><br> 💎 பிரீமியம் தரம் <br> 💎 கண்கவர் டிசைன் <br><br> இப்போதே ஆர்டர் செய்ய லிங்க்-ஐ கிளிக் பண்ணுங்க! 🛍️";
            }, 2500);
        };

        // Copy Feature
        copyBtn.onclick = () => {
            const text = soraPrompt.innerText + "\n\n" + tamilScript.innerText;
            const temp = document.createElement('textarea');
            temp.value = text;
            document.body.appendChild(temp);
            temp.select();
            document.execCommand('copy');
            document.body.removeChild(temp);
            alert("Copied successfully!");
        };
    </script>
</body>
</html>

                    <h3 class="text-xl font-bold mb-2">Graphic Design</h3>
                    <p class="text-gray-600">Adobe Photoshop, Canva, Illustrator</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="section-padding bg-white">
        <div class="container mx-auto text-center">
            <h2 class="text-3xl font-bold mb-8">My Projects</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Project Card 1 -->
                <div class="bg-gray-100 rounded-xl shadow-md overflow-hidden transform hover:scale-105 transition duration-300">
                    <img src="https://placehold.co/600x400/818cf8/fff?text=Project+1" alt="Project 1" class="w-full h-48 object-cover">
                    <div class="p-6">
                        <h3 class="text-2xl font-bold mb-2">Project 1</h3>
                        <p class="text-gray-600 text-sm mb-4">
                            A brief description of this project goes here. You can mention the technologies used.
                        </p>
                        <a href="#" class="text-indigo-600 hover:text-indigo-800 font-medium">View Details</a>
                    </div>
                </div>
                <!-- Project Card 2 -->
                <div class="bg-gray-100 rounded-xl shadow-md overflow-hidden transform hover:scale-105 transition duration-300">
                    <img src="https://placehold.co/600x400/a78bfa/fff?text=Project+2" alt="Project 2" class="w-full h-48 object-cover">
                    <div class="p-6">
                        <h3 class="text-2xl font-bold mb-2">Project 2</h3>
                        <p class="text-gray-600 text-sm mb-4">
                            A brief description of this project goes here. You can mention the technologies used.
                        </p>
                        <a href="#" class="text-indigo-600 hover:text-indigo-800 font-medium">View Details</a>
                    </div>
                </div>
                <!-- Project Card 3 -->
                <div class="bg-gray-100 rounded-xl shadow-md overflow-hidden transform hover:scale-105 transition duration-300">
                    <img src="https://placehold.co/600x400/9ca3af/fff?text=Project+3" alt="Project 3" class="w-full h-48 object-cover">
                    <div class="p-6">
                        <h3 class="text-2xl font-bold mb-2">Project 3</h3>
                        <p class="text-gray-600 text-sm mb-4">
                            A brief description of this project goes here. You can mention the technologies used.
                        </p>
                        <a href="#" class="text-indigo-600 hover:text-indigo-800 font-medium">View Details</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="section-padding bg-gray-100">
        <div class="container mx-auto text-center max-w-xl">
            <h2 class="text-3xl font-bold mb-8">Contact Me</h2>
            <form action="#" class="space-y-4">
                <input type="text" placeholder="Your Name" class="w-full p-4 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-indigo-500">
                <input type="email" placeholder="Your Email" class="w-full p-4 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-indigo-500">
                <textarea placeholder="Your Message" rows="4" class="w-full p-4 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-indigo-500"></textarea>
                <button type="submit" class="w-full bg-indigo-600 text-white font-bold py-4 px-6 rounded-lg shadow-lg hover:bg-indigo-700 transition duration-300">
                    Send
                </button>
            </form>
            <div class="mt-8">
                <p class="text-lg text-gray-600 mb-2">Or email me at:</p>
                <a href="mailto:your-email@example.com" class="text-indigo-600 hover:underline">your-email@example.com</a>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-800 text-white text-center py-6">
        <div class="container mx-auto">
            <p class="text-sm">
                © 2024 Ajith. All rights reserved.
            </p>
        </div>
    </footer>

    <!-- JavaScript -->
    <script>
        // Script to handle mobile menu functionality
        const mobileMenuButton = document.getElementById('mobile-menu-button');
        const mobileMenu = document.getElementById('mobile-menu');

        mobileMenuButton.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });

        // Smooth scrolling for page links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
    </script>
</body>
</html>
