**program to add, delete and find element in set**
```cpp
 set<int> s;
    int n;
    cin>>n;
    while(n--){
        int q,data;
        cin>>q;
        cin>>data;
        if(q==1){
            s.insert(data);
        }
        else if(q==2){
            s.erase(data);
            
        }
        else if(q==3){
            set<int>::iterator it=s.find(data);
            if(it!=s.end())cout<<"Yes"<<endl;
            else cout<<"No"<<endl;
        }
    }
   
```

```
Sample Input

8
1 9
1 6
1 10
1 4
3 6
3 14
2 6
3 6
Sample Output

Yes
No
No
```

Declaration:
```cpp
set<int>s; //Creates a set of integers.
```
Size:
```cpp
int length=s.size(); //Gives the size of the set.
```

  Insert:
```cpp
s.insert(x); //Inserts an integer x into the set s.
```
Erasing an element:
```cpp
s.erase(val); //Erases an integer val from the set s.
```
Finding an element:
```cpp
set<int>::iterator itr=s.find(val); //Gives the iterator to the element val if it is found otherwise returns s.end() .
Ex: set<int>::iterator itr=s.find(100); //If 100 is not present then it==s.end().
```


## Examples
### given n strings print given strings in lexographical order
```cpp
#include<bits/stdc++.h>
using namespace std;
//given n strings print given strings in lexographical order

int main(){
   set<string> s;
   int n;
   cin>>n;
   string temp;
   while(n--){
       cin>>temp;
       s.insert(temp);
   }
   for(auto val:s){
       cout<<val<<endl;
   }
   
    return 0;
}
```
