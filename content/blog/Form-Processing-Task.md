---
title: Form Processing Task
date: 2023-04-13
draft: true
---
<!DOCTYPE html>
<html>
<head>
  <title>Contact Form</title>
  <!-- Add the Bootstrap CSS link here -->
  <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css">
</head>
<body>

  <div class="container">
    <h1>Contact Form</h1>
    <form id="contactForm" action="submit.php" method="POST">
      <div class="form-group">
        <label for="firstName">First Name</label>
        <input type="text" class="form-control" id="firstName" name="firstName" required>
      </div>
      <div class="form-group">
        <label for="surname">Surname</label>
        <input type="text" class="form-control" id="surname" name="surname" required>
      </div>
      <div class="form-group">
        <label for="email">Email</label>
        <input type="email" class="form-control" id="email" name="email" required>
      </div>
      <div class="form-group">
        <label for="message">Message</label>
        <textarea class="form-control" id="message" name="message" rows="4" required></textarea>
      </div>
      <div class="form-group form-check">
        <input type="checkbox" class="form-check-input" id="terms" name="terms" required>
        <label class="form-check-label" for="terms">I agree to the terms and conditions</label>
      </div>
      <button type="submit" class="btn btn-primary">Submit</button>
    </form>
  </div>

  <!--  Bootstrap JS and jQuery -->
  <script src="https://code.jquery.com/jquery-3.5.1.slim.min.js"></script>
  <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.min.js"></script>
  
  <script>
    $(document).ready(function() {
      // Form submission handling
      $("#contactForm").submit(function(event) {
        event.preventDefault(); // Prevent the form from submitting

        // Perform form validation
        if (validateForm()) {
          // If form is valid, submit the form
          this.submit();
        }
      });

      // Form validation
      function validateForm() {
        let isValid = true;

        // Clear previous error messages
        $(".invalid-feedback").remove();

        // Validate each form field
        $("input, textarea").each(function() {
          const input = $(this);

          if (input.val().trim() === "") {
            // Show error message and mark field as invalid
            input.addClass("is-invalid");
            input.after('<div class="invalid-feedback">This field is required.</div>');
            isValid = false;
          } else {
            // Mark field as valid
            input.removeClass("is-invalid");
          }
        });

        // Validate terms and conditions checkbox
        if (!$('#terms').is(':checked')) {
          $('#terms').addClass("is-invalid");
          $('#terms').after('<div class="invalid-feedback">You must agree to the terms and conditions.</div>');
          isValid = false;
        } else {
          $('#terms').removeClass("is-invalid");
        }

        return isValid;
      }
    });
  </script>
</body>
</html>
