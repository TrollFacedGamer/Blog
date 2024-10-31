# Daring Debugging
## Intoduction
Introduction
On October 1st, 2024 me and my class at STEAM were given an assignment where we were given bugged code and made to identify and propose a solution to the problem causing the bug. There were 5 sets of code presented, with one already having its problem and solution given to us as an example. The code and answer was written in a google doc while the debugging primarily occurred in visual code studio.

## Code Set 1
```
text = "Hello, world, my name is"
count = 0

for char in text:
    if char == "":
       count += 1

print(count)
```

The above is the first set of the code we were given to solve. The purpose of this code was to “Count how many spaces are in a given string”. However, it didn’t work as intended, because the code can not recognize spaces to count them because its conditional statement was comparing char with blanks and counting them instead of spaces. To debug the code I had to add a space between the quotation marks on line 5, this will allow the code to recognize spaces when they come up as char as what it is counting instead of blanks.

## Code Set 2
```
print("give me a number")
n = input()

for num in range(1, n):
    if num % 2 < 0:
        print(num, "is even.")
    else:
        print(num, "is odd.")
```

The above is the second set of code we was given to solve. The purpose of this code was to “Determine if numbers 1 to n are even or odd ”. The code didn’t work as intended for two reasons. Firstly, the code was processing the input as a string and can’t use it for math because a string is just symbols and not numbers. Secondly, the code was unable to tell if the numbers it is processing is even because it believes that an even number has a negative remainder when divided by 2 because it is comparing the reminder of num and 2 to 0 with a less than sign. To fix the errors i put the input() on line 2 in an int() function to convert the input into an integer allowing the input to be used for math and change the < on line 5 to a == so the code can recognize when a number is divisible by 2 or even.

## Code Set 3
```
num = int(input("Enter an integer: "))

if num < -1:
  print("No negative numbers.")
else:
  result = 1
  for i in range(1, num):
    result *= i   

  print("Factorial of " + num + "is" + result)
```

The above is the third set of code I was given to solve. The purpose of this code was to “calculate the factorial of a given number”. The code did not work as intended for two reasons. Firstly, the code isn’t properly multiplying all the numbers from 1 to the variable num, because the range function on line 7 will not include the second number(num) given to it in the set of numbers it generates. Secondly, the print function on line 10 will return an error, because you can’t add strings with integers to create a sentence as the integer makes the code believe that you are trying to do math with a string. To fix the error I did 2 things. Firstly I added a +1 behind num in line 7 so the code registers the value of num as one of the numbers to multiply with by making it return 1 to num -1 +1. Secondly I surround the num and result variable in line 14 with a str() each, this will allow the code to add the values of the variables as strings; add a space behind and infront of is in line 14 for a better print.

## Code Set 4
```
attempts = 0
correct_password = "secret"

while True:
    password = input("Enter your password: ")
    attempts += 1

    if password == "incorrect_password":
        print("Correct password!")
    else:
        print("Incorrect password")

    if attempts > 3:
        print("Too many attempts")
        break
```

The above is the fourth set of code I was made to solve. The code was originally made to “ask user to enter the correct password but only give them 3 attempts”. However the  code does not work properly for 2 reasons. Firstly, The code isn’t registering correct_password as the correct password because the code is comparing the input to something else on line 4. Secondly the code is giving 4 attempts instead of 3 because it isn’t comparing the number of attempts with allowed attempts correctly on line 9. To fix the issue I changed “incorrect_password” string on line 8 to correct_password variable so that the code compares the input with the value in the variable correct_password and added a = sign behind the > sign on line 13 to allow the code to register 3 attempts as reaching the attempt limit.
