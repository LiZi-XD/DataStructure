## 顺序存储结构

```c
#define MAXSIZE 20
typedef int ElemType;
typrdef struct{
    ElemType data[MAXSIZE];
    int length;
}SqList;
```

Properties：

1.存储空间的起始位置----data

2.线性表的最大存储容量----MAXSIZE

3.线下表的当前长度----length

### 获得元素操作

```c
#define OK 1

#define ERROR 0

#define TRUE 1

#define FALSE 0

typedef int Status;

Status GetELem( SqList L, int i, ElemType *e )

{

	if ( L.length == 0 || i < 1 || i > L.length ){
        return ERROR;
    }

	*e = L.data[i-1];

	return OK;

}
```

原理：存储器中的每个存储单元都有自己的编号，这个编号称为地址。

​			LOC(i) = LOC(1) + (i-1)*c

性能：Time----O(1)

