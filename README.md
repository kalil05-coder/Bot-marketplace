# Bot-marketplace
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bot Marketplace</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 20px;
            background-color: #f4f4f4;
        }
        .container {
            max-width: 1200px;
            margin: 0 auto;
        }
        .bot-card {
            background: white;
            padding: 20px;
            margin: 10px 0;
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        .bot-card h2 {
            margin-top: 0;
            color: #333;
        }
        .price {
            color: #2ecc71;
            font-size: 1.2em;
            font-weight: bold;
        }
        .buy-btn {
            background: #3498db;
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        .buy-btn:hover {
            background: #2980b9;
        }
        .payment-options {
            margin-top: 10px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Marketplace de Bots - Binance Trading</h1>
        <p>Achetez des bots de trading optimisés pour Binance avec PayPal ou Crypto</p>

        <!-- Bot 1 -->
        <div class="bot-card">
            <h2>Bot Scalper Binance</h2>
            <p>Un bot de trading haute fréquence pour Binance, optimisé pour les petits profits rapides.</p>
            <p class="price">Prix: $99</p>
            <button class="buy-btn" onclick="showPayment('Scalper')">Acheter</button>
            <div class="payment-options" id="payment-scalper" style="display: none;">
                <h3>Options de paiement:</h3>
                <button onclick="payWithPaypal('Scalper', 99)">PayPal</button>
                <button onclick="payWithCrypto('Scalper', 99)">Crypto (BTC/ETH)</button>
            </div>
        </div>

        <!-- Bot 2 -->
        <div class="bot-card">
            <h2>Bot Trend Follower</h2>
            <p>Suit les tendances du marché sur Binance pour maximiser les gains à long terme.</p>
            <p class="price">Prix: $149</p>
            <button class="buy-btn" onclick="showPayment('Trend')">Acheter</button>
            <div class="payment-options" id="payment-trend" style="display: none;">
                <h3>Options de paiement:</h3>
                <button onclick="payWithPaypal('Trend', 149)">PayPal</button>
                <button onclick="payWithCrypto('Trend', 149)">Crypto (BTC/ETH)</button>
            </div>
        </div>
    </div>

    <script>
        function showPayment(botId) {
            const paymentDiv = document.getElementById(`payment-${botId.toLowerCase()}`);
            paymentDiv.style.display = paymentDiv.style.display === 'none' ? 'block' : 'none';
        }

        function payWithPaypal(botName, price) {
            // Intégration PayPal (à personnaliser avec votre ID client PayPal)
            alert(`Paiement PayPal pour ${botName} - $${price}. Redirection vers PayPal...`);
            // Exemple: window.location.href = 'https://www.paypal.com/...';
        }

        function payWithCrypto(botName, price) {
            // Logique pour paiement crypto (ex: générer une adresse wallet)
            alert(`Paiement Crypto pour ${botName} - $${price}. Veuillez envoyer à cette adresse: 1A1zP1eP5QGefi2DMPTfTL5SLmv7DivfNa`);
            // Intégrer une API comme Binance pour gérer les paiements crypto
        }
    </script>
</body>
</html>
