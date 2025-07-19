
# C Fundamentals

## course
### 1.
- **syntax** 
- **variable** 
- **data types**
- **operations**
- **scanf** / **printf**
### 2. 
- **if** **else** 
- **for** 
- **while** 
- **do-while**
- **switch-case**

- lib

## Project
???


GPT:
- Take inputs: student names, IDs, grades.
- Calculate and display averages, pass/fail counts.
- Implement basic menus using `switch-case`.
- Practice loops, conditions, I/O clearly





# C Intermediate

## course


### 1.
- **Arrays** (1D)
- **String manipulation**
- **Pointer basics**

### 2. 
 - **Arrays** (2D)
 - **pointer to pointer** 
 - **Array of strings** 

### 3. 
 - **Structs**
- **Typedef**,
- **Enums**

### 4.
- **pointer to function**
- **Union vs. Struct** (quick intro)
-  **nested structs**
### 5. 
- **multi-file structure**
- **STDIN**/**STDOUT**

## Project


# C Mastery

## course

- **ESP fundamentals**
- **CLI Libraries** **ncurses (PDCurses for Windows)**
- **GUI**?
- **Multi-Threading**
- **forking process**

## Project







# others

1. **Memory Management**:
    
    - Stack vs. Heap, memory leaks, `valgrind` basics
        
2. **Advanced Pointers**:
    
    - Function pointers (for callbacks), `void*`, pointer arithmetic
        
3. **Error Handling**:
    
    - Return codes vs. `errno`, defensive programming
        
4. **Performance Basics**:
    
    - Algorithm complexity (O-notation intro), cache locality
```mermaid
graph LR
    A[Fundamentals] --> B[Intermediate]
    B --> C[Mastery]
    
    A --> A1["stdio.h"]
    A --> A2["stdlib.h"]
    A --> A3["string.h"]
    A --> A4["math.h"]
    
    B --> B1["getopt.h"]
    B1 --> B2["ncurses"]
    B2 --> B3["readline"]
    B1 --> B4["SQLite"]
    B4 --> B5["cJSON"]
    
    C --> C1["libcurl"]
    C --> C2["PCRE"]
    C --> C3["pthread"]
    C --> C4["libusb"]
    C --> C5["ESP-IDF"]
```


