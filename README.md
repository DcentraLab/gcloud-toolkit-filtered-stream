[Developer Guide: Twitter API Toolkit for Google Cloud - Filtered Stream](https://developer.twitter.com/en/docs/tutorials/developer-guide--twitter-api-toolkit-for-google-cloud1)


# https://developer.twitter.com/en/docs/tutorials/developer-guide--twitter-api-toolkit-for-google-cloud1

gcloud config set project twitter_quorums

gcloud services enable bigquery.googleapis.com

git clone https://github.com/DcentraLab/gcloud-toolkit-filtered-stream.git

cd gcloud-toolkit-filtered-stream

vi config.js

# Edit line #5 in config.js by inserting the Twitter API bearer token (ensure the word ‘Bearer’ must be prepended before the token with a space

# Edit line#19 in config.js by inserting the Google Cloud project id

gcloud app deploy

gcloud app browse -s default
# https://twitter-quorums.ue.r.appspot.com

#to activate the stream
curl https://twitter-quorums.ue.r.appspot.com/stream
curl https://twitter-quorums.ue.r.appspot.com/stream/connect

# Deployed service [default] to [https://twitter-quorums.ue.r.appspot.com]

# You can stream logs from the command line by running:
$ gcloud app logs tail -s default

# To view your application in the web browser run:
$ gcloud app browse

# to clean resources:
https://twitter-quorums.ue.r.appspot.com/stream/clean

