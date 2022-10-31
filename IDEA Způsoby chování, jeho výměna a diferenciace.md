Při čtení [[Swarm Robotics; Past, present and future]]
velmi nedovařený nápad na chování: roboti jako jednotlivci (asi) ví, co je v prostředí čeká (jaké elementární tasky). V [[MAPC]] by to bylo třeba tahání kostiček, střílení, ničení překážek. Každý robot by tedy měl nějaké defaultní chování spolu se subjektivním (?) hodnocením (to znamená co? jak se mi dařilo předtím? má to i nějakou objektivní metriku jako třeba "počet zničených překážek"?) + nějaké argumenty pro hodnocení (jaké? jak by to fungovalo? Třeba "za posledních 100 kol jsem zabil 15 soupeřů"?). Při kontaktu by si roboti mohli říct něco ve stylu "hele, jak ty ničíš překážky?" a vzájemně by si porovnali svoje vzorce chování a třeba si je navzájem upravili.  Vzniklo by z toho i jakési "celkové chování" složené z těchle jednotlivých "modulů"/chování pro elementární task, které by postupně zkonvergovalo do nějaké "třídy chování" jako třeba střelec, ničitel, tahač kostek... 
* Problémy, co vidím na první pohled: 
	* nevznikne "vyšší koordinace", nebo to tam aspoň nevidím. Budou pouze krystalizovat třídy (viz výše) ideální pro konkrétního (byť třeba homogenního) elementa (každý má ale za sebou různou historii, tak by teoreticky mohla být i víc než jedna "ideální"), ale nevznikne koordinované chování jako "tahač kostek by měl mít kamaráda ničitele a kamaráda střelce". -> To by ale mohla řešit tvorba koalic!!!
* * Něco na ten způsob je (asi) tohle: [[Evolution of Self-Organized Task Specialization in Robot Swarms]]
* Podobně vlastně fungovaly Portie v Dětech času - předávaly si genetické balíčky zkušeností, což jim umožnilo extrémně rychlý rozvoj, i když žily čtvrtinu lidského života.
a neglected aspect in the consideration of potential effects artificial generala neglected aspect in the consideration of potential effects artificial general
IDEA: co kdyby jedinci, kteří dlouhodobě "prohrávají" ve výměně chování (jejich chování je dlouhodobě "horší" a oni pořád přejímají nová) měli větší šanci na mutaci? Způsobí to normalizaci, nebo jen feedback loop a bude to horší?

IDEA: Výměna chování by mohla probíhat jen "pravděpodobnostně" - čím je chování lepší oproti mému, tím víc pravděpodobná bude výměna/nahrazení, ale ne nutně 100%


Zdroje na jednom místě: 
* [[An Evolutionary Perspective on Self-Organized Division of Labor in Social Insects]] (ještě nčeteno)
* [[Evolution of Self-Organized Task Specialization in Robot Swarms]] 
* [[2018-Information_exchange_design_patterns_for_robot_swarm_foraging_and_their_application_in_robot_control_algorithms.pdf]]