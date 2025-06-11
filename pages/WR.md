### Formuleer de 64-bit IEEE standaard voor floating point getallen en bereken de computerprecisie.
collapsed:: true
	- De 64 bit IEEE standaard voor floating point of beter gekend als de "double" maakt gebruikt van 64 bits waarvan 53 mantisse and 11 bit exponent.
	- We gebruiken de standaard om floating getallen voor te stellen als volgt: 
	  $$fl(x) = \pm i_0.i_1....i_p \times 2^e$$
	  Het teken heeft ook 1 bit nodig voor zowel de mantisse als exponent.
	- Het grootste getal is: 
	  $$1.1.....1 \times 2^{1111....1} \approx O(10^{308})$$
	- Het kleinste getal is:
	  $$1.0 \times 2^{-111...1111} \approx O(10^{-308})$$
	- 2e getal na nul:
	   $$0.00...1 \times 2^0 = 2^{-52} \approx O(10^{-16})$$
	- $\Rightarrow$ Double systeem rekent men met 15 cijfers maximaal
- ### Bewijs en formuleer de stelling van Sterbenz. Wat bedoelt deze precies?
  collapsed:: true
	- Zij $x = fl(x)$ en $y = fl(y)$ en $\frac{y}{2} \leq x \leq 2y$ dan geldt $x - y = fl(x-y)$
	- De stelling laat vooral zien dat precisieverlies optreedt bij het aftrekking van 2 niet FP getallen. Eens we alleen FP getallen gebruiken dient men alleen de voorwaarde van Sterbenz te respecteren. De getallen worden opnieuw geordent zodat deze voorwaarde gerespecteerd wordt.
	- **Bewijs**
		- Beshouw een systeem met precisie p in basis 10 en stel
		  $$y = i_0,i_1i_2...i_p \times 10^e$$
		  $$x = j_0,j_1j_2...j_p \times 10^e$$
		  Zonder verlies aan algemeenheid stellen we dat $y \leq x$.
		- We berekenen het verschil $x-y$:
		  $$x-y = ( j_0,j_1j_2...j_p \times 10^{d-e} - i_0,i_1i_2...i_p ) \times 10^e  $$
		- Is $j_0,j_1j_2...j_p \times 10^{d-e} - i_0,i_1i_2...i_p$ een mantisse met precisie p
		  $$x - 2y \leq 0$$
		  $$\Rightarrow x - y \leq y$$
		  $$\Rightarrow  (x-y)10^{-e} \leq y 10^{-e}$$
		  $$\Leftrightarrow j_0,j_1j_2...j_p \times 10^{d-e} - i_0,i_1i_2...i_p \leq  i_0,i_1i_2...i_p $$
		- De macht van 10 is positief maar vraag niet een extra cijfer zodat p cijfers voldoende zijn. Om de verschil uit te drukken hebben we maximaal p cijfers nodig
		  Stelling van Sterbenz duidt aan dat het rekenen met machinegetallen minder gevoelig is dan niet rekenen met niet-machine getallen.
- ### Hoe definieer je de conditionering en conditiegetal? Wat stelt dit getal precies voor?
  collapsed:: true
	- De conditionering onderstelt de numerieke bewerkingen als perfect, maar **bestudeert de invloed van een invoerfout of pertubatie**. Dit is een afrondfout analyse. Hoe propageert de initiele afrondingfout zich naar het eindresultaat. Hoe rekengevoelig is het eindresultaat ten gevolgen van fouten aan de start.
	- Stel dat we de functie $F(x)$ willen evalueren met invoer $x \in \mathbb{R}$. Aangezien de invoer een afrondfout heeft beschouwen we dit eerste orde analyse
	  $$F(fl(x)) = F(x+\Delta x) \approx F(x) + F'(x) \cdot \Delta x$$
	  De relatieve fout is nu 
	  $$\delta F(fl(x)) = \frac{F'(x)}{F(x)} \Delta x =  \frac{xF'(x)}{F(x)} \delta x$$
	  Het conditiegetal $\gamma(x) = \frac{xF'(x)}{F(x)}$
	- He conditiegetal van een functie met een argument meet **hoeveel de output waarde van de functie kan veranderen voor een kleine wijzinging als input argument**.
	- **relatieve fouten in de invoer tot 1000 keer groter kunnen worden in de oplossing**.
- ### Leg het verschil uit tussen sterke en zwakke numerieke stabiliteit.