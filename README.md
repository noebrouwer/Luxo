<!DOCTYPE html>
<html lang="nl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Luxo Fashion</title>
    <link rel="stylesheet" href="styles.css"> <!-- Verbindt de CSS-stijl -->
</head>
<body>
    <header>
        <h1>Welcome to Luxo Fashion</h1>
        <nav>
            <ul>
                <li><a href="#">Home</a></li>
                <li><a href="#">Products</a></li>
                <li><a href="#">Contact</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <section class="product">
            <h2>Luxe T-shirt</h2>
            <img src="img/luxe-tshirt.jpg" alt="Luxe T-shirt">
            <p>Prijs: €59,99</p>
            <button class="add-to-cart">Toevoegen aan winkelwagentje</button>
        </section>

        <section class="product">
            <h2>Luxe Hoodie</h2>
            <img src="img/luxe-Hoodie.jpg" alt="Luxe Hoodie">
            <p>Prijs: €119,99</p>
            <button class="add-to-cart">Toevoegen aan winkelwagentje</button>
        </section>
    </main>

    <footer>
        <p>&copy; 2025 Luxo Fashion</p>
    </footer>

    <script src="scripts.js"></script> <!-- Verbindt de JavaScript-code -->
</body>
</html>
/* Algemene opmaak voor de body */
body {
    font-family: Arial, sans-serif;
    background-color: #f4f4f4;
    color: #333;
    margin: 0;
    padding: 0;
}

/* Header styling */
header {
    background-color: #333;
    color: white;
    padding: 20px;
    text-align: center;
}

header nav ul {
    list-style-type: none;
    padding: 0;
}

header nav ul li {
    display: inline;
    margin: 10px;
}

header nav ul li a {
    color: white;
    text-decoration: none;
}

/* Styling voor de productsectie */
.product {
    background-color: white;
    border-radius: 8px;
    margin: 20px;
    padding: 20px;
    text-align: center;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.product img {
    max-width: 100%;
    height: auto;
    border-radius: 8px;
}

.product button {
    background-color: #f4a261;
    color: white;
    padding: 10px 20px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}

.product button:hover {
    background-color: #e76f51;
}

/* Footer styling */
footer {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 10px;
    position: fixed;
    bottom: 0;
    width: 100%;
}
// Functie om een product toe te voegen aan het winkelwagentje
function addToCart(productName) {
    alert(`${productName} is toegevoegd aan je winkelwagentje!`);
}

// Event listener voor de knop "Toevoegen aan winkelwagentje"
const buttons = document.querySelectorAll('.add-to-cart');
buttons.forEach(button => {
    button.addEventListener('click', function() {
        const productName = this.previousElementSibling.previousElementSibling.textContent; // haalt de productnaam op
        addToCart(productName);
    });
});
