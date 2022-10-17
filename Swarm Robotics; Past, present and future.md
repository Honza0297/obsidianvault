[[Swarm robotics: Past, Present and Future.pdf]]
Autor: mj. Marco Dorigo

Původně používaná [[Stigmergy]]. 

Projekty: [[Swarm-bot]], později [[Swarmanoid]]


Ultimátní cíl swarm robotiky: tooling a metody pro použití swarmů na real-life problémy. Jinak řečeno, abychom mohli hejno nějak vysokoúrovňově programovat pro konkrétní task

NOTE: Co tak zkusit udělat framework pro kiloboty, který by něco takového umožňoval? na vysoké úrovni popsat task základními primitivy
* Find(smth)
* Make circle(somewhere)
* catch(smth)
* ???



Lessons learned/tasks to solve:
* Tasky jsou stále omezené schopnostmi mobilních robotů
* Komunikace je snad nejdůležitější - recognizing peers and their work ([[MAPC]]??)
* Simulátory needed - not my task
* **Micro-macro problem: jak nadesignovat chování hejna (macro), když můžeme programovat jen elementy (micro)?**
	* Různé metody: 20, 21, 50, 52, 65
	* Not powerful enough - adressing just too simple problems
	* Složitý task: hromada podtasků, je třeba komunikace, koordinace a následnost -> neadresuje to [[ALLL]]?! Game theory approach by asi taky mohl pomoct (ve smyslu tvorby koalic atp...)
	* 
* **Security v robot swarms - jinak řečeno, aby se hejno nedalo ovldánout**
	* Toto by taky stálo za zvážení. Pokud vím, nikdo ještě hejno nijak nezabezpečoval a přitom se jedná o poměrně jednoduchý koncept, alespoň na úrovni "prvního kroku" AKA adaptace nějakého současného zabezpečení, třeba ze senzorických sítí. Šla by použít teorie her, kde jsem četl několik článků o "[[Selfish Nodes]]", případně i ten blbý [[blockchain]]
* How to command and control swarm
	* explainability, reasonability...
* Inspirace biologií může být zrádná!
	* Biohejna se vyvíjela sice miliardy let, ale je to jen řešení, na které přišla AI zvaná evoluce. Optimální řešení (z matematického pohledu) by mělo být lepší! Stejně tak jako některé úkoly jsou v přírodě prokazatelně neefektivní, případně vůbec neřešené a my jen biopostupy ohýbáme tak, aby to pasovalo na náš konkrétní problém. Fungovat to může (a často opravdu fugnuje), ale ne nutně optimálně.
* Využití robot swarmů pro modelování živých organismů (aneb Vracení dluhu biologii)
	* Swarm roboti (třeba i ti kiloboti) by šli využít pro modelování přírodních hejn

ARGoS: simulátor pro swarmy, mj i pro kiloboty


New directions (and problems):
* **Micromacro** - cílem je mít jednoduché roboty s jednoduchým chováním, kteří se ale dohromady budou chovat více komplexně. AKA, hejno bude víc než jen součtem svých elementů.
*  **Heterogenita** - Trilobot by třeba mohl nosit dva tři kiloboty :)
* **Decentralizace vs hierarchie** - centralizace je jednodušší, ale vznika jedný point-of-failure. 
	* Teoreticky by to šlo, jako když se v Parnassovi četl Nekonečný příběh: čte jeden, pokud čtenář nemůže dál, automaticky se zvolí další leader (všichni se chtějí domluvit, nechtějí si vůdcovství přisvojit - nemělo by to být zas až tak těžké - když někdo detekuje smrt vůdce a nedostal zprávu o novém, v čase t se prohlásí za vůdce. pokud narazí na dalšího vůdce, porovnají si timestampy, kdo je vůdcem kratší dobu, ten odstupuje?).
	* Understudied - existuje způsob na přepínání (viz níže), ale už ne na jeho zakomponování (AKA kdy hierarch. a kdy self-organ.) 
	*  **N. Mathews, A. L. Christensen, R. O’Grady,  
F. Mondada, and M. Dorigo, “Mergeable nervous  
systems for robots,” Nature Commun., vol. 8,  
no. 1, p. 439, Dec. 2017.**

* **Security** - o tom jsem už psal
	* [98] E. C. Ferrer, T. Hardjono, M. Dorigo, and  
A. S. Pentland, “Secure and secret cooperation in  
robotic swarms,” 2019, arXiv:1904.09266.  
[Online]. Available: https://arxiv.org/abs/  
1904.09266  
	     * [99] V. Strobel, E. C. Ferrer, and M. Dorigo, “Blockchain  
