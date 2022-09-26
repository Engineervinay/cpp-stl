# Unordered map
## Example 
### print n strings with frequency for queries
```cpp
#include<bits/stdc++.h>
using namespace std;
//print n strings with frequency for queries

int main(){
    unordered_map<string,int> m;
    int n;
    string s;
    cin>>n;
    while(n--){
        cin>>s;
        m[s]++;
        
    }
    int q;
    cin>>q;
    while(q--){
        cin>>s;
        cout<<m[s]<<endl;
    }
    return 0;
}
```

I/p:
5
abc
qwe
qwe
qwe
hgj
2
qwe
hgj

O/p:
3
1
