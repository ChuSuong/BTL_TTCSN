# BTL_TTCSN
📽️ Movie Recommendation System using KNN
🧠 Giới thiệu
Dự án này xây dựng hệ thống gợi ý phim dựa trên hành vi người dùng bằng thuật toán K-Nearest Neighbors (KNN). Dữ liệu được xử lý từ tập MovieLens, và thuật toán tìm ra những người dùng có sở thích tương tự để đề xuất phim mà người dùng hiện tại chưa xem.

📚 Mục lục
📽️ Giới thiệu

📚 Mục lục

✨ Tính năng

🛠️ Công nghệ sử dụng

📁 Cấu trúc dự án

📦 Yêu cầu cài đặt

🔧 Hướng dẫn cài đặt

▶️ Hướng dẫn sử dụng

⚙️ Cách hoạt động

🤝 Đóng góp

✨ Tính năng
Đọc và xử lý dữ liệu từ Google Drive.

Xây dựng ma trận người dùng - phim dạng thưa (sparse matrix).

Áp dụng KNN để tìm người dùng tương tự.

Gợi ý phim mà người dùng chưa xem nhưng người dùng tương tự đã đánh giá cao.

🛠️ Công nghệ sử dụng
Python 3.x

Google Colab

Thư viện:

pandas

numpy

scikit-learn

scipy

📁 Cấu trúc dự án
plaintext
Sao chép mã
.
├── movies.csv                  # Thông tin phim
├── ratings_small.csv          # Dữ liệu đánh giá phim của người dùng
├── movie_recommendation.ipynb # File notebook chính chạy hệ thống
└── README.md                  # Tài liệu hướng dẫn
📦 Yêu cầu cài đặt
Nếu bạn sử dụng Google Colab, mọi thư viện đều đã được cài sẵn. Nếu chạy cục bộ, bạn cần:

bash
Sao chép mã
pip install pandas numpy scipy scikit-learn
🔧 Hướng dẫn cài đặt
Tải dữ liệu từ MovieLens (ratings_small.csv & movies.csv).

Tải notebook movie_recommendation.ipynb lên Google Colab.

Lưu 2 file CSV vào Google Drive của bạn.

▶️ Hướng dẫn sử dụng
Mount Google Drive trong Colab:

python
Sao chép mã
from google.colab import drive
drive.mount('/content/drive')
Cập nhật đường dẫn tới file CSV trong code:

python
Sao chép mã
movies = pd.read_csv('/content/drive/MyDrive/movies.csv')
rating = pd.read_csv('/content/drive/MyDrive/ratings_small.csv')
Chạy toàn bộ notebook để huấn luyện và nhận kết quả gợi ý phim.

⚙️ Cách hoạt động
Chọn 200 người dùng đầu tiên từ tập dữ liệu.

Xây dựng ma trận người dùng - phim (User-Item Matrix).

Dùng KNN (cosine similarity) để tìm 5 người dùng có hành vi tương tự.

Gợi ý 1 bộ phim từ mỗi người dùng tương tự mà người dùng hiện tại chưa xem, ưu tiên phim được đánh giá cao.

🤝 Đóng góp
Bạn có thể đóng góp bằng cách:

Fork repository, tạo nhánh mới và gửi pull request.

Sửa lỗi, cải thiện hiệu năng, hoặc thử nghiệm thêm các thuật toán nâng cao (SVD, hybrid, deep learning...).

Báo cáo lỗi hoặc đề xuất cải tiến thông qua phần issues trên GitHub.
