[[GESwarm.pdf]]
Paper o [[Grammatical Evolution]] pro swarmy z roku 2013 - docela starý :(

Na rodzíl od neuronek lze takto vytvořená chování analyzovat, reverznout atp...
Pravidla ve tvaru: R = P X B X A
* Pokud jsou splněny všechny preconditions P... -> offtopic: splnitelnost formulí je [[SAT problém]] :) Asi to je k ničemu, ale SAT je NP-úplný a třeba mě někdy myšlenkové pochody zavedou někam tímhle směrem splnitelnosti podmínek - takže ne, budoucí Honzo, SAT problém.
* ...a zároveň robot vykonává nějaké chování z B...
* ... jsou vykonány všechny akce z A. Akcí je i přepnutí chování - teoreticky tedy akce může být přímo chováním, kde dané nové chování nahradí to staré. To je ale jen syntactic sugar. 

![[Pasted image 20221030113641.png]]


>The evolved individual behavior is a set
of rules responsible for switching from one low-level behavior
to another in response to internal states and local environ-
mental conditions.

=> Robot = jedinec má svoje individuální chování složené z více pravidel, které se starají o přepínání stavů

Geswarm gramatika G = {N, T, P, S}
N: list pravidel R, list akcí, list chování, list podmínek, pravidlo, "nějaká akce", "nějaké chování" nějaká podmínka
T:  konkrétní akce Ax , konkr. chování Bx, konkr podmínka Px
P: pravidla, viz hore
S: start

Jak funguje evoluce
---
řetězec = list pravidel. V té původní gramatice na obrázku ovšem chybí oddělovače, takže řešení by potom mohlo vypadat třeba takhle:
P1P2B1B3B5A2P3B1A2A3A4P5B4A1A2

-> např "(R -> P1 and P2; B1; A1),(R->;B2;A2)" - toto je jeden řetězec = kandidátní řešení
	-> Přesněji, výsledek by byl jen P1P2B1A1εB2A2 :) 
