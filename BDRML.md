3 typy design primitiv:
1) Behavior: set procesů, které pokrývají nějakou situaci (hledej, zatoč, jeď rovně)
2) Interní struktura dat - info, uložené v robotovi (tam, kam jedu, nevím o zdi)
3) Externí struktura dat - info mimo robota (kolega tam o žádné stěně neví)


Relations na propojení primitiv:
1) Transition z jednoho chování do druhého
2) Read/Write Internal data
3) Send/Recv External data
4) Copy
5) Update (např. feromon level)

Chování/operace může nastat jen za nějaké podmínky, obecně definovaná funkcí -> {True, False} - "no wall", f(x,y,...),  atd.