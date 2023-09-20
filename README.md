# Resume-Matching-with-Job-Descriptions-Using-pdf-resumes

### 1. PDF Data Extraction

* **1.read_resume.ipynb**

    * dowloaded dataset(pdf) from kaggle - [here](https://www.kaggle.com/datasets/snehaanbhawal/resume-dataset)
    * extracted data using PyPDF2
    * created a df (main_df.csv)
    * preprocessed and added to tokens to df (main_df_tokens,csv)


* **2.skills_from_json1.ipynb**

    * took a json file which has skills (jz_skill_patterns.jsonl) added to spacy pipeline
    * generated skills and skill count (skills_with_json1.csv)



* **3.gen_new_skills.ipynb**

    * to generate new skills,we need to train a fasttext model with complete resume text(complete.txt)
    * take all skills from previous csv(skills_with_json1.csv)
    * then generated new skills from model(getting nearest similar words to each skill)
    * then combined the previous json and new json which has new skills
    * ![image](https://github.com/Hemasundher/Resume-Matching-with-Job-Descriptions-Using-pdf-resumes/assets/89529752/3bec7b9b-e5d8-4a8c-b01b-c394d295a8f1)






* **4.skills_from_json2.ipynb**

    * created a spacy pipeline with new json file(total_skills2.jsonl)
    * got skills and skill count using above spacy pipeline and saved it as csv(skills_final.csv)
    * then compared it with previous skills
    * got better skills count


### 2. Job Description Data Understanding
* **5.huggingface-jobdescription.ipynb**

    * from huggingface loaded dataset
    * took 15 job descriptions and saved it a csv(job_df.csv)
    * preprocessed the job description text
    * using same spacy model , got skills for each description.
    * added it to the csv file(job_df.csv)


### 3. Candidate-Job Matching
* **6.resume-skill-match.ipynb**

    * loaded both csv files(job_df.csv and skills_final.csv)
    * did a countplot for skills in skills_final.csv(resume skills)
    * eliminated some resumes with less skills
    * took word vectors using spacy model
    * calculated vectors for each row for two csv files
    * then calculated cosine similarity and took top five(results.csv)





#### Modules used
* PyPDF2
* pandas
* numpy
* spacy
* fasttext
* sklearn
* matplotlib
* seaborn
* re


##### Note:
some files are large in size so uploaded it to drive and added the link

some Challenges : mentiones - [here ](https://github.com/Hemasundher/Resume-Matching-with-Job-Descriptions-Using-pdf-resumes/blob/main/challenges.pdf)


send a mail for any query.[Send Email](mailto:hemasundheraluru@gmail.com)
        
