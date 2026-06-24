# Plant Disease Detection using MobileNetV2

Dự án nghiên cứu và phát triển mô hình Học sâu (Deep Learning) nhằm nhận diện và phân loại tự động các loại bệnh trên lá cây trồng từ bộ dữ liệu PlantVillage. Mô hình được tối ưu hóa bằng kiến trúc MobileNetV2 để đảm bảo tốc độ suy luận nhanh và hiệu năng cao, phù hợp triển khai trên các thiết bị cấu hình giới hạn.

## Công nghệ sử dụng
- Ngôn ngữ lập trình: Python
- Thư viện/Framework chính: TensorFlow, Keras, PyTorch
- Kiến trúc mô hình: MobileNetV2
- Môi trường huấn luyện: Google Colab và Local GPU

---

## Danh sách các loại bệnh phân loại (Dataset Classes)
Bộ dữ liệu gồm 38 lớp được phân loại chi tiết qua 14 loài cây trồng khác nhau:

### 1. Khoai tây (Potato) — Trọng tâm dự án
- Bệnh úa sớm (Potato Early blight)
- Bệnh mốc sương / úa muộn (Potato Late blight)
- Lá khỏe mạnh (Potato healthy)

### 2. Cà chua (Tomato)
- Bệnh đốm vi khuẩn (Tomato Bacterial spot)
- Bệnh úa sớm (Tomato Early blight)
- Bệnh mốc sương / úa muộn (Tomato Late blight)
- Bệnh mốc lá (Tomato Leaf Mold)
- Bệnh đốm lá Septoria (Tomato Septoria leaf spot)
- Bệnh nhện đỏ phá hoại (Tomato Spider mites / Two-spotted spider mite)
- Bệnh đốm bia (Tomato Target Spot)
- Bệnh virus xoăn lùn vàng lá (Tomato Yellow Leaf Curl Virus)
- Bệnh virus khảm (Tomato Mosaic virus)
- Lá khỏe mạnh (Tomato healthy)

### 3. Táo (Apple)
- Bệnh ghẻ táo (Apple Scab)
- Bệnh thối đen (Apple Black rot)
- Bệnh rỉ sắt (Apple Cedar apple rust)
- Lá khỏe mạnh (Apple healthy)

### 4. Ngô (Corn / Maize)
- Bệnh đốm lá xám (Corn Cercospora leaf spot / Gray leaf spot)
- Bệnh rỉ sắt thông thường (Corn Common rust)
- Bệnh cháy lá ngô bản địa (Corn Northern Leaf Blight)
- Lá khỏe mạnh (Corn healthy)

### 5. Nho (Grape)
- Bệnh thối đen (Grape Black rot)
- Bệnh thối thân Esca (Grape Esca / Black Measles)
- Bệnh cháy lá do nấm (Grape Leaf blight / Isariopsis Leaf Spot)
- Lá khỏe mạnh (Grape healthy)

### 6. Ớt chuông (Pepper, bell)
- Bệnh đốm vi khuẩn (Pepper bell Bacterial spot)
- Lá khỏe mạnh (Pepper bell healthy)

### 7. Đào (Peach)
- Bệnh đốm vi khuẩn (Peach Bacterial spot)
- Lá khỏe mạnh (Peach healthy)

### 8. Dâu tây (Strawberry)
- Bệnh cháy lá dâu tây (Strawberry Leaf scorch)
- Lá khỏe mạnh (Strawberry healthy)

### 9. Các loại cây trồng khác
- Việt quất (Blueberry): Lá khỏe mạnh (Blueberry healthy)
- Anh đào (Cherry): Bệnh phấn trắng (Cherry Powdery mildew), Lá khỏe mạnh (Cherry healthy)
- Cam (Orange): Bệnh vàng lá gân xanh (Orange Haunglongbing / Citrus greening)
- Phúc bồn tử (Raspberry): Lá khỏe mạnh (Raspberry healthy)
- Đậu nành (Soybean): Lá khỏe mạnh (Soybean healthy)
- Bí ngòi (Squash): Bệnh phấn trắng (Squash Powdery mildew)

---

## Tính năng chính
- Tải và tiền xử lý, tăng cường dữ liệu ảnh tự động (Data Augmentation).
- Huấn luyện mô hình phân loại dựa trên kỹ thuật Transfer Learning với MobileNetV2.
- Đánh giá độ chính xác qua ma trận nhầm lẫn (Confusion Matrix) và đồ thị loss/accuracy.
- Dự đoán và phân loại thời gian thực trạng thái sức khỏe của lá cây từ file ảnh thô đầu vào.
