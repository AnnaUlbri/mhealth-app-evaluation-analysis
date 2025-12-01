# mhealth-app-evaluation-analysis
Statistical analysis of patient and clinical expert involvement in mHealth app development
# mHealth App Evaluation Analysis

**Analyzing the relationship between stakeholder involvement and app quality ratings**

This project examines whether patient and clinical expert involvement during mHealth app development correlates with better quality ratings from two perspectives: usability (non-clinician reviewers) and clinical appropriateness (clinician reviewers).

## 🎯 Research Questions

1. Does patient involvement during app development relate to higher usability scores?
2. Does clinical expert involvement relate to higher clinical appropriateness ratings?
3. How do usability ratings (SUS) correlate with clinical ratings (NPS)?

## 📊 Data Source

This analysis uses publicly available data from the Mobile Health Apps Evaluation Dataset:

> Singh, K., Zhou, X., Ackerman, M. S., & Zheng, K. (2021). Mobile health apps evaluation dataset [Data set]. University of Michigan. https://kdpsingh.lab.medicine.umich.edu/datasets/mobile-health-apps-evaluation-dataset

The dataset contains evaluations of 137 mHealth apps rated by both non-clinician reviewers (using the System Usability Scale - SUS) and clinician reviewers (using Net Promoter Score - NPS).

## 🔬 Methods

### Statistical Analyses
- **Independent samples t-tests** to compare ratings between apps with vs. without stakeholder involvement
- **Pearson correlation** to examine the relationship between SUS and NPS scores
- **Effect size calculations** (Cohen's d) to assess practical significance
- **Reliability analysis** (Cronbach's α) to validate the SUS scale

### Tools
- R (version 4.x)
- RStudio
- Key packages: `tidyverse`, `ggplot2`, `psych`

## 📈 Key Findings

1. **Patient Involvement**: No significant effect on usability scores (p = 0.185), but limited by small sample size (only 13 apps with documented involvement)

2. **Clinical Expert Involvement**: Significant medium-sized effect (Cohen's d = 0.55, p = 0.021), with apps developed with clinical experts receiving higher ratings from clinician reviewers

3. **No Correlation Between Perspectives**: No significant correlation between usability (SUS) and clinical ratings (NPS): r = 0.11, p = 0.217, suggesting these represent independent quality dimensions—or that the NPS question was inappropriately framed for clinical evaluation

## 📁 Repository Structure
```
├── mhealth_analysis.Rmd       # Complete R Markdown analysis
├── figures/                    # Visualization outputs
│   ├── boxplot_patient.png
│   ├── boxplot_clinical.png
│   └── scatterplot_correlation.png
└── README.md
```

## 🚀 How to Reproduce

1. Download the dataset from the [source link](https://kdpsingh.lab.medicine.umich.edu/datasets/mobile-health-apps-evaluation-dataset)
2. Open `mhealth_analysis.Rmd` in RStudio
3. Install required packages: `tidyverse`, `ggplot2`, `psych`
4. Run the R Markdown file to reproduce all analyses and visualizations

## 🔍 Visualizations

### Patient Involvement vs. Usability
![Patient Involvement Boxplot](figures/boxplot_patient.png)

### Clinical Expert Involvement vs. Clinical Ratings
![Clinical Involvement Boxplot](figures/boxplot_clinical.png)

### Correlation Between Perspectives
![Correlation Scatterplot](figures/scatterplot_correlation.png)

## 💡 Discussion Highlights

- The extremely low NPS scores (M = 5.4, 69% "Detractors") suggest methodological issues with the question framing for clinical reviewers
- The field has developed specialized usability scales for patients (G-MAUQ, DHASSP) but lacks equivalent instruments for clinical expert assessment
- Future research needs mixed-methods approaches and clinical effectiveness measures beyond process metrics

## 📚 References

1. Tacke, T., et al. (2024). The German version of the mHealth App Usability Questionnaire (GER-MAUQ). *Digital Health*, *10*, 1–22.
2. Prakash, G. H., et al. (2025). Development and validation of the digital health application satisfaction scale. *Measurement and Evaluations in Cancer Care*, *3*, 100017.
3. Mathews, S. C., et al. (2019). Digital health: A path to validation. *npj Digital Medicine*, *2*, 38.

## 👤 About

This project was developed as part of a UX Research portfolio demonstrating quantitative analysis skills in the digital health domain.

**Connect:** [LinkedIn: https://www.linkedin.com/in/anna-ulbricht/] | [[Portfolio Website: https://www.notion.so/annasportfolio/UX-Research-Portfolio-0e9d7d1a911a480b80edbecf3a611ac3?source=copy_link]

---

*For questions or collaboration opportunities, feel free to reach out!*
