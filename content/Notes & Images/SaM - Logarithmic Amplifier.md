###### Memory Card
![[Samsung_SaM_Notes_05_240515_183031_3.jpg]]

---
- ***Online Source***: [Wikipedia](https://en.wikipedia.org/wiki/Log_amplifier):<br>![[Pasted image 20231203170329.png]]
- ***Formula***: $$V_{out} = -V_T \ln\left(\frac{V_{in}}{I_{\kern-2pxS}\kern2px R}\right)$$Where:$$V_T = {KT \over q}$$Form [Wikipedia](https://en.wikipedia.org/wiki/Log_amplifier) :$$V_{BE} = V_T \cdot \ln\left({I_C \over I_S}\right)$$And the [[SaM - Sensors Based on Silicon Junctions (BJT and Integrated Circuits)|BJT]] formula we found is:$$V_{BE} = \frac{kT}{q}\ln\left({I_C \over I_S}\right)$$
- [Circuit](https://www.falstad.com/circuit/circuitjs.html?ctz=CQAgjCAMB0l3BWcMBMcUHYMGZIA4UA2ATmIxAUgoqoQFMBaMMAKAHNwwURs1Pvs2QlCgsATuAAskkChQy5C+SLDwWAd1nLFshMJ2QNu-dr3gUeUQBcekGWEJVc9iyKZRY8SIUmEwxbAw8SFxsMkIfEAYYHz8AoJCQ8PJVKgATOgAzAEMAVwAbKyMUMy5LC0sy0U1eKirsBG4qww5ncEdbewxhKkNs41lJJ0bBqkqkJiRUryiYL29ff0Dg0PDIuvmjBu55KkkHUdktkfqR3dEOEv0zK9kMbl6WADd+Hj5mHeU6kCHqJl6PAgWENsDw8PZpBQuLJ8CJiAB9HzwyDwobEPDwhDI6BgeFMeEoeEI7BGMCQnQfLQKYEhN5SewdNCWOqSRGslFojFDbG4-GEsnwklAA) (*High negative inputs*):<br>![[Pasted image 20240131182835.png]]
- [Circuit](https://www.falstad.com/circuit/circuitjs.html?ctz=CQAgjCAMB0l3BWcMBMcUHYMGZIA4UA2ATmIxAUgoqoQFMBaMMAKAHNwwURs1Pvs2QlCgsATuAAskkChQy5C+SLDwWAd1nLFshMJ2QNu-dr3gUeUQBcekGWEJVc9iyKZRY8SAgS9SkYhRVQgw8MCQGGB8-YgCgyBCwpFUqABM6ADMAQwBXABsrIxQzLksLS1LRTV4qSuwEbkrDDmdwR1t7DGEqQyzjWUknBoGqCojw5C8qSM94aJR-QODQidqpo3rueSpJBxHZDeG64e3RDmL9MwvZDG4elgA3fh4+Zi3lWpBBjwgZiB7oAgWINsDw8PZpBQuLJ8CJiAB9QiSeGQeGDYh4eEoQEo6BgeFMLHwhHYIxgSE6N5aBTAyCg3hSeztNCWWrIpEotEBTEwbBcBC4-GElDw8nw0lAA) (*Low negative inputs, even reaching $0$*):<br>![[Pasted image 20240131183024.png]]