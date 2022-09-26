### stl map insert erase operation with appending value.
```cpp

    int q, type; 
    cin >> q; 
    map<string,int> m; 
    string s;
    for (int i(0), mark; i<q; ++i)
    {
        cin >> type >> s;
        if (type == 1){
            cin >> mark;
            m[s] += mark;//adding marks with name of person
        }
        else if (type == 2)
            m.erase(s);
        else
            cout << m[s] << "\n";
    }
    
    
```

```
Sample Input

7
1 Jesse 20
1 Jess 12
1 Jess 18
3 Jess
3 Jesse
2 Jess
3 Jess
Sample Output

30
20
0
```

### theory
```
Map Template:

std::map <key_type, data_type>
Declaration:

map<string,int>m; //Creates a map m where key_type is of type string and data_type is of type int.
Size:

int length=m.size(); //Gives the size of the map.
Insert:

m.insert(make_pair("hello",9)); //Here the pair is inserted into the map where the key is "hello" and the value associated with it is 9.
Erasing an element:

m.erase(val); //Erases the pair from the map where the key_type is val.
Finding an element:

map<string,int>::iterator itr=m.find(val); //Gives the iterator to the element val if it is found otherwise returns m.end() .
Ex: map<string,int>::iterator itr=m.find("Maps"); //If Maps is not present as the key value then itr==m.end().
Accessing the value stored in the key:

To get the value stored of the key "MAPS" we can do m["MAPS"] or we can get the iterator using the find function and then by itr->second we can access the value.
```
## map gfg example
```cpp

/* Adds a value with key x and value y to the map*/
void add_value(map<int,int> &m,int x,int y)
{
    //Your code here
    m[x]=y;
}

/* Returns the value of the key
 x if present else returns -1 */
int find_value(map<int,int> &m,int x)
{
  //Your code here
  auto it=m.find(x);
  if(it==m.end()){
      return -1;
      
  }
  else 
    return (*it).second;
}

/* Prints contents of the map ie keys and values*/
void print_contents(map<int,int> &m)
{
   //Your code here
   for(auto &val:m){
       cout<<val.first<<" "<<val.second<<" ";
   }
}
```
## map questions
### print unique strings in lexographical order with frequency
```cpp
#include<bits/stdc++.h>
using namespace std;
//print unique string with their lexographical order with frequency
 


int main(){
    map<string,int> m;
    int n=5;
    string s;
    for(int i=0;i<n;i++){
        cin>>s;
        auto it=m.find(s);
        if(it==m.end()){
            m[s]=1;
        }
        else{
            m[s]=m[s] + 1;
        }
        
        /*
        easier approach 
           for(int i=0;i<n;i++){
                     cin>>s;
                    m[s]++; }

        */
        
    }
    for(auto &it : m){
        cout<<it.first<<" "<<it.second<<endl;
    }
}
```
