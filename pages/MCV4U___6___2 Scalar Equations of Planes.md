- #+BEGIN_WARNING
  In this lesson our **goal** is to describe a plane with a scalar equation, i.e. an equation without vectors.
  #+END_WARNING
- ## Recall #.v-self-border
	- Given the scalar equation in 2D for a line, what is the normal vector?
		- Use $Ax+By+C=0$ or, #eg $3x-5y-1=0$.
			- **Recall:**
			  collapsed:: true
				- A normal is a vector that is perpendicular to the direction of the line.
				- Given $Ax+By+C=0$ we can get the normal vector by reading off $A$ and $B$. I.e. the normal vector is $\begin{bmatrix}A\\ B\end{bmatrix}$.
				- In the example above, a normal vector is $\begin{bmatrix}3\\ -5\end{bmatrix}$
- ## Lesson #.v-self-border
	- The scalar equation of a plane is similar to the one for a line, but has an extra parameter:
		- $$Ax+By+Cz+D=0$$
		- Where $\begin{bmatrix}A\\ B\\ C\end{bmatrix}$ is a normal vector to the plane depicted as $n$ in the diagram below where $S$ and $R$ are direction vectors in the plane.
		- ![image.png](../assets/image_1748445121689_0.png)
		- Note that our idea that a normal vector is perpendicular to the direction(s) still holds true. Our $n$ is perpendicular to **both** $S$ and $R$.
		- Try using Desmos 3D to plot the scalar equation:  $3x-2y+z-4=0$.
		  collapsed:: true
			- <iframe src="https://www.desmos.com/3d" style="height: 500px; width: 100%;"></iframe>
