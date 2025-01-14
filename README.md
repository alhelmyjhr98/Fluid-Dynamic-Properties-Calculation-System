#include<stdio.h>
#include<conio.h>
#include <iostream>
#include<windows.h>
#include<stdlib.h>
#define PI 3.142
#define G 9.81

int i=0, j=0;
char yn;
COORD coord={0,0};

void gotoxy(int x,int y)
{
    coord.X=x;
	coord.Y=y;
	SetConsoleCursorPosition(GetStdHandle(STD_OUTPUT_HANDLE),coord);
}

void SetColor(int value)
{
	SetConsoleTextAttribute(GetStdHandle(STD_OUTPUT_HANDLE),value);
}

//function water

float velocityofwater (float f, float d)
{
	float velocity;
    SetColor(11);
    for (i=99;i>=66;i--)
    {
        gotoxy(i,9);
        printf("\xDB");
	}
    for (i=66;i<=99;i++)
    {
        gotoxy(i,11);
        printf("\xDB");
	}
	gotoxy(66,10);SetColor(189);printf("   Water Properties Calculation   ");
	gotoxy(63,15);SetColor(3);printf("            Velocity Of Water");
	gotoxy(63,19);SetColor(3);printf("          The formula is V=Q/A");
	gotoxy(63,24);SetColor(15);printf("Insert Flowrate (LPS) = ");
	scanf("%f",&f);
	gotoxy(63,26);SetColor(15);printf("Insert Diameter (m) = ");
	scanf("%f",&d);
	velocity=f/((PI*d*d)/4); // V=Q/A
	return velocity;
}

float densityofwater (float m,float r,float h)
{
	float density;
    SetColor(11);
    for (i=99;i>=66;i--)
    {
        gotoxy(i,9);
        printf("\xDB");
	}
    for (i=66;i<=99;i++)
    {
        gotoxy(i,11);
        printf("\xDB");
	}
	gotoxy(66,10);SetColor(189);printf("   Water Properties Calculation   ");
	gotoxy(63,15);SetColor(3);printf("            Density Of Water");
    gotoxy(63,19);SetColor(3);printf("          The formula is p=m/V");
	gotoxy(63,23);SetColor(15);printf("Insert Mass (kg) = ");
	scanf("%f",&m);
	gotoxy(63,25);SetColor(15);printf("Insert Radius (m) = ");
	scanf("%f",&r);
	gotoxy(63,27);SetColor(15);printf("Insert Height (m) = ");
	scanf("%f",&h);
	density=m/(PI*r*r*h); // p=m/V
	return density;
}

float pressureofwater (float p,float h)
{
	float pressure;
    SetColor(11);
    for (i=99;i>=66;i--)
    {
        gotoxy(i,9);
        printf("\xDB");
	}
    for (i=66;i<=99;i++)
    {
        gotoxy(i,11);
        printf("\xDB");
	}
	gotoxy(66,10);SetColor(189);printf("   Water Properties Calculation   ");
	gotoxy(63,15);SetColor(3);printf("           Pressure Of Water");
	gotoxy(63,19);SetColor(3);printf("        The formula is P=p*G*h");
	gotoxy(63,24);SetColor(15);printf("Insert Density (kg/m^3) = ");
	scanf("%f",&p);
	gotoxy(63,26);SetColor(15);printf("Insert Height (m) = ");
	scanf("%f",&h);
	pressure=p*G*h; // P=p*G*h
	return pressure;
}

float temperatureofwater (float q,float m)
{
	float temperature;
    SetColor(11);
    for (i=99;i>=66;i--)
    {
        gotoxy(i,9);
        printf("\xDB");
	}
    for (i=66;i<=99;i++)
    {
        gotoxy(i,11);
        printf("\xDB");
	}
	gotoxy(66,10);SetColor(189);printf("   Water Properties Calculation   ");
	gotoxy(63,15);SetColor(3);printf("         Temperature Of Water");
	gotoxy(63,19);SetColor(3);printf("      The formula is T=Q/(m*4.22)");
	gotoxy(63,24);SetColor(15);printf("Insert Heat (J) = ");
	scanf("%f",&q);
	gotoxy(63,26);SetColor(15);printf("Insert Mass (kg) = ");
	scanf("%f",&m);
	temperature=q/(m*4.22); // T=Q/(m*4.22)
	return temperature;
}

//function oil

float velocityofoil (float f, float d)
{
	float velocity;
    SetColor(11);
    for (i=99;i>=66;i--)
    {
        gotoxy(i,9);
        printf("\xDB");
	}
    for (i=66;i<=99;i++)
    {
        gotoxy(i,11);
        printf("\xDB");
	}
	gotoxy(66,10);SetColor(189);printf("    Oil Properties Calculation    ");
	gotoxy(63,15);SetColor(3);printf("            Velocity Of Oil");
	gotoxy(63,19);SetColor(3);printf("          The formula is V=Q/A");
	gotoxy(63,24);SetColor(15);printf("Insert Flowrate (LPS) = ");
	scanf("%f",&f);
	gotoxy(63,26);SetColor(15);printf("Insert Diameter (m) = ");
	scanf("%f",&d);
	velocity=f/((PI*d*d)/4); // V=Q/A
	return velocity;
}

float densityofoil (float m,float r,float h)
{
	float density;
    SetColor(11);
    for (i=99;i>=66;i--)
    {
        gotoxy(i,9);
        printf("\xDB");
	}
    for (i=66;i<=99;i++)
    {
        gotoxy(i,11);
        printf("\xDB");
	}
    gotoxy(66,10);SetColor(189);printf("    Oil Properties Calculation    ");
	gotoxy(63,15);SetColor(3);printf("             Density Of Oil");
    gotoxy(63,19);SetColor(3);printf("          The formula is p=m/V");
	gotoxy(63,23);SetColor(15);printf("Insert Mass (kg) = ");
	scanf("%f",&m);
	gotoxy(63,25);SetColor(15);printf("Insert Radius (m) = ");
	scanf("%f",&r);
	gotoxy(63,27);SetColor(15);printf("Insert Height (m) = ");
	scanf("%f",&h);
	density=m/(PI*r*r*h); // p=m/V
	return density;
}

float pressureofoil (float p,float h)
{
	float pressure;
    SetColor(11);
    for (i=99;i>=66;i--)
    {
        gotoxy(i,9);
        printf("\xDB");
	}
    for (i=66;i<=99;i++)
    {
        gotoxy(i,11);
        printf("\xDB");
	}
    gotoxy(66,10);SetColor(189);printf("    Oil Properties Calculation    "); 
	gotoxy(63,15);SetColor(3);printf("           Pressure Of Oil");
	gotoxy(63,19);SetColor(3);printf("        The formula is P=p*G*h");
	gotoxy(63,24);SetColor(15);printf("Insert Density (kg/m^3) = ");
	scanf("%f",&p);
	gotoxy(63,26);SetColor(15);printf("Insert Height (m) = ");
	scanf("%f",&h);
	pressure=p*G*h; // P=p*G*h
	return pressure;
}

float temperatureofoil (float q,float m)
{
	float temperature;
    SetColor(11);
    for (i=99;i>=66;i--)
    {
        gotoxy(i,9);
        printf("\xDB");
	}
    for (i=66;i<=99;i++)
    {
        gotoxy(i,11);
        printf("\xDB");
	}
    gotoxy(66,10);SetColor(189);printf("    Oil Properties Calculation    ");
	gotoxy(63,15);SetColor(3);printf("          Temperature Of Oil");
	gotoxy(63,19);SetColor(3);printf("      The formula is T=Q/(m*4.22)");
	gotoxy(63,24);SetColor(15);printf("Insert Heat (J) = ");
	scanf("%f",&q);
	gotoxy(63,26);SetColor(15);printf("Insert Mass (kg) = ");
	scanf("%f",&m);
	temperature=q/(m*4.22); // T=Q/(m*4.22)
	return temperature;
}

//function methanol

float velocityofmethanol (float f, float d)
{
	float velocity;
    SetColor(11);
    for (i=99;i>=66;i--)
    {
        gotoxy(i,9);
        printf("\xDB");
	}
    for (i=66;i<=99;i++)
    {
        gotoxy(i,11);
        printf("\xDB");
	}
	gotoxy(66,10);SetColor(189);printf("  Methanol Properties Calculation ");
	gotoxy(63,15);SetColor(3);printf("          Velocity Of Methanol");
	gotoxy(63,19);SetColor(3);printf("          The formula is V=Q/A");
	gotoxy(63,24);SetColor(15);printf("Insert Flowrate (LPS) = ");
	scanf("%f",&f);
	gotoxy(63,26);SetColor(15);printf("Insert Diameter (m) = ");
	scanf("%f",&d);
	velocity=f/((PI*d*d)/4); // V=Q/A
	return velocity;
}

