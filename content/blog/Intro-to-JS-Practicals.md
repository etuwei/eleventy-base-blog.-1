---
title: Intro to JS Practicals. Tasks.
description: This is a post on My Blog for JS tasks.
date: 2023-05-23
---
<!DOCTYPE html>
<html>
<head>
  <title>Task Form</title>
  <style>
    .form-group {
      margin-bottom: 20px;
    }

    .form-label {
      display: block;
      font-weight: bold;
    }

    .form-input {
      width: 100%;
      padding: 8px;
      border: 1px solid #ccc;
      border-radius: 4px;
    }

    .form-button {
      padding: 10px 20px;
      background-color: #4CAF50;
      color: white;
      border: none;
      border-radius: 4px;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <h1>Task Form</h1>

  <div class="form-group">
    <label for="number">Number:</label>
    <input type="number" id="number" class="form-input" required>
  </div>

  <div class="form-group">
    <label for="percentage">Percentage:</label>
    <input type="number" id="percentage" class="form-input" required>
  </div>

  <div class="form-group">
    <button onclick="calculatePercentage()" class="form-button">Calculate Percentage</button>
  </div>

  <div class="form-group">
    <label for="size">Size:</label>
    <input type="text" id="size" class="form-input" required>
  </div>

  <div class="form-group">
    <label for="drink">Drink:</label>
    <select id="drink" class="form-input" required>
      <option value="cola">Cola</option>
      <option value="lemon">Lemonade</option>
      <option value="orange">Orangeade</option>
    </select>
  </div>

  <div class="form-group">
    <button onclick="placeOrder()" class="form-button">Place Order</button>
  </div>

  <div class="form-group">
    <label for="number1">Number 1:</label>
    <input type="number" id="number1" class="form-input" required>
  </div>

  <div class="form-group">
    <label for="number2">Number 2:</label>
    <input type="number" id="number2" class="form-input" required>
  </div>

  <div class="form-group">
    <label for="operator">Operator:</label>
    <select id="operator" class="form-input" required>
      <option value="+">+</option>
      <option value="-">-</option>
      <option value="*">*</option>
      <option value="/">/</option>
      <option value="%">%</option>
    </select>
  </div>

  <div class="form-group">
    <button onclick="performCalculation()" class="form-button">Perform Calculation</button>
  </div>

  <script>
    function calculatePercentage() {
      const number = document.getElementById('number').value;
      const percentage = document.getElementById('percentage').value;
      const result = (percentage / 100) * number;
      alert(`${percentage}% of ${number} is ${result}`);
    }

    function placeOrder() {
      const size = document.getElementById('size').value;
      const drink = document.getElementById('drink').value;
      let message;

      switch (drink) {
        case 'cola':
          message = `You have ordered a ${size} of Cola.`;

