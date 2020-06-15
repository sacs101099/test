# Markdown editor
### [1.  Scan N (take input N from user) values from user into an array. Access the array using pointer ](https://github.com/1834902551/cse214/blob/master/Lab5/1.c)
```cpp
 scanf("%d",&N);

    for(i=0; i<N; i++)
        scanf("%d",(p+i));
```
### [2.Scan values from user into an array until end of file. ](https://github.com/1834902551/cse214/blob/master/Lab5/2.c)
```cpp
for(i=0; scanf("%d",(p+i))!=EOF; i++)
        size++;

    printf("\n");

    for(i=0; i<size; i++)
        printf("%d ",*(p+i));
```

### [3.Scan values from user into an array until user input is 0 (Zero). ](https://github.com/1834902551/cse214/blob/master/Lab5/3.c)
```cpp
for(i=0; scanf("%d",(p+i))!=EOF; i++)
        if(*(p+i)==0)
            break;

    size=i;

    printf("\n");

    for(i=0; i<size; i++)
        printf("%d ",*(p+i));

```

### [4.Print entire array each element separated by space.](https://github.com/1834902551/cse214/blob/master/Lab5/4.c)
```cpp
p = &a[0];

    for(i=0; i<size; i++)
        printf("%d ", *(p+i));

```
### [5.Insert a value “X” (take input X from user) in the array at Kth (take input K from user) index and shift all other value to right. And print the whole array. ](https://github.com/1834902551/cse214/blob/master/Lab5/5.c)
```cpp
printf("Value:");
    scanf("%d",&X);

    printf("\nIndex:");
    scanf("%d",&K);

    p = &a[0];

    for (i=size; i>=K; i--)
        *(p+i) = *(p+i-1);

    size++;
```

### [6.Update Kth (take input K from user) index with the value “X” (take input X from user). And print the whole array. ](https://github.com/1834902551/cse214/blob/master/Lab5/6.c)
```cpp
printf("Value:");
    scanf("%d",&X);

    printf("\nIndex:");
    scanf("%d",&K);

    p = &a[0];

    for(i=K-1; i<size; i++)
    {
        *(p+i)=X;
        break;
    }
    printf("\n");

    for(i=0; i<size; i++)
        printf("%d ", *(p+i));
```

### [7.Search a value “X” (take input X from user) in the array and print the location if “X” found in the array otherwise print -1. ](https://github.com/1834902551/cse214/blob/master/Lab5/7.c)
```cpp
p = &a[0];

    printf("Value: ");
    scanf("%d",&X);

    for(i=0; i<size; i++)
    {
        if(*(p+i)==X)
        {
            location = i;
            temp++;
        }
    }

    if(temp==1)
        printf("%d",location);
    else
        printf("-1");
```


### [8. Delete a value from Kth index (take input K from user) from the array shift all other value to left. And print the whole array.](https://github.com/1834902551/cse214/blob/master/Lab5/8.c)
```cpp
p = &a[0];

    printf("Value: ");
    scanf("%d",&K);

    for (i=K-1; i<size; i++)
        *(p+i) = *(p+i+1);

    size--;

    for(i=0; i<size; i++)
        printf("%d ", *(p+i));
```



### [9. Find Maximum from the Array. Access the array using pointer. ](https://github.com/1834902551/cse214/blob/master/Lab5/9.c)
```cpp
max = &a[0];

    for(i=0; i<size; i++)
        printf("%d ", *(max+i));

    printf("\n");

    for(i=1; i<size; i++)
        if(*(max+i)>*max)
            *max = *(max+i);

    printf("Maximum: %d\n",*max);
```

### [10. Find Minimum from the Array. Access the array using pointer.](https://github.com/1834902551/cse214/blob/master/Lab5/10.c)
```cpp
min = &a[0];

    for(i=0; i<size; i++)
        printf("%d ",*(min+i));

    printf("\n");

    for(i=1; i<size; i++)
        if(*(min+i)<*min)
            *min = *(min+i);

    printf("Minimum: %d\n",*min);
```

### [11.Find Second Maximum from the Array. Access the array using pointer. ](https://github.com/1834902551/cse214/blob/master/Lab5/11.c)
```cpp
max = &a[0];

    for(i=0; i<size; i++)
        printf("%d ",*(max+i));

    printf("\n");

    for(i=0; i<size; i++)
    {
        if(*(max+i)>*max)
        {
            max2 = *max;
            *max = *(max+i);
        }
        else if(*(max+i)>max2 && *(max+i)<*max)
            max2 = *(max+i);
    }

    printf("Second Maxium: %d\n", max2);
```

### [12.  Find Second Minimum from the Array. Access the array using pointer.](https://github.com/1834902551/cse214/blob/master/Lab5/12.c)
```cpp
 min = &a[0];

    for(i=0; i<size; i++)
        printf("%d ",*(min+i));

    printf("\n");

    for(i=0; i<size; i++)
    {
        if(*(min+i)<*min)
        {
            min2 = *min;
            *min = *(min+i);
        }
        else if(*(min+i)<min2 && *(min+i)!=*min)
            min2 = *(min+i);
    }

    printf("%d\n", min2);
```


