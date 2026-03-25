<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <title>Tất Cả Về Top 5 Trường Đại Học - Phiên Bản Gộp</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            background-color: #f5f5f5;
        }

        header {
            background: #222;
            color: white;
            padding: 20px;
            text-align: center;
        }

        header h1 {
            font-size: 48px;
            margin: 0;
        }

        .tab-container {
            display: flex;
            background: #333;
            overflow-x: auto;
            position: sticky;
            top: 0;
            z-index: 100;
        }

        .tab-button {
            flex: 1;
            padding: 16px 20px;
            border: none;
            background: #333;
            color: white;
            cursor: pointer;
            font-size: 16px;
            font-weight: bold;
            text-align: center;
            transition: all 0.3s ease;
            min-width: 150px;
        }

        .tab-button:hover {
            background: #555;
        }

        .tab-button.active {
            background: #222;
            border-bottom: 4px solid #ff9800;
        }

        .tab-content {
            display: none;
            animation: fadeIn 0.3s ease;
            background: white;
        }

        .tab-content.active {
            display: block;
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
            }
            to {
                opacity: 1;
            }
        }

        section {
            padding: 20px;
            margin: 10px;
            background: white;
            border-radius: 10px;
        }

        h1, h2, h3, h4 {
            color: #333;
        }

        h1:hover, h2:hover, h3:hover, h4:hover {
            color: red;
            cursor: pointer;
            transition: color 0.3s ease;
        }

        img {
            max-width: 200px;
            height: auto;
            margin: 10px;
            border-radius: 10px;
        }

        .infrastructure-images {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 15px;
            margin: 20px 0;
        }

        .infrastructure-images img {
            max-width: 300px;
            width: 100%;
            height: auto;
            object-fit: cover;
            border: 2px solid #ddd;
        }

        .brand {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 15px;
            background: #f9f9f9;
            padding: 20px;
            border-radius: 8px;
            margin: 15px 0;
        }

        a {
            color: blue;
            text-decoration: none;
        }

        a:hover {
            text-decoration: underline;
        }

        p:hover {
            color: rgb(255, 0, 0);
            cursor: pointer;
            transition: color 0.3s ease;
        }

        table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
            background: white;
        }

        table th, table td {
            border: 2px solid #333;
            padding: 12px;
            text-align: center;
        }

        table th {
            background-color: #222;
            color: white;
            font-weight: bold;
        }

        table tr:hover {
            background-color: #f0f0f0;
        }

        .chart {
            margin: 20px 0;
            padding: 20px;
            background: #f9f9f9;
            border-left: 4px solid #222;
            border-radius: 5px;
        }

        .event-card {
            background: #f9f9f9;
            border-left: 4px solid #222;
            padding: 20px;
            margin: 15px 0;
            border-radius: 5px;
            transition: transform 0.3s ease;
        }

        .event-card:hover {
            transform: translateX(5px);
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }

        .event-date {
            background: #222;
            color: white;
            padding: 5px 10px;
            border-radius: 5px;
            display: inline-block;
            font-weight: bold;
            margin-bottom: 10px;
        }

        .event-location {
            color: #666;
            font-style: italic;
            margin-bottom: 10px;
        }

        .event-description {
            color: #333;
            line-height: 1.8;
        }

        .timeline {
            border-left: 3px solid #222;
            padding-left: 20px;
            margin: 20px 0;
        }

        .timeline-item {
            margin-bottom: 30px;
            position: relative;
        }

        .timeline-item:before {
            content: '';
            position: absolute;
            left: -26px;
            top: 0;
            width: 14px;
            height: 14px;
            background: #222;
            border-radius: 50%;
            border: 3px solid white;
        }

        .form-container {
            max-width: 600px;
            margin: 0 auto;
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: bold;
            color: #333;
            font-size: 16px;
        }

        .form-group input[type="text"],
        .form-group input[type="email"],
        .form-group input[type="tel"],
        .form-group textarea,
        .form-group select {
            width: 100%;
            padding: 12px;
            border: 2px solid #ddd;
            border-radius: 5px;
            font-size: 14px;
            font-family: Arial, sans-serif;
            box-sizing: border-box;
            transition: border-color 0.3s ease;
        }

        .form-group input:focus,
        .form-group textarea:focus,
        .form-group select:focus {
            outline: none;
            border-color: #222;
            background-color: #f9f9f9;
        }

        .form-group textarea {
            resize: vertical;
            min-height: 120px;
        }

        .rating-group {
            display: flex;
            gap: 10px;
            margin-top: 10px;
        }

        .rating-group input[type="radio"] {
            margin-right: 5px;
        }

        .rating-group label {
            display: flex;
            align-items: center;
            margin: 0;
            font-weight: normal;
            cursor: pointer;
        }

        .submit-button {
            background-color: #222;
            color: white;
            padding: 14px 30px;
            border: none;
            border-radius: 5px;
            font-size: 16px;
            font-weight: bold;
            cursor: pointer;
            width: 100%;
            transition: background-color 0.3s ease;
        }

        .submit-button:hover {
            background-color: #444;
        }

        .submit-button:active {
            background-color: #111;
        }

        footer {
            background: #222;
            color: white;
            text-align: center;
            padding: 15px;
            margin-top: 20px;
        }

        .back-to-top {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background: #222;
            color: white;
            padding: 12px 16px;
            border-radius: 50%;
            cursor: pointer;
            display: none;
            font-size: 20px;
            z-index: 99;
            transition: all 0.3s ease;
        }

        .back-to-top:hover {
            background: #444;
        }

        .back-to-top.show {
            display: block;
        }

        .info-box {
            background: #e3f2fd;
            border-left: 4px solid #2196F3;
            padding: 15px;
            margin: 15px 0;
            border-radius: 5px;
        }

        .success-box {
            background: #e8f5e9;
            border-left: 4px solid #4CAF50;
            padding: 15px;
            margin: 15px 0;
            border-radius: 5px;
        }
    </style>
