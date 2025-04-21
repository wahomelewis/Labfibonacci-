# Labfibonacci-
# Fibonacci Sequence Program

def fibonacci(n):
    """
    Recursive function to calculate the nth Fibonacci number.
    """
    if n == 0:
        return 0
    elif n == 1:
        return 1
    else:
        return fibonacci(n - 1) + fibonacci(n - 2)

def main():
    print("Welcome to the Fibonacci Sequence Program!")

    # Ask the user how many terms they want to generate
    while True:
        try:
            n = int(input("How many Fibonacci terms would you like to generate? "))
            if n <= 0:
                print("Please enter a positive integer.")
            else:
                break
        except ValueError:
            print("Invalid input. Please enter a valid integer.")

    print(f"\nGenerating the first {n} terms of the Fibonacci sequence:")
    for i in range(n):
        print(f"F({i}) = {fibonacci(i)}")

# Run the program
if __name__ == "__main__":
    main()

