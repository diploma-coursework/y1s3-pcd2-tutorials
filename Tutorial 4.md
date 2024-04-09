##### 1.
###### a)
```c
struct Employee {
	int socialSecurityNumber;
	char name[30];
	char address[50];
	float hourlySalaryRate;
} employees[1000];

for (int i = 0; i < 1000; i++) {
	employees[i].socialSecurityNumber = 0;
	strcpy(employees[i].name, "");
	strcpy(employees[i].address, "");
	employees[i].hourlySalaryRate = 0;	
}
```

###### b)
```c
FILE *inPtr;
inPtr = fopen("employee.txt", "r");
if (inPtr == NULL) {
	printf("Error opening employee.txt\n");
	exit(-1);
}

int i = 0;
while (fscanf(inPtr, "%d %s %s %f\n", 
			&employees[i].socialSecurityNumber,
			employees[i].name,
			employees[i].address,
			&employees[i].hourlySalaryRate) == 4) {
	++i;
}
```

##### 2.
###### a)
```c
typedef struct {
	int productCode;
	double cost;
	double sellingPrice;
	int quantity;
} ProdType;

FILE *inPtr;
inPtr = fopen("product.txt", "r");
if (inPtr == NULL) {
	printf("Error opening product.txt\n");
	exit(-1);
}

int i = 0;
while (fscanf(inPtr, "%d %f %f %d\n", 
			  prodType.productCode,
			  prodType.cost,
			  prodType.sellingPrice,
			  prodType.quantity
			   ) == 4) {
	prodType.sellingPrice *= 1.1;
	printf(
		"%d, %.2f %.2f %d\n", 
		prodType.productCode,
		prodType.cost,
		prodType.sellingPrice,
		prodType.quantity
	);
}

fclose(inPtr);
```

##### 3.
```c
FILE *filePtr1, *filePtr2;
filePtr1 = fopen("marks.txt", "r");
filePtr2 = fopen("report.txt", "w");
if (filePtr1 == NULL || filePtr2 == NULL) {
	printf("Error opening files.\n");
	exit(-1);
}

int i = 1, m1, m2, m3, m4;
double avg;
char name[20];

printf("NAME:         MARKS:       AVERAGE:\n\n");

while (1) {
	if (i % 2) {
		fscanf(filePtr1, "%[^\n]", name);
	} else {
		fscanf(filePtr1, "%d %d %d %d\n", m1, m2, m3, m4);
		avg = (m1 + m2 + m3 + m4) / 4.0;

		fprintf(filePtr2, "%-23s %d %d %d %d  %.2f%%\n", 
		name, m1, m2, m3, m4, avg);

		if (avg < 50.0)
			printf("%-23s %d %d %d %d  %.2f%%\n", name, m1, m2, m3, m4, avg);
	}

	++i;
}

fclose(filePtr1);
fclose(filePtr2);
```
