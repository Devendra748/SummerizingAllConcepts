# SummerizingAllConcepts

#  Installation
Install the OpenAI Python library by running the following command:
```
pip install openai
```

#  Usage
Import the openai module in your Python script:

```
import openai
```
Set your OpenAI API key using the following code:

```
openai.api_key = 'YOUR_API_KEY'
```
Replace 'YOUR_API_KEY' with your actual OpenAI API key.

Define the get_completion function in your script:

```
def get_completion(prompt, model="gpt-3.5-turbo"):
    messages = [{"role": "user", "content": prompt}]
    response = openai.ChatCompletion.create(
        model=model,
        messages=messages,
        temperature=0,
    )
    return response.choices[0].message["content"]
  ```
Use the get_completion function to generate a summary. Here's an example:

```
prompt = """
Your task is to generate a short summary of a product review from an ecommerce site. 

Summarize the review below, delimited by triple backticks, in at most 30 words. 

Review: ```Got this panda plush toy for my daughter's birthday, who loves it and takes it everywhere. It's soft and super cute, and its face has a friendly look. It's a bit small for what I paid though. I think there might be other options that are bigger for the same price. It arrived a day earlier than expected, so I got to play with it myself before I gave it to her.```
"""

response = get_completion(prompt)
print(response)
```
Run your script to generate the summary.

Note: Replace 'YOUR_API_KEY' in step 2 with your actual OpenAI API key, which you can obtain from the OpenAI platform.

Important: Be aware of your API usage limits and rate limits. If you encounter a rate limit error, you may need to wait for some time or adjust your usage accordingly.

#  Additional Notes
The code uses the OpenAI GPT-3.5 Turbo model by default. We can change the model parameter in the get_completion function to use a different model if desired.
The code includes several examples demonstrating how to generate summaries for different product reviews. You can modify the examples or add your own reviews to generate summaries.
Please refer to the OpenAI API documentation for more information on working with the OpenAI models and API.
