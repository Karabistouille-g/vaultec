---
tags:
  - informatique
  - conception-objet
  - patron-conception
---
> [!bookmark|center] [[Conceptions Objets]]

> [!info] Sujet lié
> - Note 1
> - Note 2

# Définition
Le patron prototype permet d'éviter d'instancier un objet trop volumineux ou consommatrice en temps. Elle copie une première instance déjà créer et apporte les modifications nécessaire à cette copie. Son utilisation se base sur l'implémentation d'une méthode `clone()`. 

# Implémentation
```java
class A implements Cloneable {
	
	int val;
	
	public A (int i) {
		this.val = i;
		this.ressource = ... // opération couteuse en mémoire
	}
	
	public A clone() throws CloneNotSupportedException {
		A r = (A) super.clone();
		r.val = this.valeur;
		r.ressource = this.ressource;
		return r;
	}
}
```

```java
A objA = new A(42);
A cloneA = objA.clone();
```

