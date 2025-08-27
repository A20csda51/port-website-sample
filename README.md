<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Portfolio | Ajith</title>
    <!-- Tailwind CSS CDN is linked here -->
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* Custom CSS styles */
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f0f4f8; /* Soft background color */
        }
        .section-padding {
            padding: 80px 20px;
        }
    </style>
</head>
<body class="text-gray-800">
    <!-- Header and Navigation Bar -->
    <header class="bg-white shadow-sm sticky top-0 z-50">
        <nav class="container mx-auto px-4 py-4 flex justify-between items-center">
            <a href="#" class="text-2xl font-bold text-indigo-600 rounded-md p-2">
                Ajith
            </a>
            <div class="hidden md:flex space-x-6">
                <a href="#about" class="text-gray-600 hover:text-indigo-600 font-medium transition duration-300">About Me</a>
                <a href="#skills" class="text-gray-600 hover:text-indigo-600 font-medium transition duration-300">Skills</a>
                <a href="#projects" class="text-gray-600 hover:text-indigo-600 font-medium transition duration-300">Projects</a>
                <a href="#contact" class="text-gray-600 hover:text-indigo-600 font-medium transition duration-300">Contact</a>
            </div>
            <!-- Mobile Menu -->
            <button id="mobile-menu-button" class="md:hidden text-gray-600 focus:outline-none">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7" />
                </svg>
            </button>
        </nav>
        <!-- Mobile Menu Content -->
        <div id="mobile-menu" class="hidden md:hidden bg-white shadow-lg py-2">
            <a href="#about" class="block px-4 py-2 text-gray-800 hover:bg-gray-100">About Me</a>
            <a href="#skills" class="block px-4 py-2 text-gray-800 hover:bg-gray-100">Skills</a>
            <a href="#projects" class="block px-4 py-2 text-gray-800 hover:bg-gray-100">Projects</a>
            <a href="#contact" class="block px-4 py-2 text-gray-800 hover:bg-gray-100">Contact</a>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="section-padding bg-gradient-to-r from-indigo-500 to-purple-600 text-white flex items-center justify-center text-center">
        <div class="max-w-3xl">
            <h1 class="text-4xl sm:text-5xl lg:text-6xl font-extrabold leading-tight mb-4">
                Hello, I'm <br class="hidden sm:block"> <span class="text-yellow-300">Ajith</span>
            </h1>
            <p class="text-lg sm:text-xl mb-8 opacity-90">
                I'm a content creator, passionate about creating innovative solutions.
            </p>
            <a href="#projects" class="inline-block bg-white text-indigo-600 font-semibold py-3 px-8 rounded-full shadow-lg hover:bg-gray-100 transform hover:scale-105 transition duration-300">
                View My Work
            </a>
        </div>
    </section>

    <!-- About Me Section -->
    <section id="about" class="section-padding bg-white">
        <div class="container mx-auto text-center">
            <h2 class="text-3xl font-bold mb-4">About Me</h2>
            <p class="text-lg text-gray-600 mb-8 max-w-2xl mx-auto">
                I am a content creator with [Your Years of Experience] years of experience. I'm passionate about implementing innovative ideas and solving complex problems. My goal is to create great user experiences.
            </p>
            <div class="flex justify-center space-x-4">
                <a href="#" class="text-gray-600 hover:text-indigo-600 transition duration-300">
                    <img src="https://placehold.co/120x120/d1d5db/000?text=Your+Photo" alt="Your Photo" class="rounded-full shadow-md">
                </a>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills" class="section-padding bg-gray-100">
        <div class="container mx-auto text-center">
            <h2 class="text-3xl font-bold mb-8">My Skills</h2>
            <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6">
                <!-- Skill Card 1 -->
                <div class="bg-white rounded-xl shadow-lg p-6 transform hover:scale-105 transition duration-300">
                    <h3 class="text-xl font-bold mb-2">Video Editing</h3>
                    <p class="text-gray-600">Adobe Premiere Pro, Final Cut Pro, DaVinci Resolve</p>
                </div>
                <!-- Skill Card 2 -->
                <div class="bg-white rounded-xl shadow-lg p-6 transform hover:scale-105 transition duration-300">
                    <h3 class="text-xl font-bold mb-2">Writing & Storytelling</h3>
                    <p class="text-gray-600">Copywriting, Scriptwriting, Blogging</p>
                </div>
                <!-- Skill Card 3 -->
                <div class="bg-white rounded-xl shadow-lg p-6 transform hover:scale-105 transition duration-300">
                    <h3 class="text-xl font-bold mb-2">Social Media Management</h3>
                    <p class="text-gray-600">YouTube, Instagram, TikTok, Twitter</p>
                </div>
                <!-- Skill Card 4 -->
                <div class="bg-white rounded-xl shadow-lg p-6 transform hover:scale-105 transition duration-300">
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
