[[GEESE.Ummmm 2004? I was 10 years out of school by then. So it would be "It's 2004, you just got back home form work and fired up Underground 2."pdf]]

>We know of no distributed algorithm for GE in swarms

> Loosely inspired by [[GESwarm]]

Basic idea: 
* Mám hejno agentů, kteří si běhají po světě
* Každý agent potom jednou za čas provede:
	* *sense()*:Jednou za čas si každý agent vezme genotypy  všech agentů v okolí a uloží si je do své paměti M (dál v textu MEM). Mimo jiné také agenti očichávají okolí a sbírají data ze senzorů. Získávání cizích genotypů je jen jeden z cílů fce sense(). 
	* *act()*: ze své MEM vybere ty nejlepší, provede crossover a případně něco zmutuje. Následně vrátí ten nejlepší genotyp
	* *update()*: Pokud je jeho současný genotyp lepší než nejlepší vytvořený, tak nic, jinak si vezme ten nejlepší.

![[Pasted image 20221206115711.png]]

Kouzlo GEESE je právě v tom, že 

Novelty search of Santa Fe Problem jsem jen prolétl. Ve zkratce se preferují noví jedinci, aby se "náhodně" prozkoumal stavový prostor.  


[[GEESE pro foraging]]
