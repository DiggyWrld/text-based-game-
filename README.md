# text-based-game-#include<iostream>
#include<string>
using namespace std;

//function declarations
void shop();

//global variables
string inventory[10];

int main() {
	//local game variables 
	int room = 1;
	string input;

	cout << "you wake up to find yourself in a spooky mental warehouse. can you escape? Good luck!" << endl;

	do { //beginning of game loop---------------------
		switch (room) {
		case 1:
			cout << "You are in room 1. You can go north.";
			getline(cin,input);
			if (input.compare("pick up") == 0)
				inventory[0] = "AR";
			if (input == "N")
				room = 2;
			
			else
				cout << "sorry, not a option." << endl;
			break;
		case 2:
			cout << "You are in room 2. You can go South or West." << endl;
			cin >> input;
			if (input == "S")
				room = 1;
			if (input == "E")
				room = 3;
			if (input == "W")
				room = 4;
			else
				cout << "Sorry, not a option." << endl;
			break;
		case 3:
			cout << "you are in room 3. You can go East. " << endl;
			cin >> input;
			if (input == "E")
				room = 2;
			else
				cout << "Sorry, not a option." << endl;
		case 4 :
			cout << "You are in room 4. You can go  west. " << endl;
			cin >> input;
			if (input == "W")
				room = 2;
			if (input == "s")
				room = 5;
			else
				cout << "Sorry, not a option." << endl;
			break;
		case 5 :
			cout << "You are in room 5. You can go north fam." << endl;
			cin >> input;
			if (input == "N")
				room = 4;
			else
				cout << "Sorry, not a option";
				break;
		} //end switch 

	} while (input != "q"); //end game loop--------------
}//end of main 

//function definition
void shop() {
	string input; //local to shop 
	do {
		cout << "hi, welcome to my shop!" << endl;
		cout << "enter k for key,p for potion,l for lamp" << endl;
		cout << "q to quit" << endl;
		cin >> input;
		if (input == "s"
}
