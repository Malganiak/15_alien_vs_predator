# 15_alien_vs_predator

Projet Alien vs. Predator - Épisode 1 : Développement d'un Programme de Vision par Ordinateur

Introduction :
Dans le cadre du projet "Alien vs. Predator - Épisode 1", l'objectif est de concevoir un programme de vision par ordinateur capable de discriminer avec précision un Alien d'un Predator. Cela devient crucial à la suite de l'éradication de la pandémie de COVID-19, marquant le début d'une ère prospère sur la planète, mais attirant l'attention de deux familles extraterrestres, les Aliens et les Prédators, qui cherchent à envahir la Terre pour prospérer. Pour défendre l'écosystème terrestre, les GAFA et les BATX ont fourni à chaque individu un smartphone équipé d'applications, mais un bug majeur nécessite le développement d'un programme de vision par ordinateur pour résoudre le problème.

Développement du Programme :

Collecte des données :

Télécharger le dataset approprié depuis le répertoire Teams de la promotion.
Implémentation du Modèle CNN avec Keras :

Construire un modèle Convolutional Neural Network (CNN) selon l'architecture suivante :
python
Copy code
model = Sequential([
    layers.Conv2D(filters=16, kernel_size=3, strides=1, activation='relu', input_shape=(150, 150, 3)),
    layers.MaxPooling2D(pool_size=(2, 2)),
    layers.Conv2D(filters=32, kernel_size=3, strides=1, activation='relu'),
    layers.MaxPooling2D(pool_size=(2, 2)),
    layers.Conv2D(filters=64, kernel_size=3, strides=1, activation='relu'),
    layers.MaxPooling2D(pool_size=(2, 2)),
    layers.Flatten(),
    layers.Dense(units=512, activation='relu'),
    layers.Dense(units=1, activation='sigmoid')
])
Entraînement du Modèle :

Utiliser l'approche full batch pour entraîner le modèle sur 100 epochs.
Conclusion :

Analyser les résultats et conclure sur l'efficacité du modèle dans la distinction entre Aliens et Prédators.
Livrables :

Fournir un Jupyter Notebook documenté, contenant le code en langage Python avec des explications claires.
Critères de Performance :

Le code doit être clair, bien structuré et commenté de manière approfondie pour assurer la compréhension.
Le modèle CNN doit être correctement implémenté et entraîné avec les spécifications mentionnées.
Le Jupyter Notebook doit être complet, détaillant chaque étape du processus, de la collecte des données à l'analyse des résultats.
