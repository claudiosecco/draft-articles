# How to choose between harmonic or arithmetic mean
## Introduction
In many cases the use of arithmetic mean (weighted or not) is mistaken, when the correct choice would be the use of harmonic mean. I intend to show a very simple and practical way to choose between the two.

The method shown here consists of a very simple way of thinking, but effective for everyday use, whether in business administration or in the most common cases of data analysis.

I do not intend to write an academic article on the statistical subject. If you need an academic approach, you can find it on [Wikipedia](https://en.wikipedia.org/wiki/Harmonic_mean).

## Definitions
### Arithmetic mean
Quotes from [Wikipedia](https://en.wikipedia.org/wiki/Arithmetic_mean):

> ... arithmetic mean, or simply the *mean* or *average*,  is the sum of a collection of numbers divided by the count of numbers in the collection.

> ... consider the monthly salary of 10 employees of a firm: 2500, 2700, 2400, 2300, 2550, 2650, 2750, 2450, 2600, 2400. The arithmetic mean is

> <img src="https://wikimedia.org/api/rest_v1/media/math/render/svg/011f2bc6eee24c97e784cc28aa7d9581ca564ee9" class="mwe-math-fallback-image-inline" aria-hidden="true" style="vertical-align: -1.838ex; width:81.293ex; height:5.176ex;" alt="{\frac {2500+2700+2400+2300+2550+2650+2750+2450+2600+2400}{10}}=2530.">

### Harmonic Mean
Quotes from [Wikipedia](https://en.wikipedia.org/wiki/Harmonic_mean):

> The harmonic mean can be expressed as the reciprocal of the arithmetic mean of the reciprocals of the given set of observations. As a simple example, the harmonic mean of 1, 4, and 4 is

> <img src="https://wikimedia.org/api/rest_v1/media/math/render/svg/eca5906ddf61080e790c0d4df33f47e12da7d019" class="mwe-math-fallback-image-inline" aria-hidden="true" style="vertical-align: -3.338ex; width:49.548ex; height:7.676ex;" alt="{\displaystyle \left({\frac {1^{-1}+4^{-1}+4^{-1}}{3}}\right)^{-1}={\frac {3}{{\frac {1}{1}}+{\frac {1}{4}}+{\frac {1}{4}}}}={\frac {3}{1.5}}=2\,.}">

## Case: $ per invoice
Consider an enterprise that have three clients:

| Client | Revenue | # invoices | $ / invoice |
| :----: | ------: | ---------: | ----------: |
| A      | 12.500  | 25         | 500         |
| B      | 28.000  | 35         | 800         |
| C      | 8.000   | 40         | 200         |

How to calculate the global average of '$ / invoice' using the mean of the individuals '$ / invoice' ratios.

You could certainly compute the global average by dividing the sums of both revenue and invoices quantity. But the goal here is to demonstrate how to achieve that same result by averaging individual ratios.

Well, let's do that (first, the wrong way).

### Calculate '$ / invoice' (the wrong way)
Since you have a series of ratios and your goal is to calculate the average ratio, you may think that you can simply calculate a simple average of the ratios. But this is not true, since the revenue is different for each ratio. Then you can think about weighing each ratio by its revenue.

Let's do this:

| Client | Revenue | weight | $ / invoice |
| :----: | ------: | -----: | ----------: |
| A      | 12.500  | 25.8%  | 500         |
| B      | 28.000  | 57.7%  | 800         |
| C      | 8.000   | 16.5%  | 200         |
| Total  | 48.500  | 100.0% |

Now it's easy!

<img src="https://latex.codecogs.com/png.latex?\bg_white&space;\large&space;0.258\cdot500&space;&plus;&space;0.577\cdot800&space;&plus;&space;0.165\cdot200=623,71" title="\large 0.258\cdot500 + 0.577\cdot800 + 0.165\cdot200=623,71" />

**Wrong!**

### Right way #1: Weighted Harmonic Mean
In the previous item, we saw a common mistake: using the arithmetic mean instead of the harmonic mean.

This is because if you are weighting the average per *revenue*, and *revenue* is in the ratio's **numerator**, you **must** use the **harmonic** mean.

That said:

<img src="https://latex.codecogs.com/png.latex?\bg_white&space;\large&space;\frac{1}{0.258\cdot\frac{1}{500}&plus;0.577\cdot\frac{1}{800}&plus;0.165\cdot\frac{1}{200}&space;}=&space;485" title="\large \frac{1}{0.258\cdot\frac{1}{500}+0.577\cdot\frac{1}{800}+0.165\cdot\frac{1}{200} }= 485" />