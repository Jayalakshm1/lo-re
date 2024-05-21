# lo-re
## html:
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css">
    <style>
    body, html {
    height: 100%;
    margin: 0;
    font-family: Arial, Helvetica, sans-serif;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: #f2f2f2;
  }
  
  .container {
    width: 350px;
    position: relative;
  }
  
  .form {
    background: #fff;
    padding: 25px 30px;
    border-radius: 5px;
    box-shadow: 0 5px 10px rgba(0,0,0,0.15);
  }
  
  header {
    font-size: 1.5em;
    color: #333;
    text-align: center;
    margin-bottom: 20px;
  }
  
  .input-field {
    position: relative;
    margin-bottom: 10px;
  }
  
  .input-field i {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    left: 10px;
    color: #333;
  }
  
  input[type="text"], input[type="password"] {
    width: 100%;
    padding: 10px 10px 10px 40px;
    margin: 5px 0 10px 0;
    display: inline-block;
    border: 1px solid #ccc;
    box-sizing: border-box;
    border-radius: 5px;
  }
  
  input[type="button"] {
    width: 100%;
    background-color: #007bff;
    color: white;
    padding: 10px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-size: 1em;
  }
  
  input[type="button"]:hover {
    background-color: #0056b3;
  }
  
  .remember-forgot {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 10px;
  }
  
  .remember-forgot a {
    color: #007bff;
    text-decoration: none;
  }
  
  .remember-forgot a:hover {
    text-decoration: underline;
  }
  
  .signup {
    text-align: center;
  }
  
  .signup label {
    color: #007bff;
    cursor: pointer;
  }
  
  .signup label:hover {
    text-decoration: underline;
  }
  
  /* Checkbox Styles */
  input[type="checkbox"] {
    margin-right: 5px;
  }
  
  #check {
    display: none;
  }
  
  .registration {
    position: absolute;
    top: 0;
    width: 100%;
    padding: 25px 30px;
    border-radius: 5px;
    background: #fff;
    transition: all 0.3s ease;
    transform: translateX(100%);
    box-shadow: 0 5px 10px rgba(0,0,0,0.15);
  }
  
  #check:checked ~ .registration {
    transform: translateX(0);
  }
  
  #check:checked ~ .login {
    transform: translateX(-100%);
  }
  body {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background-color: #f0f2f5;
    }
    .container {
      width: 400px;
      background-color: #fff;
      border-radius: 10px;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    }
    .form {
      padding: 30px;
      transition: transform 0.3s ease;
    }
    .input-field {
      display: flex;
      align-items: center;
      margin-bottom: 20px;
      padding: 10px;
      border: 1px solid #ccc;
      border-radius: 5px;
    }
    .input-field i {
      margin-right: 10px;
    }
    .input-field input {
      border: none;
      outline: none;
      width: 100%;
    }
    .remember-forgot {
      display: flex;
      justify-content: space-between;
      margin-bottom: 20px;
    }
    .button {
      width: 100%;
      padding: 10px;
      background-color: #007bff;
      border: none;
      color: #fff;
      border-radius: 5px;
      cursor: pointer;
      transition: background-color 0.3s ease;
    }
    .button:hover {
      background-color: #0056b3;
    }
    .signup {
      text-align: center;
      margin-top: 20px;
    }
    .signup label {
      color: #007bff;
      cursor: pointer;
    }
    .form-hidden {
      display: none;
    }
    </style>
</head>
<body>
    <div class="container">
        <div class="login form">
          <header>Login</header>
          <form action="#">
            <div class="input-field">
              <i class="fas fa-envelope"></i>
              <input type="text" placeholder="Enter your email">
            </div>
            <div class="input-field">
              <i class="fas fa-lock"></i>
              <input type="password" placeholder="Enter your password">
            </div>
            <div class="remember-forgot">
              <label><input type="checkbox"> Remember me</label>
              <a href="#">Forgot password?</a>
            </div>
            <input type="button" class="button" value="Login">
          </form>
          <div class="signup">
            <span>Don't have an account? 
              <label onclick="showSignup()">SignUp</label>
            </span>
          </div>
        </div>
        <div class="registration form form-hidden">
          <header>Registration</header>
          <form action="#">
            <div class="input-field">
              <i class="fas fa-envelope"></i>
              <input type="text" placeholder="Enter your email">
            </div>
            <div class="input-field">
              <i class="fas fa-lock"></i>
              <input type="password" placeholder="Create a password">
            </div>
            <div class="input-field">
              <i class="fas fa-lock"></i>
              <input type="password" placeholder="Confirm your password">
            </div>
            <input type="button" class="button" value="Signup">
          </form>
          <div class="signup">
            <span>Already have an account? 
              <label onclick="showLogin()">Login</label>
            </span>
          </div>
        </div>
      </div>
    
      <script>
        function showSignup() {
          document.querySelector('.login').classList.add('form-hidden');
          document.querySelector('.registration').classList.remove('form-hidden');
        }
    
        function showLogin() {
          document.querySelector('.registration').classList.add('form-hidden');
          document.querySelector('.login').classList.remove('form-hidden');
        }
      </script>
</body>
</html>
```

