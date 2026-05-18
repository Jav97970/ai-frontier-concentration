# The Shrinking Club: Who's Been Pushed Out of Frontier AI Development?

An empirical analysis of how the landscape of AI model development has concentrated — across institutions, organization types, and countries — between 2015 and 2026.

## Key Findings

- **Academia has effectively exited frontier AI.** Universities produced ~45% of notable AI models in 2015. By 2025, that share was 2%. In the first four months of 2026, it's zero.

- **Dozens of major institutions have dropped out.** MIT, Oxford, Cambridge, the Chinese Academy of Sciences, the University of Toronto, and many others no longer produce models that meet notability thresholds.

- **The compute gap explains the exclusion.** By 2024, the median industry model used ~75x more training compute than the median academic model. By 2025, there aren't enough academic models left to measure.

- **Frontier AI is geographically concentrated.** 85 of 123 frontier models (69%) originate from U.S.-based organizations. China has 4. Everyone else is in single digits.

- **Access is shifting from open to API-only.** Fully open model weights have declined as a share of notable models since 2020, replaced by API-gated access.

## About This Analysis

This project examines who has been systematically pushed out of frontier AI development using Epoch AI's Notable AI Models dataset — a database of over 1,000 machine learning models tracked from 1950 to the present. The analysis covers six dimensions: the collapse of academic participation, which specific organizations have exited, the training compute gap between industry and academia, geographic concentration of frontier models, shrinking competition at the top quartile of compute, and trends in model accessibility.

All code, data, and visualizations are included in this repository. The full analysis is in the Jupyter notebook and can be run locally or in Google Colab.

## Data

Source: [Epoch AI — Notable AI Models](https://epoch.ai/data/ai-models) (Creative Commons Attribution 4.0)

The dataset tracks models that meet at least one of: state-of-the-art improvement on a recognized benchmark, over 1,000 citations, historical relevance, or significant real-world deployment. The snapshot used here was downloaded in May 2026. All 2026 figures reflect data through April 24, 2026 only.

## Repository Structure

```
├── the_shrinking_club_clean.ipynb    # Full analysis with code and visualizations
├── notable_ai_models.csv             # Epoch AI dataset (May 2026 snapshot)
└── README.md
```

## Running the Analysis

Clone the repo and run the notebook:

```bash
git clone https://github.com/Jav97970/ai-frontier-concentration.git
cd ai-frontier-concentration
jupyter notebook the_shrinking_club_clean.ipynb
```

Or upload `the_shrinking_club_clean.ipynb` and `notable_ai_models.csv` to [Google Colab](https://colab.research.google.com/) and run all cells.

Requirements: Python 3.8+, pandas, matplotlib, numpy.

## Methodology

Organization type (academia, industry, government) is assigned by Epoch AI based on the lead developing organization. For models with multiple affiliated organizations, the first listed organization is used as the primary affiliation. "Frontier" models are those Epoch classifies as being in the top 10 of training compute at the time of their release. Some organizations that appear as dropouts are actually rebrandings (e.g., Google Brain → Google DeepMind, Facebook AI → Meta AI) and are excluded from the attrition analysis.

## Citation

If you reference this analysis, please cite the underlying data:

```
Epoch AI, "Data on AI Models." Published online at epoch.ai.
Retrieved from https://epoch.ai/data/ai-models. CC-BY 4.0.
```

## License

Analysis code: MIT License. Data: [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/) (Epoch AI).