</head>
<body>

<header>
    <h1>🎓 TOP 5 TRƯỜNG ĐẠI HỌC VIỆT NAM - PHIÊN BẢN GỘP</h1>
    <p>Tất cả thông tin về 5 trường đại học hàng đầu tại một trang</p>
</header>

<!-- Tab Navigation -->
<div class="tab-container">
    <button class="tab-button active" onclick="switchTab(event, 'tab1')">📖 Trang 1: Giới Thiệu</button>
    <button class="tab-button" onclick="switchTab(event, 'tab2')">📊 Trang 2: So Sánh Qua Năm</button>
    <button class="tab-button" onclick="switchTab(event, 'tab3')">🎉 Trang 3: Sự Kiện 2025</button>
</div>

<!-- TAB 1: GIỚI THIỆU -->
<div id="tab1" class="tab-content active">
    <section>
        <h2>Giới Thiệu</h2>
        <p>
            Hiện nay tại Việt Nam có nhiều trường đại học danh tiếng được công nhận trên thế giới, mỗi trường đều có những điểm mạnh và chuyên môn riêng biệt. 
            Bài viết này sẽ giúp bạn tìm hiểu về 5 trường đại học hàng đầu: Đại học Quốc gia Hà Nội, Đại học Quốc gia TP.HCM, Đại học Bách khoa Hà Nội, Trường Đại học Duy Tân, và Trường Đại học Tôn Đức Thắng. 
            Nhưng bạn thật sự nên chọn trường đại học nào?
        </p>
    </section>

    <section>
        <h2>Vị Trí & Chuyên Ngành</h2>
        <p>
            Mỗi trường đại học hàng đầu tại Việt Nam đều có vị trí địa lý và chuyên ngành mạnh riêng, 
            phục vụ nhu cầu học tập của sinh viên trên khác lĩnh vực.
        </p>

        <h3>Đại học Quốc gia Hà Nội (VNU)</h3>
        <div class="info-box">
            <p>
                <strong>Vị trí:</strong> Hà Nội - Thủ đô của Việt Nam<br>
                <strong>Chuyên ngành mạnh:</strong> Khoa học Tự nhiên, Khoa học Xã hội, Giáo dục, Công nghệ Thông tin<br>
                <strong>Đặc điểm:</strong> Đại học hàng đầu quốc gia, tạo nên cơ sở giáo dục cao cấp uy tín
            </p>
            <a href="https://vnu.edu.vn" target="_blank">→ Tìm hiểu VNU</a>
        </div>

        <h3>Đại học Quốc gia TP.HCM (VNU-HCM)</h3>
        <div class="info-box">
            <p>
                <strong>Vị trí:</strong> Thành phố Hồ Chí Minh - Trung tâm kinh tế lớn nhất Việt Nam<br>
                <strong>Chuyên ngành mạnh:</strong> Công nghệ, Kinh tế, Quản lý Kinh doanh, Khoa học Tự nhiên<br>
                <strong>Đặc điểm:</strong> Cơ hội thực tập và làm việc tại các công ty quốc tế rất lớn
            </p>
            <a href="https://www.vnuhcm.edu.vn" target="_blank">→ Tìm hiểu VNU-HCM</a>
        </div>
    </section>

    <section>
        <h3>Xếp Hạng & Đánh Giá</h3>

        <div class="brand">
            <img src="https://storage.googleapis.com/onthisinhvien.appspot.com/images/985473185-1706153059925-1406_thy_tyc_nhyp_hyc_yyi_hyc_kinh_ty_-_yyi_hyc_quyc_gia_ha_nyi_nym_2020.jpg" alt="VNU">
            <p><b>Đại học Quốc gia Hà Nội (VNU):</b> Đứng đầu các trường đại học Việt Nam về chất lượng giáo dục. VNU được xếp hạng trong top 1000 trường đại học tốt nhất thế giới. Với đội ngũ giáo sư có trình độ cao, VNU cung cấp chương trình học tập chuyên sâu, đặc biệt trong các lĩnh vực khoa học tự nhiên, công nghệ và nhân văn.</p>
        </div>

        <div class="brand">
            <img src="https://hcmussh.edu.vn/img/news/11620609.jpg?t=11620610" alt="VNU-HCM">
            <p><b>Đại học Quốc gia TP.HCM (VNU-HCM):</b> Đại học hàng đầu phía Nam, nổi tiếng về chất lượng đào tạo và nghiên cứu. VNU-HCM có liên kết quốc tế mạnh mẽ, cung cấp cơ hội trao đổi học sinh và hợp tác học thuật với các đại học nước ngoài uy tín.</p>
        </div>

        <div class="brand">
            <img src="https://xdcs.cdnchinhphu.vn/446259493575335936/2025/8/22/bk-1755856140169844190839.jpg" alt="HUST">
            <p><b>Đại học Bách khoa Hà Nội (HUST):</b> Chuyên về kỹ thuật và công nghệ, HUST là đầu tàu của ngành kỹ thuật tại Việt Nam. Trường nổi bật với các chương trình đào tạo hiện đại, phòng thí nghiệm tiên tiến, và mối liên hệ chặt chẽ với các công ty công nghệ hàng đầu thế giới.</p>
        </div>

        <div class="brand">
            <img src="https://cdn2.fptshop.com.vn/unsafe/1920x0/filters:format(webp):quality(75)/diem_chuan_dai_hoc_duy_tan_da_nang_2025_47a4cfda08.jpg" alt="DTU">
            <p><b>Trường Đại học Duy Tân (DTU):</b> Trường tư thục danh tiếng, nổi tiếng về chất lượng quản lý và cơ sở vật chất hiện đại. DTU cung cấp các chương trình học tập cập nhật kịp thời, đặc biệt trong các lĩnh vực kinh doanh, công nghệ thông tin và kỹ thuật.</p>
        </div>

        <div class="brand">
            <img src="https://cdn2.fptshop.com.vn/unsafe/Uploads/images/tin-tuc/172279/Originals/hoc-phi-truong-dai-hoc-ton-duc-thang-1.jpg" alt="TDTU">
            <p><b>Trường Đại học Tôn Đức Thắng (TDTU):</b> Trường tư thục uy tín, chuyên đào tạo kỹ sư chất lượng cao. TDTU nổi bật về mối quan hệ gần gũi với các doanh nghiệp, cung cấp cơ hội thực tập thực tế cho sinh viên, và chương trình học tập linh hoạt phù hợp với nhu cầu thị trường.</p>
        </div>
    </section>

    <section>
        <h3>Bảng So Sánh Xếp Hạng Đại Học</h3>
        <table>
            <thead>
                <tr>
                    <th>Trường Đại Học</th>
                    <th>QS World Ranking</th>
                    <th>THE Ranking</th>
                    <th>Sinh Viên</th>
                    <th>Tỷ Lệ Đỗ Tốt Nghiệp</th>
                    <th>Lương Trung Bình</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>VNU Hà Nội</td>
                    <td>#1 VN, #400 Thế giới</td>
                    <td>#300 Thế giới</td>
                    <td>70,000+</td>
                    <td>95%</td>
                    <td>15-18 triệu</td>
                </tr>
                <tr>
                    <td>VNU TP.HCM</td>
                    <td>#2 VN, #450 Thế giới</td>
                    <td>#350 Thế giới</td>
                    <td>60,000+</td>
                    <td>94%</td>
                    <td>14-17 triệu</td>
                </tr>
                <tr>
                    <td>HUST</td>
                    <td>#3 VN, #500 Thế giới</td>
                    <td>#400 Thế giới</td>
                    <td>35,000+</td>
                    <td>96%</td>
                    <td>16-20 triệu</td>
                </tr>
                <tr>
                    <td>DTU</td>
                    <td>#50 VN, #3000 Thế giới</td>
                    <td>#800 Thế giới</td>
                    <td>25,000+</td>
                    <td>92%</td>
                    <td>12-15 triệu</td>
                </tr>
                <tr>
                    <td>TDTU</td>
                    <td>#60 VN, #3500 Thế giới</td>
                    <td>#1000 Thế giới</td>
                    <td>28,000+</td>
                    <td>91%</td>
                    <td>13-16 triệu</td>
                </tr>
            </tbody>
        </table>
    </section>

    <section>
        <h2>Biểu Mẫu Phản Hồi</h2>
        <div class="form-container">
            <form id="feedbackForm" onsubmit="submitForm(event)">
                <div class="form-group">
                    <label for="fullname">Họ và Tên:</label>
                    <input type="text" id="fullname" name="fullname" required placeholder="Nhập họ và tên của bạn">
                </div>

                <div class="form-group">
                    <label for="email">Email:</label>
                    <input type="email" id="email" name="email" required placeholder="Nhập email của bạn">
                </div>

                <div class="form-group">
                    <label for="rating">Đánh Giá Thông Tin:</label>
                    <div class="rating-group">
                        <label><input type="radio" name="rating" value="5" required> Rất Hữu Ích (5⭐)</label>
                        <label><input type="radio" name="rating" value="4"> Hữu Ích (4⭐)</label>
                        <label><input type="radio" name="rating" value="3"> Bình Thường (3⭐)</label>
                    </div>
                </div>

                <div class="form-group">
                    <label for="comments">Góp Ý & Đề Xuất:</label>
                    <textarea id="comments" name="comments" placeholder="Chia sẻ ý kiến của bạn..."></textarea>
                </div>

                <button type="submit" class="submit-button">Gửi Đánh Giá</button>
            </form>
        </div>
    </section>
