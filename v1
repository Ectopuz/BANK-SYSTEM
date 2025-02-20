class BankAccount:
    def __init__(self, account_holder, balance=0):
        self.account_holder = account_holder
        self.balance = balance

    def deposit(self, amount):
        if amount > 0:
            self.balance += amount
            print(f"Deposited {amount}. New balance is {self.balance}.")
        else:
            print("Deposit amount must be greater than zero.")

    def withdraw(self, amount):
        if amount > 0 and amount <= self.balance:
            self.balance -= amount
            print(f"Withdrew {amount}. New balance is {self.balance}.")
        elif amount > self.balance:
            print("Insufficient funds.")
        else:
            print("Withdrawal amount must be greater than zero.")

    def check_balance(self):
        print(f"Your current balance is {self.balance}.")

def create_account():
    name = input("Enter your name: ")
    initial_deposit = float(input("Enter initial deposit amount: "))
    account = BankAccount(name, initial_deposit)
    print(f"Account created for {name} with balance {initial_deposit}.")
    return account

def main():
    print("Welcome to the basic banking system.")
    account = create_account()

    while True:
        print("\nChoose an option:")
        print("1. Deposit")
        print("2. Withdraw")
        print("3. Check Balance")
        print("4. Exit")

        choice = input("Enter your choice (1/2/3/4): ")

        if choice == '1':
            deposit_amount = float(input("Enter deposit amount: "))
            account.deposit(deposit_amount)
        elif choice == '2':
            withdraw_amount = float(input("Enter withdrawal amount: "))
            account.withdraw(withdraw_amount)
        elif choice == '3':
            account.check_balance()
        elif choice == '4':
            print("Thank you for using the banking system. Goodbye!")
            break
        else:
            print("Invalid choice, please try again.")

if __name__ == "__main__":
    main()
