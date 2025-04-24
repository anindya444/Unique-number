# Unique-number
Given an array arr[] containing 2*n + 2 positive numbers, out of which 2*n numbers exist in pairs whereas the other two number occur exactly once and are distinct. The task is to find the other two numbers.  Note: Return the numbers in increasing order
#include <iostream>
#include <vector> 
using namespace std;
#include <algorithm>
vector<int>finduniqueno(vector<int>&a)
{    int i=0;int n=a.size();
    vector<int>ans;
    sort(a.begin(), a.end());
    while (i<n)
     {   
        if (i+1<n && a[i] == a[i+1] ) // check until i+1<n; and next equal value;
        { i=i+2;} // skip if both eqal;
        else
        {ans.push_back (a[i]); // insert it in ans if not equal
            i++;}
         
     }  return ans;
}
int main() {
    vector<int>a= {2,2,1,3,3,4};
    vector<int>result= finduniqueno(a);
    
    cout<<result[0] << " "<<result[1];
         
}
