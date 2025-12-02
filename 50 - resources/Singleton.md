---
tags:
  - informatique
  - conception-objet
  - patron-creation
---
> [!bookmark|center] [[Science informatique]]

> [!info] Sujet lié
> - Note 1
> - Note 2

# Définition
Une classe singleton est une classe qui doit s'instancier une seule et unique instance. Cette classe implémente une méthode qui instancie l'objet si il n'existe pas déjà, sinon renvoie une référence vers l'objet en question.

# Implémentation
```java
public class CSingle {
	
	private static CSingle INSTANCE = null;
	
	// Constructeur privé
	private CSingle() { }
	
	// Retourn l'instance
	public synchronized static CSingle getInstance() {
		if (INSTANCE == null) {
			INSTANCE = new CSingle();
		}
		return INSTANCE;
	}
}
```
