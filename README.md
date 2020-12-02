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
