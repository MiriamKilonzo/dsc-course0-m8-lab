# Aviation Accident Analysis
#### Client Context
- The client is an airline/airplane insurer.
- Their concern: financial and safety risk tied to aircraft accidents.
#### Core Questions They Want Answered
- Which aircraft makes/models (professional builds only) show:<br>
      Low rates of total destruction in accidents.<br>
      Low likelihood of fatal or serious passenger injuries.
- Which factors/conditions contribute to safer outcomes?
####  Constraints & Scope
- Only aircraft that could still be active → assume max lifetime of 40 years.
- Filter dataset to 1983 onward.
- Provide separate recommendations for:<br>
     Small aircraft (general aviation, commuter planes).<br>
     Large passenger jets (commercial airline carriers).
- Ensure statistical robustness -> avoid claims based on very few accidents.
#### Deliverables
- Clean dataset (using Pandas).
- Exploratory Data Analysis (EDA): summary stats, plots, tables.
- Evidence-backed recommendations for aircraft safety.
- Identification of at least two general factors influencing accident outcomes

## Data Cleaning Workflow

The dataset was cleaned and prepared in `Aviation_Accidents_Cleaning.ipynb`.  
Key steps included:
- Filtering timeframe (1983–2023) and excluding amateur-built aircraft.
- Handling missing values and constructing key measures (e.g., FatalSerious_Fraction, Destroyed indicator).
- Standardizing manufacturer and model names, retaining statistically significant makes/models.
- Dropping columns with >40% missing values.
- Exporting the cleaned dataset (`AviationData_Cleaned.csv`) for downstream analysis.

For full details, see the notebook: `Aviation_Accidents_Cleaning.ipynb`.

