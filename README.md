# 1.Overview
As one of the most popular online travel platforms (OTPs) in China, Fliggy from Alibaba group delivers travel experiences to tens of millions of online users by providing million-scale travel-related products (e.g., flight tickets, hotels, and package tours, etc). With the large-scale product portfolio available on the platform, the platform accumulates users' behavior data，algorithms can find products that users are interested in based on long-term behavioral data of users. However, data sparseness caused by the low frequency characteristics of travel bring a huge challenge for algorithms to model user interests.

To push the state of the art in recommender system forward, we release User Behaviour data from Fliggy platform (UBF), which is the largest recommender system dataset from real industrial scenes, this data set is user desensitization behavior data, which includes the basic attributes of users and the desensitization information of the basic attributes of commodities. The goal is to model and learn the interest representation of current users from the behavior data of users and user groups, and provide users with Personalized, high-quality and professional product recommendation program.

2.Data Description
The data consists of three parts: user historical behavior desensitization data, user basic attribute desensitization data, and commodity basic attribute desensitization data.

file name	introduction	include features
user_item_behavior_history.csv	Contains all user behavior data	User ID, product ID, behavior type, timestamp
user_profile.csv	Contains all user basic attribute portraits	User ID, age, gender, occupation, habitual city, crowd tag
item_profile.csv	Contains all the basic attributes of the product	Product ID, product category ID, product city, product tag
2.1. Download
The Fliggy dataset is provided by Fliggy Trip Platform. Click "apply" button and fill in necessary information. After confirming "Terms of Use", your application will be reviewed automatically within 7 days. If agreed, you can download data directly. If rejected, you can apply again according to feedback information.

# 2.2. Data Format
user_item_behavior_history.csv

The data set covers all behaviors (including clicks, favorites, adding, and purchases) of approximately 2 million random users from June 3, 2019 to June 3, 2021. The organization of the data set is similar to MovieLens-20M, namely Each row of the collection represents a user data behavior, which is composed of user ID, product ID, behavior type, and log. Each column summarizes the detailed information of the product under investigation.

Field	Explanation
User ID	An integer, the serialized ID that represents a user
Item ID	An integer, the serialized ID that represents an item
Behavior type	A string, enum-type from ('clk', 'fav', 'cart','pay')
Timestamp	An integer, the timestamp of the behavior
user_profile.csv

This data set mainly contains the basic attributes of about five million random users, such as age, gender, occupation, resident city ID, crowd tag, etc. Each row of the data set represents a piece of user information, separated by commas. The detailed description of each column in the data set is as follows:

Field	Explanation
User ID	An integer, the serialized ID that represents a user
Age	An integer, the serialized ID that represents an user age
Gender	An integer, the serialized ID that represents the user gender
Occupation	An integer, the serialized ID that represents the user occupation
Habitual City	An integer, the serialized ID that represents the user habitual city，single value
User Tag List	A String, the ID of each tag is separated by English semicolon after serialization
item_profile.csv

This data file mainly contains the basic attribute characteristics of about 270,000 products, such as product category ID, product city, product label, etc. Each row of the data set represents the information of a product, separated by commas. The detailed description of each column in the data set is as follows:

列名称	说明
Item ID	An integer, the serialized ID that represents an item
Category ID	An integer, the serialized ID that represents an item category
Item City	An integer, the serialized ID that represents an item City
Item Tag List	A String, the ID of each tag is separated by English semicolon after serialization
Dimensions of the dataset are as follows:

Dimension	Number
# of users	5744057
# of items	267326
# of categories	115
# of ctiys	341
# of user tags	12
# of item tags	208
# of interactions	22516238
# 2.3 Data Usage
To use the UBF dataset, please refer to XXXXXX(该开源项目地址). This repo contains the processing code and a complete example.

3. Citations

}

# 4. License
This data set follows the CC BY-NC 4.0 protocol.
