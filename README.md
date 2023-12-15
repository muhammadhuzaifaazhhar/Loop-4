# Loop-4
# Problem 4: Employee Gross Pay

# Initialize variables
employee_count = 0
total_gross_pay = 0

# Prompt user to continue
user_input = input("Do you want to continue? (Yes/No): ")

# Use a while loop based on user input
while user_input.lower() == "yes":
    # Prompt user for employee data
    last_name = input("Enter last name: ")
    hours_worked = float(input("Enter hours worked: "))
    rate_of_pay = float(input("Enter rate of pay: "))
    
    # Calculate gross pay
    if hours_worked > 40:
        gross_pay = 40 * rate_of_pay + (hours_worked - 40) * 1.5 * rate_of_pay
    else:
        gross_pay = hours_worked * rate_of_pay
    
    # Display results
    print(f"{last_name}'s Gross Pay: ${gross_pay:.2f}")
    
    # Update counters
    employee_count += 1
    total_gross_pay += gross_pay
    
    # Prompt user to continue
    user_input = input("Do you want to continue? (Yes/No): ")

# Display total gross pay, number of employees, and average pay
print(f"\nTotal Gross Pay: ${total_gross_pay:.2f}")
print(f"Total Number of Employees: {employee_count}")
print(f"Average Pay: ${total_gross_pay / employee_count:.2f}")
