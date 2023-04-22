
## Cayley Theorem

**Motivation**: exploring structure of (finite) groups by embedding them in (possibly) small permutation groups. 

**Theorem:** let $H \le G$ a subgroup of a group $G$. Let $S=\{Hx:~x \in G\}$ be the set of right *cosets* of $H$ in G, $A(S)$ the set of permutations over $S$. Define the map $\phi: G \rightarrow A(S)$ by
  $$
 \phi(a) = f_a~~~,~f_a(Hx)=Hxa~.
 $$
Then $\phi$ is a homomorphism whose kernel is equal to the largest normal subgroup of $G$ inside $H$.

**Proof**: The kernel of any homomorphism is normal. Hence, we only need to show that if $H'\le H$ is normal, then $H' \subseteq \mathrm{ker}(\phi)$. Indeed, if $h \in H'$, then for any $g$, 
$$
HgH' = HH'g = Hg 
$$
 
### Implications of Cayley theorem

If $i(H)!<o(G)$ or $o(G) \nmid i(H)!$, the kernel of the above isomorphism is not trivial, i.e., there exists a not-trivial normal subgroup of $G$ inside $H$. 




