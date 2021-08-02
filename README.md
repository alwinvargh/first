# first
#include<iostream>
using namespace std;
class stack
{
public :	int top,i,d;
	int a[10];
	stack()
	{
		top=-1;
	}
	void push (int x)
		{
			if(top>=10)
			{
				cout<<"Stack Overflow";
			}	
			else
			{
				top++;		
				a[top]=x;
				cout<<"Element Inserted \n";
			}
		}
	int pop()
		{
			if(top<0)
			{
				cout<<"Stack Underflow\n";
				return 0;
			}
			else
			{
				 d=a[top--];
				return d;
			}
		}
	void isempty()
		{
			if(top<0)
			{
				cout<<"Stack is empty\n";
			}
			else
			{
				cout<<"Stack is not empty";
			}
		}
	void printstack()
	{
	
		for(i=top;i>=0;--i)
		{
			cout<<a[i]<<endl;
		}
	}
	
};
int main()
{
	int n,e;
	stack s;
	while(1)
	{
	cout<<"ENTER YOUR CHOICE : ";
	cout<<endl<<"1.PUSH (INSERTION)"<<endl;
	cout<<"2.POP (DELETION)"<<endl;
	cout<<"3.isempty"<<endl;
	cin>>n;
	//=new stack();
	switch(n)
	{
		case 1:cout<<"ENTER ELEMENT ";
			cin>>e;
			s.push(e);
			s.printstack();
			break;
		case 2:s.pop();
			//cout<<"ELEMENT IS DELETED"<<endl;
			s.printstack();
			break;
		case 3:s.isempty();
			break;
	default: cout<<"INvalid choice"<<endl;
	}
	}
	return 0;
}
          /*                           OUTPUT
                                     ---------
ENTER YOUR CHOICE : 
1.PUSH (INSERTION)
2.POP (DELETION)
3.isempty
1
ENTER ELEMENT 25
Element Inserted 
25
ENTER YOUR CHOICE : 
1.PUSH (INSERTION)
2.POP (DELETION)
3.isempty
1
ENTER ELEMENT 33
Element Inserted 
33
25
ENTER YOUR CHOICE : 
1.PUSH (INSERTION)
2.POP (DELETION)
3.isempty
1
ENTER ELEMENT 26
Element Inserted 
26
33
25
ENTER YOUR CHOICE : 
1.PUSH (INSERTION)
2.POP (DELETION)
3.isempty
2
33
25
ENTER YOUR CHOICE : 
1.PUSH (INSERTION)
2.POP (DELETION)
3.isempty
3
Stack is not empty

ENTER YOUR CHOICE : 
1.PUSH (INSERTION)
2.POP (DELETION)
3.isempty
2
25
ENTER YOUR CHOICE : 
1.PUSH (INSERTION)
2.POP (DELETION)
3.isempty
3
Stack is empty
ENTER YOUR CHOICE : 
1.PUSH (INSERTION)
2.POP (DELETION)
3.isempty


*/
