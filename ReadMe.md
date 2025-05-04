## Ex02 Commercial Website
## Date: 
## AIM
To create a commercial website using CSS Flexbox.

## ALGORITHM
STEP 1
Create an HTML file (index.html)

STEP 2
Create a CSS file (style.css)

STEP 3
Include a navigation bar with links to different sections.

STEP 4
Add structured sections for Homepage, Products / Services, About Us, Contact Details and User Account.

STEP 5
Include social media links at the footer with copyright information.

STEP 6
Define global styles for fonts, colors, and layout.

STEP 7
Style the header, navigation bar, and sections.

STEP 8
Use Flexbox for layout design.

STEP 9
Add hover effects and transitions for interactivity.

STEP 10
Add Images and Media.

STEP 11
Use optimized images for a professional look.

STEP 12
Open the HTML file in a browser to check layout and functionality.

STEP 13
Fix styling issues and refine content placement.

STEP 14
Deploy the website.

STEP 15
Upload to GitHub Pages for free hosting.

##PROGRAM
HTML
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Glamour Girls | Fancy Accessories</title>
  <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap">
</head>
<body>
  <div id="root"></div>
  <script type="module" src="/src/main.jsx"></script>
</body>
</html>
```
CSS:
```
/* Global Styles */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Poppins', sans-serif;
  }
  
  body {
    background-color: #fff5f7;
    color: #333;
  }
  
  /* Header */
  header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1.5rem 5%;
    background-color: #ff85a2;
    color: white;
    position: sticky;
    top: 0;
    z-index: 100;
    box-shadow: 0 2px 10px rgba(0,0,0,0.1);
  }
  
  .logo {
    font-size: 1.8rem;
    font-weight: 700;
    letter-spacing: 1px;
  }
  
  nav ul {
    display: flex;
    gap: 2rem;
    list-style: none;
  }
  
  nav li {
    cursor: pointer;
    font-weight: 600;
    transition: all 0.3s;
    padding: 0.5rem;
  }
  
  nav li:hover {
    transform: translateY(-3px);
    text-shadow: 0 2px 5px rgba(0,0,0,0.2);
  }
  
  /* Hero Section */
  .hero {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 70vh;
    background: linear-gradient(rgba(0,0,0,0.2), rgba(0,0,0,0.2)), 
                url('https://images.unsplash.com/photo-1551232864-3f0890e580d9') center/cover;
    color: white;
    text-align: center;
    padding: 0 2rem;
  }
  
  .hero h1 {
    font-size: 3.5rem;
    margin-bottom: 1.5rem;
    text-shadow: 0 2px 4px rgba(0,0,0,0.3);
  }
  
  .hero p {
    font-size: 1.3rem;
    margin-bottom: 2.5rem;
    max-width: 600px;
  }
  
  .shop-btn {
    background: white;
    color: #ff85a2;
    border: none;
    padding: 1rem 2.5rem;
    border-radius: 50px;
    font-weight: 700;
    font-size: 1.1rem;
    cursor: pointer;
    transition: all 0.3s;
    box-shadow: 0 4px 15px rgba(0,0,0,0.1);
  }
  
  .shop-btn:hover {
    transform: translateY(-3px);
    box-shadow: 0 6px 20px rgba(0,0,0,0.15);
  }
  
  /* Products Section */
  .products {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 2.5rem;
    padding: 4rem 5%;
    max-width: 1400px;
    margin: 0 auto;
  }
  
  .product-card {
    flex: 1 1 300px;
    max-width: 320px;
    background: white;
    border-radius: 15px;
    overflow: hidden;
    box-shadow: 0 5px 15px rgba(0,0,0,0.08);
    transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
  }
  
  .product-card:hover {
    transform: translateY(-10px) scale(1.02);
    box-shadow: 0 15px 30px rgba(255, 133, 162, 0.2);
  }
  
  .product-image {
    width: 100%;
    height: 250px;
    object-fit: cover;
    border-bottom: 1px solid #f0f0f0;
  }
  
  .product-info {
    padding: 1.5rem;
  }
  
  .product-info h3 {
    font-size: 1.3rem;
    margin-bottom: 0.8rem;
    color: #444;
  }
  
  .product-desc {
    color: #666;
    font-size: 0.95rem;
    margin-bottom: 1rem;
    line-height: 1.5;
  }
  
  .product-price {
    color: #ff85a2;
    font-weight: 700;
    font-size: 1.2rem;
    margin-bottom: 1.5rem;
  }
  
  .add-to-cart {
    background: #ff85a2;
    color: white;
    border: none;
    padding: 0.8rem;
    border-radius: 8px;
    cursor: pointer;
    width: 100%;
    font-weight: 600;
    font-size: 1rem;
    transition: all 0.3s;
  }
  
  .add-to-cart:hover {
    background: #ff6b8b;
    transform: translateY(-2px);
  }
  
  /* Footer */
  footer {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 2rem 5%;
    background-color: #333;
    color: white;
  }
  
  .social-links {
    display: flex;
    gap: 1.5rem;
  }
  
  .social-links span {
    cursor: pointer;
    transition: all 0.3s;
    font-weight: 600;
  }
  
  .social-links span:hover {
    color: #ff85a2;
    transform: translateY(-2px);
  }
  
  /* Responsive Design */
  @media (max-width: 768px) {
    header {
      flex-direction: column;
      padding: 1.5rem;
      gap: 1.5rem;
    }
  
    .hero h1 {
      font-size: 2.5rem;
    }
  
    .products {
      padding: 3rem 1rem;
      gap: 1.5rem;
    }
  
    footer {
      flex-direction: column;
      gap: 1.5rem;
      text-align: center;
    }
  }
```

## OUTPUT

![EX2MD](https://github.com/user-attachments/assets/34f1ec73-d3f9-41ac-9c83-bec2c026cd97)
![Ex2 1md](https://github.com/user-attachments/assets/3e9ac1fe-091a-49d1-a0f3-e2159119bc9c)

![Ex2 2](https://github.com/user-attachments/assets/2ce07756-b9c5-4d81-8c89-7070fcfd8c82)


## RESULT
The program for creating commercial website using CSS Flexbox is executed successfully.

