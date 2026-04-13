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

## Aviation Accident Data Analysis

The analysis of the cleaned dataset (`AviationData_Cleaned.csv`) produced the following insights:

### Large Aircraft
- Safest models: Boeing 757 variants, Boeing 777, McDonnell Douglas MD‑80/88, Canadair CL‑600.
- These aircraft consistently show low fatal/serious injury fractions, reflecting robust engineering and regulatory standards.

### Small Aircraft
- Safer makes include Waco, Bombardier, Grumman‑Schweizer, Helio, and Maule.
- Safety outcomes are more variable compared to large jets, with some accidents highly survivable and others catastrophic.

### Contextual Factors
- **Weather:** Accidents in clear conditions (VMC) have much lower severity than those in IMC or unknown conditions.
- **Phase of Flight:** Taxi, standing, and landing phases are relatively safe; takeoff, approach, and maneuvering carry higher risk.

### Recommendations
1. **Aircraft Selection:** Favor large commercial jets (e.g., Boeing 757, Boeing 777, MD‑80/88, Canadair CL‑600). For small aircraft, prioritize safer makes such as Waco or Bombardier.
2. **Operational Risk Management:** Strengthen weather‑related decision protocols and emphasize pilot training during critical phases (takeoff, approach, maneuvering).
3. **Safety Strategy:** Combine aircraft model/make performance with contextual risk factors to guide fleet acquisition, operational policies, and training programs.

