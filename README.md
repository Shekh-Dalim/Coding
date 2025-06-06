/*
Q1. A company is transmitting data to another server. The data is in the form of numbers. To secure the data during transmission,
    they plan to obtain a security key that will be sent along with the data. The security key is identified as the count of the 
    unique repeating digits in the data. Write an algorithm to find the security key for the data.

    The input consists of an integer-, representing the data to be transmitted.

    Print an integer representing the security key for the given data


input: 12345
output: 0

input: 121342 
output: 2

*/

```
#include <bits/stdc++.h>
using namespace std;

int countRepeatingUniqueDigits(string sc, int size)
{
    unordered_map<char, int> freq;

    // Count frequency of each character
    for (int i = 0; i < size; i++)
    {
        freq[sc[i]]++;
    }

    int count = 0;

    // Count how many characters appear more than once
    for (auto ans : freq)
    {
        if (ans.second > 1)
        {
            count++;
        }
    }

    return count;
}

int main()
{
    string sc;
    cout << "Enter the number: ";
    cin >> sc;
    int size = sc.length();

    int ans = countRepeatingUniqueDigits(sc, size);
    cout << "The count of unique repeating digits is: " << ans << endl;

    return 0;
}
```

/************************* Count the number of unique element ***********************/
```
#include <bits/stdc++.h>
using namespace std;

int countUniqueEle(string sc, int size)
{

    unordered_map<char, int> freq;

    for (int i = 0; i < size; i++)
    {
        freq[sc[i]]++;
    }

    int count = 0;

    for (auto ans : freq)
    {
        if (ans.second == 1)
        {
            count++;
        }
    }
    return count;
}

int main()
{
    string sc;
    cout << "Enter the number: ";
    cin >> sc;
    int size = sc.length();

    int ans = countUniqueEle(sc, size);
    cout << "The unique element is: " << ans;

    return 0;
}
```

/*
Q2.Write a program to calculate and return the sum of distances between the adjacent number in an array of positive integers.
Note: You are expected to write code in the find Total Distance function only which receive the first parameter as the numbers
 of items in the array and second paramter as the array itself. You are not required to take the input from the console.

Example Finding the total distance between adjacent items of a list of 5 numbers.

Input 1: 5

input 2: 10 11 7 12 14

e Learning)

eparation

Output 12

*/
```
#include <bits/stdc++.h>
using namespace std;

void arrInput(int arr[], int size)
{
    for (int i = 0; i < size; i++)
    {
        cin >> arr[i];
    }
}
void arrDisplay(int arr[], int size)
{
    for (int i = 0; i < size; i++)
    {
        cout << arr[i] << " ";
    }
    cout << endl;
}

int SumValue(int arr[], int size)
{
    int sum = 0;
    for (int i = 0; i < size - 1; i++)
    {
        sum += abs(arr[i] - arr[i + 1]);
    }
    return sum;
}

int main()
{
    int arr[100];
    int size;
    cout << "Enter the size: ";
    cin >> size;

    arrInput(arr, size);
    arrDisplay(arr, size);

    int ans = SumValue(arr, size);
    cout << "the adjacent sum is: " << ans;
    return 0;
}
```

/*
Q2.Write a program to calculate and return the sum of distances between the adjacent number in an array of positive integers.
Note: You are expected to write code in the find Total Distance function only which receive the first parameter as the numbers
 of items in the array and second paramter as the array itself. You are not required to take the input from the console.

Example Finding the total distance between adjacent items of a list of 5 numbers.

Input 1: 5

input 2: 10 11 7 12 14

e Learning)

eparation

Output 12

*/
```
#include <bits/stdc++.h>
using namespace std;

void arrInput(int arr[], int size)
{
    for (int i = 0; i < size; i++)
    {
        cin >> arr[i];
    }
}
void arrDisplay(int arr[], int size)
{
    for (int i = 0; i < size; i++)
    {
        cout << arr[i] << " ";
    }
    cout << endl;
}

int SumValue(int arr[], int size)
{
    int sum = 0;
    for (int i = 0; i < size - 1; i++)
    {
        sum += abs(arr[i] - arr[i + 1]);
    }
    return sum;
}

int main()
{
    int arr[100];
    int size;
    cout << "Enter the size: ";
    cin >> size;

    arrInput(arr, size);
    arrDisplay(arr, size);

    int ans = SumValue(arr, size);
    cout << "the adjacent sum is: " << ans;
    return 0;
}
```
/*  7. Write a program to count the number of vowels in a string. */
```
// #include <bits/stdc++.h>
// using namespace std;

// int countVoul(string sc, int n)
// {
//     int count = 0;
//     for (int i = 0; i < n; i++)
//     {
//         if ((sc[i] == 'a' || sc[i] == 'A') || (sc[i] == 'e' || sc[i] == 'E') || (sc[i] == 'i' || sc[i] == 'I') || (sc[i] == 'o' || sc[i] == 'O') || (sc[i] == 'u' || sc[i] == 'U'))
//         {
//             count++;
//         }
//     }
//     return count;
// }
// int main()
// {
//     string sc;
//     cout << "Enter the String: ";
//     cin >> sc;
//     int size = sc.length();

//     int ans = countVoul(sc, size);
//     cout << "the numver of voul is: " << ans;
//     return 0;
// }
```
// 8. Write a Program to check whether the string is palindrome or not
```
#include <bits/stdc++.h>
using namespace std;

bool isPalindrom(string sc, int n)
{
    int s = 0;
    int e = n -1;
    while(s < e){
        if(sc[s] != sc[e]){
            return 0;
        }
        s++;
        e--;
    }
    return 1;
}
int main()
{
    string sc;
    cout << "Enter the String: ";
    cin >> sc;
    int size = sc.length();

    
    if( isPalindrom(sc, size)){
        cout<<"The string is Palindrom";
    }
    else{
        cout<<"The string is not palimdrom";
    }
    return 0;
}
```

