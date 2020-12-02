# 30-DAYS-OF-CP-AND-DSA 
DAY 1
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
