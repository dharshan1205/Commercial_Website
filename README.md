# Ex02 Commercial Website
## Date: 20/02/2026

## AIM
To create a commercial website using CSS Flexbox.

## ALGORITHM
### STEP 1
Create an HTML file (index.html)

### STEP 2
Create a CSS file (style.css)

### STEP 3
Include a navigation bar with links to different sections.

### STEP 4
Add structured sections for Homepage, Products / Services, About Us, Contact Details and User Account.

### STEP 5
Include social media links at the footer with copyright information.

### STEP 6
Define global styles for fonts, colors, and layout.

### STEP 7
Style the header, navigation bar, and sections.

### STEP 8
Use Flexbox for layout design.

### STEP 9
Add hover effects and transitions for interactivity.

### STEP 10
Add Images and Media.

### STEP 11
Use optimized images for a professional look.

### STEP 12
Open the HTML file in a browser to check layout and functionality.

### STEP 13
Fix styling issues and refine content placement.

### STEP 14
Deploy the website.

### STEP 15
Upload to GitHub Pages for free hosting.

## PROGRAM
## HTML
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Golden Whisk | Gourmet Dining</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <nav class="navbar">
        <div class="logo">Adharsh <span>Pasta</span></div>
        <ul class="nav-links">
            <li><a href="#menu">Menu</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
        <button class="res-btn">Book a Table</button>
    </nav>

    <header class="hero">
        <div class="hero-overlay">
            <h1>Fresh. Local. Delicious.</h1>
            <p>Experience the art of fine dining in a cozy atmosphere.</p>
            <a href="#menu" class="cta-btn">View Today's Menu</a>
        </div>
    </header>

    <section id="menu" class="menu-section">
        <h2 class="section-title">Our Signature Dishes</h2>
        <div class="menu-grid">
            
            <div class="menu-item">
                <div class="food-img">
                    <img src="15c699ca6e29a629c6394d372babd65b.jpg" alt="Truffle Pasta" width="400" height="200">
                </div>
                <div class="food-info">
                    <div class="food-header">
                        <h3>Truffle Pasta</h3>
                        <span class="price">₹459</span>
                    </div>
                    <p>Handmade pappardelle with black truffle cream and parmesan.</p>
                    <button class="add-btn">Add to Order</button>
                </div>
            </div>

            <div class="menu-item">
                <div class="food-img">
                    <img src="22dab159740ca06650e1b63765a81dca.jpg" alt="White Pasta" width="400" height="200">
                </div>
                <div class="food-info">
                    <div class="food-header">
                        <h3>White Pasta</h3>
                        <span class="price">₹349</span>
                    </div>
                    <p>Classic alfredo style with creamy garlic sauce and fresh herbs.</p>
                    <button class="add-btn">Add to Order</button>
                </div>
            </div>

            <div class="menu-item">
                <div class="food-img">
                    <img src="e76e94404755aa225ab7a5f8bfbf156b.jpg" alt="Spicy Chicken Pasta" width="400" height="200">
                </div>
                <div class="food-info">
                    <div class="food-header">
                        <h3>Spicy Chicken & Tomato Pasta</h3>
                        <span class="price">₹479</span>
                    </div>
                    <p>Zippy chicken served with a tangy tomato base and a touch of heat.</p>
                    <button class="add-btn">Add to Order</button>
                </div>
            </div>

        </div>
    </section>

    <script src="script.js"></script>
</body>
</html>
```
## CSS
```
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Georgia', serif;
}

/* Flex Navbar */
.navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 15px 10%;
    background: #1a1a1a;
    color: white;
}

.logo span { color: #f39c12; }

.nav-links {
    display: flex;
    list-style: none;
    gap: 40px;
}
}
.menu-section { padding: 80px 10%; }
.section-title { text-align: center; margin-bottom: 50px; font-size: 2.5rem; }

.menu-grid {
    display: flex;
    flex-wrap: wrap; /* Makes it responsive */
    gap: 30px;
    justify-content: center;
}

.menu-item {
    flex: 1 1 300px; /* Grow, Shrink, Base width */
    max-width: 400px;
    background: #fdfdfd;
    border: 1px solid #eee;
    box-shadow: 0 4px 10px rgba(0,0,0,0.05);
}

.food-img { height: 200px; width: 100%; }

.food-info { padding: 20px; }
.food-header {
    display: flex;
    justify-content: space-between;
    margin-bottom: 10px;
}

.price { color: #f39c12; font-weight: bold; }

.add-btn {
    margin-top: 15px;
    width: 100%;
    padding: 10px;
    background: #1a1a1a;
    color: white;
    border: none;
    cursor: pointer;
}
```
## JAVA SCRIPT
```
document.addEventListener('DOMContentLoaded', () => {
 
    const resBtn = document.querySelector('.res-btn');
    resBtn.addEventListener('click', () => {
        alert("Redirecting to our reservation system...");
    });

    const addButtons = document.querySelectorAll('.add-btn');
    addButtons.forEach(btn => {
        btn.addEventListener('click', (e) => {
            const itemName = e.target.closest('.food-info').querySelector('h3').innerText;
            btn.innerText = "✓ Added";
            btn.style.background = "#27ae60";
            
            console.log(`Added ${itemName} to the order list.`);
            
            setTimeout(() => {
                btn.innerText = "Add to Order";
                btn.style.background = "#1a1a1a";
            }, 1500);
        });
    });
});
```


## OUTPUT
<img width="1889" height="828" alt="image" src="https://github.com/user-attachments/assets/fb520a98-c839-4c74-a074-2040f831cf3d" />

<img width="1886" height="1096" alt="image" src="https://github.com/user-attachments/assets/bcabcfe2-1c5c-4784-920a-736b6bcb7a85" />


## RESULT
The program for creating commercial website using CSS Flexbox is executed successfully.
