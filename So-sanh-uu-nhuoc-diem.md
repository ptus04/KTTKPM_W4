# So sánh ưu/nhược điểm

| Architecture characteristics | Layered Architecture                                | Microkernel Architecture |
| ---------------------------- | --------------------------------------------------- | ------------------------ |
| Deployability                | Khó deploy hơn vì phải deploy cả cục mỗi khi update | Dễ deploy hơn vì các plugin có thể độc lập phát triển |
| Elasticity                   | Khó hơn vì tính monolithic                          | Tương tự vì cũng là monolithic                        |
| Evolutionary                 | Khó hơn                                             | Dễ hơn vì các plugin độc lập nên dễ thay đổi          |
| Fault tolerance              | Chịu lỗi kém: Lỗi xảy ra thì cả ứng dụng đều lỗi    | Tương tự                                              |
| Modularity                   | Không có tính module                                | Có module nhưng chỉ dừng lại ở mức mở rộng            |
| Overall cost                 | Chi phí thấp                                        | Tương tự                                              |
| Performance                  | Hiệu năng kém hơn                                   | Hiệu năng trung bình                                  |
| Reliability                  | Độ tin cậy trung bình                               | Độ tin cậy tương tự                                   |
| Scalability                  | Khó scale do tính chất monolithic                   | Tương tự                                              |
| Simplicity                   | Cực kỳ đơn giản                                     | Phức tạp hơn chút                                     |
| Testability                  | Hơi khó test                                        | Dễ test hơn, đặc biệt là từng module                  |


==> Microkernel là thích hợp nhất trong 2 styles vì có nhiều tính chất tốt hơn như dễ deploy, mở rộng các tính năng hơn
