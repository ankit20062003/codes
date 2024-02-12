// z function for pattern matching
#include <bits/stdc++.h>
using namespace std;
	

vector<int> z(string str){

  int len = str.size();
  vector<int> z(len,0);
  int l =0 , r =0;

  for(int i =1 ;i< len ; i++){

   if(i > r){
     l =i;
     r=i;
     while(r < len && str[r] == str[r-l])r++;

     z[i] = r-l;
    r--;

   }

   else {

    int index= i -l;
    if(i + z[index] <= r){
      z[i] = z[index];
    }
    else {
      l =i;
      while(r < len && str[r] == str[r-l])r++;

      z[i] = r-l;
      r--;
    }

   }

  }

  return z;

}  

int main()
{
	
//  string str ;
//  cin>> str;

 string str , pat ;
 cin>> str >> pat;
 string tot  = pat + "$" + str;
 vector<int> arr = z(tot);

 for(int i =0 ;i<arr.size() ;i++ ){
 if(arr[i] == pat.size()){
   cout << i - pat.size() -1 << endl;
 }

 }



//  vector<int> arr= z(str);
//  for(int i =0 ;i< str.size() ;i++){
//   cout << arr[i]<<" " ;
//  }

//  cout << endl;



 return 0;
}


