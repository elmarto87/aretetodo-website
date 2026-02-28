---
layout: null
permalink: /open
---
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Opening ARETE…</title>
  <meta name="apple-itunes-app" content="app-id=6759307580" />
  <style>
    body {
      margin: 0;
      background: #F8FAFF;
      font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
      display: flex;
      align-items: center;
      justify-content: center;
      min-height: 100vh;
      text-align: center;
      padding: 24px;
      box-sizing: border-box;
    }
    .card {
      background: #fff;
      border-radius: 20px;
      padding: 40px 32px;
      max-width: 360px;
      width: 100%;
      box-shadow: 0 4px 24px rgba(43,74,255,0.10);
    }
    .logo {
      font-size: 42px;
      margin-bottom: 12px;
    }
    h1 {
      font-size: 22px;
      font-weight: 700;
      color: #111418;
      margin: 0 0 8px;
    }
    p {
      font-size: 15px;
      color: #64748B;
      line-height: 1.6;
      margin: 0 0 28px;
    }
    .btn {
      display: inline-block;
      background: #2B4AFF;
      color: #fff;
      font-size: 16px;
      font-weight: 600;
      text-decoration: none;
      padding: 14px 36px;
      border-radius: 12px;
    }
  </style>
  <script>
    // Try to open the app via custom URL scheme
    window.location.href = 'arete://';
    // If the app isn't installed, redirect to App Store after 1.5s
    setTimeout(function() {
      window.location.href = 'https://apps.apple.com/app/id6759307580';
    }, 1500);
  </script>
</head>
<body>
  <div class="card">
    <div class="logo">🏆</div>
    <h1>Opening ARETE…</h1>
    <p>If the app doesn't open automatically, tap below to get it from the App Store.</p>
    <a class="btn" href="https://apps.apple.com/app/id6759307590">Get ARETE</a>
  </div>
</body>
</html>
