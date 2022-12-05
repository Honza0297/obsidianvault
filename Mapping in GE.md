[[Grammatical evolution - new.pdf]] - od str 75
[[Grammatical evolution - new.pdf]] - od str 1

Grammar-based genetic programming: a survey (zdroj 31)
Možnosti:
1) Klasické mapování
3) [[Position Independent Mapping piGE]] - máme dva kodony pro jednu derivaci, jeden určí nonterminál, druhý pravidlo, kterým se rozgenermapováníuje.
4) TAGE

### Klasické mapování (genotype to phenotype mapping)
---
genotyp (kodony) - fenotyp (řetězec/derivační strom): modulo a fixní pořadí, v jakém se rozgenerovávají nonterminály (často levá derivace, jako v první ukázce):
genotyp: 0 263 2 32 42
1) S (start) se rozgeneruje prvním pravidlem (0%cokoli = 0), třeba na AB. Pro A máme 3 pravidla. 
2) 263%3 = 2 -> použijeme poslední pravidlo  na A, vznikne třeba aaB. Jediný další nonterminál je B, pro který máme třeba 2 pravidla.
3) 2%2 = 0, použijeme první pravidlo pro B, vznikne třeba aabb. Derivace u  konce, zbytek genotypu je ocásek (*tail*). 

!!! To horní byl příklad s levou derivací, ale technicky není důvod, proč by nešlo i toto !!!
1) S (start) se rozgeneruje prvním pravidlem (0%cokoli = 0), třeba na AB. Lze použít  3 pravila na A a 2 na B -> 5 pravidel
2) 263%5 = 3 ->použijeme čtvrté pravidlo (první pro B), vznikne třeba Ab. Nyní jen tři pravidla
3) 2%3 = 2, použijeme poslední pravidlo pro A, vznikne třeba ab. Derivace u  konce, zbytek genotypu je ocásek (*tail*). 

Všimni si, že v první (levé) derivaci vzniklo *aabb*, ve druhé *ab*. 

**Degenerování kodonu:**
Snížení jeho hodnoty bez toho, aby se změnilo jeho modulo v konkrétním případě?


### TAGE:
---
Tree adjunct GE
WTF: 33, 35, 36, 37¨Používá Tree adjunct grammars místo BKG
Algoritmus BKG - (L)TAG (Tre Adjunct Grammar) na straně 94 [[Grammatical evolution - new.pdf]]
přeskočeno až na summary a conclusion
* TAGE nemá rádo vysokou aritu v gramatikách, což je případ i mj. [[GESwarm]]u
* 