/*
A Cloth merchant has some pieces of cloth of different lengths. He has an order of curtains of length of 12 feet.
He has to find how many curtains can  be made from these pieces. Length of pieces of cloth is recorded in feet.

Note : You are expected to write code in the findTotalCurtains function only which receive the first parameter
 as the number of items in the array and second parameter as the array itself. You are not required to take
 the input from the console.

Example

Finding the total curtains from a list of 5 cloth pieces.

Input
input 1 : 5
input 2 : 3 42 60 6 14

Output
9

Explanation
The first parameter 5 is the size of the array. Next is an array of measurements in feet. The total number of curtains is 5 which is calculated as under

3 -> 0
42 -> 3
60 -> 5
6 -> 0
14 -> 1
total = 9

*/
```
#include <bits/stdc++.h>
using namespace std;

int findTotalCurtains(int arr[], int n){
    int count = 0;
    for (int  i = 0; i < n; i++)
    {
      count += arr[i] / 12;   
    }

    return count;
    
}

int main()
{
    int arr[] ={3, 42, 60, 6, 14};
    int size = sizeof(arr) /sizeof(arr[0]);

    int ans = findTotalCurtains(arr,size);
    cout<<"the Total curtains is: "<<ans;
    return 0;
}
```
// 6. Write a program to find the maximum element in an array.
```
#include <bits/stdc++.h>
using namespace std;

int maxNumEle(int arr[],int n){

    unordered_map<int ,int> freq;

    for (int i = 0; i < n; i++)
    {
        freq[arr[i]]++;
    }
    
    int maxcount= INT_MIN;
    int maxEle = -1;
    for(auto ans: freq){
        if(ans.second > maxcount ){
            maxcount = ans.second;
            maxEle = ans.first;
        }
    }
    return maxEle;
}
int main()
{
    int arr[] = {1,2,3,8,4,4,4,4,5};
    int size = sizeof(arr)/sizeof(arr[0]);
    int ans = maxNumEle(arr,size);
    cout<<ans;
    return 0;
}
```

/*
9. Write a program to count occurrences of a specific character in a string.

Input a string from the user.

Input a character that the user wants to search for.

Count how many times that character appears in the string.

Print the count.

*/
```
// #include <bits/stdc++.h>
// using namespace std;

// int countChar(string sc, char ch)
// {
//     unordered_map<char,int> freq;

//     for (int i = 0; i < sc.length(); i++)
//     {
//         freq[sc[i]]++;
//     }

//     for(auto ans: freq){
//         if(ans.first == ch){
//             return ans.second;
//         }
//     }
    
// }

// int main()
// {

//     string sc;
//     cout << "Enter the string: ";
//     getline(cin,sc);

//     char ch;
//     cout<<"Enter the searching key element: ";
//     cin>>ch;

//     int ans = countChar(sc,ch);
//     cout<<"Count the occurance of a specific character" << ch<<" in string is: "<<ans;
//     return 0;
// }
```
/*   Write a program to remove duplicates from an array. */
```
#include <bits/stdc++.h>
using namespace std;

int main() {
    int arr[] = {1, 2, 3, 2, 4, 3, 5};
    int n = sizeof(arr) / sizeof(arr[0]);

    set<int> s;  // A set automatically removes duplicates and stores elements in sorted order.

    // Insert elements into the set
    for (int i = 0; i < n; i++) {
        s.insert(arr[i]);
    }

    // Display the unique elements
    cout << "Array after removing duplicates: ";
    for (int val : s) {
        cout << val << " ";
    }

    return 0;
}
```

