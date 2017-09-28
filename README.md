```
#include <array> 
#include <string> 
#include <iostream> 
using namespace std ;

const array<char, 6> signs = { ' ', '.', ',', '?', '!', '/' }; 

bool isSign(char letter) 
{ 
for (auto& sign : signs) 
{ 
if (letter == sign)
{ 
return true; 
} 
} 
return false; 
} 

int main() 
{ 
string str1; 

cout<< "Enter a string:"<<endl; 

getline(cin, str1); 

bool isPalindrome = true; 

int left = 0; 

int right = str1.length() - 1; 

while(left < right)
{ 

while (isSign(str1[left]))
{
++left;
} 
while (isSign(str1[right]))
{
--right; 
} 

if (tolower(str1[left]) != tolower(str1[right]))
{ 
isPalindrome = false; 
break; 
} 

++left;
--right; 
} 

cout << isPalindrome <<endl; 

system("pause"); 
return 0; 
} 
```
