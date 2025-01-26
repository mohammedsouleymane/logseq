- Bewijzen
	- Bezout
	  collapsed:: true
		- [Bezout's Identity | Brilliant Math & Science Wiki](https://brilliant.org/wiki/bezouts-identity/)
		- De bewijs van Bézout's identiteit maakt gebruikt van a,b ∈ ℤ, a delen door b geeft een rest van r1 < |b| en ggd(a,b) = ggd(r1, b). Vervolgens hebben we door herhaalde toepassingen van het Euclidische delingsalgoritme.
		  $$a = bx_{1} + r{1}, 0 < r{1} < |b| 
		  \\b = r_{1}x_{2} + r_{2}, 0 < r_{2} < r_{1}
		  \\.....
		  \\ r_{n-1} = r_{n}x_{n+1} + r_{n+1}, 0 < r_{n+1} < r_{n}
		  \\r_{n} = r_{n+1}x_{n+2}$$
		  waar de rn+1 is de laatste niet-nulzijnde rest in het delingsproces. Nu, zoals geïllustreerd in het bovenstaande voorbeeld, kunnen we de voorlaatste vergelijking gebruiken om op te lossen voor rn+1 als een combinatie van rn en rn - 1. Als we dit uitvouwen, kunnen we het oplossen voor rn als een combinatie van rn-1 en rn-2, enz. totdat we uiteindelijk schrijven rn+1 als een lineaire combinatie van a en b. Sinds rn+1 de laatste niet-nulzijnde rest in het delingsproces is, is het de grootste gemene deler van a en b wat de identiteit van bezout bewijst.
	- chinese resttelling
	  collapsed:: true
		- **stelling** Zij $m_{1},m_{2},...,m_{n}$ paarsgewijs relatief prieme natuurlijke getallen en $a_{1},a_{2},...,a_{n}$ willekeurige gehele getallen. Dan heeft het stelsel
			- $$x \equiv 2 (mod 3) 
			  \\x \equiv 3 (mod 5)
			  \\x \equiv 1 (mod 7)$$
			  een oplossing die uniek is modulo m = $m_{1},m_{2},...,m_{n}$.
			  Dwz een unieke oplossing x met $0 \leq x < m$ en alle andere oplossingen congruent modulo me t deze x.
		- Bewijs
			- We geven een constructief bewijs. We gaan dus een algoritme geven om de oplossing werkelijk te construeren. 
			  We gaan een variabele $M_{k} = \frac{m}{m^{k}}$, dat is he product van alle moduli, behalve m_{k}.
			  Omdat alle moduli relatief priem hebben we $ggd(m_{k},M_{k}) = 1^{18}$, we weten dus als we gaan rekenen in $ℤ_{mk}, M_{k}$ inverteerbaar is en dat betekend dat we een getal $y_{k}$ kunnen vinden voor $M_{k}$ zodat:
			  $$M_{y}y_{k} \equiv 1 (mod m_{k})$$
			  Stel nu:
			  $$x = a_{1} M_{1} y_{1} + a_{2} M_{2} y_{2}+ ...+ a_{n} M_{n} y_{n} \in ℤ$$
			  We tonen nu dat deze x een oplossing is van het stelsel. 
			  Merk eerst op dat:
			  $$M_{j} \equiv 0 (mod m_{i})$$
			  van zodra $i \neq j$ Als we dus x reduceren modulo $m_{k}$, blijft er alleen maar:
			  $$x \equiv a_{k}M_{k}y_{k} \equiv a_{k} (mod m_{k})$$
			  𝑚𝑘zit er zelf al niet meer in want we hebben hem weg gedeeld, maar we weten dat die 𝑚𝑘 geen gemeenschappelijke deler had met alle die andere 𝑚𝑖 ’tjes. Dus als we naar de 𝑔𝑔𝑑(𝑚𝑘, 𝑀𝑘 ) dan zijn die relatief priemover. Onderstel nu dat 𝑦 een andere oplossing is van het stelsel. Dan geldt voor elke 𝑘 ∈ [𝑛] dat: 𝑚𝑘|𝑥 − 𝑦 
			  Vermits alle 𝑚𝑘 relatief priem zijn, volgt hieruit 𝑚 | 𝑥 − y
	- Principe van Bewijs per Inductie
	   Zij $P(n)$ een eigenschap die we willen bewijzen voor alle $n \in \mathbb{N}$
	   
	  1. **Basis van de inductie**. Zij $P(0)$ waar ($P(1)$ of $P(n_{0}$), met $n_{0}$ het kleinste natuurlijke getal waarvoor P zijn heeft.)
	    
	  2. Onderstel dat de inductiehypothese geldt, i.e. wanneer $P(k)$ waar is voor een willekeurige $k \in ℕ$, dan is $P(k+1)$ dan ook (deze stap heet de **inductiestap**)
	    
	  Dan is $P(n)$ waar voor alle $n \in \mathbb{N}$
	- Identiteit van pascal
	  collapsed:: true
		- $\binom{n- 1}{r - 1} + \binom{n- 1}{r} = \binom{n}{r}$
		  $\binom{n- 1}{r - 1} + \binom{n- 1}{r} = \frac{(n-1)!}{(n-r)!(r-1)!} + \frac{(n-1)!}{(n-1-r)!r!}$
		  $\frac{(n-1)!r}{(n-r)!r!} + \frac{(n-1)!(n-r)}{(n-r)!r!}$
		  $\frac{1}{(n-r)!r!} ((n-1)!r + (n-1)!(n-r))$
		  $\frac{1}{(n-r)!r!} ((n-1)!r + (n-1)!n - (n-1)!r)$
		  $\frac{1}{(n-r)!r!} ( n!)$
		  $\frac{n!}{(n-r)!r!}$
		  $\binom{n}{r}$
	- Duiventil
	  collapsed:: true
		- Stelling
		  Als we n identieken object verdelen over k dozen met $n > k$, dan is er minstens 1 doos met minstens 2 objecten
		- Bewijs(uit het ongerijmde)
		  Veronderstel van niet. Dan is er in elke doos hoogstens 1 object. Zij m het aantal lege dozen (met 0 objecten). Dan zijn er in totaal $k - m$ dozen met elk een object
		  Vermists alle objecten verdeeld werden geldt:
		  $$n = k - m \leq k \leq n$$
		  en dat is een tegenspraak
		- Notatie
		  Zij $x \in \mathbb{R}$. Dan noteren we 
		  #+BEGIN_EXPORT latex
		  
		  \begin{aligned}
		  \lceil x \rceil &= \text{kleinste geheel getal } \geq x \\
		  \lfloor x \rfloor &= \text{grootste geheel getal } \leq x
		  \end{aligned}
		  #+END_EXPORT
	- Boom
	  collapsed:: true
		- Definitie
		  Een samenhangende ongerichte simpele graaf zonder cyclus noemen we een boom.
		- Eigenschappen
			- Een top van graad 1 in een boom heet een blad.
			- Een boom op $n \geq 2$ toppen heeft minstens twee bladeren.
			  collapsed:: true
				- Bewijs
				  Neem een top $t$ van de boom. Dan zijn er twee mogelijkheden:
				- $t$ is geen blad. Wandel dan vanuit $t$ naar een buur, dan nog een buur, enz. zonder ooit een top tweemaal te bezoeken. Omdat de boom eindig is, stopt dit in een zekere top $s$. Dit moet een blad zijn, want als het proces gestopt zou zijn omdat $s$ meerderen buren zou hebbe die reeds eerder bezocht werden, betekent dit dat er meerdere paden van $t$ naar $s$ zijn, tegenspraak.
				  
				  Om het tweede blad te vinden gebruiken we dat $t$ geen blad is dus deg(t) > 1 zodat we vanuit $t$ nog een wandeling kunnen maken op zoek naar een andere blad.
				- $t$ is een blad. Neem dan de enige buur van $t$ in plaats van $t$. Deze top heeft graad $\geq 2$ tenzij de boom bestaat uit 2 toppen die 1 boog vormen. Maar in dit geld het lemma duidelijk.
				-
			- Een boom n toppen heeft n - 1 bogen.
			  collapsed:: true
				- Bewijs (per inductie op n)
				- ### Basisstap ( n=1 )
				  
				  Als een boom n=1 top heeft, dan bestaat deze boom alleen uit één losse top en bevat hij geen enkele boog. Dus in dit geval zijn er n−1=1−1=0bogen, wat klopt.
				- ### Inductiestap
				  
				  We nemen als inductiehypothese aan dat de stelling waar is voor een boom met n toppen: een boom met n toppen heeft precies n - 1 bogen.
				  
				  We bewijzen nu dat de stelling ook waar is voor een boom met n+1 toppen.
				- Neem een boom $\mathcal{T}$ met $n+1$ toppen.
				- Een belangrijk lemma over bomen stelt dat een boom altijd een blad heeft. Een blad is een top die verbonden is met slechts één boog. Noem dit blad $t$.
				- Verwijder het blad $t$ en de boog waarmee $t$ verbonden is uit de boom $\mathcal{T}$. Wat overblijft is een nieuwe graaf $\mathcal{T}'$, die een boom is met precies n toppen (omdat we één top en één boog hebben verwijderd).
				- Volgens de inductiehypothese heeft deze kleinere boom $′\mathcal{T}'$ precies n−1 bogen.
				  
				  In de originele boom $\mathcal{T}$ was er precies één extra boog, namelijk de boog die verbonden was met het blad $t$. Dus de totale hoeveelheid bogen in $\mathcal{T}$ is:
				  
				  (n−1)+1 = n.
				  
				  Hiermee hebben we aangetoond dat een boom met n+1 toppen precies nn bogen heeft.
				- ### Conclusie
				  
				  Door inductie volgt dat een boom met nn toppen altijd n−1 bogen heeft, voor alle n≥1n \geq 1.
				-
			- Gerichte boom + gewortelde boom
			  Definitie
			  Wanneer $\mathcal{G}$ een gerichte graaf is, dan wordt $\mathcal{G}$ een gerichte boom genoemd als de ongerichte graaf geassocieerd met $\mathcal{G}$ een boom is.
			  
			  Een gerichte boom noemen we een gewortelde boom als er een unieke top $t$ is waarvoor de ingraad nul is en alle andere toppen ingraad 1 hebben. We noten $(\mathcal{G},t)$.
			- Bos + gewortelde bos
			  Definitie
			  Een bos is een ongerichte simpele graaf zonder cyclus.
			  Een geworteld bos is een bos waarin elke samenhangscomponent geworteld is.
			  We kunnen elke ongerichte boom wortelen door een willekeurige top als wortel te kiezen waardoor alle bogen een natuurlijke orientatie krijgen weg van die wortel.
		-
	- Bewijs: Binomium van Newton
	  collapsed:: true
		- Stelling
		  
		  #+BEGIN_EXPORT latex
		  \begin{align*}
		  (a + b)^n &= \binom{n}{0} a^n b^0 + \binom{n}{1} a^{n-1} b^1 + \cdots + \binom{n}{n} a^0 b^n \\
		            &= \sum_{i=0}^{n} \binom{n}{i} a^{n-i} b^i
		  \end{align*}
		  #+END_EXPORT
		- __Bewijs__
		  Be macht 
		  $$(a + b)^n = \underbrace{(a + b)(a + b) \cdots (a + b)}_{\text{n keer}}$$
		  werken we uit aan de hand van de distributiviteit. De term met $a^{n-i}b^i$ ontstaat door in $i$ factoren $(a + b)$ de b te kiezen (en in de overige natuurlijk de a). De coëfficiënt die hoort bij $a^{n-i}b^i$ is bijgevolg gelijk aan het aantal keuzes van $i$ objecten uit n. Dat is $\binom{n}{i}$.
		-
	- Euler
	  collapsed:: true
		- Definitie
		  Een pad in een ongerichte multigraaf $\mathcal{G}$ heet een Eulerpad indien het elke boog van $\mathcal{G}$  precies 1 maal bevat. Een gesloten Eulerpad is een Eulercyclus. Een multigraaf die een Eulercyclus bevat heet een Eulergraaf.
		- Stelling
		  collapsed:: true
		  Zij $\mathcal{G}$ een ongerichte multigraaf zonder geïsoleerde toppen. Dan geld dat $\mathcal{G}$ een Eulergraaf is als en slechts al $\mathcal{G}$  samenhangend is en alle toppen van $\mathcal{G}$  even graad hebben.
			- Bewijs
				- $Rightarrow$ Omdat $\mathcal{G}$  een Eulercyclus heeft, bestaat $\forall{a,b} \in V$ een pad van a naar b, namelijk dat deel van de cyclus dat start in a en aankomt in b. Dus $\mathcal{G}$  is samenhangend. 
				  
				  Kies een willekeurige top $v$ in $\mathcal{G}$. Als we de Eulercyclus volgen, passeren we mogelijk verschillende keren in $v$. Elke doorgant in $v$ gebruikt 2 bogen: 1 om binnen te komen en 1 om terug buiten te gaan. Ook doorlopen we elke boog die $v$ bevat juist 1 keer zodat $deg(v)$ gelijk is aan tweemaal het aantal keer dat we in $v$ komen, wat een even getal is.
				  
				  $\Leftarrow$ We moeten een Eulercylus construeren. Als het aantal bogen in $\mathcal{G}$ 1 of 2 is, dan ziet $\mathcal{G}$  er als volgt uit:
				  ![f38e10b1-2c1f-445c-a6bb-bae77d588d98.webp](../assets/f38e10b1-2c1f-445c-a6bb-bae77d588d98_1735599056934_0.webp){:height 205, :width 547}
				  
				  We gaan nu verder per inductie en onderstellen dat het resultaat waar is wanneer er minder dan n bogen zijn. Wanneer $\mathcal{G}$  n bogen heeft, neem dan $v$ een willekeurige top. Kies een boog die $v$ bevat. Die heeft een andere uiteinde $u$. Kies nu een boog die $u$ bevat, maar niet de boog die je juist gebruikte om uit $v$ te vertrekken. Blijf zo bogen toevoegen, zonder tweemaal dezelfde te gebruiken. Doordat de graand van elke top even is, kunnen we steeds verder (telkens we in een to binnenkomen, is er nog een ongebruikte boog om buiten te gaan). Doet dit tot we terug in $v$ aankomen, dan hebben we een gesloten pad $P$ gemaakt dat verstrekt en aankomt in $v$ en geen enkele boog tweemaal gebruikt. Als alle bogen van $\mathcal{G}$  tot $P$ behoren, hebben we een Eulercyclus.
				  ![598f6604-6046-4e7e-8396-5d57ff6d86e4.webp](../assets/598f6604-6046-4e7e-8396-5d57ff6d86e4_1735599350410_0.webp)
				-
		- Stelling
		  Een samenhangende ongerichte multigraaf G heeft een Eulerpad dat niet gesloten is als een slechts als $\mathcal{G}$  juist twee toppen heeft van oneven graad.
			- Bewijs 
			  $\Rightarrow$ Zij $u$ en $v$ de begin- en eindtop van het Eulerpad. De eerste boog van het pad geeft een bijdrage 1 tot de graad van $u$. Telkens het pad weer langs $u$ gaat, neemt de graad met 2 toe. Dus zal de graad van $u$ in het totaal oneven zijn. Analoog zal de graad van $v$ oneven zijn omdat de laatste boog van het pad de graad met 1 laat toenemen. All overige toppen hebben duidelijk even graad.
			  
			  \Leftarrow Zij $u$ en $v$ de twee toppen met oneven graad. Voeg aan $\mathcal{G}$  de boog $\{u,v\}$ toe. Dan heeft elke top even graad en is vorige stelling van toepassing. We krijgen dus een gesloten Eulerpad. Als we hierin de boog $\{u,v\}$ weglaten, hebben we Eulerpad in $\mathcal{G}$.
	- Hamilton:
		- Definitie:
		  Een simpel pad dat alle toppen van een multigraaf $\mathcal{G}$ bevat heet een Hamiltonpad. Een Hamiltoncyclus is een gesloten Hamiltonpad. Een multigraaf die een Hamiltoncylcus bevat heeft een Hamiltongraaf.
		  ---
		- Bewijs: Als je k toppen uit een Hamiltongraaf $\mathcal{G}$  weglaat, samen me de aangrenzende bogen, dan valt $\mathcal{G}$ uiteen in hoogsteens k samenhangscomponenten.
		  
		  Zij $\mathcal{H}$ een Hamiltoncylcus in $\mathcal{G}$. Noem de grafen die uit $\mathcal{G}$ en $\mathcal{H}$ respectievelijk ontstaat door weglaten van k toppen resp. $\mathcal{G}'$ en $\mathcal{H}'$. Voor $\mathcal{H}$ is de bewering zeker waar omdat $\mathcal{H}$ een cyclus is (en die valt uiteen in hoogstens k componenten). Maar $\mathcal{G}'$ bevat meer boven dan $\mathcal{H}'$. Dus kan het aantal samenhangscomponenten van $\mathcal{G}'$ niet groter zijn dan dat van $\mathcal{H}'$.
	- ## Bewijs: Het aantal keuzes met volgorde en zonder herhaling
	  
	  **Stelling**
	  Het aantal geordende keuzes van $m$ objecten uit $n$ zonder herhaling is
	  
	  $$n (n - 1) (n - 2) \cdots (n - m + 1).$$
	  
	  **Bewijs**
	  Om zo een woord te vormen moeten we achtereenvolgend $m$ verschillende elementen van $Y$ kiezen. Voor de eerste letter zijn er $n$ keuzes, voor de tweede $n - 1$ (want we mogen om het even welke letter nemen behalve die die we als eerste kozen). Voor de derde letter $n - 2$ keuzes enz. tot we de laatste letter kiezen uit de $n - m + 1$ die overblijven.
	  
	  **Notatie**
	  De **faculteit** van een natuurlijk getal $n \in \mathbb{N}$ is het getal
	  
	  $$n! = n \cdot (n - 1) \cdot \ldots \cdot 3 \cdot 2 \cdot 1$$
	  
	  Per definitie stellen we $0! = 1$. Het aantal keuzes in de stelling is bijgevolg kort te noteren als
	  $$\frac{n!}{(n - m)!}$$
	- ## Bewijs: Het aantal keuzes zonder volgorde en zonder herhaling
	  
	  **Stelling**
	  Het aantal keuzes van $k$ elementen uit een verzameling van $n$ elementen, zonder volgorde en zonder herhaling, bedraagt
	  
	  $$
	  
	  \binom{n}{k}.
	  
	  $$
	  
	  We merken ook nog op dat
	  
	  $$
	  
	  \binom{n}{n - k} = \binom{n}{k}.
	  
	  $$
	  
	  **Bewijs**
	  Zij $A$ een verzameling en $k \in \mathbb{N}$. Een $k$**-deelverzameling** van $A$ is een deelverzameling met $k$ elementen.
	  
	  Gegeven is $|A| = n$. Hoeveel $k$-deelverzamelingen heeft $A$?
	  Kiezen we $k$ elementen uit $A$ met ordening, dan zullen we eenzelfde deelverzameling meerdere keren kiezen. Beschouw de verzameling
	  
	  $$
	  
	  S = \{(B, f) \mid B \subset A, |B| = k \text{ en } f \text{ een ordening van } B\}.
	  
	  $$
	  
	  Dan kunnen we $|S|$ op twee manieren tellen: enerzijds
	  
	  $$
	  
	  |S| = x \times k!
	  
	  $$
	  
	  met $x$ het aantal $k$-deelverzamelingen van $A$ en $k!$ het aantal ordeningen van een gegeven $k$-deelverzameling. Anderzijds is
	  
	  $$
	  
	  |S| = 1 \times \frac{n!}{(n - k)!}
	  
	  $$
	  
	  want we kunnen op $\frac{n!}{(n - k)!}$ manieren $k$ elementen kiezen uit $A$ met volgorde. Natuurlijk bepaalt elk van die keuzes juist één $k$-deelverzameling.
	  We hebben dus
	  
	  $$
	  
	  x = \frac{n!}{(n - k)! k!}
	  
	  $$
	  
	  Voor $n \geq k$ noteren we
	  
	  $$
	  
	  \frac{n!}{(n - k)! k!}
	  
	  $$
	  
	  als
	  
	  $$
	  
	  \binom{n}{k}.
	  
	  $$
	  
	  **Notatie**
	  De verzameling van alle $k$-deelverzamelingen van $A$ noteren we als $\binom{A}{k}$
	  zodat
	  $\left| \binom{A}{k} \right| = \binom{|A|}{k}.$
	- ## Bewijs: Het aantal keuzes zonder volgorde en met herhaling
	  
	  **Bewijs**
	  Stel $A = \{a, b, c, d\}$. De keuze $bcadabd$ is equivalent met de keuze $aabbcdd$ wanneer de volgorde geen rol speelt. Hoeveel mogelijkheden zijn er zo?
	  
	  We moeten hier dus de woorden tellen die bestaan uit een aantal $a$'s, gevolgd door een aantal $b$'s, dan een aantal $c$'s enz. zodat er in totaal 7 letters zijn. Let wel, het aantal in kwestie kan soms nul zijn: $bbbbbbb$ is ook een woord van zeven letters met herhaling!
	  
	  Een voorstelling van $aabbcdd$ is $\bullet\bullet|\bullet\bullet|\bullet|\bullet\bullet$ . In totaal hebben we dus 10 tekens waarvan elk een $\bullet$ of een $|$ is. We zetten een $\bullet$ voor elke letter en een $|$ als de letter verandert.
	  
	  Dus $|\bullet\bullet \ | \ |\bullet\bullet\bullet\bullet\ \bullet$ stelt het woord $bbddddd$ voor: er zijn geen $a$'s omdat er voor de eerste $|$ geen $\bullet$ staat, en geen $c$'s omdat er tussen de tweede en derde $|$ geen $\bullet$ staan.
	  
	  In het algemeen hebben we $n$ objecten waarin we $k$ keer kiezen met terugleggen en geen rekening houden met de volgorde. Het aantal manieren om dat te doen is het aantal manieren om $n - 1$ streepjes te plaatsen als er $n + k - 1$ plaatsen beschikbaar zijn. Dit is dus $\binom{n + k - 1}{n - 1}$. We weten $\binom{n + k - 1}{n - 1} = \binom{n + k - 1}{k}$ zodat het aantal **herhalingscombinaties** van $k$ objecten uit $n$ gelijk is aan
	  $$\binom{n + k - 1}{k}.$$
- # Definities
	- **Facultiet:**product van een reeks factoren die telkens met één toenemen met de eerste factor gelijk aan één
	  dus: de faculteit van een natuurlijk getal n, genoteerd als n! (n faculteit), is gedefinieerd als het product van de getallen 1 tot en met n.
	- **toernooi** is een gericht simpele graf die ontstaat door een complete graf te orienteren.
	- Een multipgraf heet **planair** indien hij in een valk kan getekend worden zonder dat twee bogen snijden.
	- De verzameling van alle gehele getallen uitgerust met $+ \; en  \; \cdot$ is een **ring** met $0$ als neutraal element voor de optelling en $1$ als neutraal element voor de vermenigvuldiging die we noteren als $(\mathbb{Z}, +, \cdot)$.
	- Een **multigraf** is een graf $G \; = \; (V, \rightarrow) uitgebreid door middel van een functie $\mu \; : \; V x  V \rightarrow \mathbb{N}$ die een multipliciteit toekent aan elke pijl.
	  Een samenhangende gerichte (multi)graf G is een gericht Eulergraf $\Leftrightarrow$ G sterk samenhangend end gebalanceerd is.
	  We zeggen dat G sterk **samenhangend** is indien er tussen elke boog bv. u en v een gericht pad bestaat.
	- Definieer de **adjacentiematrix** A_{G} van G als de (n x n)-matrix met a_{ij} gelijk aan het aantal pijlen van de i-de naar de j-de top. Een lus wordt tweemaal geteld in een ongericht graf en éénmaal in een gerichte. De adjacentiematrix bevat veel informatie over de graf F.
	- Een **ongericht graf** is een verzameling topen en bogen waarbij de volgorde van de toppen in een bogen niet uitmaakt. A -> B = B -> A
	- ### Definitie: **Ondergrens**  + I **nfimum**  
	  Zij V een verzameling met S⊂V﻿. x∈V﻿ heet een **ondergrens** van S﻿ indien ∀s∈S:x≤s﻿. Het **infimum** van S﻿ is de grootste ondergrens van S﻿.
	- ### Definitie:**Minimum**
	  Indien het infinum van een verzameling S﻿ zelf tot S﻿ behoort, dan noemen we het een **minimum**.
	- ### Hamiltoncyclus
	  Een simpel pad dat alle toppen van een multigraaf G﻿ bevat heet een **Hamiltonpad**. Een **Hamiltoncyclus** is een gesloten Hamiltonpad. Een multigraaf die een Hamiltoncyclus bevat heet een **Hamiltongraaf**.
	- ### Welgeordendheid
	  Elke niet-lege deelverzameling van Z die een ondergrens heeft, heeft ook een minimum.
	- ### Grootste gemene deler
	  
	  Stel $a, b \in \mathbb{Z}$﻿. Een geheel getal dd﻿ heet een **grootste gemene deler (ggd)** van a﻿ en b﻿ indien $d∣a$﻿ en $d∣b﻿$ (gemene deler) èn $∀c∈\mathbb{Z}:c∣a∧c∣b⟹c∣d﻿$ (grootste).
-