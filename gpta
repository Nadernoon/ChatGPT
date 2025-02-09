import openai

def chat_with_ai(prompt, model="gpt-3.5-turbo"):
    openai.api_key = "your-api-key-here"  # Replace with your actual API key
    
    response = openai.ChatCompletion.create(
        model=model,
        messages=[{"role": "system", "content": "You are a helpful AI assistant."},
                  {"role": "user", "content": prompt}]
    )
    
    return response["choices"][0]["message"]["content"]

if __name__ == "__main__":
    while True:
        user_input = input("You: ")
        if user_input.lower() in ["exit", "quit", "bye"]:
            print("AI: Goodbye!")
            break
        ai_response = chat_with_ai(user_input)
        print("AI:", ai_response)
