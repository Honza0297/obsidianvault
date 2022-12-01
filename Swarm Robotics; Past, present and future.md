git@github.com:Honza0297/obsidianvault.git[[Swarm robotics: Past, Present and Future.pdf]]
Autor: mj. Marco Dorigo

Původně používaná [[Stigmergy]]. 

Projekty: [[Swarm-bot]], později [[Swarmanoid]]


**Ultimátní cíl swarm robotiky: tooling a [[IDEA Framework pro swarm robotiku]] pro použití swarmů na real-life problémy. Jinak řečeno, abychom mohli hejno nějak vysokoúrovňově programovat pro konkrétní task**


**Lessons learned/tasks to solve:**
* Tasky jsou stále omezené schopnostmi mobilních robotů
* Komunikace je snad nejdůležitější - recognizing peers and their work ([[MAPC]]??)
* Simulátory needed - not my task
* **Micro-macro problem: jak nadesignovat chování hejna (macro), když můžeme programovat jen elementy (micro)?**
	* Různé metody: 20, 21, 50, 52, 65
	* Not powerful enough - adressing just too simple problems
	* Složitý task: hromada podtasků, je třeba komunikace, koordinace a následnost -> neadresuje to [[ALLL]]?! Game theory approach by asi taky mohl pomoct (ve smyslu tvorby koalic atp...)
* **Security v robot swarms - jinak řečeno, aby se hejno nedalo ovldánout**
	* Toto by taky stálo za zvážení. Pokud vím, nikdo ještě hejno nijak nezabezpečoval a přitom se jedná o poměrně jednoduchý koncept, alespoň na úrovni "prvního kroku" AKA adaptace nějakého současného zabezpečení, třeba ze senzorických sítí. Šla by použít teorie her, kde jsem četl několik článků o "[[Selfish Nodes]]", případně i ten blbý [[blockchain]]
* How to command and control swarm
	*  Zase micro vs macro problem
	* explainability, reasonability...
* Inspirace biologií může být zrádná!
	* Biohejna se vyvíjela sice miliardy let, ale je to jen řešení, na které přišla AI zvaná evoluce. Optimální řešení (z matematického pohledu) by mělo být lepší! Stejně tak jako některé úkoly jsou v přírodě prokazatelně neefektivní, případně vůbec neřešené a my jen biopostupy ohýbáme tak, aby to pasovalo na náš konkrétní problém. Fungovat to může (a často opravdu fugnuje), ale ne nutně optimálně.
* Využití robot swarmů pro modelování živých organismů (aneb Vracení dluhu biologii)
	* Swarm roboti (třeba i ti kiloboti) by šli využít pro modelování přírodních hejn

[[ARGoS]]: simulátor pro swarmy, mj i pro kiloboty

**New directions (and problems):**
* **Micromacro** - cílem je mít jednoduché roboty s jednoduchým chováním, kteří se ale dohromady budou chovat více komplexně. AKA, hejno bude víc než jen součtem svých elementů.
*  **Heterogenita** - Trilobot by třeba mohl nosit dva tři kiloboty :)
* **Decentralizace vs hierarchie** - centralizace je jednodušší, ale vznika jedný point-of-failure. 
	* Teoreticky by to šlo, jako když se v Parnassovi četl Nekonečný příběh: čte jeden, pokud čtenář nemůže dál, automaticky se zvolí další leader (všichni se chtějí domluvit, nechtějí si vůdcovství přisvojit - nemělo by to být zas až tak těžké - když někdo detekuje smrt vůdce a nedostal zprávu o novém, v čase t se prohlásí za vůdce. pokud narazí na dalšího vůdce, porovnají si timestampy, kdo je vůdcem kratší dobu, ten odstupuje?).
	* Understudied - existuje způsob na přepínání (viz níže), ale už ne na jeho zakomponování (AKA kdy hierarch. a kdy self-organ.) 
	*** Dorigo:  Mergeable nervous systems for robots**

* **Security** - o tom jsem už psal
	* 98 Ferre, Dorigo Secure and secret cooperation in robotic swarms  
	 * 99 Strobel, Ferrer, Dorigo Blockchain technology secures robot swarms: A comparison of consensus protocols and their resilience to Byzantine robots
* **Swarm human interaction**
* **General criterie for swarm solutions**
* **(Koordinace, komunikace)** - toto sem přidávám já, protože si myslím, že v tom jsou mezery. Jak komunikovat? Co měnit? Co robot potřebuje předat a co ne? Tolik otázek... :)


**NOTE:** [[IDEA Komunikace ve swarmech]] 

**NOTE**: [[IDEA Způsoby chování, jeho výměna a diferenciace]]
* Něco na ten způsob je (asi) tohle: [[Evolution of Self-Organized Task Specialization in Robot Swarms]] (Ferrante, Dorigo)

[[Kilobot]]i 
- "spodní hranice" pro swarm roboty. Prostě extrémně jednoduší, díky tomu jich může být hodně.
Zdroje:
* 30: Rubenstein: Kilobot: A low cost robot with scalable operations designed for collective behaviors  http://www.sciencedirect.com/science/article/pii/S0921889013001474
* 32: Valentini: [[Collective decision with 100 Kilobots]]
* 33: Slavkov et al.: Morphogenesis in robot swarms
* 34: Talamali: Sophisticated collective foraging with minimalist agents:  A swarm robotics test
Taky se tu zmiňovaly různé tooly pro [[Kilobot]]y
