# Introduction to JavaScript and DOM Manipulation

## Objectives

Write basic JavaScript functions.
Manipulate the DOM dynamically.
Respond to user interactions.

## Instructions

- Create a script.js file and link it to a HTML.
- Structure the document using DOCTYPE, html, head, and body.

>[!NOTE]
>  - Write JavaScript that:
>  - Changes text content dynamically.
>  - Modifies CSS styles via JavaScript.
>  - Adds or removes an element when a button is clicked.

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Harrison's Footwear</title>
  <link rel="stylesheet" href="styles.css" />
</head>
<body>
  <header>
    <h1 id="site-title">Harrison's Footwear</h1>
    <nav>
      <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">Shop</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </nav>
  </header>

  <main>
    <section>
      <h2 id="promo-text">Welcome to the best shoe deals!</h2>
      <button id="changeTextBtn">Update Promo</button>
    </section>

    <section>
      <h3>Featured Product</h3>
      <article id="product">
        <img src="https://via.placeholder.com/150" alt="Black Sneakers" />
        <p>Black Sneakers - Comfortable and stylish</p>
        <button id="styleBtn">Highlight Product</button>
      </article>
    </section>

    <section>
      <h3>Customer Reviews</h3>
      <div id="reviews">
        <p>⭐⭐⭐⭐⭐ - Great quality!</p>
      </div>
      <button id="toggleReviewBtn">Add/Remove Review</button>
    </section>
  </main>

  <footer>
    <p>&copy; 2025 Harrison's Footwear. All rights reserved.</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>


script.js

// Change promo text dynamically
document.getElementById("changeTextBtn").addEventListener("click", () => {
  const promo = document.getElementById("promo-text");
  promo.textContent = "Huge Sale! Up to 50% off selected items!";
});

// Modify CSS style via JavaScript
document.getElementById("styleBtn").addEventListener("click", () => {
  const product = document.getElementById("product");
  product.style.backgroundColor = "#f0f8ff";
  product.style.border = "2px solid #333";
  product.style.padding = "10px";
  product.style.borderRadius = "10px";
});

// Add/Remove a review element
document.getElementById("toggleReviewBtn").addEventListener("click", () => {
  const reviews = document.getElementById("reviews");
  const existingReview = document.getElementById("new-review");

  if (existingReview) {
    existingReview.remove();
  } else {
    const newReview = document.createElement("p");
    newReview.id = "new-review";
    newReview.textContent = "⭐⭐⭐⭐ - Good value for money!";
    reviews.appendChild(newReview);
  }
});
# Tasks
- Create a well-structured HTML5 document.
- Use at least 5 different HTML elements.
- Ensure semantic correctness.

Happy Coding! 💻✨
