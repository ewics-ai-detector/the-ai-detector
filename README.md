# the-ai-detector

# Setup
- Install dependencies specified in requirements.txt by running `pip install -r requirements.txt`
- Run the project as usual! I usually run `jupyter notebook --NotebookApp.iopub_data_rate_limit=1.0e10` in the root directory to open jupyter notebook on the browser.
- Jupyter notebook will be sufficient to start for now, but we should look into Google Colab for fine tuning our model. Transitioning from notebook to colab seems pretty straight forward

# Important Rules
- Every time you pip install a new library, you ned to run `pip freeze > requirements.txt` or `pip3 freeze > requirements.txt` (depending on your pythong version). This will make sure to keep the requirements.txt updated and will make sure that our code runs on any machine withou hiccups!

