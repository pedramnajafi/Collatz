# Collatz
The Collatz conjecture is one of the most famous unsolved problems in mathematics. The conjecture asks whether repeating two simple arithmetic operations will eventually transform every positive integer into 1


    def collatz(number):
        if number % 2 == 0:
            print(number // 2)
            return number // 2
        elif number % 2 == 1:
            result = 3 * number + 1
            print(result)
            return result
    try:
        number_inserted = input('Please enter a number ')
        while number_inserted != 1:
            number_inserted = collatz(int(number_inserted))
    except ValueError:
        print('you must enter a number')    
