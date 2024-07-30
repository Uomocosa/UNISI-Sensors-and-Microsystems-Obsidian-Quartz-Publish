###### Memory Card
![[Samsung_SaM_Notes_05_240515_183031_2.jpg]]

---
- The definition of "***Differential Amplifier***" is:<br>==A Differential Amplifier is a type of amplifier that **amplifies the voltage difference between two input signals** while **rejecting any common-mode signals** (signals that are common to both inputs)==.
- To measure how effective a Differential Amplifier is at rejecting common-mode signals, we can calculate its [[SaM - CMRR (Common Mode Rejection Ratio)|CMRR]] (*Common Mode Rejection Ratio*).
- ==*Here we can see some examples of Differential Amplifers*==:
	- [Circuit](https://www.falstad.com/circuit/circuitjs.html?ctz=CQAgjCAMB0l3BWcMBMcUHYMGZIA4UA2ATmIxAUgoqoQFMBaMMAKAENwAWTkNPXzlT4h+YJEyRh48athDYWAJS48wxFCKpqNVKoOq6o0BEpW8UPPEItRb+uYZgmADgKH43vDBodQWAc09MDQsqXB5dFgAPEAxicAxCEGI5MDiQVQ0ANVYYvAgLJOIkC3jMkCyUaN5IVPz5YiSwPB5VfgBxNgBLADsAHQBnAHsAM0GAFwALOkGAQQBbZwAbLpGuugAnQb6AR0GFIA) (Ideal Differential Amplifier)<br>![[circuit-20231124-1852.png]]
	- [Circuit](https://www.falstad.com/circuit/circuitjs.html?ctz=CQAgjCAMB0l3BWcMBMcUHYMGZIA4UA2ATmIxAUgoqoQFMBaMMAKAEMQ09P8RcAWHt25gkTJGHjxw0SnDClShKSNnIpLAO5DwxFDrApukFgCcDe8Ed36qkuGZ0oUgw92eC78R104udAlDqJuaBvoGBXg7mvm58kK7WUSbagXFhvCYASlYiloSullRU-LRBxbIsOXEeIAV+nkGlfOVQlQAOfITuvNjd8YLY5VoDAf2+JgDmAQkBaMPTEbMR88Usi-0Rm6tQLAAefKKc-IR8uMfEIIkgWQAy+5yUyPpE+pJI11kAZg+EQ2AYU5YcAYS7XABqrAOhCQLiBlxcYKsIHBKBYQA) (Differential Amplifier made with an O.A.)<br>![[circuit-20231004-1432.png]]
	- [Circuit](https://www.falstad.com/circuit/circuitjs.html?ctz=CQAgjCAMB0l3BWcMBMcUHYMGZIA4UA2ATmIxAUgoqoQFMBaMMAKAEMQ09P8RcAWHt25gkTJGHjw+seClLE8eeP27ZkUlgHch4Yil1gU3SCwBOh-eGN6DVSXHO6UKQUe4vB9+E66dXugJQfD4WQX5BQd6OFn7uIW42VLiOOkHx4bymAErWIlaEblZUVPy0wSXQCCy58Z4ghf5ewWUgzZXVAA58hB682L0JfBXaQxGDfqYA5oGQghFoIzORc0PYiyUsy4OROxtQLAAefKKc-IR8uGfEbdYg2QAyR5yUyAZEBpJIifcAZs+EdRgDAXLDgDA3H4ANVYx0ISFcoJurkhdyhKBYQA) (Differential Amplifier made with an O.A.)<br>![[Pasted image 20240131125222.png]]
	- [Circuit](https://www.falstad.com/circuit/circuitjs.html?ctz=CQAgjCAMB0l3BWcMBMcUHYMGZIA4UA2ATmIxAUgoqoQFMBaMMAKAENwAWTkbBFECk5U+AvOCRMkYePEGxZpUrOzkBM2ey49mAoVV0hiEkFOSyqnaEuJo4YEqQSFqG+CwBK2oy+K+XVJa0UCEwCJ7e2ITifrzRoSDCgglhLABOgkmG+uC2IW7pmQZ5OZgCBu4ZpRh6SaL57gDukVHeZVAszWDcgjVFveWd3mAo4t06eZBD47m1xYNVWSO8aODLFXCFOfXYq-UbU827BsvHgvgdHGcoQokOgrdjkmDSFlQMMJykeITwhNhfLBgcQfaBfJzwYHgzijcyVXitQyce6GA5DbCI06rVFDZEuJH3G48Q53FxExKccTkknXOp7fgdI70gQYlz7Qqs3gMvFc8pwlgAc1JvOF2DwxI6AAcKVTbtxxLgeNhQoKZbxIDx5bxxSqgA) ([[SaM - Instrumentational Amplifier|Instrumentational Amplifier]]):<br>![[Pasted image 20231004153201.png]]

---

![[Pasted image 20230626201332.png]]
- When you find a **single-input amplifier**, the second input is supposed to be to a reference and fixed voltage.
- In general, since I'm speaking about amplifier, I suppose that ==**it behaves linearly**==. 

So we have that:<br>![[Pasted image 20230626201348.png]]

Remember that:<br>![[Pasted image 20230626201359.png]]
- ==Real operational amplifier have this quality here, but the common mode gain is not zero==.<br>I accept it because perfect symmetry is not possible, ==but I have a differential gain which is actually much larger than the common mode gain==. 
- So for an **Ideal Differential Amplifier** we can write:$$V_o = A_d\cdot(V^+-V^-)$$Instead for a **Real DIfferential Amplifier**:$$V_o = A_1{V^+} - A_2{V^-}$$
---

- ***Online Source***: [Webpage](https://www.electrical4u.com/differential-amplifier/#:~:text=A%20differential%20amplifier%20is%20an,difference%20between%20the%20two%20voltages.&text=From%20the%20formula%20above%2C%20you,the%20output%20voltage%20is%20suppressed.)<br>![[Pasted image 20231004143428.png]]
- Formula: $$V_{out} = V_2\frac{R_3}{R_2+R_3}\frac{R_f+R_1}{R_1}-V_1\frac{R_f}{R_1}$$
- If $R_1=R_2$ & $R_f=R_3$ (this is the specific differential amplifier used for an [[SaM - Instrumentational Amplifier|instrumentational amplifier]]):$$V_{out} = V_2\frac{R_3}{R_2+R_3}\frac{R_3+R_2}{R_2}-V_1\frac{R_3}{R_2} = (V_2 - V_1)\frac{R_3}{R_2}$$
---

**NOTE**: 
A differential amplifier output functions depends only on the difference: $V^+-V^-$.
[Here](https://www.falstad.com/circuit/circuitjs.html?ctz=CQAgjCAMB0l3BWcMBMcUHYMGZIA4UA2ATmIxAUgoqoQFMBaMMAKACcKAWTkTFEQgkK8M-KmHjsBQ3vhAZCeWUqpo4LAIbThKPEoVLdSpWCRMkE+HBAMYV7KWJ742BKTzExyKywDu2kX5BHTlIKWCQXB4EbkjIHnFJDgiogOw8BNl1AHM0jIDOayow-wNePRA8MB0KlD95RWUGwwqwgCUuHj4QTmIdUShBwpsvYugEFg7iMH5sNErCHjniodVBsYnc6f4jSrxVVqgWXJil+IoZuMyS8DBsHRQeZnuro-9n4VTmfNS63IlHj1rACeJxquspCDIvMoYUVmowhwocsQNtoStLDcobtsYCwlpkecPq8TGZTN4rOBoNgaShiDTsJwELSyBAwNSGZyuQyKeokZBAShAcShZkEVI0TiBV1DpipKIqL1hHg5j0+oM5RwVfxOKriLFdV5xVptRd+PropdSTZyZj4BRoI4nFY3O4eIRYFYvVY2V76qalZVVYajlrVQhdPJ5hGVBSpKaY0GgqEsmFcqbCHIM3i3qjYghLqR+AWdvULT09fnLu0o7RI4QBomVsNiOsoONJrW1cIGzr1c2qLGNiwgA)'s an example of a differential amplifier:<br>![[Pasted image 20240131124912.png]]
Where the output is: $$V_{out} = 2(V^+-V^-)$$
While [here](https://www.falstad.com/circuit/circuitjs.html?ctz=CQAgjCAMB0l3BWcMBMcUHYMGZIA4UA2ATmIxAUgoqoQFMBaMMAKACcKAWTkTFEQgkK8M-KmjjsBQ3vhAZCeWUqph4LAIbThKPEoVLdSpWCRMka+HBAMYVyKVJ5K6FJ1KFyq+ywDu2kX5BHTlIKWCQXB4EbkjIHm9JDgiogOw8BNlJAHM0jIDOayow-wNePRA8MB0KlD95RWUGwwqwgCUuHj4Qdx1RKAHCmzEBmAQWDuIwfmw0SsIeWeLB8VGoaHHcqf4jSrxxVqgWXJjF+IppuMyS8DBsHTdb+6uj-2Zn1OZ81LrctUfCt4AdVRlJ-os5uCekUsmEOFCliBtpE5okblDdhjHmEtAjzu9hKkTGZTMh7OBoNgqdg7tTCNTdOQwJTqay2dSyep4ZBHihHgTeNjOVJkZieV1DhI4fI5r1KrMesRhOIufL+JwFcRYhqRpYcWqLvwtdFLsSbKS9fAKNBHMQXHAMO5iHg7QJYPYPXAIJabngFXK-eqFdLAxRdDLaOG0VJQwhw6HCKFYccDYnjArCEKbsbDUjiPwEJc6v4czqkbFC2IJhGw0pPAWoyskWsxtXRFQ5fXFcqmypRhsWEA) one that is **NOT** a differential amplifier:<br>![[Pasted image 20240131124803.png]]
Where the output is:$$V_{out} = V^+-{1\over 2}V^-$$