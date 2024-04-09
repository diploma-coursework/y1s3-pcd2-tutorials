#### [Questions PDF here](https://drive.google.com/file/d/1aygGfqnwAmPUAi7pitGb-J2YrVd8I9bu/view)

#### 1. 
##### (i)
```c
struct Prod {
	int id;
	int year;
	char name[40];
	double price;
};
```

##### (ii)
```c
struct Prod product[3] = {
	{ 1111, 2011, "AAA", 12.5 },
	{ 2222, 2012, "BBB", 50.0 },
	{ 3333, 2010, "CCC", 38.5 },
};
```

##### (iii)
`product[1].year` = 2012
`product[2].id` = 3333
`product[0].name` = "AAA"

#### 2.
```c
typedef struct {
	char name[20];
	char sex;
	Date birthday;
} Personal;

Personal strong;
```

#### 3.
##### (i)
```c
struct Employee {
	char employeeName[30];
	char employeeId[10];
	char address[35];
	char phoneNumber[15];
	double salary;
};
```

##### (ii)
```c
struct Employee emp[100];
```

##### (iii)
```c
for (int i = 0; i < 100; i++) {
	printf("Employee %d:", i + 1);

	printf("Name > ");
	scanf(" %[^\n]", emp[i].employeeName);

	printf("Id > ");
	scanf(" %9s", emp[i].employeeId);

	printf("Address > ");
	scanf(" %[^\n]", emp[i].address);

	printf("Phone Number > ");
	scanf(" %12s", emp[i].phoneNumber);
	
	printf("salary > ");
	scanf(" %f", emp[i].salary);
}
```

##### (iv)
```c
strcpy(emp[99].employeeName, "Anthony Swamy");
```

##### (v)
```c
typedef struct {
	char departmentCode[6];
	char managerName[20];
	struct Employee employee;
} Boss;
```

#### 4.
##### (i)
```c
typedef struct {
	int id;
	char name[30];
	char position[10];
} Employee;
```

##### (ii)
```c
struct Wrk {
	Employee emp;
	float rate;
	int hours;
	float basic;
};
```

##### (iii)
```c
struct Wrk empWrk[10] = {
	{ { 771122, "Mike Wong", "Programmer" }, 4.62, 40, 1800.0 },
	{ { 345906, "Bill John", "Manager" }, 8.51, 38, 2400.0 }
};
```

##### (iv)
```c
printf("Name: %s\n", empWrk[1].emp.name);
printf("Pay: %.2f", empWrk[1].rate * empWrk[1].hours + empWrk[1].basic);
```

#### 5.
##### (i)
```c
typedef struct {
	char subject[20];
	int time;
	char day[9];
} Schedule;
```

##### (ii)
```c
struct Address {
	char street[20];
	char city[20];
	char state[10];
	char zip[5];
};
```

##### (iii)
```c
typedef struct {
	char registrationNumber[10];
	struct Address address;
	double GPA;
	Schedule schedule[6];
} StudentData;
```

##### (iv)
```c
StudentData stud1;
```

##### (v)
```c
strcpy(stud1.schedule[0].subject, "PROGRAMMING");
```

##### (iv)
```c
stud1.schedule[5].time = 10;
```

#### 6.
##### (i)
```c
struct Date {
	int month;
	int day;
	int year;
};
```

##### (ii)
```c
typedef struct {
	char studentName[30];
	char icNo[15];
	struct Date birthDate;
} Student;
```

##### (iii)
```c
typedef struct {
	char programmeTitle[40];
	struct Date commencingDate;
	Student studentData[10];
} Programme;
```

##### (iv)
```c
Programme ibProgramme;
```

##### (v)
```c
for (int i = 0; i < 10; i++) {
	printf("Student %d:\n", i + 1);
	
	printf("Enter student name > ");
	scanf(" %30[^\n]", ibProgramme[i].studentName);

	printf("Enter student IC number > ");
	scanf(" %15s", ibProgramme[i].icNo);

	printf("Enter student birth date (e.g. 14/3/2000) > ");
	scanf(" %d/%d/%d", ibProgramme[i].day, ibProgramme[i].month, ibProgramme[i].year);
}
```

