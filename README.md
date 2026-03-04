# MachineLearningGrundlagen

Dieses Projekt bietet eine Einführung in die Grundlagen des Machine Learning.

Das Projekt besteht aus:

- Explorative Datenanalyse (EDA)

- Mathemische Konzepte

   - Logistisches Modell mit zugehörigem Gradienten

   - Kostenfunktionen ( mse und bce)

   - Gradient Descent / Gradientenabstiegverfahren

- Linearer SVM Klassifikator mit MNIST

# Explorative Datenanalyse (EDA)

## Iris Datensatz
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

## MNIST Datensatz

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

Im projekt wurde das Modell \begin{equation}
    h_\theta(x) = \frac{1}{1 + \exp(-\theta_{0} - \theta_{1}x_1 - \dots - \theta_k x_k) }
\end{equation} 
für den Parametervektor $\theta = \begin{pmatrix}\theta_0\\\theta_1\\\vdots\\\theta_k\end{pmatrix}$

Mit zugehörigem Gradienten (Jacobi-Martrix)

Matrix $G\in\mathbb{R}^{N\times(k+1)}$ mit $G_{i,j} = \frac{\partial h_\theta(x^{(i)})}{\partial \theta_j}$ 

wobei gilt

$\frac{\partial h_\theta(x^{(i)})}{\partial \theta_j}
= h_\theta(x^{(i)}) \left(1 - h_\theta(x^{(i)})\right) x^{(i)}_j$,  
 mit $x^{(i)}_0 = 1$.

Anschließend wurde eine logitische Funktion mit einem dem gewählten Parametervektor theta = [5, -5, 7] erzeugt und im Streuduagramm mit einem Konturplut dargestellt.

<img width="376" height="278" alt="download-3" src="https://github.com/user-attachments/assets/e1b0d860-b34a-4aa2-832a-434aa4d26eac" />

Weitere Details und Infos sind im Notebook zu finden.
