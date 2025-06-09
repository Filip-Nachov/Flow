# How to Contribute

<<<<<<< HEAD
Thank you for considering contributing to Flow project! We appreciate your interest and support.
=======
Thank you for considering contributing to the Flow project! We appreciate your interest and support.
>>>>>>> 88b27f73de6b9d68777aeb803e40c3ad04d57a33

1. **Fork the repository**  
   Click the "Fork" button on the top right of the repository page. 

2. **Create a branch:**  
   `git checkout -b feature/ShortDescription`

3. **Make your changes**  
   - Keep commits focused and atomic.
   - Add comments and documentation as needed.

4. **Test your changes**  
   - Make sure the project builds and runs.
   - Add or update tests if applicable.

5. **Commit your changes**  
   - Use clear, descriptive commit messages.  
   - Example:  
     ```
     Add task deletion feature

     Allows users to delete tasks from the Kanban board using a new menu option.
     ```

6. **Push and open a Pull Request**  
   - Describe what your PR changes and why.
   - Reference relevant issues if applicable.

## Pull Request Checklist

- [ ] Code compiles and runs.
- [ ] Adheres to code style.
- [ ] No merge conflicts.
- [ ] All relevant tests pass.
- [ ] PR description is clear and complete.

## Reporting Issues

- Please use GitHub Issues.
- Include as much detail as possible: steps to reproduce, expected/actual behavior, OS, etc.

# Code Style

* If any of these rules are not followed, the code will not be accepted.

## Naming
- Use **camelCase** for variables and function parameters (e.g., `taskList`, `columnIndex`)
- Use **PascalCase** for struct, class, and function names (e.g., `Task`, `BoardColumn`, `AddTask()`)
- Use **ALL_CAPS_WITH_UNDERSCORES** for macros and constants (e.g., `MAX_TASKS`)
- File names should use **snake_case** (e.g., `task_board.cpp`, `kanban.hpp`)

## Formatting
- Use 4 spaces for indentation, no tabs
- Maximum line length: 150 characters (with small exceptions)
- Braces on the same line as the statement (K&R style):
  ```cpp
  if (isDone) {
      // code
  }
  ```
- Add spaces around operators and after commas
- Max of Three statement per line
    

## Declarations
- make everything `const` that can be `const`
- Prefer to declare variables close to where they are used (if possible of course)
- Prefer `auto` only when the type is obvious or not really impactful on the code performance
- Avoid global variables.


## Functions
- Functions should be small and have one purpose but can do many things that define that purpose (ideally <100 lines but the sky is the limit)
- Use **PascalCase** for function names (e.g., `AddTask()`, `GetTaskList()`)
- Prefer free functions and structs over classes and OOP except where OOP is clearly beneficial
- Pass non-trivial types by `const &` when not modifying
- Your code of functions should be easy to read and modify so avoid using comments
- Dont use much 'goto' statements, if you need to use them then you should refactor your code (unless they are really needed)

## Classes and Structs
- Use **PascalCase** for class and struct names (e.g., `Task`, `BoardColumn`)
- Use `private` and `protected` access specifiers for member variables and functions, and `public` only when necessary
- Prefer **structs** with public members for simple data
- Use **classes** for more complex data structures with private members and public member functions
- If using classes, group members: public, protected, private (in that order)
- Avoid overusing OOP features; KISS Rule (Keep It Simple, Stupid)
- Use whatever methods of OOP you want but prefer composition over inheritance

## Comments and Documentation

- Avoid unnecessary comments, code should be self-explanatory so only use the comments when really needed
- Use clear, concise comments for complex logic.
- Document file/module purpose at the top.
- Mark TODOs and FIXMEs clearly.
- use the following tags:

* `TODO: ` for things that need to be done
* `BUG/DEBUG: ` for things that are not working as expected
* `FIXME: ` for things that need to be fixed
* `HACK: ` for things that are not the best way to do it but are working

## Includes and Headers
- Use `#pragma once` on top of all header files
- Only include what you use
- Order: related header, standard library, third-party, then project headers
- Never use `using namespace` in headers (or code in general)

## STL Usage
- Prefer using STL containers (`std::vector`, `std::map`, etc.) over raw arrays.
- Use smart pointers (`std::unique_ptr`, `std::shared_ptr`) if dynamic memory is needed
- Prefer `std::string` over C-style strings (`char*`, `char[]`)
- Use pointers when needed but be careful if doing so

## Error Handling
- Check return values and handle errors gracefully
- Use error codes for simple errors, exceptions for exceptional cases
- Avoid using exceptions for regular control flow

## Miscellaneous
- Avoid magic numbers—use named constants.
- No trailing whitespace.
- Keep code self-explanatory where possible.
- Organize code into logical modules/files.

## Memory Handling
- Prefer automatic (stack) allocation
- Feel free to use whatever Data structure and algorithm you want but keep it tidy and performant
- Always release resources properly
- Avoid manual `new`/`delete` unless absolutely necessary
- if using pointers free them when not needed anymore

# Structure

This is the main structure and should be followed, if not then the changes will not be accepted

``` 
Flow
  - .github
    - CONTRIBUTING.md
    - INSTALL.md 
  - Src 
    - headers
      - main.h 
      - ...
    - main.cpp
    - ...
  - Tests
    - ...
  - README.md
  - LICENSE
  - .gitignore
  - makefile
```

Thanks for helping make this project better!
