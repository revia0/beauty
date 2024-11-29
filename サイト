import os
import shutil

# フォルダ構成
project_name = "MyWebsite"
folders = ["css", "js"]
files = {
    "login.html": """
<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ログイン</title>
    <link rel="stylesheet" href="css/style.css">
</head>
<body>
    <main>
        <section id="login-section">
            <h1>ログイン</h1>
            <p>パスワードを入力してください:</p>
            <form id="login-form">
                <input type="password" id="password" placeholder="パスワードを入力">
                <button type="submit">ログイン</button>
            </form>
            <p id="error-message" style="color: red; display: none;">パスワードが正しくありません。</p>
        </section>
    </main>
    <script src="js/login.js"></script>
</body>
</html>
""",
    "index.html": """
<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>トップページ</title>
    <link rel="stylesheet" href="css/style.css">
</head>
<body>
    <header>
        <h1>ようこそ！</h1>
    </header>
    <main>
        <p>ここはトップページです。</p>
    </main>
</body>
</html>
""",
    "css/style.css": """
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
}

#login-section {
    text-align: center;
    margin: 50px auto;
    width: 300px;
    padding: 20px;
    border: 1px solid #ccc;
    border-radius: 10px;
    background: #f9f9f9;
}

#login-form input {
    width: 100%;
    padding: 10px;
    margin: 10px 0;
    border: 1px solid #ccc;
    border-radius: 5px;
}

#login-form button {
    width: 100%;
    padding: 10px;
    background-color: #007BFF;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}

#login-form button:hover {
    background-color: #0056b3;
}
""",
    "js/login.js": """
document.getElementById("login-form").addEventListener("submit", function (event) {
    event.preventDefault(); // フォームのデフォルト動作を無効化

    const passwordInput = document.getElementById("password").value;
    const correctPassword = "12345"; // 設定するパスワード

    if (passwordInput === correctPassword) {
        window.location.href = "index.html"; // トップページへ移動
    } else {
        const errorMessage = document.getElementById("error-message");
        errorMessage.style.display = "block";
    }
});
"""
}

# フォルダ作成
if not os.path.exists(project_name):
    os.makedirs(project_name)

for folder in folders:
    os.makedirs(os.path.join(project_name, folder), exist_ok=True)

# ファイル作成
for file_name, content in files.items():
    file_path = os.path.join(project_name, file_name)
    with open(file_path, "w", encoding="utf-8") as file:
        file.write(content)

project_path = os.path.abspath(project_name)
project_path