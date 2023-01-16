---
title: "RNN"
date: 2022-11-14T15:15:16+07:00
draft: false
---
I. RNN là gì?
-------------

Đầu tiên mình xin giới thiệu 1 số ứng dụng của Sequence Model (RNN)

![](http://www.some-emotions.studio/wp-content/uploads/2020/03/Why-sequence-models-deeplearning.ai-Coursera-Mozilla-Firefox-1024x576.jpg)

RNN là một biến thể của Neural Networks được sử dụng thường xuyên ở trong NLP (Natural language processing)  
Ở một mạng Neural thông thường, các input được xử lý thông qua các layers và chúng ta có output, trong trường hợp này những input liên tiếp nhau được xem như không phụ thuộc vào nhau (independent)

Tuy nhiên, khi gặp các bài toán thực tế, chúng ta lại mong muốn các input phụ thuộc (dependent) lẫn nhau.  
Ví dụ: dự đoán chữ tiếp theo trong một chuỗi.

Nói về nghĩa đen, Recurrent (tái xuất hiện) bởi vì chúng thực hiện cái task giống hệt nhau cho mỗi element của một chuỗi mà trong đó output hiện tại phụ thuộc vào việc tính toán trước đó.

![](http://www.some-emotions.studio/wp-content/uploads/2020/03/1-buMl05BvEPJ5P7sB5ImTCg.jpeg)

Các bạn có thể tưởng tượng bức hình như một multilayer neural network với mỗi layer biểu diện sự quan sát ở một thời gian t

II. Tại sao chúng ta cần RNN?
-----------------------------

Lý do thứ nhất mà mình có thể nói từ phần trên là vì các output của thời điểm t sẽ có input là từ thời điểm t-1 và đồng thời feature X<t>. Từ đó chúng ta có thể tạm gọi là RNN có thể "lưu trữ" thông tin phía trước

Lý do thứ hai: một mạng NN bình thường sẽ có input và output cố định (fixed-size), RNN thì không

The parameters required for handling text will be very large in case of Standard neural networks. RNN requires much less parameters to learn (lý do mình tìm được, chắc mình sẽ implement một ngày không xa để tìm hiểu tại sao, hi :D)

* * *

Tuy nhiên RNN vẫn chưa đáp ứng được so với real-world problem, sắp tới mình sẽ viết thêm về LSTM, GRU. Các bạn đón xem nhé :D

Một số tư liệu mình tham khảo:  
https://towardsdatascience.com/understanding-neural-networks-from-neuron-to-rnn-cnn-and-deep-learning-cd88e90e0a90  
https://www.quora.com/Why-do-we-use-an-RNN-instead-of-a-simple-neural-network

==Fist== What?

RNN is different type of structure of Neural Network, they designed it like that just to make use of sequence learning .

++So what is the differnt, why not use simple RNN ? ++
+ Input size and outputsize stay fixed, even u can padding it, its doesn seem to make any representation about it
-> handle??

+ Share learning ??




#implement note


AT TIME STEP T, each cell

Input X (m, nx)
hiddenstate (m,na)
=> (m, nx) * (nx, na)  =(m, na) (1)



Previous A (m, na)
hiddenstate (m, na)
=> (m,na) *  (na, na) = (m, na) (2)

(1) + (2) + ba -> (m, na)


Output y (m, ny)
hiddenstate (m, na)
=> (m, na) *  (na, ny)    = (m, ny)



#notes on foward : theo keras, way = 0, nhung phan backprop thi ko thay cap nhat way?
                    


###implement backprop base on https://towardsdatascience.com/back-to-basics-deriving-back-propagation-on-simple-rnn-lstm-feat-aidan-gomez-c7f286ba973d

#notes on building RNN step by step coursera -> + ko co dao ham layer cuoi theo Loss
                                                + tai sao lai dao ham bien X theo Hidden state (a)?
                                                + co dX va` da0 trong dao. ham (tuy nhien khong cap nhat?)
                                                + chi cap nhat dWax, dWaa, dba 
                                                + 