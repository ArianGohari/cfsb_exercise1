# Task 7 – Sequenzierung des Coronavirus

## 1. Stand der SARS-CoV-2-Sequenzierung

Zum Zeitpunkt der Aufgabenstellung (April 2020) waren bereits ca. 10.000
SARS-CoV-2-Genome verfügbar, hauptsächlich über GISAID. Mittlerweile sind es
mehrere Millionen; SARS-CoV-2 ist das am dichtesten sequenzierte Pathogen der
Geschichte. Das Referenzgenom ist **Wuhan-Hu-1** (NC_045512.2, 29.903 bp,
Dezember 2019). Die Sequenzierung erfolgt überwiegend per Illumina-
Shotgun oder Oxford-Nanopore Amplicon-Tiling (ARTIC-Protokoll).

## 2. Variabilität innerhalb von SARS-CoV-2

Die Mutationsrate liegt bei ca. **1–2 × 10⁻³ Substitutionen pro Stelle und Jahr**,
also ungefähr 2 Mutationen pro Genom pro Monat, niedrig im Vergleich zu Influenza,
weil das virale RNA-Polymerase-Komplex eine Korrekturlese-Funktion (nsp14, ExoN)
besitzt.

Wichtige frühe Linien (Stand 2020):

- **L** und **S** (Wuhan, früh)
- **G/GH/GR** (D614G im Spike, dominant in Europa/USA)

Die meisten Mutationen sind synonym oder neutral; einige im Spike-Protein
verändern Übertragbarkeit oder Antigenität (z.B. D614G → höhere Infektiosität,
spätere VOCs Alpha/Delta/Omicron mit RBD-Mutationen wie N501Y, K417N, E484K).

