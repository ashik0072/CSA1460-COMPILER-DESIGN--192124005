%{
#include
float p,flag,answer;
char cc;
%}
digit [0-9]+
op “+”|”-“|”*”|”/”
%%
{digit} {
p=atof(yytext);
if(flag==0)
{
answer=p;
flag=1;
}
else
{
switch(cc)
{
case ‘+’:answer=answer+p;
case ‘-‘:answer=answer-p;
case ‘*’:answer=answer*p;
case ‘/’:answer=answer/p;
}
}
}
{op} {
if(strcmp(yytext,”+”)==0)
cc=’+’;
if(strcmp(yytext,”-“)==0)
cc=’-‘;
if(strcmp(yytext,”*”)==0)
cc=’*’;
if(strcmp(yytext,”/”)==0)
cc=’/’;
}
! {printf(“n Final Answer = %f”,answer);exit(0);}
%%
int main()
{
flag=answer=0;
printf(“n Enter the Question String :- “);
yylex();
return(0);
}
