# capteur_de_tension_cable
In this repository you can find the presentation, document, code and CAD model of the tension sensor dynamical project.

# Configuration Expérimentale

## Description du Montage

Le système expérimental est composé des éléments suivants :

1. Trois poulies montées sur un bâti rigide
2. Un câble en fibre de kevlar passant autour des poulies
3. Un moteur pour entraîner le câble à différentes vitesses (non fonctionnel pour nos essais, nous avons donc fait uniqement des mesure par chute d'une masse)
4. Un capteur de force (cellule de charge) pour mesurer la force sur la poulie centrale
5. Un encodeur ou un tachymètre pour mesurer la vitesse du câble (non fonctionnel également)
6. Un système d'acquisition de données pour enregistrer les mesures (via un arduino, communiquant sur le port serie, à terme cet Arduino communiquera en I2C avec les reste du système)

![Montage Expérimental](images/experimental_setup.png)

## Composants Principaux

| Composant           | Modèle/Spécifications          | Quantité |
|---------------------|--------------------------------|----------|
| Structure PLA       | Obtenue par Impression FDM     | 3        |
| Roulement           | 608ZZ (8x22x7 mm)              | 3        |
| Capteur de force    | Cellule de charge 200N         | 1        |

## Protocole Expérimental

1. **Initialisation :**
   - Vérifier que le câble est correctement installé sur les poulies
   - S'assurer que les capteurs sont calibrés
   - Démarrer le système d'acquisition de données

2. **Mesures :**
   - Pour chaque vitesse cible :
     - Régler la vitesse du moteur
     - Attendre que le système atteigne un régime permanent
     - Enregistrer la vitesse mesurée et la force sur la poulie centrale
     - Répéter N fois pour chaque vitesse pour assurer la reproductibilité

3. **Plage de Vitesses :**
   - De 0 m/s à 2 m/s par incréments de 0.1 m/s

4. **Calibration :**
   - Effectuer une calibration du capteur de force avant chaque série de mesures
   - Vérifier le zéro du capteur de force

## Considérations de Sécurité

1. Ne pas toucher les parties mobiles pendant le fonctionnement
2. S'assurer que toutes les fixations sont serrées avant de démarrer le système

