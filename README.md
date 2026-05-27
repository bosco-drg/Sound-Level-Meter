# Sonomètre — Projet de mesure de niveau sonore

> Projet complet de sonomètre électronique : schéma, PCB (KiCad) et simulations (LTSpice).

---

## Aperçu rapide

Ce dépôt contient la conception d'un **sonomètre** (instrument de mesure du niveau sonore) couvrant l'adaptation d'entrée, la conditionnement du signal, le filtrage, la détection RMS/Crête, l'acquisition et les aspects matériels (schéma et PCB). Sont inclus : le **schéma**, le **PCB** et les **simulations**.

### Points clés

- **Mesure de niveau sonore** : détection RMS et/ou crête, calcul de niveaux (dB SPL)
- **Pondérations et filtres** : options de filtrage (pondération A/B) pour mesures conforme
- **Calibration** : procédures et composants pour calibration avec source connue
- **Conception matérielle** : schéma et routage PCB sous KiCad
- **Simulations** : modèles LTSpice pour valider le conditionnement et la détection
- **Documentation visuelle** : diagrammes fonctionnels et captures de simulation

---

## PCB

<div align="center">

![PCB back side](doc/1.png)

**PCB — côté composants**

</div>

<div align="center">

![PCB component side](doc/2.png)

**PCB — verso**

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

---

## Auteurs

- **Bosco de Rauglaudre**
- **Titouan Bocquet**
- **Gavin Mac Aonghusa**