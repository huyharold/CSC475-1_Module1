# CSC475-1_Module1
fun main() {
    // Step 1: Ask the user for the first number
    print("Enter first number: ")
    val number1 = readLine()?.toDoubleOrNull()

    // Step 2: Check if the first input is valid
    if (number1 == null) {
        println("Invalid input for the first number.")
        return
    }

    // Step 3: Ask the user for the operator (+, -, *, /)
    print("Enter operator (+, -, *, /): ")
    val operator = readLine()
    // Step 4: Ask for the second number
    print("Enter second number: ")
    val number2 = readLine()?.toDoubleOrNull()

    // Step 5: Check if the second input is valid
    if (number2 == null) {
        println("Invalid input for the second number.")
        return
    }

    // Step 6: Perform the calculation based on the operator
    val result = when (operator) {
        "+" -> number1 + number2
        "-" -> number1 - number2
        "*" -> number1 * number2
        "/" -> if (number2 != 0.0) {
            number1 / number2
        } else {
            println("Division by zero is not allowed.")
            return
        }
        else -> {
            println("Invalid operator.")
            return
        }
    }

    // Step 7: Output the result
    println("The result of $number1 $operator $number2 is: $result")
}