// Count frequency of each element
```
#include <bits/stdc++.h>
using namespace std;

unordered_map<int, int> frequency(int arr[], int size) {
    unordered_map<int, int> freq;

    for (int i = 0; i < size; i++) {
        freq[arr[i]]++;
    }

    return freq;
}

int main() {
    int arr[] = {1, 1, 1, 1, 2, 2, 3, 1, 4};
    int size = sizeof(arr) / sizeof(arr[0]);

    unordered_map<int, int> ans = frequency(arr, size);

    for (auto it : ans) {
        cout << "Element " << it.first << " appears " << it.second << " times." << endl;
    }

    return 0;
}
```

/*************** Q: Reverse a string ****************/
```
#include <bits/stdc++.h>
using namespace std;

void stringReverse(string &st, int n)
{
    int s = 0;
    int e = n - 1;
    while (s < e)
    {
        swap(st[s], st[e]);
        s++;
        e--;
    }
}

int main()
{
    string str = "dalim";
    int size = str.length();
    cout << "String before reverse: " << str << endl;
    stringReverse(str, size);
    cout << "String After reverse: " << str << endl;

    return 0;
}
```

/************ Q: Find the Maximum Element in an array  **********/
```
#include <bits/stdc++.h>
using namespace std;

int maxEle(int arr[], int size)
{

    int maxEle = INT_MIN;
    for (int i = 0; i < size; i++)
    {
        if (arr[i] > maxEle)
        {
            maxEle = arr[i];
        }
    }
    return maxEle;
}

int main()
{
    int arr[6] = {1, 2, 3, 9, 3, 4};
    int size = sizeof(arr) / sizeof(arr[0]);

    int maxElement = maxEle(arr, size);
    cout << "Maximum Element: " << maxElement;
    return 0;
}
```

/************ Q: Find the Most Frequent Element in an array  **********/
```
#include <bits/stdc++.h>
using namespace std;

int mostFrequent(int arr[], int size)
{
    unordered_map<int, int> freq;

    // Count frequency of each element
    for (int i = 0; i < size; i++)
    {
        freq[arr[i]]++;
    }

    int maxFreq = 0;
    int mostFreqElement = arr[0];

    // Find the element with the highest frequency
    for (auto &entry : freq)
    {
        if (entry.second > maxFreq || 
           (entry.second == maxFreq && entry.first < mostFreqElement)) // tie-breaker: smallest value
        {
            maxFreq = entry.second;
            mostFreqElement = entry.first;
        }
    }

    return mostFreqElement;
}

int main()
{
    int arr[6] = {1, 2, 3, 9, 3, 4};
    int size = sizeof(arr) / sizeof(arr[0]);

    int result = mostFrequent(arr, size);
    cout << "Most Frequent Element: " << result;
    return 0;
}

```

/**************** Q: Check if a string is a palindrome or not ************/
```
#include <bits/stdc++.h>
using namespace std;

bool isPaindrom(string str, int n)
{
    int s = 0;
    int e = n -1;
    while(s < e){
        if(str[s++] != str[e--] ){
            return 0;
        }
    }
    return 1;
}

int main()
{

    string str = "daaed";
    int size = str.length();

    if (isPaindrom(str, size))
    {
        cout << "String is Palindrom";
    }
    else
    {
        cout << "String is not Palindrom";
    }
}
```

/************  Q: Find the Missing Number in an Array *****************/
```
#include <bits/stdc++.h>
using namespace std;

int missingEle(int arr[], int n)
{
    int total = (n + 1) * (n + 2) / 2; // sum formula uses n * (n + 1) / 2
    for (int i = 0; i < n; i++)
    {
        total -= arr[i];
    }
    return total;
}
int main()
{
    int arr[] = {1, 2, 4, 5, 6};
    int size = sizeof(arr) / sizeof(arr[0]);
    int ans = missingEle(arr, size);
    cout << "The missing element is: " << ans;
    return 0;
}
```

/***********  Q: Find the intersection of Two Array  ***********/
```
#include <bits/stdc++.h>
using namespace std;

vector<int> intersectionEle(int arr1[], int arr2[], int s1, int s2)
{

    vector<int> ans;

    for (int i = 0; i < s1; i++)
    {
        for (int j = 0; j < s2; j++)
        {
            if (arr2[i] == arr1[j])
            {
                ans.push_back(arr1[i]);
                break;
            }
        }
    }

    return ans;
}

int main()
{
    int arr1[] = {1, 2, 3, 4};
    int arr2[] = {1, 3, 4};

    int size1 = sizeof(arr1) / sizeof(arr1[0]);
    int size2 = sizeof(arr2) / sizeof(arr2[0]);

    vector<int> ans = intersectionEle(arr1, arr2, size1, size2);

    for (int ele : ans)
    {
        cout << ele << " ";
    }
    return 0;
}
```
