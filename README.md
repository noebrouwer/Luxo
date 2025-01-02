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
        <div class="header-content">
            <h1>Welcome to Luxo Fashion</h1>
        </div>
    </header>

    <div class="main-container">
        <!-- Sidebar -->
        <nav class="sidebar">
            <ul>
                <li><a href="#">Man</a></li>
                <li><a href="#">Woman</a></li>
                <li><a href="#">Kids</a></li>
            </ul>
        </nav>

        <!-- Logo en leeg midden -->
        <div class="main-content">
            <img src="img/luxo-logo.png" alt="Luxo Logo" class="logo">
        </div>
    </div>

    <footer>
        <p>&copy; 2025 Luxo Fashion</p>
    </footer>

    <script src="scripts.js"></script> <!-- Verbindt de JavaScript-code -->
</body>
</html>
/* Algemene opmaak voor de body */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
}

/* Header styling */
header {
    background-color: #333;
    color: white;
    padding: 20px;
    text-align: center;
    position: absolute;
    width: 100%;
    top: 0;
}

header .header-content h1 {
    margin: 0;
}

/* Hoofdcontainer voor sidebar en inhoud */
.main-container {
    display: flex;
    justify-content: space-between;
    margin-top: 80px; /* Zorgt ervoor dat de inhoud niet achter de header zit */
    height: 90vh; /* Zorgt ervoor dat de inhoud binnen het scherm past */
}

/* Sidebar styling */
.sidebar {
    width: 20%;
    background-color: #333;
    padding-top: 20px;
    position: fixed;
    height: 100%;
    top: 80px; /* Zorgt ervoor dat de sidebar onder de header zit */
}

.sidebar ul {
    list-style-type: none;
    padding: 0;
}

.sidebar ul li {
    margin: 20px 0;
}

.sidebar ul li a {
    color: white;
    text-decoration: none;
    padding: 10px;
    display: block;
}

.sidebar ul li a:hover {
    background-color: #f4a261;
}

/* Hoofdinformatie - Logo */
.main-content {
    flex-grow: 1;
    display: flex;
    justify-content: center;
    align-items: center;
}

.logo {
    width: 300px; /* Pas de grootte van je logo aan */
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
