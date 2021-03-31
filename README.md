 # TP ENSEIRB Microstructure cardiaque par IRM

Afin d'étudier la microstructure, deux acquisitions ont été réalisées sur un imageur Bruker 9.4T sur un échantillon:

- une séquence d'écho de gradient: FLASH (Fast low angle shot magnetic resonance imaging). Les paramètres sont les suivants: TE = 9  ms;  TR = 30  ms;  matrix size = 731 × 665 × 532;  FOV = 110 × 100 × 80 mm. La résolution des voxels est 150 μm isotrope.
- une séquence d'echo de spin: DWI (Diffusion weighted imaging). La résolution des voxels est 600 μm isotrope.  Six directions de gradient sont utilisées. Les paramètres sont les suivants: TE = 22  ms, TR = 500  ms,  FOV = 100 × 80 × 110  mm, matrice = 166 × 133 × 183. 


# Objectifs 1 : repérage anatomique

## Intro

Nous allons réaliser un bref cours d'anatomie en s'appuyant sur l'image d'écho de gradient réachantillonné à 600 um. L'objectif de cette première partie est de distinguer les différentes structures présentes de le coeur et de se familiariser avec deux logiciels de traitements d'image dédié à l'IRM. Pour visualiser les images IRM, vous allez utiliser de deux logiciels open-source: `3DSlicer` ou `mrview` (visualiseur issue de la librairie `MRtrix`).   

Nous allons identifier notamment:

* les cavitées cardiaques
* les valves
* les vaisseaux
* les structures de conduction


Un bref récapitulatif est accessible à ce [lien](Annexes/README.md) .

## Pratique

 Télécharger le fichier suivant à ce [lien](https://filesender.renater.fr/?s=download&token=1588e4bd-2d63-4d3c-b6ad-6107b0b7998c):
 
- installer `3DSlicer` via ce [lien](https://download.slicer.org/) 
- lancer `3DSlicer`  
- charger l'image avec l'`icone data`, choose file to add `Intensity.nii.gz`
- cliquer sur la `icone croix jaune`
- appuyer sur la touche shift et deplacer le curseur sur l'image.
- clic droit enfoncé + mouvement : changer le zoom
- clic gauche enfoncé + mouvement de la souris : changer le contraste
- `icone loupe` pour chercher une option:
   - taper `volume rendering` , cliquer dessus et cliquer sur le petit `oeil` pour activer le rendu 
	- dans la vue 3D clic droit `rotation`
	- dans la vue 3D clic guache `zoom`


Vous devez maintenant identifier et reporter les positions suivantes avec l'onglet `fiducial`:

* haut du coeur (base)

* bas du coeur (apex)

* ventricule gauche (VG)

* ventricule droit (VD)

* septum interventriculaire (partie du myocarde qui sépare VG et VD) 

* oreillette (ou atrium) gauche (R-2,A-4.9, S30)

* oreillette (ou atrium) droite (R22,A-2.7,32S)

* artère pulmonaire (R24,A23,S25)

* aorte (R9,A11.5,S36)

* valve tricuspide (nombre de feuillets). [Un indice](https://fr.wikipedia.org/wiki/Valve_tricuspide) .

* valve mitrale (nombre de feuillets)

* valve aortique (nombre de feuillets)


# Objectifs 2 : A la recherche du faisceaux de His

## Intro

Un très bref récapitulatif est accessible à ce [lien](Annexes/README.md) .

Vous devez maintenant identifier la zone contenant le faisceaux de His. Le faisceaux de His est une:

"Voie de conduction de l’influx électrique reliant les oreillettes (plus précisément le nœud atrio-ventriculaire) aux ventricules. Situé dans la cloison des ventricules, ce faisceau est trop fin et trop court (quelques millimètres) pour être visible, même sur des examens d’imagerie moderne (échographie, scanner, IRM). Seule l’activité électrique vue sur l’électrocardiogramme ou enregistrée lors d’une exploration électrophysiologique permet de certifier son bon fonctionnement. Dans le cas contraire, on observera un blocage de la conduction des oreillettes aux ventricules (bloc atrio-ventriculaire)." 

Le faisceau de His passe dans le septum interventriculaire et se divise en deux branches.

## Pratique

Utiliser l'onglet loupe puis `crop`
 - cliquer sur display ROI
 - reduire la ROI au niveau septum interentriculaire (partie du myocarde qui sépare VG et VD) 
 - cliquer sur apply
 
 
 Télécharger ensuite le fichier suivant à ce [lien]():

En se deplacer dans la direction (A-P) localiser 

* le septum interventriculaire partie supérieure (RX,AX,SX)

* le feuille septal (du coté du septum) de la valve tricupside (RX,AX,SX). Pour cela il faut localiser les jonctions entre la cavité de l'oreillette ... et la cavité du ventricule ....

* le feuillet septal (du coté du septum) de la valve mitrale (RX,AX,SX). Pour cela il faut localiser les jonctions entre la cavité de l'oreillette ... et la cavité du ventricule ....

En utilisant les images présentes en annexe dans la partie histologie [lien](Annexes/README.md) pour donner une position approximative du faisceau de His. Les coupes d'histologie sont réalisées dans le plan `vert` en bas à droite sur `3DSlicer`.

C'est le volume acquis à la résolution de 150um coupé dans la zone d'intérêt. Quelques observations:

- Avec cette résolution, on commence à visualiser l'agencement des fibres (ou des amas de fibres cardiaques). 
- Les valves et le tissu cardiaque ont des contrastes différents avec des valeurs de proche de 2 (en blanc) et de 1 (en gris) respectivement.
- Les cordages et piliers des valves sont particulièrement visibles dans la vue 3D `volume rendering`. 

* Trouver le faisceau de His (R , A , S ) 
* L'intersection avec la branche gauche et droite (R , A , S )
* Les extrémités de la branche gauche (R , A , S) 
* Les extrémités de la branche droite (R , A , S) 


# Objectifs 3 : La microstructure cardiaque et imagerie du tenseur de diffusion

# Intro 

 DWI -> DTI : de l'imagerie pondérée en diffusion aux tenseurs de diffusions. 

- Milieu isotrope.
- Milieu anisotrope.

- Tenseur
- Vecteurs
- Tractographie 

# Pratique

- lancer MRtrix  
- charger le fichier `intensity_zoom.nii.gz`
- jouer avec le contraste
- ce déplacer dans l'espace
- vue coupe et vue volume 
- utiliser F3 (mrview) ou volume renderer (slicer)
- utiliser l'outil transform

## RGB map et orientation des fibres
- utiliser l'onglet tools
- overlay pour charger le fichier `v1.nii.gz`

## Vecteurs et orientation des fibres
- utiliser l'onglet tools
- fixel pour charger le fichier `v1.nii.gz`

## Tractographie
- utiliser l'onglet tools
- tractography pour charger le fichier `streamlines.tck`


Décrire l'orientation des vecteurs dans le septum interventriculaire.

