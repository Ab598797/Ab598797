#include <iostream>

typedef unsigned int uint;

bool isUgly(uint num) {
    if (num <= 0) return false; // Ugly numbers are positive

    // Divide num by 2, 3, and 5 as long as it is divisible
    while (num % 2 == 0) num /= 2;
    while (num % 3 == 0) num /= 3;
    while (num % 5 == 0) num /= 5;

    // After removing all 2s, 3s, and 5s, if num is 1, it's ugly
    return num == 1;
}

int main() {
    uint number; // Corrected 'Unit' to 'uint'
    std::cout << "Enter a number: ";
    std::cin >> number;
    
    if (isUgly(number)) {
        std::cout << number << " is an ugly number." << std::endl;
    } else {
        std::cout << number << " is not an ugly number." << std::endl;
    }

    return 0;
}








