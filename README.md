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

# Matrix Operations-Diagonal Matrix Elements Printer 🧮

This Python program reads a matrix of any size from the user and prints **only the diagonal elements**, leaving other elements blank in the output.

## 📌 Aim

To write a Python program that prints only the diagonal elements of a given matrix.

## 🧠 Algorithm

1. Read the number of rows and columns from the user.
2. Initialize an empty matrix of size `rows × columns`.
3. Populate the matrix with user input.
4. Display the full matrix.
5. Iterate through the matrix and:
   - If `i == j`, print the element (main diagonal).
   - Else, print a blank space.
6. Print a newline after each row.

## 🖥️ Program
      rows = int(input())
      columns = int(input())
      matrix = [[0]*columns for row in range(rows)]
      for i in range(rows):
          lines = list(map(int, input().split()))
          for j in range(columns):
              matrix[i][j] = lines[j]
      print(matrix)
      for i in range(rows):
          for j in range(columns):
              if(i==j):
                  print(matrix[i][j],end=" ")
              else:
                  print(' ',end=" ")
          print()

### Output:
<img width="1173" height="325" alt="image" src="https://github.com/user-attachments/assets/b2dfaf22-222b-4805-a69b-8f52b1a059af" />

## Result
Thus the program executed successfully

# # ➖ Matrix Operations-Matrix Subtraction in Python

## 🎯 AIM:
To write a Python program that reads two matrices from the user and performs matrix subtraction.

---

## 🧠 ALGORITHM:

1. **Start**
2. Create variables `r` and `c` for rows and columns
3. Get the values of `r` and `c` from the user
4. Define a function `create_matrix(n, m)` to:
   - Prompt user for each matrix element
   - Append each row to form a complete matrix
5. Call the `create_matrix()` function twice to read two matrices `A` and `B`
6. Define a loop to subtract the elements of matrix `B` from matrix `A`
7. Store the result in a new matrix `C`
8. Print the resulting matrix `C`
9. **Stop**

---

## 💻 PROGRAM:
        def create_matrix(n,m):
            M=[]
            for i in range(n):
                row=[]
                for j in range(m):
                    x=int(input())
                    row.append(x)
                M.append(row)
            return M 
        r,c=input().split()
        A=create_matrix(int(r),int(c))
        B=create_matrix(int(r),int(c))
        C=[]
        for i in range(int(r)):
            R=[]
            for j in range(int(c)):
                item=A[i][j]-B[i][j]
                R.append(item)
            C.append(R)
        print(A)
        print(B)
        print(C)

## OUTPUT:
<img width="752" height="802" alt="image" src="https://github.com/user-attachments/assets/9e05537d-8a31-4eac-9596-6805bc83ac71" />

## RESULT:
Thus, the program has been execueted successfully.

# 🧮 SORTING ALGORITHMS: Insertion Sort Using a Class

This program demonstrates how to implement the **Insertion Sort algorithm** using a Python class. It allows the user to input a list of numbers, sorts them using the insertion sort technique, and displays the sorted list.

---

## 🎯 Aim

To develop a Python class with functions to:
- Create a list of integers
- Sort it using the **Insertion Sort** algorithm
- Display the sorted list

---

## 🧠 Algorithm

1. **Start the program**
2. **Define a class** `InsertionSorter`
3. Inside the class:
   - `create_list()`:
     - Read number of elements
     - Store them in a list
   - `insertion_sort()`:
     - Iterate from the second element to the end
     - Move elements greater than the key to one position ahead
     - Insert the key at the correct position
   - `print_list()`:
     - Print the sorted list
4. **Create an object** of the class
5. **Call** the methods in order: `create_list()`, `insertion_sort()`, and `print_list()`
6. **End the program**

---

## 💻 PROGRAM:

        class Numbers:
            def __init__(self, N=0):
                self.N = int(input())
            def create_list(self):
                self.L=[]
                for i in range(self.N):
                    x=int(input())
                    self.L.append(x)
            def sorting(self):
                for i in range(self.N):
                    mi=i
                    for j in range(i+1,self.N):
                        if self.L[j]<self.L[mi]:
                            mi=j
                    (self.L[i],self.L[mi])=(self.L[mi],self.L[i])
            def print_List(self):
                for i in range(self.N):
                    print(self.L[i])

## OUTPUT:
<img width="614" height="525" alt="image" src="https://github.com/user-attachments/assets/b78633df-25db-4c6e-8b78-5ef5ad5c0b44" />

## RESULT:
Thus, the program has been execueted successfully.
