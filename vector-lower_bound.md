**program to find lower bound of an element in vector:**
```cpp
vector<int> v;
    int n,q;
    cin>>n;
    for(int i=0;i<n;i++){
        int data;
        cin>>data;
        v.push_back(data);
    }
    cin>> q;
    for(int i=0;i<q;i++){
        int temp;
        cin>>temp;
        vector<int>::iterator it;//creating iterator for vector
        it=lower_bound(v.begin(),v.end(),temp);//lower bound function
        if(*it==temp){
            
            cout<<"Yes"<<" "<<it-v.begin()+1<<endl;
    }
    else 
            cout<<"No"<<" "<<it-v.begin()+1<<endl;

}   
```
```
Sample Input

 8
 1 1 2 2 6 9 9 15
 4
 1
 4
 9
 15
Sample Output

 Yes 1
 No 5
 Yes 6
 Yes 8
 ```
