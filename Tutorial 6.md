##### 1.
```c
double inchToCm(double inches) {
	return inches * 2.54;
}
```

##### 2.
```c
double converter(double hectares) {
	return hectares * 2.47;
}
```

##### 3.
```c
double hypotenuse(double a, double b) {
	return sqrt(a*a + b*b);
}
```

##### 4.
```c
char gradeOf(int score) {
	if (score < 0 || score > 100) return 'X';
	if (score < 40) return 'F';
	if (score < 50) return 'D';
	if (score < 70) return 'C';
	if (score < 80) return 'B';
	return 'A';
}
```

##### 5.
###### i)
```c
void f1(int a, double x);
```

###### ii)
```
a=1, x=2.000000
a=3, x=4.300000
```

##### 6.
###### a)
```c
double calEpf(double salary) {
return salary * 0.11;
}
```

###### b)
```c
double salary, EPF;
printf("Enter the salary >");
scanf("%lf", &salary);
EPF = calEpf(salary);
printf("Total EPF charges: RM%.2f", EPF);
```

##### 7.
```c

```