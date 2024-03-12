# Machine Learning Trading Bot

![Algorithmic Trading](https://www.investopedia.com/thmb/Bo73P8i0avZhM5moZ0cgwPpwt_Y=/2190x1369/filters:fill(auto,1)/GettyImages-1151577420-0a1caa7c85a34411820816f7653c3c58.jpg)

In this challenge, I assumed the role of a financial advisor at one of the top five financial advisory firms in the world. I plan to improve the existing algorithmic trading systems and maintain the firm’s competitive advantage in the market. To do so, I have enhanced the existing trading signals with machine learning algorithms that can adapt to new data.

## Steps:

The steps for this challenge are divided into the following sections:

* Establish a Baseline Performance

* Tune the Baseline Trading Algorithm

* Evaluate a New Machine Learning Classifier

* Create an Evaluation Report

### Performance Report (Baseline Trading Algorithm)

Our baseline trading algorithm:
![Signal DataFrame](./Starter_Code/Resources/signal_df.PNG)
![Baseline Classification Report](./Starter_Code/Resources/baseline_classification_report.PNG)
![Baseline Strategy Plot](./Starter_Code/Resources/baseline_strategy_plot.PNG)

### Tuned Trading Algorithm

I increased the SMA short window to 25 and increased the DateOffset to 6 months in efforts to tune the algorithm.

Here are my results:
![Reevaluated Classification Report](./Starter_Code/Resources/revaluated_classification_report.PNG)
![Reevaluated Strategy Plot](./Starter_Code/Resources/revaluated_strategy_plot.PNG)

#### Impact of changing the training window:

When I increased the training window, there was a drop in precision with both 1 and -1 precisions averaging out at around 50%. There were also changes in recall and F1-score, with an increase for the -1 signal. Decreasing the training window saw a worse performance.

#### Impact of changing the SMA windows:

Decreasing the SMA window resulted in a poor performance of the algorithm, and increasing the window resulted in a better average performance based on precision, recall, and F1-score.

### Performance Report (New Machine Learning Model)

![New Model Classification Report](./Starter_Code/Resources/new_model_classification_report.PNG)
![New Model Strategy Plot](./Starter_Code/Resources/new_model_stategy_plot.PNG)

#### Did this new model perform better or worse than the provided baseline model?

Yes, it performed better than the baseline model.

#### Did this new model perform better or worse than your tuned trading algorithm?

It performed slightly worse than the tuned algorithm.

## Evaluation Report

The choice between which model/algorithm to use depends on the context of what we are trying to achieve. However, I will recommend the new machine learning model as it provided a more equal precision score and higher recall and F1-score. Even though the baseline had a higher accuracy score, we have to also consider the other performance metrics.