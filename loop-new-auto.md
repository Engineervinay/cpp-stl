### create short loops 
```cpp
vector<int> v={1,2,3,4,5};
    
    for(int &val:v){
        cout<<val<<" ";
    }

```
can work for any containers and arrays.


### auto keyword to dynamically assume data type
```cpp
 vector<int> v={1,2,3,4,5};
    auto a=1;//auto keyword to autmatically choose data types 
    cout<<a;
    for(auto &val:v){//usefull for writing iterators declaration
        cout<<val<<" ";
    }

```
