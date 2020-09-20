
# Recipe Search Engine
Adapted from Lyrics Search Demo Jina example

Dataset: https://www.kaggle.com/shuyangli94/food-com-recipes-and-user-interactions
##Command	Description
pip install -r requirements.txt

python app.py index	-> To index files/data

python app.py search -> To run query on the index

##View in Browser
cd static

python -m http.server

Open http://0.0.0.0:8000/ in your browser.

##Changes Made
ranker.yml - Tried using LevenshteinRanker instead of MinRanker

encode.yml - Tried using UniversalSentenceEncoder,
              used distilbert-base-cased

craft.yml - sentence length changed from 6 to 3

##Errors
While querying on the index:

netstat -ltnp | grep :65481

sudo kill -9 PID

While running server:

netstat -ltnp | grep :8000

sudo kill -9 PID
