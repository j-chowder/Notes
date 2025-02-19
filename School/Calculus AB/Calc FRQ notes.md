
##### Concept of finding f(a) from a graph of f'(x) given f(b) 
- Use f(b) as a frame of reference.
- Since you can not calculate f(a) from a graph of f'(x) without knowing f(x),
	- We ADD f(b) + the ∫f'(x) with the intervals of b to a.
	- In doing so, we add the change of positions from a -> b (integral) with our point of reference f(b) to get the actual positions of f(a)

**![](https://lh7-us.googleusercontent.com/DmYrN8a62LOJEp2XeDCSSu3BY9XaweZk-IuPJqr55UQGh8aGrJadIDlSLYxxU0KBGiY5EMvSZdGo7IxXBT4HSRovOAnf050qDtAdEHdLB_RIwcnb_ICAWgDxYIqaT_rRkAENQciQZmCQLCEyr2NPHIk)**
- f(-2) is given, need to find f(-6) so add f(-2) with the integral of f'(x) from -2 to -6.
- f(-2) is given, need to find f(5), so add f(-2) with the integral of f'(x) from -2 to 5.


---
##### Rate in-Rate out 

- Know three key things
	- Identify the rate in
		- pumped into, enter(s), adds, sells for, accumulate, arrive(s), flows into.
		- Think: if nothing else happens, there will be more because of this rate.
	- Identify the rate out
		- leaks, leave, removed, removes, costs, pumped out, get off/exit a line, process, drains.
	- Initial amount
	- **Pay attention to the interval on which the rate applies.** 
- What you'll be asked to do
	- Find the total amount that comes in/goes out on the interval.
		- Total amount in - so just integrate f(rate in).
	- Write a function that gives total at the time "t".
		- A(0) = start, rate in: f(t), rate out: g(t)
		- A(t) = start + (integral from 0 -> t (f(u) - g(u))
			- total = what you started with + rate in - rate out.
	- Find total at a specific time, t = b.
		- Evaluate A(b) = start + (integral from 0 -> b (f(u) - g(u)))
	- Determine if the total is increasing/decreasing at a time or on an interval
		- 2nd Fundamental Theorem of Calculus
			- A'(t) = In - Out
				- A' > 0, A(t) is increasing
				- A' < 0, A(t) is decreasing
					- Think of it like: if rate in > rate out, then ofc increasing.
					- Likewise, if rate out > rate in, then ofc decreasing.
	- Determine the absolute max/min on an interval
		- define total function, test the critical points and {a, b}
	- If you only need the time (and there is only one critical point) and at the crit. pt. you get a rel. max, then that's the abs. max.
		- Because there is no way to get higher. This is the only place where it turns.
	- Determine what happens after one of the rates turns off.
		- i.e. When will there be nothing if the rate in is turned off
		- When will you pass some amount if the rate off is turned off.
	- Interpret the meaning of something in context.
		- can be derivative 
		- can be an integral
	- Determine if the rate of change is increasing or decreasing
		- So basically the rate of the rate.
		- Take the derivatives at t = x of (rate in) - (rate out). 
			- If > 0, increasing, < 0, decreasing.



