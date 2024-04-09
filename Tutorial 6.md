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
void f1(double a, double x);
```

###### ii)
```
a=1, x=2
a=3.2, x=4.3
```