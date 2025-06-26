<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Khoa Lý luận Chính trị - Đại học Hải Phòng</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Roboto', sans-serif;
        }

        :root {
            --primary: #003366;
            --secondary: #b30000;
            --accent: #e6b800;
            --light: #f5f5f5;
            --dark: #222;
        }

        body {
            background-color: #f9f9f9;
            color: var(--dark);
            line-height: 1.6;
        }

        /* Header */
        header {
            background: linear-gradient(135deg, var(--primary), #002244);
            color: white;
            padding: 1rem 0;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 100;
        }

        .header-container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 2rem;
        }

        .logo-container {
            display: flex;
            align-items: center;
        }

        .logo {
            width: 80px;
            height: 80px;
            background: linear-gradient(135deg, var(--accent), #ffcc00);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-right: 15px;
            border: 2px solid white;
        }

        .logo i {
            font-size: 2.5rem;
            color: var(--primary);
        }

        .logo-text {
            display: flex;
            flex-direction: column;
        }

        .logo-text h1 {
            font-size: 1.4rem;
            font-weight: 700;
            margin-bottom: 5px;
        }

        .logo-text p {
            font-size: 1rem;
            opacity: 0.9;
        }

        nav ul {
            display: flex;
            list-style: none;
        }

        nav li {
            margin-left: 1.5rem;
        }

        nav a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s ease;
            padding: 0.5rem 0;
            position: relative;
            font-size: 1.05rem;
        }

        nav a:hover {
            color: var(--accent);
        }

        nav a::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 2px;
            background-color: var(--accent);
            transition: width 0.3s ease;
        }

        nav a:hover::after {
            width: 100%;
        }

        /* Hero Section */
        .hero {
            height: 85vh;
            display: flex;
            align-items: center;
            background: linear-gradient(rgba(0, 0, 0, 0.6), rgba(0, 0, 0, 0.6)), url('https://images.unsplash.com/photo-1562673005-7693bd6d6e54?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80') center/cover no-repeat;
            color: white;
            text-align: center;
            position: relative;
        }

        .hero-content {
            max-width: 900px;
            margin: 0 auto;
            padding: 2rem;
        }

        .hero h1 {
            font-size: 3.2rem;
            margin-bottom: 1.5rem;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
            font-weight: 700;
        }

        .hero p {
            font-size: 1.3rem;
            margin-bottom: 2.5rem;
            opacity: 0.9;
            max-width: 800px;
            margin-left: auto;
            margin-right: auto;
        }

        .btn {
            display: inline-block;
            background-color: var(--accent);
            color: var(--primary);
            padding: 14px 35px;
            border-radius: 4px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
            border: 2px solid transparent;
            cursor: pointer;
            font-size: 1.1rem;
            margin: 0 10px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }

        .btn:hover {
            background-color: transparent;
            border-color: var(--accent);
            color: white;
            transform: translateY(-5px);
            box-shadow: 0 8px 15px rgba(0,0,0,0.2);
        }

        .btn-outline {
            background-color: transparent;
            border-color: white;
            color: white;
        }

        .btn-outline:hover {
            background-color: var(--accent);
            border-color: var(--accent);
            color: var(--primary);
        }

        /* About Section */
        .about {
            padding: 5rem 2rem;
            background-color: white;
        }

        .section-title {
            text-align: center;
            margin-bottom: 3.5rem;
            color: var(--primary);
            position: relative;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -15px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background-color: var(--secondary);
        }

        .about-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            max-width: 1200px;
            margin: 0 auto;
            align-items: center;
        }

        .about-content h3 {
            font-size: 1.8rem;
            margin-bottom: 1.5rem;
            color: var(--primary);
        }

        .about-content p {
            margin-bottom: 1.2rem;
            font-size: 1.1rem;
            line-height: 1.8;
        }

        .about-image {
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0,0,0,0.15);
        }

        .about-image img {
            width: 100%;
            height: auto;
            display: block;
            transition: transform 0.5s ease;
        }

        .about-image:hover img {
            transform: scale(1.05);
        }

        /* Programs Section */
        .programs {
            padding: 5rem 2rem;
            background-color: var(--light);
        }

        .programs-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2.5rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .program-card {
            background: white;
            border-radius: 8px;
            padding: 2.5rem 2rem;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            position: relative;
            overflow: hidden;
            border-top: 4px solid var(--primary);
        }

        .program-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.1);
        }

        .program-icon {
            font-size: 3rem;
            color: var(--primary);
            margin-bottom: 1.5rem;
        }

        .program-card h3 {
            margin-bottom: 1.2rem;
            color: var(--primary);
            font-size: 1.4rem;
        }

        .program-card ul {
            list-style: none;
            text-align: left;
            margin-top: 1.5rem;
        }

        .program-card ul li {
            padding: 0.5rem 0;
            border-bottom: 1px solid #eee;
            display: flex;
        }

        .program-card ul li:before {
            content: "•";
            color: var(--secondary);
            font-weight: bold;
            display: inline-block;
            width: 1.5rem;
            font-size: 1.2rem;
        }

        /* News Section */
        .news {
            padding: 5rem 2rem;
            background-color: white;
        }

        .news-container {
            max-width: 1200px;
            margin: 0 auto;
        }

        .news-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 2rem;
        }

        .news-card {
            background: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            transition: transform 0.3s ease;
        }

        .news-card:hover {
            transform: translateY(-10px);
        }

        .news-image {
            height: 200px;
            overflow: hidden;
        }

        .news-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }

        .news-card:hover .news-image img {
            transform: scale(1.1);
        }

        .news-content {
            padding: 1.5rem;
        }

        .news-date {
            color: var(--secondary);
            font-weight: 500;
            font-size: 0.9rem;
            margin-bottom: 0.5rem;
        }

        .news-content h3 {
            margin-bottom: 0.8rem;
            color: var(--primary);
        }

        .news-content p {
            margin-bottom: 1.2rem;
            color: #555;
        }

        .read-more {
            color: var(--primary);
            font-weight: 600;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
        }

        .read-more i {
            margin-left: 5px;
            transition: transform 0.3s ease;
        }

        .read-more:hover i {
            transform: translateX(5px);
        }

        /* Contact Section */
        .contact {
            padding: 5rem 2rem;
            background: linear-gradient(to right, var(--primary), #002244);
            color: white;
        }

        .contact-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 3rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .contact-info h3 {
            font-size: 1.8rem;
            margin-bottom: 1.5rem;
            position: relative;
            padding-bottom: 0.8rem;
        }

        .contact-info h3::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 60px;
            height: 3px;
            background-color: var(--accent);
        }

        .contact-detail {
            display: flex;
            margin-bottom: 1.5rem;
        }

        .contact-icon {
            font-size: 1.5rem;
            color: var(--accent);
            margin-right: 1rem;
            min-width: 30px;
        }

        .contact-text h4 {
            margin-bottom: 0.3rem;
        }

        .map {
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
            height: 300px;
        }

        .map iframe {
            width: 100%;
            height: 100%;
            border: none;
        }

        /* Footer */
        footer {
            background-color: var(--dark);
            color: white;
            padding: 3rem 2rem 1.5rem;
        }

        .footer-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .footer-col h3 {
            position: relative;
            margin-bottom: 1.5rem;
            padding-bottom: 0.5rem;
            font-size: 1.3rem;
        }

        .footer-col h3::after {
            content: '';
            position: absolute;
            left: 0;
            bottom: 0;
            width: 40px;
            height: 2px;
            background-color: var(--accent);
        }

        .footer-col ul {
            list-style: none;
        }

        .footer-col ul li {
            margin-bottom: 0.8rem;
        }

        .footer-col ul li a {
            color: #ddd;
            text-decoration: none;
            transition: all 0.3s ease;
        }

        .footer-col ul li a:hover {
            color: var(--accent);
            padding-left: 5px;
        }

        .social-links {
            display: flex;
            gap: 1rem;
            margin-top: 1.5rem;
        }

        .social-links a {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background-color: rgba(255,255,255,0.1);
            border-radius: 50%;
            color: white;
            transition: all 0.3s ease;
        }

        .social-links a:hover {
            background-color: var(--accent);
            transform: translateY(-3px);
            color: var(--dark);
        }

        .copyright {
            text-align: center;
            padding-top: 3rem;
            margin-top: 3rem;
            border-top: 1px solid rgba(255,255,255,0.1);
            font-size: 0.9rem;
            color: #aaa;
        }

        /* Responsive */
        @media (max-width: 992px) {
            .about-container {
                grid-template-columns: 1fr;
            }
            
            .about-image {
                order: -1;
                max-width: 600px;
                margin: 0 auto;
            }
        }

        @media (max-width: 768px) {
            .header-container {
                flex-direction: column;
                text-align: center;
                padding: 1rem;
            }
            
            .logo-container {
                margin-bottom: 1rem;
            }
            
            nav ul {
                flex-wrap: wrap;
                justify-content: center;
            }
            
            nav li {
                margin: 0.5rem 0.8rem;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .hero p {
                font-size: 1.1rem;
            }
            
            .btn {
                display: block;
                margin: 10px auto;
                max-width: 250px;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="header-container">
            <div class="logo-container">
                <div class="logo">
                    <i class="fas fa-graduation-cap"></i>
                </div>
                <div class="logo-text">
                    <h1>Khoa Lý luận Chính trị</h1>
                    <p>Trường Đại học Hải Phòng</p>
                </div>
            </div>
            <nav>
                <ul>
                    <li><a href="#"><i class="fas fa-home"></i> Trang chủ</a></li>
                    <li><a href="#"><i class="fas fa-info-circle"></i> Giới thiệu</a></li>
                    <li><a href="#"><i class="fas fa-book"></i> Đào tạo</a></li>
                    <li><a href="#"><i class="fas fa-newspaper"></i> Tin tức</a></li>
                    <li><a href="#"><i class="fas fa-envelope"></i> Liên hệ</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="hero-content">
            <h1>Đào tạo nguồn nhân lực chất lượng cao về Lý luận Chính trị</h1>
            <p>Khoa Lý luận Chính trị - Trường Đại học Hải Phòng với sứ mệnh đào tạo, nghiên cứu khoa học và bồi dưỡng kiến thức chính trị cho cán bộ, giảng viên và sinh viên.</p>
            <div>
                <a href="#" class="btn">Tìm hiểu chương trình đào tạo</a>
                <a href="#" class="btn btn-outline">Liên hệ với chúng tôi</a>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section class="about" id="about">
        <h2 class="section-title">Giới thiệu về Khoa</h2>
        <div class="about-container">
            <div class="about-content">
                <h3>Khoa Lý luận Chính trị - Trường Đại học Hải Phòng</h3>
                <p>Khoa Lý luận Chính trị được thành lập với nhiệm vụ đào tạo, nghiên cứu khoa học và bồi dưỡng kiến thức chính trị cho toàn trường. Với đội ngũ giảng viên có trình độ cao, giàu kinh nghiệm, Khoa đã và đang đóng góp tích cực vào sự nghiệp giáo dục và đào tạo của nhà trường.</p>
                <p>Khoa thực hiện giảng dạy các môn lý luận chính trị cho tất cả các ngành đào tạo của Trường Đại học Hải Phòng, đồng thời tham gia đào tạo sau đại học, nghiên cứu khoa học và các hoạt động tư vấn, phản biện xã hội.</p>
                <p>Với phương châm "Chất lượng - Hiệu quả - Phát triển", Khoa Lý luận Chính trị không ngừng đổi mới nội dung, phương pháp giảng dạy, góp phần nâng cao chất lượng đào tạo nguồn nhân lực cho thành phố Hải Phòng và cả nước.</p>
                <a href="#" class="btn" style="margin-top: 20px;">Xem thêm</a>
            </div>
            <div class="about-image">
                <img src="https://images.unsplash.com/photo-1523580494863-6f3031224c94?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80" alt="Khoa Lý luận Chính trị">
            </div>
        </div>
    </section>

    <!-- Programs Section -->
    <section class="programs" id="programs">
        <h2 class="section-title">Chương trình đào tạo</h2>
        <div class="programs-container">
            <div class="program-card">
                <div class="program-icon">
                    <i class="fas fa-book-open"></i>
                </div>
                <h3>Đào tạo Đại học</h3>
                <ul>
                    <li>Chủ nghĩa Mác - Lênin</li>
                    <li>Tư tưởng Hồ Chí Minh</li>
                    <li>Đường lối Cách mạng Đảng CSVN</li>
                    <li>Pháp luật đại cương</li>
                    <li>Logic học đại cương</li>
                </ul>
            </div>
            <div class="program-card">
                <div class="program-icon">
                    <i class="fas fa-graduation-cap"></i>
                </div>
                <h3>Đào tạo Sau đại học</h3>
                <ul>
                    <li>Thạc sĩ Lý luận Chính trị</li>
                    <li>Chuyên đề nâng cao Triết học</li>
                    <li>Chuyên đề nâng cao Kinh tế chính trị</li>
                    <li>Phương pháp nghiên cứu khoa học</li>
                    <li>Lịch sử Đảng Cộng sản Việt Nam</li>
                </ul>
            </div>
            <div class="program-card">
                <div class="program-icon">
                    <i class="fas fa-chalkboard-teacher"></i>
                </div>
                <h3>Bồi dưỡng kiến thức</h3>
                <ul>
                    <li>Bồi dưỡng lý luận chính trị</li>
                    <li>Bồi dưỡng nghiệp vụ giảng dạy</li>
                    <li>Cập nhật kiến thức mới</li>
                    <li>Tập huấn chuyên đề</li>
                    <li>Hội thảo khoa học</li>
                </ul>
            </div>
        </div>
    </section>

    <!-- News Section -->
    <section class="news" id="news">
        <h2 class="section-title">Tin tức & Sự kiện</h2>
        <div class="news-container">
            <div class="news-grid">
                <div class="news-card">
                    <div class="news-image">
                        <img src="https://images.unsplash.com/photo-1523240795612-9a054b0db644?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80" alt="Hội thảo khoa học">
                    </div>
                    <div class="news-content">
                        <div class="news-date"><i class="far fa-calendar-alt"></i> 15/10/2023</div>
                        <h3>Hội thảo khoa học "Giảng dạy lý luận chính trị trong bối cảnh mới"</h3>
                        <p>Hội thảo đã thu hút sự tham gia của nhiều nhà khoa học, giảng viên đầu ngành trong lĩnh vực lý luận chính trị trên cả nước.</p>
                        <a href="#" class="read-more">Xem chi tiết <i class="fas fa-arrow-right"></i></a>
                    </div>
                </div>
                <div class="news-card">
                    <div class="news-image">
                        <img src="https://images.unsplash.com/photo-1543269865-cbf427effbad?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80" alt="Lễ kỷ niệm">
                    </div>
                    <div class="news-content">
                        <div class="news-date"><i class="far fa-calendar-alt"></i> 02/09/2023</div>
                        <h3>Lễ kỷ niệm 20 năm thành lập Khoa Lý luận Chính trị</h3>
                        <p>Khoa Lý luận Chính trị long trọng tổ chức Lễ kỷ niệm 20 năm thành lập và đón nhận Bằng khen của Bộ Giáo dục & Đào tạo.</p>
                        <a href="#" class="read-more">Xem chi tiết <i class="fas fa-arrow-right"></i></a>
                    </div>
                </div>
                <div class="news-card">
                    <div class="news-image">
                        <img src="https://images.unsplash.com/photo-1542744173-8e7e53415bb0?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80" alt="Hội thi giảng viên">
                    </div>
                    <div class="news-content">
                        <div class="news-date"><i class="far fa-calendar-alt"></i> 20/08/2023</div>
                        <h3>Khoa tổ chức Hội thi giảng viên dạy giỏi cấp Khoa năm 2023</h3>
                        <p>Hội thi là dịp để các giảng viên thể hiện năng lực, trao đổi kinh nghiệm giảng dạy và nâng cao chất lượng đào tạo.</p>
                        <a href="#" class="read-more">Xem chi tiết <i class="fas fa-arrow-right"></i></a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="contact" id="contact">
        <h2 class="section-title" style="color: white;">Liên hệ với chúng tôi</h2>
        <div class="contact-container">
            <div class="contact-info">
                <h3>Thông tin liên hệ</h3>
                <div class="contact-detail">
                    <div class="contact-icon">
                        <i class="fas fa-map-marker-alt"></i>
                    </div>
                    <div class="contact-text">
                        <h4>Địa chỉ</h4>
                        <p>Phòng 301, Nhà A1, Trường Đại học Hải Phòng<br>171 Phan Đăng Lưu, Kiến An, Hải Phòng</p>
                    </div>
                </div>
                <div class="contact-detail">
                    <div class="contact-icon">
                        <i class="fas fa-phone-alt"></i>
                    </div>
                    <div class="contact-text">
                        <h4>Điện thoại</h4>
                        <p>(0225) 3 747 661 - Số nội bộ: 301</p>
                    </div>
                </div>
                <div class="contact-detail">
                    <div class="contact-icon">
                        <i class="fas fa-envelope"></i>
                    </div>
                    <div class="contact-text">
                        <h4>Email</h4>
                        <p>khoallyct@dhhp.edu.vn</p>
                    </div>
                </div>
                <div class="contact-detail">
                    <div class="contact-icon">
                        <i class="fas fa-clock"></i>
                    </div>
                    <div class="contact-text">
                        <h4>Giờ làm việc</h4>
                        <p>Thứ 2 - Thứ 6: 7:30 - 17:00<br>Thứ 7: 7:30 - 12:00</p>
                    </div>
                </div>
            </div>
            <div class="map">
                <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3728.397097451625!2d106.68039581533165!3d20.856222197040088!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x314a7af8ae2b1a05%3A0x4f8b4f0b5f8b4b0f!2zVHLGsOG7nW5nIMSQ4bqhaSBI4buNYyBI4bqpbSBOZ2_DoQ!5e0!3m2!1svi!2s!4v1658392345678!5m2!1svi!2s" allowfullscreen="" loading="lazy"></iframe>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="footer-container">
            <div class="footer-col">
                <h3>Khoa Lý luận Chính trị</h3>
                <p>Đơn vị đào tạo, nghiên cứu và bồi dưỡng kiến thức lý luận chính trị hàng đầu tại Trường Đại học Hải Phòng.</p>
                <div class="social-links">
                    <a href="#"><i class="fab fa-facebook-f"></i></a>
                    <a href="#"><i class="fab fa-youtube"></i></a>
                    <a href="#"><i class="fab fa-twitter"></i></a>
                    <a href="#"><i class="fab fa-linkedin-in"></i></a>
                </div>
            </div>
            <div class="footer-col">
                <h3>Liên kết nhanh</h3>
                <ul>
                    <li><a href="#">Trang chủ</a></li>
                    <li><a href="#">Giới thiệu</a></li>
                    <li><a href="#">Đào tạo</a></li>
                    <li><a href="#">Nghiên cứu khoa học</a></li>
                    <li><a href="#">Tin tức - Sự kiện</a></li>
                </ul>
            </div>
            <div class="footer-col">
                <h3>Chương trình đào tạo</h3>
                <ul>
                    <li><a href="#">Đào tạo Đại học</a></li>
                    <li><a href="#">Đào tạo Sau đại học</a></li>
                    <li><a href="#">Bồi dưỡng kiến thức</a></li>
                    <li><a href="#">Tài liệu học tập</a></li>
                    <li><a href="#">Lịch học - Lịch thi</a></li>
                </ul>
            </div>
            <div class="footer-col">
                <h3>Kết nối với chúng tôi</h3>
                <p>Đăng ký nhận thông tin mới nhất từ Khoa:</p>
                <form style="margin-top: 15px;">
                    <input type="email" placeholder="Email của bạn" style="width: 100%; padding: 10px; margin-bottom: 10px; border-radius: 4px; border: none;">
                    <button type="submit" class="btn" style="width: 100%; background-color: var(--accent); color: var(--primary);">Đăng ký</button>
                </form>
            </div>
        </div>
        <div class="copyright">
            <p>&copy; 2023 Bản quyền thuộc về Khoa Lý luận Chính trị - Trường Đại học Hải Phòng</p>
        </div>
    </footer>

    <script>
        // Hiệu ứng cuộn mượt mà
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Header thay đổi khi cuộn
        window.addEventListener('scroll', () => {
            const header = document.querySelector('header');
            header.classList.toggle('scrolled', window.scrollY > 50);
        });

        // Hiệu ứng cho các thẻ khi xuất hiện
        const animateElements = document.querySelectorAll('.about-container, .program-card, .news-card');
        
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = 1;
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, { threshold: 0.1 });
        
        animateElements.forEach(element => {
            element.style.opacity = 0;
            element.style.transform = 'translateY(30px)';
            element.style.transition = 'opacity 0.6s ease, transform 0.6s ease';
            observer.observe(element);
        });
    </script>
</body>
</html>
