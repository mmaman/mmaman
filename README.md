- 👋 Hi, I’m @mmaman
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
mmaman/mmaman is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

#include <iostream>

using namespace std;

#include <queue> 
using namespace std;


void printKMax(int arr[], int n, int k){
	//Write your code here.   
    priority_queue<int> p;
    for(int i = 0; i < n; i++){
       if ( (n-i) >= k)
       {
            int ii = 0;
            while( ii < k ){
                p.push(arr[ii+i]);        
                ii++;
            }       
            cout << p.top() << " ";
            //p = priority_queue<int>();
       }
       p = priority_queue<int>();
    }
    cout << "\n";
}


int main()
{
int arr[] = {12, 1, 78, 90, 57, 89, 56};
  int n = sizeof(arr)/sizeof(int);
  printKMax(arr, n, 3);
    return 0;
}

// 12, 1, 78 -  78
// 1, 78, 90 -  90
// 78, 90, 57 - 90
// 90, 57, 89 - 90
// 57, 89, 56 - 89

