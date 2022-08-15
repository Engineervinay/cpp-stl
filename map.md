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

###theory
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
