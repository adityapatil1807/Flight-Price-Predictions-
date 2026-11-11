# Flight Price Prediction

Predicts flight ticket prices between 6 Indian cities using Linear Regression (pandas, numpy, matplotlib, scikit-learn).

![AI101 Mini-Project](https://img.shields.io/badge/AI101-Mini--Project-blue) ![Team](https://img.shields.io/badge/Team-52-blue) ![Python](https://img.shields.io/badge/Python-3.14%2B-blue)

<!-- FILL: replace XX with your team number -->

## Team and roles

| Member | Entry no. | Role |
|---|---|---|
| Aditya Patil | 2026AIB1065 | Documentation lead |
| Shaurya Kambhoj | 2026MCB1567 | Execution lead |
| Nipun Singhal | 2026EEB1386 | PPT lead |
| Jarmik Jethwa | 2026EEB1357 | Video lead |

All four members contributed code (see commit history).

## Project overview

The user enters a **boarding point, dropping point, time of flight, class** and **how many days before** the flight they are booking. The trained model predicts the ticket price and shows graphs.

- **Dataset:** `data/Dataset.csv` (flight tickets between 6 Indian cities) <!-- FILL: add source link, rows and columns -->
- **Model:** Linear Regression inside a scikit-learn `Pipeline` (`SimpleImputer` + `OneHotEncoder` + `ColumnTransformer`)
- **Metrics:** MAE, MSE, RMSE and R²

## Project structure

```
Flight-Price-Predictions-/
├── data/
│   └── Dataset.csv          # flight price dataset
├── CODE.ipynb                # main notebook (run this)
├── requirements.txt         # pinned library versions
├── outputs/                 # screenshots of expected output
├── docs/                    # 5-slide presentation
└── README.md
```

## Setup

**Tested on:** Python 3.14.7, Windows 11. 

**Required:** Python 3.14 or newer, Git, and an internet connection for the first install.

> Run all commands below in a terminal opened **inside the project folder**.
> You can use Command Prompt, PowerShell, Git Bash, VS Code's terminal, or Terminal on macOS/Linux.

### 1. Clone the repository

```bash
git clone https://github.com/adityapatil1807/Flight-Price-Predictions-.git
cd Flight-Price-Predictions-
```

### 2. Create a virtual environment

```bash
python -m venv venv
```

> On macOS / Linux, use `python3 -m venv venv` if `python` is not found.
> A virtual environment is optional but recommended. If you skip it, go straight to Step 4.

### 3. Activate the virtual environment

Use the line for your terminal:

- **Command Prompt:** `venv\Scripts\activate`
- **PowerShell:** `venv\Scripts\Activate.ps1`
- **Git Bash (Windows):** `source venv/Scripts/activate`
- **macOS / Linux:** `source venv/bin/activate`

You should see `(venv)` at the start of the terminal line.

### 4. Install the required libraries

```bash
pip install -r requirements.txt
```

Libraries used: numpy, pandas, matplotlib, scikit-learn, notebook, ipykernel.

## How to run

1. Open the project folder **(Where the repository is saved)**.
2. Click **CODE.ipynb**.
3. Click **Kernel → Restart & Run All**.
4. The notebook reads the dataset from `data/Dataset.csv`.
5. Wait for Sections 1 to 11 to finish. They load the data, train the Linear Regression model, and print MAE, MSE, RMSE and R².
6. **Section 12 asks for input.** An input box appears below the cell. Type each value and press Enter. Example:

   | Question | Example answer |
   |---|---|
   | Boarding point | Delhi |
   | Dropping point | Mumbai |
   | Time of flight | Morning |
   | Class | Economy |
   | Days before the flight (1 to 49) | 15 |

   The valid options for each question are shown in square brackets in the prompt. Boarding and dropping point cannot be the same.
6. Section 13 then draws two graphs for your flight: predicted price vs days before the flight, and predicted price by time of flight.

**Expected output:** the evaluation metrics (Section 9), the graphs in Sections 4, 10 and 13, and the predicted price for your flight (Section 12).


## Troubleshooting

| Problem | Fix |
|---|---|
| `python` is not recognized | Install Python 3.14 from python.org and tick "Add python.exe to PATH". |
| PowerShell says scripts are disabled | Use Command Prompt, or run `Set-ExecutionPolicy -Scope CurrentUser RemoteSigned`. |
| `ModuleNotFoundError` | The virtual environment is not active. Repeat Step 3, then Step 4. |
| `FileNotFoundError` for the dataset | Run `jupyter notebook` from the project root folder, not from another folder. |
| The cell keeps running with `[*]` | It is waiting for your input in Section 12. Type your answer in the box under the cell. |
| Kernel not found / no Python option | Run `python -m ipykernel install --user --name=venv` and select the `venv` kernel. |

## Links

- Slides (5): `[Final_pdf.pdf](https://github.com/adityapatil1807/Flight-Price-Predictions-/blob/main/Final_pdf.pdf)
- Video (max 5:00): <!-- FILL: unlisted YouTube or Drive link, set to "anyone with the link" -->

## AI-use disclosure

<!-- FILL: edit to match what your team actually did, including how you checked the output -->

- Claude: helped debug notebook errors, improve graph styling, and draft the setup instructions in this README; we tested every step on a fresh clone.
- AI was used to sort the dataset
- No AI was used to generate the dataset or the results.

