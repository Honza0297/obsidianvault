[[2018-Information_exchange_design_patterns_for_robot_swarm_foraging_and_their_application_in_robot_control_algorithms.pdf]]

2018, Pitonakova

Využívá [[ICR framework]]. Primárně pro [[foraging]].
Cílem je popsat design patternem:
1) Chování robota včetně závislostí
2) Identifikovat vlastnosti tohoto chování včetně vhodnosti pro daný task
3) Vše nějak modularizovaně

2.1 jen prolétnuta

[[BDRML]] Behavior-Data Relations Modelling Language použitý k popisu design patternů/chování. 

[[ICR framework]] 

IMHO to asi nepopisuje, které informace vyměňovat...

Jednotlivé design patterny:
1) Individualista - robot ignoruje hejno, sám si hledá worksite a sám pracuje
	- Nešíří se špatné informace (bo se nešíří žádné :)), jednoduché
	- Informace jdou obstarat jen z okolí (vidím kolegu, jak něco kope - asi má důvod? nepůjdu kopat taky?)
	- Neefektivní
2) Broadcaster
	* Robot šíří informaci o worksite a snaží se rekrutovat ostatní, aby mu pomohli
	* Displacement a reallocation costs pro nové roboty, původní robot musí vědět, jestli má rekrutovat další...
3) Information storage
	* Komunikace přes prostředí, ale aktivní - pohození RFID tagu, stacionnární robot jako feromon...
4) Information exchange anywhere
	* 2 a 3 zároveň 
5) 4) ale jen blízko worksite
6) Centrální informační středisko
	* Existuje informační centrum, kde roboti dostaanou info


Diskuze
---
Tohle počítá s nějakou předprogramováním robotů - asi to není to, co chci.