float densityofmethanol (float m,float r,float h)
{
	float density;
    SetColor(11);
    for (i=99;i>=66;i--)
    {
        gotoxy(i,9);
        printf("\xDB");
	}
    for (i=66;i<=99;i++)
    {
        gotoxy(i,11);
        printf("\xDB");
	}
	gotoxy(66,10);SetColor(189);printf("  Methanol Properties Calculation ");
	gotoxy(63,15);SetColor(3);printf("           Density Of Methanol");
    gotoxy(63,19);SetColor(3);printf("          The formula is p=m/V");
	gotoxy(63,23);SetColor(15);printf("Insert Mass (kg) = ");
	scanf("%f",&m);
	gotoxy(63,25);SetColor(15);printf("Insert Radius (m) = ");
	scanf("%f",&r);
	gotoxy(63,27);SetColor(15);printf("Insert Height (m) = ");
	scanf("%f",&h);
	density=m/(PI*r*r*h); // p=m/V
	return density;
}

float pressureofmethanol (float p,float h)
{
	float pressure;
    SetColor(11);
    for (i=99;i>=66;i--)
    {
        gotoxy(i,9);
        printf("\xDB");
	}
    for (i=66;i<=99;i++)
    {
        gotoxy(i,11);
        printf("\xDB");
	}
	gotoxy(66,10);SetColor(189);printf("  Methanol Properties Calculation ");
	gotoxy(63,15);SetColor(3);printf("         Pressure Of Methanol");
	gotoxy(63,19);SetColor(3);printf("        The formula is P=p*G*h");
	gotoxy(63,24);SetColor(15);printf("Insert Density (kg/m^3) = ");
	scanf("%f",&p);
	gotoxy(63,26);SetColor(15);printf("Insert Height (m) = ");
	scanf("%f",&h);
	pressure=p*G*h; // P=p*G*h
	return pressure;
}

float temperatureofmethanol (float q,float m)
{
	float temperature;
    SetColor(11);
    for (i=99;i>=66;i--)
    {
        gotoxy(i,9);
        printf("\xDB");
	}
    for (i=66;i<=99;i++)
    {
        gotoxy(i,11);
        printf("\xDB");
	}
	gotoxy(66,10);SetColor(189);printf("  Methanol Properties Calculation ");
	gotoxy(63,15);SetColor(3);printf("         Temperature Of Methanol");
	gotoxy(63,19);SetColor(3);printf("       The formula is T=Q/(m*4.22)");
	gotoxy(63,24);SetColor(15);printf("Insert Heat (J) = ");
	scanf("%f",&q);
	gotoxy(63,26);SetColor(15);printf("Insert Mass (kg) = ");
	scanf("%f",&m);
	temperature=q/(m*4.22); // T=Q/(m*4.22)
	return temperature;
}

//function air

float velocityofair (float f, float d)
{
	float velocity;
    SetColor(11);
    for (i=99;i>=66;i--)
    {
        gotoxy(i,9);
        printf("\xDB");
	}
    for (i=66;i<=99;i++)
    {
        gotoxy(i,11);
        printf("\xDB");
	}
    gotoxy(66,10);SetColor(189);printf("    Air Properties Calculation    ");
	gotoxy(63,15);SetColor(3);printf("            Velocity Of Air");
	gotoxy(63,19);SetColor(3);printf("          The formula is V=Q/A");
	gotoxy(63,24);SetColor(15);printf("Insert Flowrate (LPS) = ");
	scanf("%f",&f);
	gotoxy(63,26);SetColor(15);printf("Insert Diameter (m) = ");
	scanf("%f",&d);
	velocity=f/((PI*d*d)/4); // V=Q/A
	return velocity;
}

float densityofair (float m,float r,float h)
{
	float density;
    SetColor(11);
    for (i=99;i>=66;i--)
    {
        gotoxy(i,9);
        printf("\xDB");
	}
    for (i=66;i<=99;i++)
    {
        gotoxy(i,11);
        printf("\xDB");
	}
    gotoxy(66,10);SetColor(189);printf("    Air Properties Calculation    ");
	gotoxy(63,15);SetColor(3);printf("             Density Of Air");
    gotoxy(63,19);SetColor(3);printf("          The formula is p=m/V");
	gotoxy(63,23);SetColor(15);printf("Insert Mass (kg) = ");
	scanf("%f",&m);
	gotoxy(63,25);SetColor(15);printf("Insert Radius (m) = ");
	scanf("%f",&r);
	gotoxy(63,27);SetColor(15);printf("Insert Height (m) = ");
	scanf("%f",&h);
	density=m/(PI*r*r*h); // p=m/V
	return density;
}

float pressureofair (float p,float h)
{
	float pressure;
    SetColor(11);
    for (i=99;i>=66;i--)
    {
        gotoxy(i,9);
        printf("\xDB");
	}
    for (i=66;i<=99;i++)
    {
        gotoxy(i,11);
        printf("\xDB");
	}
    gotoxy(66,10);SetColor(189);printf("    Air Properties Calculation    ");
	gotoxy(63,15);SetColor(3);printf("            Pressure Of Air");
	gotoxy(63,19);SetColor(3);printf("        The formula is P=p*G*h");
	gotoxy(63,24);SetColor(15);printf("Insert Density (kg/m^3) = ");
	scanf("%f",&p);
	gotoxy(63,26);SetColor(15);printf("Insert Height (m) = ");
	scanf("%f",&h);
	pressure=p*G*h; // P=p*G*h
	return pressure;
}

float temperatureofair (float q,float m)
{
	float temperature;
    SetColor(11);
    for (i=99;i>=66;i--)
    {
        gotoxy(i,9);
        printf("\xDB");
	}
    for (i=66;i<=99;i++)
    {
        gotoxy(i,11);
        printf("\xDB");
	}
    gotoxy(66,10);SetColor(189);printf("    Air Properties Calculation    ");
	gotoxy(63,15);SetColor(3);printf("           Temperature Of Air");
	gotoxy(63,19);SetColor(3);printf("      The formula is T=Q/(m*4.22)");
	gotoxy(63,24);SetColor(15);printf("Insert Heat (J) = ");
	scanf("%f",&q);
	gotoxy(63,26);SetColor(15);printf("Insert Mass (kg) = ");
	scanf("%f",&m);
	temperature=q/(m*4.22); // T=Q/(m*4.22)
	return temperature;
}

//function steam

float velocityofsteam (float f, float d)
{
	float velocity;
    SetColor(11);
    for (i=99;i>=66;i--)
    {
        gotoxy(i,9);
        printf("\xDB");
	}
    for (i=66;i<=99;i++)
    {
        gotoxy(i,11);
        printf("\xDB");
	}
	gotoxy(66,10);SetColor(189);printf("   Steam Properties Calculation   ");
	gotoxy(63,15);SetColor(3);printf("            Velocity Of Steam");
	gotoxy(63,19);SetColor(3);printf("          The formula is V=Q/A");
	gotoxy(63,24);SetColor(15);printf("Insert Flowrate (LPS) = ");
	scanf("%f",&f);
	gotoxy(63,26);SetColor(15);printf("Insert Diameter (m) = ");
	scanf("%f",&d);
	velocity=f/((PI*d*d)/4); // V=Q/A
	return velocity;
}

float densityofsteam (float m,float r,float h)
{
	float density;
    SetColor(11);
    for (i=99;i>=66;i--)
    {
        gotoxy(i,9);
        printf("\xDB");
	}
    for (i=66;i<=99;i++)
    {
        gotoxy(i,11);
        printf("\xDB");
	}
	gotoxy(66,10);SetColor(189);printf("   Steam Properties Calculation   ");
	gotoxy(63,15);SetColor(3);printf("            Density Of Steam");
    gotoxy(63,19);SetColor(3);printf("          The formula is p=m/V");
	gotoxy(63,23);SetColor(15);printf("Insert Mass (kg) = ");
	scanf("%f",&m);
	gotoxy(63,25);SetColor(15);printf("Insert Radius (m) = ");
	scanf("%f",&r);
	gotoxy(63,27);SetColor(15);printf("Insert Height (m) = ");
	scanf("%f",&h);
	density=m/(PI*r*r*h); // p=m/V
	return density;
}

float pressureofsteam (float p,float h)
{
	float pressure;
    SetColor(11);
    for (i=99;i>=66;i--)
    {
        gotoxy(i,9);
        printf("\xDB");
	}
    for (i=66;i<=99;i++)
    {
        gotoxy(i,11);
        printf("\xDB");
	}
	gotoxy(66,10);SetColor(189);printf("   Steam Properties Calculation   ");
	gotoxy(63,15);SetColor(3);printf("           Pressure Of Water");
	gotoxy(63,19);SetColor(3);printf("        The formula is P=p*G*h");
	gotoxy(63,24);SetColor(15);printf("Insert Density (kg/m^3) = ");
	scanf("%f",&p);
	gotoxy(63,26);SetColor(15);printf("Insert Height (m) = ");
	scanf("%f",&h);
	pressure=p*G*h; // P=p*G*h
	return pressure;
}

