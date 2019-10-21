#include <stdio.h>
int main()
{
FILE *fp;
int line=1,str=0,word=0,ch;
int g=0;
fp=fopen("C:\\Users\\Lenovo\\Desktop\\lc.txt","r");
if (fp == NULL)
{
printf("Can't open the file\n");
return -1;
}
ch=fgetc(fp);
str++;
while(ch!=EOF)
{
printf("%c",ch);
if(ch=='\n')
{
line++;
}
else if(ch==' ')
{
word++;
}
else if(ch=='.')
{
g++;
}
str++;
ch=fgetc(fp);
}
printf("\n一共有:%d行 %d个单词 %d个字符 %d个句子\n",line,word,str,g);
fclose(fp);
} 
