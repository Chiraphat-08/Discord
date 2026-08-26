<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chearavanon City - Discord Community Portal</title>

    <!-- Meta Tags สำหรับการแชร์ลิงก์บน Discord / Facebook / LINE -->
    <meta name="theme-color" content="#5865F2">
    <meta property="og:title" content="Chearavanon City - Discord Portal">
    <meta property="og:description" content="พูดคุย แลกเปลี่ยนความคิดเห็น และรับข่าวสารใหม่ๆ พร้อมกิจกรรมต่างๆ เข้าร่วมคอมมูนิตี้กับเราได้ทันที">
    <meta property="og:type" content="website">
    <meta property="og:image" content="https://assets-global.website-files.com/6257adef93867e50d84d30e2/636e0a6a49cf127bf92de1e2_icon_clyde_blurple_RGB.png">
    
    <!-- Favicon ไอคอนส่วนหัวของแท็บเว็บ -->
    <link rel="icon" type="image/svg+xml" href="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 127.14 96.36'><path fill='%235865F2' d='M107.7 8.07A105.15 105.15 0 0 0 81.47 0a72.06 72.06 0 0 0-3.36 6.83 97.68 97.68 0 0 0-29.11 0A72.37 72.37 0 0 0 45.64 0a105.89 105.89 0 0 0-26.25 8.09C2.79 32.65-1.71 56.6.54 80.21a105.73 105.73 0 0 0 32.17 16.15 77.7 77.7 0 0 0 6.89-11.11 68.42 68.42 0 0 1-10.85-5.18c.91-.66 1.8-1.34 2.66-2a75.57 75.57 0 0 0 64.32 0c.87.68 1.76 1.36 2.66 2a68.68 68.68 0 0 1-10.87 5.19 77 77 0 0 0 6.89 11.1 105.25 105.25 0 0 0 32.19-16.14c2.64-27.38-4.51-51.11-18.9-72.15ZM42.45 65.69c-6.23 0-11.33-5.72-11.33-12.75s5-12.75 11.33-12.75c6.38 0 11.44 5.76 11.33 12.75 0 7.03-4.96 12.75-11.33 12.75Zm42.24 0c-6.24 0-11.34-5.72-11.34-12.75s5.01-12.75 11.34-12.75c6.38 0 11.44 5.76 11.34 12.75 0 7.03-4.96 12.75-11.34 12.75Z'/></svg>">

    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Font Awesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Font - Kanit & Inter -->
    <link href="https://fonts.googleapis.com/css2?family=Kanit:wght@300;400;500;600;700&family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
    
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Kanit', 'Inter', 'sans-serif'],
                    },
                    colors: {
                        discord: {
                            500: '#5865F2',
                            600: '#4752C4',
                            700: '#3c45a5',
                        }
                    }
                }
            }
        }
    </script>
    <style>
        body {
            font-family: 'Kanit', sans-serif;
            -webkit-tap-highlight-color: transparent;
            touch-action: manipulation;
        }
        .discord-glow {
            box-shadow: 0 0 35px -5px rgba(88, 101, 242, 0.4);
        }
        @media (max-width: 640px) {
            .discord-glow {
                box-shadow: 0 0 25px -5px rgba(88, 101, 242, 0.3);
            }
        }
    </style>
