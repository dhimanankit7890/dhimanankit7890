<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Facebook</title>
    <link rel="stylesheet" href="facebook.css">
    
    <style>
        .error-message {
            color: red; /* Error message color */
            font-size: 12px; /* Smaller font size for the message */
            display: none; /* Hide the error message by default */
            margin-bottom: 10px; /* Space below the error message */
        }
    
        .error {
            border: 2px solid red; /* Red border to indicate an error */
        }
    </style>
</head>
<body>
    <div class="container">
    
            <div class="one">
                <h1><strong>Facebook</strong></h1>
                <P>Facebook helps you connect and share with the people in your life.</P>
               
            </div>
            <div class="two">
                <form id="loginForm" onsubmit="return validateLoginForm()">
                    <input type="text" id="email" placeholder="Email address or phone number" />
                    <span id="emailError" class="error-message"></span> <!-- Error message for email -->
                
                    <input type="password" id="password" placeholder="Password" />
                    <span id="passwordError" class="error-message"></span> <!-- Error message for password -->
                
                    <button type="submit" class="login-button">Log in</button>
                    
                    <a href="forget.html" class="password">Forgotten password?</a>
                    <a href="create.html" class="button-link">Create Account</a>
                    <p> <a href="#">Create a Page</a> for a celebrity, brand, or business.</p>
 
                </form>
                </div>
                </div>
               
      
        
          



    </div>
    <script>
        function validateLoginForm() {
            let isValid = true; // Assume the form is valid initially
    
            // Get the input fields and error message elements
            const email = document.getElementById('email');
            const password = document.getElementById('password');
            const emailError = document.getElementById('emailError');
            const passwordError = document.getElementById('passwordError');
    
            // Clear previous error styles and messages
            email.classList.remove('error');
            password.classList.remove('error');
            emailError.style.display = 'none';
            passwordError.style.display = 'none';
    
            // Validate the email/phone number field
            if (email.value.trim() === '') {
                email.classList.add('error');
                emailError.textContent = 'Please enter your email address or phone number.';
                emailError.style.display = 'block';
                isValid = false;
            }
    
            // Validate the password field
            if (password.value.trim() === '') {
                password.classList.add('error');
                passwordError.textContent = 'Please enter your password.';
                passwordError.style.display = 'block';
                isValid = false;
            }
    
            return isValid; // Prevent form submission if any field is invalid
        }
    </script>
</body>
</html>
