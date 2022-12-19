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

Příklad: Gramatika, která generuje jazyk L = {w | \#a(w) = \#b(w)}
N = 
{
	S,
	V(int na, int nb) // na, nb jsou atributy
	X{int na, int nb}
}
T = {a,b}
start = S
R = 
{
	S -> eps
	S -> V {V.na == V.nb ? OK : not OK;} //not OK = error, string nedopadl
	V1 -> XV2 {V1.na = X.na + V.na; 
	                   V1.nb = X.nb + V.nb;}
	X -> a {X.na = 1; 
	            X.nb = 0;}
	X -> b {X.na = 0;
	             X.nb = 1;}
	
}


