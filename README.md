# Image Augmentation

Là kĩ thuật để tăng số lượng dữ liệu trong dataset trong trường hợp quá ít dữ liệu.
để training mô hình học sâu (Deep learning model)
Về cơ bản, càng nhiều dữ liệu, mô hình deep learning của mình sẽ càng hiệu quả
![alt](https://cdn.analyticsvidhya.com/wp-content/uploads/2021/03/Screenshot-from-2021-03-10-14-05-33.png)

Vấn đề ta gặp phải khi thiếu dữ liệu là việc "học vẹt" của máy, tức là có kết quả tốt với những bức ảnh đã được train, nhưng lại "bó tay với những bức ảnh mới 

Cách giải quyết vấn đề
1. Tự mình đi thu thập thêm dữ liệu
> Việc này rất tốn thời gian và công sức. Nhiều lúc dữ liệu vốn đã hạn chế và không thể tìm thêm được nữa (Ví dụ hình ảnh các con vật hiếm)

2. Tự mình vẽ ra dữ liệu fake
> Tốn thời gian và thậm chí là tiền bạc để có thể có những bức ảnh fake hoàn chỉnh. Tuy nhiên những bức ảnh đó có thể gây lỗi khi training do không đúng với thực tế

3. Bắt một đứa team AI code để tạo thêm dữ liệu từ những bức ảnh gốc ban đầu
> Việc này không tốn nhiều thời gian, chi phí thấp, chỉ khổ thằng coder thôi

![alt](https://paperswithcode.com/media/thumbnails/task/task-0000001560-029cbc00.jpg)

