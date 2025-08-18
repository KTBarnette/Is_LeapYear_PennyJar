###########################################################################
# Kyle Barnette                                                           #
# Lab 3 COSC 1336-012 Programming Fundamentals I (47440) Kathryn Rehfield #
# This program will get the user's name, birth month and year and return  #
# an output with what season they were born in and if they were born in a #
# leap year or not.                                                       #       #
# This program will ask the user how many pennies they have and count     #
# this number into dollars, quarters, dimes, nickles and pennies.         #    #
###########################################################################

def main():
    # Obtain the user's name
    name = input ('Greetings! What is your name (Type zzz to end)?: ')
    # This sentinel will allow the user to abort the program
    while name != 'zzz':
        
        
        birth_month = get_month()            
        season = find_season(birth_month)
        birth_year = get_year()            
        leap_year = is_leap_year(birth_year)
        if leap_year == True:
            leap_message = 'was a leap year'
        else:
            leap_message = 'was not a leap year'
            
        

        print(f'Hello, {name}! You were born in the {season} and {birth_year} {leap_message}.')
        # Read pennies
        pennies = int(input('How many pennies do you have?:'))
        # Call Penny_jar
        penny_jar(pennies)

        name = input ('Greetings! What is your name (Type zzz to end)?: ')
        
# Function name: get_month
# Input: none #
# Output: A number between 1-12 #
# Purpose: This function reads the integer birth month    
def get_month():
    
    # Read the integer of the entered birth month
    birth_month = int(input ('Type the month you were born in as a number 1-12: '))
    # This while loop will validate the user's input
    while birth_month <1 or birth_month > 12:
        print('Invalid entry, please try again')
        birth_month = int(input ('Type the month you were born in as a number 1-12: '))
    return birth_month

# Function name: get_year 
# Input: none 
# Output: The year the user was born
# Purpose: This function reads and validates the birth year
def get_year():
    #What year were they born in
    birth_year = int(input ('What year were you born?: '))
    while birth_year <=0:
        print('Invalid entry, please try again')
        birth_year = int(input('What year were you born?: '))
    return birth_year

# Function name: find_season
# Input: The numeric value of (month)
# Output: The season
# Purpose: This function gives us the season the user was born in
def find_season(month):
    
    # Which season were they born in
    if month <= 2 or month == 12:
        season = "winter"
    elif month <= 5:
        season = "spring"
    elif month <= 8:
        season = "summer"
    else:
        season = "fall"
    return season

# Function name: is_leap_year
# Input: The birth year
# Output: True if leap year, false otherwise
# Purpose: This function decides if the year is a leap year or not
def is_leap_year(year):

    if year % 4 == 0:
        # If year is a century year
        # check to see if it is evenly divisible by 400
        if year % 100 == 0:
            # At this point, if year is evenly divisible
            # by 400 it is a leap year
            if year % 400 == 0:
                leap_year = True
            else:
                # Century year that is not evenly 
                # divisible by 400 is not a leap year
                leap_year = False
        else:
            # A year evenly divisible by 4 that is
            # not a century year is a leap year
            leap_year = True
    else:
        # A year that is not evenly 
        # divisible by 4 is not a leap year
        leap_year = False
    return leap_year

# Function name: penny_jar
# Input: How many pennies do you have
# Output: Dollars, quarters, dimes, nickles, pennies
# Purpose: Calculate and display the coins you have
def penny_jar(cents):
    dollars = cents//100
    cents = cents - (dollars * 100)
    quarters = cents//25
    cents = cents - (quarters * 25)
    dimes = cents//10
    cents = cents - (dimes * 10)
    nickles = cents//5
    cents = cents - (nickles * 5)
    if dollars == 1:
        print(f'{dollars} Dollar')
    elif dollars != 0:
        print(f'{dollars} Dollars')
    if quarters == 1:
        print(f'{quarters} Quarter')
    elif quarters != 0:
        print(f'{quarters} Quarters')
    if dimes == 1:
        print(f'{dimes} Dime')
    elif dimes != 0:
        print(f'{dimes} Dimes')
    if nickles == 1:
        print(f'{nickles} Nickle')
    elif nickles != 0:
        print(f'{nickles} Nickles')
    if cents == 1:
        print(f'{cents} Penny')
    elif cents != 0:
        print(f'{cents} Pennies')
main()


    
            




