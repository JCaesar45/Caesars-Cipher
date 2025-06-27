```
# ROT13 Cipher Decoder

## Unlock the Secrets of the Alphabet!

Welcome to the **ROT13 Cipher Decoder**, your trusty tool to unravel the mysteries hidden within encoded messages. Whether you're a cryptography enthusiast or just love puzzles, you've come to the right place!

---

## What is ROT13?

ROT13 is a simple yet fascinating cipher that shifts each letter by **13 places** in the alphabet. It’s a special case of the Caesar cipher and is often used for fun, puzzles, or hiding spoilers. A quick example:

- `A` ↔ `N`
- `B` ↔ `O`
- `C` ↔ `P`
- ...
- `Z` ↔ `M`

**Note:** All input is expected to be in uppercase, but the decoder is flexible with non-alphabetic characters like spaces, punctuation, and numbers — they stay the same!

---

## Our Magical Decoder Function

Here's the heart of our cipher decoder — a JavaScript function that takes an encoded message and reveals the original:

```javascript
function rot13(str) {
  return str.replace(/[A-Z]/g, function(char) {
    const code = char.charCodeAt(0);
    if (code >= 65 && code <= 90) {
      return String.fromCharCode(((code - 65 + 13) % 26) + 65);
    }
    return char; // Leave non-letters untouched
  });
}
``

---

## How to Use

Simply call the `rot13()` function with your message:

```javascript
console.log(rot13("SERR PBQR PNZC")); // Outputs: FREE CODE CAMP
``

---

## Sample Decoding Adventures

- **Puzzle:** `SERR CVMMN!`  
  **Decodes to:** `FREE PIZZA!`

- **Mystery:** `SERR YBIR?`  
  **Decodes to:** `FREE LOVE?`

- **Classic Phrase:**  
  `GUR DHVPX OEBJA SBK WHZCF BIRE GUR YNML QBT.`  
  **Decodes to:** `THE QUICK BROWN FOX JUMPS OVER THE LAZY DOG.`

---

## Why Use This?

- **Educational:** Learn how simple ciphers work.
- **Fun:** Decode secret messages and puzzles.
- **Practical:** Use as a playful encoding tool for your own messages.

---

## Get Creative!

Feel free to expand this script, incorporate it into your projects, or challenge friends with encoded messages. The power of the alphabet is in your hands!

---

## License

This cipher decoder is open-source and freely available for all your cryptographic adventures.

---

Enjoy decoding! 🚀🔓

---
