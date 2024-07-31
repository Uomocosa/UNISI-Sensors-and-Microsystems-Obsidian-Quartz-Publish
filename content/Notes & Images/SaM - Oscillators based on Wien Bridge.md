##### ***Remeber***:

> Circuit:<br>![[Pasted image 20230719114922.png|500]]
> - ***Feedback coefficient***:$$\beta = - \frac{j\omega\alpha}{1- \omega^2 \alpha^2 + 3j\omega\alpha}$$Where: $\alpha = RC$
> - If we enforce $1-\omega^2\alpha^2 = 0$, we will have that $\beta A$ is a real negative number, so we will have the [[SaM - Barkhausen Conditions|second Barkhausen condition]] already satisfied.
> - Finally if we take:$${R_2 \over R_1} \ge 2 $$We will have also: $\beta(\omega) \le - {1 \over 3}$, and consequently: $|\beta(\omega) \cdot A(\omega)| \ge 1$<br>And with that all the **Barkhause conditions** are satisfied, and the system will oscillate.


> Another way of seeing things:
> $A \triangleq {\large{V_o \over V_i}} = 1 + {\large{R_2 \over R_1}}$
> $\beta = -{\large{Z_1 \over Z_1+Z_2}}$
> Then we apply the [[SaM - Barkhausen Conditions|Barkhausen conditions]], so that our oscillator does in fact oscillates, and we find:
> 	- $\omega_0 = {1\over \alpha}$, where: $\alpha = RC$.
> 	- $\beta(\omega_0) = {1 \over 3}$
> 	- $R_2 = 2R_1$.

> - We drow the plot:<br>![[Pasted image 20230719114947.png|500]]
> - Oscillators based on Wien Bridge have a constant slope around $\omega_0$:$$\left.{d\varphi(\beta) \over d\omega}\right|_{\omega = \omega_0} = {2 \over 3}$$