float temperatureofsteam (float q,float m)
{
	float temperature;
    SetColor(11);
    for (i=99;i>=66;i--)
    {
        gotoxy(i,9);
        printf("\xDB");
	}
    for (i=66;i<=99;i++)
    {
        gotoxy(i,11);
        printf("\xDB");
	}
	gotoxy(66,10);SetColor(189);printf("   Steam Properties Calculation   ");
	gotoxy(63,15);SetColor(3);printf("         Temperature Of Steam");
	gotoxy(63,19);SetColor(3);printf("      The formula is T=Q/(m*4.22)");
	gotoxy(63,24);SetColor(15);printf("Insert Heat (J) = ");
	scanf("%f",&q);
	gotoxy(63,26);SetColor(15);printf("Insert Mass (kg) = ");
	scanf("%f",&m);
	temperature=q/(m*4.22); // T=Q/(m*4.22)
	return temperature;
}

void display_msg(void)
{
    printf("Invalid Selection\n");
}


int main()
{
	float  velocity, density, pressure, temperature, f, d, m, r, h, p, q;
	int selection;
	char figure, option;
	

	char load0[50]="TO FLUID DYNAMICS PROPERTIES CALCULATION SYSTEM";
	char load1[50]="DEVELOPED BY:";
	char load2[50]="1.BURHANUDDIN AL HELMY";
	char load3[50]="2.FAHMI KHALILI";
	char load4[50]="3.NOR ATIKAH SAMSURI";
	char load5[50]="4.NUR ATIKAH MASRAN";
	char load6[50]="CHECKED BY:";
	char load7[50]="MADAM NORZALINA";
	char load8[50]="THANKS FOR USING OUR PROGRAM";
	char load9[50]="(c) 2020 MPCP , INC . ALL RIGHTS RESERVED";
	
	printf("\n\n\n\nPress any key to view your program in FULLSCREEN.\n\n");
	system("pause");
	system("cls");
	SetColor(11);
	gotoxy(60,11);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(60,12);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(60,13);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(60,14);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(60,15);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(61,14);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(62,13);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(63,12);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(64,13);
	{
		printf("\xB2");
		Sleep(50);
	}	
	gotoxy(65,14);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(66,15);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(66,14);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(66,13);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(66,12);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(66,11);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(68,11);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(68,12);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(68,13);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(68,14);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(68,15);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(69,11);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(70,11);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(71,11);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(72,11);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(69,13);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(70,13);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(71,13);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(69,15);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(70,15);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(71,15);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(72,15);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(74,11);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(74,12);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(74,13);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(74,14);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(74,15);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(75,15);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(76,15);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(77,15);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(78,15);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(84,11);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(83,11);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(82,11);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(81,11);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(80,12);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(80,13);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(80,14);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(81,15);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(82,15);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(83,15);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(84,15);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(89,11);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(88,11);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(87,11);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(86,12);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(86,13);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(86,14);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(87,15);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(88,15);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(89,15);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(90,14);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(90,13);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(90,12);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(92,15);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(92,14);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(92,13);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(92,12);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(92,11);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(93,12);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(94,13);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(95,14);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(96,13);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(97,12);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(98,11);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(98,12);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(98,13);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(98,14);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(98,15);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(100,11);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(100,12);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(100,13);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(100,14);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(100,15);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(101,11);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(102,11);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(103,11);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(104,11);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(101,13);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(102,13);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(103,13);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(101,15);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(102,15);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(103,15);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(104,15);
	{
		printf("\xB2");
		Sleep(50);
	}
	gotoxy(59,17);
	for(i=0;i<=47;i++)
	{
		printf("%c",load0[i]);
		Sleep(50);
	}
	SetColor(7);
	gotoxy(60,19);
	for(i=0;i<=13;i++)
	{
		printf("%c",load1[i]);
		Sleep(50);
	}
	gotoxy(74,21);
	for(i=0;i<=22;i++)
	{
		printf("%c",load2[i]);
		Sleep(50);
	}
	gotoxy(74,22);
	for(i=0;i<=15;i++)
	{
		printf("%c",load3[i]);
		Sleep(50);
	}
	gotoxy(74,23);
	for(i=0;i<=20;i++)
	{
		printf("%c",load4[i]);
		Sleep(50);
	}
	gotoxy(74,24);
	for(i=0;i<=19;i++)
	{
		printf("%c",load5[i]);
		Sleep(50);
	}
	gotoxy(60,25);
	for(i=0;i<=16;i++)
	{
		printf("%c",load6[i]);
		Sleep(50);
	}
	gotoxy(74,27);
	for(i=0;i<=15;i++)
	{
		printf("%c",load7[i]);
		Sleep(50);
	}
	///////////////////////////////////////////////
	SetColor(1);
	for(i=109;i>=55;i--)
	{
		gotoxy(i,7);
		printf("\xDC");
		Sleep(10);
	}
	for(i=8;i<=36;i++)
	{
		gotoxy(55,i);
		printf("\xDB");
		Sleep(10);
	}
	for(i=56;i<=109;i++)
	{
		gotoxy(i,36);
		printf("\xDC");
		Sleep(10);
	}
	for(i=36;i>=8;i--)
	{
		gotoxy(109,i);
		printf("\xDB");
		Sleep(10);
	}
	for(i=1;i<=1;i++)
	{
		gotoxy(91,30);SetColor(0);printf("              ");
		gotoxy(60,30);SetColor(14);printf("Do you want to continue? (Y/N):  ");
		scanf("%c", &yn);
		if (yn=='Y' || yn=='y')
		{
			system("cls");
			goto menu;
		}
		else if (yn=='N' || yn=='n')
		{
			system("cls");
			goto Exit;
		}
		
   }

	menu:
		{
			SetColor(7);
    	    for(i=109;i>=55;i--)
	        {
		    gotoxy(i,7);
		    printf("\xDC");
	        }
	        for(i=8;i<=36;i++)
	        {
		    gotoxy(55,i);
		    printf("\xDB");
	        }
	        for(i=56;i<=109;i++)
	        {
		    gotoxy(i,36);
		    printf("\xDC");
	        }
	        for(i=36;i>=8;i--)
	        {
		    gotoxy(109,i);
		    printf("\xDB");
        	} 
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,32);
		    printf("\xDC");
	        }
        	
        	SetColor(11);
        	for (i=105;i>=59;i--)
        	{
        		gotoxy(i,10);
        		printf("\xDB");
			}
        	for (i=59;i<=105;i++)
        	{
        		gotoxy(i,12);
        		printf("\xDB");
			}
			gotoxy(59,11);SetColor(189);printf("  FLUID DYNAMICS PROPERTIES CALCULATION SYSTEM ");  
			
        	SetColor(15);
        	for (i=75;i>=65;i--)
        	{
        		gotoxy(i,14);
        		printf("\xDB");
			}
        	for (i=65;i<=75;i++)
        	{
        		gotoxy(i,16);
        		printf("\xDB");
			}
	       	gotoxy(65,15);SetColor(253);printf ("   WATER   ");
	       	
       	    SetColor(15);
        	for (i=98;i>=88;i--)
        	{
        		gotoxy(i,14);
        		printf("\xDB");
			}
        	for (i=88;i<=98;i++)
        	{
        		gotoxy(i,16);
        		printf("\xDB");
			}
			gotoxy(88,15);SetColor(253);printf ("    OIL    ");
        	
			SetColor(15);
        	for (i=87;i>=76;i--)
        	{
        		gotoxy(i,18);
        		printf("\xDB");
			}
        	for (i=76;i<=87;i++)
        	{
        		gotoxy(i,20);
        		printf("\xDB");
			}
			gotoxy(76,19);SetColor(253);printf ("  METHANOL  ");
			
        	SetColor(15);
        	for (i=75;i>=65;i--)
        	{
        		gotoxy(i,22);
        		printf("\xDB");
			}
        	for (i=65;i<=75;i++)
        	{
        		gotoxy(i,24);
        		printf("\xDB");
			}
			gotoxy(65,23);SetColor(253);printf ("    AIR    ");
       	    
			SetColor(15);
        	for (i=98;i>=88;i--)
        	{
        		gotoxy(i,22);
        		printf("\xDB");
			}
        	for (i=88;i<=98;i++)
        	{
        		gotoxy(i,24);
        		printf("\xDB");
			}
			gotoxy(88,23);SetColor(253);printf ("   STEAM   ");
			
			SetColor(15);
        	for (i=86;i>=77;i--)
        	{
        		gotoxy(i,28);
        		printf("\xDB");
			}
        	for (i=77;i<=86;i++)
        	{
        		gotoxy(i,30);
        		printf("\xDB");
			}
			gotoxy(77,29);SetColor(253);printf ("   EXIT   "); 
        	gotoxy(61,34);SetColor(15);printf ("Enter your selection (Initial Alphabet) : ");
			scanf ("%s" , &option);
			system("cls");
		}
	
    option:
    if(option=='W' || option=='w') 
    {
        SetColor(7);
    	for(i=109;i>=55;i--)
	    {
		gotoxy(i,7);
		printf("\xDC");
	    }
	    for(i=8;i<=36;i++)
	    {
		gotoxy(55,i);
		printf("\xDB");
	    }
	    for(i=56;i<=109;i++)
	    {
		gotoxy(i,36);
		printf("\xDC");
	    }
	    for(i=36;i>=8;i--)
	    {
		gotoxy(109,i);
		printf("\xDB");
        } 
        for(i=56;i<=108;i++)
	    {
		gotoxy(i,32);
		printf("\xDC");
	    }
        
        SetColor(11);
        for (i=98;i>=65;i--)
        {
        gotoxy(i,10);
        printf("\xDB");
	    }
        for (i=65;i<=98;i++)
        {
        gotoxy(i,12);
        printf("\xDB");
	    }	
		gotoxy(65,11);SetColor(189);printf("   Water Properties Calculation   ");

        SetColor(7);
        for (i=89;i>=74;i--)
        {
            gotoxy(i,16);
        	printf("\xDC");
		}
		for (i=14;i<=16;i++)
		{
			gotoxy(74,i);
			printf("\xDB");
		}	
        for (i=74;i<=89;i++)
        {
        	gotoxy(i,14);
        	printf("\xDC");
		}
		for (i=16;i>=15;i--)
        {
        	gotoxy(89,i);
        	printf("\xDB");
		}
		gotoxy(75,15);SetColor(15);printf("  1-Velocity ");
		
        SetColor(7);
        for (i=89;i>=74;i--)
        {
            gotoxy(i,19);
        	printf("\xDC");
		}
		for (i=17;i<=19;i++)
		{
			gotoxy(74,i);
			printf("\xDB");
		}	
        for (i=74;i<=89;i++)
        {
        	gotoxy(i,17);
        	printf("\xDC");
		}
		for (i=19;i>=18;i--)
        {
        	gotoxy(89,i);
        	printf("\xDB");
		}
		gotoxy(75,18);SetColor(15);printf("  2-Density  ");
		
        SetColor(7);
        for (i=89;i>=74;i--)
        {
            gotoxy(i,22);
        	printf("\xDC");
		}
		for (i=20;i<=22;i++)
		{
			gotoxy(74,i);
			printf("\xDB");
		}	
        for (i=74;i<=89;i++)
        {
        	gotoxy(i,20);
        	printf("\xDC");
		}
		for (i=22;i>=21;i--)
        {
        	gotoxy(89,i);
        	printf("\xDB");
		}
		gotoxy(75,21);SetColor(15);printf("  3-Pressure ");
		
        SetColor(7);
        for (i=89;i>=74;i--)
        {
            gotoxy(i,25);
        	printf("\xDC");
		}
		for (i=23;i<=25;i++)
		{
			gotoxy(74,i);
			printf("\xDB");
		}	
        for (i=74;i<=89;i++)
        {
        	gotoxy(i,23);
        	printf("\xDC");
		}
		for (i=25;i>=24;i--)
        {
        	gotoxy(89,i);
        	printf("\xDB");
		}
		gotoxy(75,24);SetColor(15);printf("4-Temperature");
		
		SetColor(15);
        for (i=89;i>=74;i--)
        {
        	gotoxy(i,27);
        	printf("\xDB");
		}
        for (i=74;i<=89;i++)
        {
        	gotoxy(i,29);
        	printf("\xDB");
	    }
		gotoxy(74,28);SetColor(249);printf("   5-Main Menu  ");
		gotoxy(61,34);SetColor(15);printf("Please enter your selection : ");
		scanf ("%d" , &selection);
		system("cls");
        
        if (selection==1)
        {
			SetColor(7);
    	    for(i=109;i>=55;i--)
	        {
		    gotoxy(i,7);
		    printf("\xDC");
	        }
	        for(i=8;i<=36;i++)
	        {
		    gotoxy(55,i);
		    printf("\xDB");
	        }
	        for(i=56;i<=109;i++)
	        {
		    gotoxy(i,36);
		    printf("\xDC");
	        }
	        for(i=36;i>=8;i--)
	        {
		    gotoxy(109,i);
		    printf("\xDB");
        	} 
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,13);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,17);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,21);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,29);
		    printf("\xDC");
	        }
	        
            velocity=velocityofwater(f, d);
            gotoxy(63,31);SetColor(15);printf("Velocity Of Water is %.2f", velocity);
            
		    gotoxy(63,33);SetColor(15);printf ("Do you want to repeat to the MENU? (Y/N): " );
		    scanf("%s", &figure);
			
			if (figure=='Y' || figure=='y')
			{  
			system ("CLS");
		    goto option;
			}
			else if(figure=='N' || figure=='n')
			{
			system ("CLS");
		    goto menu;
	        }
		}
		
		else if (selection==2)
		{
			SetColor(7);
    	    for(i=109;i>=55;i--)
	        {
		    gotoxy(i,7);
		    printf("\xDC");
	        }
	        for(i=8;i<=36;i++)
	        {
		    gotoxy(55,i);
		    printf("\xDB");
	        }
	        for(i=56;i<=109;i++)
	        {
		    gotoxy(i,36);
		    printf("\xDC");
	        }
	        for(i=36;i>=8;i--)
	        {
		    gotoxy(109,i);
		    printf("\xDB");
        	} 
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,13);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,17);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,21);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,29);
		    printf("\xDC");
	        }
        	
			density=densityofwater(m,r,h);
			gotoxy(63,31);SetColor(15);printf("Density Of Water is %.2f", density);
		    
			gotoxy(63,33);SetColor(15);printf ("Do you want to repeat to the MENU? (Y/N): " );
		    scanf("%s", &figure);
			
			if (figure=='Y' || figure=='y')
			{  
			system ("CLS");
		    goto option;
			}
			else if(figure=='N' || figure=='n')
			{
			system ("CLS");
		    goto menu;
	        }
		}
		
		else if (selection==3)
		{
			SetColor(7);
    	    for(i=109;i>=55;i--)
	        {
		    gotoxy(i,7);
		    printf("\xDC");
	        }
	        for(i=8;i<=36;i++)
	        {
		    gotoxy(55,i);
		    printf("\xDB");
	        }
	        for(i=56;i<=109;i++)
	        {
		    gotoxy(i,36);
		    printf("\xDC");
	        }
	        for(i=36;i>=8;i--)
	        {
		    gotoxy(109,i);
		    printf("\xDB");
        	} 
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,13);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,17);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,21);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,29);
		    printf("\xDC");
	        }
        	
			pressure=pressureofwater(p,h);
			gotoxy(63,31);SetColor(15);printf("Pressure Of Water is %.2f", pressure);
		    
			gotoxy(63,33);SetColor(15);printf ("Do you want to repeat to the MENU? (Y/N): " );
		    scanf("%s", &figure);
			
			if (figure=='Y' || figure=='y')
			{  
			system ("CLS");
		    goto option;
			}
			else if(figure=='N' || figure=='n')
			{
			system ("CLS");
		    goto menu;
	        }
		}
        
        else if (selection==4)
		{
			SetColor(7);
    	    for(i=109;i>=55;i--)
	        {
		    gotoxy(i,7);
		    printf("\xDC");
	        }
	        for(i=8;i<=36;i++)
	        {
		    gotoxy(55,i);
		    printf("\xDB");
	        }
	        for(i=56;i<=109;i++)
	        {
		    gotoxy(i,36);
		    printf("\xDC");
	        }
	        for(i=36;i>=8;i--)
	        {
		    gotoxy(109,i);
		    printf("\xDB");
        	} 
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,13);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,17);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,21);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,29);
		    printf("\xDC");
	        }
        	
			temperature=temperatureofwater(q,m);
			gotoxy(63,31);SetColor(15);printf("Temperature Of Water is %.2f", temperature);

		    gotoxy(63,33);SetColor(15);printf ("Do you want to repeat to the MENU? (Y/N): " );
		    scanf("%s", &figure);
			
			if (figure=='Y' || figure=='y')
			{  
			system ("CLS");
		    goto option;
			}
			else if(figure=='N' || figure=='n')
			{
			system ("CLS");
		    goto menu;
	        }
		}
		
		else if (selection==5)
		{
			system("cls");
			goto menu;
		}
		
		else 
        
		display_msg();
        system ("CLS");
		goto menu;
	    
    }

    else if(option=='O' || option=='o')
    {
        SetColor(7);
    	for(i=109;i>=55;i--)
	    {
		gotoxy(i,7);
		printf("\xDC");
	    }
	    for(i=8;i<=36;i++)
	    {
		gotoxy(55,i);
		printf("\xDB");
	    }
	    for(i=56;i<=109;i++)
	    {
		gotoxy(i,36);
		printf("\xDC");
	    }
	    for(i=36;i>=8;i--)
	    {
		gotoxy(109,i);
		printf("\xDB");
        } 
        for(i=56;i<=108;i++)
	    {
		gotoxy(i,32);
		printf("\xDC");
	    }
        
        SetColor(11);
        for (i=98;i>=65;i--)
        {
        gotoxy(i,10);
        printf("\xDB");
	    }
        for (i=65;i<=98;i++)
        {
        gotoxy(i,12);
        printf("\xDB");
	    }	
		gotoxy(65,11);SetColor(189);printf("    Oil Properties Calculation    ");

        SetColor(7);
        for (i=89;i>=74;i--)
        {
            gotoxy(i,16);
        	printf("\xDC");
		}
		for (i=14;i<=16;i++)
		{
			gotoxy(74,i);
			printf("\xDB");
		}	
        for (i=74;i<=89;i++)
        {
        	gotoxy(i,14);
        	printf("\xDC");
		}
		for (i=16;i>=15;i--)
        {
        	gotoxy(89,i);
        	printf("\xDB");
		}
		gotoxy(75,15);SetColor(15);printf("  1-Velocity ");
		
        SetColor(7);
        for (i=89;i>=74;i--)
        {
            gotoxy(i,19);
        	printf("\xDC");
		}
		for (i=17;i<=19;i++)
		{
			gotoxy(74,i);
			printf("\xDB");
		}	
        for (i=74;i<=89;i++)
        {
        	gotoxy(i,17);
        	printf("\xDC");
		}
		for (i=19;i>=18;i--)
        {
        	gotoxy(89,i);
        	printf("\xDB");
		}
		gotoxy(75,18);SetColor(15);printf("  2-Density  ");
		
        SetColor(7);
        for (i=89;i>=74;i--)
        {
            gotoxy(i,22);
        	printf("\xDC");
		}
		for (i=20;i<=22;i++)
		{
			gotoxy(74,i);
			printf("\xDB");
		}	
        for (i=74;i<=89;i++)
        {
        	gotoxy(i,20);
        	printf("\xDC");
		}
		for (i=22;i>=21;i--)
        {
        	gotoxy(89,i);
        	printf("\xDB");
		}
		gotoxy(75,21);SetColor(15);printf("  3-Pressure ");
		
        SetColor(7);
        for (i=89;i>=74;i--)
        {
            gotoxy(i,25);
        	printf("\xDC");
		}
		for (i=23;i<=25;i++)
		{
			gotoxy(74,i);
			printf("\xDB");
		}	
        for (i=74;i<=89;i++)
        {
        	gotoxy(i,23);
        	printf("\xDC");
		}
		for (i=25;i>=24;i--)
        {
        	gotoxy(89,i);
        	printf("\xDB");
		}
		gotoxy(75,24);SetColor(15);printf("4-Temperature");
		
		SetColor(15);
        for (i=89;i>=74;i--)
        {
        	gotoxy(i,27);
        	printf("\xDB");
		}
        for (i=74;i<=89;i++)
        {
        	gotoxy(i,29);
        	printf("\xDB");
	    }
		gotoxy(74,28);SetColor(249);printf("   5-Main Menu  ");
		gotoxy(61,34);SetColor(15);printf("Please enter your selection : ");
		scanf ("%d" , &selection);
		system("cls");
        
        if (selection==1)
        {
			SetColor(7);
    	    for(i=109;i>=55;i--)
	        {
		    gotoxy(i,7);
		    printf("\xDC");
	        }
	        for(i=8;i<=36;i++)
	        {
		    gotoxy(55,i);
		    printf("\xDB");
	        }
	        for(i=56;i<=109;i++)
	        {
		    gotoxy(i,36);
		    printf("\xDC");
	        }
	        for(i=36;i>=8;i--)
	        {
		    gotoxy(109,i);
		    printf("\xDB");
        	} 
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,13);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,17);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,21);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,29);
		    printf("\xDC");
	        }
        	
			velocity=velocityofoil(f, d);
            gotoxy(63,31);SetColor(15);printf("Velocity Of Oil is %.2f", velocity);

		    gotoxy(63,33);SetColor(15);printf ("Do you want to repeat to the MENU? (Y/N): " );
		    scanf("%s", &figure);
			
			if (figure=='Y' || figure=='y')
			{  
			system ("CLS");
		    goto option;
			}
			else if(figure=='N' || figure=='n')
			{
			system ("CLS");
		    goto menu;
	        }
		}
		
		else if (selection==2)
		{
			SetColor(7);
    	    for(i=109;i>=55;i--)
	        {
		    gotoxy(i,7);
		    printf("\xDC");
	        }
	        for(i=8;i<=36;i++)
	        {
		    gotoxy(55,i);
		    printf("\xDB");
	        }
	        for(i=56;i<=109;i++)
	        {
		    gotoxy(i,36);
		    printf("\xDC");
	        }
	        for(i=36;i>=8;i--)
	        {
		    gotoxy(109,i);
		    printf("\xDB");
        	} 
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,13);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,17);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,21);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,29);
		    printf("\xDC");
	        }
        	
			density=densityofoil(m,r,h);
			gotoxy(63,31);SetColor(15);printf("Density Of Oil is %.2f", density);

		    gotoxy(63,33);SetColor(15);printf ("Do you want to repeat to the MENU? (Y/N): " );
		    scanf("%s", &figure);
			
			if (figure=='Y' || figure=='y')
			{  
			system ("CLS");
		    goto option;
			}
			else if(figure=='N' || figure=='n')
			{
			system ("CLS");
		    goto menu;
	        }
		}
		
		else if (selection==3)
		{
			SetColor(7);
    	    for(i=109;i>=55;i--)
	        {
		    gotoxy(i,7);
		    printf("\xDC");
	        }
	        for(i=8;i<=36;i++)
	        {
		    gotoxy(55,i);
		    printf("\xDB");
	        }
	        for(i=56;i<=109;i++)
	        {
		    gotoxy(i,36);
		    printf("\xDC");
	        }
	        for(i=36;i>=8;i--)
	        {
		    gotoxy(109,i);
		    printf("\xDB");
        	} 
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,13);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,17);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,21);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,29);
		    printf("\xDC");
	        }
			
			pressure=pressureofoil(p,h);
			gotoxy(63,31);SetColor(15);printf("Pressure Of Oil is %.2f", pressure);

		    gotoxy(63,33);SetColor(15);printf ("Do you want to repeat to the MENU? (Y/N): " );
		    scanf("%s", &figure);
			
			if (figure=='Y' || figure=='y')
			{  
			system ("CLS");
		    goto option;
			}
			else if(figure=='N' || figure=='n')
			{
			system ("CLS");
		    goto menu;
	        }
		}
        
        else if (selection==4)
		{
			SetColor(7);
    	    for(i=109;i>=55;i--)
	        {
		    gotoxy(i,7);
		    printf("\xDC");
	        }
	        for(i=8;i<=36;i++)
	        {
		    gotoxy(55,i);
		    printf("\xDB");
	        }
	        for(i=56;i<=109;i++)
	        {
		    gotoxy(i,36);
		    printf("\xDC");
	        }
	        for(i=36;i>=8;i--)
	        {
		    gotoxy(109,i);
		    printf("\xDB");
        	} 
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,13);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,17);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,21);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,29);
		    printf("\xDC");
	        }
			
			temperature=temperatureofoil(q,m);
			gotoxy(63,31);SetColor(15);printf("Temperature Of Oil is %.2f", temperature);

		    gotoxy(63,33);SetColor(15);printf ("Do you want to repeat to the MENU? (Y/N): " );
		    scanf("%s", &figure);
			
			if (figure=='Y' || figure=='y')
			{  
			system ("CLS");
		    goto option;
			}
			else if(figure=='N' || figure=='n')
			{
			system ("CLS");
		    goto menu;
	        }
		}
		
		else if (selection==5)
		{
			system("cls");
			goto menu;
		}
		
		else 
        
		display_msg();
        system ("CLS");
		goto menu;
	    
    }
    
    else if(option=='M' || option=='m')
    {
        SetColor(7);
    	for(i=109;i>=55;i--)
	    {
		gotoxy(i,7);
		printf("\xDC");
	    }
	    for(i=8;i<=36;i++)
	    {
		gotoxy(55,i);
		printf("\xDB");
	    }
	    for(i=56;i<=109;i++)
	    {
		gotoxy(i,36);
		printf("\xDC");
	    }
	    for(i=36;i>=8;i--)
	    {
		gotoxy(109,i);
		printf("\xDB");
        } 
        for(i=56;i<=108;i++)
	    {
		gotoxy(i,32);
		printf("\xDC");
	    }
        
        SetColor(11);
        for (i=98;i>=65;i--)
        {
        gotoxy(i,10);
        printf("\xDB");
	    }
        for (i=65;i<=98;i++)
        {
        gotoxy(i,12);
        printf("\xDB");
	    }
		gotoxy(65,11);SetColor(189);printf("  Methanol Properties Calculation ");

        SetColor(7);
        for (i=89;i>=74;i--)
        {
            gotoxy(i,16);
        	printf("\xDC");
		}
		for (i=14;i<=16;i++)
		{
			gotoxy(74,i);
			printf("\xDB");
		}	
        for (i=74;i<=89;i++)
        {
        	gotoxy(i,14);
        	printf("\xDC");
		}
		for (i=16;i>=15;i--)
        {
        	gotoxy(89,i);
        	printf("\xDB");
		}
		gotoxy(75,15);SetColor(15);printf("  1-Velocity ");
		
        SetColor(7);
        for (i=89;i>=74;i--)
        {
            gotoxy(i,19);
        	printf("\xDC");
		}
		for (i=17;i<=19;i++)
		{
			gotoxy(74,i);
			printf("\xDB");
		}	
        for (i=74;i<=89;i++)
        {
        	gotoxy(i,17);
        	printf("\xDC");
		}
		for (i=19;i>=18;i--)
        {
        	gotoxy(89,i);
        	printf("\xDB");
		}
		gotoxy(75,18);SetColor(15);printf("  2-Density  ");
		
        SetColor(7);
        for (i=89;i>=74;i--)
        {
            gotoxy(i,22);
        	printf("\xDC");
		}
		for (i=20;i<=22;i++)
		{
			gotoxy(74,i);
			printf("\xDB");
		}	
        for (i=74;i<=89;i++)
        {
        	gotoxy(i,20);
        	printf("\xDC");
		}
		for (i=22;i>=21;i--)
        {
        	gotoxy(89,i);
        	printf("\xDB");
		}
		gotoxy(75,21);SetColor(15);printf("  3-Pressure ");
		
        SetColor(7);
        for (i=89;i>=74;i--)
        {
            gotoxy(i,25);
        	printf("\xDC");
		}
		for (i=23;i<=25;i++)
		{
			gotoxy(74,i);
			printf("\xDB");
		}	
        for (i=74;i<=89;i++)
        {
        	gotoxy(i,23);
        	printf("\xDC");
		}
		for (i=25;i>=24;i--)
        {
        	gotoxy(89,i);
        	printf("\xDB");
		}
		gotoxy(75,24);SetColor(15);printf("4-Temperature");
		
		SetColor(15);
        for (i=89;i>=74;i--)
        {
        	gotoxy(i,27);
        	printf("\xDB");
		}
        for (i=74;i<=89;i++)
        {
        	gotoxy(i,29);
        	printf("\xDB");
	    }
		gotoxy(74,28);SetColor(249);printf("   5-Main Menu  ");
		gotoxy(61,34);SetColor(15);printf("Please enter your selection : ");
		scanf ("%d" , &selection);
		system("cls");
        
        if (selection==1)
        {
			SetColor(7);
    	    for(i=109;i>=55;i--)
	        {
		    gotoxy(i,7);
		    printf("\xDC");
	        }
	        for(i=8;i<=36;i++)
	        {
		    gotoxy(55,i);
		    printf("\xDB");
	        }
	        for(i=56;i<=109;i++)
	        {
		    gotoxy(i,36);
		    printf("\xDC");
	        }
	        for(i=36;i>=8;i--)
	        {
		    gotoxy(109,i);
		    printf("\xDB");
        	} 
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,13);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,17);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,21);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,29);
		    printf("\xDC");
	        }
        	
            velocity=velocityofmethanol(f, d);
            gotoxy(63,31);SetColor(15);printf("Velocity Of Methanol is %.2f", velocity);

		    gotoxy(63,33);SetColor(15);printf ("Do you want to repeat to the MENU? (Y/N): " );
		    scanf("%s", &figure);
			
			if (figure=='Y' || figure=='y')
			{  
			system ("CLS");
		    goto option;
			}
			else if(figure=='N' || figure=='n')
			{
			system ("CLS");
		    goto menu;
	        }
		}
		
		else if (selection==2)
		{
			SetColor(7);
    	    for(i=109;i>=55;i--)
	        {
		    gotoxy(i,7);
		    printf("\xDC");
	        }
	        for(i=8;i<=36;i++)
	        {
		    gotoxy(55,i);
		    printf("\xDB");
	        }
	        for(i=56;i<=109;i++)
	        {
		    gotoxy(i,36);
		    printf("\xDC");
	        }
	        for(i=36;i>=8;i--)
	        {
		    gotoxy(109,i);
		    printf("\xDB");
        	} 
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,13);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,17);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,21);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,29);
		    printf("\xDC");
	        }
			
			density=densityofmethanol(m,r,h);
			gotoxy(63,31);SetColor(15);printf("Density Of Methanol is %.2f", density);

		    gotoxy(63,33);SetColor(15);printf ("Do you want to repeat to the MENU? (Y/N): " );
		    scanf("%s", &figure);
			
			if (figure=='Y' || figure=='y')
			{  
			system ("CLS");
		    goto option;
			}
			else if(figure=='N' || figure=='n')
			{
			system ("CLS");
		    goto menu;
	        }
		}
		
		else if (selection==3)
		{
			SetColor(7);
    	    for(i=109;i>=55;i--)
	        {
		    gotoxy(i,7);
		    printf("\xDC");
	        }
	        for(i=8;i<=36;i++)
	        {
		    gotoxy(55,i);
		    printf("\xDB");
	        }
	        for(i=56;i<=109;i++)
	        {
		    gotoxy(i,36);
		    printf("\xDC");
	        }
	        for(i=36;i>=8;i--)
	        {
		    gotoxy(109,i);
		    printf("\xDB");
        	} 
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,13);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,17);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,21);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,29);
		    printf("\xDC");
	        }
			
			pressure=pressureofmethanol(p,h);
			gotoxy(63,31);SetColor(15);printf("Pressure Of Methanol is %.2f", pressure);

		    gotoxy(63,33);SetColor(15);printf ("Do you want to repeat to the MENU? (Y/N): " );
		    scanf("%s", &figure);
			
			if (figure=='Y' || figure=='y')
			{  
			system ("CLS");
		    goto option;
			}
			else if(figure=='N' || figure=='n')
			{
			system ("CLS");
		    goto menu;
	        }
		}
        
        else if (selection==4)
		{
			SetColor(7);
    	    for(i=109;i>=55;i--)
	        {
		    gotoxy(i,7);
		    printf("\xDC");
	        }
	        for(i=8;i<=36;i++)
	        {
		    gotoxy(55,i);
		    printf("\xDB");
	        }
	        for(i=56;i<=109;i++)
	        {
		    gotoxy(i,36);
		    printf("\xDC");
	        }
	        for(i=36;i>=8;i--)
	        {
		    gotoxy(109,i);
		    printf("\xDB");
        	} 
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,13);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,17);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,21);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,29);
		    printf("\xDC");
	        }
			
			temperature=temperatureofmethanol(q,m);
			gotoxy(63,31);SetColor(15);printf("Temperature Of Methanol is %.2f", temperature);

		    gotoxy(63,33);SetColor(15);printf ("Do you want to repeat to the MENU? (Y/N): " );
		    scanf("%s", &figure);
			
			if (figure=='Y' || figure=='y')
			{  
			system ("CLS");
		    goto option;
			}
			else if(figure=='N' || figure=='n')
			{
			system ("CLS");
		    goto menu;
	        }
		}
		
		else if (selection==5)
		{
			system("cls");
			goto menu;
		}
		
		else 
        
		display_msg();
        system ("CLS");
		goto menu;
	    
    }
    
    else if(option=='A' || option=='a')
    {
        SetColor(7);
    	for(i=109;i>=55;i--)
	    {
		gotoxy(i,7);
		printf("\xDC");
	    }
	    for(i=8;i<=36;i++)
	    {
		gotoxy(55,i);
		printf("\xDB");
	    }
	    for(i=56;i<=109;i++)
	    {
		gotoxy(i,36);
		printf("\xDC");
	    }
	    for(i=36;i>=8;i--)
	    {
		gotoxy(109,i);
		printf("\xDB");
        } 
        for(i=56;i<=108;i++)
	    {
		gotoxy(i,32);
		printf("\xDC");
	    }
        
        SetColor(11);
        for (i=98;i>=65;i--)
        {
        gotoxy(i,10);
        printf("\xDB");
	    }
        for (i=65;i<=98;i++)
        {
        gotoxy(i,12);
        printf("\xDB");
	    }	
		gotoxy(65,11);SetColor(189);printf("    Air Properties Calculation    ");

        SetColor(7);
        for (i=89;i>=74;i--)
        {
            gotoxy(i,16);
        	printf("\xDC");
		}
		for (i=14;i<=16;i++)
		{
			gotoxy(74,i);
			printf("\xDB");
		}	
        for (i=74;i<=89;i++)
        {
        	gotoxy(i,14);
        	printf("\xDC");
		}
		for (i=16;i>=15;i--)
        {
        	gotoxy(89,i);
        	printf("\xDB");
		}
		gotoxy(75,15);SetColor(15);printf("  1-Velocity ");
		
        SetColor(7);
        for (i=89;i>=74;i--)
        {
            gotoxy(i,19);
        	printf("\xDC");
		}
		for (i=17;i<=19;i++)
		{
			gotoxy(74,i);
			printf("\xDB");
		}	
        for (i=74;i<=89;i++)
        {
        	gotoxy(i,17);
        	printf("\xDC");
		}
		for (i=19;i>=18;i--)
        {
        	gotoxy(89,i);
        	printf("\xDB");
		}
		gotoxy(75,18);SetColor(15);printf("  2-Density  ");
		
        SetColor(7);
        for (i=89;i>=74;i--)
        {
            gotoxy(i,22);
        	printf("\xDC");
		}
		for (i=20;i<=22;i++)
		{
			gotoxy(74,i);
			printf("\xDB");
		}	
        for (i=74;i<=89;i++)
        {
        	gotoxy(i,20);
        	printf("\xDC");
		}
		for (i=22;i>=21;i--)
        {
        	gotoxy(89,i);
        	printf("\xDB");
		}
		gotoxy(75,21);SetColor(15);printf("  3-Pressure ");
		
        SetColor(7);
        for (i=89;i>=74;i--)
        {
            gotoxy(i,25);
        	printf("\xDC");
		}
		for (i=23;i<=25;i++)
		{
			gotoxy(74,i);
			printf("\xDB");
		}	
        for (i=74;i<=89;i++)
        {
        	gotoxy(i,23);
        	printf("\xDC");
		}
		for (i=25;i>=24;i--)
        {
        	gotoxy(89,i);
        	printf("\xDB");
		}
		gotoxy(75,24);SetColor(15);printf("4-Temperature");
		
		SetColor(15);
        for (i=89;i>=74;i--)
        {
        	gotoxy(i,27);
        	printf("\xDB");
		}
        for (i=74;i<=89;i++)
        {
        	gotoxy(i,29);
        	printf("\xDB");
	    }
		gotoxy(74,28);SetColor(249);printf("   5-Main Menu  ");
		gotoxy(61,34);SetColor(15);printf("Please enter your selection : ");
		scanf ("%d" , &selection);
		system("cls");

        if (selection==1)
        {
			SetColor(7);
    	    for(i=109;i>=55;i--)
	        {
		    gotoxy(i,7);
		    printf("\xDC");
	        }
	        for(i=8;i<=36;i++)
	        {
		    gotoxy(55,i);
		    printf("\xDB");
	        }
	        for(i=56;i<=109;i++)
	        {
		    gotoxy(i,36);
		    printf("\xDC");
	        }
	        for(i=36;i>=8;i--)
	        {
		    gotoxy(109,i);
		    printf("\xDB");
        	} 
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,13);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,17);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,21);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,29);
		    printf("\xDC");
	        }
        	
            velocity=velocityofair(f, d);
            gotoxy(63,31);SetColor(15);printf("Velocity Of Air is %.2f", velocity);

		    gotoxy(63,33);SetColor(15);printf ("Do you want to repeat to the MENU? (Y/N): " );
		    scanf("%s", &figure);
			
			if (figure=='Y' || figure=='y')
			{  
			system ("CLS");
		    goto option;
			}
			else if(figure=='N' || figure=='n')
			{
			system ("CLS");
		    goto menu;
	        }
		}
		
		else if (selection==2)
		{
			SetColor(7);
    	    for(i=109;i>=55;i--)
	        {
		    gotoxy(i,7);
		    printf("\xDC");
	        }
	        for(i=8;i<=36;i++)
	        {
		    gotoxy(55,i);
		    printf("\xDB");
	        }
	        for(i=56;i<=109;i++)
	        {
		    gotoxy(i,36);
		    printf("\xDC");
	        }
	        for(i=36;i>=8;i--)
	        {
		    gotoxy(109,i);
		    printf("\xDB");
        	} 
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,13);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,17);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,21);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,29);
		    printf("\xDC");
	        }
			
			density=densityofair(m,r,h);
			gotoxy(63,31);SetColor(15);printf("Density Of Air is %.2f", density);

		    gotoxy(63,33);SetColor(15);printf ("Do you want to repeat to the MENU? (Y/N): " );
		    scanf("%s", &figure);
			
			if (figure=='Y' || figure=='y')
			{  
			system ("CLS");
		    goto option;
			}
			else if(figure=='N' || figure=='n')
			{
			system ("CLS");
		    goto menu;
	        }
		}
		
		else if (selection==3)
		{
			SetColor(7);
    	    for(i=109;i>=55;i--)
	        {
		    gotoxy(i,7);
		    printf("\xDC");
	        }
	        for(i=8;i<=36;i++)
	        {
		    gotoxy(55,i);
		    printf("\xDB");
	        }
	        for(i=56;i<=109;i++)
	        {
		    gotoxy(i,36);
		    printf("\xDC");
	        }
	        for(i=36;i>=8;i--)
	        {
		    gotoxy(109,i);
		    printf("\xDB");
        	} 
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,13);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,17);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,21);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,29);
		    printf("\xDC");
	        }
			
			pressure=pressureofair(p,h);
			gotoxy(63,31);SetColor(15);printf("Pressure Of Air is %.2f", pressure);
		   
		    gotoxy(63,33);SetColor(15);printf ("Do you want to repeat to the MENU? (Y/N): " );
		    scanf("%s", &figure);
			
			if (figure=='Y' || figure=='y')
			{  
			system ("CLS");
		    goto option;
			}
			else if(figure=='N' || figure=='n')
			{
			system ("CLS");
		    goto menu;
	        }
		}
        
        else if (selection==4)
		{
			SetColor(7);
    	    for(i=109;i>=55;i--)
	        {
		    gotoxy(i,7);
		    printf("\xDC");
	        }
	        for(i=8;i<=36;i++)
	        {
		    gotoxy(55,i);
		    printf("\xDB");
	        }
	        for(i=56;i<=109;i++)
	        {
		    gotoxy(i,36);
		    printf("\xDC");
	        }
	        for(i=36;i>=8;i--)
	        {
		    gotoxy(109,i);
		    printf("\xDB");
        	} 
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,13);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,17);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,21);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,29);
		    printf("\xDC");
	        }
			
			temperature=temperatureofair(q,m);
			gotoxy(63,31);SetColor(15);printf("Temperature Of Air is %.2f", temperature);

		    gotoxy(63,33);SetColor(15);printf ("Do you want to repeat to the MENU? (Y/N): " );
		    scanf("%s", &figure);
			
			if (figure=='Y' || figure=='y')
			{  
			system ("CLS");
		    goto option;
			}
			else if(figure=='N' || figure=='n')
			{
			system ("CLS");
		    goto menu;
	        }
		}
		
		else if (selection==5)
		{
			system("cls");
			goto menu;
		}
		
		else 
        
		display_msg();
        system ("CLS");
		goto menu;
	    
    }

    else if(option=='S' || option=='s')
    {
        SetColor(7);
    	for(i=109;i>=55;i--)
	    {
		gotoxy(i,7);
		printf("\xDC");
	    }
	    for(i=8;i<=36;i++)
	    {
		gotoxy(55,i);
		printf("\xDB");
	    }
	    for(i=56;i<=109;i++)
	    {
		gotoxy(i,36);
		printf("\xDC");
	    }
	    for(i=36;i>=8;i--)
	    {
		gotoxy(109,i);
		printf("\xDB");
        } 
        for(i=56;i<=108;i++)
	    {
		gotoxy(i,32);
		printf("\xDC");
	    }
        
        SetColor(11);
        for (i=98;i>=65;i--)
        {
        gotoxy(i,10);
        printf("\xDB");
	    }
        for (i=65;i<=98;i++)
        {
        gotoxy(i,12);
        printf("\xDB");
	    }	
		gotoxy(65,11);SetColor(189);printf("   Steam Properties Calculation   ");

        SetColor(7);
        for (i=89;i>=74;i--)
        {
            gotoxy(i,16);
        	printf("\xDC");
		}
		for (i=14;i<=16;i++)
		{
			gotoxy(74,i);
			printf("\xDB");
		}	
        for (i=74;i<=89;i++)
        {
        	gotoxy(i,14);
        	printf("\xDC");
		}
		for (i=16;i>=15;i--)
        {
        	gotoxy(89,i);
        	printf("\xDB");
		}
		gotoxy(75,15);SetColor(15);printf("  1-Velocity ");
		
        SetColor(7);
        for (i=89;i>=74;i--)
        {
            gotoxy(i,19);
        	printf("\xDC");
		}
		for (i=17;i<=19;i++)
		{
			gotoxy(74,i);
			printf("\xDB");
		}	
        for (i=74;i<=89;i++)
        {
        	gotoxy(i,17);
        	printf("\xDC");
		}
		for (i=19;i>=18;i--)
        {
        	gotoxy(89,i);
        	printf("\xDB");
		}
		gotoxy(75,18);SetColor(15);printf("  2-Density  ");
		
        SetColor(7);
        for (i=89;i>=74;i--)
        {
            gotoxy(i,22);
        	printf("\xDC");
		}
		for (i=20;i<=22;i++)
		{
			gotoxy(74,i);
			printf("\xDB");
		}	
        for (i=74;i<=89;i++)
        {
        	gotoxy(i,20);
        	printf("\xDC");
		}
		for (i=22;i>=21;i--)
        {
        	gotoxy(89,i);
        	printf("\xDB");
		}
		gotoxy(75,21);SetColor(15);printf("  3-Pressure ");
		
        SetColor(7);
        for (i=89;i>=74;i--)
        {
            gotoxy(i,25);
        	printf("\xDC");
		}
		for (i=23;i<=25;i++)
		{
			gotoxy(74,i);
			printf("\xDB");
		}	
        for (i=74;i<=89;i++)
        {
        	gotoxy(i,23);
        	printf("\xDC");
		}
		for (i=25;i>=24;i--)
        {
        	gotoxy(89,i);
        	printf("\xDB");
		}
		gotoxy(75,24);SetColor(15);printf("4-Temperature");
		
		SetColor(15);
        for (i=89;i>=74;i--)
        {
        	gotoxy(i,27);
        	printf("\xDB");
		}
        for (i=74;i<=89;i++)
        {
        	gotoxy(i,29);
        	printf("\xDB");
	    }
		gotoxy(74,28);SetColor(249);printf("   5-Main Menu  ");
		gotoxy(61,34);SetColor(15);printf("Please enter your selection : ");
		scanf ("%d" , &selection);
		system("cls");
        
        if (selection==1)
        {
			SetColor(7);
    	    for(i=109;i>=55;i--)
	        {
		    gotoxy(i,7);
		    printf("\xDC");
	        }
	        for(i=8;i<=36;i++)
	        {
		    gotoxy(55,i);
		    printf("\xDB");
	        }
	        for(i=56;i<=109;i++)
	        {
		    gotoxy(i,36);
		    printf("\xDC");
	        }
	        for(i=36;i>=8;i--)
	        {
		    gotoxy(109,i);
		    printf("\xDB");
        	} 
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,13);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,17);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,21);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,29);
		    printf("\xDC");
	        }
        	
            velocity=velocityofsteam(f, d);
            gotoxy(63,31);SetColor(15);printf("Velocity Of Steam is %.2f", velocity);

		    gotoxy(63,33);SetColor(15);printf ("Do you want to repeat to the MENU? (Y/N): " );
		    scanf("%s", &figure);
			
			if (figure=='Y' || figure=='y')
			{  
			system ("CLS");
		    goto option;
			}
			else if(figure=='N' || figure=='n')
			{
			system ("CLS");
		    goto menu;
	        } 
		}
		
		else if (selection==2)
		{
			SetColor(7);
    	    for(i=109;i>=55;i--)
	        {
		    gotoxy(i,7);
		    printf("\xDC");
	        }
	        for(i=8;i<=36;i++)
	        {
		    gotoxy(55,i);
		    printf("\xDB");
	        }
	        for(i=56;i<=109;i++)
	        {
		    gotoxy(i,36);
		    printf("\xDC");
	        }
	        for(i=36;i>=8;i--)
	        {
		    gotoxy(109,i);
		    printf("\xDB");
        	} 
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,13);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,17);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,21);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,29);
		    printf("\xDC");
	        }
			
			density=densityofsteam(m,r,h);
			gotoxy(63,31);SetColor(15);printf("Density Of Steam is %.2f", density);

		    gotoxy(63,33);SetColor(15);printf ("Do you want to repeat to the MENU? (Y/N): " );
		    scanf("%s", &figure);
			
			if (figure=='Y' || figure=='y')
			{  
			system ("CLS");
		    goto option;
			}
			else if(figure=='N' || figure=='n')
			{
			system ("CLS");
		    goto menu;
	        }
		}
		
		else if (selection==3)
		{
			SetColor(7);
    	    for(i=109;i>=55;i--)
	        {
		    gotoxy(i,7);
		    printf("\xDC");
	        }
	        for(i=8;i<=36;i++)
	        {
		    gotoxy(55,i);
		    printf("\xDB");
	        }
	        for(i=56;i<=109;i++)
	        {
		    gotoxy(i,36);
		    printf("\xDC");
	        }
	        for(i=36;i>=8;i--)
	        {
		    gotoxy(109,i);
		    printf("\xDB");
        	} 
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,13);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,17);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,21);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,29);
		    printf("\xDC");
	        }
			
			pressure=pressureofsteam(p,h);
			gotoxy(63,31);SetColor(15);printf("Pressure Of Steam is %.2f", pressure);

		    gotoxy(63,33);SetColor(15);printf ("Do you want to repeat to the MENU? (Y/N): " );
		    scanf("%s", &figure);
			
			if (figure=='Y' || figure=='y')
			{  
			system ("CLS");
		    goto option;
			}
			else if(figure=='N' || figure=='n')
			{
			system ("CLS");
		    goto menu;
	        }
		}
        
        else if (selection==4)
		{
			SetColor(7);
    	    for(i=109;i>=55;i--)
	        {
		    gotoxy(i,7);
		    printf("\xDC");
	        }
	        for(i=8;i<=36;i++)
	        {
		    gotoxy(55,i);
		    printf("\xDB");
	        }
	        for(i=56;i<=109;i++)
	        {
		    gotoxy(i,36);
		    printf("\xDC");
	        }
	        for(i=36;i>=8;i--)
	        {
		    gotoxy(109,i);
		    printf("\xDB");
        	} 
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,13);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,17);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,21);
		    printf("\xDC");
	        }
        	for(i=56;i<=108;i++)
	        {
		    gotoxy(i,29);
		    printf("\xDC");
	        }
			
			temperature=temperatureofsteam(q,m);
			gotoxy(63,31);SetColor(15);printf("Temperature Of Steam is %.2f", temperature);

		    gotoxy(63,33);SetColor(15);printf ("Do you want to repeat to the MENU? (Y/N): " );
		    scanf("%s", &figure);
			
			if (figure=='Y' || figure=='y')
			{  
			system ("CLS");
		    goto option;
			}
			else if(figure=='N' || figure=='n')
			{
			system ("CLS");
		    goto menu;
	        }
		}
		
		else if (selection==5)
		{
			system("cls");
			goto menu;
		}
		
		else 
		
        display_msg();
        system ("CLS");
		goto menu;
	    
    }
    	
    else if (option=='E' || option=='e')
    {
	    Exit:
	    SetColor(1);
	    for (i=108;i>=56;i--)
	    {
		gotoxy(i,7);
		printf("\xDB");
	    }
	    for(i=7;i<=36;i++)
	    {
		gotoxy(55,i);
		printf("\xDB");
	    }
	    for(i=56;i<=109;i++)
	    {
		gotoxy(i,36);
		printf("\xDB");
	    }
	    for(i=36;i>=7;i--)
	    {
		gotoxy(109,i);
		printf("\xDB");
	    }
	    SetColor(14);
	    gotoxy(68,20);
	    for(i=0;i<=28;i++)
	    {
		printf("%c",load8[i]);
		Sleep(50);
	    }
	    gotoxy(62,22);
	    for(i=0;i<=41;i++)
	    {
		printf("%c",load9[i]);
		Sleep(50);
	    }
    }

    return 0;
}
