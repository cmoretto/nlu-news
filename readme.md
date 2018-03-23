pip install rasa_nlu
pip install rasa_nlu[spacy]
python -m spacy download it
python -m spacy download it_core_news_sm

per fare training:
python -m rasa_nlu.train -c config_spacy.json

runserver: 
python -m rasa_nlu.server -c config_spacy.json

per le chiamate:
WINDOWS = curl "http://localhost:5000/parse?q=I%20am%20looking%20for%20chinese%20food" | python -m json.tool
LINUX = curl -X POST localhost:5000/parse -d '{"q":"I am looking for Mexican food"}' | python -m json.tool


google news api key:
e4728a6712bc4e0397c62325aa1d069a
