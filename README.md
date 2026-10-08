# NNPSW – Delivery Planning

Semestrální projekt v rámci předmětu **KST/NNPSW** zaměřený na analýzu informačního systému pro správu firemních vozidel a plánování dodávek zákaznických objednávek.

Hlavním cílem první etapy projektu je **plánování dodávek objednávek**, kontrola dostupnosti vozidel, jejich přepravní kapacity a zabránění konfliktním rezervacím.

## Organizace práce

Úkoly v rámci projektu evidujeme a rozdělujeme pomocí Trello:

[Trello – Cinazes](https://trello.com/invite/b/6ac7875a20c978b0a22ad65d/ATTI57d0a0857b720121b6c615207fe8997b5B62DAF6/cinazes)

GitHub slouží pro ukládání a verzování projektové dokumentace, analytických modelů, UML diagramů a dalších artefaktů vznikajících během analýzy.

## Používané nástroje

### AsciiDoc

Projektová dokumentace je vytvářena pomocí **AsciiDoc**.

Dokumenty jsou ukládány jako textové soubory s příponou `.adoc`. Díky tomu lze změny jednoduše verzovat pomocí Gitu a na GitHubu zobrazit konkrétní rozdíly mezi jednotlivými verzemi dokumentů.

AsciiDoc používáme například pro:

- zadání projektu,
- požadavky,
- výsledky analýzy,
- popisy aktérů,
- Use Case specifikace,
- scénáře,
- slovník pojmů,
- analytickou dokumentaci,
- projektový plán.

### PlantUML

Pro tvorbu UML diagramů používáme **PlantUML**.

PlantUML diagramy jsou zapisovány jako text do souborů `.puml`. Díky tomu lze změny v diagramech stejně jako u dokumentace jednoduše sledovat pomocí Gitu.

PlantUML budeme používat například pro:

- Use Case diagramy,
- diagramy tříd,
- sekvenční diagramy,
- stavové diagramy,
- diagramy aktivit.

Diagramy jsou z `.puml` souborů exportovány do formátu **SVG**. Vygenerovaný SVG soubor je následně možné vložit přímo do AsciiDoc dokumentace.

Tímto způsobem zůstává zdroj diagramu textový a dobře verzovatelný, ale v dokumentaci je zároveň vidět jeho grafická podoba.

## Visual Studio Code

Dokumentaci i diagramy je možné vytvářet přímo ve **Visual Studio Code**.

Pro pohodlnou práci je potřeba nainstalovat následující rozšíření:

1. **AsciiDoc** – editace a náhled `.adoc` dokumentů,
2. **PlantUML** – editace, náhled a export `.puml` diagramů.

AsciiDoc dokument lze zobrazit pomocí **AsciiDoc Preview**.

PlantUML diagram lze zobrazit pomocí **PlantUML Preview**.

Git je ve VS Code přímo podporován a lze zde zobrazovat změny, vytvářet commity, pracovat s větvemi a porovnávat jednotlivé verze souborů.

## Struktura repozitáře

Aktuální struktura repozitáře:

```text
nnpsw-delivery-planning/
│
├── README.md
│
├── docs/
│   └── zadani.adoc
│
├── diagrams/
│   └── ...
│
├── examples/
│   ├── example.adoc
│   └── example-use-case.puml
│
└── out/
    └── examples/
        └── example-use-case/
            └── example-use-case.svg
```

### `docs/`

Obsahuje hlavní projektovou dokumentaci.

Aktuálně se zde nachází:

- `zadani.adoc` – aktuální zadání semestrální práce.

V průběhu projektu zde budou přibývat další dokumenty související s analýzou systému.

### `diagrams/`

Složka je určena pro skutečné UML diagramy projektu.

Budou zde uloženy například:

- Use Case diagram,
- analytický diagram tříd,
- activity diagramy,
- sekvenční diagramy,
- další UML modely.

Zdrojové diagramy budou ukládány jako `.puml` soubory.

### `examples/`

Obsahuje ukázkové soubory, které slouží jako jednoduchý návod pro členy týmu.

#### `example.adoc`

Ukázkový AsciiDoc dokument.

Obsahuje příklady:

- nadpisů,
- formátování textu,
- seznamů,
- tabulek,
- poznámek a upozornění,
- práce s diagramem,
- vložení vygenerovaného SVG diagramu do dokumentace.

Soubor lze otevřít pomocí **AsciiDoc Preview** a ihned zobrazit jeho výslednou podobu.

#### `example-use-case.puml`

Ukázkový PlantUML Use Case diagram.

Soubor ukazuje základní syntaxi PlantUML:

- definici aktérů,
- definici Use Cases,
- hranici systému,
- vazby mezi aktéry a případy užití.

Diagram lze otevřít pomocí **PlantUML Preview**.

### `out/`

Obsahuje vygenerované výstupy PlantUML.

Například:

```text
out/examples/example-use-case/example-use-case.svg
```

Tento SVG soubor vznikl exportem z:

```text
examples/example-use-case.puml
```

SVG se používá pro zobrazení diagramu přímo uvnitř AsciiDoc dokumentace.

Vygenerované soubory se ručně neupravují. Pokud je potřeba změnit diagram, upraví se příslušný `.puml` soubor a následně se diagram znovu exportuje.

## Jak vygenerovat SVG z PlantUML

Postup ve Visual Studio Code:

1. Otevřít požadovaný `.puml` soubor.
2. Zkontrolovat diagram pomocí **PlantUML Preview**.
3. Stisknout `Ctrl + Shift + P`.
4. Vyhledat příkaz:

   `PlantUML: Export Current Diagram`

5. Zvolit výstupní formát:

   `SVG`

6. PlantUML vytvoří SVG soubor ve výstupní složce `out/`.

Například z:

```text
examples/example-use-case.puml
```

vznikne:

```text
out/examples/example-use-case/example-use-case.svg
```

Po změně `.puml` souboru je potřeba SVG znovu exportovat, aby dokumentace zobrazovala aktuální verzi diagramu.

## Vložení SVG diagramu do AsciiDoc

SVG diagram lze vložit do AsciiDoc dokumentu pomocí:

```adoc
image::../out/examples/example-use-case/example-use-case.svg[Use Case diagram,align="center"]
```

Po otevření dokumentu pomocí **AsciiDoc Preview** se diagram zobrazí přímo v dokumentaci.

## Příklad práce s diagramem

Typický postup:

1. Otevřít nebo vytvořit `.puml` soubor.
2. Upravit zdrojový kód PlantUML.
3. Zkontrolovat výsledek pomocí **PlantUML Preview**.
4. Exportovat diagram do SVG pomocí **PlantUML: Export Current Diagram**.
5. Vložit cestu k SVG souboru do příslušného `.adoc` dokumentu.
6. Výslednou dokumentaci zkontrolovat pomocí **AsciiDoc Preview**.

## Verzování

Hlavní zdrojové soubory projektu jsou textové:

- `.adoc` pro dokumentaci,
- `.puml` pro UML diagramy.

Díky tomu lze pomocí Gitu přesně sledovat:

- kdo změnu provedl,
- co bylo přidáno,
- co bylo odstraněno,
- jak se dokumentace a modely vyvíjely v čase.

Vygenerované SVG soubory slouží především pro grafické zobrazení diagramů v dokumentaci.