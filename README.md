# Cpp_interview
post all important questions related to CPP
hacker rank interview kit quotions 
day1
arr[6][6]={INITIALIZE ELEMENTS};
Q1.find the max sum of hourglass in the 6*6 matrix?
Ans->step1:Form 6*6 array and initialise array.
step2:called function sum_Hourglass() from driver function main()
step3:create variable int result=INT_MAX; To store result.
step4:find the last hourglass in the matrix and use there row and column number resp. for limitting the traversing of array using for loop.
step 5:calculate sum of all hourglass (16)
write for(row=0;row<=3;row++)
                 for(col=0;col<=3;col++)
                 int sum+=arr[0][0]+arr[0][1]+arr[0][2]+arr[1][1]+arr[2][0]+arr[2][1]+arr[2][2];
step 6:calculate max sum using built in function 
result=std::max(result,sum);    
step 7:display the result on console.


day2:STRING ANAGRAM
 Given two strings, finds the minimum number of character deletions required to make the two strings anagrams.
//int main() {
//    char s1[10010],s2[10010];
//    cout<<"Enter String 1:"<<"Enter String 2:";;
//    cin>>s1>>s2;
//    int a[26]={0};
//    for(int i=0;i<strlen(s1);i++)
//        a[s1[i]-'a']++;
//    for(int i=0;i<strlen(s2);i++)
//        a[s2[i]-'a']--;
//    long long int ans = 0;
//    for(int i=0;i<26;i++)
//        ans += abs(a[i]);
//    cout<<ans<<endl;
//    return 0;
//}


day3:ARRAY SPARSE
INPUT :4
aba
baba
aba
xzxb
3
aba
xzxb
ab

#include <bits/stdc++.h>

using namespace std;

// Complete the matchingStrings function below.
vector<int> matchingStrings(vector<string> strings, vector<string> queries) 
{
vector<int>result;
for(int i=0;i<queries.size();i++)
{
result.push_back(0);
for(int j=0;j<strings.size();j++)
   {
    if(queries[i]==strings[j])
    result[i]++;
   }
}
return result;
}

int main()
{
    ofstream fout(getenv("OUTPUT_PATH"));

    int strings_count;
    cin >> strings_count;
    cin.ignore(numeric_limits<streamsize>::max(), '\n');

    vector<string> strings(strings_count);

    for (int i = 0; i < strings_count; i++) {
        string strings_item;
        getline(cin, strings_item);

        strings[i] = strings_item;
    }

    int queries_count;
    cin >> queries_count;
    cin.ignore(numeric_limits<streamsize>::max(), '\n');

    vector<string> queries(queries_count);

    for (int i = 0; i < queries_count; i++) {
        string queries_item;
        getline(cin, queries_item);

        queries[i] = queries_item;
    }

    vector<int> res = matchingStrings(strings, queries);

    for (int i = 0; i < res.size(); i++) {
        fout << res[i];

        if (i != res.size() - 1) {
            fout << "\n";
        }
    }

    fout << "\n";

    fout.close();

    return 0;
}
// #include<iostream>
// #include<string.h>
// #include<map>
// using namespace std;
// int main(){

//     map<string,int>m;
//     int n,q;
//     string str;
   
//     cin >> n;
//     for(int i = 0; i < n; i++){
//         cin >> str;
//         m[str]++;
//     }
//     cin >> q;
//     for(int i = 0; i < q; i++){
//         cin >> str;
//         cout << m[str] << endl;
//     }
//     return 0;
// }
