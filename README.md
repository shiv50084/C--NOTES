# C++ programs      

[Click here to download PDF!](https://github.com/abdullahfarwees/) 

### Table of contents



[TOC]



## Standard Template Library - STL
####VECTOR 

	#include <iostream> 
	#include <vector> 
	
	using namespace std; 

	int main() 
	{ 
	vector<int> v1 {10,20,30,40}; 

	v1.push_back(1);  //insert 1 at the back of v1 
	v1.push_back(2);  //insert 2 at the back of v1 
	v1.push_back(4);  //insert 3 at the back of v1 

	v1.pop_back();  

	vector<int>::iterator it; 

		for(it = v1.begin(); it != v1.end(); it++) 
		{ 
			cout << *it <<" ";   // for printing the vector 
		} 
	} 

vector_name.size() returns size of the vector.
vector_name.front() retuns the element at the front of the vector (i.e. leftmost element). 
vector_name.back() returns the element at the back of the vector (i.e. rightmost element). 

size()
empty()
push_back()
pop_back()
end()
begin()
front()
back()


copy array to vector 

int myints[] = {1,2,3,4,5,4,3,2,1}; 
std::vector<int> v(myints,myints+9);  


> **Note:**

>- comman way to use find() in containers 

> bool status = container.find(element) != container.end();

####STACK 

	#include <iostream>      
	#include <stack> 
	
	using namespace std;  
      
	int main () 
	{ 
	stack<int> s; 

	// pushing elements into stack 
	s.push(2);   
	s.push(3);   
	s.push(4);   
 
	cout << s.top();   // prints 4, as 4 is the topmost element 

	cout << s.size();  // prints 3, as there are 3 elements in 
	} 

Frequently used functions : 
push()
pop()
size()
empty()
top()



####QUEUE 

	#include <iostream>      
	#include <queue> 
	
	using namespace std;   
	     
	int main () 
	{ 
	queue <int> q;   // creates an empty queue of integer q 

	q.push>(2);   // pushes 2 in the queue  , now front = back = 2 
	q.push(3);     // pushes 3 in the queue  , now front = 2 , and back = 3 

	q.pop() ;  // removes 2 from the stack , front = 3 
	} 

front() returns the front element of the queue whereas back() returns the element at the back of the queue. 

frequently used functions
front(),
back(),
empty(),
size(),
push(),
pop(),
push_back()*,
pop_front()*


####SETS

Sets are containers that store unique elements following a specific order. 

Sets values cannot modifed but insert and remove operations can be done. 

	#include <iostream> 
	#include <set> 

	int main () 
	{ 
	
	std::set<std::string> s; 
	std::cout << "Adding 'Hello' and 'World' to the set twice" << std::endl; 
	
	s.insert("Hello"); 
	s.insert("World"); 
	s.insert("Hello"); 
	s.insert("World"); 

	std::cout << "Set contains:"; 
	while (!s.empty()) 
	{ 
		std::cout << ' ' << *s.begin(); 
		s.erase(s.begin()); 
	} 
   
	  return 0; 
	}


Sample program 2


	#include<bits/stdc++.h> 
	
	using namespace std; 
	
	int main() 
	{ 
	set<int> s; 
	
	for(int i=0;i<10;i++) 
		s.insert(i); 

	int x; 
	cin >> x; 
	
	bool status = s.find(x) != s.end(); 
	if(status) 
		cout << "present"; 
	else 
		cout << "Not present";	 
	cout<<endl; 
	
	s.insert(x); 
	
	status = s.find(x) != s.end(); 
	if(status) 
		cout << "present"; 
	else 
		cout << "Not present";	 
	cout<<endl; 
	
	while( !s.empty() ) 
	{ 
		cout << *s.begin() << endl; 
		s.erase( s.begin() ); 
	} 

	return 0; 
	}

frequently used functions
size(),
insert(),
begin(),
end(),
find(),
erase().



####LIST [ DOUBLY LINKED LIST ]


	#include <iostream> 
	#include <list> 
	
	int main () 
	{ 
	int myints[] = {75,23,65,42,13}; 
	  std::list<int> mylist (myints,myints+5); 

	  std::cout << "mylist contains:"; 
  
		for (std::list<int>::iterator it=mylist.begin(); it != mylist.end(); ++it) 
 	   	std::cout << ' ' << *it; 

 	 std::cout << '\n'; 

	  return 0; 
	} 

some more functions :

list::empty() ,
list::end() ,
list::begin() , 
list::front() ,
list::back() ,
list::insert() , 
list::size() ,
list::reverse() ,
list::sort() ,
list::swap() ,
list::pop_back() ,
list::pop_front().


####FORWARD_LIST [ SINGLY LINKEDLIST ]

	// forward_list::begin example 

	#include <iostream> 
	#include <forward_list> 
	
	int main () 
	{ 
	  std::forward_list<int> mylist = { 34, 77, 16, 2 }; 

	  std::cout << "mylist contains:"; 
  	
		for ( auto it = mylist.begin(); it != mylist.end(); ++it ) // note : auto keyword used here 
	  	std::cout << ' ' << *it; 

	  std::cout << '\n'; 

	  return 0; 
	} 

some more functions :

empty() ,
end() ,
begin() ,
push_front() ,
pop_front() ,
reverse() ,
swap() ,
sort() ,


####PAIR 

The pair container is a rather basic container. It can be used to store two elements, called first and second, and that's about it. 



	#include<bits/stdc++.h> 

	using namespace std; 

	int main() 
	{ 
	pair<int,string> pr; 

	pr = make_pair(1,"fayas"); 
	pr = make_pair(2,"shamshad"); 
	pr = make_pair(3,"majeed"); 
	 
	cout << pr.first << " " << pr.second << endl; 

	return 0; 
	}

sample program 2

 
 	#include<bits/stdc++.h> 

	typedef std::pair<int,char[100]> intPair; 
	typedef std::vector<intPair> vectorPairs; 

	int main() 
	{ 
	    int numEntries; 
	    std::cin >> numEntries; 

	    vectorPairs pairs(numEntries); 

	    for(vectorPairs::iterator itor = pairs.begin(); itor != pairs.end(); ++itor) 
	    { 
 	       std::cin >> itor->first >> itor->second; 
	    } 

 	   for(vectorPairs::iterator itor = 	pairs.begin(); itor != pairs.end(); ++itor) 
	    { 
	        std::cout << itor->first << " " << itor->second << std::endl; 
 	   } 

	    return 0; 
	} 

Some more function : 
make_pair() ,
move(),
begin(),
end().






####BINARY_SEARCH 

Returns true if any element in the range [first,last] is equivalent to val, and false otherwise. 

> **Note:** : it must be a sorted array. 

	std::cout << "looking for a 3... "; 
	if (std::binary_search (v.begin(), v.end(), 3)) 
	std::cout << "found!\n"; else std::cout << "not found.\n"; 

	std::cout << "looking for a 6... "; 
	if (std::binary_search (v.begin(), v.end(), 6, myfunction)) 
	std::cout << "found!\n"; else std::cout << "not found.\n";
	
	
#### TEMPLATE

	#include<bits/stdc++.h> 
	using namespace std; 

	template <class T> // keyword -> template //  T variable accepts any type 
	T MaxFun(T a, T b) 
	{ 
		return (a>b ? a:b); 
	} 
	
	int main() 
	{ 
	int x = 10; 
	int y = 133; 

	cout<<MaxFun(x,y)<<endl<<endl; 

	return 0; 
	}
	

####SORT array

	#include<bits/stdc++.h> 

	using namespace std; 

	int main() 
	{ 
		int arr[] = {3,2,1,6,5,4,9,8,7,6}; 
	
		for(int i=0;i<10; i++)cout<<arr[i] << " " ; 

		cout << endl; 

		sort(arr,arr+10); 
		for(int i=0;i<10;i++)cout<< arr[i] << " "; 

	return 0; 
	}		


####SORT  vector

Sorts the elements in the range [first,last] into ascending order. 
sort(arr,arr+size); 

sort(vec.begin(),vec.end()); 

> **Note:**
to sort in ASC/DESC and print vector : 

	sample vector : vector<int> vec = {1,2,3,4,5}; 

	for(vector<int>::iterator i = 0; i != vec.end(); i++)cout << vec[i]; 

	/* sort in ASC order - default */
	std::sort(arr,arr+n) ; 

	/* sort in DESC order */ 
	std::sort(arr,arr+n,std::greater<int>()) ; 

-

	#include <bits/stdc++.h> 
	using namespace std; 
	
	int main() 
	{ 
	
	int n; 
	cin >> n; 

	int arr[n]; 

	for(int i=0;i<n;i++)cin>>arr[i]; 
 
	/* sort in ASC order - default */
	std::sort(arr,arr+n); 
	
	for(int i=0;i<n;i++)cout << arr[i] <<" " ; 

	cout << endl << endl; 

	/* sort in DESC order */ 
		std::sort(arr,arr+n,std::greater<int>()); 

	for(int i=0;i<n;i++)cout << arr[i] <<" " ; 

	return 0; 
	}

/* 

this program helps to sort the struct containers by calling the 3rd parameter in stl::sort() 
functions. 

Also this program demostrates the sorting by modifying the calling functions. (i.e ASC / DESC order) 

*/ 


	#include <iostream> 
	#include <algorithm> 
	#include <vector> 
	#include <string> 

	using namespace std; 

	struct Person 
	{ 
	    string name; 
	    int age; 
	    string favoriteColor; 
	}; 

	bool sortByName(const Person &lhs, const Person &rhs) { return lhs.name < rhs.name; } 
	bool sortByAge(const Person &lhs, const Person &rhs) { return lhs.age < rhs.age; } 
	bool sortByColor(const Person &lhs, const Person &rhs) { return lhs.favoriteColor < rhs.favoriteColor; } 

	const unsigned numberOfPeople = 2; 
 
	int main() 
	{ 
	    vector<Person> people(numberOfPeople); 

	    for (vector<Person>::size_type i = 0; i != numberOfPeople; ++i) 
	    { 
	        cout << "Person #" << i + 1 << " name: "; 
	        cin >> people[i].name; 

	        cout << "Person #" << i + 1 << " age: "; 
	        cin >> people[i].age; 

	        cout << "Person #" << i + 1 << " favorite color: "; 
	        cin >> people[i].favoriteColor; 
 	   } 

    	cout << "\n\n"; 

 	   // Sort by name 
	    sort(people.begin(), people.end(), sortByName); 
	    for (Person &n : people) 
	        cout << n.name << " "; 

	    cout << endl; 

	    // Sory by age 
	    sort(people.begin(), people.end(), sortByAge); 
	    for (Person &n : people) 
	        cout << n.age << " "; 

	    cout << endl; 

	    // Sort by color 
	    sort(people.begin(), people.end(), sortByColor); 
	    for (Person &n : people) 
	        cout << n.favoriteColor << " "; 

	    return 0; 
	} 




####NEXT_PERMUTATION 

	std::string moves = "xxxxxoooo"; 
	sort(begin(moves), end(moves)); 

	while (std::next_permutation(begin(moves), end(moves))) 
	{ 
	    std::cout << moves << std::endl; 
	}


####GCD 

The libstdc++ algorithm library has a hidden gcd function (I'm using g++ 4.6.3). 

	#include <iostream> 
	#include <algorithm> 

	using namespace std; 

	int main() 
	{ 
	  cout << std::__gcd(100,24); 
	  return 0; 
	}

####POW / POWL 
 
 	std::pow(2,10);


####SWAP 

	std::swap(x,y);

####REVERSE 

	std::reverse(myvector.begin(),myvector.end());

####MIN / MAX 

 	 std::cout << std::min(2,1) << '\n'; 
	  std::cout << std::min('a','z') << '\n'; 
	  std::cout << std::min(3.14,2.72) << '\n';








####MEMSET 

Fill block of memory 
Sets the first num bytes of the block of memory 

	#include <stdio.h> 
	#include <string.h> 

	int main () 
	{ 
	  char str[] = "almost every programmer should know memset!"; 
	  memset (str,'_',6); 
	  puts (str); 
	  return 0; 
	} 

Input :

almost every programmer should know memset!

Output: 

______ every programmer should know memset!



####Dynamic Binding 

Linking a procedure call to the code that will be executed only at a run time.


	#include<bits/stdc++.h> 

	using namespace std; 

	int square(int sq) 
	{ 
		return sq*sq; 
	} 

	int cube(int cb) 
	{ 
		return cb*cb*cb; 
	} 

	int main() 
	{ 

	int ch; 
	int x = 5; 

	cout << "Enter 0 - square , 1 - cube : " << endl; 
	cin >> ch; 

	int (*ptr)(int); 

	if( ch == 0 ) 
	{ 
		ptr = square; 
	} 
	else if(ch == 1) 
	{ 
		ptr = cube; 
	} 


	cout << ptr(x) << endl; 
	
	return 0; 
	}


Output :

Enter 0 - square , 1 - cube : 
0 
25



####Simple Inheritance 

	#include<bits/stdc++.h> 

	using namespace std; 

	class Value 
	{ 

	private : 

	protected : 
	int x; 

	public : 

	void setX(int val) 
	{ 
		x = val; 
	} 

	}; 

	class SqValue : public Value 
	{ 

	private : 
	
	public : 
	
	void show() 
	{ 
		cout << "--- > " << x*x << endl; 
	} 
	
	}; 
	

	int main() 
	{ 
	
	SqValue s; 
	s.setX(5); 
	s.show(); 
	
	return 0; 
	}

Output : 

--- > 25


####Virtual Function ;

Virtual keyword is used in superclass to call the sub class member functions.

/*
Reqd :
inheritance and virtual keyword
*/

	#include<bits/stdc++.h> 
	using namespace std; 

	class SuperClass 
	{ 
	private: 
	public: 
	virtual void area() 
	{ 
		cout << "SuperClass area function" << endl; 
	} 
	}; 

	class SubClass:public SuperClass 
	{ 
	private : 
	public : 
	virtual void area() 
	{ 
		cout << "SubClass area function " << endl; 
	} 

	}; 

	int main() 
	{ 
	SuperClass *SCptr; 
	SubClass objSubClass; 

	SCptr = &objSubClass; 
	SCptr -> area(); 
	
	return 0; 
	}

Output : 
SubClass area function

/* if we remove “virtual” keyword  then output will be :

SuperClass area() function

 */


####Encapsulation ( also known as Data Abstraction )

Method of combining the data and function inside the class. Hides data from being accessed outside the class directly. Two types : Data abstraction , Function Abstraction – It is used without showing how it is implemented.

	#include<bits/stdc++.h> 

	using namespace std; 

	class Sample 
	{ 

	private: 

	int var; 

	public: 

	int addition(int a,int b) 
	{ 
		var = a+b; 
	} 

	void show() 
	{ 
		cout << var << endl; 
	} 
	
	}; 
	
	int main() 
	{ 
	
	Sample s; 

	s.addition(4,6); 
	s.show(); 
	
	return 0; 
	}


####Copy constructor

To “reproduce” a identical copy of an original existing object 

	#include<bits/stdc++.h> 

	using namespace std; 

	class Sample 
	{ 
	private: 

	int varA, varB; 

	public: 

	void setValues(int a,int b) 
	{ 
		varA = a; 
		varB = b; 
	} 

	void show() 
	{ 
		cout << varA << "  "<< varB << endl; 
	} 

	}; 

	int main() 
	{ 

	Sample One , Two; 

	One.setValues(2,3); 

	/* copy values from object One to Two */ 
	Two = One; 

	Two.show(); 
	
	return 0; 
	}


####Function overloading 


	class Sample 
	{ 
	private: 
	public: 
	/* function with no parameters */ 
	void show() 
	{ 
		cout << "show I/O" << endl; 
	} 

	/* function with integer parameters */ 
	void show(int i) 
	{ 
		cout << i << endl; 
	} 

	/* function with float parameters */ 
	void show(double f) 
	{ 
		cout << f << endl; 
	} 

	/* function with character parameters */ 
	void show(char *c) 
	{ 
		cout << c << endl; 
	} 
	}; 

	int main() 
	{ 
	Sample s; 
	
	s.show(); 
	s.show(123); 
	s.show(333.33); 
	s.show("zaza"); 

	return 0; 
	}

Output 

display show I/O 

123 

333.33 

zaza 


####Operator overloading

programmer can use operator with user-defined as well. 

	#include <bits/stdc++.h>

	using namespace std;

	class Sample
	{
	private :

	int x,y;

	public :

	void setXY(int a, int b)
	{
		x = a;
		y = b;
	}
	
	void show()
	{
		cout << x << " " << y <<endl;
	}

	/* add two objects */
	Sample operator + (const Sample &s)
	{
	
	Sample obj;
	
	obj.x = this->x + s.x;
	obj.y = this->y + s.y;
	
	return obj;
	}

	};

	int main()
	{
	
	Sample s1, s2;
	s1.setXY(2,2);
	s2.setXY(3,3);

	Sample s3 = s1+s2;
	s3.show();
	
	return 0;
	}

Output :
5  5


####Interfaces : 

Interface descrobes the capability of a class without implementation of class. A class is made abstract by declaring atleast one function is pure virtual function. (Placing “=0” in virtual function )
Abstract class provide a base class in which other class can inherit It cannot be used for instantiate for objects.

	class Shape
	{
	
	protected: // protected

	int x,y;

	public:

	/* PURE VIRTUAL FUNCTION PROVIDE INTERFACE FRAMEWORK  *
	virtual int getArea() = 0;

	void setXY(int a, int b)
	{
		x = a;
		y = b;
	}

	};

	class Rectangle : public Shape
	{

	private:

	public:
	int getArea()
	{
		return x*y;
	}

	};

	class Triangle : public Shape
	{

	private:

	public:

	int getArea()
	{
		return 0.5*x*y;
	}

	};

	int main()
	{
	Triangle t;
	Rectangle r;

	t.setXY(5,5);
	r.setXY(5,5);

	cout << "Triangle area :" << t.getArea() << endl;
	cout << "Rectangle area : " << r.getArea() << endl;

	return 0;
	}
	
	
### Simple Call back function  

/*

Callback is a function that we pass to another APIs as argument while calling them. Now these APIs are expected to use our provided callback at some point.

Callbacks in C++ can be of 3 types,

1.) Function Pointer
2.) Function Objects / Functors
3.) Lambda functions

*/

	//This encrypt function decrement all letters in string by 1.
	std::string encryptDataByLetterDec(std::string data)
	{
	for(int i = 0; i < data.size(); i++)
	{
	if( (data[i] >= 'a' && data[i] <= 'z' ) || (data[i] >= 'A' && data[i] <= 'Z' ) )
	data[i]--;
	}
	return data;
	}


	//This encrypt function increment all letters in string by 1.
	std::string encryptDataByLetterInc(std::string data)
	{
	for(int i = 0; i < data.size(); i++)
	{
	if( (data[i] >= 'a' && data[i] <= 'z' ) || (data[i] >= 'A' && data[i] <= 'Z' ) )
	data[i]++;
	}
	return data;
	}

	std::string buildCompleteMessage(std::string rawData, std::string (* encrypterFunPtr)(std::string) )
	{
	// Add some header and footer to data to make it complete message
	rawData = "[HEADER]" + rawData + "[FooTER]";

	// Call the callBack provided i.e. function pointer to encrypt the
	rawData = encrypterFunPtr(rawData);

	return rawData;
	}

	int main()
	{
	std::string msg = buildCompleteMessage("SampleString", &encryptDataByLetterInc);
	std::cout<<msg<<std::endl;    
	msg = buildCompleteMessage("SampleString", &encryptDataByLetterDec);
	std::cout<<msg<<std::endl;

	return 0;
	}		


minheap and maxheap implementation using cpp STL
 - https://www.geeksforgeeks.org/implement-min-heap-using-stl/
