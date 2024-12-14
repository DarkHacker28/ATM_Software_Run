# ATM Software Run

Overview : 

The ATM Software project simulates the functionality of an Automated Teller Machine (ATM). It integrates HTML, CSS, Python, JavaScript, and C++ to create an interactive, efficient, and user-friendly interface for ATM operations. This project demonstrates the seamless integration of various technologies while utilizing C++ functions and classes for backend computations.

# Features : 

User Authentication: Secure login system with password protection.
Balance Inquiry: Check account balance instantly.
Cash Withdrawal: Withdraw specified amounts with validation against account balance and ATM cash availability.
Deposit Cash: Deposit funds to update the account balance.
Transaction History: View recent transactions for better account management.
Responsive Design: User interface optimized for various devices.

# Technologies Used :

HTML: Structure the web interface.

CSS: Style the interface for a modern, user-friendly look.

JavaScript: Add interactivity and handle client-side validations.

Python: Backend logic for handling transactions and database operations.

C++: Core computational tasks such as processing withdrawals, deposits, and other financial calculations.

# Key Components :

Frontend:
HTML and CSS are used to design an intuitive interface with forms for inputs like PIN entry, withdrawal amount, and deposit details.
JavaScript provides client-side validation for input fields and enhances user interactions.

Backend:
Python manages the main logic for user authentication, updating account balances, and interacting with the database.
C++ is integrated using Python bindings (e.g., pybind11 or ctypes) to execute performance-critical operations like financial calculations securely and efficiently.

Database:
A simple database stores user information, balances, and transaction logs.

# How It Works :

Step 1: The user logs in by entering their account number and PIN.
Step 2: After successful authentication:
Step 3: They can check their balance.
Step 4: Perform transactions such as withdrawals or deposits.
Step 5: View a summary of their transaction history.
Step 6: Each action interacts with backend logic in Python, which calls C++ functions to ensure fast and accurate computation.
Step 7: The system provides real-time feedback through JavaScript to enhance user experience.

# Installation :

Clone this repository:

git clone (https://github.com/DarkHacker28/ATM_Software_Run)

cd atm-software

# Install dependencies :

Python libraries: pip install flask pybind11 sqlite3
Ensure a compatible C++ compiler is installed.

# Run the backend server :

python app.py
Open index.html in a browser to start using the software.

# C++ Integration Example :

Here's an example of a core financial operation implemented in C++:

class ATM {
public:
    double checkBalance(double balance) {
        return balance;
    }
    
    double withdraw(double balance, double amount) {
        if (amount > balance) {
            throw std::invalid_argument("Insufficient funds");
        }
        return balance - amount;
    }

    double deposit(double balance, double amount) {
        return balance + amount;
    }
};

The above C++ functions are compiled and accessed in Python via bindings to ensure smooth integration.


# Contributions :
Contributions are welcome! Feel free to fork the repository and submit pull requests.
