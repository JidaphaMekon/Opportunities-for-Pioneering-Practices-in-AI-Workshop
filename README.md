# Opportunities-for-Pioneering-Practices-in-AI-Workshop

Opportunities for Pioneering Practices in AI Workshop 2 (OPPA2 2025) which is  a conference from  November 12-14, 2025
Dataset and Code Preparation for the Conferences Workshop.

The committee identified the following weaknesses in the paper that should be improved:
REVIEW 1--> Completed all comment.


Review 2 -->
1. Risk of Improper Time-Series Validation**

   * *Weakness:* The study uses a standard shuffled 80/20 split, which risks data leakage from the future into the training set. This approach is not well-suited for time-series forecasting.
   * *Improvement:* Adopt a more robust validation strategy by applying cross-validation with a chronological split. The dataset will be divided into 70% training, 15% validation, and 15% testing, and a sliding window approach with a window size of 60 and step size of 1 will be implemented to better reflect real-world forecasting scenarios.

2.  Limited Generality
Weakness: The analysis is restricted to a single stock and a short time horizon.
Improvement: Extend the study to include ten companies from the Nasdaq Mega Cap Technology sector. Expand the time horizon to cover the period from 2019 to 2024, thereby capturing broader market dynamics, including the impact of chronic crises.

3. **Lack of Baseline Comparisons and Reproducible Code**

   * *Weakness:* The study does not include comparisons with widely used time-series forecasting baselines such as ARIMA, Prophet, LSTM, or Temporal Fusion Transformers (TFT). In addition, the absence of reproducible code limits transparency and verifiability.
   * *Improvement:* Implement LSTM and Prophet models with interpolation methods to serve as comparative baselines. Apply cross-validation and incorporate lagged features (e.g., 7-day lag) to ensure a fair and robust evaluation. Provide well-documented, reproducible code to allow others to replicate the experiments.

4.  **Validation Methodology**

   * *Weakness:* The current validation strategy does not adequately prevent look-ahead bias, and scaling may inadvertently include information from the test set.
   * *Improvement:* Perform validation using more robust methodologies, such as walk-forward or rolling cross-validation, while ensuring that data scaling is applied strictly to the training set in each fold. This approach better reflects real-world forecasting conditions and prevents data leakage.
5. **Statistical Significance of Model Comparisons**

   * *Weakness:* The study does not assess whether differences in forecasting performance across models are statistically significant. Without formal testing, conclusions about model superiority may be unreliable.
   * *Improvement:* Incorporate statistical significance testing by applying Diebold–Mariano (DM) tests along with complementary approaches such as paired t-tests. These methods will evaluate whether observed performance differences between forecasting models are meaningful, providing stronger evidence when comparing baseline models and the proposed approach.

6.  **Baseline Models and Alternative Pipeline**

   * *Weakness:* The current study does not include comparisons against established time-aware baseline models and relies solely on interpolation-based preprocessing. This limits the robustness of the evaluation.
   * *Improvement:* Extend the analysis to include comparisons with widely used baseline models such as ARIMA, Prophet, LSTM, and Temporal Fusion Transformers (TFT). In addition, evaluate an alternative pipeline that uses only trading days and incorporates holiday dummy variables, without applying interpolation, to serve as a benchmark against the interpolation-based approach.

7. **Imputation Techniques and Stratified Analysis**

   * *Weakness:* The study relies on a limited set of interpolation methods for handling missing values, which may not fully capture the dynamics of stock price behavior during holiday gaps. Furthermore, model performance is not analyzed in relation to the varying lengths of holiday periods.
   * *Improvement:* Explore more advanced imputation techniques such as Kalman filtering, state-space models, seasonal spline interpolation, or shock-adjusted Last Observation Carried Forward (LOCF). Additionally, conduct a stratified analysis of model performance based on the length of the holiday period to provide deeper insights into how different gaps affect predictive accuracy.

Reviwer 3--> 

1. The introduction needs to be revised.----> if the datasets are available online, please provide proper references to their sources. yahoo fihance
2. The authors should also provide more detailed explanations of Figures 1 and 2 within the body text.
   
   
