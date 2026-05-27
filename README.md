### Key features

# Sonomètre — Projet de mesure de niveau sonore

> Projet complet de sonomètre électronique : schéma, PCB (KiCad) et simulations (LTSpice).

---

## Aperçu rapide

Ce dépôt contient la conception d'un **sonomètre** (instrument de mesure du niveau sonore) couvrant l'adaptation d'entrée, la conditionnement du signal, le filtrage (pondération A), la détection RMS/Crête, l'acquisition et les aspects matériels (schéma et PCB). Sont inclus : le **schéma**, le **PCB**, les **simulations** et la documentation visuelle.

### Points clés

- **Mesure de niveau sonore** : détection RMS et/ou crête, calcul de niveaux (dB SPL)
- **Pondérations et filtres** : options de filtrage (pondération A/B) pour mesures conforme
- **Calibration** : procédures et composants pour calibration avec source connue
- **Conception matérielle** : schéma et routage PCB sous KiCad
- **Simulations** : modèles LTSpice pour valider le conditionnement et la détection
- **Documentation visuelle** : diagrammes fonctionnels et captures de simulation

---

## Architecture du système

<div align="center">

![Global diagram](doc/Diagramme%20global.png)

**Diagramme global** — *Architecture fonctionnelle du sonomètre*

</div>

<div align="center">

![Global circuit](doc/Circuit%20global.png)

**Schéma global** — *Vue d'ensemble du circuit*

</div>

---

## Détails des sous‑blocs

### Préamplification / adaptation d'entrée

<div align="center">

![Input adaptation](doc/AdaptationEntree.png)

**Adaptation d'entrée** — *Préampli micro / adaptation impédance et filtrage d'entrée*

</div>

### Conditionnement et filtrage

<div align="center">

![Amplification](doc/Ampli.png)

**Conditionnement** — *Amplification, filtrage (pondération A) et anti‑aliasing*

</div>

### Détection RMS / mesure d'enveloppe

<div align="center">

![Peak detection](doc/DetecteurCretes.png)

**Détecteur** — *Génération d'une valeur représentative (RMS/Leq/Crête) pour conversion en dB*

</div>

### Acquisition / affichage

<div align="center">

![Gain control](doc/AttenuateurControle.png)

**Acquisition et affichage** — *Convertisseur ADC, traitement embarqué et affichage/communication*

</div>

### Sortie / calibration

<div align="center">

![Output adaptation](doc/AdaptationSortieAmpli.png)

**Calibration et sortie** — *Accès pour calibration, sortie analogique/numérique et interface*

</div>

---

## Simulations LTSpice

<div align="center">

![LTSpice envelope](doc/LTspice%20demo%20enveloppe.png)

**Simulation d'enveloppe** — *Réponse du détecteur / comportement temporel*

</div>

<div align="center">

![LTSpice signal](doc/LTSpice%20demo%20signal%20a.png)

**Simulation de signal** — *Validation du conditionnement et de la chaîne de mesure*

</div>

---

## Photos PCB (si disponibles)

<div align="center">

![PCB back side](doc/1.png)

**PCB — verso**

</div>

<div align="center">

![PCB component side](doc/2.png)

**PCB — côté composants**

</div>

---

## Structure du projet

```
Sound-Level-Meter/
├── README.md
├── doc/                       # Documentation visuelle et images
├── schematic_Kicad/           # Projet KiCad (schéma + PCB)
│   └── Projet2_EC/
│       ├── Projet2_EC.kicad_sch
│       ├── Projet2_EC.kicad_pcb
│       └── fp-info-cache/
└── simulation/
	└── sound_level_meter_SPICE.asc
```

---

## Ouvrir le projet

### KiCad
- Ouvrir le projet dans [schematic_Kicad/Projet2_EC/](schematic_Kicad/Projet2_EC/)
- Fichiers principaux :
	- Schéma : [schematic_Kicad/Projet2_EC/Projet2_EC.kicad_sch](schematic_Kicad/Projet2_EC/Projet2_EC.kicad_sch)
	- PCB : [schematic_Kicad/Projet2_EC/Projet2_EC.kicad_pcb](schematic_Kicad/Projet2_EC/Projet2_EC.kicad_pcb)

### LTSpice
- Schéma de simulation : [simulation/sound_level_meter_SPICE.asc](simulation/sound_level_meter_SPICE.asc)
- Tests et fichiers PWL : voir le dossier `simulation/`

---

## Auteurs

- **Bosco de Rauglaudre**
- **Titouan Bocquet**
- **Gavin Mac Aonghusa**

---

## Authors

- **Bosco de Rauglaudre**
- **Titouan Bocquet**
- **Gavin Mac Aonghusa**


