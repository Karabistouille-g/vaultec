---
tags:
  - algorithme
  - informatique
---
> [!bookmark|center] [[Science informatique]]

> [!info] Sujet lié
> - [[Parcours en profondeur (DFS)]]

# Définition
Un algorithme qui permet de parcourir un graphe en parcourant tous les voisins immédiats d'un état avant de passer à l'état suivant. 

![[parcours-bfs.gif]]

# Implémentation
**Temps :** $O(|S| + |A|)$
**Espace :** $O(|S|)$ (pour la file et les marqueurs)
 ```c
 BFS(Graphe G, Sommet s):
	f = createFile()
	f.enfiler(s)
	marquer(s)
	tant que la file est non vide
		s = f.defiler()
		pour tout voisin t de s dans G
			f.enfiler(t)
			marquer(t)
 ```
