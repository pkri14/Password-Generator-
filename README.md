# Password-Generator-
## The challenge

Users should be able to:

- Generate a password based on the selected inclusion options
- Copy the generated password to the computer's clipboard
- See a strength rating for their generated password
- View the optimal layout for the interface depending on their device's screen size
- See hover and focus states for all interactive elements on the page
## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- JavaScript
- Dom

### What I learned

Working on the Random Password Generator project helped me strengthen my understanding of JavaScript and UI design principles:

- Generating Randomized Content with JavaScript
  I learned how to create random strings dynamically by combining character sets and iterating through them. This allowed me to customize password generation based on user-selected criteria.

```js
const lowercase = "abcdefghijklmnopqrstuvwxyz";
const uppercase = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
const numbers = "0123456789";
const specialChars = "!@#$%^&*()_+[]{}|;:,.<>?";

let characterPool = "";
if (includeUppercase) characterPool += uppercase;
if (includeLowercase) characterPool += lowercase;
if (includeNumbers) characterPool += numbers;
if (includeSymbols) characterPool += specialChars;

let password = "";
for (let i = 0; i < length; i++) {
  password += getRandomChar(characterPool);
}
Creating a Password Strength Meter
  I built a password strength meter using JavaScript and dynamically updated its visual feedback with CSS. This feature provided users with real-time guidance on the strength of their passwords.

```js
// Reset all boxes to default styles
boxes.forEach((box) => {
  box.style.backgroundColor = "transparent";
  box.style.border = `2px solid ${whiteColor}`; // Default border
});
// Set the color for boxes based on the strength
for (let i = 0; i < boxes.length; i++) {
  if (i < strength) {
    if (strength === 1) {
      boxes[i].style.backgroundColor = redColor;
    } else if (strength === 2) {
      boxes[i].style.backgroundColor = orangeColor;
    } else if (strength === 3) {
      boxes[i].style.backgroundColor = yellowColor;
    } else if (strength >= 4) {
      boxes[i].style.backgroundColor = greenColor;
    }
    boxes[i].style.border = "none"; // Remove border for active boxes
  } else {
    boxes[i].style.backgroundColor = "transparent"; // Reset the inactive boxes
  }
}

// Update the rating text based on strength
if (strength === 1) {
  rating.innerText = "too weak!";
} else if (strength === 2) {
  rating.innerText = "weak";
} else if (strength === 3) {
  rating.innerText = "medium";
} else if (strength >= 4) {
  rating.innerText = "strong";
}
```

This project not only solidified my JavaScript knowledge but also helped me understand how to implement intuitive UX/UI features that improve user interaction. I’m excited to carry these skills into future projects!

