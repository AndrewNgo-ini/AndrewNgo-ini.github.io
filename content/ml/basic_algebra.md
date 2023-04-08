---
title: "Basic Linear Algebra"
date: 2020-11-14T15:15:16+07:00
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
I. Vector
---------

*   What is a vector
*   Linear combination
*   Basis vector
*   Span
*   Linear independent

#### What is a vector
<!---
![](http://www.some-emotions.studio/wp-content/uploads/2020/09/gif.gif)
-->
A vector with its coordinates can be understood as a guide on how to go from the origin (O) to its tail.

#### Basis vector (vector cơ sở)
<!---
![](http://www.some-emotions.studio/wp-content/uploads/2020/09/linearcombination.gif)
-->
In the XY coordinate system, a vector pointing to the right with a length of 1 is called i-hat or the unit vector of the X-axis. Similarly, the vector pointing upwards with a length of 1 is called j-hat or the unit vector of the Y-axis.

#### Linear combination (tổ hợp tuyến tính)
<!---
![](http://www.some-emotions.studio/wp-content/uploads/2020/09/linearcombination2.gif)
-->
According to the gif, the i-hat basis vector of ours is scaled 3 times, while the y-hat is scaled 2 times in the opposite direction. Now, the vector is represented as the sum of the two scaled vectors (3)i + (-2)j

#### Span (bao tuyến tính)
<!---
![](http://www.some-emotions.studio/wp-content/uploads/2020/09/span.gif)
-->
By obtaining a set of all linear combinations from basis vectors, we get all the points in a 2D plane (line if 1D) This is called span.

#### Linear indepentdent (độc lập tuyến tính)
<!---
![](http://www.some-emotions.studio/wp-content/uploads/2020/09/lineardepentdent.gif)
-->
In a case, when both of our basis vectors overlap each other, the removal of one vector without affecting the span is called Linear dependent (opposite of Linear Independent). Thus, we can infer that our basis vectors have the property of Linear independence to each other.

II. Vector basic operation
--------------------------

*   Add vectors
*   Multiply by a scalar
*   Modulus
*   Dot product

#### Add vectors/ Multiply by a scarlar

The sum of two vectors is calculated by adding the values of each of them. When multiplying a vector by a number, we multiply that number by each of the values of the vector.
<!---
![](http://www.some-emotions.studio/wp-content/uploads/2020/09/Screenshot-from-2020-09-21-12-47-17.png)
-->
#### Modulus
<!---
![](http://www.some-emotions.studio/wp-content/uploads/2020/09/Screenshot-from-2020-09-21-13-01-42.png)
-->
#### Dot product (scalar product) (tích vô hướng)

**A** = \[_A_1, _A_2,..., _A__n_\] và **B** = \[_B_1, _B_2,..., _B__n_\] được định nghĩa như sau:
![](https://wikimedia.org/api/rest_v1/media/math/render/svg/af37e403a991bc025d1393175c48da59f50db69b)
Calculating the dot product leads to some interesting connections, such as:

#### Dot product vs Modulus
![](https://wikimedia.org/api/rest_v1/media/math/render/svg/4684ec0ed118a6ed4e12a43c1fb4a8cc8ef41c06)
#### Dot product vs Cosine
![](https://wikimedia.org/api/rest_v1/media/math/render/svg/e6c94733992f42b0576562b7936e4a160b058089)
III. Changing basis
-------------------

Changing the basis vectors means that we are using the Dot Product on the new basis vectors. Since the dot product is linear, the dot product of the new basis vectors will be a linear combination of the dot products of the original basis vectors. So the dot product will still be the same but with different coefficients.