</head>
<body class="bg-slate-950 text-slate-100 min-h-[100dvh] flex flex-col justify-between selection:bg-discord-500 selection:text-white antialiased">

    <!-- Toast Notification สำหรับแจ้งเตือนการคัดลอกลิงก์ -->
    <div id="copyToast" class="fixed top-5 left-1/2 -translate-x-1/2 z-50 bg-emerald-500 text-white px-5 py-3 rounded-2xl shadow-xl flex items-center gap-2 text-sm font-medium transition-all duration-300 opacity-0 pointer-events-none translate-y-[-20px]">
        <i class="fa-solid fa-circle-check text-lg"></i>
        <span>คัดลอกลิงก์ Discord เรียบร้อยแล้ว!</span>
    </div>

    <!-- ========================================== -->
    <!-- HEADER / NAVIGATION BAR                    -->
    <!-- ========================================== -->
    <header class="sticky top-0 z-40 bg-slate-900/90 backdrop-blur-md border-b border-slate-800/80">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 h-16 flex items-center justify-between">
            <!-- โลโก้เว็บไซต์ -->
            <div class="flex items-center gap-2.5 sm:gap-3">
                <div class="w-9 h-9 sm:w-10 sm:h-10 rounded-xl bg-discord-500 flex items-center justify-center text-white shadow-lg shadow-discord-500/30 shrink-0">
                    <i class="fa-brands fa-discord text-xl sm:text-2xl"></i>
                </div>
                <span class="font-bold text-lg sm:text-xl tracking-wide bg-clip-text text-transparent bg-gradient-to-r from-white to-slate-400 truncate max-w-[180px] sm:max-w-none">
                    Discord Community
                </span>
            </div>

            <!-- ปุ่มขวามือบน Navbar -->
            <div class="flex items-center gap-2">
                <!-- 📍 [จุดใส่ลิงก์ Discord 1] เปลี่ยน href="URL_Discord_ของคุณ" -->
                <a href="https://discord.gg/gepYnwyZx" target="_blank" rel="noopener noreferrer"
                   class="px-3.5 sm:px-5 py-2 rounded-xl text-xs sm:text-sm font-semibold text-white bg-discord-500 hover:bg-discord-600 shadow-md shadow-discord-500/20 transition-all active:scale-95 flex items-center gap-1.5 sm:gap-2 select-none">
                    <i class="fa-brands fa-discord text-base sm:text-lg"></i>
                    <span>เข้าสู่ Discord</span>
                </a>
            </div>
        </div>
    </header>

    <!-- ========================================== -->
    <!-- HERO SECTION                               -->
    <!-- ========================================== -->
    <main class="flex-1 flex flex-col items-center justify-center relative overflow-hidden py-10 sm:py-20 px-4">
        <!-- แสงฟุ้งพื้นหลังสี Discord -->
        <div class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-[300px] sm:w-[550px] h-[300px] sm:h-[550px] bg-discord-500/15 rounded-full blur-3xl pointer-events-none"></div>

        <div class="w-full max-w-4xl mx-auto text-center relative z-10">
            <!-- ป้ายสถานะออนไลน์ -->
            <div class="inline-flex items-center gap-2 px-3.5 py-1.5 rounded-full text-xs font-semibold bg-discord-500/10 text-discord-500 border border-discord-500/20 mb-6 sm:mb-8">
                <span class="w-2.5 h-2.5 rounded-full bg-emerald-400 animate-pulse"></span>
                เข้าร่วมคอมมูนิตี้กับเราบน Discord
            </div>

            <!-- หัวข้อหลัก -->
            <h1 class="text-3xl sm:text-6xl font-extrabold tracking-tight text-white mb-4 sm:mb-6 leading-tight">
                ✿｡WELCOME｡✿ <br>
                <span class="bg-clip-text text-transparent bg-gradient-to-r from-indigo-400 via-discord-500 to-purple-400">
                    Chearavanon City
                </span>
            </h1>

            <p class="text-sm sm:text-xl text-slate-400 max-w-2xl mx-auto mb-8 sm:mb-10 leading-relaxed font-light px-2">
                พูดคุย แลกเปลี่ยนความคิดเห็น และรับข่าวสารใหม่ๆ พร้อมกิจกรรมต่างๆได้แล้ววันนี้ กดปุ่มด้านล่างเพื่อเข้าร่วมได้ทันที
            </p>

            <!-- การ์ดปุ่มกดหลักสำหรับเข้า Discord -->
            <div class="w-full max-w-md mx-auto bg-slate-900/90 border border-slate-800 p-6 sm:p-8 rounded-3xl shadow-2xl backdrop-blur-sm discord-glow">
                <div class="w-16 h-16 sm:w-20 sm:h-20 bg-discord-500/20 text-discord-500 rounded-2xl mx-auto flex items-center justify-center text-3xl sm:text-4xl mb-5 sm:mb-6 border border-discord-500/30">
                    <i class="fa-brands fa-discord"></i>
                </div>

                <h2 class="text-xl sm:text-2xl font-bold text-white mb-1.5">Discord Server</h2>
                <p class="text-xs sm:text-sm text-slate-400 mb-6">คลิกปุ่มด้านล่างเพื่อเข้าร่วมกลุ่ม</p>

                <!-- ปุ่มหลักกดเข้าร่วม -->
                <!-- 📍 [จุดใส่ลิงก์ Discord 2] เปลี่ยน href="URL_Discord_ของคุณ" -->
                <a href="https://discord.gg/gepYnwyZx" target="_blank" rel="noopener noreferrer"
                   class="w-full py-3.5 sm:py-4 px-6 rounded-2xl font-semibold text-white bg-discord-500 hover:bg-discord-600 active:scale-95 shadow-lg shadow-discord-500/30 transition-all duration-200 flex items-center justify-center gap-3 text-base sm:text-lg group select-none mb-3">
                    <i class="fa-brands fa-discord text-xl sm:text-2xl group-hover:scale-110 transition-transform"></i>
                    <span>เข้าร่วม Discord ตอนนี้</span>
                    <i class="fa-solid fa-arrow-right text-xs sm:text-sm transition-transform group-hover:translate-x-1"></i>
                </a>

                <!-- ปุ่มคัดลอกลิงก์สำหรับมือถือ -->
                <button onclick="copyDiscordLink()" 
                        class="w-full py-3 px-4 rounded-xl font-medium text-slate-300 bg-slate-800/80 hover:bg-slate-800 active:scale-95 border border-slate-700/60 transition-all text-xs sm:text-sm flex items-center justify-center gap-2 select-none">
                    <i class="fa-regular fa-copy text-slate-400"></i>
                    <span>คัดลอกลิงก์เชิญ (Copy Link)</span>
                </button>

                <!-- แสดงข้อความบอกตำแหน่ง URL -->
                <div class="mt-5 pt-4 border-t border-slate-800/80 text-[11px] sm:text-xs text-slate-500 font-mono break-all">
                    📍 Link: <span id="discordUrlText">https://discord.gg/gepYnwyZx</span>
                </div>
            </div>
        </div>
    </main>

    <!-- ฟังก์ชัน JavaScript สำหรับคัดลอกลิงก์บนมือถือ -->
    <script>
        function copyDiscordLink() {
            const url = "https://discord.gg/gepYnwyZx";
            
            // ใช้ execCommand หรือ clipboard API เพื่อคัดลอก
            if (navigator.clipboard && window.isSecureContext) {
                navigator.clipboard.writeText(url);
            } else {
                const textArea = document.createElement("textarea");
                textArea.value = url;
                document.body.appendChild(textArea);
                textArea.select();
                document.execCommand('copy');
                document.body.removeChild(textArea);
            }

            // แสดง Toast แจ้งเตือน
            const toast = document.getElementById("copyToast");
            toast.classList.remove("opacity-0", "pointer-events-none", "translate-y-[-20px]");
            toast.classList.add("opacity-100", "translate-y-0");

            setTimeout(() => {
                toast.classList.remove("opacity-100", "translate-y-0");
                toast.classList.add("opacity-0", "pointer-events-none", "translate-y-[-20px]");
            }, 2500);
        }
    </script>

    <!-- ========================================== -->
    <!-- FOOTER SECTION                             -->
    <!-- ========================================== -->
    <footer class="bg-slate-950 border-t border-slate-900/80 py-6 text-slate-500 text-xs">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 flex flex-col sm:flex-row items-center justify-between gap-3 text-center sm:text-left">
            <div class="flex items-center gap-2 text-slate-400 font-medium">
                <i class="fa-brands fa-discord text-discord-500"></i>
                <span>Discord Portal</span>
            </div>

            <!-- 📍 [จุดใส่ลิงก์ Discord 3] เปลี่ยน href="URL_Discord_ของคุณ" -->
            <div>
                <a href="https://discord.gg/gepYnwyZx" target="_blank" rel="noopener noreferrer" class="hover:text-discord-500 transition-colors py-1 inline-block">
                    <i class="fa-brands fa-discord mr-1"></i> เข้าร่วม Discord Server
                </a>
            </div>

            <p>© 2026 Discord Community Page. All rights reserved.</p>
        </div>
    </footer>

</body>
</html>
