# Text to SQL Application

This repository contains a powerful Text to SQL application that efficiently converts natural language text input about a marketing database into the correct SQL query. With this application, you can easily interact with your database using simple and intuitive language.

## Table of Contents

- [Introduction](#introduction)
- [Database Structure](#database-structure)
- [Models and Libraries](#models-and-libraries)
- [Application Interface](#application-interface)
- [Getting Started](#getting-started)
- [Contributing](#contributing)
- [License](#license)

## Introduction

Have you ever found yourself struggling to write complex SQL queries for your marketing database? Look no further! This Text to SQL application simplifies the process by allowing you to express your queries in plain English. It leverages the power of OpenAI's gpt-3.5-turbo model, with a window size of 4,096 tokens, and LangChain.ai to accurately interpret your natural language queries.

## Database Structure

The underlying database for this application is built in ClickHouse and comprises the following tables:

1. **Agency Customers**: This table stores information about customers associated with the marketing agency. It includes the following columns:
   - CustomerId (Primary Key)
   - Name
   - Email
   - Status
   - CreatedAt

2. **Users**: The Users table contains details about the users of the marketing platform. It has the following columns:
   - UserId (Primary Key)
   - RegDate
   - Status

3. **UserActivity**: This table tracks the activity of users on the marketing platform. It includes the following columns:
   - VisitId (Primary Key)
   - UserId
   - VisitDate
   - ThroughClick
   - CampaignId

4. **CampaignActivity**: The CampaignActivity table stores information related to marketing campaigns. It has the following columns:
   - CampaignId (Primary Key)
   - Platform
   - AdStartDate
   - AdEndDate
   - TotalCost

## Models and Libraries

The Text to SQL application is built upon the following models and libraries:

- **OpenAI's gpt-3.5-turbo**: This powerful language model provides the core natural language processing capabilities of the application. It allows the system to understand and interpret your queries effectively.

- **LangChain.ai**: LangChain.ai is a library that enhances the understanding of natural language by providing additional context and processing capabilities. It works seamlessly with the gpt-3.5-turbo model, making the application more accurate and reliable.

## Application Interface

To make the Text to SQL application user-friendly and easily accessible, it is wrapped using Streamlit. Streamlit provides an interactive web interface for running the application, allowing you to input your queries in natural language and receive the corresponding SQL output in real-time.

## Getting Started

To run the Text to SQL application locally, follow these steps:

1. Clone this repository: `git clone https://github.com/your-username/your-repo.git`
2. Install the required dependencies: `pip install -r requirements.txt`
3. Start the application: `streamlit run app.py`
4. Access the application in your browser at `http://localhost:8501`

## Contributing

Contributions are welcome! If you have any ideas, suggestions, or bug reports, please open an issue or submit a pull request. Let's work together to improve this Text to SQL application and make it even more powerful.

## License

This project is licensed under the [MIT License](LICENSE). You are free to use, modify, and distribute this application for both commercial and non-commercial purposes.
