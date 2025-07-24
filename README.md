# Planet_education
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>منصة تنظيم القراية</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="style.css">
</head>
<body class="bg-gray-100 font-sans">
<header class="bg-blue-600 text-white p-4 text-center text-xl font-bold flex justify-between items-center">
    📚 منصتي لتنظيم القراية
    <button onclick="toggleDarkMode()" class="bg-gray-800 px-4 py-1 rounded">🌙</button>
</header>

<div class="max-w-4xl mx-auto p-4 grid gap-6">
    <!-- أهداف يومية -->
    <section class="bg-white shadow-md p-4 rounded-xl">
        <h2 class="text-xl font-semibold mb-2">🎯 أهدافي اليومية</h2>
        <div class="flex gap-2">
            <input type="text" id="goalInput" placeholder="أكتب هدفك..." class="border rounded-lg p-2 flex-1">
            <button onclick="addGoal()" class="bg-blue-600 text-white px-4 py-2 rounded-lg">أضف</button>
        </div>
        <ul id="goalList" class="mt-3 space-y-2"></ul>
    </section>

    <!-- جدول مراجعة -->
    <section class="bg-white shadow-md p-4 rounded-xl">
        <h2 class="text-xl font-semibold mb-2">📅 جدول المراجعة</h2>
        <table class="w-full border border-gray-300 text-center">
            <thead class="bg-gray-200">
                <tr>
                    <th class="p-2">المادة</th>
                    <th class="p-2">المدة</th>
                    <th class="p-2">الحالة</th>
                </tr>
            </thead>
            <tbody id="schedule">
                <tr>
                    <td class="p-2">رياضيات</td>
                    <td class="p-2">2 ساعات</td>
                    <td class="p-2 text-green-500">✅</td>
                </tr>
                <tr>
                    <td class="p-2">فيزياء</td>
                    <td class="p-2">1 ساعة</td>
                    <td class="p-2 text-yellow-500">⏳</td>
                </tr>
            </tbody>
        </table>
    </section>

    <!-- مؤقت Pomodoro -->
    <section class="bg-white shadow-md p-4 rounded-xl text-center">
        <h2 class="text-xl font-semibold mb-4">⏱ جلسة تركيز</h2>
        <div id="timer" class="text-3xl font-bold mb-4">25:00</div>
        <button onclick="startTimer()" class="bg-green-500 text-white px-4 py-2 rounded-lg">ابدأ</button>
        <button onclick="resetTimer()" class="bg-red-500 text-white px-4 py-2 rounded-lg ml-2">إعادة</button>
    </section>

    <!-- الامتحانات القادمة -->
    <section class="bg-white shadow-md p-4 rounded-xl">
        <h2 class="text-xl font-semibold mb-2">📌 الامتحانات القادمة</h2>
        <div class="flex gap-2">
            <input type="text" id="examName" placeholder="اسم الامتحان" class="border rounded-lg p-2 flex-1">
            <input type="date" id="examDate" class="border rounded-lg p-2">
            <button onclick="addExam()" class="bg-purple-600 text-white px-4 py-2 rounded-lg">أضف</button>
        </div>
        <ul id="examList" class="mt-3 space-y-2"></ul>
    </section>
</div>

<script src="script.js"></script>
</body>
</html>
