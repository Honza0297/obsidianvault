??Jak vlastně probíhalo to rozdělení tasků? náhodně?
IMHO prostě přepnutí chování stálo moc, tak robot radši nepřepínal. JAK SE ALE ROBOT ROZHODL NEBÝT GENERALISTOU? KDE V PROCESU SE TO STALO?

The Information-Cost-Reward framework for  
understanding robot swarm foraging[[Evolution of Self-Organized Task Specialization in Robot Swarms.pdf]]
2015 - téměř určitě už na tom někdo stavěl - kam došli?

>Division of labor is ubiquitous in biological systems, as evidenced by various forms of com-plex task specialization observed in both animal societies and multicellular organisms. Although clearly adaptive, the way in which division of labor first evolved remains enigmatic, as it requires the simultaneous co-occurrence of several complex traits to achieve the required degree of coordination. Recently, evolutionary swarm robotics has emerged as an excellent test bed to study the evolution of coordinated group-level behavior. Here we use this framework for the first time to study the evolutionary origin of behavioral task specialization among groups of identical robots. The scenario we study involves an advanced form of division of labor, common in insect societies and known as “task partitioning”, whereby two sets of tasks have to be carried out in sequence by different individuals. **Our results show that task partitioning is favored whenever the environment has features that, when exploited, reduce switching costs and increase the net efficiency of the group**, and that an optimal mix of task specialists is achieved most readily when the behavioral repertoires aimed at carrying out the different subtasks are available as pre-adapted building blocks. Nevertheless, we also show for the first time that self-organized task specialization could be evolved entirely **from scratch, starting only from basic, low-level behavioral primitives, using a nature-inspired evolutionary method known as [[Grammatical Evolution]]**. Remarkably, division of labor was achieved merely by selecting on overall group performance, and without providing any prior information on how the global object retrieval task was best divided into smaller subtasks. We discuss the potential of our method for engineering adaptively behaving robot swarms and interpret our results in relation to the likely path that nature took to evolve complex sociality and task specialization.


Podle summary a abstraktu je to dost podobné mé myšlence: roboti si automaticky dělí úkoly.

[[IDEA Rychlé přepnutí chování v návaznosti na nečekanou změnu prostředí]] - napadlo mě to při čtení tohoto paperu, zachovávám návaznost

Mj. zmiňuje i to, že pro vývoj diferenciace je nutné/dobré modelovat i **[[task-switching cost]]** (článek zde:https://www.pnas.org/doi/full/10.1073/pnas.1202233109 - z roku 2012, ale info asi platné dále). Switching cost se řeší i zde: [[An Evolutionary Perspective on Self-Organized Division of Labor in Social Insects]], což slouží i jako základ pro celé tohle odvětví.
> Out of these, there is widespread agreement on the role of switching costs and  
positional effects as key factors in promoting task specialization 


Experiment: Roboti transportovali jídlo z vrcholku kopce do hnízda dole. Strategie posílač (stojí na vrchu a hází jídlo z kopce), transportér (jen jezdí mezi úpatím a hnízdem) a generalista (dělá oboje). Robotům to nahoru trvalo dlouho a  dolů museli brzdit, jídlo jelo dolů mnohem rychleji. -> výhodnější bylo použít kopec jako pásový dopravník :)

Ukázalo se, že task partitioning se skutečně může vyvinout denovo jen ze základních chování (phototaxis, random walk...). 
Porovnání predefinovaných chování (robot se měl jen rozhodnout, čím bude) a denovo:
1) Při predef se roboti rozhodili dle fitness funkce (určená pomocí totálního prohledávání nebo jak se to jmenovalo - prostě brute force), když bylo jídlo na rovince, byli všichni generalisté. Při přítomnosti kopce se rozdělili půl na půl mezi posílače a transportéry.  transportéři přitom prohledávali cache pod kopcem, dokud v ní něco nebylo. Skóre: 144 jídla v kopci, 120 na rovině (cca)
2) Původně všichni generalisté, potom se začalo objevovat rozdělování. Bylo ale neúplné, transportéři nikdy nezačali prohledávat cache.  Skóre: 103 v kopci. Nejlepší skupina dosáhla 135 jídla, což je statisticky stejné jako 1)!! - ale rozptyl byl asi 3násobný.
Ve druhém případě opět uplatněna [[Stigmergy]] přes cache (robot lezl nahoru, pokud cestou přes cache doslova nenarazil na jídlo)

Celkově dokázáno, že specializace se může vyvinout jen z behaviorálních primitiv:
- bez rozdělení globálního úkolu
- bez předdefinování chování jiného než základního

>First, from a biological perspective, they yield novel evidence for the adaptive  
benefits of division of labor and the environmental conditions that select for it , provide a  
possible mechanistic underpinning to achieve effective task specialization and task allocation and provide possible evolutionary pathways to complex sociality. 

>Second, from an engineering perspective, our nature-inspired evolutionary method of [[Grammatical Evolution]]  clearly has significant potential as a method for the automated design of adaptively behaving teams of robots. (...) **Division of labor and the environmental conditions that  select for it, our results demonstrated that task partitioning was favored only when features in the environment (in our case a slope)**

>This implies that a combination of **individual experience**, stigmergy and  
stochastic switching alone **were able to generate adaptive task specialization**,


