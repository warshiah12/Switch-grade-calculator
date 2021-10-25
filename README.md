# Switch-grade-calculator
assigning grades based on marks using switch statement
#include<iostream>
using namespace std;
int main() {
	int marks;
	string firstname;   //declaring variable with datatype string
	string secondname;   //declaring variable with datatype string
	cout << "Enter the obtained marks: " << endl;     //enter the marks 
  cin >> marks;
	cout << "Enter your first name?\nThe first letter of your name should be an uppercase letter.\n" << endl;  //asks the user to enter their first name
	cin >> firstname;
	cout<<"\nEnter your second name?\nThe first letter of your name should be an uppercase letter.\n" << endl;  //asks the user to enter their second name
	cin >> secondname;   
	if (marks > 0 && marks <= 100) {   //if marks are within the range of 1 to 100 then the control will be transfered to switch statement
		switch (marks / 10)  //the marks entered by the user will be divided by 10 and the result will be from one of the follwing cases
		{
		case 10:
		case 9:
		case 8:
			cout << "\n"<<firstname << " " << secondname << " - Grade A " << endl;
			break;
		case 7:
			cout << firstname <<" "<< secondname << " - Grade B " << endl;
			break;
		case 6:
			cout << firstname <<" "<< secondname << " - Grade C " << endl;
			break;
		case 5:
			cout << firstname <<" "<< secondname << " - Grade D " << endl;
			break;
		case 4:
			cout << firstname <<" "<< secondname << " - Grade E " << endl;
			break;
		default:
			cout << firstname <<" "<< secondname << " - Grade F " << endl;
			break;
		}
	}
	else   //if marks are less than 1 or greater than 100 then else block of statements will be executed
	{
		cout << "Invalid Data entered! The marks should be within the range of 1-100" << endl;
	}
	return 0;
}
