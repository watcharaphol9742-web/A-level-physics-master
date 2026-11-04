<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>A-Level Physics Master by lnwWR.</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Sarabun:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        body { font-family: 'Sarabun', sans-serif; }
    </style>
</head>
<body class="bg-slate-900 text-slate-100 min-h-screen flex flex-col justify-between">
    <div class="max-w-4xl mx-auto px-4 py-8 w-full">
        <header class="text-center mb-8">
            <h1 class="text-3xl font-bold text-teal-400 mb-2">⚡ A-Level Physics Master</h1>
            <p class="text-slate-400">ระบบฝึกทำโจทย์ฟิสิกส์เตรียมสอบ TCAS พร้อมเฉลยละเอียดและหน่วย SI มาตรฐาน</p>
        </header>

        <main id="app-container" class="bg-slate-800 border border-slate-700 rounded-2xl p-6 shadow-xl">
            <!-- Content will be rendered dynamically -->
            <div id="home-screen">
                <h2 class="text-xl font-semibold mb-4 text-teal-300">เลือกหัวข้อที่ต้องการฝึกฝน</h2>
                <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mb-6">
                    <button onclick="startQuiz('mechanics')" class="p-4 bg-slate-700 hover:bg-teal-600 transition rounded-xl text-left border border-slate-600">
                        <div class="font-bold text-lg">⚙️ กลศาสตร์ (Mechanics)</div>
                        <div class="text-sm text-slate-400">การเคลื่อนที่, แรง, งานและพลังงาน, โมเมนตัม</div>
                    </button>
                    <button onclick="startQuiz('waves')" class="p-4 bg-slate-700 hover:bg-teal-600 transition rounded-xl text-left border border-slate-600">
                        <div class="font-bold text-lg">🌊 คลื่นและแสง (Waves & Optics)</div>
                        <div class="text-sm text-slate-400">คลื่นกล, เสียง, แสงเชิงคลื่นและรังสี</div>
                    </button>
                    <button onclick="startQuiz('electricity')" class="p-4 bg-slate-700 hover:bg-teal-600 transition rounded-xl text-left border border-slate-600">
                        <div class="font-bold text-lg">⚡ ไฟฟ้าและแม่เหล็ก (Electricity)</div>
                        <div class="text-sm text-slate-400">ไฟฟ้าสถิต, ไฟฟ้ากระแส, แม่เหล็กไฟฟ้า</div>
                    </button>
                    <button onclick="startQuiz('thermodynamics')" class="p-4 bg-slate-700 hover:bg-teal-600 transition rounded-xl text-left border border-slate-600">
                        <div class="font-bold text-lg">🔥 ความร้อนและแก๊ส (Thermal Physics)</div>
                        <div class="text-sm text-slate-400">ความร้อน, ทฤษฎีจลน์ของแก๊ส, อุณหพลศาสตร์</div>
                    </button>
                    <button onclick="startQuiz('modern')" class="p-4 bg-slate-700 hover:bg-teal-600 transition rounded-xl text-left border border-slate-600">
                        <div class="font-bold text-lg">⚛️ ฟิสิกส์ยุคใหม่ (Modern Physics)</div>
                        <div class="text-sm text-slate-400">ควอนตัม, ฟิสิกส์อะตอม, ฟิสิกส์นิวเคลียร์</div>
                    </button>
                    <button onclick="startQuiz('challenge')" class="p-4 bg-teal-900/40 hover:bg-teal-800 transition rounded-xl text-left border border-teal-500">
                        <div class="font-bold text-lg text-teal-300">⚡ Challenge Mode (รวมทุกบท)</div>
                        <div class="text-sm text-teal-400">ทดสอบความพร้อมเสมือนสอบจริง</div>
                    </button>
                </div>
                
                <div class="grid grid-cols-1 sm:grid-cols-2 gap-4 mb-6">
                    <div>
                        <label class="block text-sm text-slate-400 mb-2">จำนวนข้อสอบ:</label>
                        <select id="question-count" class="w-full bg-slate-700 border border-slate-600 rounded-lg p-2 text-white">
                            <option value="5">5 ข้อ</option>
                            <option value="10">10 ข้อ</option>
                            <option value="20">20 ข้อ</option>
                            <option value="30" selected>30 ข้อ</option>
                        </select>
                    </div>
                    <div>
                        <label class="block text-sm text-slate-400 mb-2">เวลาในการทำ:</label>
                        <select id="timer-duration" class="w-full bg-slate-700 border border-slate-600 rounded-lg p-2 text-white">
                            <option value="15">15 นาที</option>
                            <option value="30">30 นาที</option>
                            <option value="45">45 นาที</option>
                            <option value="60" selected>60 นาที</option>
                        </select>
                    </div>
                </div>
            </div>
        </main>

        <footer class="text-center mt-8 text-slate-500 text-sm">
            by lnwWR.
        </footer>
    </div>

    <script>
        function startQuiz(topic) {
            const count = document.getElementById('question-count').value;
            const timer = document.getElementById('timer-duration').value;
            alert(`เริ่มทำข้อสอบหมวด: ${topic} | จำนวน ${count} ข้อ | เวลา ${timer} นาที (คุณสามารถนำโค้ดนี้ไปวางใน Netlify Drop เพื่อสร้างลิงก์ส่วนตัวได้ทันทีครับ)`);
        }
    </script>
</body>
</html>
