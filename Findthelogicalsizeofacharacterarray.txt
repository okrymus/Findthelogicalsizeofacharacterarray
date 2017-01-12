// The program will find the logical size of a character array(fifth version).  
// The logical size of a character array
// Programmer: Panupong Leenawarat
// Last modify: 11/3/15

#include <iostream>
using namespace std;

int main()
{
	const int SIZE = 80 ;
	int x;
	char myName[SIZE];
	//Title
	cout
		<< endl
		<< "\t              This project uses a for loop to          \n"
		<< "\t        find the logical size of a character array     \n"
		<< "\t                    By Lee. Panupong				       "
		<< endl ;

	while (true)
	{
		cout << endl << "What is your name? ";
		cin.getline(myName, SIZE);
		
		while (myName[0] == '\0')
		{
			cout << endl << "Please give your name again: ";
			cin.getline(myName, SIZE);
		}
		
		for (x = 0; myName[x] != '\0'; x++);

		cout << "The string length is " << x << "." << endl << endl;
		
		system("pause");
	}
}