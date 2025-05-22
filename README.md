
# ShapEV | Paper : [JMI 2022](https://www.oaepublish.com/articles/jmi.2022.04) & [Aggregate 2025](https://onlinelibrary.wiley.com/doi/epdf/10.1002/agt2.70060)

A package for identifying **Equivalent Value** based on joint SHAP values.

ShapEV is an python package that identifies **Equivalent Value** among features based on cooperative game theory. By leveraging SHAP values, ShapEV decomposes feature contributions and their interactions, defining joint SHAP values to capture combined feature effects. 

An **Equivalent Value** is proposed based on the joint SHAP value, reflecting each feature's overall contribution to the regression target. ShapEV applies this equivalent value to represent the collective behavior of interacting features, allowing users to substitute original individual features with a unified **Equivalent Value**.

On the modified dataset, ShapEV calculates the contribution of the proposed **Equivalent Value** by comparing it to SHAP contributions. This validation confirms that, within the SHAP framework, the equivalent value linearly correlates with the target when showing high correlation.

## Installation

Install ShapEV using pip:

```bash
pip install ShapEV
```

## Usage Example

```python
from ShapEV import EVsearch

# Instantiate the ShapEV model
model = EVsearch.EVkit('T91-LBE-Train.csv')

# Train the model and calculate joint SHAP values
model_type = 'XGBoost'  # Options: 'GradientBoosting', 'RandomForest', 'LightGBM', 'XGBoost'
model.fit(model_type)


model.shap(SPACE=7) # SPACE (int): Maximum number of combinations to return.
```



The ShapEV package simplifies the process of identifying and validating equivalent values, allowing for a more efficient representation of feature contributions in regression models.

## About 
Maintained by Bin Cao. Please feel free to open issues in the Github or contact Bin Cao
(bcao686@connect.hkust-gz.edu.cn) in case of any problems/comments/suggestions in using the code. 

## License and Usage
© All rights reserved.

This software is provided for academic and research purposes only. Commercial use is strictly prohibited. Any violation of these terms will be subject to appropriate actions.
