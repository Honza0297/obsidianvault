[[christiansen_ortega_ITEC_2007_ps.pdf]]

Úprava [[Attribute grammar]], kde první atribut každého symbolu (?) je "Christiansenova gramatika" **IMHO chyba**, má tam být, že prvním atributem je množina všech aplikovatelných pravidel na daný symbol. 

* Nonterminály jsou zapisovány následovně: \<nonterm\>(atr1->, atr2<-......)
	* -> znamená, že atribut je inherited/zděděný (správně to má být šipka dolů)
	* <- je pro syntetizovaný atribut (správně šipka nahoru)
* V derivačních pravidlech jsou jména atributů implicitní, podobně jako v Prologu:
	*  Máme nonterminály \<n\>(a->),  \<n2\>(b->)
	*  \<n\>(a->) -> \<n2\>(a->){} znamená, že hodnota atributu a se kopíruje do b (kdyby byly šipky naopak, tak se i kopíruje naopak)
	* Do složených závorek {} se poté zapisují další semantické akce, na teré nestačí prosté přiřazení, zpravidla pomocí pseudokódu 
Celkově už dosti složité na můj vkus a nevidím tam tu výhodu jako u atributových gramatik...
Ukončeno na straně 2. 