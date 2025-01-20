# progrTPfinal
#include <iostream>
#include <conio2.h>
#include <windows.h>
using namespace std;

const int ancho=25;
const int alto=15;

void mapa()
 {
	HANDLE hConsole = GetStdHandle(STD_OUTPUT_HANDLE);
	SetConsoleTextAttribute(hConsole, FOREGROUND_BLUE);
	cout<<"teclas de movimiento: WASD"<<endl;
	cout<<"disparar con la tecla:ESPACIO"<<endl;
	cout<<"debes disparar a las X, cuidado con los asteroides!"<<endl;
	SetConsoleTextAttribute(hConsole, 7);
	
	for(int i=0; i<alto;i++)
	{
		for(int j=0;j<ancho;j++)
		{
			if(i==0||i==alto-1||j==0||j==ancho-1){
				cout<<"#";
			}
			else{
				cout<<" ";
			}
		}
		cout<<endl;
	}
}

int main()
{
	mapa();
	return 0;
}
