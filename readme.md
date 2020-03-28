# Create a virtual env
virtualenv venv
source venv/bin/activate

#Clone 
git clone https://github.com/tyiannak/pyAudioAnalysis.git 

#Install Dependencies
pip3 install -r ./App/requirements.txt
pip3 install -r ./pyAudioAnalysis/requirements.txt

#Install
pip3 install -e pyAudioAnalysis

#Using Test.py
python3 App/app.py

#Training
python3 pyAudioAnalysis/pyAudioAnalysis/audioAnalysis.py trainClassifier -i ../data/cough/not_sick ../data/cough/sick --method randomforest -o model

#Training Dataset
https://osf.io/4pt2s/