# C-codes to reverse the Word in stgring using pointer 
#include <stdio.h>
#include <string.h>

void reverse(char *str,int len)
{
    char *sw = str;
    char *ew,temp;
    char *loop = str;
    for(int i = 0;i<=len+1;i++)
    {
       if(*loop == ' '|| *loop == '\0')
        {
            ew = loop-1;
            while(sw<ew)
            {
                temp = *sw;
                *sw = *ew;
                *ew = temp;
                
                sw++;
                ew--;
            }
            
            sw = loop+1;
            *loop++;
        }
        else
            loop++;
    }
}
int main()
{
    char str[] = "my name is shahid";
    int len = strlen(str);
    printf("%s\n",str);
    reverse(str,len);
    printf("%s\n",str);
    return 0;
}
