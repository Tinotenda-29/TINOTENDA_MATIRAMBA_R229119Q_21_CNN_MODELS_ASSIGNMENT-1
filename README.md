# TINOTENDA_MATIRAMBA_R229119Q_21_CNN_MODELS_ASSIGNMENT-1
R229119Q_TINOTENDA_MATIRAMBA

Combined Hybrid Model PerformanceSummary

This analysis summarizes the performance of 20 Hybrid Dual-Input Regression Models designed for property price prediction. These models utilize a Late Fusion Architecture, combining tabular property features with visual features extracted from property images using various CNN backbones (e.g., AlexNet, VGG, ResNet).

Performance Evaluation

The models were ranked primarily by the Root Mean Squared Error (RMSE).Best Performer: The AlexNet backbone achieved the lowest RMSE of 4,428,327.46.Ranking Consistency: Model performance clustered closely; the difference between the best-performing model (AlexNet) and the worst (InceptionV3, RMSE: 4,528,834.40) was minimal in the context of the overall error magnitude.

Critical Implication:

Negative 
R
2
 ScoreA significant finding is that all 20 models exhibited negative 
R
2
 scores, ranging from 
−
0.0027
 to 
−
0.0488
.A negative 
R
2
 indicates that every trained model performs worse than a simple baseline that predicts the mean property price for all data points.This demonstrates that the complex CNN architectures and the late fusion approach failed to capture the underlying variance in the property prices, suggesting a fundamental lack of predictive power across the entire set of experiments

Conclusion

The project's outcomes, defined by a consistently high RMSE (in the millions) and universally negative 
R
2
 scores, indicate a significant failure in the model's ability to generalize and predict property prices.

1.Primary Reasons for FailureLimited Data Sample: The necessary cleaning steps, including dropping rows with missing prices or images, resulted in a dataset that was too small for effectively training complex, high-capacity hybrid models (like those using deep CNNs).

2.Image Feature Contamination: The models incorrectly extracted features because many property images contained more than one house or had irrelevant background details. This meant the CNNs picked up features from the wrong structure, corrupting the visual signal and making the late fusion process unreliable.
