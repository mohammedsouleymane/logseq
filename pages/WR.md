# Formuleer de 64-bit IEEE standaard voor floating point getallen en bereken de computerprecisie.
	- De 64 bit IEEE standaard voor floating point of beter gekend als de "double" maakt gebruikt van 64 bits waarvan 53 mantisse and 11 bit exponent.
	- We gebruiken de standaard om floating getallen voor te stellen als volgt: 
	  $$fl(x) = +- i_0.i_1....i_p \times 2^e$$
	  Het teken heeft ook 1 bit nodig voor zowel de mantisse als exponent.
	- Het grootste getal is: 
	  $$1.1.....1 \times 2^{1111....1} \approx O(10^{308})$$
	- Het kleinste getal is:
	  $$1.0 \times 2^{-111...1111} \approx O(10^{-308})$$
	- 2e getal na nul:
	   $$0.00...1 \times 2^0 = 2^{-52} \approx O(10^{-16})$$
	- $\Rightarrow$ Double systeem rekent men met 15 cijfers maximaal
	-
-
-