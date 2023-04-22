# Product Representation of Finite Abelian Groups

## Theorem
Every finite abelian group is the direct product of cyclic groups

## Proof
The proof is constructive, The following lemma instructs us how to sequentially pick the coordinates of the product.
**Lemma**: Let $H$ be a non-trivial subgroup of a finite group $G$. Then there exists an element $a \in G \setminus H$  such that
$$
(a) \cap H = \{e\}
$$
**proof by picture**
![[Abelian Finite->Products.excalidraw]]

#TBA 

## Discussion
- Where do we require that $G$ is Abelian?
	- Seems like only the the reduction to Sylow-subgroups uses the assumption.
- The construction in Herstein picks elements with decreasing order (in the corresponding quotient group). Seems like it is not necessary. Maybe it's helpful for explicitly finding the next element in the product?