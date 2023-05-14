
**Nội dung của Repo**

**Phần 2**: thực nghiệm trên bộ dữ liệu Fashion MNIST, với thuật toán Softmax Regression. Kết quả chỉ đạt 86\% cho tập train. Với độ chính xác này, mô hình này chưa thể làm mọi người tin, để mang đi phân loại. 

**Phần 3**: dùng thuật toán Multi-layer Perceptron, với 1 hidden layer có 256 neuron, và kết quả là khoảng 93\% trên tập train. Em thấy kết quả này khá tốt, liền mang qua thử với bộ dữ liệu phức tạp hơn là Cifar10, thì kết quả chỉ khoảng 55\% trên tập train. Điều này chứng tỏ thuật toán Multi-layer Perceptron tệ khi bộ dữ liệu phức tạp hơn.

**Phần 4**: dùng mạng học sâu CNN với 6 lớp convolutional layer, để thử cải tiến nhược điểm trên của Multi-layer Perceptron, và kết quả đạt 72\% trên tập train.

**Phần 5**: Theo các nhà nghiên cứu, một mô hình càng sâu thì càng tốt, vì thế em tăng lên dùng 9 hidden convolutional layer, và kết quả là bị gradient vanishing. Lý do là em đã dùng hàm activation là sigmoid cho các hidden layer.

**Phần 6**: Khắc phục nhược điểm của hàm sigmoid bằng cách dùng ReLU, và kết quả cho thấy mô hình học rất tốt trên tập train, khoảng 99\%. Tuy nhiên mô hình bị overfitting.

**Phần 7**: Thử tăng thêm layer, dùng 12 hidden convolutional layer để xem mô hình có học tốt hơn nữa không? Và kết quả là bị gradient vanishing, mặc dù đã dùng các tham số tốt nhất: optimizer là Adam, Xavier Initization mặc định trong tensorflow, hàm kích hoạt ReLU. Và em đã khắc phục vấn đề này bằng 4 phương pháp, tương ứng với 4 Phần tiếp theo.

**Phần 8**: Khắc phục bằng việc dùng Z Score Normalization để chuẩn hóa dữ liệu.

**Phần 9**: Khắc phục bằng việc dùng hàm khởi tạo mạnh hơn: He Initialization.

Phần 10: Khắc phục bằng việc dùng Batch Normalization.

Phần 11: Khắc phục bằng việc dùng Skip Connection.