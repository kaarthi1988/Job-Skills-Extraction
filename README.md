# Industry Skill Demand in Data Analytics Through Job Postings

This project analyzes job postings from various job boards, including LinkedIn, Indeed, and ZipRecruiter, to identify key trends in the fields of Data Analytics, Machine Learning, Big Data, and IT. The goal is to provide insights into the most sought-after skills, technologies, and programming languages across different job roles, such as Analysts, Data Scientists, Machine Learning Engineers, and Engineers. 

## Project Overview

The project consists of the following stages:
1. **Data Scraping**: Collect job postings from job boards using a Python web scraper. Please use this [Job Scraper Tool](https://github.com/kaarthi1988/Job_Scrapper_Python_Package) to scrape more data.
2. **Data Annotation**: Manually annotate job descriptions using open-source tools like Doccano and NER Annotators.
3. **Model Development**: Train a Named Entity Recognition (NER) model using SpaCy to extract key entities like skills, technologies, and salary from job descriptions.
4. **Analysis**: Analyze the extracted data to identify key trends and provide actionable insights for job seekers, recruiters, and educational institutions.

### Key Features
- **Data Collection**: Scraped over 4,000 job postings using Python's BeautifulSoup and Hrequests libraries.
- **Manual Annotation**: Annotated job descriptions with 53,000 entities using Doccano and NER annotators.
- **Entity Extraction**: Extracted key information such as Data Skills, Technology Skills, Soft Skills, and Salary using SpaCy's pre-trained NER model.
- **Analysis and Insights**: Analyzed trends in key job roles: **Analyst**, **Scientist**, **Machine Learning**, and **Engineer**.

### Identified Entities from Job Descriptions
- **DATA TOOLS**
- **EDUCATION**
- **EXPERIENCE**
- **SKILLS**
- **SOFT-SKILLS**
- **DOMAIN**
- **RESPONSIBILITY**
- **CERTIFICATE**
- **SALARY**

The extracted data is analyzed for each job role to understand the demand for skills, technology, soft skills, and salary for the required roles.

## Technologies Used

- **Data Scraping**: Python, BeautifulSoup, Hrequests
- **Text Annotation**: Doccano, NER Annotator
- **NLP & Model Training**: SpaCy, Fuzzy Matching (`thefuzz`), Train/Test Split
- **Data Analysis**: Pandas, Numpy
- **Data Visualization**: Seaborn, Matplotlib
- **Entity Types Identified**: 
  - DATA TOOLS
  - EDUCATION
  - EXPERIENCE
  - SKILLS
  - SOFT-SKILLS
  - DOMAIN
  - RESPONSIBILITY
  - CERTIFICATE
  - SALARY

## Data Scraping Details

The data scraping part of the project is done using Python libraries such as **BeautifulSoup** and **Hrequests**. The scraping process collects job posting details such as job titles, company names, locations, salary, and job descriptions from job boards like Indeed, LinkedIn, and ZipRecruiter.

- **Job Titles**: The job title for each posting (e.g., Data Scientist, Machine Learning Engineer).
- **Company**: The company offering the position.
- **Location**: The location of the job.
- **Salary**: The salary or compensation offered (if available).
- **Job Description**: A detailed description of the job requirements, responsibilities, and qualifications.

The scraper extracts over **4,000 job postings** from Indeed. Each job posting is retrieved by navigating through multiple pages of the website, ensuring a wide variety of postings are captured.

The code includes:
- **Requests** to fetch web pages.
- **BeautifulSoup** to parse and extract job posting information.
- Randomized **sleep intervals** between requests to avoid overloading the server and reduce the risk of getting blocked.
- A mechanism to handle possible scraping failures and retries.

**Example of scraped data**:
- **Job Title**: Data Analyst
- **Company**: ABC Tech Solutions
- **Location**: New York, NY
- **Salary**: $80,000 - $90,000
- **Job Description**: Seeking an experienced Data Analyst to work with large datasets, develop models, and produce business insights.

## Data Annotation

The job descriptions were manually annotated with key entities using open-source tools such as **Doccano** and **NER Annotator**. A total of **53,000 entities** were extracted from these job descriptions, including:
- **Data Skills**
- **Technology Skills**
- **Soft Skills**
- **Salary**

These annotations were then converted into JSON format and subsequently into SpaCy's `DocBin` format for model training. This labeled data serves as the foundation for training the NER model to automatically extract similar entities from new job descriptions.

## Model Development

A **Named Entity Recognition (NER)** model was developed using **SpaCy** to extract relevant entities from the job descriptions. The model was trained on the annotated data and achieved an **F1 score of 80%**. The model was used to extract the following entities:
- **DATA TOOLS**
- **EDUCATION**
- **EXPERIENCE**
- **SKILLS**
- **SOFT-SKILLS**
- **DOMAIN**
- **RESPONSIBILITY**
- **CERTIFICATE**
- **SALARY**
  ![image](https://github.com/user-attachments/assets/ee7413d0-ca0c-4a6b-8bbf-88ef485747a9)


### Future Improvements:
- **Annotation of More Data**: The current model can be further improved by annotating more job descriptions. As more annotated data is added, the model’s accuracy can be enhanced, leading to more reliable entity extraction.
- **Scraping More Data**: The current scraping tool can be used to scrape additional job postings from multiple job boards. With more data, the analysis can be expanded and the results will become more accurate, providing deeper insights into the job market trends.

## Analysis

The project performs analysis to identify the most in-demand skills, technologies, and salary ranges for the following job roles:
1. **Analyst**
2. **Scientist**
3. **Machine Learning Engineer**
4. **Engineer**

The analysis examines data such as:
- **Skills**
- **Technologies**
- **Soft Skills**
- **Salary**
  ![image](https://github.com/user-attachments/assets/69f689d0-4922-452d-9368-63e863329ecc)
  ![image](https://github.com/user-attachments/assets/b60de9a1-c000-4d30-ab2f-e7d2c47357c7)



By analyzing job postings, the project identifies the most common skills and technologies required by employers. It helps understand the skills gap in the job market, making it easier for job seekers to upskill and for educational institutions to adjust their curricula to meet industry needs.

## Expected Outcomes

The expected outcomes of this project include:
- **Insights on Job Roles**: Understand the skills and technologies required for roles such as Analyst, Scientist, Machine Learning Engineer, and Engineer.
- **Entity Extraction**: Extract and categorize key entities such as Data Skills, Technology Skills, Soft Skills, Salary, and more.
- **Actionable Insights**: Provide guidance for educational institutions to update curricula and for professionals looking to upskill.
- **Improved Model**: Enhance the model’s accuracy by annotating more data and scraping more job postings, resulting in a more robust entity extraction process.

## Contributions

Contributions to this project are welcome! If you would like to contribute, please fork the repository and create a pull request with your changes. Ensure to follow best practices for code quality and documentation.

## License

This project is intended for personal use and educational purposes. It is not intended for commercial use, and the author is not liable for any consequences arising from its use.

## Contact

For any questions, suggestions, or collaborations, please feel free to open an issue or contact me directly at pradeepakaarthi@gmail.com.
