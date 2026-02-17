# ZED
Zed
<!DOCTYPE html>
<html lang="hi" class="dark">
<head>
    <meta charset="utf-8" />
    <meta content="width=device-width, initial-scale=1.0" name="viewport" />
    <title>Zed Chemistry - AI Lab</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;700;800&display=swap" rel="stylesheet" />
    <link href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:wght@400;700&display=swap" rel="stylesheet" />
    
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    colors: {
                        "primary": "#f4e225",
                        "bg-dark": "#000000",
                        "card-dark": "#111111",
                    }
                }
            }
        }
    </script>

    <style>
        body { font-family: 'Plus Jakarta Sans', sans-serif; background-color: #000; color: #fff; overflow-x: hidden; }
        
        /* Robot Container */
        #ai-robot {
            position: fixed; bottom: 80px; right: 20px; z-index: 100;
            width: 100px; height: 120px; transition: all 0.3s ease;
        }
        
        /* Robot Face */
        .robot-head {
            width: 80px; height: 70px; background: #f4e225; border-radius: 20px;
            position: relative; border: 4px solid #fff; box-shadow: 0 0 20px #f4e22555;
        }

        /* Eyes */
        .eye-socket { position: absolute; top: 20px; width: 20px; height: 20px; background: #000; border-radius: 50%; }
        .eye-left { left: 15px; } .eye-right { right: 15px; }
        .pupil {
            width: 8px; height: 8px; background: #fff; border-radius: 50%;
            position: absolute; top: 5px; left: 5px; transition: transform 0.1s linear;
        }

        /* Mouth */
        .mouth {
            position: absolute; bottom: 10px; left: 50%; transform: translateX(-50%);
            width: 30px; height: 8px; background: #000; border-radius: 10px; transition: all 0.2s;
        }

        /* Floating Animation */
        .float-anim { animation: floating 3s ease-in-out infinite; }
        @keyframes floating { 0%, 100% { transform: translateY(0); } 50% { transform: translateY(-15px); } }

        .glass-card { background: rgba(255, 255, 255, 0.05); backdrop-filter: blur(10px); border: 1px solid rgba(244, 226, 37, 0.2); }
    </style>
</head>

<body class="bg-bg-dark">

    <header class="sticky top-0 z-50 bg-black/80 backdrop-blur-lg border-b border-primary/20 px-6 py-4 flex items-center justify-between">
        <div class="flex items-center gap-3">
            <div class="size-10 bg-primary rounded-lg flex items-center justify-center rotate-3 shadow-[0_0_15px_#f4e225]">
                <span class="material-symbols-outlined text-black font-bold">science</span>
            </div>
            <h1 class="text-2xl font-800 tracking-tighter">ZED <span class="text-primary font-black">CHEMISTRY</span></h1>
        </div>
        <button class="bg-primary text-black px-4 py-2 rounded-full font-bold text-sm hover:scale-105 transition">MY LAB</button>
    </header>

    <main class="max-w-4xl mx-auto px-4 pt-8">
        <div class="relative overflow-hidden rounded-3xl bg-primary p-8 mb-10 text-black shadow-[0_20px_50px_rgba(244,226,37,0.2)]">
            <h2 class="text-4xl font-900 leading-tight mb-4">Hello Scientist!<br><span class="opacity-70 text-2xl">Robot AI is watching you...</span></h2>
            <p class="font-bold mb-6">Explore the world of Atoms & Reactions.</p>
            <div class="flex gap-4">
                <button class="bg-black text-white px-6 py-3 rounded-full font-bold hover:px-8 transition-all">Start Quiz</button>
                <button class="border-2 border-black px-6 py-3 rounded-full font-bold">View Notes</button>
            </div>
        </div>

        <div class="grid grid-cols-2 md:grid-cols-4 gap-4 mb-20">
            <div class="glass-card p-6 rounded-2xl text-center group hover:border-primary transition-all cursor-pointer">
                <span class="material-symbols-outlined text-primary text-4xl mb-2 group-hover:scale-125 transition">bolt</span>
                <p class="font-bold">Organic</p>
            </div>
            <div class="glass-card p-6 rounded-2xl text-center group hover:border-primary transition-all cursor-pointer">
                <span class="material-symbols-outlined text-primary text-4xl mb-2 group-hover:scale-125 transition">water_drop</span>
                <p class="font-bold">Solutions</p>
            </div>
            <div class="glass-card p-6 rounded-2xl text-center group hover:border-primary transition-all cursor-pointer">
                <span class="material-symbols-outlined text-primary text-4xl mb-2 group-hover:scale-125 transition">hub</span>
                <p class="font-bold">Atoms</p>
            </div>
            <div class="glass-card p-6 rounded-2xl text-center group hover:border-primary transition-all cursor-pointer">
                <span class="material-symbols-outlined text-primary text-4xl mb-2 group-hover:scale-125 transition">menu_book</span>
                <p class="font-bold">UP Board</p>
            </div>
        </div>
    </main>

    <div id="ai-robot" class="float-anim">
        <div class="robot-head">
            <div class="eye-socket eye-left"><div id="pupil-l" class="pupil"></div></div>
            <div class="eye-socket eye-right"><div id="pupil-r" class="pupil"></div></div>
            <div id="robot-mouth" class="mouth"></div>
        </div>
        <div class="w-12 h-4 bg-primary mx-auto mt-2 rounded-full border-2 border-white"></div>
    </div>

    <nav class="fixed bottom-6 left-1/2 -translate-x-1/2 w-[90%] max-w-md glass-card rounded-full p-2 flex items-center justify-between shadow-2xl z-50 border border-white/10">
        <a href="#" class="flex flex-col items-center p-3 text-primary">
            <span class="material-symbols-outlined">home</span>
        </a>
        <a href="#" class="flex flex-col items-center p-3 text-zinc-500 hover:text-primary transition">
            <span class="material-symbols-outlined">explore</span>
        </a>
        <a href="#" class="flex flex-col items-center p-3 text-zinc-500 hover:text-primary transition">
            <span class="material-symbols-outlined">science</span>
        </a>
        <a href="#" class="flex flex-col items-center p-3 text-zinc-500 hover:text-primary transition">
            <span class="material-symbols-outlined">person</span>
        </a>
    </nav>

    <script>
        const robot = document.getElementById('ai-robot');
        const mouth = document.getElementById('robot-mouth');
        const pupils = document.querySelectorAll('.pupil');

        document.addEventListener('mousemove', (e) => {
            const x = e.clientX;
            const y = e.clientY;

            // Pupil Movement Logic
            pupils.forEach(pupil => {
                const rect = pupil.getBoundingClientRect();
                const center = { x: rect.left + rect.width / 2, y: rect.top + rect.height / 2 };
                const angle = Math.atan2(y - center.y, x - center.x);
                const distance = Math.min(6, Math.hypot(x - center.x, y - center.y) / 50);
                
                const moveX = Math.cos(angle) * distance;
                const moveY = Math.sin(angle) * distance;
                pupil.style.transform = `translate(${moveX}px, ${moveY}px)`;
            });

            // Funny Expression Logic
            const robotRect = robot.getBoundingClientRect();
            const distToRobot = Math.hypot(x - (robotRect.left + 50), y - (robotRect.top + 60));

            if (distToRobot < 150) {
                mouth.style.height = "20px"; // Shocked Expression
                mouth.style.borderRadius = "50%";
                mouth.style.bottom = "5px";
            } else {
                mouth.style.height = "8px"; // Normal Expression
                mouth.style.borderRadius = "10px";
                mouth.style.bottom = "10px";
            }
        });

        // Click to make him "laugh"
        robot.addEventListener('click', () => {
            mouth.style.width = "50px";
            mouth.textContent = "😂";
            mouth.style.background = "transparent";
            setTimeout(() => {
                mouth.style.width = "30px";
                mouth.textContent = "";
                mouth.style.background = "#000";
            }, 2000);
        });
    </script>
</body>
</html>