</div>

<!-- TAB 2: SO SÁNH QUA NĂM -->
<div id="tab2" class="tab-content">
    <section>
        <h2>Sự Phát Triển Xếp Hạng Các Trường (2020-2025)</h2>
        <p>
            Dưới đây là bảng so sánh sự phát triển xếp hạng của 5 trường đại học hàng đầu Việt Nam trong giai đoạn 2020-2025.
            Dữ liệu này cho thấy xu hướng cải thiện và thay đổi trong chất lượng giáo dục của các trường.
        </p>

        <h3>Xếp Hạng QS World University Ranking (2020-2025)</h3>
        <table>
            <thead>
                <tr>
                    <th>Trường Đại Học</th>
                    <th>2020</th>
                    <th>2021</th>
                    <th>2022</th>
                    <th>2023</th>
                    <th>2024</th>
                    <th>2025</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td><b>VNU Hà Nội</b></td>
                    <td>#600</td>
                    <td>#550</td>
                    <td>#500</td>
                    <td>#450</td>
                    <td>#420</td>
                    <td>#400</td>
                </tr>
                <tr>
                    <td><b>VNU TP.HCM</b></td>
                    <td>#700</td>
                    <td>#650</td>
                    <td>#580</td>
                    <td>#500</td>
                    <td>#470</td>
                    <td>#450</td>
                </tr>
                <tr>
                    <td><b>HUST</b></td>
                    <td>#650</td>
                    <td>#600</td>
                    <td>#550</td>
                    <td>#520</td>
                    <td>#510</td>
                    <td>#500</td>
                </tr>
                <tr>
                    <td><b>DTU</b></td>
                    <td>#3500+</td>
                    <td>#3200</td>
                    <td>#3100</td>
                    <td>#3050</td>
                    <td>#3020</td>
                    <td>#3000</td>
                </tr>
                <tr>
                    <td><b>TDTU</b></td>
                    <td>#3600+</td>
                    <td>#3400</td>
                    <td>#3300</td>
                    <td>#3200</td>
                    <td>#3100</td>
                    <td>#3500</td>
                </tr>
            </tbody>
        </table>

        <div class="chart">
            <h4>📊 Nhận Xét:</h4>
            <p>✓ <b>VNU Hà Nội</b> đã có sự tiến bộ đáng kể, từ #600 (2020) xuống #400 (2025), chứng tỏ chất lượng giáo dục đã cải thiện đáng kể.</p>
            <p>✓ <b>VNU TP.HCM</b> cũng ghi nhận sự cải thiện, từ #700 xuống #450, cho thấy tính cạnh tranh ngày càng tăng.</p>
            <p>✓ <b>HUST</b> duy trì vị trí hàng đầu giữa các trường kỹ thuật, liên tục cải thiện từ #650 xuống #500.</p>
        </div>
    </section>

    <section>
        <h3>So Sánh Số Lượng Sinh Viên Qua Các Năm</h3>
        <table>
            <thead>
                <tr>
                    <th>Trường Đại Học</th>
                    <th>2020</th>
                    <th>2021</th>
                    <th>2022</th>
                    <th>2023</th>
                    <th>2024</th>
                    <th>2025</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td><b>VNU Hà Nội</b></td>
                    <td>62,000</td>
                    <td>64,000</td>
                    <td>66,000</td>
                    <td>68,000</td>
                    <td>69,000</td>
                    <td>70,000</td>
                </tr>
                <tr>
                    <td><b>VNU TP.HCM</b></td>
                    <td>55,000</td>
                    <td>57,000</td>
                    <td>58,000</td>
                    <td>59,000</td>
                    <td>60,000</td>
                    <td>60,000</td>
                </tr>
                <tr>
                    <td><b>HUST</b></td>
                    <td>30,000</td>
                    <td>31,000</td>
                    <td>32,000</td>
                    <td>33,000</td>
                    <td>34,000</td>
                    <td>35,000</td>
                </tr>
                <tr>
                    <td><b>DTU</b></td>
                    <td>20,000</td>
                    <td>21,000</td>
                    <td>22,000</td>
                    <td>23,000</td>
                    <td>24,000</td>
                    <td>25,000</td>
                </tr>
                <tr>
                    <td><b>TDTU</b></td>
                    <td>24,000</td>
                    <td>25,000</td>
                    <td>26,000</td>
                    <td>27,000</td>
                    <td>28,000</td>
                    <td>28,000</td>
                </tr>
            </tbody>
        </table>
    </section>

    <section>
        <h3>Tỷ Lệ Tốt Nghiệp Qua Các Năm (%)</h3>
        <table>
            <thead>
                <tr>
                    <th>Trường Đại Học</th>
                    <th>2020</th>
                    <th>2021</th>
                    <th>2022</th>
                    <th>2023</th>
                    <th>2024</th>
                    <th>2025</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td><b>VNU Hà Nội</b></td>
                    <td>92%</td>
                    <td>93%</td>
                    <td>94%</td>
                    <td>94%</td>
                    <td>95%</td>
                    <td>95%</td>
                </tr>
                <tr>
                    <td><b>VNU TP.HCM</b></td>
                    <td>91%</td>
                    <td>92%</td>
                    <td>93%</td>
                    <td>93%</td>
                    <td>94%</td>
                    <td>94%</td>
                </tr>
                <tr>
                    <td><b>HUST</b></td>
                    <td>94%</td>
                    <td>95%</td>
                    <td>95%</td>
                    <td>96%</td>
                    <td>96%</td>
                    <td>96%</td>
                </tr>
                <tr>
                    <td><b>DTU</b></td>
                    <td>88%</td>
                    <td>89%</td>
                    <td>90%</td>
                    <td>91%</td>
                    <td>92%</td>
                    <td>92%</td>
                </tr>
                <tr>
                    <td><b>TDTU</b></td>
                    <td>87%</td>
                    <td>88%</td>
                    <td>89%</td>
                    <td>90%</td>
                    <td>91%</td>
                    <td>91%</td>
                </tr>
            </tbody>
        </table>
    </section>
