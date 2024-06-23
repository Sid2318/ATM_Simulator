# ATM_Simulator
print("Welcome to the Simple ATM Simulator")

acc_bal= 1000.00
verify_pin = '1234'

pin = input("Enter the Verify Pin: ")
if verify_pin == pin:
    atm_on = True
else:
    print("Invalid PIN. Exiting.")
    atm_on = False  

while atm_on == True:
    print("Main Menu: ")
    print("1. Check Balance")
    print("2. Deposite Money")
    print("3. Withdraw Money")
    print("4. Exit")

    choice = input("Enter the choice: ")

    if choice == '1':
        print(f"Current Bank Balance = Rs.{acc_bal}")

    elif choice == '2' : 
        deposit_money = float(input("Enter the Amount you want to Deposite: "))  
        print(f"Previous account balance Rs.{acc_bal}")
        print(f"Deposite Amount Rs.{deposit_money}")
        acc_bal = acc_bal + deposit_money
        print(f"Updated Balance Rs.{acc_bal}")

    elif choice == '3' :
        withdraw_money = float(input("Enter the amount you want to Withdraw: "))
        if withdraw_money > acc_bal:
            print("Insufficient Balance")
        else:
            print("Withdrawal Confirmed")
            print(f"Previous account balance Rs.{acc_bal}")
            print(f"Withdraw Amount Rs.{deposit_money}")
            acc_bal = acc_bal - withdraw_money
            print(f"Updated Balance Rs.{acc_bal}")    

    elif choice == '4' :
        atm_on = False
        print("Thank You for Using ATM. Goodbye!")
        break

    else:
        print("Invalid Choice")        
        print("Try Again!")
