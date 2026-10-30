# Food Image Classifier 
CNN vs Fine-tuned VGG16

**Tools**: Python, Keras, VGG16

## Data 
10 classes from Food-101 Kaggle dataset: apple_pie, baby_back_ribs, breakfast_burrito, chocolate_cake, cup_cakes, eggs_benedict, escargots, falafel, risotto, sushi
750 / 200 / 50 per class, giving 7,500 train / 2,000 validation / 500 held-out test images, resized to 100x100 due to computing power required to process a larger size. 

## Approach
1. **Baseline CNN trained from scratch**
2. **Transfer learning with VGG16**

## Results (500 image test set, chance = 10%)
| Model | Test accuracy |
| --- | --- |
| CNN from scratch | 47.0% |
| Fine-tuned VGG16 | **70.8%** |

Regularisation cut the train-validation accuracy gap from about 16 points to 1-2 points. An early VGG16 variant scored higher on test accuracy but over fit more, so I chose the more stable final model. 
