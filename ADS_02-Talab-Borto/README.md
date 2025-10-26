Immobilienpreis-Vorhersage Milwaukee

Projektbeschreibung:
Dieses Forschungsprojekt analysiert den Immobilienmarkt in Milwaukee für den Zeitraum 2002 bis 2025 mit dem Ziel, ein robustes maschinelles Lernmodell zur Vorhersage von Immobilienverkaufspreisen zu entwickeln. Das Projekt implementiert den vollständigen Data-Science-Prozess von der Datenakquisition und -bereinigung über Feature Engineering bis hin zur Modellentwicklung und Evaluation.

Projektstruktur:
ADS_02-Immobilienpreisvorhersage/
├── notebooks/
│   └── property_price_analysis.ipynb           # Hauptanalyse inkl. Exploration, Modellierung, Evaluation
├── input/
│   └── 2002-2025-property-sales-data.csv       # Originaldatensatz (Milwaukee Open Data)
├── output/
│   ├── final_model.pkl                         # Trainiertes finales Modell (Optimierter Random Forest)
│   ├── preprocessor.pkl                        # Preprocessing-Pipeline (Skalierung & Encoding)
│   ├── metrics.json                            # Modellmetriken und Performance-Kennzahlen
│   └── model_metadata.pkl                      # Modell-Metadaten und Hyperparameter
├── docs/
│   └── projektbeschreibung.pdf                 # Wissenschaftlicher Report
├── README.md                                   # Projektdokumentation
└──  requirements.txt                           # Python-Abhängigkeiten

Installation und Setup

Voraussetzungen

Python 3.8 oder höher
Git

Installation

1. Repository klonen:

git clone [repository-url]
cd ADS_02-Immobilienpreisvorhersage

2. Virtuelle Umgebung erstellen und aktivieren:

# Mit conda
conda env create -f environment.yml
conda activate ads_immobilien

# Alternativ mit pip
pip install -r requirements.txt

3 Datensatz sicherstellen:

Datei 2002-2025-property-sales-data.csv im input/ Ordner platzieren
Datensatz verfügbar unter: Milwaukee Open Data - Property Sales

Reproduktion der Analyse

Jupyter Notebook (Empfohlen)

Notebook notebooks/property_price_analysis.ipynb öffnen
Alle Zellen sequentiell ausführen
Modelle und Ergebnisse werden automatisch im output/ Ordner gespeichert

Skript-basierte Ausführung

python -m notebooks.property_price_analysis

Wichtige Ergebnisse

Modellperformance

Bestes Modell: Optimierter Random Forest Regressor
Vorhersagegüte: R² = 0.737 (Testdaten)
Durchschnittlicher absoluter Fehler: 27.531 USD (17.5% relativer Fehler)
Bootstrap-Konfidenzintervall R²: [0.695, 0.764]
Geschäftsrelevante KPIs

37.0% der Vorhersagen mit <10% Fehler
63.8% der Vorhersagen mit <20% Fehler
Wichtigste Einflussfaktoren

Nachbarschaft (nbhd) - Mikrolage als dominanter Preisfaktor
Zimmeranzahl (Rooms) - Grundrisseffekt
Stadtbezirk (District) - Administrative Lageeinteilung
Wohnfläche (FinishedSqft) - Grundlegender Werttreiber
Gebäudealter (Building_Age) - Wertminderung über Zeit
Technische Implementierung

Programmiersprache und Bibliotheken

Python 3.12
Machine Learning: scikit-learn, XGBoost
Datenverarbeitung: pandas, numpy
Visualisierung: matplotlib, seaborn
Statistik: scipy
Machine Learning Methoden

Verglichene Algorithmen: Random Forest, Gradient Boosting, XGBoost, Ridge Regression
Hyperparameteroptimierung: RandomizedSearchCV mit 3-facher Cross-Validation
Feature Engineering: Temporale Features, strukturelle Metriken, boolesche Features
Preprocessing: ColumnTransformer mit StandardScaler und OneHotEncoder
Datenverarbeitungspipeline

Datenbereinigung: Behandlung fehlender Werte, Ausreißerentfernung (IQR-Methode)
Feature Engineering: Generierung von 11 neuen Features
Transformation: Log-Transformation der Zielvariable
Modelltraining: Pipeline-basierte Verarbeitung
Evaluation: Umfassende Validierung mit Cross-Validation und Bootstrap-Konfidenzintervallen
Anwendungsfälle

Praktische Implementierung

Automatisierte Immobilienbewertung für Makler und Gutachter
Preisempfehlungen für Immobilienplattformen
Marktanalyse und Trendüberwachung für Investoren
Feature-Analyse zur Identifikation zentraler Preistreiber
Kommunale Planung und Grundsteuerbemessung

Akademischer Kontext

Dieses Projekt wurde im Rahmen der Lehrveranstaltung ADS_02 – Applied Data Science in Machine Learning und Reporting erstellt und dient ausschließlich akademischen Zwecken.

Autor und Betreuung: 

Autor: Talab Borto
Betreuer: Sebastian Seck
Abgabedatum: Oktober 2025