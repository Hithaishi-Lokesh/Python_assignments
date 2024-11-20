# Python_assignments

#write programe to print - 
# pyton is fun
#"quotes" and 'single quotes'can be tricky

print('''pyton is fun.\n"quotes" and 'single quotes' can be tricky ''')
#or
print ('pyton is fun.\n "quotes" and \'single quotes\' can be tricky')
print('"hello"')
print('''you'r a 'good' man''')

#   create 3 variable  and store name, age , cty , then print in a sentence useing those variables.
name = input('provide a name: ')
city = input('provide city name: ')
age = input('provide a age: ')

print(f'the name is {name}, the age is {age}, the city is {city}')

# write a python program to input students name and marks of 3 subject. print name and percentage in output

Student_name = input('provide students name:  ')
math_mark = float(input('provide math_mark  name:  '))
eng_mark = float(input('provide eng_mark  name:  '))
science_mark = float(input('provide science_mark  name:  '))

total_marks = math_mark + eng_mark + science_mark

percentage = (total_marks / 300) * 100

print(f'the student name is {Student_name}', f'the student percentage is {percentage}%')

#programe to collect multiple types of data ( name, age, height, status)for user input, stores them in dictionary, and then print out the collected data

#first give empty dictionary
user_data = {}

#give values and Key

user_data['name'] = input("provide your name:  ")
user_data['age']  =int(input("provide your age:  "))
user_data['height'] = int(input("provide your height:  "))
user_data['status'] = input("your status:  ")

print(user_data)

# for key,value in user_data.items():
#     print(F"{key}:{value}")

# programe to determine leap year- 
# leap year occurs once a 4 years
# a year is leap year if divisible by 4 , but not divisible by 100 unless also divisible by 400

# year = int(input('enter a year'))

# def leap_year(year):
#     if (year % 4 == 0 ) and (year % 400 ==0 or  year % 100 != 0 ):
#         print('a leap year')
#     else:
#         print("not a leap year")
    
# leap_year(year)

#using conditional statement , assume username and password are predefined
#program that prompts  the user  to enter a username  and password  and checks whether they match, provded 
#both usernname and password  are correct
#username is correct  but  password is incorrect 
#user name is incorrect

predef_username = "hithaishi"
predef_password = 'hitha123#'

username = input('please enter username:  ')
password = input('please enter password:  ')

if username == predef_username:
    if password ==predef_password:
        print("both usernname and password  are correct")
    else:
        print("username is correct  but  password is incorrect")
else:
    print("user name is incorrect")

a university has following eligiblity criteriafor admission 
marks is maths >=65
marsk in physics >=55
marks in chemistry >=50
total marks in all 3 sub  >180 or total  marks  matha and physics>=140
#program that takes marks in 3 sub  and prints whether  the student is eligible  for admission 


student_name = input('please enter students name: ')
student_math_marks =int(input('please enter math_marks: '))
student_physics_marks=int(input('please enter physics_marks: '))
student_chemistry_marks =int(input('please enter chemistry_marks: '))
total_marks = student_math_marks + student_physics_marks + student_chemistry_marks 
total_maths_physics_marks = student_math_marks + student_physics_marks 
print(f'the total mark = ',total_marks)
print(f'the total of math and physics',total_maths_physics_marks)

if student_math_marks >=65 and student_physics_marks >= 55 and student_chemistry_marks >=50:
    if total_marks >180 and total_maths_physics_marks >140:
        print('eligible')
else:
    print('not eligible')


#limit the decimal places  to 2 digit using .format method and print result, for variable pi

pi = 3.14145890
print(round(pi,2))
print("the value of pi : {}".format(pi,2)) #
print("the value of pi : {:.2f}".format(pi,2)) #.format
print(f"the value of pi : {pi:.2f}") # fstring 

#extract  characters from  2 to 8 with  a step of 2 : 
#given my_string = python course, slice characters from index 2 to 8 , skipping every other charcter 

my_string = "python course"
print(my_string[2:8:2])


#slice  to get only the middle character   for my_string = python course

my_string_odd = "hithaishi"
my_string_even = "hithaishil"

def mid_string(word):
    middle = int(len(word)/2)
    if len(word) % 2== 0:
        return word[middle-1 : middle +1 ]
    else:
        return word[middle]
    

print(mid_string(my_string_odd))
print(mid_string(my_string_even))

#remove the first and last 3 character , string  = regression analysis 

my_string = 'regression analysis'

print(my_string[3:-3])

# # get the  substring that start 4 characters from the end  to the last character for my_string = "classification", slice the string starting from the 4th char  from the end to the last charc

# my_string = "classification"
# print(my_string[-4:])

# how to reverse a string

my_string = 'hithu'
# print(my_string[::-1])

def reverse_string(string):
    return(string[::-1])

print(reverse_string(my_string))



#program   to check if the string is a palindrom using string method

my_string1 = "tatat"
my_string2 = "tata"

def check_palindrom(word):
    task = (word[::-1])

    if task == word:
        return('palindrom')
    else:
        return('not a palindrom')

print(check_palindrom(my_string1))
print(check_palindrom(my_string2))




diff  between find() and index()

#### find() it returns the first occurence index  of the string  in the original string otherwise return -1 
 #syntax  : 
string = "running"
search = "un"
search1 = "gi"
result1 = string.find(search)
result2 = string.find(search1)
print(result1)
print(result2)
#### index() it returns the frist occurance index of the string in the orriginal string otherwise will generate error as exceptional value error and stops execution
#syntax:
string = "running"
search = "u"
#search1 = "gi"
result1 = string.index(search)
#result2 = string.index(search1)
print(result1)
#print(result2)




# efficeint  string concatenate, Why is using join() often more efficient than using + for string concatenation in a loop?
 
### The simplest method for concatenating strings in Python uses the + operator: While this method is straightforward, it does not add any spaces between the concatenated strings, which leads us to the next topic.
SYNTAX :
String_1 = "hello"
string_2 = "world"
result = String_1 + ' ' + string_2
print(result)
### Alternatively, you can use formatted strings (f-strings), which are available in Python 3.6 and later:
String_1 = "hello"
string_2 = "world"
result = f"{String_1} {string_2}"
print(result)

###Concatenating Strings in a List

string = ['hello' , 'world' , 'hello' , 'you']
new_string = ' '.join(string)
print(new_string)

If you have a list of strings that you want to concatenate, Python provides the join() method, which is both efficient and elegant. Here's how you can do it:

The join() method is particularly useful when you need to concatenate a large number of strings since it is more efficient than repeatedly using the + operator.
