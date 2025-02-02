# SwingCalculator-U23MTH1022-

Adeleke Oluwatimilehin 

U23MTH1022

MATHEMATICS 

This Java code implements a basic Swing-based calculator application. Let's break down its functionality, structure, and limitations in detail:
Functionality:
The calculator allows users to perform simple arithmetic calculations involving two operands and one operator.  It supports addition, subtraction, multiplication, and division. Users input numbers using the number buttons, select an operator, input the second number, and then press the equals button to see the result. The clear button resets the calculator.
Structure:
 * Imports: The code imports necessary classes from the javax.swing, java.awt, and java.awt.event packages. These provide the foundation for creating the graphical user interface (GUI) and handling user interactions.
 * Class Declaration: The SwingCalculator class extends JFrame, making it a top-level window. It also implements the ActionListener interface, which enables it to respond to button clicks.
 * Instance Variables: The class declares instance variables to represent the GUI components:
   * displayField: A JTextField to display the input and results.
   * numberButtons: An array of JButton objects for the digits 0-9.
   * operatorButtons: An array of JButton objects for the operators +, -, *, and /.
   * decimalButton, equalButton, clearButton: JButton objects for the decimal point, equals, and clear operations.
   * currentInput: A String to store the user's input as it's being typed.
   * operator: A String to store the selected operator.
 * Constructor (SwingCalculator()): The constructor is responsible for setting up the GUI:
   * It sets the title, size, and close operation of the window.
   * It uses a BorderLayout for the main window layout.
   * It creates the JTextField for the display and adds it to the NORTH of the window.
   * It creates JPanel objects to hold the buttons and uses a GridLayout for the number buttons and operator buttons.
   * It instantiates the JButton objects, sets their text, and adds ActionListener instances (the calculator object itself) to them so that clicks can be handled.
   * It adds the button panels and individual buttons to the main window's CENTER using a FlowLayout.
   * Finally, it sets the window to visible.
 * actionPerformed(ActionEvent e): This method is called whenever a button is clicked. It retrieves the action command (the text on the button) and performs the appropriate action:
   * If it's a digit, it appends it to currentInput and updates the display.
   * If it's a decimal point, it adds it to currentInput only if there's not already one present.
   * If it's an operator, it stores the operator and appends it (with spaces) to currentInput.
   * If it's the equals button, it calls evaluateExpression to calculate the result, displays it, and updates currentInput.  It also includes a try-catch block to handle potential exceptions during the evaluation.
   * If it's the clear button, it resets currentInput, operator, and the display.
 * evaluateExpression(String expression): This method takes the expression string (e.g., "5 + 3") and calculates the result.
   * It splits the string into parts based on spaces.
   * It parses the first and third parts as doubles (operands).
   * It uses a switch statement to perform the correct calculation based on the stored operator.
   * It handles division by zero by throwing an ArithmeticException.
 * main(String[] args): The main method creates an instance of the SwingCalculator class, which starts the application.
Limitations:
 * Order of Operations: The calculator does not respect operator precedence.  It evaluates expressions strictly from left to right.  For example, 2 + 3 * 4 will be calculated as (2 + 3) * 4 = 20, not the correct 2 + (3 * 4) = 14.
 * Chained Operations: Performing a sequence of calculations (e.g., 2 + 3 = then * 4) is not directly supported.
 * Error Handling: Error handling is basic. It catches division by zero but doesn't handle other potential errors, like invalid input (e.g., non-numeric characters).
 * User Interface: The layout is simple. A GridLayout for the buttons would provide a more standard calculator appearance.  The display text is left-aligned, whereas right alignment is typical for calculators.
 * No Memory: The calculator doesn't have memory functionality (e.g., storing and recalling previous results).
Summary:
This code provides a basic implementation of a Swing calculator. It demonstrates the use of Swing components, event handling, and simple arithmetic calculations. However, it has significant limitations regarding order of operations, chained operations, error handling, and user interface design. It serves as a good starting point for learning Swing but would need significant improvements to be considered a robust and user-friendly calculator application.
