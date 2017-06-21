# Python Summary
Just another repository


(1)Numbers and strings:
. Arithmetic
. Integers & Floats
. Errors
. Variables I

# The current volume of a water reservoir (in cubic metres)
reservoir_volume = 4.445e8
# The amount of rainfall from a storm (in cubic metres)
rainfall = 5e6

# decrease the rainfall variable by 10% to account for runoff
rainfall *= .9
# add the rainfall variable to the reservoir_volume variable
reservoir_volume += rainfall
# increase reservoir_volume by 5% to account for stormwater that flows
# into the reservoir in the days following the storm
reservoir_volume *= 1.05
# decrease reservoir_volume by 5% to account for evaporation
reservoir_volume *= 0.95
# subtract 2.5e5 cubic metres from reservoir_volume to account for water
# that's piped to arid regions.
reservoir_volume -= 2.5e5
# print the new value of the reservoir_volume variable
print(reservoir_volume)

. Variables II
. Comparison Operators

sf_population, sf_area = 864816, 231.89
rio_population, rio_area = 6453682, 486.5

san_francisco_pop_density = sf_population/sf_area
rio_de_janeiro_pop_density = rio_population/rio_area

# Write code that prints True if San Francisco is denser than Rio, and False otherwise
san_francisco_pop_density < rio_de_janeiro_pop_density
False
san_francisco_pop_density > rio_de_janeiro_pop_density
True
print(san_francisco_pop_density > rio_de_janeiro_pop_density)

. Strings I

# TODO: Fix this string!
messiah = 'He\'s not the Messiah, he\'s a very naughty boy!'
print(messiah)

. Built-In Functions

given_name = "Charlotte"
middle_names = "Hippopotamus"
family_name = "Turner"

#todo: calculate how long this name is
given_name = len("Charlotte")
print(given_name)
middle_names = len("Hippopotamus")
print(middle_names)
family_name = len("Turner")
print(family_name)
name_length = given_name + middle_names + family_name + 2
print(name_length)

. Types & Type Conversion

mon_sales = "121"
tues_sales = "105"
wed_sales = "110"
thurs_sales = "98"
fri_sales = "95"

#TODO: Print a string with this format: This week's total sales: xxx
# You will probably need to write several lines of code before the print statement.
weekly_sales = int(mon_sales) + int(tues_sales) + int(wed_sales) + int(thurs_sales) + int(fri_sales)
weekly_sales = str(weekly_sales)  #convert the type back!!
print("This week's total sales: " + weekly_sales)

. String Methods I

prophecy = "And there shall in that time be rumours of things going astray, and there will be a great confusion as to where things really are, and nobody will really know where lieth those little things with the sort of raffia work base, that has an attachment…at this time, a friend shall lose his friends’s hammer and the young shall not know where lieth the things possessed by their fathers that their fathers put there only just the night before around eight o’clock…"

vowel_count = 0
lower_prophecy = prophecy.lower()
vowel_count += lower_prophecy.count('a')
vowel_count += lower_prophecy.count('e')
vowel_count += lower_prophecy.count('i')
vowel_count += lower_prophecy.count('o')
vowel_count += lower_prophecy.count('u')

# TODO: set the value of vowel_count to be the number of vowels in prophecy
# Print the final count
print(vowel_count)

. String Methods II

city = "Seoul"
high_temperature = 18
low_temperature = 9
temperature_unit = "degrees Celsius"
weather_conditions = "light rain"

#todo rewrite this line to use the format method rather than string concatenation
alert = "Today's forecast for " + city + ": The temperature will range from " + str(low_temperature) + " to " + str(high_temperature) + " " + temperature_unit + ". Conditions will be " + weather_conditions + ".".format(city, low_temperature, high_temperature, temperature_unit, weather_conditions)

# print the alert
print(alert)

(2)Functions, Installtion and Conditionals:
. Defining Functions I

# todo: define a function named `population_density` that takes two arguments, 
# `population` and `land_area` (in square kilometres), and returns a population 
# density calculated from those values.

# Your code goes here!
def population_density(population, land_area):
    return population/land_area




# Here are test cases to verify that your function works as expected:
test1 = population_density(10, 1)
expected_result1 = 10
print("expected result: {}, actual result: {}".format(expected_result1, test1))

test2 = population_density(864816, 121.4)
expected_result2 = 7123.6902801
print("expected result: {}..., actual result: {}".format(expected_result2, test2))

. Defining Functions II