Phylogenien und geographische Cluster sind auf [nextstrain.org](https://nextstrain.org)
einsehbar (siehe Task 8).

## 3. Vergleich SARS-CoV-2 / SARS-CoV-1 / MERS-CoV

Alle drei sind **Betacoronaviren** mit (+)ssRNA-Genom. Aus Task 4 (NCBI RefSeq):

| Virus      | Accession   | Länge     | Wirt-Rezeptor | Letalität  |
| ---------- | ----------- | --------- | ------------- | ---------- |
| SARS-CoV-2 | NC_045512.2 | 29.903 bp | ACE2          | ~1 % (CFR) |
| SARS-CoV-1 | NC_004718.3 | 29.751 bp | ACE2          | ~10 %      |
| MERS-CoV   | NC_019843.3 | 30.119 bp | DPP4 (CD26)   | ~35 %      |

**Sequenzidentität:**

- SARS-CoV-2 vs. SARS-CoV-1: ~79 % Genom, ~76 % Spike
- SARS-CoV-2 vs. MERS-CoV: ~50 % Genom
- SARS-CoV-2 vs. RaTG13 (Fledermaus-CoV): ~96 %, was auf einen zoonotischen Ursprung hinweist

## 4. Genomorganisation

Alle drei haben dieselbe Grundstruktur:

```
5'-UTR | ORF1ab (~21 kb, Polyprotein → 16 nsps) | S | ORF3 | E | M | ORF6-8 | N | 3'-UTR
```

- **ORF1ab** (~2/3 des Genoms): kodiert pp1a/pp1ab, gespalten in **nsp1–nsp16**
  (RNA-Polymerase nsp12, Helicase nsp13, ExoN-Korrekturlese nsp14, Hauptprotease
  Mpro/3CLpro = nsp5).
- **Strukturproteine**: S (Spike), E (Envelope), M (Membran), N (Nucleocapsid).
- **Akzessorische ORFs**: variabel zwischen den Spezies. SARS-CoV-1 hat ORF8a/8b
  (in SARS-CoV-2 verschmolzen zu ORF8), MERS hat zusätzliche ORF4a/4b/5.

## 5. Wichtige Proteinunterschiede

**Spike (S):**

- SARS-CoV-2 hat eine **Furin-Spaltstelle (PRRAR)** an der S1/S2-Grenze, die
  weder SARS-CoV-1 noch RaTG13 besitzen. Das verbessert die Spaltung in vielen
  Geweben und gilt als Schlüsselfaktor für die hohe Übertragbarkeit.
- RBD bindet ACE2 mit höherer Affinität als SARS-CoV-1 (Wrapp et al., Science 2020).
- MERS-RBD bindet ein anderes Target (DPP4), mit einer komplett anderen Bindungsfläche.

**ORF8:**

- Kandidat für Immun-Evasion; in SARS-CoV-2 stärker variabel.

**N-Protein:**

- Hochkonserviert; bevorzugtes Target für serologische Tests.

## 6. Phänotypische / Lebenszyklus-Unterschiede

|                      | SARS-CoV-1                               | MERS-CoV                | SARS-CoV-2              |
| -------------------- | ---------------------------------------- | ----------------------- | ----------------------- |
| Reservoirwirt        | Hufeisennasen-Fledermaus → Schleichkatze | Fledermaus → Dromedar   | Fledermaus → ?          |
| Auftreten            | 2002/03                                  | 2012–                   | 2019–                   |
| R₀                   | ~2–3                                     | <1 (kaum Mensch-Mensch) | ~3 (Wuhan) – 5+ (VOCs)  |
| Inkubation           | 4–6 d                                    | 5–7 d                   | 5 d                     |
| Hauptreplikationsort | untere Atemwege                          | untere Atemwege         | obere + untere Atemwege |
| Präsymp. Übertragung | nein                                     | minimal                 | **ja, signifikant**     |
| Letalität            | ~10 %                                    | ~35 %                   | ~1 %                    |

Die effektive **prä-/asymptomatische Übertragung** unterscheidet SARS-CoV-2
fundamental von SARS-CoV-1 und ist der Hauptgrund, warum Containment so viel
schwieriger war.

## 7. Lassen sich Phänotyp und Wirts-Spezifität auf Sequenz zurückführen?

**Teilweise, ja.**

- **Wirts-Spezifität:** Hauptsächlich durch RBD-Sequenz determiniert. Wenige
  Aminosäuren in der RBD-Receptor-Binding-Motif-Region entscheiden, welcher
  Rezeptor (ACE2 vs. DPP4) und welche Spezies-Variante davon gebunden wird.
  Xu et al. (2020) modellierten dies für SARS-CoV-2 und zeigten enge Verwandtschaft
  zur Fledermaus-RBD plus Anpassungen Richtung humanem ACE2.

- **Übertragbarkeit:** Die Furin-Spaltstelle in SARS-CoV-2-Spike ist ein
  konkretes Sequenzmerkmal, das funktional die Tropismus-Erweiterung in obere
  Atemwege erklärt → höhere Transmissibilität.

- **Immunogenität:** Konservierte Epitope (z.B. das von Yuan et al. 2020
  beschriebene kryptische RBD-Epitop, das sowohl SARS-CoV-1- als auch
  SARS-CoV-2-Antikörper bindet) zeigen, dass strukturelle Konservierung
  Kreuzreaktivität ermöglicht, wichtig für pan-Sarbecovirus-Impfstoffe.

- **Letalität** dagegen ist nur **schlecht direkt** aus der Sequenz ableitbar:
  sie hängt von Tropismus, Immunantwort und klinischem Verlauf ab, also von
  einem komplexen Zusammenspiel viraler und Wirtsfaktoren.

**Fazit:** Sequenzanalyse erklärt Rezeptornutzung und einzelne
Pathogenitätsfaktoren (Furin-Site) gut, aber die Gesamtphänotypen erfordern
funktionelle Studien, Strukturbiologie (Task 9) und Netzwerkanalysen (Task 11).

## Quellen

- Wu F. et al., _A new coronavirus associated with human respiratory disease in China_, Nature 2020, 579:265–269.
- Wrapp D. et al., _Cryo-EM structure of the 2019-nCoV spike in the prefusion conformation_, Science 2020.
- Xu et al., _Evolution of the novel coronavirus from the ongoing Wuhan outbreak and modelling of its spike protein for risk of human transmission_, Sci China Life Sci 63 (3), 457–460, 2020.
- Yuan M. et al., _A highly conserved cryptic epitope in the receptor-binding domains of SARS-CoV-2 and SARS-CoV_, Science 2020.
- Andersen K.G. et al., _The proximal origin of SARS-CoV-2_, Nat Med 2020.
- NCBI RefSeq, GISAID, nextstrain.org.
