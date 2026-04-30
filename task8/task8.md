# Task 8 – Evolution des Coronavirus (nextstrain & GISAID)

## Ressourcen

- **GISAID**: zentrale Sequenzdatenbank für Influenza und Coronaviren; Forscher
  laden SARS-CoV-2-Genome inklusive Sammeldatum und Ort hoch.
- **nextstrain.org/ncov**: nutzt GISAID-Daten und baut daraus interaktive
  Phylogenien mit geografischer und zeitlicher Annotation
  (Auggur-Pipeline, Visualisierung mit Auspice).

## Was man aus den Phylogenien lernt

- Der Stammbaum zeigt, dass alle SARS-CoV-2-Sequenzen auf einen gemeinsamen
  Vorfahren Ende 2019 in Wuhan zurückgehen, konsistent mit einer einzelnen
  zoonotischen Übertragung.
- Die Mutationsrate (~2 Substitutionen/Genom/Monat) ist hoch genug, um
  Übertragungsketten über Wochen aufzulösen, aber niedrig genug, dass das
  Genom über Monate stabil bleibt.
- Cluster im Baum entsprechen oft Ausbruchsereignissen (z.B. Skigebiet Ischgl,
  Norditalien, US-Ostküste).

## Mutationen vs. geografische Muster

Ja, Mutationen und Geografie korrelieren, aber **nicht weil das Virus sich
lokal anpasst**, sondern wegen **Founder-Effekten und Reise-Verbindungen**:

- Frühe Linien **L/S** in Wuhan; **A** und **B** als Hauptzweige.
- **D614G** (im Spike) entstand früh in Europa, verbreitete sich global und
  verdrängte die ursprüngliche Variante mit einem leichten Selektionsvorteil
  (höhere Infektiosität).
- Regionale Cluster (z.B. B.1.1 in Großbritannien, B.1.177 in Spanien) zeigen,
  dass einzelne Reise-Einträge ganze Wellen prägen.
- Spätere VOCs (Alpha, Delta, Omicron) entstanden vermutlich in
  immunsupprimierten Patienten oder unter Selektionsdruck und breiteten sich
  dann weltweit aus.

## Fazit

Die Phylogenien zeigen: Mutationen treten weitgehend zufällig auf, ihre
geografische Verteilung wird vor allem durch menschliche Mobilität und
Containment-Maßnahmen geprägt. Echter Selektionsdruck wird sichtbar bei
Mutationen mit funktionalem Vorteil (D614G, später VOCs). nextstrain
visualisiert beides: zufällige Drift entlang von Übertragungsketten
und gerichtete Selektion einzelner Varianten.

## Quellen

- Hadfield J. et al., _Nextstrain: real-time tracking of pathogen evolution_, Bioinformatics 34 (23), 2018.
- nextstrain.org/ncov · gisaid.org
- Korber B. et al., _Tracking changes in SARS-CoV-2 Spike: D614G increases infectivity_, Cell 182 (4), 2020.
