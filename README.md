# Roll 
## Toilet Paper, a difficult choice!
### Intro
One day I was in a shop buying toilet paper. 
That time wasn’t an easy decision. 
A special offer was proposing a set of 3 rolls at a price of 2€. 
At the same time a set of 6 rolls was offerd for 1.5€. 
An naïve estimation can easily drive to the second hypothesis because you have twice the rolls for half of the price…but…
the 3 rolls were much bigger in diameter than the regular rolls. 
In the label of both packages I didn’t find any indication of the length of paper so I was struggling in a dilemma.
When I went home I decided to try to solve it parcticaly
When I went home I decided to try to solve it practically.

### The model
The few equations are written in latex. Before to go into the details I would like to make some assumptions (simplifications):
* The roll is a single strand of paper but could be simplified as $n$ concentric circles where the first is wrapped around a cylinder of diameter $a$, the second around the first and so on.
* Each circle has a thickness $x$.
* The roll is a perfect circular cylinder.

Given these simple assumption the total length of the roll is the summation of the perimeter of the $n$ circles

$$ l= \sum_{i=1}^{n} r^i$$

where $r^i$ is the radius of the circle $i$.

Obviously each radius $r^i$ can be written as $$r^i=r^{i-1}+x$
and the summation can be transcribed as

$$l=2\pi  \big(a+(a+x)+(a+2x)+…+(a+nx)\big)=2\pi\big((n+1)a+x+2x+…+nx\big)=2\pi \Big((n+1)a+x{(n+1)n \over 2}\Big)$$

This is enclosed in this comfortable equation
$$l(a,n,x)=2\pi (n+1)\Big(a+{nx \over 2} 

Three parameters are sufficient to extrapolate the length of the toilet paper:  
the radius of the first cylinder, the total number of layers and the thickness of a layer. 
$n$ is not easy to obtain and is better to express it using a new parameter that is the external diameter of the roll $b$. 

Because $n={b-a\over x}$, the equation becomes

$$ l(a,b,x)=2 \pi \Big({b-a} over x +1 \Big) \Big(a+ {b-a} over 2 \Big)$$

###USAGE
#### Example
A discount sell 10 rolls for 2€ ($a1=2.2$, $b1=4.7$, $x=0.0236$) whereas another 
brand without discount propose 6 rolls for 3€ ($a2=1.6$, $b2=5.8$, $x=0.0236$). 
Which is the best choice?

Do the substitutions in the equation

$$ 10l_1=6.28(2.5/0.0236+1)(2.2+1.25)10=232$$ meters

$$ 6l_2= 6.28(4.2/0.0236+1)(1.6+2.1)6=250$$ meters

The first has a price of $0.8€m^-1$ and the second $1.16€m^-1$ and is convenient.

###The Template
I designed a master (paperModel.pdf) that can be printed and used to measure $a$ and $b$ directly with the roll. On it you can measure the diameters and infer the length using a set of precomputed tables. Different tables correspond to a different number of plies that compose a single layer of paper. The most common toilette papier has 2 plies.
