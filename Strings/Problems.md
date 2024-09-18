
**Basic String Operations**

**1.	Reverse a String**

**Testcase 1:**

  Input: "hello"
  
  Output: "olleh"
  
**Testcase 2:**

  Input: "world"
  
  Output: "dlrow"
  
**Code**
```
#include<stdio.h>
#include<string.h>
int main()
{
    char str[100];
    scanf("%s",str);
    printf("%s\n",str);
    int size=strlen(str);
    for(int i=size-1;i>=0;i--)
    {
        printf("%c",str[i]);
    }
    printf("\n");
}
```

**2.	Check if a String is a Palindrome**

**Testcase 1:**

  Input: "radar"
  
  Output: true
  
**Testcase 2:**
 
   Input: "hello"
   
   Output: false
   
**Code**
```
#include<stdio.h>
#include<string.h>
int main()
{
    char str[100];
    char str2[100];
    scanf("%s",str);
    int size=strlen(str);
    int k=0;
    for(int i=size-1;i>=0;i--)
    {
        str2[k++]=str[i];
    }
    int isequal=1;
    for(int i=0;i<size;i++)
    {
        if(str[i]!=str2[i])
        {
            isequal=0;
            break;
        }
    }
    if(isequal)
    {
        printf("Equal");
    }
    else
    {
        printf("Not equal");
    }
    return 0;
}
```

**3.	Find the Length of a String**

 **Testcase 1:**
 
	Input: "hello"
 
	Output: 5
 
 **Testcase 2:**
 
	Input: "world"
 
	Output: 5
 
**Code**
```
#include<stdio.h>
#include<string.h>
int main()
{
    char str[100];
    scanf("%s",str);
    int length=0;
    while(str[length]!='\0')
    {
        length++;
    }
    printf("%d",length);
    return 0;
}
```

**4.	Concatenate Two Strings**

**Testcase 1:**

	Input: "hello", "world"
        
	Output: "helloworld"	
  
**Testcase 2:**

	Input: "foo", "bar"
 
	Output: "foobar"
 
**Code**

**Method 1**
```
#include<stdio.h>
#include<string.h>
int main()
{
    char str1[100];
    char str2[100];
    scanf("%s",str1);
    scanf("%s",str2);
    int l1=strlen(str1);
    int l2=strlen(str2);
    int size=l1+l2;
    char str3[size];
    int k=0;
    for(int i=0;i<l1;i++)
        {
         str3[k++]=str1[i];
        }
        for(int j=0;j<l2;j++)
        {
         str3[k++]=str2[j]; 
        }
    for(int k=0;k<size;k++)
    {
        printf("%c",str3[k]);
    }
    
    return 0;
}
```

**Method 2**
```
#include<stdio.h>
#include<string.h>

int main() {
    char str1[100];
    char str2[100];
    
    // Input the two strings
    scanf("%s", str1);
    scanf("%s", str2);

    // Get lengths of the strings
    int l1 = strlen(str1);
    int l2 = strlen(str2);
    int size = l1 + l2 + 1;  // +1 for the null terminator

    // Create a new array to store the concatenated result
    char str3[size];

    // Copy str1 to str3
    int k = 0;
    for (int i = 0; i < l1; i++) {
        str3[k++] = str1[i];
    }

    // Copy str2 to str3
    for (int j = 0; j < l2; j++) {
        str3[k++] = str2[j];
    }

    // Null-terminate the concatenated string
    str3[k] = '\0';

    // Output the concatenated string
    printf("%s\n", str3);
    
    return 0;
}
```
