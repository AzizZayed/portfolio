---
# date: '2025-01-11T00:18:58-05:00'
title: 'The Most Straight-to-the-Point Deep Dive Into Deep Learning'
draft: true
math: true
---
This article serves as the most straight-to-the-point deep dive into Deep Learning, from the pre-requisite math, K-Nearest Neighbours, Multi-Layer Perceptrons all the way to Transformers, inspired by the Deep Learning book.

$$
\newcommand{\train}{\mathcal{D}}
\newcommand{\valid}{\mathcal{D_{\mathrm{valid}}}}
\newcommand{\test}{\mathcal{D_{\mathrm{test}}}}
% Vector
\def\va{{\pmb{a}}}
\def\vb{{\pmb{b}}}
\def\vc{{\pmb{c}}}
\def\vw{{\pmb{w}}}
\def\vx{{\pmb{x}}}
\def\vy{{\pmb{y}}}
% Matrix
\def\mA{{\pmb{A}}}
\def\mB{{\pmb{B}}}
\def\mC{{\pmb{C}}}
\def\mI{{\pmb{I}}}
\def\mW{{\pmb{W}}}
\def\mX{{\pmb{X}}}
\def\mY{{\pmb{Y}}}
% Sets
\def\sN{{\mathbb{N}}}
\def\sR{{\mathbb{R}}}
\def\sZ{{\mathbb{Z}}}
$$

## Math Background
### Linear Algebra
#### Vectors and Matrices
A **vector** is a list of numbers, or a 
$$
\begin{align}
    \va &= 
	\begin{bmatrix}
		a_{1} \\
		a_{2} \\
		\vdots \\
		a_{n}
	\end{bmatrix}
\end{align}
$$

The **matrix product** of matrices $\mA$ and $\mB$ is $\mC = \mA\mB$ where the first element at the top left corner of $\mC$ is the dot product of the first row of $\mA$ and the first column of $\mB$.
Thus, the element $C_{i, j}$ is the dot product of the $i^{th}$ row of $\mA$, $\mA_{i,:}$ and the $j^{th}$ column of $\mB$, $\mB_{:,j}$.
More formally, $C_{i,j}=\sum_k A_{i,k}B_{k,j}$. A matrix product is associative, distributive, but *not* commutative. 
The **identity matrix** $\mI$ is neutral element in matrix multiplication where $\mA\mI=\mI\mA=\mA$. An element-wise matrix product would be the **Hadamard product** $\mC=\mA \odot \mB$ where $C_{i,j}=A_{i,j}B_{i,j}$.

The **dot product** of vectors $\va$ and $\vb$ is a special case of a matrix product denoted as  $\va \cdot \vb$ or $\va^{\top}\vb$, simply an element-wise product of the vectors.

The **inverse** of a matrix $\mA$ is $\mA^{-1}$, meant to solve equations like $\mA\vx=\vb$. We isolate $\vx$ by multiplying each side (to the left) by the inverse of $\mA$ and using the property $\mA^{-1}\mA=\mI$. Finally $\vx=\mA^{-1}\vb$.

To measure the size of a vector, we can use the $L^P$ norm of a vector

$$
L^P=|| \va ||_p = \sqrt[p]{\sum_i |a_i|^p}=\left ( \sum_i |a_i|^p \right )^{1/p}
$$

where $p \in \sR$ and $p \ge 1$.
Note that the commonly used norm is the $L^2$ norm

$$
L^2=|| \va ||_2 = \sqrt{\sum_i |a_i|^2}=\sqrt{\sum_i a_i^2}=\sqrt{\va^{\top}\va}
$$

Refer to the matrix cookbook for more matrix operations and properties.
### Calculus
### Probability Theory

## Introduction
- subset of ML .. read ML article first is recommended, but not strictly necessary
- ML had 3 phases, then DL happened
- I won't start by the perceptron like the tradition, I'll motivate DL first