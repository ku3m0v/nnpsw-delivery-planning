# NNPSW – Delivery Planning

Semestrální projekt v rámci předmětu **KST/NNPSW** zaměřený na analýzu informačního systému pro správu firemních vozidel a plánování dodávek zákaznických objednávek.

Hlavním cílem první etapy projektu je **plánování dodávek objednávek**, kontrola dostupnosti vozidel, jejich přepravní kapacity a zabránění konfliktním rezervacím.

## Organizace práce

Úkoly v rámci projektu evidujeme a rozdělujeme pomocí Trello:

👉 [Trello – Cinazes](https://trello.com/invite/b/6ac7875a20c978b0a22ad65d/ATTI57d0a0857b720121b6c615207fe8997b5B62DAF6/cinazes)

GitHub slouží především pro ukládání a verzování projektové dokumentace, analytických modelů a diagramů.

## Dokumentace

Projektová dokumentace bude vytvářena pomocí **AsciiDoc**.

AsciiDoc používá textové soubory s příponou `.adoc`, díky čemuž lze všechny změny dobře verzovat pomocí Gitu a v GitHubu jednoduše zobrazit rozdíly mezi jednotlivými verzemi dokumentů.

Dokumentace bude obsahovat například:

- zadání projektu,
- požadavky,
- výsledky analýzy,
- popisy aktérů,
- Use Case scénáře,
- analytický model,
- další projektovou dokumentaci.

## Diagramy

Pro tvorbu UML diagramů budeme používat **PlantUML**.

Diagramy jsou zapisovány jako text do souborů `.puml`. Díky tomu lze stejně jako u dokumentace pomocí Gitu sledovat konkrétní změny v diagramech.

PlantUML bude používán například pro:

- Use Case diagramy,
- diagramy tříd,
- sekvenční diagramy,
- stavové diagramy,
- diagramy aktivit.

## VS Code

Dokumentaci i diagramy je možné vytvářet přímo ve **Visual Studio Code**.

Pro pohodlnou práci je potřeba do VS Code nainstalovat rozšíření:

- **AsciiDoc** – editace a náhled `.adoc` dokumentů,
- **PlantUML** – editace a náhled `.puml` diagramů.

Git je ve VS Code přímo podporován a lze zde zobrazovat změny, vytvářet commity, pracovat s větvemi a porovnávat jednotlivé verze souborů.

Pro lokální vykreslování PlantUML může být podle konfigurace rozšíření potřeba také **Java** a **Graphviz**.

## Navrhovaná struktura repozitáře

```text
nnpsw-delivery-planning/
│
├── README.md
│
├── docs/
│   ├── zadani.adoc
│   ├── pozadavky.adoc
│   ├── analyza.adoc
│   └── use-cases/
│
├── diagrams/
│   ├── use-case.puml
│   ├── class-diagram.puml
│   ├── activity-diagram.puml
│   └── sequence-diagram.puml
│
└── meetings/
    └── ...
```

Struktura se může v průběhu projektu podle potřeby dále upravovat.
