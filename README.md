<<<<<<< HEAD
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

=======


# Scale image vừa với size mình đã setting. Chiều rộng và chiều dài của bức ảnh mới bằng hoặc lớn hơn bức ảnh cũ (vẫn phải giữ đúng tỉ lệ của bức ảnh) 
> torchvision.transforms. CenterCrop ( size )
![before_CenterCrop](https://i.stack.imgur.com/5YQBV.jpg)

![after_CenterCrop](https://i.stack.imgur.com/Bovxw.jpg)  

#Chỉnh độ sáng, độ tương phản, độ bão hòa, màu sắc
> torchvision.transforms. ColorJitter ( brightness=0 , contrast=0 , saturation=0 , hue=0 )

![colorjitter](https://paperswithcode.com/media/methods/output_35_0_DxAQHli.png)

#Cắt bức ảnh ban đầu thành 4 ảnh cắt 4 góc và phần ở giữa
#size: output size của bức ảnh cắt (ở dạng (...,h,w)
torchvision.transforms. FiveCrop ( size )

# Chuyển bức ảnh thành Grayscale image (ảnh đen trắng)
torchvision.transforms. Grayscale ( num_output_channels=1 )

# Bồi thêm vào tất cả các cạnh của bức ảnh một giá trị "pad" cho trước.
# padding(int, hoặc (...x,y)): nếu là int thì là pad cả 4 cạnh, 
# nếu là (x,y) thì pad viền trái, phải giá trị x, pad viền trên/ dưới giá trị y; 
# nếu là (x, y, z, t) thì là pad cả 4 cạnh giá trị tương ứng

#fill = số/ str/ tuple : Nếu là tuple (x, y, z) sẽ fill vào channels R, G, B tương ứng, chỉ dùng khi padding_mode = 'constant'

#padding_mode: 
'constant': pad vói một giá trị cụ thể được khai báo ở 'fill'
'edge' : pad với giá trị ở neighbor (giá trị ở cạnh) 
	
torchvision.transforms. Pad ( padding , fill=0 , padding_mode=‘constant’ )
torchvision.transforms. RandomAffine
torchvision.transforms. RandomApply
torchvision.transforms. RandomChoice
torchvision.transforms. RandomCrop
torchvision.transforms. RandomGrayscale
torchvision.transforms. RandomHorizontalFlip
torchvision.transforms. RandomOrder
torchvision.transforms. RandomPerspective
torchvision.transforms. RandomResizedCrop
torchvision.transforms. RandomRotation
torchvision.transforms. RandomSizedCrop
torchvision.transforms. RandomVerticalFlip
torchvision.transforms. Resize
torchvision.transforms. Scale
torchvision.transforms. TenCrop
torchvision.transforms. LinearTransformation
torchvision.transforms. Normalize
torchvision.transforms. ToPILImage
torchvision.transforms. ToTensor
torchvision.transforms. Lambda
torchvision.transforms.functional. adjust_brightness
torchvision.transforms.functional. adjust_contrast
torchvision.transforms.functional. adjust_gamma
torchvision.transforms.functional. adjust_hue
torchvision.transforms.functional. adjust_saturation
torchvision.transforms.functional. affine
torchvision.transforms.functional. crop
torchvision.transforms.functional. five_crop
torchvision.transforms.functional. hflip
torchvision.transforms.functional. vflip
torchvision.transforms.functional. normalize
torchvision.transforms.functional. pad
torchvision.transforms.functional. perspective
torchvision.transforms.functional. resize
torchvision.transforms.functional. resized_crop
torchvision.transforms.functional. rotate
torchvision.transforms.functional. ten_crop
torchvision.transforms.functional. to_grayscale
>>>>>>> 4c269454d3f742ee5e8e1b479afadfbe7f8ec8e4
