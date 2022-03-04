# Library Installation :

### Create New Environment Variable :
check no of env : conda env list or conda info --envs

create : conda create -n RasaEnv python=3.7 anaconda

conda activate RasaEnv

conda deactivate

conda env remove --name ENVIRONMENT

### Required Libraries :
pip install rasa 

pip install rasa[spacy]

pip install pandas

pip install flask_mail

python -m spacy download en_core_web_md
##### OR
python -m spacy link en_core_web_md en

### NLU : 

##### Rasa NLU Run :
rasa train nlu # train nlu model

rasa shell nlu # test nlu model

rasa test nlu # Evaluate nlu model

rasa run actions # expose the nlu model 

##### Rasa Core Run :



##### OR
rasa train -vv -dump-stories --force 

rasa run actions # expose the core model

rasa shell  # test core model

rasa test core # Evaluate core model

##### Note : actions server run in terminal 1 and test model in terminal 2



# Run Chatbot :
### Terminal 1 :
rasa init --no-prompt #note : do not run this command

### Start directly from here :
rasa run -m models --enable-api --cors "*" --debug

### Terminal 2 :
./ngrok http 5005 #linux

ngrok http 5005 #windows
 
##### Expose URL : http://a1becb115fae.ngrok.io  # check url in googel browser(copy and paste in  google chrome) : Hello from Rasa: 1.10.3
 

