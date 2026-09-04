# Individuele data-analyseopdracht: treinverstoringen voorspellen

In deze repo staan de bestanden voor mijn data-analyse over treinverstoringen. 
Ik heb proberen antwoord te geven op de vraag: " Kan op het moment dat een treinverstoring begint worden voorspeld of deze langer dan 60 minuten zal duren, op basis van de oorzaak, het getroffen traject, het aantal getroffen stations en het startmoment?"
Om antwoord te geven op deze vraag heb ik gebruik gemaakt van de CRISP-DM methode. Ik heb bij sommmige opdrachten van opdracht 4 ChatGPT als hulpmiddel gebruikt, heb hem enkel gebruikt om te vragen wat er van me gevraagd werd.

## Starten

Plaats de volgende bestanden in dezelfde map:

- Studenttemplate_CRISP-DM_treinverstoringen_ingevuld.ipynb

- Dataset.csv

- prepared_train_disruptions.csv (die is automatisch gemaakt door de notebook)

Open het notebook in JupyterLab en kies Restart Kernel and Run All.

## Python en packages

Getest met Python 3.13. Benodigde packages:

- pandas

- numpy

- matplotlib

- seaborn

- scikit-learn

- jupyter

Installatievoorbeeld:
` python -m pip install pandas numpy matplotlib seaborn scikit-learn jupyterlab `

## Analyse

In de notebook wordt de CRISP-DM-methode gebruikt tot en met Evaluation. Het model voorspelt of een treinverstoring langer dan 60 minuten duurt.

Voor de voorspelling gebruiken we alleen gegevens die al bekend zijn wanneer de verstoring begint. Gegevens zoals end_time, duration_minutes, long_disruption en rdt_id gebruiken we daarom niet.

We gebruiken een 80/20 verdeling voor de train- en testdata. Daarna vergelijken we een paar modellen: een simpel basismodel, logistische regressie en een random forest. De modellen worden met 5-fold cross-validatie met elkaar vergeleken.

## Output

De notebook maakt ook het bestand prepared_train_disruptions.csv. Dit is de dataset die is voorbereid voor het model.






