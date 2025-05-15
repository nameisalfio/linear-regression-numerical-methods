# Linear Regression Numerical Methods

Analisi comparativa di metodi numerici per regressione lineare applicati al dataset WHO dell'aspettativa di vita globale.

## Descrizione del Progetto

Questo repository contiene l'implementazione e l'analisi di cinque diversi metodi numerici per la risoluzione di problemi di regressione lineare. La ricerca confronta metodi diretti (Least Squares, SVD, QR Decomposition) e metodi iterativi (Conjugate Gradient, Adam Optimization), valutandone efficienza computazionale, stabilità numerica e performance predittiva.

Il dataset utilizzato è il "Life Expectancy Data" dell'Organizzazione Mondiale della Sanità (WHO), che contiene indicatori sanitari, socioeconomici e demografici per diversi paesi nel periodo 2000-2015.

## Contenuti del Repository

- `Life Expectancy Data.csv.xls` - Dataset dell'OMS sull'aspettativa di vita
- `linear-regression-tutorial.ipynb` - Jupyter notebook con l'implementazione dei metodi e l'analisi
- `README.md` - Questo file

## Metodi Implementati

### Metodi Diretti
1. **Least Squares (Equazioni Normali)** - Soluzione diretta di $(X^TX)^{-1}X^Ty$
2. **Singular Value Decomposition (SVD)** - Utilizzo della decomposizione $X = U\Sigma V^T$
3. **QR Decomposition** - Utilizzo della decomposizione $X = QR$

### Metodi Iterativi
4. **Conjugate Gradient** - Algoritmo iterativo ottimizzato per funzioni quadratiche
5. **Adam Optimization** - Algoritmo adattivo di ottimizzazione del gradiente

## Risultati Principali

- I metodi diretti e il Conjugate Gradient convergono alla stessa soluzione per problemi ben condizionati
- Il Conjugate Gradient mostra una convergenza drasticamente più rapida rispetto ad Adam (≈10 vs >500 iterazioni)
- L'estensione a un modello polinomiale di grado 2 riduce l'errore del 40% rispetto al modello lineare, evidenziando la natura non lineare delle relazioni nel dataset

## Come Utilizzare

#### Clonare il repository

```bash
git clone https://github.com/tuousername/linear-regression-numerical-methods.git
cd linear-regression-numerical-methods
```

#### Installare le dipendenze
```bash
pip install numpy pandas matplotlib scikit-learn jupyter
```

#### Avviare Jupyter Notebook
```bash
jupyter notebook linear-regression-tutorial.ipynb
```

## Struttura del Notebook

Il notebook `linear-regression-tutorial.ipynb` è organizzato nelle seguenti sezioni:

1. Definition & Working principle: Introduce la regressione lineare, i suoi principi e la rappresentazione dell'ipotesi per regressione semplice e multipla.
2. Import Library and Dataset: Importazione delle librerie Python necessarie e caricamento del dataset.
3. 📊 Dataset Structure: Descrizione della struttura del dataset, dettaglio delle feature, obiettivo dell'analisi e un esempio di equazione di regressione.
4. Matrix Formulation: Spiegazione della formulazione matriciale per la regressione lineare.
5. Cost function: Definizione della funzione di costo (OLS/MSE) e la sua rappresentazione matriciale.
6. Normal Equation: Derivazione matematica della Normal Equation per risolvere analiticamente la regressione lineare.
7. Problem of Ill-Conditioning and Multicollinearity in Regression Models: Discussione del problema della multicollinearità, i suoi effetti e le soluzioni (Ridge e Lasso Regression).
8. Exploratory data analysis: Analisi esplorativa dei dati, inclusi grafici come:
  - Relazione tra GDP e Aspettativa di Vita (lmplot)
  - Matrice di Correlazione
  - Analisi dei Violin Plots (Aspettativa di vita vs Stato; GDP vs Stato)
  - Analisi dei Boxplot (Aspettativa di vita vs Categoria GDP e Stato)
  - Scatter Plot (Aspettativa di vita vs GDP, con HIV/AIDS come hue)
9. Data Preprocessing: Passaggi di pre-elaborazione dei dati, inclusa la divisione in set di training e test e la normalizzazione.
10. Model Building: Definizione e implementazione di diversi modelli di regressione (Least Squares, SVD, QR, Conjugate Gradient, Adam). Include la valutazione di questi modelli.
11. Polynomial Model with Ridge Regularization: Spiegazione e implementazione della regressione polinomiale con regolarizzazione Ridge.
12. Linear vs. Polynomial Model: Confronto delle performance tra il modello lineare semplice e il modello polinomiale regolarizzato.
13. 📌 Conclusions: Riassunto dei risultati, dei principali insegnamenti e considerazioni finali.

## Requisiti

- Python 3.6+
- NumPy
- Pandas
- Matplotlib
- Scikit-learn (facoltativo, per confronto)
- Jupyter Notebook

## Autore

Alfio Spoto - Università di Catania  
Dipartimento di Matematica e Informatica

## Riferimenti

- Golub, G. H., & Van Loan, C. F. (2013). Matrix Computations (4th ed.)
- Nocedal, J., & Wright, S. J. (2006). Numerical Optimization (2nd ed.)
- Kingma, D. P., & Ba, J. (2014). Adam: A Method for Stochastic Optimization
- Hestenes, M. R., & Stiefel, E. (1952). Methods of Conjugate Gradients for Solving Linear Systems
- Dataset: WHO Life Expectancy Data (2000-2015)
