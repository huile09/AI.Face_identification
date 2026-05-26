# Hệ Thống Nhận Diện Khuôn Mặt

Dự án sử dụng mạng nơ-ron tích chập (CNN) tự dựng dựa trên thư viện Keras/TensorFlow để giải quyết hai bài toán: Nhận diện khuôn mặt.

---

## Tải Xuống Mô Hình Đã Huấn Luyện (Pre-trained Models)

Do kích thước file ma trận trọng số `.h5` của các mô hình Deep Learning khá lớn và vượt quá giới hạn lưu trữ thông thường của GitHub, bạn vui lòng truy cập vào các đường liên kết Google Drive dưới đây để tải file cấu hình dự án:

* **Mô hình Nhận diện Khuôn mặt (80 Epochs):** 👉 [Tải file mo_hinh_cnn_80_epochs.h5 tại đây](https://drive.google.com/file/d/1QxVkbvjlQpVqofOmhwwaA3ePAnUzzg0L/view?usp=sharing)

## Hướng Dẫn Sử Dụng Trong Google Colab

Để chạy thử nghiệm và kiểm tra mô hình với các tập dữ liệu ảnh mới, bạn chỉ cần nạp lại file `.h5` bằng đoạn mã Keras sau:

```python
from tensorflow.keras.models import load_model

# Nạp mô hình từ đường dẫn lưu trữ
model_path = 'mo_hinh_cnn_80_epochs.h5' # hoặc file tiền polymer
reloaded_model = load_model(model_path)

print("Đã nạp thành công mô hình! Sẵn sàng thực hiện predict ảnh test.")