</div>

<!-- TAB 3: SỰ KIỆN 2025 -->
<div id="tab3" class="tab-content">
    <section>
        <h2>Sự Kiện và Hoạt Động Nổi Bật Năm 2025</h2>
        <p>
            Các trường đại học hàng đầu Việt Nam đang tổ chức nhiều sự kiện lớn nhằm nâng cao chất lượng giáo dục, 
            hỗ trợ sinh viên phát triển kỹ năng, và tạo cơ hội kết nối với các doanh nghiệp quốc tế.
        </p>

        <div class="timeline">
            <div class="timeline-item">
                <div class="event-card">
                    <div class="event-date">📅 Tháng 3 - 4, 2025</div>
                    <h3>VNU Hà Nội - Hội Thảo Quốc Tế: "Đổi Mới Sáng Tạo trong Giáo Dục"</h3>
                    <div class="event-location">📍 Hội Trường Chính, Đại học Quốc gia Hà Nội (Cầu Giấy)</div>
                    <div class="event-description">
                        Sự kiện quy tụ hơn 500 đại biểu từ các đại học hàng đầu thế giới, chuyên gia giáo dục, 
                        và nhà tài trợ. Các bài phát biểu chính sẽ tập trung vào xu hướng công nghệ AI trong giáo dục 
                        và phương pháp dạy học hiện đại.
                    </div>
                </div>
            </div>

            <div class="timeline-item">
                <div class="event-card">
                    <div class="event-date">📅 Tháng 4, 2025</div>
                    <h3>HUST - Cuộc Thi Khởi Nghiệp "HUST Startup Challenge 2025"</h3>
                    <div class="event-location">📍 Khuôn viên HUST, Thanh Xuân, Hà Nội</div>
                    <div class="event-description">
                        Cuộc thi quy mô lớn nhằm tìm kiếm những ý tưởng khởi nghiệp độc đáo. 
                        Giải thưởng tổng cộng <b>500 triệu đồng</b> cho 3 dự án xuất sắc nhất.
                    </div>
                </div>
            </div>

            <div class="timeline-item">
                <div class="event-card">
                    <div class="event-date">📅 Tháng 5, 2025</div>
                    <h3>VNU TP.HCM - Hội Chợ Việc Làm Quốc Tế</h3>
                    <div class="event-location">📍 Trung Tâm Hội Nghị Hòa Bình, TP.HCM</div>
                    <div class="event-description">
                        Sự kiện quy tụ hơn <b>150 công ty</b>, tổ chức quốc tế tuyển dụng nhân lực. 
                        Sinh viên có cơ hội phỏng vấn trực tiếp với các HR manager.
                    </div>
                </div>
            </div>

            <div class="timeline-item">
                <div class="event-card">
                    <div class="event-date">📅 Tháng 5 - 6, 2025</div>
                    <h3>DTU & TDTU - Chương Trình Trao Đổi Sinh Viên Quốc Tế</h3>
                    <div class="event-location">📍 Đà Nẵng & TP.HCM</div>
                    <div class="event-description">
                        Chương trình trao đổi sinh viên với các đại học ở <b>Nhật Bản, Hàn Quốc, và Đức</b>. 
                        Sinh viên sẽ được học tập, thực tập tại các công ty quốc tế trong 3-6 tháng.
                    </div>
                </div>
            </div>

            <div class="timeline-item">
                <div class="event-card">
                    <div class="event-date">📅 Tháng 6, 2025</div>
                    <h3>Hội Thảo Liên Trường: "Tương Lai của Giáo Dục Đại Học Việt Nam"</h3>
                    <div class="event-location">📍 Trực tuyến + Trực tiếp tại 5 trường</div>
                    <div class="event-description">
                        Hội thảo quy tụ <b>lãnh đạo các trường</b> VNU Hà Nội, VNU TP.HCM, HUST, DTU, TDTU 
                        để thảo luận những thách thức và cơ hội trong lĩnh vực giáo dục đại học.
                    </div>
                </div>
            </div>

            <div class="timeline-item">
                <div class="event-card">
                    <div class="event-date">📅 Tháng 7, 2025</div>
                    <h3>VNU & HUST - Chương Trình Đại Sứ Giáo Dục</h3>
                    <div class="event-location">📍 Các trường phổ thông trên toàn quốc</div>
                    <div class="event-description">
                        Hai trường hàng đầu sẽ cử các sinh viên xuất sắc đi thuyết trình tại các trường phổ thông. 
                        <b>Số lượng học sinh hỗ trợ: 50,000+ học sinh</b>
                    </div>
                </div>
            </div>

            <div class="timeline-item">
                <div class="event-card">
                    <div class="event-date">📅 Tháng 9, 2025</div>
                    <h3>Lễ Khai Giảng Năm Học 2025-2026</h3>
                    <div class="event-location">📍 Các trường đại học (Tổ chức độc lập)</div>
                    <div class="event-description">
                        Tất cả các trường đại học tổ chức lễ khai giảng cho các tân sinh viên năm học mới. 
                        Các sự kiện sẽ bao gồm tham quan khuôn viên, giới thiệu chương trình học tập.
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section>
        <h2>Cơ Hội Tham Gia Các Sự Kiện</h2>
        
        <div class="event-card">
            <h4>📢 Dành cho Sinh Viên Hiện Tại:</h4>
            <ul>
                <li>✓ Tham gia các hội thảo và workshop miễn phí</li>
                <li>✓ Cơ hội thực tập tại các công ty quốc tế</li>
                <li>✓ Trao đổi sinh viên quốc tế (học bổng có thể có sẵn)</li>
                <li>✓ Cuộc thi khởi nghiệp với giải thưởng hấp dẫn</li>
            </ul>
        </div>

        <div class="event-card">
            <h4>👨‍🎓 Dành cho Học Sinh Phổ Thông:</h4>
            <ul>
                <li>✓ Tham gia chương trình giáo dục chuẩn bị đại học</li>
                <li>✓ Tìm hiểu thêm về các ngành học tại các trường</li>
                <li>✓ Gặp gỡ những sinh viên xuất sắc và nhận lời khuyên</li>
                <li>✓ Cơ hội tham gia các khóa học tăng thêm kỹ năng</li>
            </ul>
        </div>

        <div class="event-card">
            <h4>🏢 Dành cho Doanh Nghiệp & Nhân Viên HR:</h4>
            <ul>
                <li>✓ Tuyển dụng nhân lực trẻ tại các hội chợ việc làm</li>
                <li>✓ Hỗ trợ chương trình thực tập cho sinh viên</li>
                <li>✓ Thiết lập quan hệ đối tác với các trường đại học</li>
            </ul>
        </div>
    </section>

    <section>
        <h2>Liên Hệ & Thông Tin Thêm</h2>
        <div class="success-box">
            <h4>📧 Email Liên Hệ:</h4>
            <p>
                <b>VNU Hà Nội:</b> event@vnu.edu.vn<br>
                <b>VNU TP.HCM:</b> contact@vnuhcm.edu.vn<br>
                <b>HUST:</b> PR@hust.edu.vn<br>
                <b>DTU:</b> events@dtu.edu.vn<br>
                <b>TDTU:</b> activity@tdtu.edu.vn
            </p>
        </div>
    </section>
