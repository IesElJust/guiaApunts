## **Què és Material?**

**Material per Mkdocs** és un tema basat en el disseny Material Design creat per Google, per a llocs web generats amb **Mkdocs**. Material Design és un conjunt de directrius de disseny que se centra en l'ús de l'espai, les animacions suaus i els colors vius per crear una experiència d'usuari coherent i atractiva.

El tema Material per Mkdocs adapta aquestes directrius per a la creació de documentació tècnica, facilitant la personalització i una gran flexibilitat visual. Les seves característiques inclouen:

* Disseny net i modern.
* Suport per a temes clars i foscos.
* Taules de contingut dinàmiques.
* Integració fàcil amb extensions com **Mermaid**, **Admonitions**, i més.
* Compatibilitat amb diferents dispositius, ja que és completament responsive.

## **Com funciona la plantilla?**

El tema **Material** funciona mitjançant un conjunt de plantilles i fulls d'estil que s'integren en el sistema de **Mkdocs**. Quan es configura en el fitxer `mkdocs.yml`, **Mkdocs** utilitza aquests fulls d'estil per renderitzar el lloc web amb el disseny Material.

Per a personalitzar el tema, només cal modificar el fitxer `mkdocs.yml` per configurar opcions com els colors, el disseny, la tipografia o les imatges de fons, entre d'altres. Això fa que el procés de creació de llocs web de documentació siga ràpid i flexible.

## **Requisits previs i instal·lació**

Per treballar amb Material per a Mkdocs partirem de la instal·lació que ja tenim realitzada prèviament en el nostre entorn virtual de Python.

Aixi doncs, partint d'aquesta instal·lació, en primer lloc activem el nostre entorn virtual que vam anomenar mkdocsenv executant:

```bash
source mkdocsenv/bin/activate
```

O bé per als usuaris de Windows:

```bash
mkdocsenv\Scripts\activate
```

!!!tip "Entorn virtual"
    Canvieu el nom mkdocsenv pel nom del vostre entorn virtual en cas que el nom del vostre entorn siga un altre.

Una vegada amb l'entorn activat, instal·lem el tema *Material*:

```bash
pip install mkdocs-material
```

I finalment, configurem el tema al fitxer `mkdocs.yml` .Recordem que aquest fitxer es fa servir per definir les opcions generals del lloc web, inclòs el tema que s'utilitza. Un exemple bàsic de configuració seria:

```yaml
site_name: Nom del projecte
theme:
   name: 'material'
```

<!--
Algunes **configuracions opcionals** que podrem incorporar en estos moments per millorar l'aparença o la funcionalitat del lloc poden ser les següents:

```yaml
theme:
   name: 'material'
   features:
      - navigation.sections
      - navigation.top
```

On afegim seccions i la barra de navegació superior.
-->

## **Plugins i extensions: ampliant les possibilitats de MkDocs**

El tema **Material per a MkDocs** ofereix moltes funcionalitats per defecte, però la seua autèntica potència apareix quan hi afegim **plugins** i **extensions Markdown**.

Aquests components permeten ampliar les capacitats bàsiques de MkDocs i afegir-li característiques més avançades, com ara:

* **Generar documents PDF** de tot el lloc o d’una pàgina concreta.
* **Afegir diagrames Mermaid**, per representar fluxos, processos o esquemes amb text.
* **Crear blocs informatius (admonitions)** per remarcar notes, advertències o exemples.
* **Millorar la visualització del codi font de programes informàtics** amb ressaltat de sintaxi i numeració de línies.
* **Afegir búsqueda interna** per facilitar la localització de contingut concret.
* **Mostrar imatges en finestres emergents** (lightbox).
* **Personalitzar la interfície** amb configuracions de tema, colors i icones addicionals.

Els plugins i extensions s’instal·len mitjançant **pip** dins del nostre entorn virtual i s’activen al fitxer `mkdocs.yml`. La seua configuració sol seguir un esquema semblant a aquest:

```yaml
plugins:
   - search
   - glightbox
   - pdf-export

markdown_extensions:
   - admonition
   - pymdownx.highlight
   - pymdownx.superfences
```

Als següents apartats ens dedicarem a conéixer algunes d’aquestes funcionalitats de manera més detallada.
