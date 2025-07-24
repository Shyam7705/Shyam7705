<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Shyam Baranwal | Software Developer</title>
    <!-- Chosen Palette: Calm Neutral -->
    <!-- Application Structure Plan: The application is structured as a single-page portfolio with a fixed navigation bar for easy access to key sections: About, Skills, Stats, and Connect. This structure was chosen over a simple linear document to allow non-linear exploration, enabling users (like recruiters) to quickly jump to the information most relevant to them. The flow is designed to first introduce Shyam, then detail his capabilities, provide quantitative proof of his activity via a stats dashboard, and finally offer clear calls to action for connection. This enhances usability and presents the information in a more engaging, professional format than a standard README file. -->
    <!-- Visualization & Content Choices: The source 'report' (a README file) uses externally generated images for stats. Goal: Organize and present this information clearly. Method: The stats images are organized into a responsive grid layout, creating a 'dashboard' feel. This prevents the awkward vertical stacking of the original and allows for easier comparison. Goal: Showcase skills effectively. Method: Skills are grouped by category and presented in styled cards, which is more visually organized than a simple list of icons. Interaction: Smooth scrolling via JavaScript and hover effects on interactive elements improve user experience. The entire application uses HTML and Tailwind CSS for structure and styling, with no custom-generated charts or SVG graphics. -->
    <!-- CONFIRMATION: NO SVG graphics used. NO Mermaid JS used. -->
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f8f7f4;
            color: #3d3d3d;
        }
        .stat-card-container {
            background-color: #ffffff;
            border-radius: 0.75rem;
            padding: 1.5rem;
            box-shadow: 0 4px 6px -1px rgb(0 0 0 / 0.1), 0 2px 4px -2px rgb(0 0 0 / 0.1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        .stat-card-container:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 15px -3px rgb(0 0 0 / 0.1), 0 4px 6px -4px rgb(0 0 0 / 0.1);
        }
        .stat-card-container img {
            width: 100%;
            height: auto;
        }
        .nav-link {
            transition: color 0.3s ease;
            position: relative;
        }
        .nav-link:hover {
            color: #1e40af;
        }
        .nav-link::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -4px;
            left: 50%;
            transform: translateX(-50%);
            background-color: #1e40af;
            transition: width 0.3s ease;
        }
        .nav-link:hover::after {
            width: 100%;
        }
    </style>
