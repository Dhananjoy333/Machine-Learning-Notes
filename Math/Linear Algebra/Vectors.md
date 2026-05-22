Vector can be understood in three ways :

-  Physics Perspective : Vectors are arrows pointing in space which has two main component magnitude and direction. If both remain the same we can move it around and its the same.
    
    - Here all are same vector as magnitude and direction remain same
    

![[vectors.png]]

- Computer Science perspective : its simply is a list of number representing some quantity. For ex - [2000, 5] here 2000 could be house rent price and 5 could be rooms, or 2000 could be price of 5 bicycle. here the order matters [2000, 5] ≠ [5, 2000], here we represent house vs price as vector.

- Mathematician Perspective : It basically says vector can be anything as long as we can add or multiple vectors.

In Linear algebra when we talk about vectors almost all the time we imagine tail of vector to be at origin of coordinate plane.

![[Screenshot_(446).png]]

in 3D

![[Screenshot_(448).png]]

  

## Vector Addition/Subtraction

To add or subtract two vector we can think of it as

![[Screenshot_(451).png]]

- when we add two vectors we can think of moving the tail of any one vector to head of other vector and drawing a vector from origin to moved vector’s head.

Why ?

- When we see learn in 1 D i.e, number line 5 + 2 can be said as moving file step to front and again 2 more step then we reach 7 same with first 2 step and then 5 step here too vector addition is simple first moving in any one vector direction and then moving in second vector direction. i.e, resultant of moving in x-axis vector A = 2 and vector B = 2 so in x-axis we move 2 + 2 till position 4 and in y-axis vector A = 3; vector B = -2 so 2 + (-3) = 1 so move 1 position in y-axis. So resultant is 4,1.

## Scalar Multiplication

When we multiply a number to a vector we increase or decrease the vector this is called ==Scaling== and the number by which we multiply its called ==Scalars.==

![[Screenshot_(452).png]]

- The resultant vector is simply the the scalar multiplication of individual values of vector.

![[Screenshot_(453).png]]

## Basis Vectors

==Basis Vectors== are basically a reference from which we create the vector they are represented by : $\hat{i}$ and $\hat{j}$ (i-hat and j-hat).

We represent all other vector as vector scaling and addition of basis vectors. Here basis vector are unit vectors.

![[Screenshot_(455).png]]

It necessarily does not has to be unit it can be any value

![[Screenshot_(457).png]]

Here the basis vector are (1, 1) and (1, -1). Here the vector C is same but as basis vector changed coordinate of Vector C changed but no matter what basis vector we choose we can recreate any vector in different basises its just that coordinate changes.

This act of showing vector as scaling and addition of basis vector is called ==Linear Combination.==

## Span

The set of all vector that can be created by linear combination of two vector is called ==span.==

For a given v and w vector in 2D space there are 3 possible cases :

- If vector v and w are not overlapping and allowed to move freely it can create all possible vector existing in 2D space. So, here the span of vector v and w is all vector existing in the 2D plane.

![[Screenshot_(458).png]]

- If vector v and w overlap each other and allowed to move freely all vector existing in the line of overlap can be created by v and w. So, here the span of vector v and w is all vector which exist in line overlapping the vectors.

![[Screenshot_(459).png]]

- If both vector are 0 only possible vector is origin. So, here span of vector v and w is just the origin.

![[Screenshot_(460).png]]s $\vec{v} = \begin{bmatrix} 5 \\ 3 \\ 0 \end{bmatrix}$