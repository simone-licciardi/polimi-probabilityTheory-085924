## Bassetti

### Roadmap
- Discrete
- Bounded
- Positive
- General

### Key props
- (Linearity) $E[aX + bY + c] = a E[X] + b E[X] + c$
- (Monotonicity) if $X \leq Y$ then $E[X] \leq E[Y]$
- (Absolute value) $|E[X]| \leq E[|X|]$

### Notes



## Karr

### Roadmap
- Simple
- Positive
- General

### Key props
Fixed points (that is, requirements of output given some inputs. They normalize the results and fix parameters which else we would need to account for): $E[1_A] = P(A)$.

- (Linearity) $E[aX + bY + c] = a E[X] + b E[X] + c$ which includes the costant
- (Monotonicity) if $X \leq Y$ then $E[X] \leq E[Y]$
- (Continuity) if $X_n \to X$ then $E[X_n] \to E[X]$

### Notes

The expectation of discrete rv is not always well defined! Consider the example 4.3 of X-Y = +inf - +inf. This shows why simple rv are more suitable for a definition.