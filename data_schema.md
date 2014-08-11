# Data schema

## Some notes on DateTime data type in mongodb

According to mongodb doc, creating DateTime objects is extremely slow.
http://api.mongodb.org/perl/current/MongoDB/DataTypes.html#Dates

It's suggested that saving dates as numbers and converting the numbers to DateTime when needed. **A single DateTime** field can make deserialization up to **10 times slower**. 

### SpeakeasyAdmin

* objectId: String
* username: String
* password: String
* email: String
* emailVerified: String
* ACL: acl object
* log: String (SpeakeasyAdminLog::objectId)
* createdAt: Number (convert to DateTime)
* updatedAt: Number (convert to DateTime)

### SpeakeasyAdminLog

* objectId: String
* adminId: String (SpeakeasyAdmin::objectId)
* createdAt: Number (convert to DateTime)
* location: String (login|logout|home|search)
* action: String
* target: String

### SpeakeasyImage

* objectId: String
* userId: String (SpeakeasyUser::objectId)
* content: String (actual content that user writes)
* font: String (name of the font chosen for the content over the image)
* keywords: Array (String)
* replies: Array (SpeakeasyImage::objectId)
* orgImgSrc: String
* rawImage: String (SpeakeasyRawImage::objectId)
* isTweeted: Boolean
* tweetUrl: String
* isFacebooked: Boolean
* facebookUrl: String
* isSpokeneasy: Boolean
* viewCounts: Number
* createdAt: Number (convert to DateTime)
* updatedAt: Number (convert to DateTime)
* trending: Boolean (by author)
* hidden: Boolean

### SpeakeasyRawImage

* objectId: String
* img: (Raw File)
* createdAt: Number (convert to DateTime)
* updatedAt: Number (convert to DateTime)

### SpeakeasyUser

* objectId: String
* userName: String (allow null and for future)
* password: String (allow null and for future)
* email: String (allow null and for future and facebook/twitter)
* IFA: String (Advertising Identifier for identifying device)
* APNSDeviceToken: String (Apple Push Notification Service)
* IPAddress: String
* createdAt: Number (convert to DateTime)
* updatedAt: Number (convert to DateTime)