2019, IJCAI-19 conference

Rozhodně se podívat na Jones et. al (2018): **Evolving behaviour trees for swarm robotics**

## GEESE-BT
GEESE, ale nad BT :)

## Grammar
28 behavior primitives - HUGEEEEE search space. BUT I have something they don't - attributes!



## Fitness function types
#### Type I: Diversity
* Only during evolution itself
* Problem what genome from new generation is good. Simulation of all individuals is a bullshit due to complexity -> need to use heuristics
* Working principle:
	* Extract all nodes and save them to a Python dict
	* diversity = total number of unique behavior nodes divided total behaviors in the grammar (13 behavior nodes of 6 types and grammar has 28 primitives -> diversity fitness is 6/28)
* Compared to Random and simplified (simplified = get-carry-drop behaviors are present): ![[Pasted image 20230322122547.png]]
* !!!!!!! Co takhle zkombinovat simplified (pomocí atributů) s diversity? !!!
#### Type II:  Task-specific
* Three parts: 
	* Task Fitness: klasická task-specific objective funkce
		* Cílem je prostě nějak popsat úkol ve stylu "přineseš papu" = super, "nepřineseš papu" = not super
		* Pro single source foraging prostě počet papu, kolik jich robot zvládl donést
	* Exploration Fitness: 
		* Number of unique locations visited
		* Cíl: odměnit agenty, kteří objevují svět
	* Prospective Fitness:
		* Number of items that agent is carying
		* IDEA: odměňování za vyšší dobro (dobro celku), které ale přímo nepomůže danému jedinic
![[Pasted image 20230322123340.png]]
At ... Fitness II of agent A in time t
beta ... jak hodně řešit předchozí kvalitu
#### Type III: Bootstrap
* Leads to the search space where type II can be used



### Nest maintenance
Úkol, kdy je cílem uklidit okolí hnízda
Real life: úklid sutin, těžba dřeva, vytváření koridorů, technicky i armádní využití (prostřílení se?)


### Behavior sampling
Máme naučenou populaci agentů, kde ale někteří můžou být totální degeni. Co s tím? Behavior sampling, kdy vyberu x procent nejlepších. Překvapivě (pokud to není překlep) nejlépe fungovalo O.1% elitismus


### Závěr
Diversity is the key! (That's what he wrote!)
Problém s prostorem omžných řešení -> na to ale máme atributy! (Ty vole, ono to snad k něčemu bude! PLS!)

