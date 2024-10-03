# Local Explanations of Inception V3 pretrained model with Lime
The aim of this repo is to demonstrate the application of LIME to a pretrained InceptionV3 image classification model. The purpose of using LIME is to obtain local explanations for the classification decisions made by black box models for specific classifications/predictions.

## Example of a local explanation using LIME

> Original image & Groom classification from the Iception V3 model.

![image](https://github.com/user-attachments/assets/9c83ddc9-7fba-499c-a29f-69590db0c171)

> parts of the image was responsible for the Groom prediction according to LIME.

![image](https://github.com/user-attachments/assets/338e1d4e-c37a-4f92-8674-de2a9e486ce2)

> parts of the image that positively contributed to the groom prediction (highlighted in green), and also the parts of the image that negatively contributed to the groom prediction (highligted in red).

![image](https://github.com/user-attachments/assets/b925ed12-94ac-40d1-8730-976a91fefba5)

> Oveall explanation weights assigne by LIME

![image](https://github.com/user-attachments/assets/5e86927e-99c8-4bde-b4dc-ffe944954d3f)

## Discussion

> Why LIME?

LIME is a popular explanation technique that provides local interpretability for machine learning models. It works by approximating the model locally with an interpretable model, such as a linear model, to explain individual predictions. 

> I chose LIME for the following reasons:

**Model-Agnostic**: LIME can be applied to any machine learning model, including complex models like InceptionV3, without requiring access to the model’s internal structure.

**Local Explanations**: LIME focuses on explaining individual predictions, which is useful for understanding specific instances and identifying potential biases or errors in the model.

**Human-Interpretable**: The explanations provided by LIME are easy to understand for humans, making it suitable for communicating model behavior to non-experts.

>Strengths

**Versatility**: LIME can be used with any machine learning model, making it a versatile tool for interpretability.

**Simplicity**: The technique is relatively simple to implement and understand, providing clear and concise explanations.

**Flexibility**: LIME allows for the use of different interpretable models (e.g., linear models, decision trees) to approximate the local behavior of the complex model.

>Limitations

**Approximation Quality**: The quality of the explanations depends on how well the interpretable model approximates the complex model locally. In some cases, the approximation may not be accurate.

**Computational Cost**: Generating explanations with LIME can be computationally expensive, especially for large datasets or complex models like InceptionV3.

**Stability**: The explanations provided by LIME can be sensitive to the choice of parameters and the sampling process, leading to variability in the results.

> Potential Improvements

**Enhanced Sampling**: Improving the sampling process to better capture the local behavior of the model can lead to more accurate explanations.

**Hybrid Approaches**: Combining LIME with other interpretability techniques, such as SHAP (SHapley Additive exPlanations), can provide more robust and comprehensive explanations.

**Parameter Tuning**: Fine-tuning the parameters of LIME, such as the number of samples and the type of interpretable model, can improve the stability and quality of the explanations.

In summary, LIME is a powerful and flexible technique for explaining individual predictions of complex models like InceptionV3. While it has some limitations, potential improvements can enhance its effectiveness and reliability.

### References

https://github.com/marcotcr/lime/blob/master/doc/notebooks/Tutorial%20-%20Image%20Classification%20Keras.ipynb

https://colab.research.google.com/github/AIPI-590-XAI/Duke-AI-XAI/blob/dev/explainable-ml-example-notebooks/local_explanations.ipynb#scrollTo=TBoIW4G-gpC9

Microsoft co-pilot was used to help with the discussion.
