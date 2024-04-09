#### [Questions PDF here](https://drive.google.com/file/d/1AsHOWDAdG6IS_GMOoLiz8GQCzsjs6Pzb/view)

#### 1. 
##### (i)
```c
FILE *pOut;
```

##### (ii)
```c
pOut = fopen("sample.txt", "w");
```

##### (iii)
```c
if (pOut == NULL) {
	printf("Error opening sample.txt");
	exit(-1);
}
```

##### (iv)
```c
int int1, int2, int3, int4;
scanf("%d %d %d %d", &int1, &int2, &int3, &int4);
fprintf(pOut, "%d %d %d %d\n", int1, int2, int3, int4);
```

##### (iv)
```c
fclose(pOut);
```

#### 2.
```c
FILE *salesFilePtr;
int itemCode, unitSold;
double unitSalesPrice;

salesFilePtr = fopen("sales.txt", "w");

if (salesFilePtr == NULL) {
	printf("Error opening sales.txt");
	exit(-1);
}

while (1) {
	printf("Enter a sales record (-1 to Quit): ");
	scanf(" %d", &itemCode);
	if (itemCode < 0) break;

	printf("Unit sold: ");
	scanf(" %d", &unitSold);
	
	printf("Unit sales price: ");
	scanf(" %f", &unitSalesPrice);
	
	fprintf(salesFilePtr, "3d")
}

fclose(salesFilePtr);
```

#### 3.
```c
FILE *fPtr;
fPtr = fopen("number.txt", "r");
if (fPtr == NULL) {
	printf("Error opening number.txt\n");
	exit(-1);
}

int num, count = 0;
while (fscanf(fPtr, "%d", &num) != EOF) ++count;
printf("Count of numbers = %d", count);
```

#### 4.
```c
FILE *fPtr;
fPtr = fopen("alumni.txt", "r");
if (fPtr == NULL) {
	printf("Error opening alumni.txt\n");
	exit(-1);
}

char name[15], designation[20], category[10], location[20];
while (fscanf("%s %s %s %s\n", name, designation, category, location) != EOF) {
	printf("Name: %s\n", name);
	printf("Designation: %s\n", designation);
	printf("Category: %s\n", category);
	printf("Location: %s\n", location);
}
```

#### 5.
