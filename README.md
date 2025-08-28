# ================================================
# Python Interactive Cybersecurity & IT Simulation
# Author: Abhijeet Kumar Ray
# ================================================

# ------------------ User Introduction ------------------
def introduction():
    user_name = input("Enter your name: ")
    print(f"Welcome {user_name} to the game!")
    
    first_name = input("Enter your first name: ")
    print(f"Hello everyone, my name is {first_name}")
    
    user_age = int(input("Enter your age: "))
    print(f"I am {user_age} years old")
    
    user_gender = input("Enter your gender: ")
    print(f"I am a {user_gender}")
    
    user_address = input("Enter your address: ")
    print(f"I am from {user_address}")
    
    user_phone = input("Enter your phone number: ")
    print(f"My phone number is {user_phone}")
    
    user_email = input("Enter your email: ")
    print(f"My email is {user_email}")
    
    user_marks = float(input("Enter your marks (out of 500): "))
    percentage = (user_marks / 500) * 100
    print(f"My percentage is {percentage:.2f}%")
    print("Thanks for playing the introduction game!\n")

# ------------------ Password Strength Checker ------------------
def password_checker():
    password = input("Enter your password: ")
    if (len(password) >= 10 and any(char.isdigit() for char in password) 
        and any(char.isupper() for char in password) 
        and any(char.islower() for char in password) 
        and any(char in "!@#$%^&*()-+" for char in password)):
        print("Strong password\n")
    elif (len(password) >= 8 and any(char.isdigit() for char in password) 
          and any(char.isupper() for char in password) 
          and any(char.islower() for char in password)):
        print("Weak password\n")
    else:
        print("Very weak password\n")

# ------------------ Internet Bandwidth Allocation ------------------
def bandwidth_allocation():
    customer_type = input("Enter customer type (premium/normal): ")
    if customer_type.lower() == "premium":
        print("Welcome! Enjoy world-class high-speed features!\n")
    else:
        print("Please upgrade your plan for better internet experience.\n")

# ------------------ Salary Tax Calculator ------------------
def salary_tax_calculator():
    salary = int(input("Enter your salary: "))
    if salary > 100000:
        tax = salary * 0.20
    elif salary > 50000:
        tax = salary * 0.10
    else:
        tax = 0
    print(f"Your salary after tax: {salary - tax}\n")

# ------------------ Failed Login Attempts ------------------
def login_attempts():
    failed_attempts = int(input("Enter number of failed login attempts: "))
    if failed_attempts >= 3:
        print("🔒 Account Locked for Security Reasons\n")
    else:
        print("✅ You still have chances to login\n")

# ------------------ File Storage Decision ------------------
def file_storage():
    file_size = int(input("Enter the file size in MB: "))
    if file_size > 100:
        print("☁️ Store in Cloud Storage\n")
    else:
        print("💾 Store in Local Storage\n")

# ------------------ Transaction Verification ------------------
def transaction_verification():
    amount = int(input("Enter transaction amount: "))
    if amount > 100000:
        print("🚨 Transaction flagged! Needs verification.\n")
    else:
        print("✅ Transaction Successful\n")

# ------------------ Server Load Monitoring ------------------
def server_load_monitoring():
    load = int(input("Enter server load percentage: "))
    if load > 80:
        print("🚨 Critical Server Load! Add more servers.\n")
    elif load >= 50:
        print("⚠️ High Load, Monitor Closely.\n")
    else:
        print("✅ Server Load Normal\n")

# ------------------ Menu to Run Each Module ------------------
def main():
    while True:
        print("===== Cybersecurity & IT Simulation Menu =====")
        print("1. User Introduction")
        print("2. Password Strength Checker")
        print("3. Internet Bandwidth Allocation")
        print("4. Salary Tax Calculator")
        print("5. Login Attempt Check")
        print("6. File Storage Decision")
        print("7. Transaction Verification")
        print("8. Server Load Monitoring")
        print("9. Exit")
        choice = input("Enter your choice (1-9): ")
        
        if choice == "1":
            introduction()
        elif choice == "2":
            password_checker()
        elif choice == "3":
            bandwidth_allocation()
        elif choice == "4":
            salary_tax_calculator()
        elif choice == "5":
            login_attempts()
        elif choice == "6":
            file_storage()
        elif choice == "7":
            transaction_verification()
        elif choice == "8":
            server_load_monitoring()
        elif choice == "9":
            print("Thanks for using the simulation! Goodbye.")
            break
        else:
            print("Invalid choice. Please enter 1-9.\n")

# Run the program
if __name__ == "__main__":
    main()
