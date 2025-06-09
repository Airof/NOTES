## How GCC Works.

1. **Preprocessing** (`cpp`)  
	- Processes directives like `#include` and `#define`.
    
2. **Compilation**  
    - Translates preprocessed source code into assembly code.
    
3. **Assembly**  
    - Converts assembly code into machine code, producing object files (`.o`).
    
4. **Linking**  
    - Combines object files and libraries into a final executable.

```bash
gcc myprogram.c -o myprogram
```
