---
title: Loops, Arrays and Objects
date: 2023-06-06
author: Ieva Alaunyte
tags:
  - Loops
  - Arrays
  - Objects
---
```javascript
// Task 1: Print the 7 times table from 1 to 12
const number = 7;
console.log("Task 1: 7 Times Table");
for (let i = 1; i <= 12; i++) {
  const product = number * i;
  console.log(`${number} x ${i} = ${product}`);
}

// Task 2: Print some favorite foods
console.log("\nTask 2: Favorite Foods");
const favoriteFoods = ["Pizza", "Burger", "Ice Cream"];
console.log(favoriteFoods[0]);
console.log(favoriteFoods[2]);

// Task 3: Print all favorite foods using a loop
console.log("\nTask 3: All Favorite Foods");
for (let i = 0; i < favoriteFoods.length; i++) {
  console.log(favoriteFoods[i]);
}

// Task 4: Display favorite recipe properties
console.log("\nTask 4: Favorite Recipe");
const favoriteRecipe = {
  recipeTitle: "Chocolate Cake",
  servings: 8,
  ingredients: ["Flour", "Sugar", "Cocoa Powder", "Eggs", "Butter", "Milk", "Vanilla Extract"],
  directions: "1. Preheat oven .\n2. Mix ingredients.\n3. Pour batter into greased baking pan.\n4. Bake for 30 minutes."
};
console.log(favoriteRecipe.recipeTitle);
console.log(favoriteRecipe.servings);
console.log(favoriteRecipe.ingredients);
console.log(favoriteRecipe.directions);

// Loop through the ingredients and print each one
for (let i = 0; i < favoriteRecipe.ingredients.length; i++) {
  console.log(favoriteRecipe.ingredients[i]);
}

// Print the directions of the recipe
console.log(favoriteRecipe.directions);

// Task 5: Call the letsCook function
console.log("\nTask 5: Let's Cook!");
function letsCook() {
  const recipeTitle = "Spaghetti Bolognese";
  console.log("I'm hungry! Let's cook... " + recipeTitle);
}
letsCook();
