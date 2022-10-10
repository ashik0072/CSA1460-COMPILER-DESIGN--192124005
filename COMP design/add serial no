%{
int line_number = 1; // initializing line number to 1
%}

definition of line*/
line .*\n	

%%
{line} { printf("%10d %s", line_number++, yytext); }

%%

int yywrap(){}

int main(int argc, char*argv[])
{
extern FILE *yyin; // yyin as pointer of File type

yyin = fopen("testtest.c","r"); 

yylex(); // The function that starts the analysis.

return 0;
}
