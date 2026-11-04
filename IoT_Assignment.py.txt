
# Question 1: Function to calculate factorial

def factorial(n):
    result = 1
    for i in range(1, n + 1):
        result = result * i
    return result

num = int(input("Enter a number: "))
print("Factorial:", factorial(num))


# Question 2: Function using keyword arguments

def student_info(name, roll_no, department):
    print("Name:", name)
    print("Roll No:", roll_no)
    print("Department:", department)

student_info(name="Murk", roll_no="Your Roll No", department="Artificial Intelligence")


# Question 3: Function using *args to calculate sum

def calculate_sum(*args):
    total = 0
    for num in args:
        total += num
    return total

print("Sum:", calculate_sum(10, 20, 30, 40))


# Question 4: Function using **kwargs

def employee_info(**kwargs):
    for key, value in kwargs.items():
        print(key, ":", value)

employee_info(name="Ali", age=25, department="IT", salary=50000)


# Question 5: Function to check password

def check_password(password):
    if (len(password) >= 8 and
        any(char.islower() for char in password) and
        any(char.isdigit() for char in password) and
        any(not char.isalnum() for char in password)):
        print("Password is valid")
    else:
        print("Password is invalid")

password = input("Enter password: ")
check_password(password)
