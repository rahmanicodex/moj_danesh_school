
<html lang="fa" dir="rtl">
<head>
  <meta charset="UTF-8" />
  <title>سامانه مدیریت مکتب افغان</title>
  <link href="https://fonts.googleapis.com/css2?family=Vazirmatn&display=swap" rel="stylesheet" />
  <link
    rel="stylesheet"
    href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css"
  />
  <style>
    * {
      font-family: 'Vazirmatn', sans-serif;
    }
    body {
      background: url('https://images.unsplash.com/photo-1577896851231-70ef18881754?ixlib=rb-4.0.3&auto=format&fit=crop&w=1350&q=80') no-repeat center center fixed;
      background-size: cover;
      margin: 0;
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      color: #3a3a3a;
    }
    .container,
    .admin-panel,
    .teacher-panel,
    .parent-panel {
      background-color: rgba(255, 255, 255, 0.95);
      border-radius: 15px;
      padding: 30px;
      width: 90%;
      max-width: 600px;
      box-shadow: 0 0 25px rgba(0, 0, 0, 0.15);
      text-align: center;
      color: #2c3e50;
    }
    h1,
    h2,
    h3 {
      color: #1d3557;
      margin-bottom: 15px;
    }
    input,
    select,
    textarea,
    button {
      font-family: 'Vazirmatn', sans-serif;
      font-size: 16px;
      border-radius: 10px;
      border: 1.5px solid #bbb;
      padding: 10px;
      width: 100%;
      box-sizing: border-box;
      margin-top: 10px;
      transition: border-color 0.3s, box-shadow 0.3s;
    }
    input:focus,
    select:focus,
    textarea:focus {
      outline: none;
      border-color: #6c757d;
      box-shadow: 0 0 8px rgba(108, 117, 125, 0.5);
    }
    button {
      background-color: #4a90e2;
      color: white;
      border: none;
      cursor: pointer;
      font-weight: 600;
      transition: background-color 0.3s ease;
      margin-top: 20px;
    }
    button:hover {
      background-color: #2c70c9;
    }
    .hidden {
      display: none;
    }
    .record {
      background: #f0f4f8;
      border: 1px solid #ddd;
      border-radius: 10px;
      padding: 15px;
      margin-top: 15px;
      text-align: right;
      box-shadow: inset 0 1px 3px #e1e8f0;
    }
    .record strong {
      color: #2c3e50;
    }
    .school-info {
      margin-top: 15px;
      text-align: right;
      font-size: 14px;
      line-height: 1.8;
      color: #555;
    }
    .school-info i {
      margin-left: 8px;
      color: #4a90e2;
    }
    .school-info a {
      color: #2c3e50;
      text-decoration: none;
      font-weight: 600;
    }
    .school-info a:hover {
      text-decoration: underline;
    }
    .user-list {
      text-align: right;
      margin-top: 20px;
    }
    .user-item {
      background: #e9eff5;
      padding: 10px;
      border-radius: 10px;
      margin-top: 10px;
      display: flex;
      justify-content: flex-start;
      align-items: center;
      gap: 10px;
      direction: rtl;
    }
    .user-item input {
      width: 40%;
      padding: 8px;
      border-radius: 6px;
      border: 1px solid #bbb;
    }
    .user-item button {
      padding: 6px 14px;
      width: auto;
      font-size: 14px;
      border-radius: 6px;
      background-color: #2980b9;
      border: none;
      cursor: pointer;
      color: #fff;
      transition: background-color 0.25s ease;
    }
    .user-item button:hover {
      background-color: #1c5980;
    }
    /* معلم: لیست شاگردان ثبت شده */
    #teacherRecords p {
      background-color: #dbe9f4;
      border-radius: 8px;
      padding: 10px;
      margin-top: 8px;
      cursor: pointer;
      color: #2c3e50;
      font-weight: 600;
      transition: background-color 0.3s ease;
    }
    #teacherRecords p:hover {
      background-color: #a8c4e9;
    }
    /* پنل ویرایش و حذف */
    #editRecordPanel {
      background: #f7faff;
      border: 1px solid #a3b1c6;
      border-radius: 15px;
      margin-top: 20px;
      padding: 20px;
      text-align: right;
      box-shadow: 0 0 15px rgba(0, 0, 0, 0.05);
    }
    #editRecordPanel input,
    #editRecordPanel select,
    #editRecordPanel textarea {
      margin-top: 10px;
    }
    #editRecordPanel button {
      width: auto;
      margin-top: 15px;
      padding: 10px 25px;
      font-size: 15px;
      background-color: #e74c3c;
      border-radius: 8px;
    }
    #editRecordPanel button:hover {
      background-color: #c0392b;
    }
    #editRecordPanel .save-btn {
      background-color: #27ae60;
      margin-left: 10px;
    }
    #editRecordPanel .save-btn:hover {
      background-color: #1e8449;
    }
    /* استایل جدید برای پنل والدین */
    #studentInfo .record {
      font-size: 15px;
      direction: rtl;
      line-height: 1.8;
      background-color: #fdfefe;
      border: 1px solid #ccc;
    }
  </style>
</head>
<body>
  <!-- باقی کد شما اینجا ادامه می‌یابد -->
</body>
</html>
