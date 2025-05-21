# BTL_TTCSN
# Đề Tài: Xây dựng hệ thống gợi ý phim

## Giới Thiệu
Dự án này xây dựng hệ thống gợi ý phim dựa trên hành vi người dùng bằng thuật toán K-Nearest Neighbors (KNN). Dữ liệu được xử lý từ tập MovieLens, và thuật toán tìm ra những người dùng có sở thích tương tự để đề xuất phim mà người dùng hiện tại chưa xem.

## Mục lục
- [Giới thiệu](#giới-thiệu).

- [Tính năng](#tính-năng)

- [Công nghệ sử dụng](#công-nghệ-sử-dụng)

- [Cấu trúc dự án](#cấu-trúc-dự-án)

- [Yêu cầu cài đặt (Prerequisites)](#yêu-cầu-cài-đặt-prerequisites)

- [Hướng dẫn cài đặt](#hướng-dẫn-cài-đặt)

- [Hướng dẫn sử dụng](#hướng-dẫn-sử-dụng)

- [Cách hoạt động](#cách-hoạt-động)

- [Đóng góp](#đóng-góp)

## ✨ Tính năng
- Đọc và xử lý dữ liệu từ Google Drive.
- Xây dựng ma trận người dùng - phim dạng thưa (sparse matrix).
- Áp dụng KNN để tìm người dùng tương tự.
- Gợi ý phim mà người dùng chưa xem nhưng người dùng tương tự đã đánh giá cao.

## 🛠️ Công nghệ sử dụng
- **Ngôn ngữ lập trình**:  Python
- **IDE**: Google Colab
- **Thư viện**:pandas, numpy, scikit-learn, scipy

## 📁 Cấu trúc dự án
plaintext
Sao chép mã
.
├── movies.csv                  # Thông tin phim
├── ratings_small.csv          # Dữ liệu đánh giá phim của người dùng
├── movie_recommendation.ipynb # File notebook chính chạy hệ thống
└── README.md                  # Tài liệu hướng dẫn

## Yêu cầu cài đặt
Nếu bạn sử dụng Google Colab, mọi thư viện đều đã được cài sẵn. Nếu chạy cục bộ, bạn cần:

   ```bash
    pip install pandas numpy scipy scikit-learn
   ```

## Hướng dẫn cài đặt
Tải dữ liệu từ MovieLens (ratings_small.csv & movies.csv).
Tải notebook movie_recommendation.ipynb lên Google Colab.
Lưu 2 file CSV vào Google Drive của bạn.

## Hướng dẫn sử dụng
 ### 1.Mount Google Drive trong Colab:
   ```bash
    from google.colab import drive
    drive.mount('/content/drive')
   ```
 ### 2.Cập nhật đường dẫn tới file CSV trong code:
   ```bash
  movies = pd.read_csv('/content/drive/MyDrive/movies.csv')
  rating = pd.read_csv('/content/drive/MyDrive/ratings_small.csv')
   ```
 ### 3.Chạy toàn bộ notebook để huấn luyện và nhận kết quả gợi ý phim.

## ⚙️ Cách hoạt động
- Chọn 200 người dùng đầu tiên từ tập dữ liệu.
- Xây dựng ma trận người dùng - phim (User-Item Matrix).
- Dùng KNN (cosine similarity) để tìm 5 người dùng có hành vi tương tự.
Gợi ý 1 bộ phim từ mỗi người dùng tương tự mà người dùng hiện tại chưa xem, ưu tiên phim được đánh giá cao.

## 🤝 Đóng góp
Bạn có thể đóng góp bằng cách: 
1. Fork repository, tạo nhánh mới và gửi pull request.
2. Sửa lỗi, cải thiện hiệu năng, hoặc thử nghiệm thêm các thuật toán nâng cao (SVD, hybrid, deep learning...).
3. Báo cáo lỗi hoặc đề xuất cải tiến thông qua phần issues trên GitHub.
