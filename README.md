# CODSOFT_TASKSNO1
CodSoft internship repo..


import re
import random

responses = {
    "greeting": [
        "Hello! How can I assist you with your internship today?",
        "Hi there! Ready to write some code?",
        "Hey! What CodSoft task are we working on?"
    ],
    "how_are_you": [
        "I'm just a script running in Colab, but I'm doing great! How are you?",
        "Operating at 100% efficiency! How can I help?"
    ],
    "thanks": [
        "You're welcome! Keep up the good work.",
        "Happy to help!",
        "Anytime. Let me know if you need anything else."
    ],
    "fallback": [
        "I'm not quite sure I caught that. Could you rephrase?",
        "I don't have a rule for that yet. Ask me about the internship tasks!",
        "Sorry, my logic doesn't cover that input. Try asking about 'submission' or 'Task 2'."
    ]
}

def codsoft_bot(user_input):
    user_input = user_input.lower()

    if re.search(r'\b(hello|hi|hey)\b', user_input):
        return random.choice(responses["greeting"])

    elif re.search(r'\b(how are you|how is it going)\b', user_input):
        return random.choice(responses["how_are_you"])

    elif re.search(r'\b(thank you|thanks)\b', user_input):
        return random.choice(responses["thanks"])

    elif re.search(r'\b(rules|requirements|completion)\b', user_input):
        return "To complete the internship, you must finish at least 3 tasks, maintain a GitHub repo named CODSOFT_TASKSNO, and post a video explanation on LinkedIn."

    elif re.search(r'\b(submit|submission|linkedin|github)\b', user_input):
        return "Share your GitHub repo link in the submission form (emailed later). Also, post your demo video on LinkedIn, tag @CODSOFT, and use #codsoft."

    elif re.search(r'\b(task 2|tic tac toe)\b', user_input):
        return "Task 2 is Tic-Tac-Toe AI. Implement an unbeatable agent using algorithms like Minimax, optionally with Alpha-Beta Pruning."

    elif re.search(r'\b(task 3|image captioning)\b', user_input):
        return "Task 3 is Image Captioning. Use models like VGG/ResNet for feature extraction and an RNN/transformer to generate captions."

    elif re.search(r'\b(task 4|recommendation)\b', user_input):
        return "Task 4 is a Recommendation System. Suggest items using collaborative filtering or content-based filtering techniques."

    elif re.search(r'\b(task 5|face detection)\b', user_input):
        return "Task 5 is Face Detection and Recognition. Use Haar cascades or deep learning detectors, and optionally Siamese networks for recognition."

    else:
        return random.choice(responses["fallback"])

print("🤖 CodSoft Assistant is live! Ask me about your tasks or type 'quit' to exit.")

while True:
    text = input("You: ")

    if re.search(r'\b(bye|goodbye|quit|exit)\b', text.lower()):
        print("Bot: Good luck with your CodSoft internship tasks! Goodbye.")
        break

    print("Bot:", codsoft_bot(text))
     
🤖 CodSoft Assistant is live! Ask me about your tasks or type 'quit' to exit.
You: hi
Bot: Hi there! Ready to write some code?
You: how are you?
Bot: I'm just a script running in Colab, but I'm doing great! How are you?
You: thanks
Bot: Happy to help!
You: fallback'
Bot: Sorry, my logic doesn't cover that input. Try asking about 'submission' or 'Task 2'.
You: you
Bot: Sorry, my logic doesn't cover that input. Try asking about 'submission' or 'Task 2'.
