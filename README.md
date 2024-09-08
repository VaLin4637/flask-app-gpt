# flask-app-gpt (sentiment) api

## Template openai connect model
```python
import openai

# Set your OpenAI API key
openai.api_key = "sk-QxICix1ZvIs0MGaue0vmunGsnzI3_vuWtt11V7ALAjT3BlbkFJBZZI-TU9B6mk9FXXLFBmBc9G1jd4siBdNu0mU8eK0A"

# Define the text you want to analyze or interact with
text = "เรียน CS ยากมั้ย"

# Make a request to the OpenAI GPT-3.5 API
response = openai.ChatCompletion.create(
    model="gpt-3.5-turbo-0125",
    messages=[
        # prompt
        {"role": "system", "content": "คุณต้องรวบรวมข้อคิดเห็นที่เกี่ยวกับ Computer Science ทั้งในเชิงลบเเละบวก:"},
        {"role": "user", "content": text}
    ]
)

# Extract the response text
response_text = response['choices'][0]['message']['content'].strip()

print("Response from GPT-3.5:", response_text)

# Extract the response text
response_text = response['choices'][0]['message']['content'].strip()

print("Response from GPT-3.5:", response_text)
```
