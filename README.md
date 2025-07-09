# Hospital Voicemail Prioritization and Department Routing System  
This project is an AI-powered system designed to handle hospital voicemails. It prioritizes voicemails based on urgency (High/Medium/Low) and routes them to the correct department such as Emergency, Doctors, Pharmacy, or Accounts. It uses audio feature extraction (via OpenSMILE), transcription with PII redaction, and machine learning models to automate and streamline voicemail management.  
## 📁 Project Structure  
```  
├── app/                          # Main application logic  
├── templates/                   # HTML templates for the web interface  
├── static/                      # Static files (CSS, JS, audio, etc.)  
├── Sample Voicemails/           # Contains sample voicemail audio files  
├── OpenSmile Output/            # OpenSMILE-generated CSV feature files  
├── Hospital_Voicemail_Transcription.xlsx     # Transcription dataset  
├── OpenSmile_Output.xlsx                     # Combined OpenSMILE output  
├── OpenSmile_Features_Dataset.xlsx           # Cleaned dataset for model training  
├── voicemails.xlsx                           # Voicemail metadata  
├── transcription_model.py       # Voice-to-text transcription logic  
├── pii_redation.py              # Redacts personally identifiable information  
├── combined_urgency.py          # Merges audio and text urgency scores  
├── random_forest_classifier.py  # Model training logic for urgency detection  
├── random_forest_model.pkl      # Trained urgency detection model  
├── dept_model_test.py           # Department classification model testing  
├── Department_model.py          # Final department routing model  
├── Model_Test_Final.py          # Final script for integrated model testing  
├── Voicemail_Handling.py        # Handles voicemail download, processing, and routing  
├── PRESENTATION_PPT.pdf         # Project presentation slides  
├── MAIN_PROJECT_REPORT.pdf      # Final project report  
```  
## 🛠️ Setup Instructions  
### 1. Clone the Repository  
```bash  
git clone https://github.com/yourusername/hospital-voicemail-system.git  
cd hospital-voicemail-system  
```  
### 2. Install Required Libraries  
```bash  
pip install -r requirements.txt  
```  
### 3. Prepare Data  
- Put sample audio files in the `Sample Voicemails/` folder.  
- Ensure OpenSMILE is installed and the configuration file is set up for feature extraction.  
- Update any paths in your code to reflect your local structure.  
### 4. Run Preprocessing Scripts  
```bash  
python transcription_model.py       # Converts voicemails to text  
python pii_redation.py              # Redacts sensitive text from transcripts  
python combined_urgency.py          # Combines urgency from audio & text  
```  
### 5. Train and Evaluate Models  
```bash  
python random_forest_classifier.py  # Train urgency classification model  
python dept_model_test.py           # Test department classification model  
```  
### 6. Run Final Model Pipeline  
```bash  
python Model_Test_Final.py  
```  
### 7. (Optional) Launch Flask App  
```bash  
python app/main.py  
```  
## 🧠 Features  
- ✅ Audio feature extraction using OpenSMILE  
- ✅ Transcription using speech recognition  
- ✅ Urgency detection using Random Forest  
- ✅ Department classification  
- ✅ Personally identifiable information (PII) redaction  
- ✅ Web-based interface (optional)  
- ✅ Automation of voicemail analysis  
## 🎓 Skills You Can Add to Your Resume  
- Audio Analysis using OpenSMILE  
- Natural Language Processing (NLP)  
- Urgency and Intent Detection  
- Machine Learning (scikit-learn, Random Forest)  
- Data Preprocessing & Feature Engineering  
- Flask Web Application Development  
- Privacy-Preserving PII Redaction  
- End-to-End AI Pipeline Implementation  
## 🧰 Tools & Technologies  
- Python  
- OpenSMILE Toolkit  
- scikit-learn  
- Flask  
- Pandas, NumPy  
- Google Speech Recognition  
- Excel/CSV processing  
- Automation & Data Engineering  
## 📄 References  
- https://audeering.github.io/opensmile/  
- https://scikit-learn.org/stable/documentation.html  
- https://flask.palletsprojects.com/  
- https://pypi.org/project/SpeechRecognition/  
## 🏥 Use Case  
Ideal for hospitals and clinics to automate and improve the triaging and routing of voicemails. High-priority cases can be attended to faster, and voicemails can be routed correctly without manual filtering.  
## 📌 License  
This project is for academic and research use. Contact the author if you wish to use it commercially.  
