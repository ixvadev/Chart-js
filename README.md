# Chart.js

Quyida `Chart.js` yordamida chiziqli diagramma yaratish misoli keltirilgan.

## HTML

```html
<!DOCTYPE html>
<html lang="uz">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chart.js Misol</title>
    <!-- Chart.js CDN -->
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
</head>
<body>
    <!-- Diagramma uchun canvas elementi -->
    <canvas id="myChart" width="400" height="200"></canvas>

    <!-- JavaScript kodi -->
    <script>
        const ctx = document.getElementById('myChart').getContext('2d');
        const myChart = new Chart(ctx, {
            type: 'line', // Diagramma turi: chiziqli
            data: {
                labels: ['Yanvar', 'Fevral', 'Mart', 'Aprel', 'May', 'Iyun'],
                datasets: [{
                    label: 'Sotuvlar', // Ma'lumotlar seriyasining nomi
                    data: [12, 19, 3, 5, 2, 3], // Ma'lumotlar
                    backgroundColor: 'rgba(75, 192, 192, 0.2)', // Orqa fon rangi
                    borderColor: 'rgba(75, 192, 192, 1)', // Chiziq rangi
                    borderWidth: 1 // Chiziq qalinligi
                }]
            },
            options: {
                scales: {
                    y: {
                        beginAtZero: true // Y o'qini nol nuqtadan boshlash
                    }
                }
            }
        });
    </script>
</body>
</html>

Tavsif

Yuqoridagi HTML kod misolida Chart.js kutubxonasidan foydalanib, oddiy chiziqli diagramma yaratish ko’rsatilgan. Mana asosiy qadamlar:

	1.	Chart.js kutubxonasini qo’shish:
	•	HTML faylingizga Chart.js kutubxonasini CDN orqali ulaysiz. Bu esa diagramma yaratishda kerak bo’lgan barcha funksiyalarni ta’minlaydi.
	2.	Canvas elementini yaratish:
	•	canvas tegi diagramma chiziladigan joyni belgilaydi. id atributi bilan uni aniqlaymiz, masalan, id="myChart".
	3.	Diagramma yaratish:
	•	JavaScript yordamida Chart obyekti yaratiladi va u yerdan diagrammaning turi (line), ma’lumotlar (labels va datasets), va qo’shimcha sozlamalar (options) beriladi.

Ushbu misol Chart.js bilan ishlashning asosiy tushunchalarini beradi va oddiy diagrammalarni yaratishga yordam beradi.
