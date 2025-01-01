# the-ai-detector
Please see `cs4765-project.ipynb`, in the notebook, there contains training code as well as code for testing our fine tuned model. There also contains code on some data exploration we did before fine tuning our model. Every cell contains comments explaining what its purpose is. Please be sure to adjust the dataset file paths as needed. The dataset and zipped DistilBert model were submitted through D2L.

If you would like to use this model yourself, it can be downloaded from the Hugging Face Hub from [this repository](https://huggingface.co/EwicGoat/ai-gen-1/tree/main)

# Setup
- Install dependencies specified in requirements.txt by running `pip install -r requirements.txt`. There is also a cell that can be copied that contains all the necessary pip installs. Please see cell 2. `pip install datasets transformers torch matplotlib seaborn`
- Run the project as usual! I usually run `jupyter notebook --NotebookApp.iopub_data_rate_limit=1.0e10` in the root directory to open jupyter notebook on the browser.
- The datasets required are found in shared Google Drive (I was not able to upload it to Github due to the large file sizes). Please make sure to download the datasets as well as the zip file of the fine tuned model. Dr. Cook, I sent an invite to the google drive folder which can be accessed [here](https://drive.google.com/drive/folders/1DgatdyEcVV8CqqulSdvbG4hQkT75YaFC?usp=drive_link), please contact eric.cuenat@unb.ca if any issues arise.  Thank you!

# Important Rules for devs
- Every time you pip install a new library, you ned to run `pip freeze > requirements.txt` or `pip3 freeze > requirements.txt` (depending on your pythong version). This will make sure to keep the requirements.txt updated and will make sure that our code runs on any machine withou hiccups!

# Important Notes On Performance
<img width="713" alt="image" src="https://github.com/user-attachments/assets/cc4e003c-e399-480b-ae3f-4573656ad577" />

- The table above are the results of the DistilBert model, it performed better than the most frequent class baseline and also outperformed logistic regression which was great to see.
- For the future, I would like to retrain the model to address the overfitting observed in the table. The training data was composed of 50% AI generated text and 50% non AI generated, although this was a good start, we can see that the model is having a hard time recalling non AI generated text with a poor score of 0.64. Retraining the model to incliude more non AI generated text as well as adjusting the model thresholding to remove the AI detection bias.
