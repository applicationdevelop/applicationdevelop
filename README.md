
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Login and Signup Page</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }

        .container {
            width: 300px;
            padding: 20px;
            background-color: #fff;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            border-radius: 8px;
        }

        h2 {
            text-align: center;
            margin-bottom: 20px;
        }

        .form-group {
            margin-bottom: 15px;
        }

        .form-group label {
            display: block;
            margin-bottom: 5px;
        }

        .form-group input {
            width: 100%;
            padding: 8px;
            box-sizing: border-box;
        }

        .btn {
            width: 100%;
            padding: 10px;
            background-color: #5cb85c;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        .btn:hover {
            background-color: #4cae4c;
        }

        .toggle-link {
            text-align: center;
            display: block;
            margin-top: 15px;
            color: #007bff;
            cursor: pointer;
        }
    </style>
</head>
<body>

    <div class="container" id="login-container">
        <h2>Login</h2>
        <form>
            <div class="form-group">
                <label for="login-username">Username</label>
                <input type="text" id="login-username" required>
            </div>
            <div class="form-group">
                <label for="login-password">Password</label>
                <input type="password" id="login-password" required>
            </div>
            <button type="submit" class="btn">Login</button>
        </form>
        <a class="toggle-link" onclick="toggleForm()">Don't have an account? Sign up</a>
    </div>

    <div class="container" id="signup-container" style="display: none;">
        <h2>Sign Up</h2>
        <form>
            <div class="form-group">
                <label for="signup-username">Username</label>
                <input type="text" id="signup-username" required>
            </div>
            <div class="form-group">
                <label for="signup-email">Email</label>
                <input type="email" id="signup-email" required>
            </div>
            <div class="form-group">
                <label for="signup-password">Password</label>
                <input type="password" id="signup-password" required>
            </div>
            <button type="submit" class="btn">Sign Up</button>
        </form>
        <a class="toggle-link" onclick="toggleForm()">Already have an account? Login</a>
    </div>

    <script>
        function toggleForm() {
            const loginContainer = document.getElementById('login-container');
            const signupContainer = document.getElementById('signup-container');
            if (loginContainer.style.display === "none") {
                loginContainer.style.display = "block";
                signupContainer.style.display = "none";
            } else {
                loginContainer.style.display = "none";
                signupContainer.style.display = "block";
            }
        }
    </script>

</body>
</html>
