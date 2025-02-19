
##### Turn the limit definition into an actual integral:
- The format is Δx f(x$_i$)
	- Look for the Δx first (which comes in the form (b-a)/n). 
		- This will be multiplied on the outside.
			- Or you might have to extract it out --> always going to be (b-a)/n form. (Note that the n will always be to the 1st power.)
- x$_i$ + a replaces the x of f(x).
	- x$_i$ = (Δx)( i )
	- Where "a" is the lower bound of the integral.
	- Which basically means that it is f(Δx(i)) - Δx is the same as the one on the outside being multiplied - just with an i attached to it.

Update: Simple braindead method:
- Identify bounds, get Δx from (b-a)/n
- Get x$_i$ : a + Δx(k)
- Now plug into sumnation 
	- Δx(f(x$_i$)



![[Pasted image 20240326115138.png]]


---
Working backwards...

To identify the definite integral of a limit definition/summation definition of Riemann.
1. First identify Δx 
	- It is almost always separated from the rest of the junk - at the start or at the end.
2. Identify f(x)
	- which is basically what the Δx is being multiplied to. The junk.
3. Identify your x$_i$ 
	- Since  "x$_i$ + a" replaces the x of f(x), we can deduce what it is.
	- General form of "a" + i(Δx)
4. Identify a
	- a = x$_0$
	- a is what is added to iΔx inside the function.
		- If there is nothing, then a = 0.
5. Identify b
	- b = x$_n$ = a + n(Δx)
	- Will cancel out since Δx is (b-a)/n.
6. Construct your definite integral.