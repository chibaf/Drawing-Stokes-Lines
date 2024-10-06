# Drawing-Stokes-Lines

Drawing Stokes Lines on complex plane

We consider the following ordinary differential equation(*)(**) on the complex plane:

- u''[x] + eta Q[x]u[x]==0,
  
where eta is usually very large number.

Stokes lines start from the turning points "a" that satisfy Q[a]==0.

Stokes lines are 1 dimensional integral curves of the vector field defined by the following form:

Im[Integrate[Sqrt[Q[z]],{z,a,x}]==0.

The directions of lines(=dx) at the turning point "a" are determined by

Im[Integrate[Sqrt[Q[z]],{z,a,a+dx}]==0.

From this equation, by Taylar expansion and omitting higher order terms of dx, we obtain

Im[Sqrt[Q'[a]dx]dx]==0.

Here, in our porgram we suppose Q'[a]!=0 for ease of explanation.

On and after the start point, the next step dx is determined by

Im[Integrate[Sqrt[Q[z]],{z,x,x+dx}]==0.

(*) In the case u''[x]+A[x]u'[x]+B[x]u[x]==0,

Using substitution: phi[x]=Exp[(1/2)Integrate[A[x],x]]u[x],

we have

phi''[x]+(B[x]-A[x]^2/4-A'[x]/2)phi[x]==0.

(**) We consider Q[x] in the domain where Q[x] is a regular function.

Case: Q(x)==x

![stokes01](https://github.com/user-attachments/assets/c96448e4-a152-4657-b8ab-f6f8d48418c9)


Case: Q(x)==x^3+1

![stokes02](https://github.com/user-attachments/assets/42e4fcb2-8971-4e56-bdd3-e52275f4a52b)


Case: Q(x)==-x^2+2

![stokes03](https://github.com/user-attachments/assets/af501797-1021-4266-bf45-32f9777027da)


This code is due to the precept of Prof. T. Aoki (Kinki Univ).

References

"General connection formulae for Liouville-Green approximations in the complex domain", F. E. J. Olver, Phil. Trans. Roy. Soc. London, Ser A, Vol. 289, 1978, pp501--548

