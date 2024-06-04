## 1. *Embodied emissions*

- **Définition : émissions provenant des matériaux et processus de production d'un produit, réparties sur sa durée d'utilisation**
- **Équipement : modèle BLOOM entraîné sur des serveurs HPE Apollo 6500 Gen10 Plus avec des GPU Nvidia A100**
- **Estimation des émissions des GPU : Environ 150 kg CO2e par GPU Nvidia A100**
- **Calculs :**
    - **Serveur : 0,056 kg CO2e par heure**
    - **GPU : 0,003 kg CO2e par heure**
    - **Total embodied emissions : 11,2 tonnes CO2e (7,57 tonnes des serveurs ; 3,64 tonnes des GPU)**

## 2. Dynamic Power Consumption

- **Focus** : Émissions provenant de l'électricité utilisée pendant l'entraînement du modèle.
- **Détails de l'entraînement** : 1,08 million d'heures de GPU utilisant 384 GPU
- **Consommation énergétique** : 433 195 kWh (400W TDP par GPU)
- **Intensité Carbone** : 57 gCO2e/kWh
- **Émissions** : 24,69 tonnes CO2e provenant de la consommation énergétique dynamique

## 3. *Idle Power Consumption*

- **Définition** : Énergie utilisée pour maintenir et connecter le matériel lorsqu'il n'est pas activement utilisé
- **Calculs** :
    - Consommation supplémentaire : 256 646 kWh
    - Émissions : 14,6 tonnes CO2e

#### Répartition des émissions

- **Embodied emissions** : 11,2 tonnes CO2e (22,2 %)
- **Dynamic power consumption** : 24,69 tonnes CO2e (48,9 %)
- **Idle power consumption** : 14,6 tonnes CO2e (28,9 %)
- **Total** : 50,5 tonnes CO2e

## 5. *Deployment and inference*

- **Analyse de déploiement** : réalisée sur Google Cloud Platform avec 16 GPU Nvidia A100 sur 18 jours
- **Consommation énergétique** : fluctuait entre 1252W et 2735W (78-171W par GPU)
- **Énergie totale utilisée : 914 kWh (75,3 % par les GPU, 22,7 % par la RAM, 2 % par le CPU)
- **Intensité carbone** : 394 gCO2e/kWh
- **Émissions de déploiement** : ~19 kg CO2e par jour, 340 kg sur 18 jours

---
Source :

**Estimating the Carbon Footprint of BLOOM, a 176B Parameter Language Model**
*Alexandra Sasha Luccioni (HuggingFace), Sylvain Viguier (GraphCore), Anne-Laure Ligozat (LISN & ENSIIE)*
https://ar5iv.labs.arxiv.org/html/2211.02001