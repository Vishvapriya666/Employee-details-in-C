# Employee-details-in-C
The following program is to print pay slip of an employee using structures

#include<stdio.h> 

struct emp 

{ 

int id; 

char name[30]; 

char desig[20]; 

char dept[20]; 

int pf; 

float basic,hra,da,ta,net; 

}; 

int main() 

{ 

struct emp e; 

printf("Enter id, name, designation, department and basic salary"); 

scanf("%d %s %s %s %f",&e.id,e.name,e.desig,e.dept,&e.basic); 

e.hra = e.basic * 0.3; 

e.da = e.basic * 1.25; 

e.ta = e.basic * 0.15; 

e.pf = 2500; 

e.net = (e.basic + e.hra + e.ta + e.da) - e.pf; 

printf("\n****************EMPLOYEE PAY SLIP**************\n"); 

printf("\nName : %s\tDesignation : %s\n",e.name,e.desig); 

printf("\nDept : %s\tEmployee ID : %d\n",e.dept,e.id); 

printf("\nBasic salary : %6.2f\tNet Salary:%6.2f",e.basic,e.net); 

printf("\n******************************************\n"); 

printf("\nNote:HRA as 30 percent, DA as 125 percent,\nTA as 15 percent of basic, PF - 2500 INR\n"); 

return 0; 

} 
