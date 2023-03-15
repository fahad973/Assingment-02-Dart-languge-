# Assingment-02-Dart-languge-
class Circle {
  double _radius = 0;

  double get radius => _radius;

  set radius(double value) {
    if (value <= 0) {
      throw ArgumentError('Radius cannot be zero or negative.');
    }
    _radius = value;
  }

  double getCircumference() {
    return 2 * 3.14 * _radius;
  }
}

class Student {
  String _name = '';
  int _age = 0;
  String _major = '';
  double _gpa = 0;

  String get name => _name;

  set name(String value) {
    if (value.isEmpty) {
      throw ArgumentError('Name cannot be empty.');
    }
    _name = value;
  }

  int get age => _age;

  set age(int value) {
    if (value <= 0) {
      throw ArgumentError('Age cannot be zero or negative.');
    }
    _age = value;
  }

  String get major => _major;

  set major(String value) {
    if (value.isEmpty) {
      throw ArgumentError('Major cannot be empty.');
    }
    _major = value;
  }

  double get gpa => _gpa;

  set gpa(double value) {
    if (value < 0 || value > 4) {
      throw ArgumentError('GPA must be between 0 and 4.');
    }
    _gpa = value;
  }

  String getGradeLevel() {
    if (_age < 18) {
      return 'High School';
    } else if (_age >= 18 && _age < 22) {
      return 'College';
    } else {
      return 'Graduate School';
    }
  }
}

class Book {
  String _title = '';
  String _author = '';
  String _publisher = '';
  double _price = 0;

  String get title => _title;

  set title(String value) {
    if (value.isEmpty) {
      throw ArgumentError('Title cannot be empty.');
    }
    _title = value;
  }

  String get author => _author;

  set author(String value) {
    if (value.isEmpty) {
      throw ArgumentError('Author cannot be empty.');
    }
    _author = value;
  }

  String get publisher => _publisher;

  set publisher(String value) {
    if (value.isEmpty) {
      throw ArgumentError('Publisher cannot be empty.');
    }
    _publisher = value;
  }

  double get price => _price;

  set price(double value) {
    if (value <= 0) {
      throw ArgumentError('Price cannot be zero or negative.');
    }
    _price = value;
  }

  double getDiscountPrice(double percentage) {
    if (percentage < 0 || percentage > 100) {
      throw ArgumentError('Percentage must be between 0 and 100.');
    }
    double discount = percentage / 100;
    return _price - (_price * discount);
  }
}

void main() {
  // Code to test the classes
}
class Course {
  String _name = '';
  String _code = '';
  String _instructor = '';
  int _credits = 0;
  double _costPerCredit = 0.0;

  String get name => _name;

  set name(String value) {
    if (value.isEmpty) {
      throw ArgumentError('Name cannot be empty.');
    }
    _name = value;
  }

  String get code => _code;

  set code(String value) {
    if (value.isEmpty) {
      throw ArgumentError('Code cannot be empty.');
    }
    _code = value;
  }

  String get instructor => _instructor;

  set instructor(String value) {
    if (value.isEmpty) {
      throw ArgumentError('Instructor cannot be empty.');
    }
    _instructor = value;
  }

  int get credits => _credits;

  set credits(int value) {
    if (value <= 0) {
      throw ArgumentError('Credits cannot be zero or negative.');
    }
    _credits = value;
  }

  double get costPerCredit => _costPerCredit;

  set costPerCredit(double value) {
    if (value <= 0) {
      throw ArgumentError('Cost per credit cannot be zero or negative.');
    }
    _costPerCredit = value;
  }

  double getTotalCost() {
    return _credits * _costPerCredit;
  }
}

class Bank {
  List<BankAccount> _accounts = [];

  void addAccount(BankAccount account) {
    _accounts.add(account);
  }

  void removeAccount(BankAccount account) {
    _accounts.remove(account);
  }

  BankAccount? getAccountWithHighestBalance() {
    if (_accounts.isEmpty) {
      return null;
    }
    BankAccount highestBalanceAccount = _accounts[0];
    for (int i = 1; i < _accounts.length; i++) {
      if (_accounts[i].balance > highestBalanceAccount.balance) {
        highestBalanceAccount = _accounts[i];
      }
    }
    return highestBalanceAccount;
  }
}

class BankAccount {
  String _accountNumber = '';
  String _accountHolderName = '';
  double _balance = 0.0;

  String get accountNumber => _accountNumber;

  set accountNumber(String value) {
    if (value.isEmpty) {
      throw ArgumentError('Account number cannot be empty.');
    }
    _accountNumber = value;
  }

  String get accountHolderName => _accountHolderName;

  set accountHolderName(String value) {
    if (value.isEmpty) {
      throw ArgumentError('Account holder name cannot be empty.');
    }
    _accountHolderName = value;
  }

  double get balance => _balance;

  set balance(double value) {
    if (value < 0) {
      throw ArgumentError('Balance cannot be negative.');
    }
    _balance = value;
  }
}

void main() {
  String input = 'racecar';
  bool isPalindrome = true;

  for (int i = 0; i < input.length ~/ 2; i++) {
    if (input[i] != input[input.length - i - 1]) {
      isPalindrome = false;
      break;
    }
  }

  if (isPalindrome) {
    print('$input is a palindrome.');
  } else {
    print('$input is not a palindrome.');
  }
}
