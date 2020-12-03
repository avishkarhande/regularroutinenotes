# Regular Routine Notes (DSA,CLASS,CP)
DAY 1 (2/12/2020)
---
DSA
---
|Array | LinkedList |
|------|------------|
|1.Fixed Size|1.No Fixed Size|
|2.Accessing Element in O(1)|2. Accessing Element in O(n)|
|3.Traversing can be done in any order from any element |3. Traversal Possible only through head|
|4.Inserting an element takes O(n) in worst case|4.Inserting element takes O(1) but needs traversing so O(n)overall|
|5. Point 4 applicable for deleting as well|5. Point 4 for deleting as well|
---
OOP CLASS
---
  Exception Handling
```cpp
int main(){
  int a,b;
  cin>>a>>b;
  try{
    if(b!=0){
      cout<<a/b<<endl;
    }else{
      throw(b);
    }
  }
  catch(int b){
    cout<<"b cannot be "<<0<<endl;
  }
}
```
---
* All excpetions can be caught using "Catch all exception"
  * Syntax
    ```cpp
    catch(...){
    cout<<"Caught an exception"<<endl;
    }
    ```
  * Type of exception cannot be specified using catch all.
* Rethrowing Exception
  ```cpp
  void divide(double x,double y){
    try{
      if(y==0){
        throw y;
      }else{
        cout<<"DIVISION"<<endl;
      }
    }
    catch(double){
      cout<<"Excpetion inside function";
      throw;
    }
  }
  int main(){
    try{
      divide(10.5,2.0);
      divide(20.0,0.0);
    }
    catch(double){
      cout<<"Exception inside main"<<endl;
    }
  }
  //Output
  // Division 5.25
  // Exception inside function
  // Exception inside main function
  ```
* Exception thrown from functions
  ```cpp
  void test(int x){
    cout<<"Inside Func "<<x<<endl;
  }
  int main(){
    cout<<"Start"<<endl;
  }
  try{
    test(0);
    test(1);
    test(2);
  }
  catch(int x){
    cout<<"Caught an int Exception"<<endl;
  }
  //Output
  //Start
  //Inside Function 0;
  // Inside function 1;
  // Caught an int exception 1
  ```
* User Defined Exception
    ```cpp
    #include<exception>
    class myexception:public exception{
      const char* what() const throw(){
        return "My Exception happened";
      } // always use const before return type
    } myex;
    int main(){
      try{
        throw myex;
      }
      catch(exception& e){
        cout<<e.what()<<endl;
      }
    }
    // Output
    // My exception happened
    ```
DAY 2
---
OOP
---
* Error handling Function
   ```cpp
   #include<fstream>
   #using<iostream>
   using namespace std;
   int main(){
   // method 1
    ifstream fin;
    fin.open("sam10.txt");
    if(!fin){
      cout<<"File can not be opened"<<endl;
      return 0;
    }
    cout<<"file is opened"<<endl;
    //method 2
    fin.open("sam10.txt");
    if(fin.fail()){
      cout<<"File doesn't exist"<<endl;
      return 0;
    }
    cout<<"file is opened";
    return 0;
   }
   ```
* CASE STUDY
  * - [ ] Study Features used for MS office, I.E and VS COde that are written in visual C++ 
---
* Exception handling (Contd.)
 * If Exception is not found then the program runs without causing any interference.
 * The code that handles the error is called exception handler or catch block.
 * Errors generated in try block are catched in catch block.
    ```cpp
    try {
      // code that operates on object that might cause an exception
      throw e:
    }
    catch(E e){
      //handle exception
    }
    ```
 * ```cpp
 int main(){
  int x = -1;
  try{
    cout<<"Inside Try"<<endl;
    if(x<0){
      throw x;
      cout<<"After throw"<<endl;
    }
  }
  catch(int x){
    cout<<"Exception Caught"<<endl;
  }
  cout<<"After Catch"<<endl;
  return 0;
 }
 // Before Try
 // Inside try
 //Exception Caught
 ```
