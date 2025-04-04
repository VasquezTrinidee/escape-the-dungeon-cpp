#include <iostream>
#include <limits>

using namespace std;

int getChoice(int min, int max) {
    int choice;
    while (true) {
        cout << "Enter your choice: ";
        cin >> choice;
        if (cin.fail() || choice < min || choice > max) {
            cin.clear();
            cin.ignore(numeric_limits<streamsize>::max(), '\n');
            cout << "Invalid input! Please enter a number between " << min << " and " << max << ".\n";
        } else {
            return choice;
        }
    }
}

int main() {
    int health = 100; 
    int choice;

    cout << "Welcome to 'Escape the dungeon'!\n";
    cout << "You wake up in a dark dungeon with a note beside you: 'Escape before the dungeon claims you.'\n";
    cout << "Your health starts at 100.\n\n";

    cout << "You reach a fork in the dungeon. Do you:\n";
    cout << "1. Go left (a dark and damp corridor)\n";
    cout << "2. Go right (a flickering torch illuminates the path)\n";

    choice = getChoice(1, 2);

    if (choice == 1) {
        cout << "You trip over a loose stone and hit your head! (-10 Health)\n";
        health -= 10;
    } else {
        cout << "The torchreveals a hidden passage.\n";
    }

    cout << "Current Health: " << health << "\n\n";


    cout << "A shadowy figure blocks your way! Do you:\n";
    cout << "1. Fight the creature\n";
    cout << "2. Try to sneak past\n";

    choice = getChoice(1, 2);

    if (choice == 1) {
        cout << "You fight bravely but take some damage. (-20 Health)\n";
        health -= 20;
    } else {
        cout << "You successfully sneak past, avoiding a fight.\n";
    }

    cout << "Current Health: " << health << "\n\n";


    cout << "You find a glowing bottle. Do you drink it?\n";
    cout << "1. Yes (It could be a health potion)\n";
    cout << "2. No (It might be poisoned)\n";

    choice = getChoice(1, 2);

    switch (choice) {
        case 1:
            cout << "The potion restores 20 health!\n";
            health += 20;
            break;
        case 2: 
            cout << "You leave it alone and move forward.\n";
            break;
    }

    cout << "Current Health: " << health << "\n\n";

    
    if (health <= 0) {
        cout << "Your health dropped to 0. You collapse... GAME OVER.\n";
    } else {
        cout << "You see a door at the end of the corridor. You push it open... FREEDOM! You escaped the dungeon!\n";
    }

    return 0;
}