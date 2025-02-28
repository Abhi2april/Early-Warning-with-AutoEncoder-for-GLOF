# Early-Warning with AutoEncoder for GLOF -> OUR SOLUTION IN SMART INDIA HACKATHON'S PROBLEM STATEMENT -VISIT OUR [WEBSITE](https://glof-plum.vercel.app/)

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


## References
## References

[1] S. Harrison, J. S. Kargel, C. Huggel, J. Reynolds, D. H. Shugar, R. A. Betts, A. Emmer, N. Glasser, U. K. Haritashya, J. Klimeš, L. Reinhardt, Y. Schaub, A. Wiltshire, D. Regmi, and V. Vilímek, “Climate change and the global pattern of moraine-dammed glacial lake outburst floods,” *The Cryosphere*, vol. 12, no. 4, pp. 1195–1209, 2018.

[2] Rayees Ahmed, Gowhar Farooq Wani, Syed Towseef Ahmad, Mehebub Sahana, Harmeet Singh, and Pervez Ahmed, “A review of glacial lake expansion and associated glacial lake outburst floods in the Himalayan region,” *Earth Systems and Environment*, vol. 5, no. 3, pp. 695–708, 2021.

[3] Nazir Ahmed Bazai, Peng Cui, Paul A. Carling, Hao Wang, Javed Hassan, Dingzhu Liu, Guotao Zhang, and Wen Jin, “Increasing glacial lake outburst flood hazard in response to surge glaciers in the Karakoram,” *Earth-Science Reviews*, vol. 212, pp. 103432, 2021.

[4] Yuchen Fang, Jiandong Xie, Yan Zhao, Lu Chen, Yunjun Gao, and Kai Zheng, “Temporal-frequency masked autoencoders for time series anomaly detection,” in *2024 IEEE 40th International Conference on Data Engineering (ICDE)*, 2024, pp. 1228–1241.

[5] Pratima Pandey, Prakash Chauhan, C. M. Bhatt, Praveen K. Thakur, Suresh Kannaujia, Pankaj R. Dhote, Arijit Roy, Santosh Kumar, Sumer Chopra, Ashutosh Bhardwaj, and S. P. Aggrawal, “Cause and process mechanism of rockslide triggered flood event in Rishiganga and Dhauliganga river valleys, Chamoli, Uttarakhand, India using satellite remote sensing and in situ observations,” *Journal of the Indian Society of Remote Sensing*, vol. 49, no. 5, pp. 1011–1024, May 2021.

[6] Ashim Sattar, Ajanta Goswami, Anil V. Kulkarni, Adam Emmer, Umesh K. Haritashya, Simon Allen, Holger Frey, and Christian Huggel, “Future glacial lake outburst flood (GLOF) hazard of the South Lhonak Lake, Sikkim Himalaya,” *Geomorphology*, vol. 388, pp. 107783, 2021.

[7] Ashim Sattar, Ajanta Goswami, and Anil V. Kulkarni, “Hydrodynamic moraine-breach modeling and outburst flood routing - a hazard assessment of the South Lhonak Lake, Sikkim,” *Science of The Total Environment*, vol. 668, pp. 362–378, 2019.

[8] Caroline Taylor, Tom R. Robinson, Stuart Dunning, J. Rachel Carr, and Matthew Westoby, “Glacial lake outburst floods threaten millions globally,” *Nature Communications*, vol. 14, no. 1, pp. 487, 2023.

[9] Noel Gorelick, Matt Hancher, Mike Dixon, Simon Ilyushchenko, David Thau, and Rebecca Moore, “Google Earth Engine: Planetary-scale geospatial analysis for everyone,” *Remote Sensing of Environment*, vol. 202, pp. 18–27, 2017, Big Remotely Sensed Data: tools, applications and experiences.

[10] Sanjaya Gurung, Saroj Dhoj Joshi, and Binod Parajuli, “Overview of an early warning system for glacial lake outburst flood risk mitigation in Dudh-Koshi Basin, Nepal,” *Sciences in Cold and Arid Regions*, vol. 13, no. 3, pp. 206–219, 2021.

[11] Salvador García, Sergio Ramírez-Gallego, Julián Luengo, José Manuel Benítez, and Francisco Herrera, “Big data preprocessing: methods and prospects,” *Big Data Analytics*, vol. 1, no. 1, pp. 9, 2016.

[12] Pankaj Malhotra, Anusha Ramakrishnan, Gaurangi Anand, Lovekesh Vig, Puneet Agarwal, and Gautam Shroff, “LSTM-based encoder-decoder for multi-sensor anomaly detection,” 2016.

[13] Haipeng Ji, Xiaoqiang Qiao, Jiang Zhang, Yihang Du, Tao Zhang, and Fayu Wan, “Spectrum anomaly detection under multiple sensors using metric-adversarial learning,” *IEEE Communications Letters*, 2025.

[14] Hongsong Chen, Xingyu Li, and Wenmao Liu, “Multivariate time series anomaly detection by fusion of deep convolution residual autoencoding reconstruction model and ConvLSTM forecasting model,” *Computers & Security*, vol. 137, pp. 103581, 2024.

[15] A. Emmer, S. K. Allen, M. Carey, H. Frey, C. Huggel, O. Korup, M. Mergili, A. Sattar, G. Veh, T. Y. Chen, S. J. Cook, M. Correas-Gonzalez, S. Das, A. Diaz Moreno, F. Drenkhan, M. Fischer, W. W. Immerzeel, E. Izagirre, R. C. Joshi, I. Kougkoulos, R. Kuyakanon Knapp, D. Li, U. Majeed, S. Matti, H. Moulton, F. Nick, V. Piroton, I. Rashid, M. Reza, A. Ribeiro de Figueiredo, C. Riveros, F. Shrestha, M. Shrestha, J. Steiner, N. Walker-Crawford, J. L. Wood, and J. C. Yde, “Progress and challenges in glacial lake outburst flood research (2017–2021): a research community perspective,” *Natural Hazards and Earth System Sciences*, vol. 22, no. 9, pp. 3041–3061, 2022.
