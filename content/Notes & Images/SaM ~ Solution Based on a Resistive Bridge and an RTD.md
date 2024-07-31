**RTD**: *Resistance Temperature Sensor*

I can use an RTD to get the voltage related to a specific temperature, in this case temperature $T$:
![[Pasted image 20230719115727.png]]
- The actual value would be:$$V_{TH} = V\left(\frac{R_{io}(1+\alpha T)}{R_{io}(1+\alpha T)+R_4}-\frac{R_2}{R_2+R_3}\right)$$
- If we take $K \gg 1$, so $R_3 \gg R_2$ and $R_4 \gg R_1$, we obtain a much simpler formula:$$V_{TH} \simeq V \frac{R_{io}}{R_4}\alpha T = V \frac{R_2}{R_3}\alpha T = V \frac{1}{K}\alpha T$$
- **NOTE** the sensitivity of this device will not be the maximum possible since we have taken $K \neq 1$.
