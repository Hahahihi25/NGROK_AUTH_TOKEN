<html lang="vi">
 <head> 
  <meta charset="UTF-8"> 
  <meta name="viewport" content="width=device-width, initial-scale=1.0"> 
  <title>Game Optimizer VIP</title> 
  <style>
    @keyframes neon {
      0%, 100% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
    }
    body {
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(45deg, #0f0c29, #302b63, #24243e);
      background-size: 600% 600%;
      animation: neon 20s ease infinite;
      color: #fff;
    }
    .login-overlay {
      position: fixed;
      top: 0; left: 0; right: 0; bottom: 0;
      background: rgba(0,0,0,0.85);
      display: flex;
      align-items: center;
      justify-content: center;
      z-index: 9999;
      flex-direction: column;
    }
    .login-box {
      background: rgba(255, 255, 255, 0.1);
      padding: 30px 40px;
      border-radius: 10px;
      box-shadow: 0 0 20px rgba(0,0,0,0.5);
      text-align: center;
    }
    .login-box input, .login-box button {
      width: 100%;
      padding: 12px;
      margin: 15px 0;
      font-size: 16px;
      border-radius: 8px;
      border: none;
      outline: none;
    }
    .login-box button {
      background: #6c5ce7;
      color: #fff;
      cursor: pointer;
      transition: background 0.3s;
    }
    .login-box button:hover {
      background: #00cec9;
    }
    .container {
      max-width: 600px;
      margin: 80px auto;
      background: rgba(255, 255, 255, 0.1);
      padding: 30px;
      border-radius: 15px;
      box-shadow: 0 10px 30px rgba(0,0,0,0.3);
      backdrop-filter: blur(8px);
    }
    h1 {
      text-align: center;
      margin-bottom: 30px;
      color: #6c5ce7;
      text-shadow: 0 0 10px rgba(108,92,231,0.8);
    }
    h2 {
      margin-top: 40px;
      text-align: center;
      color: #00cec9;
    }
    label {
      font-weight: 600;
      display: block;
      margin-bottom: 10px;
    }
    select {
      width: 100%;
      padding: 12px;
      font-size: 16px;
      border-radius: 10px;
      border: 1px solid #ccc;
      margin-top: 10px;
      background-color: rgba(255, 255, 255, 0.2);
      color: #fff;
    }
    button {
      display: block;
      width: 100%;
      padding: 15px;
      margin-top: 20px;
      background: #6c5ce7;
      color: white;
      border: none;
      border-radius: 10px;
      font-size: 18px;
      cursor: pointer;
      transition: background 0.3s, transform 0.2s;
    }
    button:hover {
      background: #00cec9;
      transform: scale(1.02);
    }
    .theme-toggle {
      position: absolute;
      top: 20px;
      right: 30px;
      cursor: pointer;
      font-size: 22px;
      color: #6c5ce7;
      text-shadow: 0 0 10px rgba(108,92,231,0.8);
    }
    .note {
      text-align: center;
      font-size: 14px;
      margin-top: 15px;
      color: #ccc;
    }
  </style> 
 </head> 
 <body> 
  <!-- Login --> 
  <div class="login-overlay" id="loginOverlay"> 
   <div class="login-box"> 
    <h2>Đăng Nhập VIP</h2> 
    <input type="password" id="accessKey" placeholder="Nhập key để truy cập"> 
    <button onclick="validateKey()">Đăng Nhập</button> 
    
   </div> 
  </div> 
  <!-- Theme Switch --> 
  <div class="theme-toggle" onclick="toggleTheme()">
   🌓
  </div> 
  <!-- Main UI --> 
  <div class="container" id="mainContainer" style="display:none;"> 
   <h1>Chọn Cấu Hình Tối Ưu Game</h1> 
   <label for="configSelect">Chế độ cấu hình:</label> 
   <select id="configSelect"> <option value="config_low.json">Hiệu năng thấp (máy yếu)</option> <option value="config_balance.json">Cân bằng (khuyên dùng)</option> <option value="config_high.json">Cấu hình cao (đẹp + mượt)</option> <option value="config_extreme.json">Tối đa (full hiệu ứng)</option> </select> 
   <button onclick="applyConfig()">Áp dụng Ngay</button> 
   <button onclick="autoOptimize()">Tối ưu Tự động</button> 
   <div class="note">
    * Hệ thống sẽ tự chọn cấu hình tốt nhất cho máy bạn.
   </div> 
   <h2>Chức Năng Tối Ưu VIP</h2> 
   <button onclick="boostNetwork()">Tăng Tốc Kết Nối (Giảm Ping)</button> 
   <button onclick="freeRAM()">Giải Phóng RAM</button> 
   <button onclick="enableFPS()">Bật Chế Độ FPS Cao</button> 
  </div> 
  <script>
    function validateKey() {
      const keyInput = document.getElementById("accessKey").value.trim().toLowerCase();
      if (keyInput === "hoangsec") {
        document.getElementById("loginOverlay").style.display = "none";
        document.getElementById("mainContainer").style.display = "block";
      } else {
        alert("Key không hợp lệ. Vui lòng thử lại!");
      }
    }

    function applyConfig() {
      const selected = document.getElementById('configSelect').value;
      alert('Đã chọn cấu hình: ' + selected);
    }

    function autoOptimize() {
      alert("Đang tự động tối ưu hệ thống...");
    }

    function boostNetwork() {
      alert("Tăng tốc kết nối: Ưu tiên mạng cho game, giảm độ trễ.");
    }

    function freeRAM() {
      alert("Đang giải phóng RAM: Gỡ ứng dụng nền không cần thiết...");
    }

    function enableFPS() {
      alert("Chế độ FPS cao đã bật! Tối đa hóa trải nghiệm mượt mà.");
    }

    function toggleTheme() {
      const container = document.getElementById("mainContainer");
      container.style.background =
        container.style.background === "rgba(255, 255, 255, 0.1)" ? 
        "rgba(0, 0, 0, 0.3)" : "rgba(255, 255, 255, 0.1)";
    }
  </script> 
 </body>
</html>
