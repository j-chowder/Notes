
U-sub is a method for [[Integration]] that basically reverses the [[Chain Rule]] for derivatives. 
- Needing to do [[Product Rule]] or [[Quotient Rule]] often means that you will use U-sub.

---
You can use U-sub on 
- complex bases
- the entire term
- complex angle (of trig)
![[Pasted image 20240111194839.png]]

--- 
When doing U-sub, we need to turn the entire integrand into variables of u, so you can either scoop up everything else with "du," or substitute x in relation to u.
- du is pretty straightforward, try to foresee what "u" can differentiate into the rest of the terms in the integrand during "du"
![[Pasted image 20240111195113.png]]
---
###### Substituting x w/ relation to u

When to do it:
- Need to u-sub, (base is complex, angle is complex, etc.)
	- Make sure to check if it is proper first -> ([[Proper and Improper Fractions]])
- du can not scoop up everything bc. there is a variable that, unlike coefficients, can not be added in by tinkering with du.

How to do it:
- obtain your u.  (u = x + b)
- then, isolate x in that equation: (x = u - b)
- You can substitute that directly into the normal integrand with full u-substitution.
- Will often need to simplify the integrand by breaking up the fraction and splitting into different integrals.

--- 
##### Special case of substituting/du

- **often used when there is a variable inside radical 
- Same start, but instead of instantly differentiating the "u," you cancel out the radical of the variable and completely isolate it in on one side of the equation. 
- Then you differentiate into du/dx.
- the x becomes 1, you multiply dx to the other side. 
- Thus, you are able to make an otherwise much more messy and complex u-sub procedure to something more clean and easy to work with.

![[Pasted image 20240111195955.png]]
![[Pasted image 20240111200616.png]]
Note that for the second example that 
1. We did this special technique because of variables in nasty radicals
2. Utilized **both** x-substitution and special du to completely revamp the integrand to only relate to the variable u.
	1. Remember than when using u-sub, everything has to be in regards to u in order for you it to work.


--- 
###### U-sub with Definite Integrals

When u-subbing with a definite integral, (has an interval) you will need to:
1. Change the interval to u as well by plugging in the numbers into the (u = x + b) formula as x. Those are your new lower and upper bounds.
2. When plugging in to solve the actual upper bound - lower bound, keep the terms as u and just sub the uppers, lowers, in.
3. Keep the upper and lower bounds in the same place even if their values change to the point where the lower is actually greater than the upper.

![[Pasted image 20240111194530.png]]