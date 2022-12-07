[[GEESE.pdf]]


Idea: 
* generuje se list pravidel, jako v GESwarmu
* Pravidla mají strukturu: STATE x PC x TRANSITION
	* STATE: low level behavior (8)
	*  PC: bitové pole 7 *preconditions*: Phas_food, Pon_nest, Pon_source, Pdr op_food, Pwant _food, Pon_signals and Pon_cues. výsledná hodnota se ANDuje,  jinak řečeno, všechny podmínky musí být True nebo dont care, aby pravidlo mohlo být aplikovatelné. 
	* TRANSITION: pstní přechod mezi stavy (6) nebo změna MEM (7)
		* Změna MEM: v MEM jen dva údaje, *wantfood* a *dropfood*. 



Algoritmus:
![[Pasted image 20221206191435.png]]



Konkrétní aplikace [[GEESE]]
_ ![[Pasted image 20221206124920.png]]
![[Pasted image 20221206124911.png]]



[[GESwarm vs GEESE in foraging]]