def readable_timedelta(days):
    "Print the number of weeks and days in a number of days."
    # to get the number of weeks we use the integer division
    weeks = days // 7
    #to get the number of days that remain we use %, the modulus operator
    remainder = days % 7
    return "{} week(s) and {} day(s)".format(weeks, remainder)
    
. Defining Functions III
. Downloading Python
. Pyhton Programming Setup
. Code with Branches I

def readable_timedelta(days):
    "Print the number of weeks and days in a number of days."
    # to get the number of weeks we use the integer division
    weeks = days // 7
    #to get the number of days that remain we use %, the modulus operator
    remainder = days % 7
    return "{} week(s) and {} day(s)".format(weeks, remainder)
    
. Code with Branches II
. Code with Branches III

def cylinder_surface_area(radius, height, has_top_and_bottom):
    side_area = height * 6.28 * radius
    if has_top_and_bottom:
        top_area = 3.14 * radius ** 2
        side_area += 2 * top_area
    return side_area
    
. Code with Branches IV

def which_prize(points):
    """
    Returns the number of prize-winning message, given a number of points
    """
    prize = None
    if points <= 50:
        prize = "a wooden rabbit"
    elif 150 <= points <= 180:
        prize = "a wafer-thin mint"
    elif points >= 181:
        prize = "a penguin"
    if prize:
        return "Congratulations! You have won " + prize + "!"
    else:
        return "Oh dear, no prize this time."
        
. Code with Branches V
. Breaking Programs into smaller Pieces
. Outlining and Building a Program

def convert_to_numeric(score):
    """
    Convert the score to a numerical type.
    """
    converted_score = #convert the score
    return converted_score

def sum_of_middle_three(score1,score2,score3,score4,score5):
    """
    Find the sum of the middle three numbers out of the five given.
    """
    sum = #add them together and take away the max and min
    return sum

def score_to_rating_string(score):
    """
    Convert the average score, which should be between 0 and 5, 
    into a string rating.
    """
    rating =
    return rating

def scores_to_rating(score1,score2,score3,score4,score5):
    """
    Turns five scores into a rating by averaging the
    middle three of the five scores and assigning this average
    to a written rating.
    """
    #STEP 1 convert scores to numbers
    score1 = convert_to_numeric(score1)
    score2 = convert_to_numeric(score2)
    score3 = convert_to_numeric(score3)
    score4 = convert_to_numeric(score4)
    score5 = convert_to_numeric(score5)

    #STEP 2 and STEP 3 find the average of the middle three scores
    average_score =     
        sum_of_middle_three(score1,score2,score3,score4,score5)/3

    #STEP 4 turn average score into a rating
    rating = score_to_rating_string(average_score)

    return rating
    
. Breaking Program Pieces I

def convert_to_numeric(score):
    """
    Convert the score to a float.
    """
    converted_score = float(score)
    return converted_score
    
. Breaking Program Pieces II

def sum_of_middle_three(score1,score2,score3,score4,score5):
    """
    Find the sum of the middle three numbers out of the five given.
    """
    max_score = max(score1,score2,score3,score4,score5)
    min_score = min(score1,score2,score3,score4,score5)
    sum = score1 + score2 + score3 + score4 + score5 - max_score - min_score
    return sum
    
. Breaking Program Pieces III

def score_to_rating_string(av_score): 
    """
    Convert the average score, which should be between 0 and 5, 
    into a rating.
    """
    if av_score < 1:
        return "Terrible"
    elif av_score < 2:
        return "Bad"
    elif av_score < 3:
        return "OK"
    elif av_score < 4:
        return "Good"
    else:
        return "Excellent"
        
. Breaking Program Pieces IV

def convert_to_numeric(score):
    """
    Convert the score to a float.
    """
    converted_score = float(score)
    return converted_score

def sum_of_middle_three(score1,score2,score3,score4,score5):
    """
    Find the sum of the middle three numbers out of the five given.
    """
    max_score = max(score1,score2,score3,score4,score5)
    min_score = min(score1,score2,score3,score4,score5)
    sum = score1 + score2 + score3 + score4 + score5 - max_score - min_score
    return sum


def score_to_rating_string(av_score):
    """
    Convert the average score, which should be between 0 and 5, 
    into a rating.
    """
    if av_score < 1:
        rating = "Terrible"
    elif av_score < 2:
        rating = "Bad"
    elif av_score < 3:
        rating = "OK"
    elif av_score < 4:
        rating = "Good"
    else:          #Using else at the end, every possible case gets caught
        rating = "Excellent"
    return rating


