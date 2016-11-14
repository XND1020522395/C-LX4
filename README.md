# C-LX4#include "stdafx.h"
#include "iostream"
#include "stdio.h"

using namespace std;

class CStudent
{
public:
	void value()
	{
		cout << "请输入学号, 姓名, 性别, 年龄, 地址" << endl;
		cin >> num >> name >> sex;
	}
	void display()
	{
		cout << "num:" << num << endl;
		cout << "name:" << name << endl;
		cout << "sex:" << sex << endl;
	}
private:
	int num;
	char name[20];
	char sex[5];
};

class CStudent1 :  public CStudent
{
public:
	void value_1()
	{
		cin >> age >> addr;
	}
	void display_1()
	{
		cout << "age:" << age << endl;
		cout << "addr:" << addr << endl;
	}
private:
	int age;
	char addr[10];
};



int main()
{
	CStudent1 stud;
	stud.value();
	stud.value_1();
	stud.display();
	stud.display_1();
    return 0;
}
