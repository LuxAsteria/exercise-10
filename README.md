# exercise-10
***
###Abstract

Here in this assignment, I'm going to investigate the problem about the motion of celestial planets. As is known to all, the motion is induced, or dominated, mostly by the gravity. According to Newtown's law, it's easy to get the odeint formula of the movement. Based on it, we can write the programme which simulates the motion in 2d space, and then I'll gain insights into 3d motion, which takes the angle between the ecliptic plane and the equatorial plane.
***

###Background

####Problem 4.10 
>Calculate the precession of the perihelion of mercury, following the approach described in this section.
####Problem 4.11
>Investigate how the precessioin of the perihelion of a planet's orbit due to general relativity varies as as function of the eccentricity of the orbit. Study the precession of different eclliptical orbits with different eccentricities, but with thesame value of the perihelion. Let the perihilion have the same value as for Mercury, so that you can compare it with the results shown in this section.

***
###Exercise

####Motion Show(visualization)

![img](https://github.com/LuxAsteria/test3/blob/master/orbit%202d.gif)

![img](https://github.com/LuxAsteria/test3/blob/master/orbit3d.gif)

[For code please click here](https://github.com/LuxAsteria/exercise-10/blob/master/code%202)

####Analysis

To study the motion of celestial planet in solar system, we will first peek into Newtown's law of gravitation. The law is expressed as following:

<img src="http://latex.codecogs.com/gif.latex?F_{G}=\frac{GM_{S}M_{m}}{r^{2}}" alt="" title="" />

Here we get G=6.67x10<sup>-11</sup>(constant), and Ms is the mass of sun while Mm is that of the planet of interest, r is the length between 2 planets.
However, if we take the relativity into consideration, we will find the equation needed to be corrected by adding a term to it, and finally we are able to obtain the equation in such form:
<img src="http://latex.codecogs.com/gif.latex?F_{G}\approx\frac{GM_{S}M_{m}}{r^{2}}(1+\frac{\alpha}{r^{2}})" alt="" title="" />
In which the constant alpha is associated with the planet and will change as we calcualting different planets.

Second, let's think about some other factors involved in the simulation--the initial conditions.
Take the orbit of the planet a ecllipse, according to Kepler's laws, it's conspicuously that:
<img src="http://latex.codecogs.com/gif.latex?v\timesr=constant" alt="" title="" />
What's more, based on the knowledge of geometry, the longest distance between planets could be enumerated by the following equation:
<img src="http://latex.codecogs.com/gif.latex?r=e(1+a)" alt="" title="" />
in which e denotes the eccentricity and a represents the length of semimajor axis.

Based on previous illustration, we can then break the force vector into vectors along 3 orthogonal directions--x,y,z.
First, let's start with the simplest one---the 2d motion.

Suppose that the angle between the line linking 2 planets and the x axis is theta, thus:
<img src="http://latex.codecogs.com/gif.latex?F_{x}=F_{G}\timescos(\theta)" alt="" title="" />
<img src="http://latex.codecogs.com/gif.latex?F_{Y}=F_{G}\timessin(\theta)" alt="" title="" />

And if we move further more, consider the 3d situation, suppose the angle between the line and axis z is phi, then we can get:
<img src="http://latex.codecogs.com/gif.latex?F_{Z}=F_{G}\timescos(\phi)" alt="" title="" />
<img src="http://latex.codecogs.com/gif.latex?F_{X}=F_{G}\timessin(\phi)cos(\theta)" alt="" title="" />
<img src="http://latex.codecogs.com/gif.latex?F_{Y}=F_{G}\timessin(\phi)sin(\theta)" alt="" title="" />

####level 1: study the motion with regard to eccentricity and the coefficient alpah
First, the 2d condition
![img](https://github.com/LuxAsteria/test3/blob/master/屏幕快照%202016-11-22%20下午8.49.37.png)
![img](https://github.com/LuxAsteria/test3/blob/ad4668a773d85ed0237b47e66fdf76220462936c/屏幕快照%202016-11-22%20下午8.50.36.png)


[For code please click here](https://github.com/LuxAsteria/exercise-10/blob/master/code%201)

Then, the difference caused by r^d(d is a constant)
![img](https://github.com/LuxAsteria/test3/blob/master/屏幕快照%202016-11-27%20下午7.18.00.png)
![img](https://github.com/LuxAsteria/test3/blob/master/屏幕快照%202016-11-27%20下午7.19.33.png)
![img](https://github.com/LuxAsteria/test3/blob/ad4668a773d85ed0237b47e66fdf76220462936c/屏幕快照%202016-11-27%20下午7.18.09.png)

####level 2: the association between the angle theta when the planet reaches the closest point to the sun.
![img](https://github.com/LuxAsteria/test3/blob/ad4668a773d85ed0237b47e66fdf76220462936c/屏幕快照%202016-11-23%20下午2.41.18.png)

####level 3:the relationship between <img src="http://latex.codecogs.com/gif.latex?\frac{d\theta}{dt}" alt="" title="" /> and <img src="http://latex.codecogs.com/gif.latex?\alpha" alt="" title="" />:
![img](https://github.com/LuxAsteria/test3/blob/master/屏幕快照%202016-11-24%20下午5.48.18.png)

####level 4: the 3d situation:
![img](https://github.com/LuxAsteria/test3/blob/master/orbit%203d.png)

***
###Conclusion
Here in this assignment, we've gained insight into the motion of celestial planets, and we've found that if we take the relativity into consideration, there will be procession of perihilion, and the most apparent one is the motion of Mercury.What's more, the linear relationship between <img src="http://latex.codecogs.com/gif.latex?\frac{d\theta}{dt}" alt="" title="" />and <img src="http://latex.codecogs.com/gif.latex?\alpha" alt="" title="" />, as well as it between the closest point and time.
***
###Acknowledge

[1]Norton's Star Altas and Reference Handbook

##PS:All Rights Reserved
