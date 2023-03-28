[[evolving behavior trees for swarm robotics.pdf]]

Z roku 2016, využití [[Behavioral Trees]] pro [[Kilobot]]y

Proč BT: srozumitelný, modulární

Všichni kiloboti stejný kód - už teď víme, že to nemusí být ideální.

Zdroje:
(1): obecné kecy o swarm robotics? podívat se, co to bude
	* je to [[Swarm robotics: a review from the swarm engineering perspective.pdf]]
	* už jsem to četl, ale asi z toho nemám poznámky 
(3): něco o sr, worth check)
	* Z ROKU 2005: [[Swarm robotics: From sources of inspiration to domains of application..pdf]], strany 10-20
(7): survey on the state of automatic
	[[automatic design of robot swarms.pdf]]
(14): Dk, že FSM -> BT. JDE TO I OBRÁCENE?
	* ten dk jsem tam nenašel... whatever, skip
(15): zmiňují se "fundamental properties of nature". WTF? čeknout
swarm controller generation
	* [[The evolutionary origins of modularity.pdf]] 
==NOTE: BT jsou modulární (můžu přesouvat celé subtrees). Co kdybych místo evoluce stromku evolvoval stromek právě z těchle subtrees? Dal bych tam ta základní primitiva a další by se přidávala on the fly.  ==

> One problem with automatic generation of swarm controllers is that of boot-
strapping; it is difficult to devise fitness functions to get complex behaviours (8, 9),
the evolutionary process will often get stuck in uninteresting local maxima.

==Ogren (14) shows that all FSM can be represented by BT ==

interface mezi controllerem (BT) a robotem: blackboard, kde si BT čte values a do jiných zapisuje. Underlying soft už potom vykonává low level řízení
![[Pasted image 20230327104423.png]]
