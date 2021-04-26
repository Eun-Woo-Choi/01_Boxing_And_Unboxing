# C# : About Boxing and Unboxing

### To understand _**boxing**_ and _**unboxing**_, let's first look at two types of memory storage.
<br>
There are two types of memory storage.

- **Value Type** : A data type in which the variable holds values.
                      (Integer type, real type, character type, boolean type)

- **Reference Type** : A data type that holds the location (reference) where the variable has a value instead of a value.
                                   (Array,  ArrayList, HashTable etc.)
<br>

And these are stored in two separate spaces.

- The location to store the _**value type**_ is '**Stack Memory**'.

- The location to store the **_reference type_** is '**Heap Memory**'.

<br>

### Here, _'Boxing'_ is that the data stored in the Stack memory is stored in the Heap memory.

### In contrast, _'Unboxing'_ is that data stored in the Heap memory is stored in the Stack memory.

<br>

---

### < For example : **Boxing** >

`ArrayList _arrayList = new ArrayList();`
<br>
`_arrayList.Add(100);`

![image](https://user-images.githubusercontent.com/80008824/116013087-ed067400-a636-11eb-9132-d42bd5cb481f.png)

<br>

### < Explain >

1.  `_arrayList.Add(100);` stores the integer value '100' on the **Stack**.

2.  `_arrayList.add()` is executed.

3.  The integer value stored on the **Stack** are stored at an address on the **Heap**.

<br>

---

### Unboxing is the opposite concept.

### < For example : **Unboxing** >

`int num = int.Parse(_arrayList[0]);`

![image](https://user-images.githubusercontent.com/80008824/116014020-c0089000-a63b-11eb-8c7a-c6d8fc8927b1.png)

<br>

### < Explain >

1. `_arrayList[0]` is a value stored at index 0 of the **Heap**.

2. Converts to integer type with `int.parse(_arrayList [0]);`.

3. The integer value '100' is stored in the **Stack** memory as the value of the variable 'num'.

4. The value of **Heap** memory remains and the copied value is stored on the **Stack** memory.

---

However, storing a value in the heap memory through Boxing, which is not a general method, consumes up to 20 times the time. 

Also, storing a value in the stack memory through Unboxing consumes up to 4 times the time.

These days, computers are getting better. So it may not be a big problem.

Please let me know by reply if there is anything I need to revise.
