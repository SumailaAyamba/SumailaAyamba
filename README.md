### Hi there 👋

<!--
**SumailaAyamba/SumailaAyamba** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on Python projects
- 🌱 I’m currently working on C++ projects  ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me:sumailaayamba14@gmail.com
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->



// DemoW.cpp : This file contains the 'main' function. Program execution begins and ends there.
//

#include <iostream>
#include<list>
#include<stack>
#include<vector>
#include<process.h>
using namespace std;

//void printReated(int arr[])
//{
//
//
//	int size = sizeof(arr);
//
//	for (int i = 0; i < size; i++)
//	{
//
//		for(int j=i+1; j<size; j++)
//
//			if (arr[i] == arr[j])
//			{
//				cout << "Duplicate element: " << arr[i];
//
//			}
//
//	
//	}
//}
//

//
//
//int getMax(int arr[])
//{
//	int size = sizeof(arr);
//
//	int max = arr[0], count = 1, maxCount = 1;
//
//	for (int i = 0; i < size; i++)
//	{
//		count = 1;
//		for (int j = i + 1; j < size; j++)
//		{
//			if (arr[i] == arr[j])
//			{
//				count++;
//
//			}
//
//			if (count > maxCount)
//			{
//				max = arr[i];
//				maxCount = count;
//			}
//		}
//		return max;
//	}
//
//
//}


//bool findPair(int arr, int value)
//{
//	int size = sizeof(arr);
//
//	for (int i = 0; i < size; i++)
//	{
//		for (int j = 0; j < i + 1; j++)
//		{
//			if (arr[i] + arr[j] == value)
//			{
//				cout << "The pairs is: " << arr[i] << " " << arr[j] << endl;
//			}
//		}
//	}
//}

//
//
//class Demo_sum {
//private:
//	int num;
//	static int count;
//
//public:
//	void input()
//	{
//		cout << "Enter the number for : " << "Object" << ++count << endl;
//		cin >> num;
//
//	}
//	
//	void operator +(Demo_sum temp)
//	{
//		int x;
//		x = num + temp.num;
//
//		cout << "Sum of two is " << x << endl;
//
//	}
//	void show()
//	{
//		cout << "The num is " << num << endl;
//
//	}
//
//};
//
//int Demo_sum::count;



//
//
//class First
//{
//	int fx;
//public:
//	void input(int x)
//	{
//		fx = x;
//	}
//	friend void findMax(First, second);
//
//};
//
//class Second {
//	int sx;
//public:
//	void inputs(int x)
//	{
//		sx = x;
//	}
//
//	friend void findMax(First, Second);
//};
//
//void findMax(First A, Second B)
//{
//	if (A.fx > B.sx)
//	{
//
//	}
//}



struct Node
{
	int data;
	Node* next;


};

class Link_list
{
private:
	Node* start;

public:
	Link_list()
	{
		start = NULL;

	}

	void add_data(int i)
	{
		Node* new_link = new Node;
		new_link->data = i;
		new_link->next = start;
		start = new_link;

	}
	


	void create(int i)
	{
		Node* new_node = new Node;

		new_node->data = i;
		new_node->next = start;

		start = new_node;

	}
	void display(int);
	void insert(int, int);


};

void Link_list::display(int delete_node)

{
	Node* move = start;
	Node* temp;
	while (move)
	{
		cout << move->data << "->";
		temp = move;
		move = move->next;

		if (delete_node)
		{
			delete(temp);
		}

	}

	cout << "NULL\n";

}

void Link_list::insert(int position, int data)
{
	Node* move = start;
	int steps = 1;
	while (steps < position - 1)
	{
		move = move->next;
		steps++;


	}

	Node* new_node = new Node;
	new_node->data = data;
	if (position == 1)
	{
		new_node->next = start;
		start = new_node;
	}

	else
	{
		new_node->next = move->next;
		move->next = new_node;
	}
}
int main()
{
	//("clrs");


	int value, data, choice, position, total = 0;

	Link_list link;
	cout << "Enter the elements of the linked list terminated by negative number:\n: " 
		<< endl;

	cin >> value;

	do
	{
		link.create(value);
		total++;
		cin >> value;


	} while (value >=0);


	cout << "\n\nThe list before any operation is performed(LIFO):\n\n";

	int i;
		//link.add_data(i);
		link.display(0);

		cout << "\n\nTotal node :=" << endl;
		cout << "\n\nEnter the position where node is to be inserted:";
		cin >> position;

		if (position <= 0 || position > total + 1)
		{
			cout << "\nWrong position inputted\n";
			exit(1);


		}

		cout << "\n\nEnter the value of the node to be inserted : = ";

		cin >> data;
		link.insert(position, data);

		cout << "\nThe list after insertion is : \n";
		link.display(1);




	

}


