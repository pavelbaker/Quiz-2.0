import random

def quiz(questions, difficulty, operation):
    score= 0
    difficulty = difficulty.lower()
    operation = operation.lower()

    if difficulty not in ["easy", "medium", "hard"]:
        print("This is not a recognised difficulty, please choose 'easy', 'medium' or 'hard'")
        return
    
    if operation not in ["addition", "subtraction", "multiplication", "division"]:
        print("This is not a recognised operation, please choose 'addition', 'subtraction', 'multiplication' or 'division'")
        return
    
    ranges = {
        "easy": 10,
        "medium": 100,
        "hard": 1000
        }

    max_val = ranges[difficulty]
    
    for j in range(questions):
        a = random.randint(1, max_val)
        b = random.randint(1, max_val)

        
        if operation == "addition":
            answer = a+b
            operator = "+"
        elif operation == "subtraction":
            answer = a-b
            operator = "-"
        elif operation == "multiplication":
            answer = a*b
            operator = "*"
        elif operation == "division":
            answer = a/b
            operator = "/"
       


        while True:
            try:
                user_answer = input(f"What is {a} {operator} {b}? ")

                if operator == "/":
                    user_answer = float(user_answer)
                    if round(user_answer,2) == round(answer, 2):
                        print("You are correct")
                        score +=1
                    else:
                        print(f"Incorrect, the correct answer was {round(answer, 2)}")
                else:
                    user_answer = int(user_answer)
                    if user_answer == answer:
                        print("You are correct")
                        score+=1
                    else:
                        print(f"Incorrect, the correct answer was {answer}")
                break
            except ValueError:
                print("This is not a number, try again")

    print(f"You got {score} out of {questions}")
    return score
