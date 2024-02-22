# User Detection

For user detection, the first approach is to determine if user's identity is guaranteed on a given platform, as this is one of the key things to note when trying to create a digitally respected identity.

So we analyse the user social footprint to generate a constructive proof, which can then be verifiable without the user having to give out access to their data again.

In mathematics, a constructive proof is a method of proof that demonstrates the existence of a mathematical object by creating or providing a method for creating the object but in our case we'll be providing a method to verify that the said generated proof is valid.

Hence the need for AI (ML) to train the model to be able to take in user data ("all data is hashed after being consumed by the model") and determine which accounts show good levels of activity to pass after which we use the Mina zk library to generate a verifiable proof for the user.

The project will implement a novel method to detect bots (bot management).

Another challenge for us would be in creating a base implementation for this user detector, after it has been been exposed to the social media section seeing each social media incorporate different design methos as weell as exposed api for consumption.

The first social media we'd work with is X.com (formally known as twitter) as currently there's a lot of reference material (albeit deprecated or old) we can start development using these materials.

- Botometer by Indiana University
- twitonomy
- botsentinel

None of these cited examples are running ever since twitter deactivated the free V1.1 endpoints.

## Twitter Analysis

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

3. Text Mining: Text mining also gives insight on whether an account is bot
controlled. Bot accounts may post the same, or very similar, messages repeatedly to evade Twitter’s spam filters, which identify repeated messages. [String similarity algorithms](https://yassineelkhal.medium.com/the-complete-guide-to-string-similarity-algorithms-1290ad07c6b7) will be used here to analyse a section of user tweets as the api limits allow.
