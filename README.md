#include <stdio.h>
int ns;
struct students
{
 char name[25];
 int rollno;
 int marks[11];
};
int main()
{
 int n,i,j,op,rn,op1,op2=2,mm;
 double markss,markss1,markss2=0,markss3=0;
 char sn[20];
 printf("ENTER THE NUMBER OF STUDENTS\n");
 scanf("%d",&n);
 struct students st[n];
 printf("ENTER THE NUMBER OF SUBJECTS\n");
 scanf("%d",&ns);
 printf("ENTER THE MAXIMUM MARKS\n");
 scanf("%d",&mm);
 for(i=0;i<n;i++)
 {
 printf("THE NAME OF THE STUDENT\n");
 scanf("%s",st[i].name);
 printf("THE ROLL NO. OF THE STUDENT\n");
 scanf("%d",&st[i].rollno);
 printf("ENTER THE NAME OF THE SUBJECT AND MARKS OBTAINED IN IT:-\n");
 for(j=0;j<ns;j++)
 {
 printf("ENTER THE NAME OF SUBJECT\n");
 scanf("%s",sn);
 printf("ENTER THE MARKS OBTAINED IN %s\n",sn);
 scanf("%d",&st[i].marks[j]);
 }
 printf("===========================================================\n");
 }
 printf("ENTER 1 TO OPEN MAIN MENUE\n");
 scanf("%d",&op1);
 while(op2==2)
 {
 switch(op1)
 {
 case 1:
 printf("NOW ENTER YOUR CHOICE ACCORDING TO THIS:-\n");
 printf("ENTER 1 FOR SEEING THE HIGHEST MARKS OF A STUDENT\n");
 printf("ENTER 2 FOR SEEING THE LOWEST MARKS OF A STUDENT\n");
 printf("ENTER 3 FOR SEEING THE AVERRAGE MARKS OF A STUDENT OF A STUDENT\n");
 printf("ENTER 4 FOR SEEING THE PERCENTAGE OBTAINED BY A STUDENT\n");
 scanf("%d",&op);
 switch(op)
 {
 case 1:
 printf("THE ROLL NO OF THE STUDENT\n");
 scanf("%d",&rn);
 for(i=0;i<n;i++)
 {
 if(rn==st[i].rollno)
 {
 for(j=0;j<ns;j++)
 {
 if(st[i].marks[0]<st[i].marks[j])
 {
 markss=st[i].marks[j];
 }
 }
 }
 }
 printf("HIGHEST MARKS BY ROLL NO. %d is %lf\n",rn,markss);
 printf("ENTER 2 TO RETURN TO MAIN MENUE\n");
 printf("ENTER ANY OTHER NUMBER TO EXIT\n");
 scanf("%d",&op2);
 break;
 case 2:
 printf("ENTER THE ROLL NO OF THE STUDENT\n");
 scanf("%d",&rn);
 for(i=0;i<n;i++)
 {
 if(rn==st[i].rollno)
 {
 for(j=0;j<ns;j++)
 {
 if(st[i].marks[0]>st[i].marks[j])
 {
 markss1=st[i].marks[j];
 }
 }
 }
 }
 printf("LOWEST MARKS BY ROLL NO. %d is %lf\n",rn,markss1);
 printf("ENTER 2 TO RETURN TO MAIN MENUE\n");
 printf("ENTER ANY OTHER NUMBER TO EXIT\n");
 scanf("%d",&op2);
 break;
 case 3:
 printf("ENTER THE ROLL NO OF THE STUDENT\n");
 scanf("%d",&rn);
 for(i=0;i<n;i++)
 {
 if(rn==st[i].rollno)
 {
 for(j=0;j<ns;j++)
 {
 markss2=markss2+st[i].marks[j];
 }
 printf("AVERAGE MARKS OF ROLL NO. %d IS %.2lf\n",rn,(markss2/ns));
 }
 }
 printf("ENTER 2 TO RETURN TO MAIN MENUE\n");
 printf("ENTER ANY OTHER NUMBER TO EXIT\n");
 scanf("%d",&op2);
 break;
 case 4:
 printf("ENTER THE ROLL NO OF THE STUDENT\n");
 scanf("%d",&rn);
 for(i=0;i<n;i++)
 {
 if(rn==st[i].rollno)
 {
 for(j=0;j<ns;j++)
 {
 markss3=markss3+st[i].marks[j];
 }
 markss3=(markss3/(mm*ns))*100;
 printf("PERCENTAGE OBTAINED BY ROLL NO. %d IS %.2lf\n",rn,markss3);
 }
 }
 printf("ENTER 2 TO RETURN TO MAIN MENUE\n");
 printf("ENTER ANY OTHER NUMBER TO EXIT\n");
 scanf("%d",&op2);
 break;
 default:
 printf("==========WRONG CHOICE==========\n");
 printf("ENTER 2 TO RETURN TO MAIN MENUE\n");
 printf("ENTER ANY OTHER NUMBER TO EXIT\n");
 scanf("%d",&op2);
 }
 break;
 default:
 printf("==========WRONG CHOICE==========\n");
 printf("ENTER 1 TO OPEN MAIN MENUE\n");
 printf("ENTER ANY OTHER NUMBER TO EXIT\n");
 scanf("%d",&op1);
 }
 }
 printf("=====THANKYOU=====");
return 0; 
}
