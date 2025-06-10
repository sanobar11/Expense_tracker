# How to Run the Expense/Income Tracker Java Application

This document provides step-by-step instructions to compile and run the Java Expense/Income Tracker application on both Windows and Linux systems.

## Prerequisites

- Java Development Kit (JDK) 8 or higher installed
- Internet connection (for downloading dependencies)

## Windows Instructions (PowerShell)

### Step 1: Navigate to Project Directory
```powershell
cd "c:\Users\OMER\Desktop\nfnfn\Expense_Income_Tracker"
```

### Step 2: Create Library Directory and Download FlatLaf Dependency
```powershell
mkdir -p lib
curl -o lib/flatlaf-3.4.1.jar https://repo1.maven.org/maven2/com/formdev/flatlaf/3.4.1/flatlaf-3.4.1.jar
```

### Step 3: Compile the Java Files
```powershell
javac -cp "src;lib/flatlaf-3.4.1.jar" src/expense_income_tracker/*.java
```

### Step 4: Run the Application
```powershell
java -cp "src;lib/flatlaf-3.4.1.jar" expense_income_tracker.ExpensesIncomesTracker
```

## Linux Instructions (Bash)

### Step 1: Navigate to Project Directory
```
git clone https://github.com/bhavesh003/Expense_Income_Tracker
```
```bash
cd /path/to/your/Expense_Income_Tracker
```

### Step 2: Create Library Directory and Download FlatLaf Dependency
```bash
mkdir -p lib
curl -o lib/flatlaf-3.4.1.jar https://repo1.maven.org/maven2/com/formdev/flatlaf/3.4.1/flatlaf-3.4.1.jar
```
*Alternative using wget:*
```bash
wget -O lib/flatlaf-3.4.1.jar https://repo1.maven.org/maven2/com/formdev/flatlaf/3.4.1/flatlaf-3.4.1.jar
```

### Step 3: Compile the Java Files
```bash
javac -cp "src:lib/flatlaf-3.4.1.jar" src/expense_income_tracker/*.java
```

### Step 4: Run the Application
```bash
java -cp "src:lib/flatlaf-3.4.1.jar" expense_income_tracker.ExpensesIncomesTracker
```

## Expected Output

After running Step 4, you should see:
- A GUI window with dark theme opens
- The application title "Expense/Income Tracker"
- A table for displaying entries
- Buttons for Add, Edit, Remove operations
- A balance display at the bottom

## Troubleshooting

### Common Issues:

1. **Java not found**: Ensure Java is installed and added to your system PATH
2. **Compilation errors**: Make sure all Java files are present in the src/expense_income_tracker/ directory
3. **Download fails**: Check internet connection or use alternative download method
4. **GUI doesn't appear**: Ensure you have a graphical environment (not running in headless mode)

### Verification Commands:

Check Java version:
```bash
# Windows (PowerShell) or Linux
java -version
javac -version
```

Check if JAR file downloaded correctly:
```bash
# Windows (PowerShell)
ls lib/

# Linux
ls -la lib/
```

## Notes

- The application uses FlatLaf library for a modern dark theme UI
- Compilation warnings about unchecked operations are normal and don't affect functionality
- The application will create/use a data file named `expenses_incomes_data.dat` for persistence
- Make sure you have sufficient permissions to create files in the project directory
