---
title: Pseudocode & Comments
description: This is a post on My Blog creating pseudocodes and comments for 
date: 2018-07-04
tags:
  - Pseudocode
---

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Code Comments</title>
</head>
<body>

  <script>
    // Task 1

    // Define a function to calculate the percentage of a number
    function percentageCalculator(number, percentage) {
      const result = (percentage / 100) * number; // Calculate the result by multiplying the number with the percentage divided by 100
      return result; // Return the calculated percentage
    }

    // Define the number and percentage values
    const number = 135;
    const percentage = 30;

    // Call the percentageCalculator function with the given number and percentage
    const calculatedPercentage = percentageCalculator(number, percentage);

    // Output the result
    console.log(`${percentage}% of ${number} is ${calculatedPercentage}`);
  </script>
</body>
</html>



// Task 2

// 1.Reading List

// Create an array of book objects called "books"

// For each book in "books":
//     Log the book's title and author
//     If the book is already completed:
//         Log: "You already read {book.title} by {book.author}"
//     Else:
//         Log: "You still need to read {book.title} by {book.author}"

// 2. Recipe

// Create an object called "favoriteRecipes" with properties:
//     - recipeTitle (a string)
//     - servings (a number)
//     - ingredients (an array of strings)
//     - directions (a string)

// For each recipe in "favoriteRecipes":
//     Log the recipeTitle

// For each recipe in "favoriteRecipes":
//     For each ingredient in recipe.ingredients:
//         Log the ingredient
