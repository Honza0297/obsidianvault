[[Collective decision with 100 Kilobots.pdf]]
Video: https://www.youtube.com/watch?v=5lz_HnOLBW4

2015, poměrně dost citovaný (119 dle researchgate)
**Abstrakt**:
>Achieving fast and accurate collective decisions with a large number of simple  agents without relying on a central planning unit or on global communication is essential  for developing complex collective behaviors. In this paper, we investigate the speed versus  
accuracy trade-off in collective decision-making in the context of a binary discrimination  problem—i.e., how a swarm can collectively determine the best of two options. We describe  
a novel, fully distributed collective decision-making strategy that only requires agents with  
minimal capabilities and is faster than previous approaches. We evaluate our strategy xperi-  
mentally, using a swarm of 100 Kilobots, and we study it theoretically, using both continuum  
and finite-size models. We find that the main factor affecting the speed versus accuracy  
trade-off of our strategy is the agents’ neighborhood size—i.e., the number of agents with  
whom the current opinion of each agent is shared. The proposed strategy and the associated  theoretical framework can be used to design swarms that take collective decisions at a given  level of speed and/or accuracy."*

X MAS, roboti ve swarmu jsou často málo informovaní, asynchronní...
Přenáší se ne kompletní info, ale jen "pozitivní feedback" (10)
**Strategie DMMD**:  Direct Modulation of Majority-based Decisions z (47). Funguje to tak, že agenti ukazují svůj názor takovou dobu, jak kvalitní se jim zdá. Rozhodování je potom majoritní - agent přijímá názor většiny svých sousedů. Inspired by [[social insects]]

Zmíněny reputation algoritmy jako prostředek k rozhodování - nejsou ale primárně pro rozhodování mezi dvěma možnostmi. 

Princip:
* Dvě možnosti a,b s kvalitou p_{a, b}
* Každý agent je ve stavu 
	* "diseminace" = aktivně hlásí svůj názor (= preference a X b) všem svým sousedům, kteří taky diseminují. Čas diseminace je poměrný tomu, jak kvalitní je daná možnost (lepší = delší čas). Btw, diseminace = "rozšiřování ložisek procesu", zpravidla negativní :)
	* exploration - zkoumá okolí dle svého názoru
	* projde všechny získané názory včetně svého současného a jeho nový názor bude ten častější. Přepočítává také kvalitu názoru. A v neposlední řadě se podle něj chová (třeba zkoumá danou cestu...)

Přeskočil jsem teorii a modely