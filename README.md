# Ex01 Portfolio
## Date:

## AIM
To create a Portfolio using HTML and CSS.

## ALGORITHM
### STEP 1
Create an HTML file (index.html)

### STEP 2
Create a CSS file (style.css)

### STEP 3
Include a navigation bar with links to different sections.

### STEP 4
Add structured sections for introduction, about, projects, and contact details.

### STEP 5
Define global styles for fonts, colors, and layout.

### STEP 6
Style the header, navigation bar, and sections.

### STEP 7
Use Flexbox or CSS Grid for layout design.

### STEP 8
Add hover effects and transitions for interactivity.

### STEP 9
Add Images and Media.

### STEP 10
Use optimized images for a professional look.

### STEP 11
Open the HTML file in a browser to check layout and functionality.

### STEP 12
Fix styling issues and refine content placement.

### STEP 13
Deploy the Portfolio.

### STEP 14
Upload to GitHub Pages for free hosting.

## PROGRAM
```html
<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Karthikeyan A | AI & Data Science Student</title>
    
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700;800&display=swap" rel="stylesheet">
    
    <!-- FontAwesome for Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

    <!-- Tailwind Configuration -->
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                    },
                    colors: {
                        black: '#000000',
                        'dark-card': '#0a0a0a',
                        'neon-blue': '#00f3ff',
                        'neon-purple': '#bc13fe',
                    }
                }
            }
        }
    </script>

    <!-- Custom CSS for Scrollbar and specific animations -->
    <style>
        body {
            background-color: #000000;
            color: #ffffff;
            overflow-x: hidden;
        }

        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #000000;
        }
        ::-webkit-scrollbar-thumb {
            background: #333;
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #bc13fe;
        }

        /* Scroll Reveal Utility Classes */
        .reveal {
            opacity: 0;
            transform: translateY(30px);
            transition: all 0.8s ease-out;
        }
        .reveal.active {
            opacity: 1;
            transform: translateY(0);
        }

        /* Glow effects */
        .glow-text {
            text-shadow: 0 0 10px rgba(0, 243, 255, 0.5);
        }
        .glow-box:hover {
            box-shadow: 0 0 20px rgba(188, 19, 254, 0.4);
        }
    </style>
</head>
<body class="antialiased selection:bg-neon-purple selection:text-white relative">

    <!-- Sticky Navigation -->
    <nav class="fixed w-full z-50 top-0 left-0 backdrop-blur-md bg-black/70 border-b border-white/10 transition-all duration-300">
        <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-16">
                <div class="flex-shrink-0 flex items-center">
                    <a href="#hero" class="text-xl font-bold text-transparent bg-clip-text bg-gradient-to-r from-neon-blue to-neon-purple tracking-wider">
                        KA.
                    </a>
                </div>
                <!-- Desktop Menu -->
                <div class="hidden md:flex space-x-8">
                    <a href="#about" class="text-gray-300 hover:text-white transition-colors duration-300 text-sm font-medium">About</a>
                    <a href="#education" class="text-gray-300 hover:text-white transition-colors duration-300 text-sm font-medium">Education</a>
                    <a href="#skills" class="text-gray-300 hover:text-white transition-colors duration-300 text-sm font-medium">Skills</a>
                    <a href="#projects" class="text-gray-300 hover:text-white transition-colors duration-300 text-sm font-medium">Projects</a>
                </div>
                <!-- Mobile Menu Button -->
                <div class="md:hidden flex items-center">
                    <button id="mobile-menu-btn" class="text-gray-300 hover:text-white focus:outline-none">
                        <i class="fas fa-bars text-xl"></i>
                    </button>
                </div>
            </div>
        </div>
        <!-- Mobile Menu (Hidden by default) -->
        <div id="mobile-menu" class="hidden md:hidden bg-dark-card border-b border-white/10 absolute w-full">
            <div class="px-2 pt-2 pb-3 space-y-1 sm:px-3 flex flex-col">
                <a href="#about" class="mobile-link text-gray-300 hover:text-white block px-3 py-2 rounded-md text-base font-medium">About</a>
                <a href="#education" class="mobile-link text-gray-300 hover:text-white block px-3 py-2 rounded-md text-base font-medium">Education</a>
                <a href="#skills" class="mobile-link text-gray-300 hover:text-white block px-3 py-2 rounded-md text-base font-medium">Skills</a>
                <a href="#projects" class="mobile-link text-gray-300 hover:text-white block px-3 py-2 rounded-md text-base font-medium">Projects</a>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="hero" class="min-h-screen flex items-center justify-center pt-20 pb-12 px-4 relative overflow-hidden">
        <!-- Background decorative elements -->
        <div class="absolute top-1/4 left-1/4 w-96 h-96 bg-neon-blue rounded-full mix-blend-screen filter blur-[128px] opacity-20 animate-pulse"></div>
        <div class="absolute bottom-1/4 right-1/4 w-96 h-96 bg-neon-purple rounded-full mix-blend-screen filter blur-[128px] opacity-20 animate-pulse delay-700"></div>

        <div class="max-w-4xl mx-auto text-center z-10 reveal">
            <!-- Profile Photo -->
            <div class="relative w-40 h-40 mx-auto mb-8 group">
                <div class="absolute -inset-1 rounded-full bg-gradient-to-r from-neon-blue to-neon-purple opacity-75 group-hover:opacity-100 blur transition duration-500"></div>
                <img src="https://placehold.co/400x400/111111/ffffff?text=KA" alt="Karthikeyan A" class="relative w-full h-full object-cover rounded-full border-2 border-black">
            </div>

            <h1 class="text-5xl md:text-7xl font-extrabold mb-4 tracking-tight">
                Hi, I'm <br class="md:hidden">
                <span class="text-transparent bg-clip-text bg-gradient-to-r from-neon-blue to-neon-purple glow-text">Karthikeyan A</span>
            </h1>
            <h2 class="text-xl md:text-2xl text-gray-400 font-medium mb-4">
                AI & Data Science Student <span class="text-neon-blue">|</span> Developer
            </h2>
            <p class="text-gray-500 flex items-center justify-center gap-2 mb-10">
                <i class="fas fa-map-marker-alt"></i> Tamil Nadu, India
            </p>

            <!-- Action Buttons -->
            <div class="flex flex-wrap justify-center gap-4">
                <a href="mailto:karthi8668keyan@gmail.com" class="px-6 py-3 rounded-full bg-white text-black font-semibold hover:bg-gray-200 transition-all duration-300 hover:scale-105 shadow-[0_0_15px_rgba(255,255,255,0.3)]">
                    <i class="fas fa-envelope mr-2"></i>Email Me
                </a>
                <a href="#" target="_blank" class="px-6 py-3 rounded-full border border-white/20 bg-dark-card hover:bg-white/10 hover:border-white/50 transition-all duration-300 hover:scale-105">
                    <i class="fab fa-github mr-2"></i>GitHub
                </a>
                <a href="#" target="_blank" class="px-6 py-3 rounded-full border border-white/20 bg-dark-card hover:bg-white/10 hover:border-white/50 transition-all duration-300 hover:scale-105">
                    <i class="fab fa-linkedin mr-2"></i>LinkedIn
                </a>
                <a href="#" target="_blank" class="px-6 py-3 rounded-full border border-white/20 bg-dark-card hover:bg-white/10 hover:border-white/50 transition-all duration-300 hover:scale-105 text-neon-blue hover:text-white">
                    <i class="fas fa-file-alt mr-2"></i>Resume
                </a>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="py-20 px-4 bg-dark-card/30">
        <div class="max-w-4xl mx-auto reveal">
            <h2 class="text-3xl md:text-4xl font-bold mb-8 text-center"><span class="text-neon-blue">01.</span> About Me</h2>
            <div class="bg-dark-card border border-white/10 rounded-2xl p-8 md:p-10 shadow-lg relative overflow-hidden glow-box transition-all duration-500">
                <!-- Decorative accent -->
                <div class="absolute top-0 left-0 w-1 h-full bg-gradient-to-b from-neon-blue to-neon-purple"></div>
                
                <p class="text-gray-300 leading-relaxed text-lg mb-6">
                    I'm <strong class="text-white font-semibold">Karthikeyan A</strong>, an Artificial Intelligence and Data Science student at Saveetha Engineering College, passionate about technology, software development, and problem-solving.
                </p>
                <p class="text-gray-300 leading-relaxed text-lg mb-6">
                    I enjoy exploring programming, web development, machine learning, and emerging technologies. I focus on learning by building practical projects that solve real-world problems and improve my technical skills.
                </p>
                <p class="text-gray-300 leading-relaxed text-lg">
                    I'm continuously working to strengthen my programming knowledge, develop creative solutions, and turn ideas into useful applications. My goal is to grow as a developer and contribute to innovative projects in AI, data science, and software engineering.
                </p>
            </div>
        </div>
    </section>

    <!-- Education Section -->
    <section id="education" class="py-20 px-4">
        <div class="max-w-4xl mx-auto reveal">
            <h2 class="text-3xl md:text-4xl font-bold mb-8 text-center"><span class="text-neon-purple">02.</span> Education</h2>
            
            <div class="relative border-l-2 border-white/20 pl-8 ml-4 md:ml-0 group">
                <!-- Timeline Dot -->
                <div class="absolute -left-[11px] top-2 w-5 h-5 rounded-full bg-black border-2 border-neon-purple group-hover:bg-neon-purple transition-colors duration-300 shadow-[0_0_10px_#bc13fe]"></div>
                
                <div class="bg-dark-card border border-white/10 rounded-2xl p-6 hover:-translate-y-2 transition-all duration-300 hover:border-neon-purple/50 glow-box">
                    <div class="flex flex-col md:flex-row justify-between items-start md:items-center mb-4">
                        <h3 class="text-2xl font-bold text-white">Saveetha Engineering College</h3>
                        <span class="inline-block mt-2 md:mt-0 px-3 py-1 bg-white/10 rounded-full text-sm font-medium text-neon-purple border border-neon-purple/30">
                            Expected 2029
                        </span>
                    </div>
                    <h4 class="text-xl text-gray-400 font-medium mb-4">Artificial Intelligence and Data Science (AIDS)</h4>
                    <p class="text-gray-500">Currently pursuing foundational and advanced concepts in AI, Data Structures, Machine Learning, and core software development methodologies.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills" class="py-20 px-4 bg-dark-card/30">
        <div class="max-w-4xl mx-auto reveal">
            <h2 class="text-3xl md:text-4xl font-bold mb-12 text-center"><span class="text-neon-blue">03.</span> Skills & Expertise</h2>
            
            <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                <!-- Languages & Web -->
                <div class="bg-dark-card border border-white/10 rounded-2xl p-8 hover:border-neon-blue/40 transition-all duration-300">
                    <div class="flex items-center gap-4 mb-6">
                        <div class="p-3 bg-neon-blue/10 rounded-lg text-neon-blue">
                            <i class="fas fa-code text-xl"></i>
                        </div>
                        <h3 class="text-xl font-semibold">Languages & Web</h3>
                    </div>
                    <div class="flex flex-wrap gap-3">
                        <span class="px-4 py-2 bg-black border border-white/10 rounded-lg text-sm hover:border-neon-blue hover:text-neon-blue cursor-default transition-colors">JavaScript</span>
                        <span class="px-4 py-2 bg-black border border-white/10 rounded-lg text-sm hover:border-neon-blue hover:text-neon-blue cursor-default transition-colors">HTML</span>
                        <span class="px-4 py-2 bg-black border border-white/10 rounded-lg text-sm hover:border-neon-blue hover:text-neon-blue cursor-default transition-colors">CSS</span>
                        <span class="px-4 py-2 bg-black border border-white/10 rounded-lg text-sm hover:border-neon-blue hover:text-neon-blue cursor-default transition-colors">Node.js</span>
                        <span class="px-4 py-2 bg-black border border-white/10 rounded-lg text-sm hover:border-neon-blue hover:text-neon-blue cursor-default transition-colors">C</span>
                        <span class="px-4 py-2 bg-black border border-white/10 rounded-lg text-sm hover:border-neon-blue hover:text-neon-blue cursor-default transition-colors">Python</span>
                        <span class="px-4 py-2 bg-black border border-white/10 rounded-lg text-sm hover:border-neon-blue hover:text-neon-blue cursor-default transition-colors">Bash Shell</span>
                    </div>
                </div>

                <!-- Core Concepts -->
                <div class="bg-dark-card border border-white/10 rounded-2xl p-8 hover:border-neon-purple/40 transition-all duration-300">
                    <div class="flex items-center gap-4 mb-6">
                        <div class="p-3 bg-neon-purple/10 rounded-lg text-neon-purple">
                            <i class="fas fa-brain text-xl"></i>
                        </div>
                        <h3 class="text-xl font-semibold">Core Concepts</h3>
                    </div>
                    <div class="flex flex-wrap gap-3">
                        <span class="px-4 py-2 bg-black border border-white/10 rounded-lg text-sm hover:border-neon-purple hover:text-neon-purple cursor-default transition-colors">Machine Learning</span>
                        <span class="px-4 py-2 bg-black border border-white/10 rounded-lg text-sm hover:border-neon-purple hover:text-neon-purple cursor-default transition-colors">Data Structures</span>
                        <span class="px-4 py-2 bg-black border border-white/10 rounded-lg text-sm hover:border-neon-purple hover:text-neon-purple cursor-default transition-colors">Operating Systems</span>
                        <span class="px-4 py-2 bg-black border border-white/10 rounded-lg text-sm hover:border-neon-purple hover:text-neon-purple cursor-default transition-colors">Computer Networking</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="py-20 px-4">
        <div class="max-w-6xl mx-auto reveal">
            <h2 class="text-3xl md:text-4xl font-bold mb-12 text-center"><span class="text-neon-purple">04.</span> Featured Projects</h2>
            
            <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                
                <!-- Project 1 -->
                <div class="group bg-dark-card border border-white/10 rounded-2xl overflow-hidden hover:-translate-y-2 transition-all duration-500 hover:shadow-[0_0_20px_rgba(0,243,255,0.2)] hover:border-neon-blue/50 flex flex-col h-full">
                    <div class="p-8 flex flex-col flex-grow relative">
                        <!-- Icon top right -->
                        <div class="absolute top-8 right-8 text-gray-600 group-hover:text-neon-blue transition-colors duration-300">
                            <i class="fas fa-external-link-alt text-xl"></i>
                        </div>
                        
                        <div class="mb-4">
                            <i class="fas fa-route text-3xl text-neon-blue mb-4"></i>
                            <h3 class="text-2xl font-bold text-white mb-3">RailNav AI</h3>
                        </div>
                        <p class="text-gray-400 leading-relaxed mb-6 flex-grow">
                            A Smart India Hackathon (SIH) proposal featuring multi-platform indoor station navigation. Incorporates 3D mapping, BLE beacons, and AR pathfinding for seamless user transit.
                        </p>
                        <div class="flex flex-wrap gap-2 mt-auto">
                            <span class="text-xs font-medium text-neon-blue px-2 py-1 bg-neon-blue/10 rounded">3D Mapping</span>
                            <span class="text-xs font-medium text-neon-blue px-2 py-1 bg-neon-blue/10 rounded">AR</span>
                            <span class="text-xs font-medium text-neon-blue px-2 py-1 bg-neon-blue/10 rounded">BLE Beacons</span>
                        </div>
                    </div>
                </div>

                <!-- Project 2 -->
                <div class="group bg-dark-card border border-white/10 rounded-2xl overflow-hidden hover:-translate-y-2 transition-all duration-500 hover:shadow-[0_0_20px_rgba(188,19,254,0.2)] hover:border-neon-purple/50 flex flex-col h-full">
                    <div class="p-8 flex flex-col flex-grow relative">
                        <div class="absolute top-8 right-8 text-gray-600 group-hover:text-neon-purple transition-colors duration-300">
                            <i class="fas fa-external-link-alt text-xl"></i>
                        </div>
                        
                        <div class="mb-4">
                            <i class="fas fa-calendar-check text-3xl text-neon-purple mb-4"></i>
                            <h3 class="text-2xl font-bold text-white mb-3">Auto-Slot Booker</h3>
                        </div>
                        <p class="text-gray-400 leading-relaxed mb-6 flex-grow">
                            A Chrome extension designed for efficient event verification, integrated with Telegram notifications and robust auto-retry logic for high-demand booking scenarios.
                        </p>
                        <div class="flex flex-wrap gap-2 mt-auto">
                            <span class="text-xs font-medium text-neon-purple px-2 py-1 bg-neon-purple/10 rounded">Chrome Extension</span>
                            <span class="text-xs font-medium text-neon-purple px-2 py-1 bg-neon-purple/10 rounded">JS</span>
                            <span class="text-xs font-medium text-neon-purple px-2 py-1 bg-neon-purple/10 rounded">Telegram API</span>
                        </div>
                    </div>
                </div>

                <!-- Project 3 -->
                <div class="group bg-dark-card border border-white/10 rounded-2xl overflow-hidden hover:-translate-y-2 transition-all duration-500 hover:shadow-[0_0_20px_rgba(188,19,254,0.2)] hover:border-neon-purple/50 flex flex-col h-full">
                    <div class="p-8 flex flex-col flex-grow relative">
                        <div class="absolute top-8 right-8 text-gray-600 group-hover:text-neon-purple transition-colors duration-300">
                            <i class="fas fa-external-link-alt text-xl"></i>
                        </div>
                        
                        <div class="mb-4">
                            <i class="fas fa-puzzle-piece text-3xl text-neon-purple mb-4"></i>
                            <h3 class="text-2xl font-bold text-white mb-3">Auto-Enroller Extension</h3>
                        </div>
                        <p class="text-gray-400 leading-relaxed mb-6 flex-grow">
                            A browser tool built for the MyCamu portal that automates course enrollment. Features PDF/image course data extraction and intelligent slot clash detection.
                        </p>
                        <div class="flex flex-wrap gap-2 mt-auto">
                            <span class="text-xs font-medium text-neon-purple px-2 py-1 bg-neon-purple/10 rounded">Browser Tool</span>
                            <span class="text-xs font-medium text-neon-purple px-2 py-1 bg-neon-purple/10 rounded">Automation</span>
                            <span class="text-xs font-medium text-neon-purple px-2 py-1 bg-neon-purple/10 rounded">Data Extraction</span>
                        </div>
                    </div>
                </div>

                <!-- Project 4 -->
                <div class="group bg-dark-card border border-white/10 rounded-2xl overflow-hidden hover:-translate-y-2 transition-all duration-500 hover:shadow-[0_0_20px_rgba(0,243,255,0.2)] hover:border-neon-blue/50 flex flex-col h-full">
                    <div class="p-8 flex flex-col flex-grow relative">
                        <div class="absolute top-8 right-8 text-gray-600 group-hover:text-neon-blue transition-colors duration-300">
                            <i class="fas fa-external-link-alt text-xl"></i>
                        </div>
                        
                        <div class="mb-4">
                            <i class="fas fa-train text-3xl text-neon-blue mb-4"></i>
                            <h3 class="text-2xl font-bold text-white mb-3">IRCTC Booking Simulator</h3>
                        </div>
                        <p class="text-gray-400 leading-relaxed mb-6 flex-grow">
                            A local Node.js simulation environment designed to test automated payment selection and rigorous seat availability polling systems.
                        </p>
                        <div class="flex flex-wrap gap-2 mt-auto">
                            <span class="text-xs font-medium text-neon-blue px-2 py-1 bg-neon-blue/10 rounded">Node.js</span>
                            <span class="text-xs font-medium text-neon-blue px-2 py-1 bg-neon-blue/10 rounded">Simulation</span>
                            <span class="text-xs font-medium text-neon-blue px-2 py-1 bg-neon-blue/10 rounded">Scripting</span>
                        </div>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="py-8 border-t border-white/10 mt-12 bg-dark-card/50 text-center">
        <div class="max-w-4xl mx-auto px-4">
            <div class="flex justify-center space-x-6 mb-6">
                <a href="#" class="text-gray-400 hover:text-white transition-colors"><i class="fab fa-github text-xl"></i></a>
                <a href="#" class="text-gray-400 hover:text-white transition-colors"><i class="fab fa-linkedin text-xl"></i></a>
                <a href="mailto:karthi8668keyan@gmail.com" class="text-gray-400 hover:text-white transition-colors"><i class="fas fa-envelope text-xl"></i></a>
            </div>
            <p class="text-gray-500 text-sm">
                Designed & Built by Karthikeyan A &copy; <script>document.write(new Date().getFullYear())</script>
            </p>
        </div>
    </footer>

    <!-- Interactive Scripts -->
    <script>
        // Mobile Menu Toggle
        const btn = document.getElementById('mobile-menu-btn');
        const menu = document.getElementById('mobile-menu');
        const links = document.querySelectorAll('.mobile-link');

        btn.addEventListener('click', () => {
            menu.classList.toggle('hidden');
        });

        // Close mobile menu on link click
        links.forEach(link => {
            link.addEventListener('click', () => {
                menu.classList.add('hidden');
            });
        });

        // Scroll Reveal Animation (Intersection Observer)
        const revealElements = document.querySelectorAll('.reveal');

        const revealOptions = {
            threshold: 0.15,
            rootMargin: "0px 0px -50px 0px"
        };

        const revealOnScroll = new IntersectionObserver(function(entries, observer) {
            entries.forEach(entry => {
                if (!entry.isIntersecting) {
                    return;
                }
                entry.target.classList.add('active');
                observer.unobserve(entry.target);
            });
        }, revealOptions);

        revealElements.forEach(el => {
            revealOnScroll.observe(el);
        });
    </script>
</body>
</html>
```
## OUTPUT
![alt text](image.png)
![alt text](image-1.png)
![alt text](image-2.png)
## RESULT
The program for creating Portfolio using HTML and CSS is executed successfully.
