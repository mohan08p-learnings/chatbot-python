# chatbot-python

## Training your house AI

#### Problem
You just bought Jordan, the smartest AI in the world, for your house. Now you have to set it up for use.

Your task is to train Jordan with all of the world’s information and then to train it with your personal information for restricted access.

To prevent unauthenticated access to your house, only two people are allowed to access Jordan: you and another trustworthy person in your life, which can be anyone from your friends and family.

To protect your personal information, only you will have access to your personal information.

#### Task 1: security check
Your first task is to enter the identity of a person and respond accordingly based on the permissions you give Jordan. We will be using the name of one person, Mark, and a trustworthy friend, Jane.

Here are the two scenarios that need to be checked:

If it is Mark, you have to respond with the following and continue with the program:

```
Welcome, Mark. Happy to have you at home.
```

If it is Jane, you have to respond with the following and continue with the program:

```
Mark is out right now, but you are welcome to the house.
```

If it is none of the above, you have to respond with the following and exit the program:

```
Your access is denied here.
```

You can exit the program using the exit() command. To get you started with the activity, here is a hint.

#### Task 2: training custom data
Once the bot has identified you, you will train the bot with the following personal information about you. The blanks contain your personal information.

**Where was I born?**
You were born in ___________.

**What is my favorite book?**
That is easy. Your favourite book is __________.

**What is my favorite movie?**
You have watched ___________ more times than I can count.

**What is my favorite sport?**
You have always loved ___________.

#### Code
Let’s start coding now. You are provided with the skeleton of the code, and you have to fill in the missing pieces. Instructions have been given as highlighted code comments for you to structure your solution accordingly.

A sample custom data for the house owner’s information is trained for your guidance:

```
house_owner = [
    "Who is the owner of this house?",
    "Mark Nicholas is the owner of this house."
]
```

Follow the pattern to get started. Good luck!

```
To quit talking to Jordan, say any of these: bye, bye jordan or good bye.
```

#### Explanation

After checking for the identity of the user in line 10, we have written rules and facts for responding to the different identities.

If the identity is Mark, we skip all the cases below and go straight to line 23. Otherwise, we check if the identity is Jane.

If the identity is unknown, we respond accordingly and exit the program using the exit() command.

Once the identity is confirmed as Mark or Jane, the program skips to line 24, and the code below is executed.

In line 32, we check whether the identity is Mark before we train the bot with Mark’s personal information. Otherwise, code jumps to line 51 and starts the bot.

If the identity is Mark, we add our custom data in the form of lists from lines 33-51. The first object of the list is the question, and the second object of the list is the answer.

Once we have added all of our new data, we train the bot with the custom data using the custom_train() function from lines 53-56. The bot will not learn the answers to the questions by simply adding the custom data in the code. We will need to explicitly train the bot with all the custom data.

After training the bot with our custom data, we start the bot using the start_chatbot() function.