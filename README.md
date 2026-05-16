# portfolio
<!DOCTYPE html>

<html lang="en">

<head>

    <meta charset="UTF-8">

    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Nishi D. Patel | Business Analytics Portfolio</title>

    <script src="https://cdn.tailwindcss.com"></script>

    <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>

    <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/gsap.min.js"></script>

    <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/ScrollTrigger.min.js"></script>

    <script src="https://unpkg.com/@phosphor-icons/web"></script>

    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;600;800&family=Space+Grotesk:wght@500;700&display=swap" rel="stylesheet">

    

    <style>

        :root {

            --primary: #4f46e5;

            --secondary: #ec4899;

            --accent: #06b6d4;

            --bg-light: #f8fafc;

        }



        body {

            font-family: 'Plus Jakarta Sans', sans-serif;

            background-color: var(--bg-light);

            color: #1e293b;

            overflow-x: hidden;

        }



        h1, h2, h3 { font-family: 'Space Grotesk', sans-serif; }



        #canvas-container {

            position: fixed;

            top: 0;

            left: 0;

            width: 100%;

            height: 100vh;

            z-index: -1;

            background: radial-gradient(circle at top right, #e0e7ff, #f8fafc 50%);

        }



        /* Fancy Glassmorphism */

        .glass-card {

            background: rgba(255, 255, 255, 0.7);

            backdrop-filter: blur(12px);

            border: 1px solid rgba(255, 255, 255, 0.8);

            border-radius: 32px;

            box-shadow: 0 20px 50px rgba(0, 0, 0, 0.05);

            transition: all 0.4s cubic-bezier(0.23, 1, 0.32, 1);

        }



        .glass-card:hover {

            transform: translateY(-10px) scale(1.01);

            background: rgba(255, 255, 255, 0.9);

            box-shadow: 0 30px 60px rgba(79, 70, 229, 0.15);

            border-color: var(--primary);

        }



        /* Animated Cartoon Character */

        .data-mascot {

            animation: bounce 3s ease-in-out infinite;

            filter: drop-shadow(0 20px 30px rgba(79, 70, 229, 0.3));

        }



        @keyframes bounce {

            0%, 100% { transform: translateY(0) rotate(-2deg); }

            50% { transform: translateY(-25px) rotate(3deg); }

        }



        .gradient-text {

            background: linear-gradient(135deg, var(--primary), var(--secondary));

            -webkit-background-clip: text;

            -webkit-text-fill-color: transparent;

        }



        /* Floating Analytics Emojis */

        .floating-icon {

            position: absolute;

            pointer-events: none;

            z-index: 0;

            opacity: 0.6;

        }



        .btn-fancy {

            background: linear-gradient(135deg, var(--primary), #6366f1);

            color: white;

            padding: 1rem 2rem;

            border-radius: 100px;

            font-weight: 700;

            box-shadow: 0 10px 20px rgba(79, 70, 229, 0.3);

            transition: all 0.3s;

        }



        .btn-fancy:hover {

            transform: scale(1.05);

            box-shadow: 0 15px 30px rgba(79, 70, 229, 0.4);

        }

        

        .cert-tag {

            @apply px-3 py-1 bg-white/60 border border-indigo-100 rounded-full text-[10px] font-bold text-indigo-700 shadow-sm transition-all hover:bg-indigo-600 hover:text-white cursor-default;

        }

    </style>

</head>

<body>



    <div id="canvas-container"></div>



    <nav class="fixed top-0 w-full z-[100] px-6 py-4 flex justify-between items-center bg-white/30 backdrop-blur-xl border-b border-white/50">

        <div class="flex items-center gap-3">

            <div class="w-12 h-12 bg-indigo-600 rounded-2xl flex items-center justify-center text-white font-bold text-xl shadow-lg">NP</div>

            <div class="hidden sm:block">

                <span class="text-lg font-extrabold tracking-tight">Nishi D. Patel</span>

                <p class="text-[10px] uppercase tracking-widest text-indigo-500 font-bold">Business Analytics & Management</p>

            </div>

        </div>

        <div class="flex gap-4 items-center">

            <a href="mailto:niship505@gmail.com" class="hidden md:flex items-center gap-2 text-sm font-semibold hover:text-indigo-600 transition">

                <i class="ph ph-envelope"></i> niship505@gmail.com

            </a>

            <a href="tel:7737989802" class="px-4 py-2 bg-slate-900 text-white rounded-full text-xs font-bold hover:bg-indigo-600 transition">

                (773) 798-9802

            </a>

        </div>

    </nav>



    <header class="min-h-screen flex flex-col items-center justify-center pt-24 px-6 relative">

        <div class="data-mascot mb-8 relative">

            <svg width="180" height="180" viewBox="0 0 200 200" fill="none" xmlns="http://www.w3.org/2000/svg">

                <circle cx="100" cy="100" r="80" fill="url(#grad1)" />

                <path d="M60 85C60 76.1634 67.1634 69 76 69H124C132.837 69 140 76.1634 140 85V135C140 143.837 132.837 151 124 151H76C67.1634 151 60 143.837 60 135V85Z" fill="white"/>

                <circle cx="85" cy="100" r="8" fill="#4f46e5" class="eye" />

                <circle cx="115" cy="100" r="8" fill="#4f46e5" class="eye" />

                <rect x="80" y="125" width="40" height="6" rx="3" fill="#e2e8f0" />

                <path d="M100 40V60M70 45L85 62M130 45L115 62" stroke="#ec4899" stroke-width="6" stroke-linecap="round"/>

                <defs>

                    <linearGradient id="grad1" x1="0" y1="0" x2="200" y2="200">

                        <stop offset="0%" stop-color="#4f46e5" />

                        <stop offset="100%" stop-color="#ec4899" />

                    </linearGradient>

                </defs>

            </svg>

        </div>



        <div class="text-center max-w-5xl">

            <div class="inline-flex items-center gap-2 px-4 py-2 mb-6 rounded-full bg-indigo-50 border border-indigo-100 text-indigo-600 text-sm font-bold animate-pulse">

                <span class="w-2 h-2 rounded-full bg-indigo-500"></span> Currently Pursuing MS in Business Analytics

            </div>

            <h1 class="text-6xl md:text-8xl font-black mb-6 leading-[1.1] tracking-tight">

                Data Science meets <br/><span class="gradient-text">Management Strategy.</span>

            </h1>

            <p class="text-slate-500 text-xl md:text-2xl max-w-3xl mx-auto mb-10 font-medium leading-relaxed">

                I'm <span class="font-bold text-slate-800">Nishi Dineshkumar Patel</span>. Currently specializing in Analytics & Management Tools to transform complex data into executive decisions.

            </p>

            

            <div class="flex flex-wrap justify-center gap-6">

                <a href="#experience" class="btn-fancy flex items-center gap-2">

                    <i class="ph-bold ph-chart-line-up"></i> My Analytics Journey

                </a>

                <a href="https://www.linkedin.com/in/nishi-patel-948021257" target="_blank" class="px-8 py-4 bg-white border-2 border-slate-100 rounded-full font-bold text-slate-800 hover:border-indigo-600 hover:text-indigo-600 transition-all flex items-center gap-2">

                    <i class="ph-bold ph-linkedin-logo text-2xl"></i> Connect on LinkedIn

                </a>

            </div>

        </div>

    </header>



    <section class="py-20 px-6">

        <div class="max-w-6xl mx-auto grid grid-cols-1 md:grid-cols-3 gap-8">

            <div class="glass-card p-10 text-center pop-in">

                <div class="w-16 h-16 bg-blue-100 rounded-3xl flex items-center justify-center text-blue-600 mx-auto mb-6 text-3xl">

                    <i class="ph-fill ph-shield-check"></i>

                </div>

                <h3 class="text-5xl font-black text-slate-800 mb-2">98%</h3>

                <p class="text-slate-500 font-bold uppercase tracking-widest text-xs">Defect-Free Quality Assurance (TCS)</p>

            </div>

            <div class="glass-card p-10 text-center pop-in" style="transition-delay: 0.1s">

                <div class="w-16 h-16 bg-rose-100 rounded-3xl flex items-center justify-center text-rose-600 mx-auto mb-6 text-3xl">

                    <i class="ph-fill ph-timer"></i>

                </div>

                <h3 class="text-5xl font-black text-slate-800 mb-2">30%</h3>

                <p class="text-slate-500 font-bold uppercase tracking-widest text-xs">Automated Reporting Efficiency</p>

            </div>

            <div class="glass-card p-10 text-center pop-in" style="transition-delay: 0.2s">

                <div class="w-16 h-16 bg-amber-100 rounded-3xl flex items-center justify-center text-amber-600 mx-auto mb-6 text-3xl">

                    <i class="ph-fill ph-trend-up"></i>

                </div>

                <h3 class="text-5xl font-black text-slate-800 mb-2">12%</h3>

                <p class="text-slate-500 font-bold uppercase tracking-widest text-xs">Projected Sales Growth Modeling</p>

            </div>

        </div>

    </section>



    <section id="experience" class="py-24 px-6 bg-white/40">

        <div class="max-w-5xl mx-auto">

            <div class="flex flex-col md:flex-row justify-between items-end mb-16 gap-4">

                <div>

                    <span class="text-indigo-600 font-black uppercase tracking-[0.3em] text-xs">Professional Growth</span>

                    <h2 class="text-5xl font-black text-slate-900 mt-2">Core <span class="gradient-text">Experience.</span></h2>

                </div>

            </div>



            <div class="space-y-12 relative">

                <div class="absolute left-8 top-0 bottom-0 w-1 bg-slate-100 rounded-full hidden md:block"></div>



                <div class="relative pl-0 md:pl-24 group pop-in">

                    <div class="absolute left-4 md:left-[22px] top-0 w-8 h-8 bg-indigo-600 rounded-full border-4 border-white shadow-lg hidden md:block z-10 group-hover:scale-150 transition-all"></div>

                    <div class="glass-card p-10 hover:border-indigo-400">

                        <div class="flex flex-wrap justify-between items-start mb-6 gap-4">

                            <div>

                                <h3 class="text-2xl font-bold">Policy Research & Data Analytics Intern</h3>

                                <p class="text-indigo-600 font-bold">Rhode Island State Government</p>

                            </div>

                            <span class="px-4 py-1 bg-slate-900 text-white rounded-full text-xs font-bold">SEPT 2025 – DEC 2025</span>

                        </div>

                        <ul class="space-y-4 text-slate-600 font-medium">

                            <li class="flex gap-3 items-start"><i class="ph ph-check-circle text-emerald-500 text-xl mt-1"></i> Statistical evaluation of legislative datasets to identify socio-economic impact trends.</li>

                            <li class="flex gap-3 items-start"><i class="ph ph-check-circle text-emerald-500 text-xl mt-1"></i> Generating executive-ready reports for state-level strategic planning.</li>

                        </ul>

                    </div>

                </div>



                <div class="relative pl-0 md:pl-24 group pop-in">

                    <div class="absolute left-4 md:left-[22px] top-0 w-8 h-8 bg-rose-500 rounded-full border-4 border-white shadow-lg hidden md:block z-10 group-hover:scale-150 transition-all"></div>

                    <div class="glass-card p-10 hover:border-rose-400">

                        <div class="flex flex-wrap justify-between items-start mb-6 gap-4">

                            <div>

                                <h3 class="text-2xl font-bold">Quality Analytics Intern</h3>

                                <p class="text-rose-600 font-bold">Tata Consultancy Services (TCS)</p>

                            </div>

                            <span class="px-4 py-1 bg-slate-900 text-white rounded-full text-xs font-bold">JAN 2023 – JAN 2024</span>

                        </div>

                        <ul class="space-y-4 text-slate-600 font-medium">

                            <li class="flex gap-3 items-start"><i class="ph ph-check-circle text-emerald-500 text-xl mt-1"></i> Implemented RPA and Python scripts to reduce production cycle time by 15%.</li>

                            <li class="flex gap-3 items-start"><i class="ph ph-check-circle text-emerald-500 text-xl mt-1"></i> Developed dynamic Tableau KPI dashboards for real-time operations monitoring.</li>

                        </ul>

                    </div>

                </div>

            </div>

        </div>

    </section>



    <section id="projects" class="py-24 px-6">

        <div class="max-w-6xl mx-auto">

            <h2 class="text-4xl font-black mb-12 text-center">Selected <span class="gradient-text">Analytics Projects</span></h2>

            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">

                <div class="glass-card p-8 group">

                    <div class="text-4xl mb-4 group-hover:scale-125 transition-transform inline-block">📈</div>

                    <h3 class="text-xl font-bold mb-2">Nike Sales Forecasting</h3>

                    <p class="text-sm text-slate-500 mb-4 font-medium">Regression-based predictive model contributing to 12% revenue growth projection.</p>

                </div>

                <div class="glass-card p-8 group">

                    <div class="text-4xl mb-4 group-hover:scale-125 transition-transform inline-block">🔋</div>

                    <h3 class="text-xl font-bold mb-2">IoT Smart Energy</h3>

                    <p class="text-sm text-slate-500 mb-4 font-medium">Predictive consumption model reducing energy costs by 10% via real-time Tableau insights.</p>

                </div>

                <div class="glass-card p-8 group">

                    <div class="text-4xl mb-4 group-hover:scale-125 transition-transform inline-block">💄</div>

                    <h3 class="text-xl font-bold mb-2">Sephora Churn Analysis</h3>

                    <p class="text-sm text-slate-500 mb-4 font-medium">Engagement analysis identifying key drivers for repeat purchase behavior and customer retention.</p>

                </div>

            </div>

        </div>

    </section>



    <section class="py-24 px-6 bg-white/20">

        <div class="max-w-6xl mx-auto">

            <div class="grid grid-cols-1 lg:grid-cols-2 gap-12">

                <div class="glass-card p-12 relative overflow-hidden border-indigo-100">

                    <div class="flex items-center gap-4 mb-8">

                        <div class="w-14 h-14 bg-indigo-100 rounded-2xl flex items-center justify-center text-2xl shadow-sm">🎓</div>

                        <h2 class="text-3xl font-black">Academic <span class="text-indigo-600">Foundation</span></h2>

                    </div>

                    <div class="mb-8">

                        <div class="flex justify-between items-start mb-2">

                            <h3 class="text-xl font-bold leading-tight">Master of Science in Management <br/><span class="text-indigo-600">(Business Analytics)</span></h3>

                            <span class="px-3 py-1 bg-indigo-600 text-white rounded-full text-sm font-black whitespace-nowrap">3.5 GPA</span>

                        </div>

                        <p class="text-slate-500 font-bold">St. Francis College, Brooklyn, NY</p>

                        <p class="text-slate-400 font-semibold text-sm">Expected May 2026</p>

                    </div>

                    <div class="pt-6 border-t border-indigo-50">

                        <p class="text-[10px] font-black uppercase tracking-widest text-indigo-400 mb-4">Core Management Tools</p>

                        <div class="flex flex-wrap gap-2">

                            <span class="px-3 py-1 bg-white border border-slate-100 rounded-full text-[10px] font-bold">Python</span>

                            <span class="px-3 py-1 bg-white border border-slate-100 rounded-full text-[10px] font-bold">SQL</span>

                            <span class="px-3 py-1 bg-white border border-slate-100 rounded-full text-[10px] font-bold">Tableau</span>

                            <span class="px-3 py-1 bg-white border border-slate-100 rounded-full text-[10px] font-bold">RPA</span>

                            <span class="px-3 py-1 bg-white border border-slate-100 rounded-full text-[10px] font-bold">Statistical Analysis</span>

                        </div>

                    </div>

                </div>



                <div class="glass-card p-12 border-rose-100">

                    <div class="flex items-center gap-4 mb-8">

                        <div class="w-14 h-14 bg-rose-100 rounded-2xl flex items-center justify-center text-2xl shadow-sm">📜</div>

                        <h2 class="text-3xl font-black">Expert <span class="text-rose-600">Certs</span></h2>

                    </div>

                    <div class="grid grid-cols-1 gap-4">

                        <div class="p-5 bg-white/80 rounded-2xl border border-indigo-50 flex items-center justify-between group hover:border-indigo-400 transition-all">

                            <div class="flex items-center gap-4">

                                <i class="ph-fill ph-medal text-amber-500 text-2xl"></i>

                                <div>

                                    <p class="text-xs font-black text-slate-800">PMI-PBA Professional</p>

                                    <p class="text-[10px] text-slate-400 font-bold uppercase">Business Analysis (2025)</p>

                                </div>

                            </div>

                            <span class="text-[10px] font-bold text-indigo-500">41.5 Hrs</span>

                        </div>

                        

                        <div class="p-5 bg-white/80 rounded-2xl border border-indigo-50 flex items-center justify-between group hover:border-indigo-400 transition-all">

                            <div class="flex items-center gap-4">

                                <i class="ph-fill ph-briefcase text-blue-500 text-2xl"></i>

                                <div>

                                    <p class="text-xs font-black text-slate-800">Global Markets Analyst</p>

                                    <p class="text-[10px] text-slate-400 font-bold uppercase">Bank of America | Forage (2025)</p>

                                </div>

                            </div>

                            <span class="text-[10px] font-bold text-emerald-500">Completed</span>

                        </div>



                        <div class="p-5 bg-white/80 rounded-2xl border border-indigo-50 flex items-center justify-between group hover:border-indigo-400 transition-all">

                            <div class="flex items-center gap-4">

                                <i class="ph-fill ph-database text-indigo-500 text-2xl"></i>

                                <div>

                                    <p class="text-xs font-black text-slate-800">Big Data 101</p>

                                    <p class="text-[10px] text-slate-400 font-bold uppercase">IBM SkillsBuild (2025)</p>

                                </div>

                            </div>

                            <span class="text-[10px] font-bold text-indigo-500">Verified</span>

                        </div>



                        <div class="p-5 bg-white/80 rounded-2xl border border-indigo-50 flex items-center justify-between group hover:border-indigo-400 transition-all">

                            <div class="flex items-center gap-4">

                                <i class="ph-fill ph-certificate text-purple-500 text-2xl"></i>

                                <div>

                                    <p class="text-xs font-black text-slate-800">Business Intelligence & Analytics</p>

                                    <p class="text-[10px] text-slate-400 font-bold uppercase">Saylor Academy (88% Grade)</p>

                                </div>

                            </div>

                            <span class="text-[10px] font-bold text-indigo-500">46 Hrs</span>

                        </div>

                    </div>

                </div>

            </div>

        </div>

    </section>



    <footer class="py-20 px-6 text-center">

        <h2 class="text-4xl font-black mb-4 tracking-tight">Let's Connect for <span class="gradient-text">Strategic Opportunities.</span></h2>

        <p class="text-slate-500 font-medium mb-10">Based in Columbia, TN 38401 | Available for Global Relocation</p>

        

        <div class="flex flex-wrap justify-center gap-8">

            <a href="mailto:niship505@gmail.com" class="group text-center">

                <div class="w-14 h-14 bg-white rounded-2xl shadow-sm flex items-center justify-center text-xl mb-2 group-hover:bg-indigo-600 group-hover:text-white transition-all mx-auto">

                    <i class="ph ph-envelope-simple"></i>

                </div>

                <span class="text-[10px] font-bold text-slate-400 uppercase tracking-widest">Email</span>

            </a>

            <a href="https://www.linkedin.com/in/nishi-patel-948021257" target="_blank" class="group text-center">

                <div class="w-14 h-14 bg-white rounded-2xl shadow-sm flex items-center justify-center text-xl mb-2 group-hover:bg-indigo-600 group-hover:text-white transition-all mx-auto">

                    <i class="ph ph-linkedin-logo"></i>

                </div>

                <span class="text-[10px] font-bold text-slate-400 uppercase tracking-widest">LinkedIn</span>

            </a>

            <a href="tel:7737989802" class="group text-center">

                <div class="w-14 h-14 bg-white rounded-2xl shadow-sm flex items-center justify-center text-xl mb-2 group-hover:bg-indigo-600 group-hover:text-white transition-all mx-auto">

                    <i class="ph ph-phone"></i>

                </div>

                <span class="text-[10px] font-bold text-slate-400 uppercase tracking-widest">Call</span>

            </a>

        </div>

        

        <p class="mt-20 text-[10px] text-slate-400 font-bold uppercase tracking-[0.5em]">Nishi Dineshkumar Patel © 2026</p>

    </footer>



    <script>

        let scene, camera, renderer, particles;



        function init3D() {

            scene = new THREE.Scene();

            camera = new THREE.PerspectiveCamera(75, window.innerWidth / window.innerHeight, 0.1, 1000);

            renderer = new THREE.WebGLRenderer({ alpha: true, antialias: true });

            renderer.setSize(window.innerWidth, window.innerHeight);

            document.getElementById('canvas-container').appendChild(renderer.domElement);



            const geometry = new THREE.BufferGeometry();

            const vertices = [];

            for (let i = 0; i < 1500; i++) {

                vertices.push(

                    THREE.MathUtils.randFloatSpread(1500),

                    THREE.MathUtils.randFloatSpread(1500),

                    THREE.MathUtils.randFloatSpread(1500)

                );

            }

            geometry.setAttribute('position', new THREE.Float32BufferAttribute(vertices, 3));

            

            const material = new THREE.PointsMaterial({ 

                color: 0x6366f1, 

                size: 2, 

                transparent: true, 

                opacity: 0.3 

            });



            particles = new THREE.Points(geometry, material);

            scene.add(particles);



            camera.position.z = 500;

            animate();

        }



        function animate() {

            requestAnimationFrame(animate);

            particles.rotation.y += 0.0003;

            particles.rotation.x += 0.0001;

            renderer.render(scene, camera);

        }



        function initGSAP() {

            gsap.registerPlugin(ScrollTrigger);



            gsap.utils.toArray('.pop-in').forEach(el => {

                gsap.fromTo(el, 

                    { opacity: 0, y: 30, scale: 0.98 },

                    { 

                        scrollTrigger: {

                            trigger: el,

                            start: "top 90%",

                        },

                        opacity: 1, 

                        y: 0, 

                        scale: 1, 

                        duration: 0.8, 

                        ease: "power2.out"

                    }

                );

            });



            window.addEventListener('mousemove', (e) => {

                const eyes = document.querySelectorAll('.eye');

                const x = (e.clientX / window.innerWidth - 0.5) * 8;

                const y = (e.clientY / window.innerHeight - 0.5) * 8;

                eyes.forEach(eye => {

                    gsap.to(eye, { x: x, y: y, duration: 0.2 });

                });

            });

        }



        window.onload = () => {

            init3D();

            initGSAP();



            const icons = ['📊', '📉', '💼', '💡', '🔍', '⚙️'];

            for(let i=0; i<12; i++) {

                const el = document.createElement('div');

                el.className = 'floating-icon text-3xl select-none';

                el.innerText = icons[Math.floor(Math.random() * icons.length)];

                el.style.left = Math.random() * 90 + 'vw';

                el.style.top = Math.random() * 90 + 'vh';

                document.body.appendChild(el);

                

                gsap.to(el, {

                    y: "-=80",

                    x: "+=40",

                    rotation: 15,

                    duration: 15 + Math.random() * 15,

                    repeat: -1,

                    yoyo: true,

                    ease: "sine.inOut"

                });

            }

        };



        window.addEventListener('resize', () => {

            camera.aspect = window.innerWidth / window.innerHeight;

            camera.updateProjectionMatrix();

            renderer.setSize(window.innerWidth, window.innerHeight);

        });

    </script>

</body>

</html>
