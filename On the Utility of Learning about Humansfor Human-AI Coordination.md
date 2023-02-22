[[On the Utility of Learning about Humans.pdf]]

**O čem to je**: Paper řeší, že současné algoritmy trénování agentů stojí často na tom, že agenti "hrají danou hru" = řeší danou úlohu proti sobě - nebo spolu, pokud je kooperativní (a  tím pádem předpokládají stejně kvalitního soupeře/pomocníka). Člověk se ale vždy nechová racionálně a agenti potom při spolupráci s člověkem mají výrazně horší výsledky. Při hraní proti němu naopak ještě lepší, než čekali. Důvod je stejný, člověk není v dané hře tak dokonalý jako agent.  
Navrhované řešení: trénování agenta s/proti "proxy člověku" = modelu, který se chová podobně jako člověk.

Cíl:
* Natrénovat agenty způsobem self-play, population based training a pak proti "člověka simulujícímu modelu"

Výsledky:

* Agenti, kteří trénovali proti/s proxy člověkem, poté dosahovali lepších výsledků i s reálným člověkem.

Závěr: Pokud mají agenti spolupracovat s člověkem, musí se to zohlednit už během tréninku. A stačí i nedokonalý model chování člověka - stále lepší něco než nic. 


Poznámky
* Proxy člověk byl trénovaný pomocí **behavioral cloning** - jednoduše se modelu ukázalo množství dat o tom, jak by se choval člověk, a ten se na tom natrénoval.
* Testování probíhalo na hře, která připomínala *Overcooked*. Jde o to, že na hracím plánku je hrnec, cibule, talíř a výdejní okénko. Cílem je vhodit do hrnce 3 cibule, udělat polévku, vzít talíř, nalít do něj polévkua donést ho k okénku. To vše pokud možno co nejrychleji/co nejvíckrát za daný čas. Fígl je v tom, že na ploše jsou dva agenti a často např. jen jeden z nich má přístup k talířům a cibuli a/nebo je má výrazně blíž než ten druhý...
* 