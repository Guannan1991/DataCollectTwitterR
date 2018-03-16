# DataCollectTwitterR
install.packages("twitteR") #installs TwitteR library (twitteR) #loads TwitteR
library(twitteR)

api_key <- "CBxyH6y5C1*******S81hyNJp" #in the quotes, put your API key 
api_secret <- "LhpgpQCvPEohILSQ4n**********CbHKYvve6368jzsMY4Yx" #in the quotes, put your API secret token
token <- "929816555646603268-V30pExK********0JcmQE0olxloU" #in the quotes, put your token 
token_secret <- "aM5iQwxN7Cx*********ko9qxQSpKLjBHtttK3qPVQ" #in the quotes, put your token secret

setup_twitter_oauth(api_key, api_secret, token, token_secret)
tweets <- searchTwitter(" AND #MWC OR Mobile World Congress OR Huawei OR Samsung OR LG", n = 200, lang = "en")

tweets.df <-twListToDF(tweets)
write.csv(tweets.df, "C:/Users/gli/Desktop/Guannan/tweets.csv")# DataCollectTwitterR

## Methods to get Twitter API
https://www.slickremix.com/docs/how-to-get-api-keys-and-tokens-for-twitter/
https://opensource.com/article/17/6/collecting-and-mapping-twitter-data-using-r
