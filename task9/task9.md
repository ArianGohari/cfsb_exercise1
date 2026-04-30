# Task 9 – Struktur des Coronavirus

## Verfügbare Strukturen

In der **PDB** sind bereits 2020 mehrere hundert SARS-CoV-2-Strukturen
hinterlegt; mittlerweile mehrere tausend. Frühe Schlüssel­strukturen:

| Protein              | PDB               | Methode | Auflösung |
| -------------------- | ----------------- | ------- | --------- |
| Spike (Prefusion)    | 6VSB (Wrapp 2020) | Cryo-EM | 3.5 Å     |
| Spike-RBD + ACE2     | 6M0J (Lan 2020)   | X-ray   | 2.5 Å     |
| Hauptprotease Mpro   | 6LU7 (Jin 2020)   | X-ray   | 2.2 Å     |
| RNA-Polymerase nsp12 | 6M71              | Cryo-EM | 2.9 Å     |
| Nucleocapsid N       | 6VYO              | X-ray   | 1.7 Å     |

Strukturen werden außerdem in **CoV3D** und auf der **PDB-COVID-19-Seite** kuratiert.

## Homologie-Modellierung

Ja, gut möglich. SARS-CoV-1 und SARS-CoV-2 teilen ~76–80 % Spike-Sequenz, fast
alle nsp-Strukturen sind hochkonserviert. Tools wie **SWISS-MODEL**,
**Phyre2** oder **AlphaFold** liefern brauchbare Modelle bevor experimentelle
Strukturen verfügbar sind. Xu et al. (2020) modellierten so das SARS-CoV-2-Spike
auf Basis von SARS-CoV-1 noch vor Wrapp et al.s Cryo-EM-Struktur.

## Strukturelle Unterschiede zwischen den Viren

- **Spike-RBD:** SARS-CoV-2 und SARS-CoV-1 binden beide ACE2, aber SARS-CoV-2
  hat eine kompaktere Bindefläche und höhere ACE2-Affinität (~10–20×).
- **Furin-Spaltstelle (PRRAR)** in SARS-CoV-2 an der S1/S2-Grenze, fehlt bei
  SARS-CoV-1 → Tropismus-Erweiterung.
- **MERS-Spike** bindet DPP4 (CD26), also eine komplett andere Bindefläche.
- **Mpro / RdRp / Helikase** sind hochkonserviert (>95 % Identität SARS1↔2),
  Strukturen praktisch austauschbar, wichtig für Drug-Repurposing
  (z.B. Remdesivir gegen RdRp).

## Antikörper-Bindung (Yuan et al. 2020)

Yuan et al. lösten den Komplex aus dem RBD von SARS-CoV-2 und einem
neutralisierenden Antikörper (**CR3022**) eines früheren SARS-Patienten bei
**3.1 Å** auf. Schlüsselbeobachtungen:

- CR3022 erkennt ein **kryptisches Epitop**, das nur sichtbar ist, wenn
  mindestens zwei der drei RBDs im Spike-Trimer in der "up"-Konformation sind.
- Das Epitop ist **hochkonserviert** zwischen SARS-CoV-1 und SARS-CoV-2
  (28 von 31 Kontakt-Resten identisch).
- Trotz Konservierung neutralisiert CR3022 SARS-CoV-2 _nicht_ direkt, da die
  Bindung benötigt eine offene Konformation, die selten ist.
- Bedeutung: Hinweis auf konservierte Targets für **pan-Sarbecovirus-Antikörper**
  und Impfstoffe; Designprinzip, das Epitop durch RBD-Stabilisierung in
  "open"-Form besser zugänglich zu machen.

## Virus-Wirt-Interaktion (Xu et al. 2020)

Xu et al. modellierten das Spike-Protein und analysierten die RBD–ACE2-Schnittstelle
homologie­basiert. Wichtige Befunde:

- Die SARS-CoV-2-RBD passt strukturell besser an humanes ACE2 als die SARS-CoV-1-RBD.
- Wenige Aminosäure-Unterschiede in der **Receptor Binding Motif (RBM)**
  (z.B. um die Positionen 482–485) erklären die erhöhte Affinität.
- Das Modell sagte korrekt eine hohe humane Übertragbarkeit voraus, was später bestätigt wurde
  später durch Wrapps Cryo-EM-Struktur und epidemiologische Daten.

## Fazit

Die Strukturbiologie liefert die mechanistische Grundlage für Übertragbarkeit
(Spike–ACE2, Furin-Site), Wirkstoffziele (Mpro, RdRp) und Impfstoffdesign
(konservierte RBD-Epitope). Homologie­modellierung war in der Frühphase der
Pandemie entscheidend, bevor experimentelle Strukturen verfügbar waren.

## Quellen

- Wrapp D. et al., Science 367, 1260–1263 (2020). [PDB 6VSB]
- Lan J. et al., Nature 581, 215–220 (2020). [PDB 6M0J]
- Jin Z. et al., Nature 582, 289–293 (2020). [PDB 6LU7]
- Yuan M. et al., _A highly conserved cryptic epitope in the receptor-binding domains of SARS-CoV-2 and SARS-CoV_, Science (2020), doi:10.1126/science.abb7269.
- Xu et al., _Evolution of the novel coronavirus from the ongoing Wuhan outbreak and modelling of its spike protein for risk of human transmission_, Sci China Life Sci 63, 457–460 (2020).