technology secures robot swarms: A comparison  
of consensus protocols and their resilience to  
Byzantine robots,” Frontiers Robot. AI, vol. 7,  
p. 54, May 2020.

* **Swarm human interaction**
* **General criterie for swarm solutions**
* **(Koordinace, komunikace)** - toto sem přidávám já, protože si myslím, že v tom jsou mezery. Jak komunikovat? Co měnit? Co robot potřebuje předat a co ne? Tolik otázek... :)


**NOTE:** stále se točíme kolem komunikace. někde na str 9/15 se píše i o tom, jak by se měla měnit strategie. Příkladem je to, když jeden jedinec zmerčí predátora, zdrhne celé heno. POdobným způsobem by se mohly předávat informace i v umělém hejnu. - je tenhle nápad k něčemu vůbec? Možná jo. Situace:  Kilobot "hlídka" je vpředu a uvidí překážku/slepou chodbu. v tu chvíli bude vysílat nějaký "tvrdý" signál "tudy ne" a ostatní půjdou jinudy. (Ehm, něco se mi na tom nelíbí, ale nevím co)

**NOTE**: velmi nedovařený nápad na chování: roboti jako jednotlivci (asi) ví, co je v prostředí čeká (jaké elementární tasky). V [[MAPC]] by to bylo třeba tahání kostiček, střílení, ničení překážek. Každý robot by tedy měl nějaké defaultní chování spolu se subjektivním (?) hodnocením (to znamená co? jak se mi dařilo předtím? má to i nějakou objektivní metriku jako třeba "počet zničených překážek"?) + nějaké argumenty pro hodnocení (jaké? jak by to fungovalo? Třeba "za posledních 100 kol jsem zabil 15 soupeřů"?). Při kontaktu by si roboti mohli říct něco ve stylu "hele, jak ty ničíš překážky?" a vzájemně by si porovnali svoje vzorce chování a třeba si je navzájem upravili.  Vzniklo by z toho i jakési "celkové chování" složené z těchle jednotlivých "modulů"/chování pro elementární task, které by postupně zkonvergovalo do nějaké "třídy chování" jako třeba střelec, ničitel, tahač kostek... 
* Problémy, co vidím na první pohled: 
	* nevznikne "vyšší koordinace", nebo to tam aspoň nevidím. Budou pouze krystalizovat třídy (viz výše) ideální pro konkrétního (byť třeba homogenního) elementa (každý má ale za sebou různou historii, tak by teoreticky mohla být i víc než jedna "ideální"), ale nevznikne koordinované chování jako "tahač kostek by měl mít kamaráda ničitele a kamaráda střelce". -> To by ale mohla řešit tvorba koalic!!!
* Něco na ten způsob je (asi) tohle: E. Ferrante, A. E. Turgut, E. Duéñez-Guzmán,  
M. Dorigo, and T. Wenseleers, “Evolution of  
self-organized task specialization in robot  
swarms,” PLOS Comput. Biol., vol. 11, no. 8,  
Aug. 2015, Art. no. e1004273

[[Kilobot]]i
zdroje:
30: M. Rubenstein, C. Ahler, N. Hoff, A. Cabrera, and  
R. Nagpal, “Kilobot: A low cost robot with scalable  
operations designed for collective behaviors,”  
Robot. Auton. Syst., vol. 62, no. 7, pp. 966—975,  
2014, reconfigurable Modular Robotics. [Online].  
Available: http://www.sciencedirect.com/science/  
article/pii/S0921889013001474

32: G. Valentini, E. Ferrante, H. Hamann, and  
M. Dorigo, “Collective decision with 100 kilobots:  
Speed versus accuracy in binary discrimination  
problems
33: I. Slavkov et al., “Morphogenesis in robot  
swarms,” Sci. Robot., vol. 3, no. 25, 2018
**34: M. S. Talamali, T. Bose, M. Haire, X. Xu,  
J. A. R. Marshall, and A. Reina, “Sophisticated  
collective foraging with minimalist agents:  
A swarm robotics test,” Swarm Intell., vol. 14,  
no. 1, pp. 25—56, Mar. 2020**

59] A. Reina, A. J. Cope, E. Nikolaidis,  
J. A. R. Marshall, and C. Sabo, “ARK: Augmented  
reality for kilobots,” IEEE Robot. Autom. Lett.,  
vol. 2, no. 3, pp. 1755—1761, Jul. 2017.  
[60] G. Valentini et al., “Kilogrid: A novel experimental  
environment for the Kilobot robot,” Swarm Intell.,  
vol. 12, no. 3, pp. 245—266, Sep. 2018
