# QPoisson
[![license](https://img.shields.io/github/license/MuGemSt/QPoisson.svg)](https://github.com/MuGemSt/QPoisson/blob/main/LICENSE)
[![Build status](https://ci.appveyor.com/api/projects/status/832yt4vq8lw6hgjr?svg=true)](https://ci.appveyor.com/project/MuGemSt/qpoisson)
[![GitHub release](https://img.shields.io/github/release/MuGemSt/QPoisson.svg)](https://github.com/MuGemSt/QPoisson/releases/latest)
[![bilibili](https://img.shields.io/badge/bilibili-BV1aMDZYnEtN-fc8bab.svg)](https://www.bilibili.com/video/BV1aMDZYnEtN)

Implement Poisson blending algorithm in a simple photo editor with Qt Frame on Windows.

## Usage
| Click ![](https://user-images.githubusercontent.com/20459298/233123164-23dac4e6-6488-4686-b458-1d5bba09b72e.png) to open dest img, then click ![](https://user-images.githubusercontent.com/20459298/233123278-290fe42e-0731-45fe-9d1a-85b876947311.png) to open src img                                           | ![](https://user-images.githubusercontent.com/20459298/233123365-cfa819c6-60e0-4b47-9b7e-12f5b439e513.PNG) |
| :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :--------------------------------------------------------------------------------------------------------: |
| <b>Click ![](https://user-images.githubusercontent.com/20459298/233123432-9c14faa7-fe41-44f0-9857-0ea282d95cd7.png) to circle an area on src img, then click ![](https://user-images.githubusercontent.com/20459298/233123647-b854bb57-391c-4cd6-bf9c-accd84539437.png) to paste the circled area onto dst img</b> | ![](https://user-images.githubusercontent.com/20459298/233123748-3634ce53-28f4-44c6-9d39-9bccfac3fbf3.PNG) |
| <b>Click ![](https://user-images.githubusercontent.com/20459298/233123837-eb66ca36-32ac-495d-810a-0db32e5a3ba3.png) to blend the pasted area into dst img</b>                                                                                                                                                      | ![](https://user-images.githubusercontent.com/20459298/233123915-39ee1092-9c09-4e99-9539-e2cd36301e4c.PNG) |

## Download
```bash
git clone https://github.com/MuGemSt/QPoisson.git
cd QPoisson
```

## Environment installation, configuration & code debugging, release
Please refer to this [blog post](https://www.cnblogs.com/MuGem/p/17017063.html) for this section.

## Dependency library
[Eigen](http://eigen.tuxfamily.org) is a C++ library for linear algebra: matrices, vectors, numerical solvers, and related algorithms.

## Method
The core method for the blending process comes from [_Poisson Image Editing_](http://www.cs.jhu.edu/~misha/Fall07/Papers/Perez03.pdf), in which the formula of computing vector **_b_** is as follow:<br>
```cpp
b[i] = div ( G( Source(x,y) ) ) - Neighbor(target i) ;  // i=1..N
```

## Thanks
 - [Easyicon](https://www.easyicon.cc)
