# Early-Warning with AutoEncoder for GLOF

Glacial Lake Outburst Floods (GLOFs) are a significant climate-induced hazard, requiring innovative solutions for timely prediction and mitigation. This study presents a multifaceted Early Warning System (EWS) for GLOFs, integrating satellite data, time-series analysis, and deep learning. Using Google Earth Engine (GEE), a curated dataset of key parameters—snow reflux, temperature, precipitation, lake size, and water level—was preprocessed to ensure accuracy and consistency. Seasonal and trend decomposition, coupled with anomaly detection via convolutional autoencoders (CAEs), identified deviations in meteorological patterns indicative of potential GLOF events.

A time-series anomaly detection and forecasting model captured short and long-term trends in critical variables. Validated against historical GLOF events in Ronti Lake and South Lhonak Lake, the prototype achieved strong prediction performance with RMSE of 0.0218 and R² value of 0.696. Additionally, 30-day forecasts of parameters such as snow reflux and water levels provided actionable insights into alarming trends.

This study underscores the effectiveness of developing a scalable and transparent Early Warning System for GLOFs. While promising, further refinement is needed to incorporate additional variables and expand coverage to other glacial lakes, paving the way for real-time decision-making and disaster risk reduction in vulnerable regions.

## Result

The proposed EWS for glacial lake outburst floods (GLOFs) integrates time-series analysis with satellite data to address this critical hazard. The system focuses on snow retreat cover and increasing glacial lake volumes as key indicators, leveraging data from flood-prone areas such as Ronti Lake and South Lhonak Lake. A functional prototype was developed using a dataset curated via Google Earth Engine (GEE), incorporating thermodynamic parameters such as snow reflux, temperature variations, precipitation, lake size, and water level.

The data underwent preprocessing, including cleaning, interpolation, outlier removal, and normalization, to ensure consistency. Time series data was structured with lag features to capture historical trends, and seasonal and trend decomposition highlighted cyclical and long-term patterns.

If the reconstruction loss for a sample exceeds this threshold value [14], it can be inferred that the model is observing a pattern with which it is unfamiliar. This sample will be designated as an anomaly.

The model trained on historical data using a 90-10 train-test split and rolling forecast cross-validation to preserve temporal dependencies. The prototype demonstrated promising results in forecasting past GLOF events, achieving RMSE of 0.06 and MSE of 0.3, indicating accurate hazard prediction. A separate test yielded RMSE of 0.0218, MSE of 0.000476, and R² value of 0.696, meaning the model is able to explain approximately 69.6% variance in the target variable (shown in Table 1). Although 30.4% of the variance remains unexplained, these results are encouraging for a prototype, as it captures a significant portion of underlying patterns. The trained AR model successfully forecasted key parameters, such as snow reflux and water level, for the next 30 days, enabling the identification of alarming trends [15]. These predictions were integrated into an early warning system to provide real-time alerts for potential GLOFs.

### Table 1. Performance Metrics for Time-Series Prediction

| Metric   | Training | Testing  | Interpretation          |
|----------|----------|----------|-------------------------|
| RMSE     | 0.06     | 0.0218   | Low prediction error    |
| MSE      | 0.3      | 0.000476 | Low squared error       |
| R²       | -        | 0.696    | Strong correlation      |