def scores_to_rating(score1,score2,score3,score4,score5):
    """
    Turns five scores into a rating by averaging the
    middle three of the five scores and assigning this average
    to a written rating.
    """
    #STEP 1 convert scores to numbers
    score1 = convert_to_numeric(score1)
    score2 = convert_to_numeric(score2)
    score3 = convert_to_numeric(score3)
    score4 = convert_to_numeric(score4)
    score5 = convert_to_numeric(score5)

    #STEP 2 and STEP 3 find the average of the middle three scores
    average_score = sum_of_middle_three(score1,score2,score3,score4,score5)/3

    #STEP 4 turn average score into a rating
    rating = score_to_rating_string(average_score)

    return rating
    
. Putting together the pieces

(3)Data Structures & Loops:
. Lists I
. Lists II

def median(numbers):
    numbers.sort() 
    if len(numbers) % 2:
        # if the list has an odd number of elements,
        # the median is the middle element
        middle_index = int(len(numbers)/2)
        return numbers[middle_index]
    else:
        # if the list has an even number of elements,
        # the median is the average of the middle two elements
        right_of_middle = len(numbers)//2 
        left_of_middle = right_of_middle - 1
        return (numbers[right_of_middle] + numbers[left_of_middle])/2
        
. For Loops

def starbox(width, height):
    """print a box made up of asterisks.

    width: width of box in characters, must be at least 2
    height: height of box in lines, must be at least 2
    """
    print("*" * width) #print top edge of box
   
    # print sides of box
    # todo: print this line height-2 times, instead of three times
    print("*" + " " * (width-2) + "*") 
    print("*" + " " * (width-2) + "*")
    print("*" + " " * (width-2) + "*")

    print("*" * width) #print bottom edge of box

# Test Cases
print("Test 1:")
starbox(5, 5) # this prints correctly

print("Test 2:")
starbox(2, 3)  # this currently prints two lines too tall - fix it!

. For Loops II

def starbox(width, height):
    """print a box made up of asterisks.

    width: width of box in characters, must be at least 2
    height: height of box in lines, must be at least 2
    """
    print("*" * width) #print top edge of box

    # print sides of box
    for _ in range(height-2):
        print("*" + " " * (width-2) + "*") 

    print("*" * width) #print bottom edge of box
    
. While Loops
. Reorganizing Code

def starbox(width, height):
    """print a box made up of asterisks.

    width: width of box in characters, must be at least 2
    height: height of box in lines, must be at least 2
    """
    print("*" * width) #print top edge of box

    # print sides of box
    for _ in range(height-2):
        print("*" + " " * (width-2) + "*") 

    print("*" * width) #print bottom edge of box
    
. Sets

n = 1
while n**2 < 2000:
    squares.add(n**2)
    n += 1
    
. Sets II
. Dictionaries

population = {'Shanghai': 17.8,
              'Istanbul': 13.3,
              'Karachi': 13.0,
              'Mumbai': 12.5}
              or 
              population = {'Shanghai': 17.8, 'Istanbul': 13.3, 'Karachi': 13.0, 'Mumbai': 12.5}
              
. Dictionaries II
. Compound Data Structures
. Problem Solving Skills

(4)Files & Modules:
. Tuples
. Default Arguments
. Variable Scope
. Reading From a file

def create_cast_list(filename):
    cast_list = []
    # use with to open the file filename
    with open(filename) as f:
    # use the for loop syntax to process each line        
    # and add the actor name to cast_list
        for line in f:
            line_data = line.split(',')
            cast_list.append(line_data[0])
    return cast_list
    
. The Standard Library
. Password Generator Solution

def generate_password():
    return random.choice(word_list) + random.choice(word_list) + random.choice(word_list)
    or
    def generate_password():
    return str().join(random.sample(word_list,3))
    
. Third-Party Libraries
. Using Online Resources

(5)Wikipedia Web Crawl Case Study:
. Introduction

Automating the Wikipedia Crawl
Whilst it's interesting to click through Wikipedia, it takes a lot of time to click through and read all those articles. We're going to work on automating this process, ending up with a program that will go through Wikipedia for us, keeping track of the first links on each page and seeing where they lead. In order to do this, we'll need to find out about how web pages work and get to know some of the Python tools we can use to interact with the web and web content.

. Laying the Groundwork
. Designing the Program
. Implementing the Program
. Implementing the Program II
. Implementing the Program III
. Iterative Programming I
. Iterative Programming II
. Iterative Programming III
. Finishing Touches
. Conclusion

