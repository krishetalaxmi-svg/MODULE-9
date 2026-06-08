# 🧾 List Comprehension:Generates all even numbers between 200 and 300
## 🎯 AIM:
To write a Python class-based program that generates all even numbers between 200 and 300 using **list comprehension**, and stores them in a list.

---

## 🧠 ALGORITHM:

1. **Start**
2. Create a class named `program`
3. Create variables `a`, `b`, and `c` to represent:
   - `a`: Lower limit
   - `b`: Step value
   - `c`: Upper limit
4. Initialize the values using a constructor `__init__`
5. Define a method `display()` that uses **list comprehension** to store even numbers
6. Print the resulting list of even numbers
7. **Stop**

---

## 💻 PROGRAM:
      L=[]
      n=int(input())
      for i in range(n):
          x=int(input())
          L.append(x) 
      ODD=[x for x in L if x%2!=0]
      EVEN=[x for x in L if x%2==0]
      print(L)
      print(ODD)
      print(EVEN)

## OUTPUT:
<img width="1170" height="508" alt="image" src="https://github.com/user-attachments/assets/020461aa-4d3c-4c94-bf89-f3da2d4f86ad" />

## RESULT:
Thus the program executed successfully

# 🧮 List Comprehension:Transpose of Matrix 

## 🎯 AIM:
To write a Python program to compute the **transpose** of a matrix using **list comprehension**.

---

## 🧠 ALGORITHM:

1. **Start**
2. Create variables `r` and `c` to represent the number of rows and columns of the matrix.
3. Get the values of `r` and `c` from the user.
4. Define a function `create(r, c)` to create the matrix by reading the elements from the user.
5. Use **list comprehension** to calculate the transpose of the matrix.
6. Print the transposed matrix.
7. **Stop**

---

## 💻 PROGRAM:
    def read_matrix(r,c):
        matrix = [[0]*c for row in range(r)]
        for i in range(r):
            lines = list(map(int, input().split()))
            for j in range(c):
                matrix[i][j] = lines[j]
        return matrix
    def print_matrix(M):
        print("Matrix:")
        for i in range(len(M)):
            for j in range(len(M[0])):
                print(M[i][j],end=" ")
            print()
    def transpose(M):
        result = [[0]*(len(M)) for rows in range(len(M[0]))]
        for i in range(len(M)):
            for j in range(len(M[0])):
                result[j][i] = M[i][j]
        return result

## OUTPUT:
<img width="1168" height="476" alt="image" src="https://github.com/user-attachments/assets/4012cf00-6cae-43d3-8914-5b02f77b6f69" />

## RESULT:

Thus the program executed successfully
