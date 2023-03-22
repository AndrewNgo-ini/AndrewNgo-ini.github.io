---
title: "What is Neural Network?"
date: 2020-12-14T15:15:16+07:00
tags:
  - "tech"
  - "learn"
draft: false
cover:
    #image: "https://i.ibb.co/K0HVPBd/paper-mod-profilemode.png"
    # can also paste direct link from external site
    # ex. https://i.ibb.co/K0HVPBd/paper-mod-profilemode.png
    alt: "<alt text>"
    caption: "<text>"
    relative: false # To use relative path for cover image, used in hugo Page-bundles
---
Xin chào mừng các bạn tới với serie Deep Learning đầu tiên của mình, mục tiêu của serie này là:

*   Hiểu rõ về thuật toán Neural Networks (Deep Learning)
*   Tìm hiểu sơ lược qua để học AI bạn cần biết những gì

Để có thể dễ dàng hiểu serie này bạn chỉ cần có kiến thức lập trình cơ bản, một chút toán hoặc nếu bạn tò mò AI là gì thì vẫn có thể đọc vì trong quá trình viết mình sẽ cung cấp những kiến thức cần thiết để bạn tìm hiểu thêm nếu hứng thú.

**I: Vậy AI/ML là gì ?**
------------------------

Mình tin chắc về khoản định nghĩa google có thể làm tốt hơn mình, cho nên nói một cách dân dã thì AI/ML cũng chỉ là 1 function nhận vào input và cho ra output mình mong muốn.

Vd:  
\+ Function tìm số lớn hơn max(a,b) giữa 2 số cho trước. Input : a, b. Output: số lớn hơn  
\+ Ở AI/ML bạn có thể có input là 1 mảng chứa các thuộc tính của 1 căn nhà (độ dài, độ rộng, số phòng ngủ,..) Output sẽ là giá nhà dự kiến

![](http://www.some-emotions.studio/wp-content/uploads/2020/03/Supervised-Learning-with-Neural-Networks-deeplearning.ai-Coursera-Mozilla-Firefox.jpg)

Một vài ví dụ khác:  
Input: 1 tấm ảnh- Output: tất cả các vật thể trong tấm ảnh - Ứng dụng trong tag ảnh  
Input: Quảng cáo, thông tin người dùng- Output: 1 (người dùng click), 0(người dùng không click) - Ứng dụng trong quảng cáo online  
  

### **II. Neural networks**  
**_1\. Nguồn cảm hứng:_**

Một neural (nơ-rôn) là tế bào thần kinh não sẽ nhận được các tín hiệu điện từ các neural khác trong não của bạn sau đó sẽ thực hiện tính toán và tiếp tục quá trình này tới các neural khác. Các neural (x1,x2,x3) -> tính toán -> y

![](http://www.some-emotions.studio/wp-content/uploads/2020/03/What-does-this-have-to-do-with-the-brain-deeplearning.ai-Coursera-Mozilla-Firefox.jpg)

Sự liên quan giữa Deep Neural Network và bộ não con người, và 1 đống công thức toán bạn sẽ học :D

### **_2.Bắt đầu nhẹ nhàng..._**

Bạn nhớ mình nói NN (Neural Networks) thật chất chỉ là một function thôi chứ. Bây giờ mình sẽ thử tạo một function theo phép tính OR.  

    def pheptoanOR(x1, x2):
        return sigmoid(-10 + 20*x1 + 20*x2)

  
Theo đoạn code trên, pheptoanOR của mình trả về 1 biểu thức toán (-10 +20x1 +20x2) đặt trong 1 function tên sigmoid(), hiện tại các bạn cứ hiểu nó sẽ output 1 con số trong dãy từ 0 -> 1 với bất kỳ input nhận vào, mình sẽ còn gặp lại sigmoid ở phần sau.

![](http://www.some-emotions.studio/wp-content/uploads/2020/03/Command-Prompt.jpg)

Kết quả của chúng ta khi gọi function

Và với 1 chút biến đổi ...  

![](http://www.some-emotions.studio/wp-content/uploads/2020/03/Examples-and-Intuitions-I-Coursera-Mozilla-Firefox.jpg)

Cũng là đoạn function trên nhưng là dưới dạng 1 NN

Ở đây các hệ số -10, 20, 20 sẽ được gọi là w (weights), như vậy ta sẽ có  
w1 = -10  
w2 = 20  
w3 = 20  
Input là x1,x2  
Output là g(-10 + 20x1 + 20x2)

Một vài câu hỏi được đặt ra: những con số -10, 20,20 nó ở đâu ra vậy, có thể hiểu đơn giản là những con số này được nghĩ ra để phù hợp với mục đích là phép tính OR. Với bất kì input x1, x2 nhận vào đều thỏa mãn kết quả chúng ta mong muốn.

Nếu chúng ta điều chỉnh w1, w2, w3 khác đi, kết quả là function này có thể không còn là function của phép tính OR nữa. Trên thực tế output chúng ta không phải lúc nào cũng là một phép tính OR đơn giản để ta có thể tự suy ra w1, w2, w3. Chính vì thế w1,w2,w3,... cần phải được "HỌC" để "điều chỉnh" tới một con số nào đó mà thỏa mãn Output của chúng ta

* * *

Thế là hết phần 1 rồi, ở phần tới mình sẽ tiến hành giới thiệu ngay một mô hình hoàn chỉnh của Deep Neural Networks, một số hình ảnh được lấy trong khóa học Machine Learning with Andrew Ng, Deep Learning Specialization (2 khóa học bất hủ của đối với những bạn self-taught :D, nếu hứng thú bạn có thể xem qua nhé, nếu có bất kì thắc mắc hoặc sai sót nào bạn có thể comment cho mình biết. Thank you for reading !!!