> We have also seen another variation of an oscillators based on the Wien Bridge:<br>![[Pasted image 20230719115000 1.png|500]]
> - This kind of circuit ensures to reduce the distortion due to an unstable behavior of the circuit.
> - Here are some circuits comparisons:
> 	- [Circuit Comparison I (both unstable)](https://www.falstad.com/circuit/circuitjs.html?ctz=CQAgjCAMB0l3BWEAWAnNAbADgOwCZlk4NUxUtIkFIQqaEBTAWjDACgAnEPBDcDGmEL8a9OGwDu3XiOl9UfSGwCGc8Dj4BmbOr5ZwSFkjDx4IFtAV5skHKhyQBeLBj4Wr2MDhxYijrAjI4KbwnGoKINr6ETR4oVJRIBGJXoqSkTqpKGB8WUoJmRoZ+jxpAMZqpZGQQVWisKaoTc0trajmGNBEds5gCDjIYL5geAZhmjVqiXXB4lJVCzITQfngwjk0FLJKAOYgWxv7sVj6omwVeATVtVeavlBQDfBtL83mYJYY1lhePn7YgSgYWc+mW3BOkXugni3FukyqYNWCPhEMR6UuQTutSWUPRqPuCNx8xx2L4fiBeyq5KpOQeSJkZFGizSAAdsrkioM+Ai6Ww9ly1AK8PheXtfCUZOLuCKzmypVkpTyzlIKDRkPpVUk0lJsPp1SBdVqgVxDfqcNoUKdZqEAF5HNX6DR6kogAAmDAAZsoAK4AGwALkwbQwAHYMDhsO3msmOnT60bur1+wPBsMRnUQxkGiF1PnZvVwfPs3kZ0H3U2F1b4GhYou11YYEl1ol1ybV65AnVLSaGtFcdtggdQ63nA3doKNrTDmAhV6vDrQTRkQiaNDC1zIHAU2gjWQIXcgku0IqHfejQ4NnMyXuTJT9i1VTUzEziCqGqrRtT1WdztqPUjIHE+6aLwkDaA4QR9OkmoKoWuYqoWCr6nk0GFhEMFFHeRboWhijcKEqiGrBghFPofTvMYIQ0EwmiwAQFCaN45DRk4C5LqgK5rhoGCbtapjpERAjYWkJqZkJ-S5EJYhKAAblqsQigoJF4RAIzQDwBh0o8CBsAA9twEA8Q8RDkPhjwQGq3ArDuDz7pEbBAA) 
> 	- [Circuit Comparison II (both stable)](https://www.falstad.com/circuit/circuitjs.html?ctz=CQAgjCAMB0l3BWEAWA7NAbAgnMgHJBpMgEzIaokgKTXW0ICmAtGGAFABOIJCG4RcMmQDatMPHYB3Hn1Gz+2fpHYBDBeFT8AzBjyb++sElZIJ8OCGbJo2VJW27sebSW148Ea7ftuEYbDBkbG1sQPALSW5eRR09ECUoHkkZXX1EtIMoaRBMsC0UMH585Ry8gsyY7IBjDSrtYg0xWAswtvaOsJRofAxsSCLsBF581HAELlzG+viq8RS6uXrGlRkgkSLaAnkVAHMQbc2D2hIPJJVakjIpkSuRdxFmyM6XtqsbOwd-QODQ8JVomcGrcgXhHhE4Dk7jcNMDsjJliD9HDVjxrg9YWD4TxQbc5BjUfUsVVkJY9hpSSc5MgiucoXIAlQqnN2AAHQrFAo0-j1On7bkU2kkSh8g74DRg-TCqhiNliowFSWwukyAi0cVqhKlGR6fTi3Va7LcA3i1C6FD6eYWdgAL2O6v0Wj1UpAABNGAAzVQAVwANgAXZg2xgAO0YnFtIDN-FN8XFVHdXr9geDYYjOrOjJABpZ+xNlhNtNlGeRWPzxajJFoGINBJyWB0Zdx2NrjUo1ZW9fxjVbj0m7ZhA4JEIu2e7IgbuSxT1arxeVgQsAwoUgCAQugQeCGnmy+38VCO+5xluxCAKh7AB8EqJzcl7Rqj5qqmrmI-YtVv-GjTSgLXgc-nGwaC0PRkBoZdgnFYwck1Ep7SaGDLDgpU4NRTVElggoAWzM4MMsRITkkdQDWQpDFXGKxjBHeB3lsXAsE8M1IBIIZUC8RdCBXNcNy3TcIHMSJ60zQQDQIyYSMEM9imvBJ+nYAA3CEpQZOAjBk-jFyGCixF-CYAHseAgDBwVJZxkl-CB1R4cF-CSWztHYIA) 
> 	- [Circuit Comparison III (one unstable and one stable)](https://www.falstad.com/circuit/circuitjs.html?ctz=CQAgjCAMB0l3BWEAWAnNAbADgOwCZlk4NUxUtIkFIQqaEBTAWjDACgAnEPBDcDGmEL8aNVNTYB3brxEy+qPpDYBDeeBx8AzNg18s4JCyRh48FNCxbKYHAhxbHlcrWitrCVI9R4MYLTgGpmZwnOqKIDoGETR48FKRuhFRelAJKbZ8yGB8mWnSGZqJBjxKbADG6qWRkMjqorBmqM0trW2oIEx4lqw5yFhY-mS4AYZh1nXVKdWC8dLVC7IT+eDCOTQUcsoA5iCb63uxA1BplXgENZMXWlh1DSHtjy2u7s7evv6BaVx4x8u-Bhud3Ac2411q6mWynmSwhAMuK3OdSBkNuiL+aKmaOhqMmsiIojYu2qBPU2SUiNkZDwVVkygADigcqlyZCTjsmXwScy8Ph2US9v11LcSnzCYyRalJVN+dIKDQhfKQDEEtgDEK1cqylxNUKHFkDII4qEAF6HBUGTTqkogAAmDAAZioAK4AGwALkwTQwAHYMDhsM36lCW3RCmn2p1uz3ev0B6Sa6kgTUzAW6uDJ46swkJjF1dM5kD4GgozUonEYJZosvY1V-CHFhEV2H5+t3MKN5ad7Eg0KVSvaCEDyI9mAPJ6PVyQVCQHTILSeAR4MhaNK7BBgGkHDc0+GF+y5AS0TdbOslWRliHKLjB6pKma95T947VW90qCNeATydMBCwKy1LyvxgAgWjIEUIEJEqeT3nSUEZjBQp5DiSoRNBRTXpm0T6BmMTcPEaiJkU6H6IYnQgY+5h-rU2AIP0kBWGBODZFOM5zguiiQMuXiUaCiZHpqKo6sc24QUeYgSAAblqsR8pxqSCOA3Q8GRogfggbAAPbcBAGDAkQLhxB+EAKtwwIbicFlaGwQA) 
> - Remeber that:
> 	- If we take $|A \beta| = 1$ the output will be a sinisuidal function.
> 	- Instead for $|A \beta| > 1$ the output will diverge. (this is the "**unstable behaviour**" we refer to)

---
###### Memory Card
![[Samsung_SaM_Notes_24_240516_113108_1.jpg]]

---
I will show you two different kind of oscillators, sine wave oscillators, one, which is meant for low frequency and the other one, instead, which is suitable for high frequency applications
![[Pasted image 20230719114922.png]]
- **NOTE**: To find $A$ we need first to detach the positive feedback loop.
- [Circuit](https://www.falstad.com/circuit/circuitjs.html?ctz=CQAgjCAMB0l3BWECAstIIEwDZsHZNJ8MAOZSZc5AUwFowwAoAJxEwW3GwrBRS4o94jAO5sOA8ZwCcnSIwCGU8Hk4BmbGTCqQWpPSRh48cNASQUYDnjVqwa6QiucwZi1bxgSKNSWwI1APBjYVZ2GXVNEFkoNmExDTIYxJU5URAU7U5LFx15BKisjKjwqEYAY2VStQtlQXR4aSbmltbpEFpMaBJMTC8-BgIwQk5MFgza6pKJITh00oWJGv588D5JEh5uMoBzXS2KTbYSMkEKtkx+ZYur71iYELan5tNzSwRPb19-QLUysJOE34mEBvhWwTmYl6V0mS1qq2qk1B8Pmlwyd2qdwRoIxSyx8zxwIkKDgu2UJIopRy90YAAcQNSitTqjSoRIwNJMFUZow9sziWBRgQaQB7OIgbDgknSLT1CA8RhAA) <br>![[circuit-20230922-1810.png]]<br>**NOTE**:
	- In this circuit **there is no** $V_i$, this is an **ideal oscillator**, so it is designed to relay on no exitation (exept the power given to the amplifier by $\pm V_{DC}$)
	- The "initial power", that makes the ciruit work is stored in one of the capacitors, i've set $V_{C_1}(0) = 2V$ and $V_{C_2}(0) = 0V$.
	- In reality a DC voltage exatation is needed, at first to start the circuit and then we'll need to mantain it (small exatation need at the input), since some power will be lost for non-ideality reasons.

![[Pasted image 20230719114929.png]]
- ***Online Source***: [Youtube](https://www.youtube.com/watch?v=gbUXbaxvX94)
- We define our **positive feedback coefficient** as $\beta$.
- In this case we also have an **arbitrary negtive feedback coefficient**: $A = 1+\frac{R_2}{R_1}$.<br>I call it arbitrary beacause usually it is defiened as just the gain of the amplifier $A_0$.
- So as it stands the only way for the circuit to oscillate is that $\beta(\omega_0) > 1+\frac{R_2}{R_1}$
- Also remember that we need the product $\beta A$ to be a **real negative number**, such that $\angle \beta A = 180°$.

So we have found (in the note the $-$ sign disappears at the end): $$\beta = - \frac{j\omega\alpha}{1- \omega^2 \alpha^2 + 3j\omega\alpha}$$Where:
- $\alpha = RC$.

Remember the "feedback loop formula" is:$$V_0 = \frac{A}{1+\beta A}V_i$$Starting from this formula we have seen the two Barkhausen conditions:
1. $\angle \beta A = 180°$
2. $|\beta A| \geq 1$


 So if we enforce $1-\omega^2\alpha^2 = 0$, we will have that $\beta A$ is a real negative number, so:
![[Pasted image 20230719114938.png]]
- Now we need the positive feedback loop coefficient $\beta$ to be greater than the negative feedback loop, so the positive feedback loop is: $A = 1+\frac{R_2}{R_1}$, and we must meet the condition: $\beta \geq A$.<br>**NOTE** this is equivalent to the second "***Barkhausen condition***":$$|\beta(\omega_0) A(\omega_0)| \geq 1$$
- [Positive Feed Back Loop Example](https://www.falstad.com/circuit/circuitjs.html?ctz=CQAgjCAMB0l3BWcMBMcUHYMGZIA4UA2ATmIxAUgoqoQFMBaMMAKAHcQUFDxCquexHpHYhshPCCFiJ4DMNHjJYeSAAscOQoBuWzijV6wfKKY3Uql6AhYBzPSgMPzllgENO3PUr3FwSJiQweHhTIJCRewFwYhRPHgNLKFFo4yoVHjTkgCd4qR4faXT4FgB7ThBCQyoNUk4rELJCbi5TOLjsFiA) <br>![[circuit-20230922-1306.png]]
- [Positive Feed Back Loop Example (2)](https://www.falstad.com/circuit/circuitjs.html?ctz=CQAgjCAMB0l3BWcMBMcUHYMGZIA4UA2ATmIxAUgoqoQFMBaMMAKAHcQUFDxCquexHpHYhshPCCFiJ4DMNHjJYeSAAscOQoBuWzijV6wfKKY3Uql6AhYBzPSgMPzlu527hiKdzwOWoogK8VCo8xq4ATj5SPEoxpmDwLACG0aEyyqrKSExIifCaSCEFIgD2nCCEhlQapJxWBWSE3Fym3t7YLEA) <br>![[circuit-20230922-1308.png]]
- Notice how the sign of the AO changes the sign of the oputput, but it does not mean that the feedback loop at the $+$ is a positive feedback loop and the one at the $-$ is a negative one, however oftein it is actually like this, but just thanks to the construction of the loop.
- [Open Loop AO](https://www.falstad.com/circuit/circuitjs.html?ctz=CQAgjCAMB0l3BWcMBMcUHYMGZIA4UA2ATmIxAUgoqoQFMBaMMAKAEMQ8xCQU88QxPr36dwSJkjDx41KtJksAbiAxoQ2BClXrM2qlQAstKKZgIWAdx1U9nbrzVQWAcxsat77IQEHX9nlxDAI0fM38EQiogiijQ32c3Q0JgzW1k1LC-awzHbUjbJ0hlEFy00pS8s1KTAyhoCw4CkQFCSJbBcRBJZBk6qT6WIA) <br>![[circuit-20230922-1315.png]]

So we have found:
1. $\omega_0 = \frac{1}{RC}$
2. $1 + \frac{R_2}{R_1} = 3$

We draw the plot:<br>![[Pasted image 20230719114947.png]]

![[Pasted image 20230719114952.png]]
- We analize the "inclination/slope" of the phase of $\beta$ at $\omega = \omega_0$, and we obtain this value #NOT_SURE_ABOUT_THIS 

![[Pasted image 20230719115000.png]]
- If we take $|A \beta| = 1$ the output will be a sinisuidal function.
- Instead for $|A \beta| > 1$ the output will diverge.
- This kind of circuit ensures to reduce the distortion due to an unstable behavior of the circuit.
- Here are some circuits comparisons:
	- [Circuit Comparison I (both unstable)](https://www.falstad.com/circuit/circuitjs.html?ctz=CQAgjCAMB0l3BWEAWAnNAbADgOwCZlk4NUxUtIkFIQqaEBTAWjDACgAnEPBDcDGmEL8a9OGwDu3XiOl9UfSGwCGc8Dj4BmbOr5ZwSFkjDx4IFtAV5skHKhyQBeLBj4Wr2MDhxYijrAjI4KbwnGoKINr6ETR4oVJRIBGJXoqSkTqpKGB8WUoJmRoZ+jxpAMZqpZGQQVWisKaoTc0trajmGNBEds5gCDjIYL5geAZhmjVqiXXB4lJVCzITQfngwjk0FLJKAOYgWxv7sVj6omwVeATVtVeavlBQDfBtL83mYJYY1lhePn7YgSgYWc+mW3BOkXugni3FukyqYNWCPhEMR6UuQTutSWUPRqPuCNx8xx2L4fiBeyq5KpOQeSJkZFGizSAAdsrkioM+Ai6Ww9ly1AK8PheXtfCUZOLuCKzmypVkpTyzlIKDRkPpVUk0lJsPp1SBdVqgVxDfqcNoUKdZqEAF5HNX6DR6kogAAmDAAZsoAK4AGwALkwbQwAHYMDhsO3msmOnT60bur1+wPBsMRnUQxkGiF1PnZvVwfPs3kZ0H3U2F1b4GhYou11YYEl1ol1ybV65AnVLSaGtFcdtggdQ63nA3doKNrTDmAhV6vDrQTRkQiaNDC1zIHAU2gjWQIXcgku0IqHfejQ4NnMyXuTJT9i1VTUzEziCqGqrRtT1WdztqPUjIHE+6aLwkDaA4QR9OkmoKoWuYqoWCr6nk0GFhEMFFHeRboWhijcKEqiGrBghFPofTvMYIQ0EwmiwAQFCaN45DRk4C5LqgK5rhoGCbtapjpERAjYWkJqZkJ-S5EJYhKAAblqsQigoJF4RAIzQDwBh0o8CBsAA9twEA8Q8RDkPhjwQGq3ArDuDz7pEbBAA) 
	- [Circuit Comparison II (both stable)](https://www.falstad.com/circuit/circuitjs.html?ctz=CQAgjCAMB0l3BWEAWA7NAbAgnMgHJBpMgEzIaokgKTXW0ICmAtGGAFABOIJCG4RcMmQDatMPHYB3Hn1Gz+2fpHYBDBeFT8AzBjyb++sElZIJ8OCGbJo2VJW27sebSW148Ea7ftuEYbDBkbG1sQPALSW5eRR09ECUoHkkZXX1EtIMoaRBMsC0UMH585Ry8gsyY7IBjDSrtYg0xWAswtvaOsJRofAxsSCLsBF581HAELlzG+viq8RS6uXrGlRkgkSLaAnkVAHMQbc2D2hIPJJVakjIpkSuRdxFmyM6XtqsbOwd-QODQ8JVomcGrcgXhHhE4Dk7jcNMDsjJliD9HDVjxrg9YWD4TxQbc5BjUfUsVVkJY9hpSSc5MgiucoXIAlQqnN2AAHQrFAo0-j1On7bkU2kkSh8g74DRg-TCqhiNliowFSWwukyAi0cVqhKlGR6fTi3Va7LcA3i1C6FD6eYWdgAL2O6v0Wj1UpAABNGAAzVQAVwANgAXZg2xgAO0YnFtIDN-FN8XFVHdXr9geDYYjOrOjJABpZ+xNlhNtNlGeRWPzxajJFoGINBJyWB0Zdx2NrjUo1ZW9fxjVbj0m7ZhA4JEIu2e7IgbuSxT1arxeVgQsAwoUgCAQugQeCGnmy+38VCO+5xluxCAKh7AB8EqJzcl7Rqj5qqmrmI-YtVv-GjTSgLXgc-nGwaC0PRkBoZdgnFYwck1Ep7SaGDLDgpU4NRTVElggoAWzM4MMsRITkkdQDWQpDFXGKxjBHeB3lsXAsE8M1IBIIZUC8RdCBXNcNy3TcIHMSJ60zQQDQIyYSMEM9imvBJ+nYAA3CEpQZOAjBk-jFyGCixF-CYAHseAgDBwVJZxkl-CB1R4cF-CSWztHYIA) 
	- [Circuit Comparison III (one unstable and one stable)](https://www.falstad.com/circuit/circuitjs.html?ctz=CQAgjCAMB0l3BWEAWAnNAbADgOwCZlk4NUxUtIkFIQqaEBTAWjDACgAnEPBDcDGmEL8aNVNTYB3brxEy+qPpDYBDeeBx8AzNg18s4JCyRh48FNCxbKYHAhxbHlcrWitrCVI9R4MYLTgGpmZwnOqKIDoGETR48FKRuhFRelAJKbZ8yGB8mWnSGZqJBjxKbADG6qWRkMjqorBmqM0trW2oIEx4lqw5yFhY-mS4AYZh1nXVKdWC8dLVC7IT+eDCOTQUcsoA5iCb63uxA1BplXgENZMXWlh1DSHtjy2u7s7evv6BaVx4x8u-Bhud3Ac2411q6mWynmSwhAMuK3OdSBkNuiL+aKmaOhqMmsiIojYu2qBPU2SUiNkZDwVVkygADigcqlyZCTjsmXwScy8Ph2US9v11LcSnzCYyRalJVN+dIKDQhfKQDEEtgDEK1cqylxNUKHFkDII4qEAF6HBUGTTqkogAAmDAAZioAK4AGwALkwTQwAHYMDhsM36lCW3RCmn2p1uz3ev0B6Sa6kgTUzAW6uDJ46swkJjF1dM5kD4GgozUonEYJZosvY1V-CHFhEV2H5+t3MKN5ad7Eg0KVSvaCEDyI9mAPJ6PVyQVCQHTILSeAR4MhaNK7BBgGkHDc0+GF+y5AS0TdbOslWRliHKLjB6pKma95T947VW90qCNeATydMBCwKy1LyvxgAgWjIEUIEJEqeT3nSUEZjBQp5DiSoRNBRTXpm0T6BmMTcPEaiJkU6H6IYnQgY+5h-rU2AIP0kBWGBODZFOM5zguiiQMuXiUaCiZHpqKo6sc24QUeYgSAAblqsR8pxqSCOA3Q8GRogfggbAAPbcBAGDAkQLhxB+EAKtwwIbicFlaGwQA) 
- So in this case the output get's limited by the diodes, and if we take $R_5 \gg R_2$ the $A$ value doesn't change (much), so that the frequency remains the same, which is important.
- For $V_{out}$ small, $A$ it's maybe approximately $3.2$.

---