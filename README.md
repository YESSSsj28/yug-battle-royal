<!doctype html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no" />
    <title>CSL</title>
    <link rel="stylesheet" href="styles.css?v=<?php echo time(); ?>">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.1.1/css/all.min.css" />
    <meta http-equiv="Cache-Control" content="no-cache, no-store, must-revalidate">
    <meta http-equiv="Pragma" content="no-cache">
    <meta http-equiv="Expires" content="0">
    <style>
        :root {
            --primary-color: #ff0000;
            --secondary-color: #000000;
            --text-color: #ffffff;
            --background-color: var(--secondary-color);
            --navbar-footer-bg: #808080;
            --button-bg-color: var(--primary-color);
            --button-text-color: var(--text-color);
            --container-border-color: var(--primary-color);
        }

        body {
            margin: 0;
            font-family: 'Arial', sans-serif;
            background-color: var(--background-color);
            color: var(--text-color);
            display: flex;
            flex-direction: column;
            min-height: 100vh;
        }

        nav, footer {
            background-color: var(--navbar-footer-bg);
            color: var(--text-color);
            padding: 1rem;
        }

        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .nav-container a, .nav-container i {
            color: var(--text-color);
            margin: 0 10px;
            text-decoration: none;
        }

        .container {
            flex: 1;
            padding: 2rem;
            text-align: center;
            border: 2px solid var(--container-border-color);
            border-radius: 10px;
            margin: 2rem auto;
            max-width: 800px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
        }

        h1 {
            font-size: 2.5rem;
            margin-bottom: 2rem;
        }

        form {
            max-width: 600px;
            margin: 0 auto;
            background-color: var(--secondary-color);
            padding: 2rem;
            border-radius: 10px;
        }

        .file-input, .password-input {
            margin-bottom: 1.5rem;
            text-align: left;
        }

        label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: bold;
        }

        input[type="file"], input[type="password"] {
            width: 100%;
            padding: 0.5rem;
            margin-top: 0.5rem;
            border: 1px solid var(--primary-color);
            border-radius: 5px;
            background-color: var(--background-color);
            color: var(--text-color);
        }

        button {
            background-color: var(--button-bg-color);
            color: var(--button-text-color);
            border: none;
            padding: 0.75rem 1.5rem;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s;
        }

        button:hover {
            background-color: darkred;
        }

        footer {
            text-align: center;
            padding: 1rem;
        }
    </style>
</head>
<body>
    <nav>
        <div class="nav-container">
            <div class="theme-toggle">
                <i class="fas fa-n" id="themeToggle"></i>
            </div>
            <a href="https://discord.gg/cherry-sideloading-tm-ios-x-pc-1231663278984265809" class="nav-icon discord-icon" target="_blank" rel="noopener noreferrer">
                <i class="fab fa-discord"></i>
            </a>
            <a href="#" class="nav-icon" id="signInButton">
                <i class="fas fa-sign-in-alt"></i>
            </a>
            <span id="userInfo" class="user-info hidden">
                <i class="fas fa-user"></i>
                <span id="username-display"></span>
                <button id="devButton" class="dev-button hidden">Admin Panel</button>
            </span>
        </div>
    </nav>
    <div class="container">
        <h1>CSL</h1>
        <form id="ASrequest" enctype="multipart/form-data">
            <div class="file-input">
                <label for="p12"><i class="fas fa-file-archive"></i> P12 File:</label>
                <input type="file" id="p12" name="p12" accept=".p12" required />
            </div>
            <div class="file-input">
                <label for="mobileprovision"><i class="fas fa-mobile-alt"></i> Mobile Provision File:</label>
                <input type="file" id="mobileprovision" name="mp" accept=".mobileprovision" required />
            </div>
            <div class="file-input">
                <label for="ipa"><i class="fas fa-file-archive"></i> IPA File:</label>
                <input type="file" id="ipa" name="ipa" accept=".ipa" required />
            </div>
            <div class="password-input">
                <label for="password"><i class="fas fa-lock"></i> P12 Password:</label>
                <input type="password" id="password" name="password" required />
            </div>
            <button type="submit"><i class="fas fa-sign-in-alt"></i> Sign IPA</button>
        </form>
    </div>
    <footer>
        <p>&copy; 2024 CSL. All rights reserved.</p>
    </footer>
    <script src="database.js?v=<?php echo time(); ?>"></script>
    <script src="script.js"></script>
    <script src="admin.js?v=<?php echo time(); ?>"></script>
</body>
</html>
