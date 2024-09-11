# flutterwithdat1



void main() {
  // 1. Define Variables
  int age = 25;
  double height = 5.9;
  String name = "John Doe";
  bool isStudent = false;
  List<int> numbers = [1, 20, 30, 15, 200];

  // 2. Type Conversion
  // Convert String to int and double
  String numberStr = "123";
  int numberInt = int.parse(numberStr);
  double numberDouble = double.parse(numberStr);

  // Convert int to String and double
  int anotherInt = 456;
  String anotherIntStr = anotherInt.toString();
  double anotherIntDouble = anotherInt.toDouble();

  // 3. Function for Conversion
  convertAndDisplay("789");

  // 4. Control Flow: If-Else Statements
  checkNumberSign(-10);
  checkVotingEligibility(age);

  // Switch Case for Days of the Week
  printDayOfWeek(4);

  // 5. Loops
  printNumbersForLoop();
  printNumbersWhileLoop();
  printNumbersDoWhileLoop();

  // 6. Complex Example
  analyzeNumbers(numbers);
}

// Function to convert and display String to int and double
void convertAndDisplay(String number) {
  int numInt = int.parse(number);
  double numDouble = double.parse(number);
  print("Converted $number to int: $numInt and double: $numDouble");
}

// If-Else Statements for number sign check
void checkNumberSign(int number) {
  if (number > 0) {
    print("$number is positive");
  } else if (number < 0) {
    print("$number is negative");
  } else {
    print("$number is zero");
  }
}

// If-Else Statements for voting eligibility
void checkVotingEligibility(int age) {
  if (age >= 18) {
    print("Eligible to vote.");
  } else {
    print("Not eligible to vote.");
  }
}

// Switch-Case for days of the week
void printDayOfWeek(int day) {
  switch (day) {
    case 1:
      print("Monday");
      break;
    case 2:
      print("Tuesday");
      break;
    case 3:
      print("Wednesday");
      break;
    case 4:
      print("Thursday");
      break;
    case 5:
      print("Friday");
      break;
    case 6:
      print("Saturday");
      break;
    case 7:
      print("Sunday");
      break;
    default:
      print("Invalid day");
  }
}

// For Loop to print numbers from 1 to 10
void printNumbersForLoop() {
  for (int i = 1; i <= 10; i++) {
    print(i);
  }
}

// While Loop to print numbers from 10 to 1
void printNumbersWhileLoop() {
  int i = 10;
  while (i >= 1) {
    print(i);
    i--;
  }
}

// Do-While Loop to print numbers from 1 to 5
void printNumbersDoWhileLoop() {
  int i = 1;
  do {
    print(i);
    i++;
  } while (i <= 5);
}

// Complex Example with a List and Control Flow
void analyzeNumbers(List<int> numbers) {
  for (int num in numbers) {
    print("Number: $num");

    // Check if the number is even or odd
    if (num % 2 == 0) {
      print("$num is even.");
    } else {
      print("$num is odd.");
    }

    // Categorize the number using switch statement
    switch (num) {
      case 1:
      case 2:
      case 3:
      case 4:
      case 5:
      case 6:
      case 7:
      case 8:
      case 9:
      case 10:
        print("$num is small.");
        break;
      case 11 ... 100:
        print("$num is medium.");
        break;
      default:
        print("$num is large.");
    }
  }
}
