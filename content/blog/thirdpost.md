---
title: Loops, Arrays and Objects - Practical lesson tasks.
description: More tasks for Loops, Arrays and Objects.
date: 2023-05-18
tags:
  - Loops
  - Arrays
  - Objects
---

```Javascript
// Task 1 - Shopping Cart

let shoppingCart = [
  { name: "loaf of bread", type: "food", quantity: 1, price: 0.85 },
  { name: "multipack beans", type: "food", quantity: 1, price: 1 },
  { name: "mushrooms", type: "food", quantity: 10, price: 0.1 },
  { name: "can of beer", type: "alcohol", quantity: 4, price: 1.1 },
  { name: "prosecco", type: "alcohol", quantity: 1, price: 8.99 },
  { name: "steak", type: "food", quantity: 2, price: 3.99 },
  { name: "blue cheese", type: "food", quantity: 1, price: 2.99 },
  { name: "candles", type: "home", quantity: 3, price: 1.99 },
  { name: "cheesecake", type: "food", quantity: 1, price: 4.99 },
  { name: "onions", type: "food", quantity: 3, price: 0.4 },
];

//  Part 1
function calculateTotal(cart) {
  let totalPrice = 0;
  for (let i = 0; i < cart.length; i++) {
    totalPrice += cart[i].quantity * cart[i].price;
  }
  return totalPrice;
}

console.log("Total Price (Part 1):", calculateTotal(shoppingCart));

// Part 2
function calculateTotalWithDiscount(cart) {
  let totalPrice = 0;
  for (let i = 0; i < cart.length; i++) {
    let itemPrice = cart[i].quantity * cart[i].price;
    if (cart[i].type === "food") {
      itemPrice *= 0.8; // Apply 20% discount for food items
    }
    totalPrice += itemPrice;
  }
  return totalPrice;
}

console.log("Total Price with Discount (Part 2):", calculateTotalWithDiscount(shoppingCart));

// Part 3
function calculateTotalWithCustomDiscount(cart, discountAmount, type) {
  let totalPrice = 0;
  for (let i = 0; i < cart.length; i++) {
    let itemPrice = cart[i].quantity * cart[i].price;
    if (cart[i].type === type || type === "any") {
      itemPrice *= 1 - discountAmount / 100; // Apply custom discount
    }
    totalPrice += itemPrice;
  }
  return totalPrice;
}

console.log("Total Price with Custom Discount (Part 3):", calculateTotalWithCustomDiscount(shoppingCart, 20, "food"));

// Part 4
function getItemsInPriceRange(cart, lowPrice, highPrice) {
  let arrItems = [];
  for (let i = 0; i < cart.length; i++) {
    let itemPrice = cart[i].quantity * cart[i].price;
    if (itemPrice >= lowPrice && itemPrice <= highPrice) {
      arrItems.push(cart[i]);
    }
  }
  return arrItems;
}

console.log("Items in Price Range (Part 4):", getItemsInPriceRange(shoppingCart, 2, 5));

// Part 5
function getItemsInPriceRange(cart, lowPrice, highPrice, includeQuantity) {
  let itemsInRange = [];
  for (let i = 0; i < cart.length; i++) {
    let totalPrice = cart[i].quantity * cart[i].price;
    if (includeQuantity) {
      if (totalPrice >= lowPrice && totalPrice <= highPrice) {
        itemsInRange.push(cart[i]);
      }
    } else {
      if (cart[i].price >= lowPrice && cart[i].price <= highPrice) {
        itemsInRange.push(cart[i]);
      }
    }
  }
  return itemsInRange;
}

console.log("Items in Price Range (Part 5, includeQuantity=true):", getItemsInPriceRange(shoppingCart, 2, 5, true));
console.log("Items in Price Range (Part 5, includeQuantity=false):", getItemsInPriceRange(shoppingCart, 2, 5, false));
  
  
  
  
  
// Additional Tasks

// Part 1
let numbers = [4, 2, 7, 5, 9, 2, 1, 6, 3]; // Example array of random numbers

// Function to calculate the mean of an array of numbers
function calculateMean(arr) {
  let sum = 0;
  for (let i = 0; i < arr.length; i++) {
    sum += arr[i];
  }
  return sum / arr.length;
}

// Function to calculate the mode of an array of numbers
function calculateMode(arr) {
  let frequency = {};
  let maxFrequency = 0;
  let mode = [];

  for (let i = 0; i < arr.length; i++) {
    if (frequency[arr[i]]) {
      frequency[arr[i]]++;
    } else {
      frequency[arr[i]] = 1;
    }

    if (frequency[arr[i]] > maxFrequency) {
      maxFrequency = frequency[arr[i]];
      mode = [arr[i]];
    } else if (frequency[arr[i]] === maxFrequency) {
      mode.push(arr[i]);
    }
  }

  return mode;
}

// Function to calculate the median of an array of numbers
function calculateMedian(arr) {
  arr.sort((a, b) => a - b);
  let middleIndex = Math.floor(arr.length / 2);

  if (arr.length % 2 === 0) {
    return (arr[middleIndex - 1] + arr[middleIndex]) / 2;
  } else {
    return arr[middleIndex];
  }
}

console.log("Mean:", calculateMean(numbers));
console.log("Mode:", calculateMode(numbers));
console.log("Median:", calculateMedian(numbers));

// Part 2
function calculateNumberStats(arr, type) {
  switch (type) {
    case "mean":
      return calculateMean(arr);
    case "mode":
      return calculateMode(arr);
    case "median":
      return calculateMedian(arr);
    default:
      return "Invalid type";
  }
}

console.log("Number Stats (Mean):", calculateNumberStats(numbers, "mean"));
console.log("Number Stats (Mode):", calculateNumberStats(numbers, "mode"));
console.log("Number Stats (Median):", calculateNumberStats(numbers, "median"));