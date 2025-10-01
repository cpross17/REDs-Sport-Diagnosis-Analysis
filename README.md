# RED-s Sport Classification Dataset

## Overview
This dataset contains sport-specific observations of Relative Energy Deficiency in Sport (RED-s) prevalence extracted from 56 published studies, representing 15,314 female athletes. The data was compiled to examine how sport characteristics and screening tool methodology affect reported RED-s prevalence rates.

## Dataset Description
- **Total observations:** 145 sport-specific entries
- **Total athletes represented:** 15,314
- **Source studies:** 56 peer-reviewed publications
- **Data collection period:** May 2025 - Sep 2025

## Variables

### Sport Classification Variables
- `Aesthetic_Scoring`: Whether sport involves aesthetic judging in the scoring component (Yes/No)
- `Sport_Type`: Team vs individual sport structure (Team/Individual)
- `Fitness_Category`: Primary fitness demands on 1-5 scale
  - 1 = Pure endurance (e.g. triathalon, marathon, cross-country)
  - 2 = Endurance-dominant (e.g. dance, swimming, crew)
  - 3 = Combination (e.g. ball sports)
  - 4 = Strength-leaning (e.g. ice hockey, gymnastics, cheer)
  - 5 = Pure strength (e.g. weightlifting, body building)
- `Competition_Attire_Modesty_Level`: Uniform coverage on 1-5 scale
  - 1 = Minimal coverage; skin-exposing (midriff or upper thighs), tight-fitting uniforms (e.g., bikinis, briefs, leotards)
  - 2 = Moderate coverage; tight or fitted gear (e.g., compression shorts/tops, spandex kits)
  - 3 = Athletic coverage; moderate modesty (e.g., loose shorts/jerseys in ball sports, golf, tennis)
  - 4 = Full coverage due to tradition or function (e.g., equestrian, fencing, softball, karate)
  - 5 = Body-hiding uniforms with bulky or layered gear that obscure physique entirely (e.g., ice hockey, tackle football, goalkeepers)
- `Weight_or_Physique_Class_Required`: Whether sport requires weigh-ins for competition (Yes/No) (e.g. weightlifting, crew, combat sports)

### Outcome Variable
- `%_REDs_Risk_Reported`: Proportion of athletes identified as at-risk for RED-s in each observation
- `High Risk?`: Binary indicator of whether the observation's RED-s prevalence was above the median for its specific screening tool (Yes/No). This variable standardizes risk assessment within measurement method to control for tool-specific bias. Median thresholds varied by tool: LEAF-Q (63.0%), EA calculation (63.0%), MD (17.3%), etc.

### Measurement Variables
- `Primary_Screening_Tool_Used`: Method used to assess RED-s risk. When multiple indicators were available in a single study, the following prioritization hierarchy was applied:

**Risk % Prioritization Hierarchy (Screening Tools)**

1. LEAF-Q (≥8 cutoff) – use reported prevalence
2. Calculated Energy Availability (EA <30 kcal/kg FFM) – use reported prevalence
3. DEAQ (Dance-Specific Energy Availability Questionnaire) – use reported prevalence
4. Disordered Eating screen (DE screen) as proxy for LEA – use prevalence from EDE-Q, EAT-26, or similar validated DE screen above clinical cutoff
5. Composite Triad risk – if study reports prevalence of athletes meeting ≥1 Triad criteria (LEA/DE, MD, or low BMD)
6. Menstrual dysfunction (MD) – use prevalence of oligomenorrhea/amenorrhea (≤10-11 menses per year)
7. Lab measures (e.g., ferritin <20 ng/ml, hemoglobin <12 g/dl, other clinical markers of deficiency) – use prevalence of athletes below cutoff
8. Low BMD – use prevalence of athletes with BMD Z-score ≤-1.0 (or equivalent)

### Other Variables
- `Sport_Type`: Specific sport (e.g., Soccer, Volleyball, Ballet)
- `N`: Sample size for each observation

## Data Collection Methods
Sport-specific prevalence data was extracted from published studies reporting RED-s risk or related indicators (low energy availability, menstrual dysfunction, low bone mineral density). Each sport mentioned in a study was coded as a separate observation. Sport characteristics were classified independently by the research team based on established sport typologies and competition requirements.

## Intended Use
This dataset supports research on:
- Sport-specific RED-s risk factors
- Measurement bias in RED-s screening tools
- Meta-analysis of RED-s prevalence across sports
- Development of targeted screening protocols

## Citation
If you use this dataset, please cite: Ross, Carolyn, "Sport-Specific Risk Factors and Measurement Bias in RED-s: A Multi-Factor Classification Analysis," MIT Sloan Sports Analytics Conference, 2025.

## Contact
cpross17@gmail.com

## License
This dataset is shared under CC BY 4.0 (Creative Commons Attribution 4.0 International). You are free to use, modify, and distribute with attribution.
