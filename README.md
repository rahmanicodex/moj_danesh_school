
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
  </style>
</head>
<body>
  <div class="container" id="login-panel">
    <h1>سامانه مدیریت درسی لیسه عالی موج دانش</h1>
    <div class="school-info">
      <p><i class="fas fa-map-marker-alt"></i> آدرس: کابل،دشت برچی، ایستگاه بیست متره، بهارستان8، لیسه عالی موج دانش</p>
      <p><i class="fas fa-phone"></i> شماره تماس:۰۷۷۲۲۸۰۰۱۵ </p>
      <p><i class="fab fa-whatsapp"></i> واتساپ: ۰۷۴۴۸۹۳۲۶۸</p>
      <p><i class="fab fa-telegram"></i> کانال تلگرام: <a href="#" target="_blank">لیسه عالی موج دانش</a></p>
      <p><i class="fab fa-facebook"></i> صفحه فیسبوک: <a href="#" target="_blank">لیسه عالی موج دانش</a></p>
    </div>
    <select id="userTypeSelect" required>
      <option value="" disabled selected>نقش شما چیست؟</option>
      <option value="admin">مدیر</option>
      <option value="teacher">معلم</option>
      <option value="parent">والدین</option>
    </select>
    <input type="text" id="username" placeholder="نام کاربری" autocomplete="off" />
    <input type="password" id="password" placeholder="رمز عبور" autocomplete="off" />
    <button onclick="handleLogin()">ورود</button>
  </div>

  <div class="admin-panel hidden" id="admin-panel">
    <h2>پنل مدیریت</h2>
    <h3>افزودن معلم</h3>
    <input type="text" id="teacherUser" placeholder="نام کاربری معلم" autocomplete="off" />
    <input type="password" id="teacherPass" placeholder="رمز عبور معلم" autocomplete="off" />
    <button onclick="registerSpecificUser('teacher')">ثبت معلم</button>
    <div id="teacherList" class="user-list"></div>

    <h3>افزودن والد</h3>
    <input type="text" id="parentUser" placeholder="نام کاربری والد" autocomplete="off" />
    <input type="password" id="parentPass" placeholder="رمز عبور والد" autocomplete="off" />
    <button onclick="registerSpecificUser('parent')">ثبت والد</button>
    <div id="parentList" class="user-list"></div>

    <button onclick="logout()">خروج</button>
  </div>

  <div class="teacher-panel hidden" id="teacher-panel">
    <h2>پنل معلم</h2>
    <input type="text" id="studentName" placeholder="نام شاگرد" autocomplete="off" />
    <input type="text" id="studentFather" placeholder="نام پدر شاگرد" autocomplete="off" />
    <select id="grade">
      <option value="" disabled selected>انتخاب صنف</option>
      <script>
        for (let i = 1; i <= 12; i++) {
          document.write(`<option value="${i}الف">صنف ${i} الف</option><option value="${i}ب">صنف ${i} ب</option>`);
        }
      </script>
    </select>
    <input type="text" id="subject" placeholder="مضمون" autocomplete="off" />
    <select id="performance">
      <option value="عالی">عالی</option>
      <option value="متوسط">متوسط</option>
      <option value="ضعیف">ضعیف</option>
    </select>
    <textarea id="extraNote" placeholder="توضیحات اضافی"></textarea>
    <input type="date" id="recordDate" />
    <button onclick="submitStudentData()">ثبت آمار</button>

    <div id="teacherRecords"></div>

    <div id="editRecordPanel" class="hidden">
      <h3>ویرایش آمار شاگرد</h3>
      <input type="text" id="editStudentName" placeholder="نام شاگرد" autocomplete="off" />
      <input type="text" id="editStudentFather" placeholder="نام پدر شاگرد" autocomplete="off" />
      <select id="editGrade">
        <option value="" disabled>انتخاب صنف</option>
        <script>
          for (let i = 1; i <= 12; i++) {
            document.write(
              `<option value="${i}الف">صنف ${i} الف</option><option value="${i}ب">صنف ${i} ب</option>`
            );
          }
        </script>
      </select>
      <input type="text" id="editSubject" placeholder="مضمون" autocomplete="off" />
      <select id="editPerformance">
        <option value="عالی">عالی</option>
        <option value="متوسط">متوسط</option>
        <option value="ضعیف">ضعیف</option>
      </select>
      <textarea id="editExtraNote" placeholder="توضیحات اضافی"></textarea>
      <input type="date" id="editRecordDate" />
      <br />
      <button class="save-btn" onclick="saveEditedRecord()">ذخیره تغییرات</button>
      <button onclick="cancelEdit()">لغو</button>
    </div>

    <button onclick="logout()">خروج</button>
  </div>

  <div class="parent-panel hidden" id="parent-panel">
    <h2>پنل والدین</h2>
    <div id="studentInfo"></div>
    <button onclick="logout()">خروج</button>
  </div>

  <script>
    let users = JSON.parse(localStorage.getItem('users')) || {
      admin: { admin: 'admin@123' },
      teacher: {},
      parent: {},
    };
    let studentRecords = JSON.parse(localStorage.getItem('records')) || [];
    let currentUser = null;
    let currentRole = null;
    let editingIndex = null;

    function saveData() {
      localStorage.setItem('users', JSON.stringify(users));
      localStorage.setItem('records', JSON.stringify(studentRecords));
    }

    function handleLogin() {
      const username = document.getElementById('username').value.trim();
      const password = document.getElementById('password').value.trim();
      const userType = document.getElementById('userTypeSelect').value;

      if (!userType) {
        alert('لطفاً نقش خود را انتخاب کنید.');
        return;
      }

      if (users[userType][username] === password) {
        currentUser = username;
        currentRole = userType;
        showPanel(userType);
      } else {
        alert('نام کاربری یا رمز عبور اشتباه است.');
      }
    }

    function showPanel(role) {
      document.getElementById('login-panel').classList.add('hidden');
      document.getElementById('admin-panel').classList.add('hidden');
      document.getElementById('teacher-panel').classList.add('hidden');
      document.getElementById('parent-panel').classList.add('hidden');

      if (role === 'admin') {
        document.getElementById('admin-panel').classList.remove('hidden');
        refreshUserLists();
      } else if (role === 'teacher') {
        document.getElementById('teacher-panel').classList.remove('hidden');
        showTeacherRecords();
      } else if (role === 'parent') {
        document.getElementById('parent-panel').classList.remove('hidden');
        showParentInfo();
      }
    }

    function logout() {
      currentUser = null;
      currentRole = null;
      editingIndex = null;
      document.getElementById('username').value = '';
      document.getElementById('password').value = '';
      document.getElementById('userTypeSelect').value = '';
      document.getElementById('login-panel').classList.remove('hidden');
      document.getElementById('admin-panel').classList.add('hidden');
      document.getElementById('teacher-panel').classList.add('hidden');
      document.getElementById('parent-panel').classList.add('hidden');
      clearTeacherFields();
      clearEditPanel();
    }

    function registerSpecificUser(type) {
      let userInput = type === 'teacher' ? 'teacherUser' : 'parentUser';
      let passInput = type === 'teacher' ? 'teacherPass' : 'parentPass';
      let username = document.getElementById(userInput).value.trim();
      let password = document.getElementById(passInput).value.trim();

      if (!username || !password) {
        alert('لطفاً نام کاربری و رمز عبور را وارد کنید.');
        return;
      }
      if (users[type][username]) {
        alert('نام کاربری تکراری است.');
        return;
      }

      users[type][username] = password;
      saveData();
      alert(`کاربر ${type} با موفقیت ثبت شد.`);
      document.getElementById(userInput).value = '';
      document.getElementById(passInput).value = '';
      refreshUserLists();
    }

    function refreshUserLists() {
      const teacherList = document.getElementById('teacherList');
      const parentList = document.getElementById('parentList');

      teacherList.innerHTML = '';
      for (const t in users.teacher) {
        const div = document.createElement('div');
        div.textContent = t;
        teacherList.appendChild(div);
      }

      parentList.innerHTML = '';
      for (const p in users.parent) {
        const div = document.createElement('div');
        div.textContent = p;
        parentList.appendChild(div);
      }
    }

    // معلم: ثبت آمار جدید
    function submitStudentData() {
      const studentName = document.getElementById('studentName').value.trim();
      const studentFather = document.getElementById('studentFather').value.trim();
      const grade = document.getElementById('grade').value;
      const subject = document.getElementById('subject').value.trim();
      const performance = document.getElementById('performance').value;
      const extraNote = document.getElementById('extraNote').value.trim();
      const recordDate = document.getElementById('recordDate').value;

      if (!studentName || !studentFather || !grade || !subject || !performance || !recordDate) {
        alert('لطفاً همه فیلدهای ضروری را پر کنید.');
        return;
      }

      // اعتبارسنجی تطابق نام پدر شاگرد با نام والد ثبت شده (اگر والد ثبت شده باشد)
      let parentExists = false;
      for (const p in users.parent) {
        if (p === studentFather) {
          parentExists = true;
          break;
        }
      }
      if (!parentExists) {
        alert('نام پدر شاگرد با هیچ والد ثبت شده‌ای مطابقت ندارد.');
        return;
      }

      studentRecords.push({
        teacher: currentUser,
        studentName,
        studentFather,
        grade,
        subject,
        performance,
        extraNote,
        recordDate,
      });
      saveData();
      alert('آمار شاگرد با موفقیت ثبت شد.');
      clearTeacherFields();
      showTeacherRecords();
    }

    function clearTeacherFields() {
      document.getElementById('studentName').value = '';
      document.getElementById('studentFather').value = '';
      document.getElementById('grade').value = '';
      document.getElementById('subject').value = '';
      document.getElementById('performance').value = 'عالی';
      document.getElementById('extraNote').value = '';
      document.getElementById('recordDate').value = '';
    }

    function showTeacherRecords() {
      const recordsDiv = document.getElementById('teacherRecords');
      recordsDiv.innerHTML = '<h3>آمار ثبت شده</h3>';
      const filteredRecords = studentRecords.filter(r => r.teacher === currentUser);

      if (filteredRecords.length === 0) {
        recordsDiv.innerHTML += '<p>هیچ آمار ثبت شده‌ای وجود ندارد.</p>';
        return;
      }

      filteredRecords.forEach((rec, idx) => {
        const p = document.createElement('p');
        p.textContent = `شاگرد: ${rec.studentName} - صنف: ${rec.grade} - مضمون: ${rec.subject}`;
        p.style.cursor = 'pointer';
        p.onclick = () => openEditPanel(idx);
        recordsDiv.appendChild(p);
      });
    }

    function openEditPanel(index) {
      editingIndex = index;
      const rec = studentRecords[index];
      document.getElementById('editStudentName').value = rec.studentName;
      document.getElementById('editStudentFather').value = rec.studentFather;
      document.getElementById('editGrade').value = rec.grade;
      document.getElementById('editSubject').value = rec.subject;
      document.getElementById('editPerformance').value = rec.performance;
      document.getElementById('editExtraNote').value = rec.extraNote;
      document.getElementById('editRecordDate').value = rec.recordDate;
      document.getElementById('editRecordPanel').classList.remove('hidden');
    }

    function cancelEdit() {
      editingIndex = null;
      clearEditPanel();
    }

    function clearEditPanel() {
      document.getElementById('editStudentName').value = '';
      document.getElementById('editStudentFather').value = '';
      document.getElementById('editGrade').value = '';
      document.getElementById('editSubject').value = '';
      document.getElementById('editPerformance').value = 'عالی';
      document.getElementById('editExtraNote').value = '';
      document.getElementById('editRecordDate').value = '';
      document.getElementById('editRecordPanel').classList.add('hidden');
    }

    function saveEditedRecord() {
      if (editingIndex === null) return;

      const editedName = document.getElementById('editStudentName').value.trim();
      const editedFather = document.getElementById('editStudentFather').value.trim();
      const editedGrade = document.getElementById('editGrade').value;
      const editedSubject = document.getElementById('editSubject').value.trim();
      const editedPerformance = document.getElementById('editPerformance').value;
      const editedExtraNote = document.getElementById('editExtraNote').value.trim();
      const editedDate = document.getElementById('editRecordDate').value;

      if (!editedName || !editedFather || !editedGrade || !editedSubject || !editedPerformance || !editedDate) {
        alert('لطفاً همه فیلدهای ضروری را پر کنید.');
        return;
      }

      // اعتبارسنجی تطابق نام پدر شاگرد با نام والد ثبت شده (اگر والد ثبت شده باشد)
      let parentExists = false;
      for (const p in users.parent) {
        if (p === editedFather) {
          parentExists = true;
          break;
        }
      }
      if (!parentExists) {
        alert('نام پدر شاگرد با هیچ والد ثبت شده‌ای مطابقت ندارد.');
        return;
      }

      studentRecords[editingIndex] = {
        ...studentRecords[editingIndex],
        studentName: editedName,
        studentFather: editedFather,
        grade: editedGrade,
        subject: editedSubject,
        performance: editedPerformance,
        extraNote: editedExtraNote,
        recordDate: editedDate,
      };
      saveData();
      alert('آمار شاگرد با موفقیت ویرایش شد.');
      clearEditPanel();
      showTeacherRecords();
      editingIndex = null;
    }

    function showParentInfo() {
      const div = document.getElementById('studentInfo');
      div.innerHTML = '';
      const myRecords = studentRecords.filter(r => r.studentFather === currentUser);
      if (myRecords.length === 0) {
        div.textContent = 'هیچ آمار مرتبطی یافت نشد.';
        return;
      }
      myRecords.forEach(rec => {
        const d = document.createElement('div');
        d.className = 'record';
        d.innerHTML = `
          <strong>شاگرد:</strong> ${rec.studentName} <br/>
          <strong>صنف:</strong> ${rec.grade} <br/>
          <strong>مضمون:</strong> ${rec.subject} <br/>
          <strong>عملکرد:</strong> ${rec.performance} <br/>
          <strong>توضیحات:</strong> ${rec.extraNote} <br/>
          <strong>تاریخ ثبت:</strong> ${rec.recordDate}
        `;
        div.appendChild(d);
      });
    }
  </script>
</body>
</html>
