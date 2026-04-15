
# Skillhive: Skill Assessment Platform Using Multi-Factor Evaluation and ML-Based Analysis

## Overview
Skillhive is an advanced skill assessment and learning platform designed for students, particularly B. Tech undergraduates. Unlike traditional assessment systems that focus solely on correctness, Skillhive evaluates user proficiency using a multi-parameter methodology. It incorporates question difficulty, time management, subtopic relevance, and user confidence to provide a comprehensive analysis of learner performance. The platform leverages machine learning—especially Random Forest Regression—to predict user scores and deliver adaptive, personalized feedback.

## Key Features
- **Multi-factor Evaluation:** Considers difficulty, time efficiency, subtopic weightage, and confidence for each question.
- **Adaptive Scoring Engine:** Uses weighted multipliers for each parameter, promoting adaptive testing and user-specific feedback.
- **ML-Based Analysis:** Employs Random Forest Regressor and compares it with other models (Linear, Polynomial, Gradient Boosting) for optimal prediction accuracy.
- **Detailed Analytics:** Provides post-assessment analysis, identifying strengths and areas for improvement.
- **User Feedback Loop:** Continuously improves the platform based on user feedback.

## System Architecture
The system consists of three main modules:
1. **Test Interface:** Presents questions categorized by topic, difficulty, and confidence, adapting in real-time to user performance.
2. **Scoring Engine:** Calculates scores using a composite formula that integrates all evaluation parameters.
3. **Result Analysis Module:** Uses ML models to analyze results and generate actionable feedback.

![System Flowchart](Methodology.png)

## Evaluation Methodology
- **Difficulty-Based Scoring:** Easy (2), Medium (4), Hard (6) points per question.
- **Subtopic Weightage:** Core subtopics get a 1.2x multiplier.
- **Time Efficiency:** <50% time used = 1.5x, <75% = 1.2x multiplier.
- **Confidence Adjustment:** High/Medium/Low confidence modifies score with bonuses/penalties.
- **Composite Score:** Combines all factors for a holistic evaluation.

## Machine Learning Models Compared
- **Linear Regression:** Baseline model for linear relationships.
- **Polynomial Regression:** Captures non-linear patterns but prone to overfitting.
- **Random Forest Regressor:** Ensemble model, best overall performance, robust to overfitting.
- **Gradient Boosting Regressor:** Sequential ensemble, good for complex patterns.

## Model Evaluation Metrics
- **RMSE (Root Mean Square Error):** Measures prediction error magnitude.
- **MAE (Mean Absolute Error):** Average absolute prediction error.
- **R² Score:** Proportion of variance explained by the model.
- **Concordance Correlation Coefficient (CCC):** Measures agreement between predictions and actual values.
- **Cross-Validation R² Mean:** Average R² across 5 folds for generalizability.

## Results Summary
- **Best Model:** Random Forest Regressor
	- RMSE: 0.5276
	- MAE: 0.4384
	- R²: 0.7379
	- CCC: 0.8049
	- Cross-validation R² Mean: 0.4040
	- Comprehensive Score: 0.9180
- **Feature Importance:**
	- Weightage and difficulty are the most predictive features.
	- Time and confidence metrics add value when combined with other features.

![Model Comparison](Img1.jpg)
![Comprehensive Score Comparison](Img2.jpg)
![Model Comparison Summary](Img3.jpg)
![Feature Importance Analysis](Img4.jpg)
![Random Forest Application](Img5.jpg)

## Limitations
- Focused on JavaScript assessments (can be extended to other domains).
- Dataset size and diversity can be improved.
- Does not yet track learning progression over time.
- Current focus is on correctness and performance, not code quality.

## Future Scope
- **AI-Driven MCQ Generation:** Use transformer models (e.g., GPT-3.5) for automated, high-quality question creation.
- **Confidence-Based Assessment:** Enhance adaptive feedback and metacognitive evaluation.
- **Automated Data Preprocessing:** Improve reliability and extensibility for ML models.
- **Broader Algorithm Comparison:** Explore more ML models for classification and regression.
- **Improved MCQ Design:** Align with pedagogical models for higher-order skill assessment.

## Conclusion
Skillhive demonstrates the power of machine learning in educational assessment, moving beyond binary correctness to provide nuanced, multi-dimensional feedback. The platform’s use of Random Forest Regression enables accurate, robust prediction of learner performance, with actionable insights for both students and educators. The methodology and results highlight the importance of integrating multiple assessment factors and advanced analytics for effective skill evaluation.

---

## How to Use
- Review and run the code in `Regression_compaission.ipynb` for model training, evaluation, and analysis.
- Refer to the images for visual summaries of model performance and feature importance.
- Extend or adapt the methodology for other domains or larger datasets as needed.

---

## Authors
- Arunabha Mukhopadhyay
- Dhawse Spandan Yashwant
- Rishi Saxena
- Shanvi Srivastava
- Ranjeet Vasant Bidwe

---

## References
See the main paper for a detailed bibliography and citations.
