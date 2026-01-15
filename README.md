# Online-Quiz-platform-Using-Python
print("Welcome to the Online Quiz Platform")
name = input("Enter your name: ")

questions = [
    {
        "question": "1. What is the capital of India?",
        "options": ["A. Mumbai", "B. Delhi", "C. Pune", "D. Chennai"],
        "answer": "B"
    },
    {
        "question": "2. Which language is used for web development?",
        "options": ["A. Python", "B. Java", "C. HTML", "D. C++"],
        "answer": "C"
    },
    {
        "question": "3. What does CPU stand for?",
        "options": ["A. Central Processing Unit", "B. Control Processing Unit", 
                    "C. Central Program Unit", "D. Core Processing Unit"],
        "answer": "A"
    },
    {
        "question": "4. Which keyword is used to define a function in Python?",
        "options": ["A. function", "B. define", "C. def", "D. fun"],
        "answer": "C"
    },
    {
        "question": "5. Which data type is immutable?",
        "options": ["A. List", "B. Set", "C. Dictionary", "D. Tuple"],
        "answer": "D"
    }
]

score = 0

for q in questions:
    print("\n" + q["question"])
    for option in q["options"]:
        print(option)
    user_answer = input("Enter your answer (A/B/C/D): ").upper()
    
    if user_answer == q["answer"]:
        print("Correct!")
        score += 1
    else:
        print("Wrong! Correct answer is:", q["answer"])

print("\nQuiz Completed!")
print(f"Name: {name}")
print(f"Your Score: {score}/{len(questions)}")