- ## Action #.v-self-border
	- Examples
	  logseq.order-list-type:: number
		- Find the scalar equation of the plane, $t,k\in\R$:
		  logseq.order-list-type:: number
		  $$\begin{bmatrix}x\\ y\\ z\end{bmatrix}=\begin{bmatrix}1\\ 2\\ 3\end{bmatrix}+t\begin{bmatrix}-2\\ 4\\ 6\end{bmatrix}+k\begin{bmatrix}1\\ 3\\ -4\end{bmatrix}$$
			- **Strategy:**
			  logseq.order-list-type:: number
			  collapsed:: true
				- We need a vector perpendicular to both direction vectors. We need the **cross product**!
				  logseq.order-list-type:: number
				  collapsed:: true
					- logseq.order-list-type:: number
					  $$\begin{matrix}\cancel{-2} & 4 & 6 & -2 & 4 & \cancel{6}\\ \cancel{1} & 3 & -4 & 1 & 3 & \cancel{-4}\end{matrix}$$
					- So then
					  logseq.order-list-type:: number
					  $$\begin{align*}&\begin{bmatrix}
					  4\left(-4\right)-3\left(6\right)\\ 6\left(1\right)-\left(-2\right)\left(-4\right)\\ -2\left(3\right)-4\left(1\right)
					  \end{bmatrix} \\
					  &= \begin{bmatrix}
					  -34 \\ -2 \\ -10
					  \end{bmatrix} \\
					  &= -\frac12 \begin{bmatrix}
					  17 \\ 1 \\ 5
					  \end{bmatrix}
					  \end{align*}$$
					- And we'll let $\vec{n}=\begin{bmatrix}17\\ 1\\ 5\end{bmatrix}$
					  logseq.order-list-type:: number
				- Therefore the scalar equation is (so far):
				  logseq.order-list-type:: number
				  collapsed:: true
					- $16x-7y+5+D=0$
					  logseq.order-list-type:: number
				- Substituting $(1,2,3)$ to solve for $D$:
				  logseq.order-list-type:: number
				  collapsed:: true
					- $17(1)+1(2)+5(3)=-D$
					  logseq.order-list-type:: number
					- logseq.order-list-type:: number
					  $$\begin{align*}17+2 +15&= -D \\ 17+17 &= \\ 34 &=-D\end{align*}$$
					- Therefore, $D=-34$
					  logseq.order-list-type:: number
				- Therefore, the scalar equation is $17x+y+5z-34=0$
				  logseq.order-list-type:: number
		- Show that the point represented by $t=4$ and $k=-3$ is in fact also on the scalar equation you found. You can also check this using Desmos 3D.
		  logseq.order-list-type:: number
			- **Strategy:**
			  logseq.order-list-type:: number
			  collapsed:: true
				- Get the point defined by $t=4$ and $k=-3$.
				  logseq.order-list-type:: number
				  collapsed:: true
					- logseq.order-list-type:: number
					  $$\begin{align*}
					  \begin{bmatrix}x\\ y\\ z\end{bmatrix}&=\begin{bmatrix}1\\ 2\\ 3\end{bmatrix}+4\begin{bmatrix}-2\\ 4\\ 6\end{bmatrix}-3\begin{bmatrix}1\\ 3\\ -4\end{bmatrix} \\
					  &= \begin{bmatrix}
					  1 -8 -3 \\ 2 + 16 -9 \\ 3 + 24 +12
					  \end{bmatrix} \\
					  &= \begin{bmatrix}
					  -10 \\  9 \\ 39
					  \end{bmatrix}
					  \end{align*}$$
				- Checking $(-10,9,39)$ on $16x+y+5z-34=0$
				  logseq.order-list-type:: number
				  collapsed:: true
					- logseq.order-list-type:: number
					  $$\begin{align*}
					  0 &\stackrel{?}{=} 17(-10) +(9) + 5(39) -34 \\
					  &= -170 +9 + 195 -34 \\
					  &=0
					  \end{align*}$$
	- Find the scalar equation of the plane that contains the points $(1,4,5)$ and $(3, 2, 1)$ and is perpendicular to $2x-y+z-10=0$.
	  logseq.order-list-type:: number
		- **Strategy:**
		  logseq.order-list-type:: number
		  collapsed:: true
			- Unlike in 2D, for vectors in 3D we need two vectors to find a ==[[perpendicular]]== third vector by using the cross product. Where do our two vectors come from in this problem?
			  logseq.order-list-type:: number
			- One is the normal vector of $2x-y+z-10=0$ which serves as one of our new plane's direction vectors.
			  logseq.order-list-type:: number
			- A second is the vector $\vec{AB}$ given we set $A=(1,4,5)$ and $B=(3,2,1)$.
			  logseq.order-list-type:: number
			  collapsed:: true
				- logseq.order-list-type:: number
				  $$\begin{align*}
				  \vec{AB} &= (3,2,1)-(1,4,5) \\
				  &= (2,-2,-4)
				  \end{align*}$$
				- So $(2,-2,-4)$ is our second direction vector for our new plane.
				  logseq.order-list-type:: number
			- To get the scalar equation for our new plane, we need a normal vector for the plane, which can be found using the cross product.
			  logseq.order-list-type:: number
			  collapsed:: true
				- logseq.order-list-type:: number
				  $$\begin{matrix}\cancel{2} & -1 & 1 & 2 & -1 & \cancel{1}\\ 
				  \cancel{2} & -2 & -4 & 2 & -2 & \cancel{-4}\end{matrix}$$
				- $\begin{bmatrix}-1\left(-4\right)-\left(1\right)\left(-2\right)\\ 1\left(2\right)-\left(2\right)\left(-4\right)\\ 2\left(-2\right)-\left(-1\right)\left(2\right)\end{bmatrix}=\begin{bmatrix}6\\ -6\\ -2\end{bmatrix}$
				  logseq.order-list-type:: number
				- We'll use $\vec{n}=(3,-3,-1)$ for simplicity.
				  logseq.order-list-type:: number
			- Our scalar equation is currently $3x-3y-z+D=0$. We know $(3,2,1)$ is a point on the plane. Let's substitute to solve for $D$.
			  logseq.order-list-type:: number
			  collapsed:: true
				- $D=-(3(3)-3(2)-1)=-(9-6-1)=-2$
				  logseq.order-list-type:: number
			- Therefore our Scalar Equation is $3x-3y-z-2=0$.
			  logseq.order-list-type:: number
- ## Consolidation #.v-self-border
	- What information is needed to create a scalar equation of a plane?
	- What are the steps to use a vector equation of a plane to get the scalar equation?
	- Add this information to your toolbox:
		- Scalar Equation of a Plane:  $Ax+By+Cz+D=0$
		- $(A,B,C)$ is a ==[[normal]]== vector to the plane.
- ## Practice
	- For the plane $x-7y-18z=0$:
	  logseq.order-list-type:: number
		- What is the normal vector?
		  logseq.order-list-type:: number
		- Does this plane pass through the origin?
		  logseq.order-list-type:: number
		- Find the coordinates of any three points on the plane.
		  logseq.order-list-type:: number
	- Find the scalar equation of the plane that passes through $(1,2,3)$ and has $\vec{n}=(2,-5,7)$.
	  logseq.order-list-type:: number
	- Find the scalar equation of the plane containing the points $A(-2,3,1)$, $B(3,4,5)$, and $C(1,1,0)$.
	  logseq.order-list-type:: number
	- The line $(x,y,z) = (2,0,1)+t(-4,5,5)$ for $t\in\R$ lies on a plane that contains the point $(1,3,0)$. Find the scalar equation of this plane.
	  logseq.order-list-type:: number
	- Determine the scalar equation of the plane passing through $(1,4,5)$ and $(3,2,1)$ and is perpendicular to the plane $2x-y+z-1=0$.
	  logseq.order-list-type:: number
	  collapsed:: true
		- ![image.png](../assets/image_1748457342973_0.png)
		  logseq.order-list-type:: number