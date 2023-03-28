> “The main advantage is that individual behaviors
can easily be reused in the context of another higher-level behavior, without needing
to specify how they relate to subsequent behaviors”.

==Ekvivalentní FSM (konečnémuautomatu)==, v [[Behavior trees in robotics and IA.pdf]] jsou důkazy (2.2.1 a 2.2.2)

Node types:
![[Pasted image 20230327122432.png]]
![[Pasted image 20230327122826.png]]
![[Pasted image 20230327124359.png]]
Dekorátor je mimo, ten má user-defined algoritmus

Shrnutí:
![[Pasted image 20230327124343.png]]

![[Pasted image 20230327135132.png]]

## Pruning of Ineffective Subtrees  
Once obtained the BT that satisfies the goal, we can search for ineffective subtrees,  
i.e. those action compositions that are superfluous for reaching the goal. To identify  
the redundant or unnecessary subtrees, we enumerate the subtrees with a Breadth-  
first enumeration. We run the BT without the first subtree and checking whether the  
reward function has a lower value or not. In the former case the subtree is kept, in the  
latter case the subtree is removed creating a new BT without the subtree mentioned.  
Then we run the same procedure on the new BT. The procedure stops when there  
are no ineffective subtree found. This procedure is optional.

-> AG by měla pomoct!