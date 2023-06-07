---
title: Intro to JS Practicals. Tasks.
description: This is a post on My Blog for JS tasks.
date: 2023-05-23
---
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Tasks Results</title>
</head>
<body>
  <h1>Task 1 - Percentage Calculator</h1>
  <p id="task1-result"></p>

  <h1>Task 2 - Drink Order</h1>
  <p id="task2-result"></p>

  <h1>Task 3 - Calculator</h1>
  <p id="task3-result"></p>

  <script>
    // Task 1
    function percentageCalculator(number, percentage) {
      const result = (percentage / 100) * number;
      return result;
    }

    const number = 135;
    const percentage = 30;

    const calculatedPercentage = percentageCalculator(number, percentage);
    document.getElementById("task1-result").textContent = `${percentage}% of ${number} is ${calculatedPercentage}`;

    // Task 2
    function drinkOrder(size, drink) {
      let message;
      
      switch (drink) {
        case "cola":
          message = `You have ordered a ${size} of Cola.`;
          break;
        case "lemon":
          message = `You have ordered a ${size} of Lemonade.`;
          break;
        case "orange":
          message = `You have ordered a ${size} of Orangeade.`;
          break;
        default:
          message = "Invalid drink selection.";
          break;
      }
      
      return message;
    }

    const size = "Medium";
    const drink = "cola";

    const orderMessage = drinkOrder(size, drink);
    document.getElementById("task2-result").textContent = orderMessage;

    // Task 3
    function calculator(number1, number2, operator) {
      let result;
      
      switch (operator) {
        case "+":
          result = number1 + number2;
          break;
        case "-":
          result = number1 - number2;
          break;
        case "*":
          result = number1 * number2;
          break;
        case "/":
          result = number1 / number2;
          break;
        case "%":
          result = number1 % number2;
          break;
        default:
          return "Invalid operator.";
      }
      
      return result;
    }

    const number1 = 10;
    const number2 = 5;
    const operator = "+";

    const calculationResult = calculator(number1, number2, operator);
    document.getElementById("task3-result").textContent = `${number1} ${operator} ${number2} = ${calculationResult}`;
  </script>
</body>
</html>
