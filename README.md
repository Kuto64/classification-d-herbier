# Détection et Lecture Automatique d’Étiquettes d’Herbier

Ce projet propose un pipeline automatisé pour la détection et la lecture d’étiquettes présentes sur les spécimens d’herbiers. En combinant des techniques de détection d’objets et de reconnaissance optique de caractères (OCR), ce pipeline vise à faciliter la numérisation et l'analyse des collections d'herbiers.

## Objectifs
- Détection automatique des étiquettes sur les images d’herbiers à l’aide de YOLOv5.
- Extraction du contenu textuel (manuscrit ou imprimé) grâce à des modèles OCR.
- Automatisation complète pour réduire le temps de traitement et améliorer l'accès aux données.

## Méthodologie
1. **Détection des étiquettes** :
   - Utilisation de YOLOv5 pour localiser les étiquettes dans les images.
2. **Segmentation et classification** :
   - Découpage des régions détectées et identification du type d’étiquette (manuscrite, imprimée, institutionnelle, etc.).
3. **Extraction textuelle** :
   - Utilisation de Tesseract pour les textes imprimés et EasyOCR pour les écritures manuscrites.
4. **Stockage des résultats** :
   - Les textes extraits sont sauvegardés dans des fichiers CSV ou des bases de données.

## Résultats
- **Détection des étiquettes** :
  - Précision : 0.983
  - Rappel : 0.969
  - mAP@0.5–0.95 : 0.847
- **Extraction textuelle** :
  - Taux de reconnaissance supérieur à 95% pour les textes imprimés.
  - Performances satisfaisantes pour les écritures manuscrites avec EasyOCR, malgré des limitations sur les textes très complexes ou dégradés.
- Temps moyen de traitement par image : 1.5 secondes.
- Taux global de précision du pipeline : 92%.

## Technologies Utilisées
- **YOLOv5** : Détection des étiquettes.
- **Tesseract** et **EasyOCR** : Extraction de texte.
- **OpenCV** : Traitement d’images.
- **Pandas** : Manipulation et stockage des données.
- **Python** : Langage de programmation principal.

## Structure du Pipeline
1. Chargement des images depuis le dataset.
2. Détection des étiquettes avec YOLOv5.
3. Recadrage des régions détectées.
4. Classification des types d’étiquettes.
5. Extraction textuelle via OCR.
6. Sauvegarde des données extraites.

## Limitations et Améliorations Futures
- Difficultés avec les images de faible qualité (artefacts, ombres, reflets).
- Erreurs sur les écritures manuscrites complexes.
- Propositions pour l’avenir :
  - Enrichir les datasets avec des exemples plus variés.
  - Utiliser des modèles OCR plus avancés.
  - Optimiser les performances du pipeline pour réduire le temps de traitement.

## Applications
- Numérisation et gestion des collections d’herbiers.
- Recherche scientifique (analyse écologique, taxonomique, etc.).
- Archivage numérique et valorisation patrimoniale.
- Extension possible à d'autres domaines (documents historiques, manuscrits, musées).

## Conclusion
Ce pipeline illustre le potentiel des techniques modernes de vision par ordinateur et d'apprentissage profond pour la numérisation d'herbiers. Il fournit une solution rapide et scalable, tout en ouvrant des perspectives pour des améliorations futures.

