# Assignment 1 — Linear Regression

Three runnable Jupyter notebooks for SDT 408 Assignment 1. The notebooks reproduce the reference linear-regression workflow and compare fitted coefficients and held-out RMS error across three feature sets and three test/train ratios.

## Contents

| File | Purpose |
|---|---|
| `Assignment1_2_Student.ipynb` | Carsmall: predict horsepower from MPG, MPG plus MPG², and MPG plus MPG² plus weight. |
| `Assignment1_3_Student.ipynb` | Toyota Corolla listings: predict price from year, year plus mileage, and year plus mileage plus mileage². |
| `Assignment1_4_Student.ipynb` | Kaggle CarDekho listings: predict selling price from year, year plus kilometers driven, and year plus kilometers driven plus kilometers driven squared. |
| `carsmall1.csv` | Carsmall input data for item 2. |
| `cars-cleaned.csv` | Toyota Corolla input data for item 3. |
| `cardekho_used_cars.csv` | Kaggle CarDekho input data for item 4. |
| `requirements.txt` | Python dependencies. |
| `DATA_LICENSE.md` | Dataset attribution and license notes. |

The notebook filenames use `Student` because the surname was not supplied. Rename those three files to `Assignment1_<item>_<surname>.ipynb` before submitting if your instructor expects your actual surname in each name.

## Run the notebooks

1. Install Python 3.10 or newer.
2. From this folder, install the dependencies:

   ```bash
   python -m pip install -r requirements.txt
   ```

3. Open any notebook in Jupyter and choose **Run All**. The CSV it reads is in the same folder as the notebook.

Google Colab also works: upload the notebook and its matching CSV, or open the notebook from this repository and place the CSV in the Colab session's working directory.

The notebooks include saved tables and plots from a full run. Run All again if you change the data or code.

## Submission

If the course site accepts one file, upload `Assignment1_submission_Student.zip`. It contains all three `.ipynb` notebooks, all three CSV datasets, and the supporting files. If it accepts multiple files, upload the three notebooks and three CSV datasets individually. A repository URL can also be used where the course site permits a website URL submission.

## Evaluation details

All models use ordinary least squares. Each notebook reports full-data coefficients (`w`, `b`) and evaluates test/train ratios 0.25, 0.5, and 1.0 with a fixed random seed of 42. The final notebook cell contains the coefficient table, RMS table, and a short interpretation. It also contains cells for the cost surface, polynomial-degree comparison, and scaled gradient-descent parameter experiments.

## Sources

- Items 2 and 3 CSVs were provided with the course assignment.
- Item 4 uses the [Kaggle Vehicle dataset from CarDekho](https://www.kaggle.com/datasets/nehalbirla/vehicle-dataset-from-cardekho). Kaggle describes the dataset fields as vehicle name, year, selling price, kilometers driven, fuel, seller type, transmission, and owner. The CSV included here is the `CAR DETAILS FROM CAR DEKHO.csv` file. Kaggle's page requires sign-in to download; the file was retrieved from a [public GitHub mirror](https://github.com/bagassenop/cardekho/blob/main/CAR%20DETAILS%20FROM%20CAR%20DEKHO.csv). See `DATA_LICENSE.md` before redistributing the dataset.
