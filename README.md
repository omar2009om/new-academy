<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>نيو أكاديمي - المنصة التعليمية الرقمية</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css">
    <style>
        :root {
            --primary-color: #5b4bda;
            --secondary-color: #7c6bff;
            --accent-color: #ff7a68;
            --light-color: #f8f9fa;
            --dark-color: #2c3e50;
            --success-color: #27ae60;
            --warning-color: #f39c12;
            --text-color: #333;
            --light-gray: #f5f7fb;
        }
        
        body {
            font-family: 'Tajawal', 'Arial', sans-serif;
            background-color: var(--light-gray);
            margin: 0;
            padding: 0;
            min-height: 100vh;
            color: var(--text-color);
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        /* تصميم صفحة تسجيل الدخول */
        .login-wrapper {
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            background: linear-gradient(135deg, rgba(91,75,218,0.1) 0%, rgba(124,107,255,0.1) 100%);
            padding: 20px;
        }
        
        .login-container {
            background-color: white;
            border-radius: 25px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
            padding: 40px;
            width: 450px;
            text-align: center;
            animation: fadeIn 1s;
            position: relative;
            overflow: hidden;
            border: 1px solid rgba(255, 255, 255, 0.3);
            transition: all 0.4s;
        }
        
        .login-container:hover {
            transform: translateY(-5px);
            box-shadow: 0 25px 50px rgba(0, 0, 0, 0.15);
        }
        
        .login-container::before {
            content: "";
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: linear-gradient(
                45deg,
                rgba(91, 75, 218, 0.05) 0%,
                rgba(124, 107, 255, 0.05) 50%,
                rgba(255, 122, 104, 0.05) 100%
            );
            transform: rotate(30deg);
            z-index: 0;
        }
        
        .logo-img {
            width: 120px;
            height: auto;
            margin-bottom: 20px;
            filter: drop-shadow(0 5px 15px rgba(91, 75, 218, 0.3));
        }
        
        .login-content {
            position: relative;
            z-index: 1;
        }
        
        .login-container h2 {
            color: var(--primary-color);
            margin-bottom: 30px;
            font-size: 28px;
            font-weight: 700;
            text-shadow: 0 2px 4px rgba(0, 0, 0, 0.05);
        }
        
        .form-group {
            margin-bottom: 25px;
            text-align: right;
            position: relative;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            color: var(--dark-color);
            font-weight: 600;
            font-size: 15px;
        }
        
        .form-group input {
            width: 100%;
            padding: 15px 20px;
            border: 2px solid #e0e3eb;
            border-radius: 12px;
            font-size: 16px;
            transition: all 0.3s;
            background-color: #f8f9fc;
        }
        
        .form-group input:focus {
            border-color: var(--primary-color);
            box-shadow: 0 0 0 4px rgba(91, 75, 218, 0.2);
            outline: none;
            background-color: white;
        }
        
        .btn {
            background: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
            color: white;
            border: none;
            padding: 16px 30px;
            border-radius: 12px;
            cursor: pointer;
            font-size: 16px;
            font-weight: 600;
            transition: all 0.3s;
            width: 100%;
            box-shadow: 0 4px 15px rgba(91, 75, 218, 0.3);
            position: relative;
            overflow: hidden;
        }
        
        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(91, 75, 218, 0.4);
        }
        
        .btn:active {
            transform: translateY(1px);
        }
        
        .btn-secondary {
            background: white;
            color: var(--primary-color);
            border: 2px solid var(--primary-color);
            box-shadow: none;
        }
        
        .btn-secondary:hover {
            background: var(--light-gray);
            box-shadow: none;
        }
        
        .btn-danger {
            background: linear-gradient(135deg, #e74c3c 0%, #ff6b6b 100%);
            box-shadow: 0 4px 15px rgba(231, 76, 60, 0.3);
        }
        
        .btn-danger:hover {
            box-shadow: 0 8px 25px rgba(231, 76, 60, 0.4);
        }
        
        /* تصميم الصفحة الرئيسية */
        .header {
            background: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
            color: white;
            padding: 25px 0;
            border-radius: 0 0 25px 25px;
            box-shadow: 0 10px 30px rgba(91, 75, 218, 0.2);
            position: relative;
            overflow: hidden;
        }
        
        .header::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100" preserveAspectRatio="none"><path fill="rgba(255,255,255,0.1)" d="M0,0 L100,0 L100,100 L0,100 Z" /></svg>');
            opacity: 0.1;
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            position: relative;
        }
        
        .logo {
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .logo img {
            height: 40px;
            width: auto;
        }
        
        .logo-text {
            font-size: 22px;
            font-weight: 700;
        }
        
        .user-info {
            display: flex;
            align-items: center;
            gap: 20px;
        }
        
        .user-info img {
            width: 45px;
            height: 45px;
            border-radius: 50%;
            object-fit: cover;
            border: 2px solid rgba(255, 255, 255, 0.3);
        }
        
        /* تصميم اختيار السنة الدراسية */
        .grade-selection {
            background-color: white;
            border-radius: 20px;
            padding: 25px;
            margin: 35px 0;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
            border: 1px solid rgba(0, 0, 0, 0.05);
        }
        
        .grade-selection h3 {
            color: var(--primary-color);
            margin-bottom: 25px;
            border-bottom: 2px solid var(--primary-color);
            padding-bottom: 12px;
            font-size: 22px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .grade-options {
            display: flex;
            flex-wrap: wrap;
            gap: 20px;
        }
        
        .grade-option {
            background-color: white;
            border: 2px solid #e0e3eb;
            border-radius: 15px;
            padding: 20px;
            cursor: pointer;
            transition: all 0.4s;
            flex: 1;
            min-width: 220px;
            text-align: center;
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.03);
        }
        
        .grade-option:hover {
            border-color: var(--primary-color);
            transform: translateY(-8px);
            box-shadow: 0 15px 30px rgba(91, 75, 218, 0.15);
        }
        
        .grade-option i {
            font-size: 28px;
            color: var(--primary-color);
            transition: all 0.3s;
        }
        
        .grade-option.selected {
            background: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
            color: white;
            border-color: var(--primary-color);
            box-shadow: 0 10px 25px rgba(91, 75, 218, 0.3);
        }
        
        .grade-option.selected i {
            color: white;
        }
        
        /* تصميم قسم الحصص */
        .lessons-section {
            margin: 35px 0;
        }
        
        .lessons-section h3 {
            color: var(--primary-color);
            margin-bottom: 25px;
            border-bottom: 2px solid var(--primary-color);
            padding-bottom: 12px;
            font-size: 22px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .subjects {
            display: flex;
            flex-wrap: wrap;
            gap: 25px;
        }
        
        .subject {
            background-color: white;
            border-radius: 18px;
            padding: 25px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
            flex: 1;
            min-width: 280px;
            transition: all 0.4s;
            border: 1px solid rgba(0, 0, 0, 0.05);
            position: relative;
            overflow: hidden;
        }
        
        .subject::after {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 5px;
            height: 100%;
            background: linear-gradient(to bottom, var(--primary-color), var(--secondary-color));
        }
        
        .subject:hover {
            transform: translateY(-8px);
            box-shadow: 0 15px 35px rgba(91, 75, 218, 0.15);
        }
        
        .subject h4 {
            color: var(--dark-color);
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            gap: 12px;
            font-size: 18px;
        }
        
        .subject h4 i {
            color: var(--primary-color);
            font-size: 22px;
        }
        
        .lessons-list {
            list-style: none;
            padding: 0;
            margin: 0;
        }
        
        .lesson-item {
            padding: 12px 0;
            border-bottom: 1px solid #f0f0f0;
            display: flex;
            justify-content: space-between;
            align-items: center;
            transition: all 0.3s;
        }
        
        .lesson-item:hover {
            background-color: #f9f9ff;
            padding: 12px 15px;
            border-radius: 8px;
        }
        
        .lesson-item:last-child {
            border-bottom: none;
        }
        
        .join-btn {
            background: linear-gradient(135deg, var(--accent-color) 0%, #feb47b 100%);
            color: white;
            border: none;
            padding: 8px 16px;
            border-radius: 8px;
            cursor: pointer;
            font-size: 14px;
            font-weight: 600;
            transition: all 0.3s;
            box-shadow: 0 4px 10px rgba(255, 122, 104, 0.3);
            display: flex;
            align-items: center;
            gap: 5px;
        }
        
        .join-btn:hover {
            background: linear-gradient(135deg, #ff6b4a 0%, #f9a56a 100%);
            transform: translateY(-2px);
            box-shadow: 0 6px 15px rgba(255, 122, 104, 0.4);
        }
        
        /* تصميم قسم المذكرات */
        .notes-section {
            background-color: white;
            border-radius: 20px;
            padding: 25px;
            margin: 35px 0;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
            border: 1px solid rgba(0, 0, 0, 0.05);
        }
        
        .notes-section h3 {
            color: var(--primary-color);
            margin-bottom: 25px;
            border-bottom: 2px solid var(--primary-color);
            padding-bottom: 12px;
            font-size: 22px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .notes-list {
            display: flex;
            flex-wrap: wrap;
            gap: 25px;
        }
        
        .note-card {
            background-color: white;
            border-radius: 15px;
            padding: 20px;
            width: calc(33.333% - 25px);
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.06);
            transition: all 0.4s;
            border: 1px solid rgba(0, 0, 0, 0.05);
            position: relative;
            overflow: hidden;
        }
        
        .note-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 15px 35px rgba(91, 75, 218, 0.15);
        }
        
        .note-card h4 {
            color: var(--dark-color);
            margin-bottom: 15px;
            font-size: 17px;
        }
        
        .note-meta {
            display: flex;
            justify-content: space-between;
            color: #666;
            font-size: 14px;
            margin-bottom: 20px;
            gap: 10px;
        }
        
        .note-meta span {
            display: flex;
            align-items: center;
            gap: 5px;
        }
        
        .note-meta i {
            font-size: 14px;
        }
        
        .download-btn {
            background: linear-gradient(135deg, var(--primary-color) 0%, var(--secondary-color) 100%);
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 8px;
            cursor: pointer;
            font-size: 14px;
            font-weight: 600;
            transition: all 0.3s;
            display: block;
            width: 100%;
            text-align: center;
            box-shadow: 0 4px 15px rgba(91, 75, 218, 0.3);
        }
        
        .download-btn:hover {
            background: linear-gradient(135deg, #4a3cb6 0%, #6a5bf0 100%);
            transform: translateY(-2px);
            box-shadow: 0 8px 20px rgba(91, 75, 218, 0.4);
        }
        
        /* تصميم واجهة المدير */
        .admin-panel {
            background-color: white;
            border-radius: 20px;
            padding: 25px;
            margin: 35px 0;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
            border: 1px solid rgba(0, 0, 0, 0.05);
        }
        
        .admin-panel h3 {
            color: var(--primary-color);
            margin-bottom: 25px;
            border-bottom: 2px solid var(--primary-color);
            padding-bottom: 12px;
            font-size: 22px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .admin-tabs {
            display: flex;
            border-bottom: 1px solid #e0e3eb;
            margin-bottom: 25px;
            gap: 5px;
        }
        
        .admin-tab {
            padding: 12px 25px;
            cursor: pointer;
            border-bottom: 3px solid transparent;
            transition: all 0.3s;
            font-weight: 600;
            color: #666;
            border-radius: 8px 8px 0 0;
        }
        
        .admin-tab.active {
            border-bottom-color: var(--primary-color);
            color: var(--primary-color);
            background-color: #f8f9ff;
        }
        
        .admin-tab:hover:not(.active) {
            background-color: #f5f5f5;
            color: #444;
        }
        
        .admin-content {
            display: none;
        }
        
        .admin-content.active {
            display: block;
        }
        
        .form-row {
            display: flex;
            gap: 25px;
            margin-bottom: 20px;
        }
        
        .form-col {
            flex: 1;
        }
        
        select.form-control {
            width: 100%;
            padding: 14px 20px;
            border: 2px solid #e0e3eb;
            border-radius: 12px;
            font-size: 16px;
            transition: all 0.3s;
            background-color: #f8f9fc;
            color: #333;
        }
        
        select.form-control:focus {
            border-color: var(--primary-color);
            box-shadow: 0 0 0 4px rgba(91, 75, 218, 0.2);
            outline: none;
            background-color: white;
        }
        
        /* تصميم متحركات */
        .floating {
            animation: floating 3s ease-in-out infinite;
        }
        
        @keyframes floating {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-12px); }
            100% { transform: translateY(0px); }
        }
        
        .pulse {
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }
        
        /* تصميم متجاوب */
        @media (max-width: 992px) {
            .note-card {
                width: calc(50% - 25px);
            }
        }
        
        @media (max-width: 768px) {
            .login-container {
                width: 90%;
                padding: 30px;
            }
            
            .grade-options, .subjects, .notes-list {
                flex-direction: column;
            }
            
            .grade-option, .subject, .note-card {
                width: 100%;
            }
            
            .form-row {
                flex-direction: column;
                gap: 15px;
            }
            
            .admin-tabs {
                flex-wrap: wrap;
            }
        }
        
        @media (max-width: 576px) {
            .login-container {
                padding: 25px;
            }
            
            .header-content {
                flex-direction: column;
                gap: 15px;
                text-align: center;
            }
            
            .user-info {
                flex-direction: column;
            }
        }
        
        /* تصميم فوتر الصفحة */
        .footer {
            text-align: center;
            padding: 30px 20px;
            color: #666;
            font-size: 14px;
            margin-top: 50px;
            border-top: 1px solid #eee;
            background-color: white;
        }
        
        .developer-info {
            background-color: #f8f9ff;
            padding: 15px;
            border-radius: 10px;
            margin-top: 20px;
            display: inline-block;
            border: 1px solid #e0e3eb;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }
        
        /* تصميم نافذة إدخال الكود */
        .modal-overlay {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.5);
            z-index: 1000;
            justify-content: center;
            align-items: center;
            backdrop-filter: blur(5px);
        }
        
        .modal-content {
            background-color: white;
            padding: 30px;
            border-radius: 20px;
            width: 450px;
            max-width: 90%;
            box-shadow: 0 15px 50px rgba(0, 0, 0, 0.2);
            animation: modalFadeIn 0.3s;
            position: relative;
        }
        
        @keyframes modalFadeIn {
            from { opacity: 0; transform: translateY(-20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .modal-close {
            position: absolute;
            top: 15px;
            left: 15px;
            font-size: 24px;
            color: #999;
            cursor: pointer;
            transition: all 0.3s;
        }
        
        .modal-close:hover {
            color: #666;
            transform: rotate(90deg);
        }
        
        .modal-title {
            color: var(--primary-color);
            margin-bottom: 20px;
            font-size: 22px;
            text-align: center;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
        }
        
        /* تأثيرات إضافية */
        .ripple {
            position: relative;
            overflow: hidden;
        }
        
        .ripple-effect {
            position: absolute;
            border-radius: 50%;
            background-color: rgba(255, 255, 255, 0.4);
            transform: scale(0);
            animation: ripple 0.6s linear;
            pointer-events: none;
        }
        
        @keyframes ripple {
            to {
                transform: scale(2.5);
                opacity: 0;
            }
        }
        
        /* تخصيص شريط التمرير */
        ::-webkit-scrollbar {
            width: 8px;
            height: 8px;
        }
        
        ::-webkit-scrollbar-track {
            background: #f1f1f1;
            border-radius: 10px;
        }
        
        ::-webkit-scrollbar-thumb {
            background: var(--primary-color);
            border-radius: 10px;
        }
        
        ::-webkit-scrollbar-thumb:hover {
            background: var(--secondary-color);
        }
        
        /* تحسينات إضافية */
        .empty-state {
            text-align: center;
            padding: 40px 20px;
            color: #666;
        }
        
        .empty-state i {
            font-size: 50px;
            color: #ddd;
            margin-bottom: 20px;
        }
        
        .badge {
            display: inline-block;
            padding: 4px 10px;
            border-radius: 20px;
            font-size: 12px;
            font-weight: 600;
            background-color: var(--primary-color);
            color: white;
        }
        
        .badge-secondary {
            background-color: #e0e3eb;
            color: #666;
        }
        
        .badge-success {
            background-color: var(--success-color);
        }
        
        .badge-warning {
            background-color: var(--warning-color);
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@400;500;700&display=swap" rel="stylesheet">
</head>
<body>
    <!-- صفحة تسجيل الدخول -->
    <div id="login-page" class="animate__animated animate__fadeIn">
        <div class="login-wrapper">
            <div class="login-container pulse">
                <div class="login-content">
                    <img src="https://via.placeholder.com/120x120?text=New+Academy" alt="شعار نيو أكاديمي" class="logo-img">
                    <h2>مرحباً بك في نيو أكاديمي</h2>
                    <div class="form-group">
                        <label for="phone">رقم الهاتف</label>
                        <input type="tel" id="phone" placeholder="أدخل رقم الهاتف">
                    </div>
                    <div class="form-group">
                        <label for="password">كلمة السر</label>
                        <input type="password" id="password" placeholder="أدخل كلمة السر (8 أرقام)" maxlength="8">
                    </div>
                    <button class="btn ripple" onclick="login()">تسجيل الدخول</button>
                    <p style="margin-top: 20px; color: #666;">ليس لديك حساب؟ <a href="#" style="color: var(--primary-color); font-weight: 600;">سجل الآن</a></p>
                    <p><a href="#" style="color: var(--primary-color); font-size: 14px; font-weight: 500;">ربط الحساب برقم هاتف آخر</a></p>
                </div>
            </div>
        </div>
        
        <div class="footer">
            <div class="developer-info">
                <p>Created by <strong>Omar Mohamed</strong></p>
                <p>Tel: <strong>01202952387</strong></p>
            </div>
        </div>
    </div>

    <!-- الصفحة الرئيسية (مخفية في البداية) -->
    <div id="main-page" style="display: none;">
        <!-- الهيدر -->
        <div class="header">
            <div class="container header-content">
                <div class="logo">
                    <img src="https://via.placeholder.com/40x40?text=NA" alt="شعار نيو أكاديمي">
                    <span class="logo-text">نيو أكاديمي</span>
                </div>
                <div class="user-info">
                    <span id="username-display">مرحباً، محمد</span>
                    <img src="https://ui-avatars.com/api/?name=طالب&background=5b4bda&color=fff" alt="صورة المستخدم">
                    <button class="btn btn-secondary ripple" style="width: auto; padding: 10px 20px;" onclick="logout()">تسجيل الخروج</button>
                </div>
            </div>
        </div>

        <div class="container">
            <!-- اختيار السنة الدراسية -->
            <div class="grade-selection">
                <h3><i class="fas fa-book-open"></i> اختر السنة الدراسية</h3>
                <div class="grade-options">
                    <div class="grade-option" onclick="selectGrade('first-secondary')">
                        <i class="fas fa-award"></i>
                        <span>أولى ثانوي</span>
                    </div>
                    <div class="grade-option" onclick="selectGrade('second-secondary-science')">
                        <i class="fas fa-flask"></i>
                        <span>ثانية ثانوي علمي</span>
                    </div>
                    <div class="grade-option" onclick="selectGrade('second-secondary-literary')">
                        <i class="fas fa-pen-fancy"></i>
                        <span>ثانية ثانوي أدبي</span>
                    </div>
                </div>
            </div>

            <!-- قسم الحصص -->
            <div class="lessons-section" id="lessons-section">
                <h3><i class="fas fa-chalkboard-teacher"></i> الحصص المتاحة</h3>
                <div class="subjects" id="subjects-container">
                    <!-- سيتم ملؤها ديناميكياً حسب الصف المختار -->
                    <div class="empty-state">
                        <i class="fas fa-book-reader"></i>
                        <p>الرجاء اختيار الصف الدراسي أولاً لعرض الحصص المتاحة</p>
                    </div>
                </div>
            </div>

            <!-- قسم المذكرات -->
            <div class="notes-section">
                <h3><i class="fas fa-file-download"></i> المذكرات والملخصات</h3>
                <div class="notes-list" id="notes-list">
                    <!-- سيتم ملؤها ديناميكياً -->
                    <div class="empty-state">
                        <i class="fas fa-file-alt"></i>
                        <p>الرجاء اختيار الصف الدراسي أولاً لعرض المذكرات المتاحة</p>
                    </div>
                </div>
            </div>
        </div>
        
        <div class="footer">
            <div class="developer-info">
                <p>Created by <strong>Omar Mohamed</strong></p>
                <p>Tel: <strong>01202952387</strong></p>
            </div>
        </div>
    </div>

    <!-- واجهة المدير (مخفية في البداية) -->
    <div id="admin-page" style="display: none;">
        <div class="header">
            <div class="container header-content">
                <div class="logo">
                    <img src="https://via.placeholder.com/40x40?text=NA" alt="شعار نيو أكاديمي">
                    <span class="logo-text">لوحة تحكم نيو أكاديمي</span>
                </div>
                <div class="user-info">
                    <span>مرحباً، عمر (مدير)</span>
                    <img src="https://ui-avatars.com/api/?name=عمر&background=5b4bda&color=fff" alt="صورة المدير">
                    <button class="btn btn-secondary ripple" style="width: auto; padding: 10px 20px;" onclick="logout()">تسجيل الخروج</button>
                </div>
            </div>
        </div>

        <div class="container">
            <div class="admin-panel">
                <div class="admin-tabs">
                    <div class="admin-tab active" onclick="openAdminTab('lessons-tab')">إدارة الحصص</div>
                    <div class="admin-tab" onclick="openAdminTab('notes-tab')">إدارة المذكرات</div>
                    <div class="admin-tab" onclick="openAdminTab('students-tab')">إدارة الطلاب</div>
                </div>

                <div id="lessons-tab" class="admin-content active">
                    <h3><i class="fas fa-plus-circle"></i> إضافة حصة جديدة</h3>
                    <div class="form-row">
                        <div class="form-col">
                            <div class="form-group">
                                <label for="lesson-title">عنوان الحصة</label>
                                <input type="text" id="lesson-title" placeholder="أدخل عنوان الحصة">
                            </div>
                        </div>
                        <div class="form-col">
                            <div class="form-group">
                                <label for="lesson-subject">المادة</label>
                                <select id="lesson-subject" class="form-control">
                                    <option value="arabic">اللغة العربية</option>
                                    <option value="english">اللغة الإنجليزية</option>
                                    <option value="math">الرياضيات</option>
                                    <option value="science">العلوم المتكاملة</option>
                                    <option value="philosophy">الفلسفة</option>
                                    <option value="history">التاريخ</option>
                                </select>
                            </div>
                        </div>
                    </div>
                    
                    <div class="form-row">
                        <div class="form-col">
                            <div class="form-group">
                                <label for="lesson-grade">الصف</label>
                                <select id="lesson-grade" class="form-control">
                                    <option value="first">أولى ثانوي</option>
                                    <option value="second-science">ثانية ثانوي علمي</option>
                                    <option value="second-literary">ثانية ثانوي أدبي</option>
                                </select>
                            </div>
                        </div>
                        <div class="form-col">
                            <div class="form-group">
                                <label for="lesson-code">كود الحصة (مطلوب)</label>
                                <input type="text" id="lesson-code" placeholder="أدخل كود الحصة" required>
                            </div>
                        </div>
                    </div>
                    
                    <div class="form-row">
                        <div class="form-col">
                            <div class="form-group">
                                <label for="lesson-date">تاريخ الحصة</label>
                                <input type="date" id="lesson-date" class="form-control">
                            </div>
                        </div>
                        <div class="form-col">
                            <div class="form-group">
                                <label for="lesson-time">وقت الحصة</label>
                                <input type="time" id="lesson-time" class="form-control">
                            </div>
                        </div>
                    </div>
                    
                    <button class="btn ripple" onclick="addLesson()">إضافة الحصة</button>
                    
                    <h3 style="margin-top: 30px;"><i class="fas fa-list"></i> الحصص المضافة</h3>
                    <div id="admin-lessons-list">
                        <!-- سيتم ملؤها بالحصص المضافة -->
                        <div class="empty-state">
                            <i class="fas fa-chalkboard-teacher"></i>
                            <p>لا توجد حصص مضافة بعد</p>
                        </div>
                    </div>
                </div>

                <div id="notes-tab" class="admin-content">
                    <h3><i class="fas fa-upload"></i> رفع مذكرة جديدة</h3>
                    <div class="form-row">
                        <div class="form-col">
                            <div class="form-group">
                                <label for="note-title">عنوان المذكرة</label>
                                <input type="text" id="note-title" placeholder="أدخل عنوان المذكرة">
                            </div>
                        </div>
                        <div class="form-col">
                            <div class="form-group">
                                <label for="note-subject">المادة</label>
                                <select id="note-subject" class="form-control">
                                    <option value="arabic">اللغة العربية</option>
                                    <option value="english">اللغة الإنجليزية</option>
                                    <option value="math">الرياضيات</option>
                                    <option value="science">العلوم المتكاملة</option>
                                    <option value="philosophy">الفلسفة</option>
                                    <option value="history">التاريخ</option>
                                </select>
                            </div>
                        </div>
                    </div>
                    
                    <div class="form-row">
                        <div class="form-col">
                            <div class="form-group">
                                <label for="note-grade">الصف</label>
                                <select id="note-grade" class="form-control">
                                    <option value="first">أولى ثانوي</option>
                                    <option value="second-science">ثانية ثانوي علمي</option>
                                    <option value="second-literary">ثانية ثانوي أدبي</option>
                                </select>
                            </div>
                        </div>
                        <div class="form-col">
                            <div class="form-group">
                                <label for="note-file">ملف المذكرة</label>
                                <input type="file" id="note-file" class="form-control" style="padding: 11px 20px;">
                            </div>
                        </div>
                    </div>
                    
                    <div class="form-group">
                        <label for="note-description">وصف المذكرة (اختياري)</label>
                        <textarea id="note-description" class="form-control" rows="3" placeholder="أدخل وصفاً للمذكرة"></textarea>
                    </div>
                    
                    <button class="btn ripple" onclick="uploadNote()">رفع المذكرة</button>
                    
                    <h3 style="margin-top: 30px;"><i class="fas fa-file-alt"></i> المذكرات المرفوعة</h3>
                    <div id="admin-notes-list">
                        <!-- سيتم ملؤها بالمذكرات المرفوعة -->
                        <div class="empty-state">
                            <i class="fas fa-file-alt"></i>
                            <p>لا توجد مذكرات مرفوعة بعد</p>
                        </div>
                    </div>
                </div>

                <div id="students-tab" class="admin-content">
                    <h3><i class="fas fa-user-plus"></i> إضافة طالب جديد</h3>
                    <div class="form-row">
                        <div class="form-col">
                            <div class="form-group">
                                <label for="student-name">اسم الطالب</label>
                                <input type="text" id="student-name" placeholder="أدخل اسم الطالب">
                            </div>
                        </div>
                        <div class="form-col">
                            <div class="form-group">
                                <label for="student-phone">رقم الهاتف</label>
                                <input type="tel" id="student-phone" placeholder="أدخل رقم الهاتف">
                            </div>
                        </div>
                    </div>
                    
                    <div class="form-row">
                        <div class="form-col">
                            <div class="form-group">
                                <label for="student-password">كلمة السر</label>
                                <input type="password" id="student-password" placeholder="أدخل كلمة السر (8 أرقام)" maxlength="8">
                            </div>
                        </div>
                        <div class="form-col">
                            <div class="form-group">
                                <label for="student-grade">الصف</label>
                                <select id="student-grade" class="form-control">
                                    <option value="first">أولى ثانوي</option>
                                    <option value="second-science">ثانية ثانوي علمي</option>
                                    <option value="second-literary">ثانية ثانوي أدبي</option>
                                </select>
                            </div>
                        </div>
                    </div>
                    
                    <button class="btn ripple" onclick="addStudent()">إضافة الطالب</button>
                    
                    <h3 style="margin-top: 30px;"><i class="fas fa-users"></i> قائمة الطلاب</h3>
                    <div id="admin-students-list">
                        <!-- سيتم ملؤها بقائمة الطلاب -->
                        <div class="empty-state">
                            <i class="fas fa-users"></i>
                            <p>لا توجد طلاب مسجلين بعد</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        
        <div class="footer">
            <div class="developer-info">
                <p>Created by <strong>Omar Mohamed</strong></p>
                <p>Tel: <strong>01202952387</strong></p>
            </div>
        </div>
    </div>

    <!-- نافذة إدخال كود الحصة -->
    <div id="code-modal" class="modal-overlay">
        <div class="modal-content">
            <span class="modal-close" onclick="closeCodeModal()">&times;</span>
            <h3 class="modal-title"><i class="fas fa-key"></i> أدخل كود الحصة</h3>
            <div class="form-group">
                <input type="text" id="lesson-code-input" placeholder="أدخل كود الحصة" style="width: 100%;">
            </div>
            <div style="display: flex; gap: 15px; margin-top: 20px;">
                <button class="btn ripple" onclick="submitCode()" style="flex: 1;">دخول</button>
                <button class="btn btn-danger ripple" onclick="closeCodeModal()" style="flex: 1;">إلغاء</button>
            </div>
        </div>
    </div>

    <script>
        // الأكواد الأساسية للحصص
        const basicCodes = [
            "AR101", "AR102", "AR103", "AR104",
            "EN101", "EN102", "EN103", "EN104",
            "MATH101", "MATH102", "MATH103", "MATH104",
            "SCI101", "SCI102", "SCI103", "SCI104",
            "PHIL101", "PHIL102", "HIST101", "HIST102"
        ];

        // بيانات المدير
        const admin = {
            phone: "01234567890",
            password: "12345678",
            name: "عمر"
        };

        // بيانات الطلاب (سيتم ملؤها من قبل المدير)
        let students = [];

        // الحصص المضافة (سيتم ملؤها من قبل المدير)
        let lessons = [];

        // المذكرات المرفوعة (سيتم ملؤها من قبل المدير)
        let notes = [];

        // المستخدم الحالي
        let currentUser = null;
        let selectedGrade = null;

        // تسجيل الدخول
        function login() {
            const phone = document.getElementById('phone').value;
            const password = document.getElementById('password').value;
            
            if (!phone || !password) {
                alert("الرجاء إدخال رقم الهاتف وكلمة السر");
                return;
            }
            
            if (password.length !== 8 || !/^\d+$/.test(password)) {
                alert("كلمة السر يجب أن تكون 8 أرقام فقط");
                return;
            }
            
            // تحقق إذا كان مديراً
            if (phone === admin.phone && password === admin.password) {
                currentUser = { ...admin, role: "admin" };
                document.getElementById('login-page').style.display = "none";
                document.getElementById('admin-page').style.display = "block";
                renderAdminLessons();
                renderAdminNotes();
                renderAdminStudents();
                return;
            }
            
            // تحقق إذا كان طالباً
            const student = students.find(s => s.phone === phone && s.password === password);
            if (student) {
                currentUser = { ...student, role: "student" };
                document.getElementById('login-page').style.display = "none";
                document.getElementById('main-page').style.display = "block";
                document.getElementById('username-display').textContent = `مرحباً، ${student.name}`;
                return;
            }
            
            alert("رقم الهاتف أو كلمة السر غير صحيحة");
        }

        // تسجيل الخروج
        function logout() {
            currentUser = null;
            selectedGrade = null;
            document.getElementById('login-page').style.display = "block";
            document.getElementById('main-page').style.display = "none";
            document.getElementById('admin-page').style.display = "none";
            document.getElementById('phone').value = "";
            document.getElementById('password').value = "";
        }

        // اختيار السنة الدراسية
        function selectGrade(grade) {
            selectedGrade = grade;
            const options = document.querySelectorAll('.grade-option');
            options.forEach(opt => opt.classList.remove('selected'));
            event.currentTarget.classList.add('selected');
            
            // عرض الحصص والمذكرات المناسبة للصف المختار
            renderLessons();
            renderNotes();
        }

        // عرض الحصص حسب الصف المختار
        function renderLessons() {
            if (!selectedGrade) return;
            
            const container = document.getElementById('subjects-container');
            container.innerHTML = "";
            
            // تصفية الحصص حسب الصف المختار
            const filteredLessons = [...lessons, ...basicCodes.map(code => ({
                code,
                title: getLessonTitleByCode(code),
                subject: getSubjectByCode(code),
                grade: getGradeByCode(code)
            }))].filter(lesson => {
                if (selectedGrade === 'first-secondary') return lesson.grade === 'first';
                if (selectedGrade === 'second-secondary-science') return lesson.grade === 'second-science';
                if (selectedGrade === 'second-secondary-literary') return lesson.grade === 'second-literary';
                return false;
            });
            
            if (filteredLessons.length === 0) {
                container.innerHTML = `
                    <div class="empty-state">
                        <i class="fas fa-book-reader"></i>
                        <p>لا توجد حصص متاحة للصف المختار</p>
                    </div>
                `;
                return;
            }
            
            // تجميع الحصص حسب المادة
            const lessonsBySubject = {};
            filteredLessons.forEach(lesson => {
                if (!lessonsBySubject[lesson.subject]) {
                    lessonsBySubject[lesson.subject] = [];
                }
                lessonsBySubject[lesson.subject].push(lesson);
            });
            
            // عرض الحصص
            for (const subject in lessonsBySubject) {
                const subjectEl = document.createElement('div');
                subjectEl.className = "subject";
                
                const subjectTitle = document.createElement('h4');
                subjectTitle.innerHTML = `<i class="${getSubjectIcon(subject)}"></i> ${getSubjectName(subject)}`;
                
                const lessonsList = document.createElement('ul');
                lessonsList.className = "lessons-list";
                
                lessonsBySubject[subject].forEach(lesson => {
                    const lessonItem = document.createElement('li');
                    lessonItem.className = "lesson-item";
                    lessonItem.innerHTML = `
                        <span>${lesson.title}</span>
                        <button class="join-btn ripple" onclick="joinLesson('${lesson.code}')">
                            دخول <i class="fas fa-sign-in-alt"></i>
                        </button>
                    `;
                    lessonsList.appendChild(lessonItem);
                });
                
                subjectEl.appendChild(subjectTitle);
                subjectEl.appendChild(lessonsList);
                container.appendChild(subjectEl);
            }
        }

        // عرض المذكرات حسب الصف المختار
        function renderNotes() {
            if (!selectedGrade) return;
            
            const container = document.getElementById('notes-list');
            container.innerHTML = "";
            
            // تصفية المذكرات حسب الصف المختار
            const filteredNotes = notes.filter(note => {
                if (selectedGrade === 'first-secondary') return note.grade === 'first';
                if (selectedGrade === 'second-secondary-science') return note.grade === 'second-science';
                if (selectedGrade === 'second-secondary-literary') return note.grade === 'second-literary';
                return false;
            });
            
            if (filteredNotes.length === 0) {
                container.innerHTML = `
                    <div class="empty-state">
                        <i class="fas fa-file-alt"></i>
                        <p>لا توجد مذكرات متاحة للصف المختار</p>
                    </div>
                `;
                return;
            }
            
            // عرض المذكرات
            filteredNotes.forEach(note => {
                const noteCard = document.createElement('div');
                noteCard.className = "note-card";
                noteCard.innerHTML = `
                    <h4>${note.title}</h4>
                    ${note.description ? `<p style="color: #666; font-size: 14px; margin-bottom: 10px;">${note.description}</p>` : ''}
                    <div class="note-meta">
                        <span><i class="fas fa-book"></i> ${getSubjectName(note.subject)}</span>
                        <span><i class="fas fa-calendar-alt"></i> ${note.date}</span>
                    </div>
                    <button class="download-btn ripple" onclick="downloadNote('${note.id}')">
                        تحميل <i class="fas fa-download"></i>
                    </button>
                `;
                container.appendChild(noteCard);
            });
        }

        // الانضمام إلى حصة
        function joinLesson(code) {
            document.getElementById('code-modal').style.display = "flex";
            document.getElementById('lesson-code-input').value = code;
            document.getElementById('lesson-code-input').focus();
        }

        // إغلاق نافذة كود الحصة
        function closeCodeModal() {
            document.getElementById('code-modal').style.display = "none";
            document.getElementById('lesson-code-input').value = "";
        }

        // إدخال كود الحصة
        function submitCode() {
            const code = document.getElementById('lesson-code-input').value;
            
            if (!code) {
                alert("الرجاء إدخال كود الحصة");
                return;
            }
            
            // التحقق من كود الحصة
            const isValidCode = basicCodes.includes(code) || lessons.some(l => l.code === code);
            
            if (isValidCode) {
                alert(`تم الدخول إلى الحصة بنجاح باستخدام الكود: ${code}`);
                closeCodeModal();
                
                // هنا يمكنك إضافة التوجيه إلى الحصة الفعلية
                // window.location.href = `/lesson/${code}`;
            } else {
                alert("كود الحصة غير صحيح");
            }
        }

        // فتح تبويب في لوحة المدير
        function openAdminTab(tabId) {
            document.querySelectorAll('.admin-tab').forEach(tab => tab.classList.remove('active'));
            document.querySelectorAll('.admin-content').forEach(content => content.classList.remove('active'));
            
            event.currentTarget.classList.add('active');
            document.getElementById(tabId).classList.add('active');
        }

        // إضافة حصة جديدة
        function addLesson() {
            const title = document.getElementById('lesson-title').value;
            const subject = document.getElementById('lesson-subject').value;
            const grade = document.getElementById('lesson-grade').value;
            const code = document.getElementById('lesson-code').value;
            const date = document.getElementById('lesson-date').value;
            const time = document.getElementById('lesson-time').value;
            
            if (!title || !code) {
                alert("الرجاء إدخال عنوان الحصة والكود");
                return;
            }
            
            // التحقق من أن الكود غير مستخدم
            if (lessons.some(l => l.code === code) {
                alert("هذا الكود مستخدم بالفعل، الرجاء اختيار كود آخر");
                return;
            }
            
            const lesson = {
                id: Date.now(),
                title,
                subject,
                grade,
                code,
                date: date || new Date().toLocaleDateString(),
                time: time || "00:00"
            };
            
            lessons.push(lesson);
            renderAdminLessons();
            
            // مسح الحقول
            document.getElementById('lesson-title').value = "";
            document.getElementById('lesson-code').value = "";
            document.getElementById('lesson-date').value = "";
            document.getElementById('lesson-time').value = "";
            
            alert("تم إضافة الحصة بنجاح");
        }

        // عرض الحصص في لوحة المدير
        function renderAdminLessons() {
            const container = document.getElementById('admin-lessons-list');
            container.innerHTML = "";
            
            if (lessons.length === 0) {
                container.innerHTML = `
                    <div class="empty-state">
                        <i class="fas fa-chalkboard-teacher"></i>
                        <p>لا توجد حصص مضافة بعد</p>
                    </div>
                `;
                return;
            }
            
            lessons.forEach(lesson => {
                const lessonEl = document.createElement('div');
                lessonEl.className = "lesson-item";
                lessonEl.style.display = "flex";
                lessonEl.style.justifyContent = "space-between";
                lessonEl.style.alignItems = "center";
                lessonEl.style.padding = "15px";
                lessonEl.style.borderBottom = "1px solid #eee";
                lessonEl.style.borderRadius = "10px";
                lessonEl.style.marginBottom = "10px";
                lessonEl.style.backgroundColor = "#f9f9ff";
                
                const info = document.createElement('div');
                info.innerHTML = `
                    <strong style="font-size: 16px;">${lesson.title}</strong>
                    <div style="font-size: 14px; color: #666; margin-top: 5px;">
                        ${getSubjectName(lesson.subject)} - ${getGradeName(lesson.grade)} 
                        <span class="badge" style="margin-right: 10px;">كود: ${lesson.code}</span>
                        ${lesson.date} ${lesson.time !== "00:00" ? `- ${lesson.time}` : ''}
                    </div>
                `;
                
                const actions = document.createElement('div');
                actions.innerHTML = `
                    <button class="btn btn-danger ripple" style="padding: 8px 15px; font-size: 14px;" 
                            onclick="deleteLesson(${lesson.id})">
                        <i class="fas fa-trash"></i> حذف
                    </button>
                `;
                
                lessonEl.appendChild(info);
                lessonEl.appendChild(actions);
                container.appendChild(lessonEl);
            });
        }

        // حذف حصة
        function deleteLesson(id) {
            if (confirm("هل أنت متأكد من حذف هذه الحصة؟")) {
                lessons = lessons.filter(l => l.id !== id);
                renderAdminLessons();
                
                // إذا كان الطالب في الصفحة الرئيسية، نقوم بتحديث الحصص
                if (currentUser?.role === "student" && selectedGrade) {
                    renderLessons();
                }
            }
        }

        // رفع مذكرة جديدة
        function uploadNote() {
            const title = document.getElementById('note-title').value;
            const subject = document.getElementById('note-subject').value;
            const grade = document.getElementById('note-grade').value;
            const fileInput = document.getElementById('note-file');
            const description = document.getElementById('note-description').value;
            
            if (!title) {
                alert("الرجاء إدخال عنوان المذكرة");
                return;
            }
            
            if (!fileInput.files || fileInput.files.length === 0) {
                alert("الرجاء اختيار ملف المذكرة");
                return;
            }
            
            const note = {
                id: Date.now(),
                title,
                subject,
                grade,
                fileName: fileInput.files[0].name,
                description,
                date: new Date().toLocaleDateString(),
                fileSize: formatFileSize(fileInput.files[0].size)
            };
            
            notes.push(note);
            renderAdminNotes();
            
            // مسح الحقول
            document.getElementById('note-title').value = "";
            document.getElementById('note-description').value = "";
            fileInput.value = "";
            
            alert("تم رفع المذكرة بنجاح");
        }

        // تنسيق حجم الملف
        function formatFileSize(bytes) {
            if (bytes === 0) return '0 Bytes';
            const k = 1024;
            const sizes = ['Bytes', 'KB', 'MB', 'GB'];
            const i = Math.floor(Math.log(bytes) / Math.log(k));
            return parseFloat((bytes / Math.pow(k, i)).toFixed(1) + ' ' + sizes[i];
        }

        // عرض المذكرات في لوحة المدير
        function renderAdminNotes() {
            const container = document.getElementById('admin-notes-list');
            container.innerHTML = "";
            
            if (notes.length === 0) {
                container.innerHTML = `
                    <div class="empty-state">
                        <i class="fas fa-file-alt"></i>
                        <p>لا توجد مذكرات مرفوعة بعد</p>
                    </div>
                `;
                return;
            }
            
            notes.forEach(note => {
                const noteEl = document.createElement('div');
                noteEl.className = "lesson-item";
                noteEl.style.display = "flex";
                noteEl.style.justifyContent = "space-between";
                noteEl.style.alignItems = "center";
                noteEl.style.padding = "15px";
                noteEl.style.borderBottom = "1px solid #eee";
                noteEl.style.borderRadius = "10px";
                noteEl.style.marginBottom = "10px";
                noteEl.style.backgroundColor = "#f9f9ff";
                
                const info = document.createElement('div');
                info.innerHTML = `
                    <strong style="font-size: 16px;">${note.title}</strong>
                    <div style="font-size: 14px; color: #666; margin-top: 5px;">
                        ${getSubjectName(note.subject)} - ${getGradeName(note.grade)} 
                        <span class="badge" style="margin-right: 10px;">${note.fileName}</span>
                        <span class="badge badge-secondary">${note.fileSize}</span>
                        ${note.date}
                    </div>
                    ${note.description ? `<p style="margin-top: 10px; color: #666; font-size: 14px;">${note.description}</p>` : ''}
                `;
                
                const actions = document.createElement('div');
                actions.innerHTML = `
                    <button class="btn btn-danger ripple" style="padding: 8px 15px; font-size: 14px;" 
                            onclick="deleteNote(${note.id})">
                        <i class="fas fa-trash"></i> حذف
                    </button>
                `;
                
                noteEl.appendChild(info);
                noteEl.appendChild(actions);
                container.appendChild(noteEl);
            });
        }

        // حذف مذكرة
        function deleteNote(id) {
            if (confirm("هل أنت متأكد من حذف هذه المذكرة؟")) {
                notes = notes.filter(n => n.id !== id);
                renderAdminNotes();
                
                // إذا كان الطالب في الصفحة الرئيسية، نقوم بتحديث المذكرات
                if (currentUser?.role === "student" && selectedGrade) {
                    renderNotes();
                }
            }
        }

        // تحميل مذكرة
        function downloadNote(id) {
            const note = notes.find(n => n.id === id);
            if (note) {
                // هنا يمكنك تنفيذ عملية التحميل الفعلية
                // في هذا المثال، سنقوم بمحاكاة التحميل
                alert(`جاري تحميل المذكرة: ${note.title}\nحجم الملف: ${note.fileSize}`);
                
                // يمكنك استبدال هذا الكود بالكود الفعلي للتحميل
                // window.location.href = `/download/note/${id}`;
            }
        }

        // إضافة طالب جديد
        function addStudent() {
            const name = document.getElementById('student-name').value;
            const phone = document.getElementById('student-phone').value;
            const password = document.getElementById('student-password').value;
            const grade = document.getElementById('student-grade').value;
            
            if (!name || !phone || !password) {
                alert("الرجاء إدخال جميع البيانات المطلوبة");
                return;
            }
            
            if (password.length !== 8 || !/^\d+$/.test(password)) {
                alert("كلمة السر يجب أن تكون 8 أرقام فقط");
                return;
            }
            
            if (students.some(s => s.phone === phone)) {
                alert("هذا الرقم مسجل بالفعل");
                return;
            }
            
            const student = {
                id: Date.now(),
                name,
                phone,
                password,
                grade,
                joinDate: new Date().toLocaleDateString()
            };
            
            students.push(student);
            renderAdminStudents();
            
            // مسح الحقول
            document.getElementById('student-name').value = "";
            document.getElementById('student-phone').value = "";
            document.getElementById('student-password').value = "";
            
            alert("تم إضافة الطالب بنجاح");
        }

        // عرض الطلاب في لوحة المدير
        function renderAdminStudents() {
            const container = document.getElementById('admin-students-list');
            container.innerHTML = "";
            
            if (students.length === 0) {
                container.innerHTML = `
                    <div class="empty-state">
                        <i class="fas fa-users"></i>
                        <p>لا توجد طلاب مسجلين بعد</p>
                    </div>
                `;
                return;
            }
            
            students.forEach(student => {
                const studentEl = document.createElement('div');
                studentEl.className = "lesson-item";
                studentEl.style.display = "flex";
                studentEl.style.justifyContent = "space-between";
                studentEl.style.alignItems = "center";
                studentEl.style.padding = "15px";
                studentEl.style.borderBottom = "1px solid #eee";
                studentEl.style.borderRadius = "10px";
                studentEl.style.marginBottom = "10px";
                studentEl.style.backgroundColor = "#f9f9ff";
                
                const info = document.createElement('div');
                info.innerHTML = `
                    <strong style="font-size: 16px;">${student.name}</strong>
                    <div style="font-size: 14px; color: #666; margin-top: 5px;">
                        <span class="badge">${student.phone}</span>
                        <span class="badge badge-secondary">${getGradeName(student.grade)}</span>
                        <span class="badge badge-success">${student.joinDate}</span>
                        <span class="badge badge-warning">كلمة السر: ${student.password}</span>
                    </div>
                `;
                
                const actions = document.createElement('div');
                actions.innerHTML = `
                    <button class="btn btn-danger ripple" style="padding: 8px 15px; font-size: 14px;" 
                            onclick="deleteStudent(${student.id})">
                        <i class="fas fa-trash"></i> حذف
                    </button>
                `;
                
                studentEl.appendChild(info);
                studentEl.appendChild(actions);
                container.appendChild(studentEl);
            });
        }

        // حذف طالب
        function deleteStudent(id) {
            if (confirm("هل أنت متأكد من حذف هذا الطالب؟")) {
                students = students.filter(s => s.id !== id);
                renderAdminStudents();
            }
        }

        // مساعدات للحصول على الأسماء
        function getSubjectName(subject) {
            const subjects = {
                "arabic": "اللغة العربية",
                "english": "اللغة الإنجليزية",
                "math": "الرياضيات",
                "science": "العلوم المتكاملة",
                "philosophy": "الفلسفة",
                "history": "التاريخ"
            };
            return subjects[subject] || subject;
        }

        function getSubjectIcon(subject) {
            const icons = {
                "arabic": "fas fa-language",
                "english": "fas fa-globe",
                "math": "fas fa-square-root-alt",
                "science": "fas fa-atom",
                "philosophy": "fas fa-brain",
                "history": "fas fa-landmark"
            };
            return icons[subject] || "fas fa-book";
        }

        function getGradeName(grade) {
            const grades = {
                "first": "أولى ثانوي",
                "second-science": "ثانية ثانوي علمي",
                "second-literary": "ثانية ثانوي أدبي"
            };
            return grades[grade] || grade;
        }

        function getLessonTitleByCode(code) {
            const prefixes = {
                "AR": "اللغة العربية - ",
                "EN": "اللغة الإنجليزية - ",
                "MATH": "الرياضيات - ",
                "SCI": "العلوم - ",
                "PHIL": "الفلسفة - ",
                "HIST": "التاريخ - "
            };
            
            const prefix = Object.keys(prefixes).find(p => code.startsWith(p));
            const number = code.replace(prefix, "");
            
            const titles = {
                "101": "الدرس الأول",
                "102": "الدرس الثاني",
                "103": "الدرس الثالث",
                "104": "الدرس الرابع"
            };
            
            return (prefix ? prefixes[prefix] : "") + (titles[number] || "درس جديد");
        }

        function getSubjectByCode(code) {
            if (code.startsWith("AR")) return "arabic";
            if (code.startsWith("EN")) return "english";
            if (code.startsWith("MATH")) return "math";
            if (code.startsWith("SCI")) return "science";
            if (code.startsWith("PHIL")) return "philosophy";
            if (code.startsWith("HIST")) return "history";
            return "other";
        }

        function getGradeByCode(code) {
            // يمكن تخصيص هذا حسب احتياجاتك
            return ["first", "second-science", "second-literary"][Math.floor(Math.random() * 3)];
        }

        // تأثير الريبل للأزرار
        document.addEventListener('click', function(e) {
            if (e.target.classList.contains('ripple')) {
                const btn = e.target;
                const rect = btn.getBoundingClientRect();
                const x = e.clientX - rect.left;
                const y = e.clientY - rect.top;
                
                const ripple = document.createElement('span');
                ripple.className = 'ripple-effect';
                ripple.style.left = `${x}px`;
                ripple.style.top = `${y}px`;
                
                btn.appendChild(ripple);
                
                setTimeout(() => {
                    ripple.remove();
                }, 600);
            }
        });

        // تهيئة الصفحة
        document.addEventListener('DOMContentLoaded', function() {
            // إضافة بعض البيانات الأولية للاختبار
            students = [
                { id: 1, name: "محمد أحمد", phone: "01111111111", password: "12345678", grade: "first", joinDate: "01/10/2023" },
                { id: 2, name: "أحمد علي", phone: "01222222222", password: "12345678", grade: "second-science", joinDate: "05/10/2023" },
                { id: 3, name: "علي محمود", phone: "01000000000", password: "12345678", grade: "second-literary", joinDate: "10/10/2023" }
            ];
            
            notes = [
                { id: 1, title: "ملخص قواعد اللغة العربية", subject: "arabic", grade: "first", fileName: "arabic-notes.pdf", description: "ملخص شامل لقواعد النحو للصف الأول الثانوي", date: "15/10/2023", fileSize: "2.5 MB" },
                { id: 2, title: "أسئلة مراجعة الرياضيات", subject: "math", grade: "second-science", fileName: "math-questions.pdf", description: "مجموعة أسئلة مراجعة للفصل الأول", date: "10/10/2023", fileSize: "1.8 MB" },
                { id: 3, title: "ملخص الفلسفة للصف الثاني الأدبي", subject: "philosophy", grade: "second-literary", fileName: "philosophy-summary.pdf", description: "ملخص شامل لمنهج الفلسفة كاملاً", date: "20/10/2023", fileSize: "3.2 MB" }
            ];
            
            lessons = [
                { id: 1, title: "مراجعة النحو - الجملة الاسمية", subject: "arabic", grade: "first", code: "AR201", date: "18/10/2023", time: "10:00" },
                { id: 2, title: "حل مسائل التفاضل", subject: "math", grade: "second-science", code: "MATH202", date: "19/10/2023", time: "14:00" },
                { id: 3, title: "مناقشة كتاب الأدب", subject: "arabic", grade: "second-literary", code: "AR203", date: "22/10/2023", time: "11:00" }
            ];
            
            // إذا كانت الصفحة محملة كمدير، نعرض البيانات
            if (document.getElementById('admin-lessons-list')) {
                renderAdminLessons();
                renderAdminNotes();
                renderAdminStudents();
            }
        });
    </script>
</body>
</html>
