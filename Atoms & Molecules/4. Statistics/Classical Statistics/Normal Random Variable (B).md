Type: #atom
Atom: [[(Common) Random Variables (Z)]]
Subtopic: Classical Statistics
Topic: Statistics
Status: #inprogress  
Understanding: #Exploratory Intuition

----
# PDF of Normally Distributed Random Variable

Most importantly, the Gaussian density function is $$f(x)=\frac{1}{\sigma\sqrt{2\pi}}e^{-\frac{1}{2}(\frac{x-\mu}{\sigma})^2}$$
To take note, the fraction $\frac{1}{\sigma\sqrt{2\pi}}$ is a normalizing constant to ensure the PDF integrates to 1.

# Integrating the Gaussian PDF to get the CDF

This involves evaluating $Q^2=1$ implying $Q=1$. Full steps here: [Stat Course - Integrating Normal Density](https://www.youtube.com/watch?v=Bjh5Yvml4RM&ab_channel=StatCourses).

## Substitution Step

Substitute $u=\frac{(x-\mu)}{\sigma}$.  And $du=dx/\sigma$ so $dx=\sigma du$. Then, $Q=\int \frac{1}{\sqrt{2\pi}}e^{-\frac{1}{2}u^2} du$. Squaring it: 
$$Q^2=\frac{1}{2\pi}\int\int e^{-\frac{1}{2}(u^2+v^2)}dudv$$
This came from writing out the RHS of $Q$, changing one of the $u \mapsto v$, rearranging the integral signs.

## Change of Variables Step - Polar Coordinates

Now, we need to change $u$ and $v$ from cartesian to a polar coordinate system - $u=r\cos\theta$ and $v=r\sin\theta$. Then, we rewrite $Q^2$ with a change of variables transformation (including the Jacobian determinant so $dudv=|J|drd\theta$) and the limits of both integrals ($\theta$ and $r$).





