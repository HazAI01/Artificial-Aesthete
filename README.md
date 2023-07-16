# Artificial Aesthete
<br/>
In this project I implement the ResNet-50 CNN on a dataset for <a href="https://www.kaggle.com/datasets/ikarus777/best-artworks-of-all-time"> Best Artworks of All Time </a> which is a collection of paintings of the 50 most influential artists of all time, in the goal of creating a model that is able to identify the artist just by looking at the painting.
<br/>
I was heavily guided by one of the published Kaggle notebooks (<a href="https://www.kaggle.com/code/supratimhaldar/deepartist-identify-artist-from-art/notebook">link here</a>) that worked on the same dataset for the same objective, however I’ve made some modifications by introducing a Max Pooling layer in the ResNet model and then freezing the first 25 layers for the second training, it was also observed that in my version the Early Stopping callback wasn’t triggered in the second training so the model trained for 50 full epochs while the original notebook stopped early by the 31st epoch.
<br/>
This produced better results compared to the original notebook. The prediction accuracy slightly improved by 3%, the confusion matrix results showed a clearer distinction between different artists and better recognition of the same artist through Actual vs Predicted comparison. However, the major difference was in the actual prediction testing, where mine were much higher while the original notebook had a lot of low prediction probabilities even reaching 27.65%.
<br/><br/>
<b>Results:</b>
<br/>
<img width="685" alt="Screenshot 2023-07-16 at 11 23 17 PM" src="https://github.com/HazAI01/Artificial-Aesthete/assets/120788731/616cbef2-24d0-4657-b238-92d4fe15e1db">
