# NUMBER-GUESSING-GAME
#include <iostream>
#include <cstdlib> // for rand() and srand()
#include <ctime> // for time()

using namespace std;

int main() {
    // Seed the random number generator
    srand(time(nullptr));

    // Generate a random number between 1 and 100
    int secretNumber = rand() % 100 + 1;

    int guess;
    int attempts = 0;

    cout << "Welcome to the Number Guessing Game!" << endl;

    // Keep looping until the user guesses the correct number
    while (true) {
        cout << "Guess the number (between 1 and 100): ";
        cin >> guess;
        attempts++;

        // Provide feedback on the guess
        if (guess < secretNumber) {
            cout << "Too low! Try again." << endl;
        } else if (guess > secretNumber) {
            cout << "Too high! Try again." << endl;
        } else {
            cout << "Congratulations! You've guessed the correct number " << secretNumber << " in " << attempts << " attempts!" << endl;
            break;
        }
    }

    return 0;
}
