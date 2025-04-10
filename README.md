# CSS Layouts and Responsive Design

## Objectives

Implement Flexbox and Grid for layout design.
Make the webpage responsive using media queries.
Ensure proper alignment and spacing.

## Instructions

- use Flexbox or CSS Grid.
- Add a navigation bar and structure the content.
- Use media queries to adjust layout for mobile, tablet, and desktop.

>[!NOTE]
>  - Include at least:
>  - navigation bar
>  - media queries

# Tasks

- Apply Flexbox or Grid for layout.
- Make the page responsive.
- Test across different screen sizes.

Happy Coding! 💻✨

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Layout with Flexbox and Grid</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <nav class="navbar">
            <ul>
                <li><a href="#">Home</a></li>
                <li><a href="#">About</a></li>
                <li><a href="#">Services</a></li>
                <li><a href="#">Contact</a></li>
            </ul>
        </nav>
    </header>

    <main class="main-content">
        <section class="intro">
            <h1>Welcome to Our Website</h1>
            <p>Discover our services and what we can do for you.</p>
        </section>

        <section class="grid-container">
            <div class="grid-item">Service 1</div>
            <div class="grid-item">Service 2</div>
            <div class="grid-item">Service 3</div>
        </section>
    </main>

    <footer>
        <p>&copy; 2025 Your Company</p>
    </footer>
</body>
</html>


/* Global Styles */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

header {
    background-color: #333;
    color: white;
    padding: 1rem;
}

.navbar ul {
    list-style-type: none;
    padding: 0;
    display: flex;
    justify-content: center;
}

.navbar li {
    margin: 0 1rem;
}

.navbar a {
    color: white;
    text-decoration: none;
}

/* Main Content Flexbox Layout */
.main-content {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 2rem;
}

/* Intro Section */
.intro {
    text-align: center;
    margin-bottom: 2rem;
}

/* Grid Layout for Services Section */
.grid-container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 1rem;
    width: 100%;
}

.grid-item {
    background-color: #f4f4f4;
    padding: 1rem;
    border: 1px solid #ccc;
    text-align: center;
}

/* Footer Styles */
footer {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 1rem;
}

/* Media Queries for Responsiveness */

/* Tablet */
@media (max-width: 768px) {
    .grid-container {
        grid-template-columns: repeat(2, 1fr);
    }
}

/* Mobile */
@media (max-width: 600px) {
    .navbar ul {
        flex-direction: column;
        text-align: center;
    }

    .grid-container {
        grid-template-columns: 1fr;
    }
}
