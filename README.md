# Permutation-of-String

# Input & Output:

Enter the string :

ABC

Permutations of string :

ABC
ACB
BAC
BCA
CBA
CAB

# CODE 
 
    #include<stdio.h>
    #include<string.h>
    void swap(char *a,char *b){
        char t=*a;
        *a=*b;
        *b=t;
    }
    void permute(char *a,int start,int end){
        if(start==end){
            printf("%s\n",a);
        }
        else{
           for(int i=start;i<=eend;i++){
                swap((a+start),(a+i));
                permute(a,start+1,end);
                swap((a+start),(a+i));
           }
        }
    }
    int main()
    {
         char str[1000];
         printf("Enter the string :\n");
         scanf("%s",str);
         printf("Permutations of a given string :\n");
         int len=strlen(str);
         int start=0;
         int end=len-1;
         permute(str,start,end);
    }
