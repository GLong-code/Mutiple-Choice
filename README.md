# Mutiple-Choice
from Useful_tool import Test


Test_prompt = [
    "What is even number? \n(a).1  (b).2  (c).3   (d).5 \n",
    "5 = x + 3, x = ? \n(a).2   (b).1   (c).3   (d).4 \n ",
    "Square of 3 is ? \n(a).7  (b).8   (c).9  (d).10 \n ",
]

Testes = [
    Test(Test_prompt[0],"b"),
    Test(Test_prompt[1],"a"),
    Test(Test_prompt[2],"c"),
]

def run_test(Testes):
    score = 0
    for test in Testes:
        answer = input(test.question)
        if answer == test.answer:
            score = score + 1
            print("You have 1 point")
        else:
            print("Wrong answer")

    print("You have " + str(score) + " correctly")

run_test(Testes)

###
class Test:
    def __init__(self,question,answer):
        self.question = question
        self.answer = answer
###
