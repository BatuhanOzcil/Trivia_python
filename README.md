You can see the code below:

    class Question:
        def __init__(self, question, answer1,answer2,answer3,answer4,correct_answer):
            self.question = question
            self.answer1= answer1
            self.answer2= answer2
            self.answer3= answer3
            self.answer4= answer4
            self.correct_answer = correct_answer
    
        def get_question(self):
            return self.question
    
        def get_answer1(self):
            return self.answer1
    
        def get_answer2(self):
           return self.answer2
    
        def get_answer3(self):
            return self.answer3
    
        def get_answer4(self):
            return self.answer4
    
        def get_correct_answer(self):
            return self.correct_answer
    
    questions = [
        Question("What is the capital of Turkiye ?","Istanbul","Izmir","Gaziantep",
                 "Ankara",4),
        Question("What is the chemical symbol for Iron ?","Fe","Au","Na","Cu",
                 1),
        Question("Who is the strongest one in the Skywalker family ?","Anakin","Luke",
                 "Leia","Padme",2),
        Question("What is the most consumed manufactured drink in the world ?","Coffe","Coke",
                 "Tea","Milk",3),
        Question("Which is the only edible food that never goes bad ?","Butter","Honey",
                 "Potato","Egg",2),
        Question("What country has the most natural lakes?","Canada","Russia","Germany",
                 "Turkey",1),
        Question("How many hearts does an octopus have ?","One","Two","Three",
                 "Four",3),
        Question("What is the hottest planet in the solar system?","Earth","Venus",
                 "Mercury","Jupiter",2),
                 Question("Who is the founder of the Modern Turkiye ?","Mustafa Kemal Ataturk","Osman Bey",
                 "Ismet Inonu","Timur",1),
        Question("Which team has the most championships in Formula 1 ?","Red Bull","Mercedes",
                 "Williams","Ferrari",4),
    ]
    
    player1_score = 0
    player2_score = 0
    
    for i, question in enumerate(questions,1):
        print("Question",i)
        print(question.get_question())
        print("1. ", question.get_answer1())
        print("2. ", question.get_answer2())
        print("3. ", question.get_answer3())
        print("4. ", question.get_answer4())
    
        player1_answer = int(input("Player 1, please enter your answer (1-4): "))
        player2_answer = int(input("Player 2, please enter your answer (1-4): "))
    
        if player1_answer == question.get_correct_answer():
            print("Player 1 answered correctly !")
            player1_score += 1
        else:
            print("Player 1 answered incorrectly.")
    
        if player2_answer == question.get_correct_answer():
            print("Player 2 answered correctly !")
            player2_score += 1
        else:
           print("Player 2 answered incorrectly.")
    
    print("Player 1 score:",player1_score)
    print("Player 2 score:",player2_score)
    
    if player1_score > player2_score:
      print("Player 1 wins !")
        elif player2_score > player1_score:
      print("Player 2 wins !")
    else:
        print("It's a tie !")
