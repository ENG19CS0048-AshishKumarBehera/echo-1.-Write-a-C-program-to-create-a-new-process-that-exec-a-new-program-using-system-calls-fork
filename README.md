# echo-1.-Write-a-C-program-to-create-a-new-process-that-exec-a-new-program-using-system-calls-fork
#include <stdio.h>
#include <stdlib.h>
#include <unistd.h>
void main(int argc, char *arg[])
{
int pid;
pid = fork();
if(pid<0){
printf("fork failed");
exit(1);
}
else if(pid==0){
execlp("date", "ls", NULL);
exit(0);
}
else{
wait(NULL);
printf("child complete\n");
exit(0);
}}
#include <stdio.h>
#include <stdlib.h>
#include <unistd.h>
void main(int argc, char *arg[])
{
int pid;
pid = fork();
if(pid<0){
printf("fork failed");
exit(1);
}
else if(pid==0){
execlp("cal", "ls", NULL);
exit(0);
}
else{
wait(NULL);
printf("child complete\n");
exit(0);
}
