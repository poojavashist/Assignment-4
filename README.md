# Assignment-4
1.1 Write a Python Program(with class concepts) to find the area of the triangle using the below #formula. #area = (s*(s-a)*(s-b)*(s-c)) ** 0.5 #Function to take the length of the sides of triangle from user should be defined in the parent# #class and function to calculate the area should be defined in subclass.

#Parent class
class tri:
    def __init__(self, a, b, c):
        ''' This method has been used as an 
            self constructor for Traingle class'''
        self.a = float(a)
        self.b = float(b)
        self.c = float(c)
        self.area = 0
        def insert_sides(self):
            self.a = int(input)

            
#Sub class
class triangle(tri):
    def __init__(self, a, b, c):
        tri.__init__(self, a, b, c)

    def calculate_area(self):
        s = (self.a + self.b + self.c) / 2
        self.area = float((s * (s - self.a) * (s - self.b) * (s - self.c))) ** 0.5

    def get_area(self):
        return self.area     

a, b, c = input("insert side a value = "), input("insert side b value = "), input("insert side c value = ")

t = triangle(a, b, c)
t.calculate_area()
print("area : {}".format(t.get_area()))

output
insert side a value = 8
insert side b value = 6
insert side c value = 9
area : 23.525252389719434

#Problem 2: Write a function filter_long_words() that takes a list of words and an integer n and returns 
#the list of words that are longer than n. 


def filter_long_words(l,a):
    words=[]
    for j in l:
        if(len(j)>=a):
            words.append(j)
    return words

n=input("Enter words:")
nt=n.split(",")
na=input("Enter Min Length:")
print("\n Output:")
long=filter_long_words(nt,int(na))

print(" The List of longest words ""\n or" "longer than given number are" ,long)

output
Enter words:shreeyan,boy
Enter Min Length:5
 The List of longest words 
 orlonger than given number are ['shreeyan']
 
 #Problem_2.1 Write a Python program using function concept that maps list of words into a list of integers representing the lengths of the corresponding words . 
#Hint: If a list [ ab,cde,erty] is passed on to the python function output should come as [2,3,4] 
#Here 2,3 and 4 are the lengths of the words in the list.



#Function to map length of words with words 
def map_Words_to_Length(List):
    ''' This function Map's the words with their corresponding length'''
    return list(map(len, List))

word_List=list(input("Input : Please enter Words : ").split(","))
#List Comprehension has been done to remove white trailing white spaces
List=[x.strip() for x in word_List]
#function Execution
Words_lengths=map_Words_to_Length(List)

print("Output: Length of Words are :",Words_lengths )

output
Input : Please enter Words : ac,cde,erty
Output: Length of Words are : [2, 3, 4]

#Problem_2.2 Write a Python function which takes a character (i.e. a string of length 1) and returns True
#True if it is a vowel, False otherwise.

def vowel_checker(inputChar):
    #docstring
    '''This function will return True/False based upon input character provided by user'''
    return_value=''
    if(len(inputChar)==1):
        vowel_list=['a','e','i','o','u']
        if (inputChar.lower() in vowel_list):
            return_value= True
        else:
            return_value= False
    else:
        return_value="Please enter single character only!"        
    return return_value
print("Enter character to check that it is Vowel or not")
input_value = input("Input Value: ")
output_value=vowel_checker(input_value) 
print("Output Value:",output_value)

output
Enter character to check that it is Vowel or not
Input Value: a
Output Value: True
