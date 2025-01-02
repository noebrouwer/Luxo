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
        <div class="logo">
            <img src="img/luxo-logo.png" alt="Luxo Logo">
        </div>
        <nav>
            <ul>
                <li><a href="#">Home</a></li>
                <li><a href="#">Contact</a></li>
                <li><a href="#">Men</a></li>
                <li><a href="#">Woman</a></li>
                <li><a href="#">Kids</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <section class="intro">
            <h2>Welcome to Luxo Fashion</h2>
            <p>Luxo' where comfort meets class</p>
        </section>

        <section class="products">
            <h3>Onze producten</h3>
            <div class="product">
                <img src="img/T-shirt.jpg" alt=" T-shirt">
                <h4> T-shirt</h4>
                <p>Prijs: €64,99</p>
                <button class="add-to-cart">Toevoegen aan winkelwagentje</button>
            </div>
            <div class="product">
                <img src="img/hoodie.jpg" alt=" Hoodie">
                <h4> Hoodie</h4>
                <p>Prijs: €129,99</p>
                <button class="add-to-cart">Toevoegen aan winkelwagentje</button>
            </div>
            <div class="product">
                <img src="img/Sweatpants.jpg" alt=" Sweatpants">
                <h4> Sweatpants</h4>
                <p>Prijs: €129,99</p>
                <button class="add-to-cart">Toevoegen aan winkelwagentje</button>
            </div>
        </section>
    </main>

    <footer>
        <p>&copy; 2025 Luxo Fashion | Alle rechten voorbehouden</p>
    </footer>

    <script src="scripts.js"></script> <!-- Verbindt de JavaScript-code -->
</body>
</html>
/* Algemene opmaak */
body {
    font-family: Arial, sans-serif;
    background-color: #f4f4f4;
    margin: 0;
    padding: 0;
    color: #333;
}

/* Header styling */
header {
    background-color: #000080;
    color: white;
    padding: 20px;
    text-align: center;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 10px 20px;
}

header .logo img {
    width: 150px;
}

header nav ul {
    list-style-type: none;
    padding: 0;
    margin: 0;
    display: flex;
}

header nav ul li {
    margin: 0 15px;
}

header nav ul li a {
    color: white;
    text-decoration: none;
    font-weight: bold;
}

/* Main content */
main {
    padding: 20px;
}

/* Introductie sectie */
.intro {
    text-align: center;
    margin-bottom: 40px;
}

/* Product sectie */
.products {
    display: flex;
    justify-content: space-around;
    flex-wrap: wrap;
}

.product {
    background-color: white;
    border-radius: 8px;
    margin: 15px;
    padding: 20px;
    text-align: center;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    width: 250px;
}

.product img {
    width: 100%;
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
    margin-top: 10px;
}

.product button:hover {
    background-color: #e76f51;
}

/* Footer */
footer {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 10px;
    margin-top: 40px;
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
/projectmap
    /img
        T-shirt.jpg
        Hoodie.jpg
        Sweatpants.jpg
        luxo-logo.png
    index.html
    styles.css
    scripts.js

