# Sample Game:

```cpp
// RockPaper Sessior Game:

#include <iostream>
#include <ctime>  // Just to use the random function we use this header file.
using namespace std;

char getUserChoice();
char getComputerChoice();
void showChoice(char choice);
void choosewinner(char player, char computer);

int main() {
    char player;
    char computer;

    player = getUserChoice();
    cout << "your choice: " << "\n";
    showChoice(player);
    computer = getComputerChoice();
    cout << "Computer Choice: ";
    showChoice(computer);
    choosewinner(player, computer);

    return 0;
}

char getUserChoice(){
    string name;
    char player;

    do{
        cout << "******** Rock Paper Sessior Game *************"<<"\n";
        cout << "***************************************************\n";
        cout << "Welcome to the game! Enter your name to begin: ";
        getline(cin,name);
        cout << "Hello " << name << " Hope you are doing great! Welcome to the game.\n";
        cout << "Choose One of the Following\n";
        cout << "*******************************************************\n";
        cout << "'r' for rock\n";
        cout << "'p' for paper\n";
        cout << "'s' for scissors\n";
        cin >> player;

    }while(player != 'r' && player != 'p' && player != 's');
    return player;
 

}
char getComputerChoice(){

    srand(time(0));
    int num = rand() % 3 + 1;
    switch(num){
        case 1: return 'r';
        case 2: return 'p';
        case 3: return 's';
    }
    return 0;

}
void showChoice(char choice){

    switch(choice){
        case 'r': cout << "Rock\n";
        break;
        case 'p': cout << "Paper\n";
        break;
        case 's': cout << "sessiors";
        break;
        default: cout <<"Enter the right Character between ('r','p','s')";
    }

}
void choosewinner(char player, char computer){
    switch(player){
case 'r': if(computer == 'r'){
            cout << "It's a Tie\n";
        }
          else if(computer == 'p'){
            cout << "You loose\n";
        }
          else{
            cout << "User win!\n";
        }
         break;

case 'p': if(computer == 'r'){
        cout << "You Win\n";
    }
      else if(computer == 'p'){
        cout << "It's a Tie\n";
    }
      else{
        cout << "You Loose!\n";
    }
     break;

case 's': if(computer == 'r'){
    cout << "you Loose\n";
}
  else if(computer == 'p'){
    cout << "You won" << "\n";
}
  else{
    cout << "It's a Tie!"<< "\n";
}
 break;
}
}

```
