#include <iostream>
#include <stdlib.h>
#include<windows.h>
using namespace std;
//Array for the board
char board[3][3] = {{'1','2','3'},{'4','5','6'},{'7','8','9'}};
//Variable Declaration
int choice;
int row,column;
char turn = 'X';
bool draw = false;

//Function to show the current status of the gaming board

void display_board(){

    //Rander Game Board LAYOUT

    cout<<"\t\t\t\t         PLAYER - 1 [X]\t PLAYER - 2 [O]\n\n";
    cout<<"\t\t\t\t\t\t     |     |     \n";
    cout<<"\t\t\t\t\t\t  "<<board[0][0]<<"  |  "<<board[0][1]<<"  |  "<<board[0][2]<<"\n";
    cout<<"\t\t\t\t\t\t_____|_____|_____\n";
    cout<<"\t\t\t\t\t\t     |     |     \n";
    cout<<"\t\t\t\t\t\t  "<<board[1][0]<<"  |  "<<board[1][1]<<"  |  "<<board[1][2]<<"\n";
    cout<<"\t\t\t\t\t\t_____|_____|_____\n";
    cout<<"\t\t\t\t\t\t     |     |     \n";
    cout<<"\t\t\t\t\t\t  "<<board[2][0]<<"  |  "<<board[2][1]<<"  |  "<<board[2][2]<<"\n";
    cout<<"\t\t\t\t\t\t     |     |     \n";
}

//Function to get the player input and update the board

void player_turn(){
	cout<<"\n\t\t\t\t         Enter Place Number:-";
    if(turn == 'X'){
        cout<<"\n\t\t\t\t         Player - 1 [X] turn : ";
    }
    else if(turn == 'O'){
        cout<<"\n\t\t\t\t         Player - 2 [O] turn : ";
    }
    //Taking input from user
    //updating the board according to choice and reassigning the turn Start

    cin>> choice;

    //switch case to get which row and column will be update

    switch(choice){
        case 1: row=0; column=0; break;
        case 2: row=0; column=1; break;
        case 3: row=0; column=2; break;
        case 4: row=1; column=0; break;
        case 5: row=1; column=1; break;
        case 6: row=1; column=2; break;
        case 7: row=2; column=0; break;
        case 8: row=2; column=1; break;
        case 9: row=2; column=2; break;
        default:
            cout<<"Invalid Move";
    }

    if(turn == 'X' && board[row][column] != 'X' && board[row][column] != 'O'){
        //updating the position for 'X' symbol if
        //it is not already occupied
        board[row][column] = 'X';
        turn = 'O';
    }else if(turn == 'O' && board[row][column] != 'X' && board[row][column] != 'O'){
        //updating the position for 'O' symbol if
        //it is not already occupied
        board[row][column] = 'O';
        turn = 'X';
    }else {
        //if input position already filled
        cout<<"Box already filled!\n Please choose another!!\n\n";
        player_turn();
    }
    /* Ends */
    
}

//Function to get the game status e.g. GAME WON, GAME DRAW GAME IN CONTINUE MODE

bool gameover(){
    //checking the win for Simple Rows and Simple Column
    for(int i=0; i<3; i++)
    if(board[i][0] == board[i][1] && board[i][0] == board[i][2] || board[0][i] == board[1][i] && board[0][i] == board[2][i])
    return false;

    //checking the win for both diagonal

    if(board[0][0] == board[1][1] && board[0][0] == board[2][2] || board[0][2] == board[1][1] && board[0][2] == board[2][0])
    return false;

    //Checking the game is in continue mode or not
    for(int i=0; i<3; i++)
    for(int j=0; j<3; j++)
    if(board[i][j] != 'X' && board[i][j] != 'O')
    return true;

    //Checking the if game already draw
    draw = true;
    return false;
}

//Program Main Method
void intro()

