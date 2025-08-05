# C++ Module 04 - Subtype Polymorphism, Abstract Classes, and Interfaces

## 🧠 Overview

This module introduces **runtime polymorphism**, **abstract classes**, and **interface-like structures** in C++. It reinforces your understanding of object-oriented programming principles such as inheritance, dynamic dispatch, and deep copying. All code must comply with the **C++98 standard**.

---

## 🧪 Exercises Summary

### **ex00 - Polymorphism**
- Create a base class `Animal` with a virtual method `makeSound()`.
- Create derived classes `Dog` and `Cat`, overriding `makeSound()` and setting `type`.
- Implement a `WrongAnimal` and `WrongCat` to show the effect of missing virtual methods.
- ✅ Must demonstrate **dynamic dispatch**.

### **ex01 - Brain Management**
- Add a `Brain` class with 100 `std::string` ideas.
- `Dog` and `Cat` now contain a `Brain*`.
- Must implement **deep copies** in copy constructors and assignment operators.
- Create and destroy arrays of animals to check for **memory leaks**.

### **ex02 - Abstract Animal**
- Make `Animal` abstract by turning `makeSound()` into a **pure virtual function**.
- Prevent instantiation of base `Animal` objects.
- Program should still behave exactly like ex01.

### **ex03 - Interface & Materia System**
- Implement an interface-like base class `AMateria` with:
  - `clone()` (pure virtual)
  - `use()` (virtual)
- Create derived classes `Ice` and `Cure`.
- Implement:
  - `ICharacter` interface
  - `Character` class (with 4-slot inventory)
  - `IMateriaSource` interface
  - `MateriaSource` class (learns and creates Materia by type)
- Demonstrate use of interface-based programming and **composition**.

---

## ⚙️ Requirements

- Comply with C++98
- Use `-Wall -Wextra -Werror -std=c++98`
- No use of:
  - `printf`, `malloc`, `free`
  - STL containers or `<algorithm>`
  - `using namespace` or `friend`
- Implement **Orthodox Canonical Form**:
  - Default constructor
  - Copy constructor
  - Copy assignment operator
  - Destructor

---

## 🧼 Memory & Design

- No memory leaks allowed (`new` → `delete`)
- All resources (Brain, Materia, etc.) must be properly managed
- Use **include guards** in all headers

---

## 💡 Tips

- Add destructors with visible output to track object lifecycle
- Write comprehensive tests beyond what's shown in the subject
- Ensure deep copies (especially for `Brain` and `Character` inventories)
- Avoid using raw pointers directly in interfaces — clone when necessary

---

Made with ❤️ by [`ghwa`](mailto:ghwa@student.42.fr)