### [13. Calculate the summation of all elements of the given array. ](https://github.com/1834902551/cse214/blob/master/Lab5/13.c)
```cpp
p = &a[0];

    for(i=0; i<size; i++)
        printf("%d ",*(p+i));

    printf("\n");

    for(i=0; i<size; i++)
        sum += *(p+i);

    printf("%d\n", sum);
```

### [14. Copy the given array into another array. ](https://github.com/1834902551/cse214/blob/master/Lab5/14.c)
```cpp
 p = &a[0];
    q = &b[0];

    for(i=0; i<size; i++)
        printf("%d ",*(p+i));

    printf("\n");

    for(i=0; i<size; i++)
    {
        temp = *(p+i);
        *(q+i) = temp;
    }

    for(i=0; i<size; i++)
        printf("%d ",*(q+i));
```


### [15. Reverse the given array within the same array. ](https://github.com/1834902551/cse214/blob/master/Lab5/15.c)
```cpp
 p = &a[0];
    q = &b[0];

    for(i=0; i<size; i++)
        printf("%d ",*(p+i));

    printf("\n");

    for(i=0; i<=size; i++)
    {
        temp = *(p+size-i);
        *(q+i-1) = temp;
    }

    for(i=0; i<size; i++)
        printf("%d ",*(q+i));
```


### [16.  Declare another array with ten (10) values and compare both arrays whether they are same or not.](https://github.com/1834902551/cse214/blob/master/Lab5/16.c)
```cpp
 p = &a[0];
    q = &b[0];

    for(i=0; i<size; i++)
        printf("%d ",*(p+i));

    printf("\n");

    for(i=0; i<size; i++)
        printf("%d ",*(q+i));

    for(i=0; i<size; i++)
        if(*(p+i)==*(q+i))
            same++;

    if(same==size)
        printf("\nTwo array are same\n");
    else
        printf("\nTwo array are not same\n");
```

### [17. Declare another array with five (5) values and merge two arrayinto one array.](https://github.com/1834902551/cse214/blob/master/Lab5/17.c)
```cpp
 p = &a[0];
    q = &b[0];

    for(i=0; i<size_a; i++)
        printf("%d ",*(p+i));

    printf("\n");

    for(i=0; i<size_b; i++)
        printf("%d ",*(q+i));

    size = size_a + size_b;

    for(i=size_a, j=0; i<=size; i++,j++)
       *(p+i)=*(q+j);

    printf("\n");

    for(i=0; i<size; i++)
        printf("%d ",*(p+i));
```

### [18.  Merge the Elements of two Sorted Array.](https://github.com/1834902551/cse214/blob/master/Lab5/18.c)
```cpp
 p = &a[0];
    q = &b[0];

    for(i=0; i<size_a; i++)
        printf("%d ",*(p+i));

    printf("\n");

    for(i=0; i<size_b; i++)
        printf("%d ",*(q+i));

    size = size_a + size_b;

    for(i=size_a, j=0; i<=size; i++,j++)
    {
        size_a++;
        *(p+i)=*(q+j);
    }

    printf("\n");

    for(i=0; i<size; i++)
        printf("%d ",*(p+i));

    printf("\n");

    for(i=0; i<size; i++)
    {
        for(j=i+1; j<size; j++)
        {
            if(*(p+i)>*(p+j))
            {
                temp = *(p+i);
                *(p+i) = *(p+j);
                *(p+j) = temp;
            }
        }
    }

    for(i=0; i<size; i++)
        printf("%d ",*(p+i));

    printf("\n");
```

### [19. Split an Array after Kth (take input K from user) elements into two different Arrays. ](https://github.com/1834902551/cse214/blob/master/Lab5/19.c)
```cpp
 p = &a[0];
    q = &b[0];
    r = &c[0];

    scanf("%d",&K);

    for(i=0; i<size_a; i++)
        printf("%d ",*(p+i));

    for(i=0; i<size_a; i++)
    {
        if(i<K)
        {
            *(q+i) = *(p+i);
            size_b++;
        }
        else
        {
            *(r+j++) = *(p+i);
            size_c++;
        }
    }

    printf("\n");

    for(i=0; i<size_b; i++)
        printf("%d ",*(q+i));

    printf("\n");

    for(i=0; i<size_c; i++)
        printf("%d ", *(r+i));
```

### [20. Cyclically permute the elements of an array. ](https://github.com/1834902551/cse214/blob/master/Lab5/20.c)
```cpp
 p = &a[0];
    for(i=0; i<size; i++)
        printf("%d ",*(p+i));

    printf("\n");

    *(p+size) = *p;

    for (i=0; i<size; i++)
        *(p+i) = *(p+i+1);

    for(i=0; i<size; i++)
        printf("%d ",*(p+i));
```
