# AmazonFashionDiscoveryEngine

Online shopping is all over the internet. All our needs are just a click away. The biggest online shopping website is Amazon. Amazon is known not only for its variety of products but also for its strong recommendation system.

In our project we are taking into consideration the amazon review dataset for Clothes, shoes and jewelleries and Beauty products. We are considering the reviews and ratings given by the user to different products as well as his/her reviews about his/her experience with the product(s).

Based on these input factors, sentiment analysis is performed on predicting the helpfulness of the reviews. Moreover, we also designed item-based collaborative filtering model based on k-Nearest Neighbors to find the 2 most similar items.

# loading the data using pandas' read_json file
	data = pd.read_json('tops_fashion.json')
	
# Data Pre-processing 
	 What is a dataset? 
	 Rows and columns ,  Data-point ,   Feature/variable 
# Text Pre-processing
	NLTK download stop words. [RUN ONLY ONCE]
	goto Terminal (Linux/Mac) or Command-Prompt (Window) 
	In the temrinal, type these commands
	$python3 , $import nltk ,	$nltk.download()	
# Text based product similarity
	1.Bag of Words (BoW) on product titles.
	2.TF-IDF based product similarity
	3.IDF based product similarity
	4.Average Word2Vec product similarity
	5.Weighted similarity using brand and color

# Using Keras and Tensorflow to extract features
	## https://gist.github.com/fchollet/f35fbc80e066a49d65f1688a7e99f069
	## Code reference: https://blog.keras.io/building-powerful-image-classification-models-using-very-little-data.html
# Visual features based product similarity
	#load the features and corresponding ASINS info.
		bottleneck_features_train = np.load('16k_data_cnn_features.npy')
		asins = np.load('16k_data_cnn_feature_asins.npy')
		asins = list(asins)

	# load the original 16K dataset
		data = pd.read_pickle('pickels/16k_apperal_data_preprocessed')
		df_asins = list(data['asin'])
