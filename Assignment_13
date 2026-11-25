import threading

# Function to count numbers
def count_numbers():
    for i in range(1, 6):
        print("Number:", i)

# Function to calculate squares
def calculate_squares():
    for i in range(1, 6):
        print("Square of", i, "=", i * i)

# Function to calculate cubes
def calculate_cubes():
    for i in range(1, 6):
        print("Cube of", i, "=", i * i * i)

# Main function
if __name__ == "__main__":

    # Create threads
    t1 = threading.Thread(target=count_numbers)
    t2 = threading.Thread(target=calculate_squares)
    t3 = threading.Thread(target=calculate_cubes)

    # Start threads
    t1.start()
    t2.start()
    t3.start()

    # Wait for threads to complete
    t1.join()
    t2.join()
    t3.join()

    print("All threads completed successfully.")