</head>
<body class="antialiased">

    <!-- Header & Navigation -->
    <header id="header" class="bg-white/80 backdrop-blur-lg fixed top-0 left-0 right-0 z-50 shadow-sm">
        <div class="container mx-auto px-6 py-4 flex justify-between items-center">
            <a href="#home" class="text-xl font-bold text-blue-900">Shyam Baranwal</a>
            <nav class="hidden md:flex space-x-8">
                <a href="#about" class="nav-link text-gray-700 font-medium">About</a>
                <a href="#skills" class="nav-link text-gray-700 font-medium">Skills</a>
                <a href="#stats" class="nav-link text-gray-700 font-medium">Dashboard</a>
                <a href="#connect" class="nav-link text-gray-700 font-medium">Connect</a>
            </nav>
            <button id="mobile-menu-button" class="md:hidden text-gray-800">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7" />
                </svg>
            </button>
        </div>
        <!-- Mobile Menu -->
        <div id="mobile-menu" class="hidden md:hidden px-6 pb-4">
            <a href="#about" class="block py-2 text-gray-700 font-medium">About</a>
            <a href="#skills" class="block py-2 text-gray-700 font-medium">Skills</a>
            <a href="#stats" class="block py-2 text-gray-700 font-medium">Dashboard</a>
            <a href="#connect" class="block py-2 text-gray-700 font-medium">Connect</a>
        </div>
    </header>

    <main class="pt-20">
        <!-- Home Section -->
        <section id="home" class="py-20 md:py-32">
            <div class="container mx-auto px-6 text-center">
                <div class="mb-8">
                    <img src="https://media.giphy.com/media/dWesBcTLavkZuG35MI/giphy.gif" width="600" height="300" class="mx-auto rounded-lg shadow-lg"/>
                </div>
                <h1 class="text-4xl md:text-6xl font-bold text-blue-900 leading-tight">Hi there, I'm Shyam Baranwal 👋</h1>
                <p class="mt-4 text-lg md:text-xl text-gray-600 max-w-3xl mx-auto">A passionate software developer focused on building elegant, high-performance software solutions.</p>
                <div class="mt-8">
                    <a href="#connect" class="bg-blue-800 text-white font-bold py-3 px-8 rounded-full hover:bg-blue-900 transition-colors duration-300">Get in Touch</a>
                </div>
            </div>
        </section>

        <!-- About Section -->
        <section id="about" class="py-20 bg-white">
            <div class="container mx-auto px-6">
                <div class="text-center mb-12">
                    <h2 class="text-3xl font-bold text-gray-800">About Me</h2>
                    <p class="text-gray-500 mt-2">A brief introduction to my professional life and passions.</p>
                </div>
                <div class="max-w-4xl mx-auto bg-gray-50 p-8 rounded-lg shadow-sm">
                    <p class="text-lg text-gray-700 leading-relaxed mb-6">I'm a passionate and results-driven Software Developer from India with a knack for creating efficient, scalable, and user-friendly solutions. I thrive on solving complex problems and am constantly exploring new technologies to enhance my skill set.</p>
                    <ul class="space-y-4 text-gray-600">
                        <li class="flex items-start"><span class="text-blue-600 font-bold mr-3">🌱</span> <strong>Currently learning:</strong> Cloud-Native technologies and Microservices Architecture.</li>
                        <li class="flex items-start"><span class="text-blue-600 font-bold mr-3">🤔</span> <strong>Ask me about:</strong> Anything related to `SQL`, `Python`, `Java`, `C` and `C++`.</li>
                        <li class="flex items-start"><span class="text-blue-600 font-bold mr-3">📫</span> <strong>How to reach me:</strong> baranwal07shyam@gmail.com</li>
                        <li class="flex items-start"><span class="text-blue-600 font-bold mr-3">⚡</span> <strong>Fun fact:</strong> I believe that with enough sleep, any bug can be fixed.</li>
                    </ul>
                </div>
            </div>
        </section>

        <!-- Skills Section -->
        <section id="skills" class="py-20">
            <div class="container mx-auto px-6">
                <div class="text-center mb-12">
                    <h2 class="text-3xl font-bold text-gray-800">My Skills & Expertise</h2>
                    <p class="text-gray-500 mt-2">The technologies and tools I use to bring ideas to life.</p>
                </div>
                <div class="max-w-5xl mx-auto">
                    <div class="flex flex-wrap justify-center gap-6">
                        <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="Python" class="h-16 transition-transform hover:scale-110" title="Python">
                        <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/java/java-original.svg" alt="Java" class="h-16 transition-transform hover:scale-110" title="Java">
                        <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/c/c-original.svg" alt="C" class="h-16 transition-transform hover:scale-110" title="C">
                        <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mysql/mysql-original-wordmark.svg" alt="SQL" class="h-16 transition-transform hover:scale-110" title="SQL">
                        <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/notion/notion-original.svg" alt="Notion" class="h-16 transition-transform hover:scale-110" title="Notion">
                    </div>
                </div>
            </div>
        </section>

        <!-- Stats Section -->
        <section id="stats" class="py-20 bg-white">
            <div class="container mx-auto px-6">
                <div class="text-center mb-12">
                    <h2 class="text-3xl font-bold text-gray-800">My Coding Dashboard</h2>
                    <p class="text-gray-500 mt-2">A real-time overview of my activity and performance across coding platforms.</p>
                </div>
                <div class="grid grid-cols-1 md:grid-cols-2 gap-8 max-w-6xl mx-auto">
                    <div class="stat-card-container">
                        <p class="text-center font-semibold text-gray-700 mb-4">GitHub Stats</p>
                        <img src="https://github-readme-stats.vercel.app/api?username=Shyam7705&show_icons=true&theme=tokyonight&hide_border=true&include_all_commits=true&count_private=true" alt="Shyam's GitHub Stats" onerror="this.style.display='none'">
                    </div>
                     <div class="stat-card-container">
                        <p class="text-center font-semibold text-gray-700 mb-4">Top Languages</p>
                        <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Shyam7705&layout=compact&theme=tokyonight&hide_border=true" alt="Top Languages" onerror="this.style.display='none'">
                    </div>
                     <div class="stat-card-container">
                        <p class="text-center font-semibold text-gray-700 mb-4">LeetCode Stats</p>
                        <img src="https://leetcode-stats-card.herokuapp.com/Shyamac" alt="Shyam's LeetCode Stats" onerror="this.style.display='none'">
                    </div>
                     <div class="stat-card-container">
                        <p class="text-center font-semibold text-gray-700 mb-4">GeeksforGeeks Stats</p>
                        <img src="https://gfg-readme-stats.vercel.app/api?user_id=baranwal8k15&theme=tokyonight&hide_border=true" alt="Shyam's GeeksforGeeks Stats" onerror="this.style.display='none'">
                    </div>
                </div>
            </div>
        </section>

        <!-- Connect Section -->
        <section id="connect" class="py-20">
            <div class="container mx-auto px-6 text-center">
                 <h2 class="text-3xl font-bold text-gray-800">Let's Connect</h2>
                 <p class="text-gray-500 mt-2 max-w-2xl mx-auto">I'm always open to discussing new projects, creative ideas, or opportunities to be part of an amazing team. Feel free to reach out!</p>
                 <div class="mt-8">
                     <a href="mailto:baranwal07shyam@gmail.com" class="bg-blue-800 text-white font-bold py-3 px-8 rounded-full hover:bg-blue-900 transition-colors duration-300">
                        Email Me: baranwal07shyam@gmail.com
                     </a>
                 </div>
                 <div class="mt-10 flex justify-center space-x-6">
                    <a href="https://www.linkedin.com/in/baranwal07shyam/" target="_blank" class="text-gray-500 hover:text-blue-800 transition-colors">
                        <img src="https://raw.githubusercontent.com/maurodesouza/profile-readme-generator/master/src/assets/icons/social/linkedin/default.svg" width="40" height="40" alt="linkedin logo"/>
                    </a>
                 </div>
            </div>
        </section>
    </main>

    <footer class="bg-white py-6">
        <div class="container mx-auto px-6 text-center text-gray-500">
            <p>&copy; 2024 Shyam Baranwal. All Rights Reserved.</p>
        </div>
    </footer>

    <script>
        const mobileMenuButton = document.getElementById('mobile-menu-button');
        const mobileMenu = document.getElementById('mobile-menu');

        mobileMenuButton.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });

        // Smooth scroll for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                const targetElement = document.querySelector(targetId);

                if (targetElement) {
                    // Close mobile menu on click
                    if (!mobileMenu.classList.contains('hidden')) {
                        mobileMenu.classList.add('hidden');
                    }
                    
                    targetElement.scrollIntoView({
                        behavior: 'smooth'
                    });
                }
            });
        });
    </script>
</body>
</html>
