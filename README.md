# CSS3 Transitions, Animations, and Advanced JavaScript Functions

## Objectives

Create smooth CSS transitions and animations.
Use JavaScript functions for dynamic behavior.
Implement local storage for data persistence.

## Instructions
Add CSS animations to elements like buttons or images.

>[!NOTE]
> - Write a JavaScript function that:
> - Stores and retrieves user preferences using localStorage.
> - Implements an animation triggered by user actions.

## Tasks

Create a CSS animation.
Store data in localStorage.
Apply JavaScript to trigger animations.

Happy Coding! 💻✨
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Footwear Store</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>

    <div class="product">
        <h2>Comfortable Running Shoes</h2>
        <p>Click below to add to your cart</p>
        <button id="buyButton">Buy Now</button>
    </div>

    <script>
        // Check if the animation was already triggered
        if (!getUserPreference()) {
            const buyButton = document.getElementById('buyButton');

            // Trigger animation on button click
            buyButton.addEventListener('click', function () {
                buyButton.classList.add('animate');
                saveUserPreference(); // Save user preference to avoid repeating animation
            });
        } else {
            // If the user already clicked, no animation
            const buyButton = document.getElementById('buyButton');
            buyButton.classList.remove('animate');
        }
    </script>
</body>
</html>
