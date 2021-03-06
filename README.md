# TINDER BOT 

### About Tinder_bot

Tinder_bot is kind of project that aims to automate of the Tinder activities like login, swiping and messaging

Tinder_bot use Selenium to automate process communicating with Tinder web UI. 
It then use Seq2Seq LSTMs for messaging (chatbot) with the matches. 

The chatbot LSTM used is inspired by:  [seq2seq-chatbot](https://github.com/tensorlayer/seq2seq-chatbot) 

It contain two process:
1. Login(): authentication for login with SMS provided.
2. Swipe(): Swipe right (max 5 at time ).
3. ChatBot(interface()): It uses the LSTM mentioned above to chat with matched users.

 
### SETUP
Download [chromedriver](http://chromedriver.chromium.org/downloads) and extract for selenium into the current directory.

```shell
#enviornment setup
python -m venv tinder_bot
#for mac and linux 
  source ./env/bin/activate 
#for window
  env\Scripts\activate.bat

python -m pip upgrade
python -m pip install -r requirements.txt

```

### TO RUN
```shell
python pytinder.py
```

### IMPORTANT 
If Model are Already trained skip this part

You have to train model before running the [pytinder.py](https://github.com/y-agg/TINDER_BOT/blob/master/pytinder.py) 
for that 
1. Select twitter or cornell_corpus dataset in [tinder_bot.py](https://github.com/y-agg/TINDER_BOT/blob/master/tinder_bot.py) between line 30 to 35
2. Train the model by uncommenting line 100 to 145 . this may take few hours 
3. After that run 
```shell
python tinder_bot.py
#For training 
```
