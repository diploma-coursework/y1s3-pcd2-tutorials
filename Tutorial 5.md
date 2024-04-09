##### 1.
| Text file               | Binary file                       |
|-------------------------|-----------------------------------|
| File extension is .txt  | File extensions are .bin and .dat |
| Stores ASCII characters | Stores data in binary format      |
| Slower                  | Faster                            |

##### 2.
```c
typedef struct {
	int x, y;
} Coord;

Coord point = { 7, 8 };
FILE *sp;

sp = fopen("COORD.bin", "wb");
fwrite(&point, sizeof(Coord), 1, sp);
fclose(sp);
```

##### 3.
```c
FILE *fPtr;
char str[10] = "Hello";
fPtr = fopen("binary.bin", "wb");
fwrite(str, sizeof(str), 1, fPtr);
```

##### 4.
```c

```