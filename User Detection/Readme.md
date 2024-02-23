# User Detection

For user detection, the first approach is to determine if user's identity is guaranteed on a given platform, as this is one of the key things to note when trying to create a digitally respected identity.

So we analyse the user social footprint to generate a constructive proof, which can then be verifiable without the user having to give out access to their data again.

In mathematics, a constructive proof is a method of proof that demonstrates the existence of a mathematical object by creating or providing a method for creating the object but in our case we'll be providing a method to verify that the said generated proof is valid.

The approach taken by this project is to use AI (ML) to create and train a model able to take in user data ("all data is hashed after being consumed by the model") in order to determine which accounts show good levels of activity to pass after which we use the Mina zk library to generate a verifiable proof for the user.

## Machine Learning approach

This is an main analytical approach used in Bot detection field, where the tasks of classification, clustering, and anomaly detection are highlighted.

These tasks are performed by means of the following algorithms:

- Supervised
- Unsupervised
- Reinforcement
- Deep Learning

### Supervised learning

Characterized by a simplicity of implementation, supervised learning algorithms are usually the initial choices in classification problems. The good performance of these algorithms is always the result of good data preparation, since the training process is supervised. Despite their advantages mentioned above, they are not immune to the evil of dimensionality. There are several types of supervised learning algorithms applied in the state of the art of bot detection, which are selected according to several criteria based for example on the type and size of data, robustness to noise and computational complexity.

The most frequent supervised algorithms are the:

1. Random Forests (RF)
2. Decision Trees (DT)
3. K-Nearest Neighbor (K-NN)
4. Vector Support Machine (SVM)
5. Naı̈ve Bayes (NB)

### Unsupervised learning

Clustering and anomaly detection are the highlight unsupervised leaning activities used for bot detection, without eliminating their importance in data preprocessing stage. As well as the supervised learning approach, both are limited to the accuracy of data training. Although the mining process is indirect, there are bot detection solutions based on clustering. The use of unsupervised learning
approach is motivated by the fact that in real life several bots are camouflaged and when we have a historical user session data set, some bot sessions may be improperly labelled as human-generated.

With a lower frequency than the previous approach, in the state of the art clustering approaches are applied,
such as:

1. BotGrab
2. SMART based on Markov Clustering (MCL)
3. Agglomerative Information Bottleneck (AIB)
4. K-Means and Graded Possibilistic C-Means (GPCM)

We also have the anomaly detection approach such as:

1. Correlation analysis
2. Botmark

### Reinforcement learning

The reinforcement learning methods are a bit different from conventional supervised or unsupervised methods. In this context, an agent is trained over a period of time, to interact with a specific environment and improve its performance over a period of time, with regard to the type of actions it performs on the environment

### Deep Learning

Although they are not a solution for all variants of the bot detection problem, it is important to reference the use
of Artificial Neural Networks (ANN)-based models in several studies of the state of the art. Multiple purposes,
scalability, robustness to incomplete and noisy data, can be the reasons for the choice, conversely, they are
very detrimental at saving computing resources. Some ANNs approaches are as follows:

1. Convolutional Neural Networkss (CNNs)
2. Long Short-Term Memory (LSTM)
3. Deep Neural Networks and Active Learning Bot detection (DABot) based on RGA, a deep ANN that comprises a Resisual Networks (ResNet).
4. Bidirectional Gated Recurrent Unit (BiGRU)

## Social Networks

The first social media we'd work with is X.com (formally known as twitter) as currently there's a lot of reference material (albeit deprecated or old) we can start development using these materials.

- Botometer by Indiana University
- twitonomy
- botsentinel

None of these cited examples are running ever since twitter deactivated the free V1.1 endpoints.

### Twitter Analysis

On Twitter, information can be gained about a user from their personal account information, tweets, likes, retweets, and direct messages. Users’ direct messages are not accessible for privacy reasons. To identify bots, we set up three basic areas for analysis: profile, account activity, and text mining.

1. Profile: On social media platforms, most users place some personal information about themselves or details to express their individuality. An example of this is a Twitter user’s profile image. The image can be of the user, a corporation, or other image that expresses a characteristic that the user wants identified with their account. Lack of such imagery and individual information might be a sign that a Twitter account is a bot. Bots can lack these profile details when a botnet system creates many bots at once. However, these are not sure signs that a Twitter account is run by a bot. With the privacy concerns of today, some users on social media accounts may intentionally hold back personal information to prevent their information from being
stolen.

    Possible areas for testing in a user's profile:

    - unique screen name (checking for similarities with other users)
    - profile picture
    - followers (further analyses of ratio of accounts followed against follower accounts)
    - geo location status
    - description

2. Account Activity: Account activity is also an indication if an account is operating by a bot. A bot’s automated activity is identified through abnormal user patterns, such as posting all hours of the day and night and posts occurring at the exact time daily or weekly. With Twitter, users are able to pre-set a written tweet to be sent at a certain time. An account that sends a tweet at the same time daily, maybe advertising a limited time offer, would be an example of activity similar to how a bot would behave.

3. Text Mining: Text mining also gives insight on whether an account is bot controlled. Bot accounts may post the same, or very similar, messages repeatedly to evade Twitter’s spam filters, which identify repeated messages. [String similarity algorithms](https://yassineelkhal.medium.com/the-complete-guide-to-string-similarity-algorithms-1290ad07c6b7) will be used here to analyse a section of user tweets as the api limits allow.

## Updates

After reading
