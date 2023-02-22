Systém pro GE v Pythonu.

## Jak funguje workflow
* Načtou se atributy přes set_params()
*  WTF trackers?
* TODO edit DEBUG na True a VERBOSE na True
* V set_params() se inituje i gramatika
### zpracovani gramatiky BKG
1) Načtení vstupního souboru
2) Přes regex rozsekat soubor na pravidla

self.start_rule = startovni SYMBOL
self.non_terminals = dict s klíči = nonterminály a values je struktura:
{  
    'id': nonterminál (=klíč),  
    'min_steps': maxsize,  
    'expanded': False,  
    'recursive': True,  
    'b_factor': 0
}
			