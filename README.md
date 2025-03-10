# 📊 Báo Cáo Kiểm Thử Hiệu Suất JMeter

## 1️⃣ Thời Gian Phản Hồi

### **Lần chạy 1:**
- **Trung bình:** 581ms
- **Tối thiểu:** 245ms
- **Tối đa:** 21670ms
- **Độ lệch chuẩn:** 2326.01ms

### **Lần chạy 2:**
- **Trung bình:** 657ms
- **Tối thiểu:** 26ms
- **Tối đa:** 21632ms
- **Độ lệch chuẩn:** 2583.64ms

### **📌 Nhận xét:**
✅ Thời gian phản hồi trung bình tăng từ **581ms → 657ms**, có thể do thay đổi tải hoặc tài nguyên hệ thống.  
⚠️ Thời gian phản hồi tối đa lên đến **~21 giây**, có khả năng do tắc nghẽn xử lý.

---

## 2️⃣ Thông Lượng (Throughput)

- **Lần chạy 1:** `31.6 requests/giây`
- **Lần chạy 2:** `42.8 requests/giây`

### **📌 Nhận xét:**
✅ Throughput tăng từ **31.6 → 42.8 requests/s**, cho thấy hệ thống có thể xử lý tải cao hơn.  
⚠️ Nếu throughput tăng mà thời gian phản hồi cũng tăng, có thể hệ thống đang chịu tải lớn hơn khả năng chịu đựng.

---

## 3️⃣ Tỷ Lệ Lỗi (Error Rate)

- **Lần chạy 1:** `0.00%` (Không có lỗi)
- **Lần chạy 2:** `0.29%` (Xuất hiện một số lỗi nhỏ)

### **📌 Nhận xét:**
✅ Mức lỗi **0.29%** vẫn thấp, nhưng có thể do một số request bị timeout hoặc lỗi từ server.  
⚠️ Nếu tải tiếp tục tăng, cần kiểm tra kỹ hơn để tránh lỗi tăng cao.

---

## 4️⃣ Tốc Độ Truyền Dữ Liệu

### **Lần chạy 1:**
- **Tốc độ nhận:** `674.15 KB/s`
- **Tốc độ gửi:** `7.35 KB/s`

### **Lần chạy 2:**
- **Tốc độ nhận:** `910.31 KB/s`
- **Tốc độ gửi:** `9.93 KB/s`

### **📌 Nhận xét:**
✅ Tốc độ nhận và gửi dữ liệu tăng, có thể do số lượng request hoặc dung lượng dữ liệu phản hồi lớn hơn.  
⚠️ Nếu tiếp tục tăng, có thể ảnh hưởng đến băng thông hoặc tải máy chủ.

---

## 🔎 Kết Luận Hiệu Suất

### ✅ **Ưu điểm:**
✔️ Throughput tăng từ **31.6 → 42.8 requests/s**, hệ thống có thể xử lý nhiều yêu cầu hơn.  
✔️ Tỷ lệ lỗi vẫn **thấp (0.29%)**, chưa có dấu hiệu lỗi nghiêm trọng.

### ⚠️ **Nhược điểm & Cảnh báo:**
❗ **Thời gian phản hồi tối đa quá cao (~21 giây)**, có thể làm giảm trải nghiệm người dùng.  
❗ **Độ lệch chuẩn lớn (~2300ms+),** phản ánh sự không ổn định của hệ thống.  
❗ Nếu tải tiếp tục tăng, hệ thống có thể gặp **vấn đề hiệu suất & tài nguyên.**

---

## 📌 Kết Quả Kiểm Thử Với Số Lượng Người Dùng Khác Nhau

### **20 Người Dùng:**
![image](https://github.com/user-attachments/assets/d47ed002-4c0b-4b78-bf70-db04730c36cf)
![image](https://github.com/user-attachments/assets/f2267e39-02fe-4443-9803-eaad7f7ddf23)



### **30 Người Dùng:**
![image](https://github.com/user-attachments/assets/46bcca6a-a1ab-441b-826a-8d5fc0469232)
![image](https://github.com/user-attachments/assets/bd31a6a3-a082-428f-b2d4-07763024f84d)


---

## 📝 Câu Hỏi Thảo Luận

### 1️⃣ **Tại sao kiểm thử phi chức năng lại quan trọng trong phần mềm?**
- Đảm bảo hệ thống không chỉ chạy đúng chức năng mà còn đáp ứng yêu cầu về **hiệu suất, bảo mật, khả năng mở rộng, độ ổn định và trải nghiệm người dùng.**

### 2️⃣ **Các thông số quan trọng cần theo dõi trong kiểm thử hiệu suất**
- **Thời gian phản hồi (Response Time)**: Tốc độ xử lý yêu cầu của hệ thống.  
- **Thông lượng (Throughput)**: Số lượng request xử lý trong một đơn vị thời gian.  
- **Sử dụng tài nguyên (Resource Utilization)**: CPU, RAM, băng thông, ổ cứng.  
- **Số lượng người dùng đồng thời (Concurrent Users)**: Khả năng chịu tải của hệ thống.  
- **Tỷ lệ lỗi (Error Rate)**: Phần trăm yêu cầu gặp lỗi.

### 3️⃣ **Giải pháp nếu hệ thống không đạt yêu cầu hiệu suất**
✅ **Tối ưu hóa mã nguồn**: Cải thiện thuật toán, loại bỏ truy vấn dư thừa.  
✅ **Tối ưu hóa cơ sở dữ liệu**: Sử dụng indexing, caching, tối ưu truy vấn SQL.  
✅ **Cải thiện tài nguyên hệ thống**: Tăng server, tối ưu network.  

---
