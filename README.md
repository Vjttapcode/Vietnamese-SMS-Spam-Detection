# Vietnamese-SMS-Spam-Detection

Dự án ứng dụng NLP và mô hình học máy để xây dựng mô hình phát hiện các tin nhắn rác, "spam" từ tập dữ liệu tin nhắn văn bản Tiếng Việt cho trước. Việc xây dựng ứng dụng mô hình ngôn ngữ lớn trong hệ thống phân loại tin nhắn giúp cá nhân và các doanh nghiệp tiết kiệm thời gian và công sức cũng như là vận dụng sự phát triển mạnh mẽ của các mô hình xử lý ngôn ngữ tự nhiên (NLP).

Dự án là đề tài môn Thực tập cơ sở tại Học viện Công nghệ Bưu chính Viễn thông.

## Mục lục

- [Giới thiệu](#giới-thiệu)
- [Thuật toán](#thuật-toán)
- [Kết quả](#kết-quả)
- [Liên hệ](#liên-hệ)

## Giới thiệu:

- phạm vi đề tài: Tập trung vào phân loại nội dung tin nhắn đầu vào dựa trên ngữ nghĩa, không xét đến các yếu tố bổ sung như thời gian gửi, người gửi hay tác động từ các yếu tố bên ngoài.
- Mô hình: Sử dụng mô hình ngôn ngữ lớn (LLM) có khả năng xử lý tiếng Việt PhoBERT. Chủ yếu sử dụng kỹ thuật fine-tuning trên mô hình đã được huấn luyện trước.
- Tham số đánh giá: chỉ số như Accuracy, F1-score, AUC và CM.

## Thuật toán, mô hình sử dụng:
- phoBERT: mở fine tune các lớp cuối (lớp 8 trở lên) tập trung vào đặc trưng ngữ nghĩa của văn bản.
- Kỹ thuật tăng cường dữ liệu EDA (Easy Data Augmentation): tăng số lượng và tạo sự đa dạng cho của dữ liệu huấn luyện.
- Cấu hình hàm mất mát: Xây dựng hàm mất mát BCEWityhLogitsLoss có trọng số lớp để cân bằng tác động giữa mẫu “spam” và “ham” trong mô hình phân loại nhị phân giúp mô hình không thiên lệch về lớp chiếm đa số.

## Kết quả: 

Kết quả trên tập thử đã đạt 97% accuracy và mô hình đã hội tụ sau 3 vòng lặp. Đây là một kết quả cho thấy mô hình đã phân loại tin nhắn spam rất tốt với tỉ lệ bỏ sót tin nhắn spam là 0%.
