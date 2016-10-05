# Inheritence-

#include<iostream>

using namespace std;

class professional
{
	public:
	char sub[100], guide[100];
	
	void getdata1()
	{	
		cout<<"Enter the name of your project:"<<endl;
		cin>>sub;
		
		cout<<"Enter Project guide's name:"<<endl;
		cin>>guide;
	}

	void display1()
	{

		cout<<"PROJECT NAME:\t\t"<<sub<<endl;
		cout<<"PROJECT GUIDE:\t\t"<<guide<<endl;
	}
}r;

class academic
{
	public:
	int year, marks;
	
	void getdata2()
	{	
		cout<<"Enter the year:"<<endl;
		cin>>year;
		
		cout<<"Enter Total marks:"<<endl;
		cin>>marks;
	}

	void display2()
	{
		cout<<"YEAR:\t\t\t"<<year<<endl;
		cout<<"TOTAL MARKS:\t\t"<<marks<<endl;
	}
}a;

class personal:public professional, public academic
{
	public:
	char name[50];
	int rno;

	void getdata()
	{
		cout<<"Enter the name of the student:"<<endl;
		cin>>name;

		cout<<"Enter the roll number:"<<endl;
		cin>>rno;
		r.getdata1();
		a.getdata2();
	}

	void display()
	{
		cout<<"\nNAME:\t\t\t"<< name<<endl;
		cout<<"ROLL NO.:\t\t"<<rno<<endl;
		r.display1();
		a.display2();
	}
}p;

int main()
{
	int ch;
	class personal p;

	p.getdata();
	cout<<"STUDENT'S BIO-DATA:"<<endl;
	p.display();
	return 0;
}



