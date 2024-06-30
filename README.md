# Desafio Dio - Consumindo a API do Twitter com Python



Neste projeto, criaremos um aplicativo Python que consome a API do Twitter para buscar e analisar tweets. O aplicativo usará a biblioteca Tweepy para se autenticar com a API do Twitter e buscar tweets.



## Consumindo a API do Twitter com Python



Criar um projeto prático com o objetivo de consumir a API REST do Twitter seguindo uma série de boas práticas e dicas foram apresentadas pelo expert. Entre elas o Tweepy, para reduzir a complexidade no consumo da API do Twitter.

### Tecnoligias Utilizadas:



- Python 3.10

- MongoDB

- Docker

- FastAPI

  

### **Pré-requisitos**

- Conta do Twitter
- Conhecimento básico de Python



### **Passos**



### **1. Criar um Aplicativo do Twitter**

- Acesse o Portal de Desenvolvedores do Twitter e crie um aplicativo.
- Você precisará fornecer informações como o nome do aplicativo, descrição e URL do site.



### **2. Obter Chaves de API**



- Depois de criar um aplicativo, você obterá chaves de API. Essas chaves são usadas para autenticar seu aplicativo com a API do Twitter.



### **3. Instalar a Biblioteca Tweepy**



- Instale a biblioteca Tweepy, que facilita o uso da API do Twitter em Python:

plaintext



```plaintext
pip install tweepy
```



### **4. Autenticar com a API do Twitter**



- Use as chaves de API para autenticar seu aplicativo com a API do Twitter:

python



```python
import tweepy

consumer_key = 'SUA_CONSUMER_KEY'
consumer_secret = 'SEU_CONSUMER_SECRET'
access_token = 'SEU_ACCESS_TOKEN'
access_token_secret = 'SEU_ACCESS_TOKEN_SECRET'

auth = tweepy.OAuthHandler(consumer_key, consumer_secret)
auth.set_access_token(access_token, access_token_secret)

api = tweepy.API(auth)
```



### **5. Buscar Tweets**



- Use o método `search()` para buscar tweets:

python



```python
tweets = api.search(q='palavra-chave', count=100)

for tweet in tweets:
    print(tweet.text)
```



### **6. Analisar Tweets**



- Use a biblioteca TextBlob para analisar o sentimento dos tweets:

python



```python
from textblob import TextBlob

for tweet in tweets:
    sentiment = TextBlob(tweet.text).sentiment.polarity
    print(f"Tweet: {tweet.text}")
    print(f"Sentimento: {sentiment}")
```



### **Conclusão**



Neste projeto, criamos um aplicativo Python que consome a API do Twitter para buscar e analisar tweets. Isso demonstra o poder da API do Twitter e da biblioteca Tweepy para criar aplicativos que podem acessar e analisar dados do Twitter.
