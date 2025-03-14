<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
    <meta name="apple-mobile-web-app-capable" content="yes">
    <meta name="apple-mobile-web-app-status-bar-style" content="black">
    <title>Tina's Coquito</title>
    <link href="https://fonts.googleapis.com/css2?family=Fredoka+One&family=Montserrat:wght@400;700&family=Sacramento&display=swap" rel="stylesheet">
    <style>
        body {
            margin: 0;
            font-family: 'Montserrat', sans-serif;
            background-color: #000;
            color: #fff;
            overflow-x: hidden;
            -webkit-font-smoothing: antialiased;
            -moz-osx-font-smoothing: grayscale;
        }

        /* Main Section */
        .main {
            background: #000;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 15px;
            box-sizing: border-box;
        }

        h1 {
            font-family: 'Sacramento', cursive;
            font-size: 3.5em;
            color: #ff6f91;
            margin: 0;
            text-shadow: 2px 2px 4px rgba(255, 255, 255, 0.1);
        }

        .subtitle {
            font-family: 'Fredoka One', cursive;
            font-size: 1.2em;
            color: #ff8c94;
            margin: 5px 0;
        }

        /* Legend */
        .legend {
            background: #222;
            padding: 10px;
            border-radius: 8px;
            max-width: 90%;
            margin: 8px auto;
            font-size: 0.85em;
            color: #ffcccb;
        }

        .legend p {
            margin: 3px 0;
        }

        /* Order Form */
        .order-form {
            background: #333;
            padding: 15px;
            border-radius: 12px;
            max-width: 90%;
            width: 100%;
            box-shadow: 0 5px 15px rgba(255, 255, 255, 0.1);
            margin-top: 10px;
            box-sizing: border-box;
        }

        form {
            display: flex;
            flex-direction: column;
            gap: 8px;
        }

        label {
            font-family: 'Fredoka One', cursive;
            font-size: 0.9em;
            color: #ff6f91;
            text-align: left;
        }

        input[type="text"],
        input[type="email"],
        input[type="tel"],
        input[type="number"] {
            padding: 8px;
            border: 2px solid #ffcccb;
            border-radius: 8px;
            font-size: 0.9em;
            background: #fff;
            width: 100%;
            box-sizing: border-box;
            -webkit-appearance: none;
            -moz-appearance: none;
            appearance: none;
        }

        input:focus {
            border-color: #ff6f91;
            outline: none;
        }

        /* Flavor Inputs */
        .flavor-inputs {
            display: flex;
            flex-direction: column;
            gap: 6px;
            max-height: 200px;
            overflow-y: auto;
            padding: 8px;
            background: #444;
            border-radius: 8px;
        }

        .flavor-row {
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .flavor-row label {
            flex: 1;
            text-align: left;
            color: #ffcccb;
            font-size: 0.85em;
        }

        .flavor-row input {
            width: 50px;
            text-align: center;
            font-size: 0.85em;
        }

        /* Bottle-Shaped Button */
        button {
            background: linear-gradient(135deg, #ff8c94, #ffb6c1);
            color: #fff;
            padding: 10px 20px;
            border: none;
            border-radius: 25px 25px 8px 8px;
            font-family: 'Fredoka One', cursive;
            font-size: 1.1em;
            cursor: pointer;
            box-shadow: 0 5px 10px rgba(255, 255, 255, 0.2);
            transition: transform 0.3s ease, background 0.3s ease;
            width: 100%;
            max-width: 200px;
            margin: 10px auto;
        }

        button:hover {
            background: linear-gradient(135deg, #ffb6c1, #ff8c94);
            transform: scale(1.05);
        }

        /* Footer */
        footer {
            background: #222;
            color: #ff6f91;
            text-align: center;
            padding: 8px;
            font-size: 0.7em;
        }

        /* iPhone Optimization */
        @media (max-width: 768px) {
            h1 {
                font-size: 2.8em;
            }

            .subtitle {
                font-size: 1em;
            }

            .legend {
                font-size: 0.75em;
                padding: 8px;
            }

            .order-form {
                padding: 12px;
            }

            label {
                font-size: 0.85em;
            }

            input[type="text"],
            input[type="email"],
            input[type="tel"],
            input[type="number"] {
                padding: 6px;
                font-size: 0.85em;
            }

            .flavor-row label {
                font-size: 0.8em;
            }

            .flavor-row input {
                width: 45px;
                font-size: 0.8em;
            }

            button {
                padding: 8px 15px;
                font-size: 1em;
                max-width: 180px;
            }
        }
    </style>
</head>
<body>
    <div class="main">
        <h1>Tina's Coquito</h1>
        <p class="subtitle">Homemade Holiday Magic</p>

        <div class="legend">
            <p>Price: $20 each or 3 for $50</p>
            <p>Enter quantity for each flavor</p>
            <p>Fill in your details and click Send</p>
        </div>

        <div class="order-form">
            <form id="orderForm">
                <label for="name">Name</label>
                <input type="text" id="name" name="name" placeholder="Your name" required>

                <label for="email">Email</label>
                <input type="email" id="email" name="email" placeholder="Your email" required>

                <label for="phone">Phone</label>
                <input type="tel" id="phone" name="phone" placeholder="Your phone" required>

                <label>Flavors</label>
                <div class="flavor-inputs">
                    <div class="flavor-row">
                        <label>Original</label>
                        <input type="number" name="Original" min="0" value="0">
                    </div>
                    <div class="flavor-row">
                        <label>Strawberry Swirl</label>
                        <input type="number" name="Strawberry Swirl" min="0" value="0">
                    </div>
                    <div class="flavor-row">
                        <label>Regular Strawberry</label>
                        <input type="number" name="Regular Strawberry" min="0" value="0">
                    </div>
                    <div class="flavor-row">
                        <label>Almond Joy</label>
                        <input type="number" name="Almond Joy" min="0" value="0">
                    </div>
                    <div class="flavor-row">
                        <label>Pistachio (Favorite)</label>
                        <input type="number" name="Pistachio" min="0" value="0">
                    </div>
                    <div class="flavor-row">
                        <label>Banana</label>
                        <input type="number" name="Banana" min="0" value="0">
                    </div>
                    <div class="flavor-row">
                        <label>Strawberry Banana</label>
                        <input type="number" name="Strawberry Banana" min="0" value="0">
                    </div>
                    <div class="flavor-row">
                        <label>Peanut Butter</label>
                        <input type="number" name="Peanut Butter" min="0" value="0">
                    </div>
                    <div class="flavor-row">
                        <label>Reese’s</label>
                        <input type="number" name="Reese’s" min="0" value="0">
                    </div>
                    <div class="flavor-row">
                        <label>Chocolate Banana</label>
                        <input type="number" name="Chocolate Covered Banana" min="0" value="0">
                    </div>
                    <div class="flavor-row">
                        <label>Nutella</label>
                        <input type="number" name="Nutella" min="0" value="0">
                    </div>
                </div>

                <button type="submit">Send</button>
            </form>
        </div>
    </div>

    <footer>
        <p>© 2023 Tina's Coquito</p>
    </footer>

    <script>
        document.getElementById('orderForm').addEventListener('submit', function(event) {
            event.preventDefault();

            // Collect user input
            const name = document.getElementById('name').value;
            const email = document.getElementById('email').value;
            const phone = document.getElementById('phone').value;

            // Collect flavor quantities
            const flavors = [
                'Original', 'Strawberry Swirl', 'Regular Strawberry', 'Almond Joy', 'Pistachio',
                'Banana', 'Strawberry Banana', 'Peanut Butter', 'Reese’s', 'Chocolate Covered Banana', 'Nutella'
            ];

            let orderDetails = [];
            let totalBottles = 0;
            let totalCost = 0;

            flavors.forEach(flavor => {
                const quantity = parseInt(document.querySelector(`input[name="${flavor}"]`).value);
                if (quantity > 0) {
                    orderDetails.push(`${flavor}: ${quantity}`);
                    totalBottles += quantity;
                }
            });

            // Calculate total cost
            if (totalBottles >= 3) {
                totalCost = Math.floor(totalBottles / 3) * 50 + (totalBottles % 3) * 20;
            } else {
                totalCost = totalBottles * 20;
            }

            // Format the email body
            const emailBody = `Order from: ${name}\n\n` +
                              `Contact Info:\n` +
                              `Email: ${email}\n` +
                              `Phone: ${phone}\n\n` +
                              `Order Details:\n` +
                              (orderDetails.length > 0 ? orderDetails.join('\n') : 'No flavors selected') + `\n\n` +
                              `Total Bottles: ${totalBottles}\n` +
                              `Total Cost: $${totalCost}\n\n` +
                              `Thank you for ordering from Tina's Coquito!`;

            // Create mailto link
            const mailtoLink = `mailto:aytmout@gmail.com?subject=Coquito Order from ${encodeURIComponent(name)}&body=${encodeURIComponent(emailBody)}`;
            window.location.href = mailtoLink;

            // Alert user
            alert('Check your email app to review and send your order to Tina!');
        });
    </script>
</body>
</html>
