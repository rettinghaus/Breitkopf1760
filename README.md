# Verzeichniß Muſikaliſcher Bücher (Leipzig, 1760)

## Overview

This repository contains a full digital TEI XML transcription and high-resolution facsimiles of the historical music book and sheet music sales catalog:

> **Verzeichniß Muſikaliſcher Bücher**, ſowohl zur Theorie als Praxis, und für alle Jnſtrumente, in ihre gehörige Claſſen ordentlich eingetheilet; welche bey Johann Gottlob Jmmanuel Breitkopf in Leipzig um beyſtehende Preiſe in Louis d'or à 5 Thlr. zu bekommen ſind.
> **Erſte Ausgabe.** Leipzig, in der Neujahr-Meſſe, **1760**.

Published for the Leipzig New Year's Fair (*Neujahr-Messe*) in 1760 by Johann Gottlob Immanuel Breitkopf (1719–1794), this catalog represents a pivotal document in 18th-century music publishing and distribution. Breitkopf was an innovator in movable music typography and one of the most prominent music publishers and booksellers of the Enlightenment era.

The catalog encompasses theoretical treatises, instructional methods, vocal works, operas, cantatas, organ music, keyboard music (*Clavecimbel* / *Clavier*), chamber music, orchestral symphonies, and works for various instruments (violin, viola da gamba, lute, transverse flute, oboe, etc.) by composers such as Johann Sebastian Bach, Carl Philipp Emanuel Bach, Johann Mattheson, Friedrich Wilhelm Marpurg, Georg Andreas Sorge, Christoph Willibald Gluck, Baldassare Galuppi, Johann Adolph Hasse, and many others.

---

## Repository Structure

```
.
├── Breitkopf01.xml      # Full TEI XML encoding according to DTA Basisformat
├── facsimiles/          # High-resolution facsimile page scans (TIFF)
│   ├── f0001.tif        # Title page ([S. 1])
│   ├── f0002.tif        # Table of contents: Inhalt ([S. 2])
│   ├── f0003.tif        # S. 3: I. Hiſtorie der Muſik / II. Schriften & Critik
│   ├── ...
│   └── f0032.tif        # S. 32: XIV. Die Oboe / XV. Sammlungen / Nachricht
├── LICENSE.txt          # Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)
└── README.md            # Project description and documentation
```

---

## Contents of the Catalog

The catalog is structured into 15 main sections (*Classen*):

1. **I. Hiſtorie der Muſik** (p. 3)
2. **II. Schriften, die Muſik und deren Critik insgemein betreffend** (pp. 3–4)
3. **III. Anfangsgründe der Muſik** (p. 4)
   - *A. Zur Muſik überhaupt*
   - *B. Zur Jnſtrumentalmuſik beſonders*
4. **IV. Anweiſungen zum Generalbaß** (pp. 4–6)
5. **V. Die Setzkunſt** (pp. 6–7)
   - *Die Fuge*
6. **VI. Das Singen** (pp. 7–13)
   - *1. Anweiſungen zum Singen*
   - *2. Singen allein, ohne Accompagnement* (*a. Geiſtliche Lieder*, *b. Weltliche Lieder*)
   - *3. Choralbücher, geiſtliche Lieder und Arien*
   - *4. Weltliche Oden und Lieder mit dem Clavecimbel*
   - *5. Opern, Cantaten und Arien* (*a. mit dem Clavecimbel*, *b. mit verſchiedenen Jnſtrumenten*)
   - *6. Vollſtimmige Kirchen- und andere geiſtliche Muſiken*
7. **VII. Die Orgel und das Clavecimbel** (pp. 13–24)
   - *1. Die Stimmung und Temperatur*
   - *2. Anweiſung zur Orgel und Clavecimbel* (*a. Zum Clavier*, *b. Zur Orgel*)
   - *3. Stücke für die Orgel*
   - *4. Kleine Stücke für das Clavecimbel*
   - *5. Größere Stücke für das Clavecimbel* (Partien, Suiten, Piecen, Concerte, Sinfonien)
   - *6. Sonaten für das Clavecimbel*
   - *7. Obligates und concertirendes Clavecimbel mit verſchiedenen Jnſtrumenten*
8. **VIII. Die Violine** (pp. 25–28)
   - *1. Anweiſung zur Violine*
   - *2. Solos für die Violine*
   - *3. Duette*
   - *4. Trios*
   - *5. Concerte für die Violine*
   - *6. Sinfonien* (*a. mit 3 u. 4 Stimmen*, *b. mit 5 u. 6 Stimmen*, *c. mit 8, 10 u. 12 Stimmen*)
9. **IX. Die Viola da Gamba** (pp. 28–29)
10. **X. Der Violoncell** (p. 29)
11. **XI. Die Harfe** (p. 29)
12. **XII. Die Laute** (pp. 29–30)
    - *1. Solos und Duette*
    - *2. Concerte für die Laute und andere Jnſtrumente*
13. **XIII. Die Flöte traverſiere** (pp. 30–31)
    - *1. Anweiſung*
    - *2. Solos*
    - *3. Duette*
    - *4. Trios*
    - *5. Concerte*
14. **XIV. Die Oboe** (p. 32)
15. **XV. Sammlungen für allerley Jnſtrumente** (p. 32)
    - *Nachricht* (closing notice by J. G. I. Breitkopf)

---

## Encoding Principles

The transcription in `Breitkopf01.xml` follows the standards of the **TEI P5** guidelines and the **Deutsche Textarchiv Basisformat (DTA-Basisformat)**:

- **Typography & Font Shifts (`<hi>` / `@rendition`)**:
  - The base typeface of the catalog is Fraktur (*Gebrochene Schrift*).
  - Non-German text, Latin passages, French/Italian phrases, titles, author epithets, formats (`fol.`, `4to.`, `8vo.`, `transv.`), and price indicators (`à`) printed in Antiqua (*Lateinische Schrift*) are marked using `<hi rendition="#aq">`.
  - Spaced type (*Sperrdruck*) is encoded using `<hi rendition="#g">`.
  - Centered text headers are encoded with `<head rendition="#c">`.
  - Horizontal decorative separation rules (*Zierleisten* / *Linien*) are tagged with `<milestone unit="section" rendition="#hr"/>`.
- **Orthography**:
  - Historical spelling is preserved strictly, including the distinction between long 's' (`ſ`) and round 's' (`s`), consonant doublings, and historical capitalization.
  - Line breaks (`<lb/>`) and column breaks (`<cb/>`) correspond to the layout of the original printed catalog.
- **Page Structure (`<pb/>`)**:
  - Page breaks correlate directly with the facsimiles via `@facs` (e.g. `<pb n="3" facs="#f0003"/>`).
- **Entity Linking**:
  - Where identified, historical figures and authorities are tagged with `<persName>` (including GND URIs where appropriate in `@ref`).
  - Place names are tagged with `<placeName>`.

---

## Validation

The TEI XML document can be validated with Python using `lxml` against the official DTA Basisformat RelaxNG schema:

```python
import lxml.etree as ET

tree = ET.parse("Breitkopf01.xml")
print("Well-formed XML:", tree.getroot().tag)
```

---

## License

- The digital transcription and TEI XML encoding are licensed under the [Creative Commons Attribution-ShareAlike 4.0 International License (CC BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/). See `LICENSE.txt` for the complete license text.
