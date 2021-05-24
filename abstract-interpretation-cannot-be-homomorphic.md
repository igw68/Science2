# Abstract interpretation cannot be homomorphic

Very seldom we have enough information in abstract interpretation to make it
homomorphic (abstract operations reflect exactly the real ones). 

Consider for example sign abstraction for arithmetic operations. Even though we know the
signs of $x$ and $y$, we do not know the sign of $x+y$. 

This is why we have normally partial-order $\sleq$ on the domain. The order says
how good is approximation.