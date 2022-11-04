Pracovní název: Diferenciace chování v robotích hejnech s využitím GE a <to, co vymýšlím>

Teď se už GE ve swarmech používá: [[Evolution of Self-Organized Task Specialization in Robot Swarms]]. GE v tuhle chvíli funguje jako genetický algoritmus nad gramatikou. 

Můj přístup bude fungovat trochu jinak - chci nahradit genetický algoritmus něčím novým:
* Evoluce bude probíhat přímo v reálném prostředí, inspirovaná principem skutečné evoluce
* Na základě fyzické blízkosti dojde k evolučnímu kroku mezi dvěma jedinci:
	* Jedinci vyberou jedno své chování (pravidlo) a na základě kritérií, která by sama mohla být automaticky generovaná, by došlo k vytvoření nového chování pomocí pravidel genetického algoritmu. Toto nové chování by si nstavili oba jedinci jako prioritní (staré ale ponechali) a určitou dobu ho testovali. Pokud by se ukázalo jako lepší, trvale jím nahradí původní, jinak se k původnímu vrátí.
* Když jedinec testuje nové chování, nemůže dané chování znovu modifikovat 

**Hypotéza: Nahrazení genetického algoritmu explicitní argumentací způsobí, že takto získané chování bude efektivnější než předchozí principy (třeba čistý GESWARM nebo ručně kódované řešení)**



Kritéria kvality chování:
Podle mě by šel genetický algoritmus použít tady - roboti by měli přístup k nějakým údajům o tom, jak které chování používali, 

GE pro swarmy: [[GESwarm]]
 * Máme nějakou gramatiku (viz odkaz)
 * Prvotní chování se vygeneruje náhodně
 * Poté se postupuje genetickým algoritmem
	 * Kříží se stringy, ve kterých jsou zakódovaná pravidla

Co teď dělat do prosince:
- Detailně pochopit:
	- Gramatickou evoluci
	- GESwarm a [[Evolution of Self-Organized Task Specialization in Robot Swarms]]
* Lépe zformalizovat svou představu
	* Konkrétně popsat způsob, jakým by mělo docházet ke vzniku nového chování
	* 