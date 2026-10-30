<!DOCTYPE html>  
<html lang="uz">  
<head>  
    <meta charset="UTF-8">  
    <meta name="viewport" content="width=device-width, initial-scale=1.0">  
    <title>Mening Mini Ilovam</title>  
    <!-- Telegram WebApp SDK -->  
    <script src="https://telegram.org/js/telegram-web-app.js"></script>  
    <style>  
        body {  
            font-family: Arial, sans-serif;  
            text-align: center;  
            padding: 40px;  
            background-color: var(--tg-theme-bg-color, #ffffff);  
            color: var(--tg-theme-text-color, #000000);  
        }  
        h1 {  
            font-size: 24px;  
        }  
        button {  
            background-color: var(--tg-theme-button-color, #2481cc);  
            color: var(--tg-theme-button-text-color, #ffffff);  
            border: none;  
            padding: 12px 20px;  
            font-size: 16px;  
            border-radius: 8px;  
            cursor: pointer;  
            margin-top: 20px;  
        }  
    </style>  
</head>  
<body>  
  
    <h1 id="greeting">Xush kelibsiz!</h1>  
    <p>Bu mening birinchi Telegram Mini Ilovam.</p>  
    <button id="btn">Tugmani bosing</button>  
  
    <script>  
        const tg = window.Telegram.WebApp;  
        tg.expand(); // Ilovani to'liq ekranga yoyish  
  
        // Agar foydalanuvchi Telegram'dan kirgan bo'lsa, ismini chiqarish  
        if (tg.initDataUnsafe && tg.initDataUnsafe.user) {  
            document.getElementById('greeting').innerText = `Salom, ${tg.initDataUnsafe.user.first_name}! 👋`;  
        }  
  
        // Tugma bosilganda xabar chiqarish  
        document.getElementById('btn').addEventListener('click', () => {  
            tg.showAlert("Tabriklayman! Mini ilovangiz ishlayapti! 🚀");  
        });  
    </script>  
  
</body>  
</html>  
