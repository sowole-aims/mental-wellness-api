# Mental Health API

This README provides an overview of the files and functionality of the chatbot implemented using LangChain, OpenAI and FastApi. The chatbot is designed to provide answers related to mental health queries using conversational AI. 
## Files
The codebase consists of the following files:

- [app.py](): This file contains the main code for the FastAPI application. It sets up the server, and communicates with the Langchain library to generate responses for the chatbot.
- [Mental_Health_FAQ.csv](): This file is a CSV (Comma-Separated Values) file that contains a dataset of frequently asked questions (FAQs) related to mental health. The chatbot utilizes this dataset to provide answers and information on mental health topics.

## Setup
-   Download and extract the codebase into your local machine:
```
git clone https://github.com/sowole-aims/mental-wellness-api.git
```

``` 
cd mental-wellness-api
```

- Install the required Python packages by running the following command in the project directory:
```
pip install -r requirements.txt
```
- Set up the OpenAI API key by creating a `.env` file in the project directory. Add the following line to the .env file, replacing <your_api_key> with your actual OpenAI API key:
~~~
OPENAI_API_KEY=<your_api_key>
~~~

## Usage
### Run the application:
- Run the application by executing the following command in the project directory:
```
uvicorn app:app --reload
```
- Open your browser and visit `http://localhost:8000` to access the chatbot.
- Enter your queries or statements related to mental health in the input field.
- The chatbot will provide responses to queries based on the pre-trained models and the `Mental Health FAQ` dataset.
- If you encounter any errors or issues, please try again or seek assistance from a mental health professional.


### Build the Docker image
```
docker build -t mental-wellness-api .
```
### Run the Docker container
```
docker run -p 8000:8000 mental-wellness-api
```
6. Access the API:

Open your web browser and navigate to `http://localhost:8000` to access the API.

### API Usage

Add `/docs` to the URL to get the Swagger UI Docs or `/redoc`.

The API provides a single endpoint:

- `POST /process_prompt` - Accepts a user question as input and returns the AI-generated response.

## License
This project is licensed under the [MIT License](LICENSE).

## Acknowledgments
This project utilizes the Langchain library, OpenAI's GPT-3 language model and FastApi Web Framework.

## Important Note
Please ensure that you have a valid OpenAI API key to use the chatbot. If you don't have one, sign up for an API key at the OpenAI website before running the chatbot.

### Medium Blog
- [Medium Blog](https://medium.com/@oladimejisamuel/building-a-mental-health-chatbot-using-fastapi-langchain-and-openai-1e22d9c6edc1).