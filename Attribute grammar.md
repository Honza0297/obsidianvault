[[Attribute_grammar.pdf]] Knuth 1968

Moje trochu upravená definice, protože v 60. letech se evidentně nepoužívalo T, N pro terminály a nonterminály, ale V a N pro kompletní slovník (Vocabulary) a noneterminály N


G = (N, T, P, S, A)
N ... konečná neprázdná množina nonterminálů
T ... konečná množina terminálů
S ... S in N, startovní neterminál
P ... N -> (N U T), konečná množina pravidel
A ... konečná množina dvojic množin(1) A(X) definovaných následovně: A(X) = (Ai(X), As(X)), Ai(X) je množina inherited atributů znaku X, As(X) je množina syntetizovaných atributů znaku X pro všechny X z (N U T).
Dále: Ai(S) = {}.  As(t) = {} pro všechny terminály t z T

Atributy:
* Syntetizované: získané od potomků 
	* Např: B -> LR, B.val = L.val + R.val
* Inherited (zděděné):
	* Např: X -> Aa, A.len = X.len - 1 (a nemá atributy) 


(1) ble. Ve zkratce: A je množina dvojic, třeba A = {(Ai1, As1), (Ai2, As2)}. Axn je potom sama o sobě množina samotných atributů