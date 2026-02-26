# Projet_s-rie_temporelle-

# Présentation du Projet

L'objectif est d'analyser les dynamiques sectorielles contrastées et de proposer des prévisions à court terme en utilisant des modèles de séries temporelles.


# Données : Valeurs annuelles de l'IPI (Insee) sur la période 1990-2024.

Secteurs étudiés : * Automobile : Secteur très cyclique et volatil.
**Pharmacie** : Secteur stable avec une croissance régulière.
**Énergie** : Trajectoire intermédiaire, choisie pour la modélisation approfondie en raison de ses propriétés statistiques.

# Méthodologie

**Analyse Exploratoire**  : Étude de la stationnarité via le test de Dickey-Fuller (ADF) et analyse des corrélogrammes (ACF/PACF).
**Modélisation**  : Sélection et estimation d'un modèle ARMA(1,1) pour le secteur de l'énergie, jugé le plus adapté après différenciation logarithmique.
**Estimation :** Sélection du modèle **ARIMA(1,1,1)** (ou ARMA(1,1) sur la série différenciée) basé sur les critères AIC/BIC.
**Validation :** Test de Ljung-Box pour s'assurer que les résidus sont un bruit blanc (absence d'information non capturée).

# Résultats et Prévisions

L'analyse de l'Indice de la Production Industrielle (IPI) entre 1990 et 2024 a permis de dégager trois conclusions majeures :

**1. Dynamiques Sectorielles Contrastées** 
L'étude comparative montre des comportements très différents selon les secteurs :

- **Secteur de l'Automobile**: Marquée par une forte cyclicité et une grande sensibilité aux crises économiques. C'est le secteur le plus volatil du panel.

- **Secteur Pharmaceutique**: Affiche une croissance structurelle quasi-linéaire et régulière, démontrant une forte résilience face aux cycles économiques.

- **Secteur de l'Énergie**: Présente une trajectoire intermédiaire avec des fluctuations notables, mais une tendance globale à la stabilisation sur la période récente

**2. Modélisation et Performance (Focus Énergie)**

Le modèle ARIMA(1,1,1) a été retenu pour sa capacité à capturer à la fois la persistance des données (AR1) et l'impact des chocs récents (MA1).

**Validation** : Le test de Ljung-Box confirme que les résidus sont un "bruit blanc", validant la robustesse du modèle.

**Précision** : Les critères AIC et les erreurs de prévision (RMSE/MAE) indiquent que ce modèle est le plus performant pour ce secteur par rapport aux modèles AR ou MA simples.

**3. Prévisions à Court Terme (h= 4)**

Les projections pour les 4 prochaines années suggèrent :Une croissance modérée avec une tendance à la stabilisation de la production énergétique.Une dépendance continue aux facteurs exogènes (contexte géopolitique et transition énergétique) qui pourraient influencer ces prévisions.

**Point économique important** : Les résultats soulignent que, bien que la production industrielle montre des signes de résilience, elle reste conditionnée par un environnement macroéconomique incertain et des transformations structurelles en cours.


# Limites
Bien que le modèle ARIMA(1,1,1) soit robuste pour l'analyse de court terme, l'étude présente plusieurs limites importantes à prendre en compte :

**1.Nature univariée du modèle**: La modélisation repose uniquement sur le passé de la série (auto-corrélation).
Elle ne prend pas en compte les variables exogènes déterminantes comme la variation des prix de l'énergie, les chocs géopolitiques mondiaux ou les changements de politiques fiscales.

**2.Fréquence des données**: L'utilisation de données annuelles limite le nombre d'observations et ne permet pas de capturer les dynamiques de très court terme (saisonnalité mensuelle ou trimestrielle). Une fréquence plus élevée aurait permis une analyse conjoncturelle plus fine.

**3.Incapacité à prévoir les ruptures structurelles**: Le modèle suppose une continuité des tendances passées. Il ne peut pas anticiper des ruptures majeures comme une crise sanitaire soudaine, une innovation technologique de rupture ou un basculement brutal dans la transition énergétique.

**4.Périmètre de généralisation**: L'analyse économétrique approfondie s'est concentrée sur le secteur de l'énergie. Les résultats et la précision du modèle ne sont donc pas directement transposables aux secteurs de l'automobile ou de la pharmacie sans une étude dédiée.







