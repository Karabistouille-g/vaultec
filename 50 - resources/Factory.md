---
tags:
  - informatique
  - conception-objet
  - patron-conception
---
> [!bookmark|center] [[Conceptions Objets]]

> [!info] Sujet lié
> - [[Singleton]]

# Définition
Création d'une classe qui permet d'instancier d'autre classe en fonction des paramètres données. Comme les fabriques sont généralement unique, on utilise souvent le patron singleton pour gérer leur création.

# Implémentation
```java
public class FabriqueHTMLElement {

	public HTMLElement create(String type) throws ExceptionCreation {
		if (type.equals("div")) {
			return new HTMLDivElement();
		}
		if (type.equals("p")) {
			return new HTMLParagrapheElement();
		}
		if (type.equals("img")) {
			return new HTMLImageElement();
		}
		throw new ExceptionCreation("Impossible de créer un type " + type);
	}
}
```

