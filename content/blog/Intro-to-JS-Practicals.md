---
title: Intro to JS Practicals. Tasks.
description: This is a post on My Blog about agile frameworks.
date: 2023-05-23
tags:
  - another tag
---
<!DOCTYPE html>
<html>
<head>
  <title>JavaScript Tasks</title>
  <script>
    // Task 1
    function percentageCalculator(number, percentage) {
      const result = (percentage / 100) * number;
      return result;
    }

    const number = 135;
    const percentage = 30;

    const calculatedPercentage = percentageCalculator(number, percentage);
    console.log(`${percentage}% of ${number} is ${calculatedPercentage}`);

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
    console.log(orderMessage);

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
    console.log(`${number1} ${operator} ${number2} = ${calculationResult}`);
  </script>
</head>
<body>
  <!-- You can add any HTML content here if needed -->
</body>
</html>

