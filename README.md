# What is counterfactual?

Counterfactual is a feature explainability method that consists in explaining the importance of a feature in the prediction of an output, 
by displaying a similar prediction but with a variation in the feature that explains itself the difference in the prediction.

# Method:
I used the MNIST dataset to apply the following method:
1. Clustering samples in the Latent Layer with an autoencoder --> Take a random element from class J and encode it in the latent layer
2. Generating samples from a specific class in the Latent Layer with multivariate_normal --> in the latent layer, generate samples from class K
3. Choosing in the latent layer the closest neighbor from a class K to a sample of class J 
4. Decoding the closest neighbor in the output space with the decoder --> Decode sample from class K in the latent layer and see the decoded result in the output layer 
