# MachineLearningGrundlagen

(Noch in überarbeitung)

Dieses Projekt bietet eine Einführung in die Grundlagen des Machine Learning.

Das Projekt besteht aus:

- Explorative Datenanalyse (EDA)

- Mathemische Konzepte

   - Logistisches Modell mit zugehörigem Gradienten

   - Kostenfunktionen ( mse und bce)

   - Gradient Descent / Gradientenabstiegverfahren

- Linearer SVM Klassifikator mit MNIST

# Explorative Datenanalyse (EDA)

### Iris Datensatz
**Zum Datensatz**: 

Dieser besteht aus Eigenschaften der Blüten verschiedener Lilienarten. Im Datensatz sind die Eigenschaften der Blüten, die Features, unter data hinterlegt. Die Lilienart ist im target kodiert.

Im Projekt wurde auf folgende Fragestellungen eingegangen:

- wie viele Datenpunkte enthält der Datensatz

- wie viele verschiedene Lilienarten sind im Datensatz enthalten

- welche Eigenschaften der Blüten werden notiert

Anschließend wurde ein Streudiagramm der ersten beiden Features, aufgeschlüsselt nach Art der Blüte erstellt.

**Ergebnisse**

- der Datensatz enthält 150 Datenpunkte
- Es gibt 3 verschiedene Lilienarten im Datensatz ('setosa' 'versicolor' 'virginica')
- Die Blüten haben folgende Eigenschaften: 'sepal length (cm)', 'sepal width (cm)', 'petal length (cm)', 'petal width (cm)'

**Streudiagramm**

<img width="387" height="278" alt="download-5" src="https://github.com/user-attachments/assets/bcfb378f-a5a3-4a4c-b7f6-84507b50c144" />

ERKLÄRUNG!!!!!!

### MNIST Datensatz

Dieser besteht aus Bilder handgeschriebener Ziffern (0–9). Die Pixelwerte der 28×28 Bilder sind als Features unter data hinterlegt. Die jeweilige Ziffer ist im target codiert.

Im Projekt wurde auf folgende Fragestellungen eingegangen:

- Anzahl und Form der Datenpunkte

- Plot der ersten 10 Datenpunkte an

**Ergebnisse**

- der Datensatz hat 7000 Datenpunkte und welche form?


<img width="1127" height="122" alt="download-6" src="https://github.com/user-attachments/assets/69144291-80b9-4910-8bde-c55e214c5cae" />

(Die ersten 10 Datenpunkte)

## Mathematische Modelle

### Logistisches Modell mit zugehörigem Gradienten

Im Projekt wurde das Modell logitische Modell mit zugehörigem Gradienten implmentiert.

Anschließend wurde eine logitische Funktion mit einem dem gewählten Parametervektor theta = [5, -5, 7] erzeugt und im Streuduagramm mit einem Konturplut dargestellt.

<img width="376" height="278" alt="download-3" src="https://github.com/user-attachments/assets/e1b0d860-b34a-4aa2-832a-434aa4d26eac" />

Weitere Details und Infos sind im Notebook zu finden.

### Kostenfunktionen

Im Projekt wurde die mse und bce Kostenfunktion implementiert.
Anschließend wurd die Kostenlandschaft untersucht.

<img width="718" height="264" alt="download-4" src="https://github.com/user-attachments/assets/e9b180ab-c5c4-4658-a623-6372507f5f9b" />

Der BCE-Plot zeigt eine glatte elliptisch förmige Landschaft.
Das Modell findet von jedem Startpunkt aus schnell und direkt den Weg zum Ziel (globales Minimum).

Der MSE-Plot zeigt eine unebene Landschaft mit flachen Bereichen.
DasModell bleibt leicht stecken, da es in der flachen Ebene keine Richtung mehr für die minimierung findet

**Fazit**

Die Visualisierung bestätigt, dass BCE für Klassifikationsaufgaben deutlich besser ist, da der Lernprozess stabil und zielgerichtet verläuft

### Gradient Descent

Im Projekt wurde das Gradientenabstiegverfahren implementiert. Das Modell soll universell für verschiedene mathematische Modelle verwendbar sein. 
Anschließend wurde das verfahren für die mse und bse kostenfukntion benutzt.

# Linearer SVM Klassifikator mit MNIST

**Ziel** 

Es soll ein möglicht optimaler SVM Klassifikatir auf die MNIST-Daten trainiert werden.

**Vorgehensweise**
Dafür wurden folgende Punkte untersucht und kam folgendes raus

- Effekt der Trainingsdatensatzgröße für verschiedene Kernel-Funktionen
<img width="386" height="270" alt="download-7" src="https://github.com/user-attachments/assets/39548ce8-a22d-4b9b-9308-284790fa45ca" />


- Rolle des Hyperparameters  𝐶 für das Training einer SVM
- 
<img width="330" height="429" alt="down![Uploading download-9.png…]()
load-8" src="https://github.com/user-attachments/assets/71cd32fa-1082-4b37-814d-84815b1f126e" />

<img width="339" height="429" alt="download-9" src="https://github.com/user-attachments/assets/19146d01-c7b9-40a2-801a-b4feb1e0dd4b" />


Anhand dieser Erkenntnisse wurde folgendes ausgewählt:

Kernel = rbf, weil es im Plot im vergleich zu anderen Kernels die höchste accuracy aufzeigt (bei 10^4 Trainingsdaten)

C = 5.0, weil danach kein signifikanter anstieg zu sehen war

###Ergebnisse

**Accuracy** 

Das Modell erreicht eine Accuary von 0.9679, was als hoch zu bewerten ist.

**Confusion Matrix**


<img width="319" height="278" alt="download-10" src="https://github.com/user-attachments/assets/ef4b1d0c-7033-46d3-ac20-52e067f47381" />

**Plot der ersten 100 Fehlklassifikationen (von 321 vielen):**




<img width="3911" height="3882" alt="download-11" src="https://github.com/user-attachments/assets/bc725468-8725-443f-9fed-f981f8e62bb5" />


#

Anmerkung: 
Im Darkmode können die Beschriftungen der Diagramme 'unsichtbar' werden-