{

    cout << "\n\n\n";
    Sleep(300);
    cout << "\t\t\t\t\t * * *  **** *      ****  ***   ***   ****   " << endl;
    Sleep(300);
    cout << "\t\t\t\t\t * * * *     *     *     *   * * * * *        "<< endl;
    Sleep(300);
    cout << "\t\t\t\t\t * * * ***** *     *     *   * * * * *****    " << endl;
    Sleep(300);
    cout << "\t\t\t\t\t * * * *     *     *     *   * * * * *         " << endl;
    Sleep(300);
    cout << "\t\t\t\t\t  ***   **** *****  ****  ***  * * *  ****     " << endl;
    Sleep(300);
    cout<<endl;
    cout<<"\t\t\t\t\t============================================"<<endl;
    Sleep(500);
    cout<<"\t\t\t\t\t    T I C K -- T A C -- T O E -- G A M E"<<endl;
    Sleep(500);
    cout<<"\t\t\t\t\t============================================"<<endl;
    Sleep(500);
    cout<<"\t\t\t\t\t\t\tFOR 2 PLAYERS\n";
    Sleep(500);
    cout<<"\t\t\t\t\t============================================"<<endl;
    Sleep(500);
    cout<<"press any key to continue...";
    cin.ignore();
    cin.get();
}

int main()
{

	system("color e");
	intro();
    system("cls");
    while(gameover()){
    	system("color b");
        display_board();
        player_turn();
        system("cls");
        Sleep(200);
        gameover();
    }
    system("color c");
    
    
    if(turn == 'X' && draw == false){
   	cout << "\n\n\n";
    Sleep(300);
    cout << "\t\t\t\t\t      ****  **    *  ****     " << endl;
    Sleep(300);
    cout << "\t\t\t\t\t     *      * *   *  *    *   "<< endl;
    Sleep(300);
    cout << "\t\t\t\t\t     *****  *  *  *  *     *  " << endl;
    Sleep(300);
    cout << "\t\t\t\t\t     *      *   * *  *    *   " << endl;
    Sleep(300);
    cout << "\t\t\t\t\t      ****  *    **  ****     " << endl;
    Sleep(300);
    cout<<endl;
    cout<<"\t\t\t\t\t================================"<<endl;
    Sleep(500);
    cout<<"\t\t\t\t\t       G A M E--O V E R"<<endl;
    Sleep(500);
    cout<<"\t\t\t\t\t================================"<<endl;
    Sleep(500);
    cout<<"\t\t\t\t\t       PLAYER 1[O] WON!\n";
    Sleep(500);
    cout<<"\t\t\t\t\t================================"<<endl;
       
       
    }
    else if(turn == 'O' && draw == false){
          	cout << "\n\n\n";
    Sleep(300);
    cout << "\t\t\t\t\t      ****  **    *  ****     " << endl;
    Sleep(300);
    cout << "\t\t\t\t\t     *      * *   *  *    *   "<< endl;
    Sleep(300);
    cout << "\t\t\t\t\t     *****  *  *  *  *     *  " << endl;
    Sleep(300);
    cout << "\t\t\t\t\t     *      *   * *  *    *   " << endl;
    Sleep(300);
    cout << "\t\t\t\t\t      ****  *    **  ****     " << endl;
    Sleep(300);
    cout<<endl;
    cout<<"\t\t\t\t\t================================"<<endl;
    Sleep(500);
    cout<<"\t\t\t\t\t       G A M E--O V E R"<<endl;
    Sleep(500);
    cout<<"\t\t\t\t\t================================"<<endl;
    Sleep(500);
    cout<<"\t\t\t\t\t       PLAYER 2[X] WON!\n";
    Sleep(500);
    cout<<"\t\t\t\t\t================================"<<endl;
       
    }
    else
    	cout << "\n\n\n";
    Sleep(300);
    cout << "\t\t\t\t\t      ****  **    *  ****     " << endl;
    Sleep(300);
    cout << "\t\t\t\t\t     *      * *   *  *    *   "<< endl;
    Sleep(300);
    cout << "\t\t\t\t\t     *****  *  *  *  *     *  " << endl;
    Sleep(300);
    cout << "\t\t\t\t\t     *      *   * *  *    *   " << endl;
    Sleep(300);
    cout << "\t\t\t\t\t      ****  *    **  ****     " << endl;
    Sleep(300);
    cout<<endl;
    cout<<"\t\t\t\t\t================================"<<endl;
    Sleep(500);
    cout<<"\t\t\t\t\t       G A M E--O V E R"<<endl;
    Sleep(500);
    cout<<"\t\t\t\t\t================================"<<endl;
    Sleep(500);
    cout<<"\t\t\t\t\t            D R A W\n";
    Sleep(500);
    cout<<"\t\t\t\t\t================================"<<endl;
       
} 
