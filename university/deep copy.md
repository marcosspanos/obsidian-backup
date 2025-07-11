# what it does:
deep copy allows us to create a new object which copies all the data of the variables and also allocates similar memory resources with the same value to the object 
In order to perform Deep copy we need to explicitly define the copy constructor and assign dynamic memory
it is required to dynamically allocate memory to the variables in the other constructors as well??
![[Pasted image 20241209104313.png]]
```c++
// C++ program to implement the
// deep copy
#include <iostream>
using namespace std;

// Box Class
class box {
private:
    int length;
    int* breadth;
    int height;

public:
    // Constructor
    box()
    {
        breadth = new int;
    }

    // Function to set the dimensions
    // of the Box
    void set_dimension(int len, int brea,
                       int heig)
    {
        length = len;
        *breadth = brea;
        height = heig;
    }

    // Function to show the dimensions
    // of the Box
    void show_data()
    {
        cout << " Length = " << length
             << "\n Breadth = " << *breadth
             << "\n Height = " << height
             << endl;
    }

    // Parameterized Constructors for
    // for implementing deep copy
    box(box& sample)
    {
        length = sample.length;
        breadth = new int;
        *breadth = *(sample.breadth);
        height = sample.height;
    }

    // Destructors
    ~box()
    {
        delete breadth;
    }
};

// Driver Code
int main()
{
    // Object of class first
    box first;

    // Set the dimensions
    first.set_dimension(12, 14, 16);

    // Display the dimensions
    first.show_data();

    // When the data will be copied then
    // all the resources will also get
    // allocated to the new object
    box second = first;

    // Display the dimensions
    second.show_data();

    return 0;
}
```

## differences between deep and shallow copy 
![[Pasted image 20241209104445.png]]
these are the important differences when considering deep and shallow copy and what to choose 

**resources:**
	https://www.geeksforgeeks.org/shallow-copy-and-deep-copy-in-c/