</div>

<!-- Back to Top Button -->
<div class="back-to-top" onclick="scrollToTop()">↑</div>

<footer>
    <p>Thông Liên Hệ: Lớp 12C12, THPT Võ Trường Toản</p>
    <p>© 2025 - Tất cả các quyền được bảo lưu</p>
</footer>

<script>
    function switchTab(evt, tabName) {
        // Ẩn tất cả tab content
        const contents = document.getElementsByClassName("tab-content");
        for (let i = 0; i < contents.length; i++) {
            contents[i].classList.remove("active");
        }

        // Xóa active class từ tất cả buttons
        const buttons = document.getElementsByClassName("tab-button");
        for (let i = 0; i < buttons.length; i++) {
            buttons[i].classList.remove("active");
        }

        // Hiển thị tab được chọn
        document.getElementById(tabName).classList.add("active");
        evt.currentTarget.classList.add("active");

        // Scroll to top
        window.scrollTo(0, 0);
    }

    function submitForm(event) {
        event.preventDefault();
        
        const fullname = document.getElementById('fullname').value;
        const email = document.getElementById('email').value;
        const rating = document.querySelector('input[name="rating"]:checked').value;
        const comments = document.getElementById('comments').value;
        
        const message = `Cảm ơn ${fullname}!\n\nThông tin của bạn đã được ghi nhận:\n- Email: ${email}\n- Đánh giá: ${rating}⭐\n- Nhận xét: ${comments || 'Không có'}\n\nCảm ơn bạn đã góp ý!`;
        
        alert(message);
        document.getElementById('feedbackForm').reset();
    }

    function scrollToTop() {
        window.scrollTo({ top: 0, behavior: 'smooth' });
    }

    // Back to top button visibility
    window.addEventListener('scroll', function() {
        const backToTopBtn = document.querySelector('.back-to-top');
        if (window.pageYOffset > 500) {
            backToTopBtn.classList.add('show');
        } else {
            backToTopBtn.classList.remove('show');
        }
    });
</script>

</body>
</html>
