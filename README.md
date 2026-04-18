# Programming Fundamentals I — Lab 13

## Sphere

**Due Date:** May 5, 2026 @ 11:59 p.m.

**Submission:** Push to GitHub repository + Submit link to Blackboard

---

## 📋 Overview

You've already worked with two-dimensional shapes like `Circle`. Now it's time to extend that thinking into three dimensions. In this lab, you'll design and implement a `Sphere` class from scratch — field, constructors, and methods — and then put it to work in a separate demo program.

**Learning Objectives:**
- Write and structure a custom Java class with a field, constructors, and methods
- Use a UML class diagram as a blueprint for implementation
- Instantiate objects and invoke methods on them
- Understand the separation between a class definition and a class driver across two files

---

## 🚀 Getting Started with GitHub Codespaces

### Initial Setup
1. **Accept the assignment** via the GitHub Classroom link provided
2. **Open your repository** in GitHub Codespaces:
   - Click the green "**Code**" button
   - Select "**Codespaces**" tab
   - Click "**Create codespace on main**"
3. **Wait for the environment to load** (this may take 1–2 minutes on first launch)
4. **Explore your workspace** — on the left side you'll see the file explorer with:
   - `README.md` (this file)
   - `Cube.java` — in-class starter file
   - `CubeTester.java` — in-class tester file

**Note:** You will create `Sphere.java` and `SphereDemo.java` yourself — these files do not exist in the repository yet.

---

## 📝 Part 1: In-Class Activity — The Cube Class (Participation Points)

### Background: Classes, Objects, and 3D Shapes

In addition to representing two-dimensional shapes with classes like `Circle` or `Rectangle`, we can expand our thinking to three-dimensional shapes. A **class** acts as a blueprint: it defines the data an object holds (its *fields*) and the behaviors it can perform (its *methods*).

A key thing to understand: when you write a class, you are defining a *type*. When you write a tester or demo program, you are *using* that type by creating objects and calling methods on them. These two responsibilities live in **separate files** — and that's the structure you'll follow for both the in-class activity and the main lab.

### The Cube Class

Use the UML class diagram below as your blueprint for `Cube.java`:

```
┌─────────────────────────────┐
│            Cube             │
├─────────────────────────────┤
│ - side: double              │
├─────────────────────────────┤
│ + Cube()                    │
│ + Cube(double)              │
│ + getSide(): double         │
│ + setSide(double): void     │
│ + getSurfaceArea(): double  │
│ + getVolume(): double       │
└─────────────────────────────┘
```

The diagram tells you everything you need: the field name and type, the constructors and their parameters, and each method with its return type. Method names are intentional and descriptive — let them guide your thinking about what each one should do.

### Instructions

**In `Cube.java`**, implement the field, both constructors, and all methods shown in the UML diagram.

**In `CubeTester.java`**, write a `main` method that:
1. Creates a `Cube` object using one of the constructors
2. Prints the side length, surface area, and volume
3. Updates the side length using the setter
4. Prints the new side length, surface area, and volume

### How to Compile and Run

```bash
# Compile both files together:
javac Cube.java CubeTester.java

# Run the tester:
java CubeTester
```

💡 **Remember:** Take a screenshot of your terminal output and add it to your repository (drag and drop into the file explorer on the left).

---

## 🔬 Part 2: Main Lab Assignment — Sphere

Create two files:
- `Sphere.java` — the class definition
- `SphereDemo.java` — the program that uses it

Include comments describing your program's purpose and each method's role — comments are a significant part of the grade.

The steps below build the class piece by piece before moving to the demo program.

### UML Class Diagram for Sphere

Use this diagram as your blueprint for `Sphere.java`:

```
┌─────────────────────────────┐
│           Sphere            │
├─────────────────────────────┤
│ - radius: double            │
├─────────────────────────────┤
│ + Sphere()                  │
│ + Sphere(double)            │
│ + getRadius(): double       │
│ + setRadius(double): void   │
│ + getSurfaceArea(): double  │
│ + getVolume(): double       │
└─────────────────────────────┘
```

### Step 1 — Declare the field

**What this step accomplishes:** gives every `Sphere` object a place to store its radius.

Declare the `radius` field as shown in the UML diagram.

---

### Step 2 — Implement the constructors

**What this step accomplishes:** defines two ways a `Sphere` object can be created.

- **No-args constructor** — creates a sphere with a sensible default radius of **1**
- **Parameterized constructor** — accepts a radius value at the time of creation and stores it in the field

---

### Step 3 — Implement the getter and setter

**What this step accomplishes:** allows other code to read and update the stored radius after an object has been created.

- **`getRadius()`** — returns the current value of the radius field
- **`setRadius(double newRadius)`** — updates the radius field to the value passed in

---

### Step 4 — Implement the calculation methods

**What this step accomplishes:** computes geometric properties of the sphere using the stored radius.

- **`getSurfaceArea()`** — returns the surface area using the formula:  
  A = 4 × π × r²

- **`getVolume()`** — returns the volume using the formula:  
  V = (4/3) × π × r³

💡 **Hint:** Java's `Math` class provides both a constant for π and a method for raising a value to a power — look these up before you start.

---

### Step 5 — Implement `main` in SphereDemo

**What this step accomplishes:** demonstrates that all parts of the `Sphere` class work correctly together.

In `SphereDemo.java`, write a `main` method that:
1. Constructs a `Sphere` object with a radius of **5**
2. Prints the radius, surface area, and volume
3. Changes the radius to **7.5** using the setter
4. Prints the updated radius, surface area, and volume

Each printed line should include a descriptive label so the output is clear to the reader.

---

## Example Output

```
The radius of the sphere is 5.0
The surface area of the sphere is 314.1592653589793
The volume of the sphere is 523.5987755982989
The radius of the sphere is 7.5
The surface area of the sphere is 706.8583470577034
The volume of the sphere is 1767.1458676442585
```

---

## 📊 Grading Criteria (100 points)

| Component | Points |
|---|---|
| **Comments describing this program** | 5 |
| **`radius` field** | 3 |
| **Constructors** | **16** |
| &nbsp;&nbsp;&nbsp;No-args constructor | 8 |
| &nbsp;&nbsp;&nbsp;Parameterized constructor | 8 |
| **`getRadius()` method** | 4 |
| **`getSurfaceArea()` method** | 15 |
| **`getVolume()` method** | 15 |
| **`setRadius()` method** | 4 |
| **`main` method** | **30** |
| &nbsp;&nbsp;&nbsp;Constructing `Sphere` object | 5 |
| &nbsp;&nbsp;&nbsp;Printing initial radius, surface area, and volume | 9 |
| &nbsp;&nbsp;&nbsp;Setting the new radius | 4 |
| &nbsp;&nbsp;&nbsp;Printing updated radius, surface area, and volume | 12 |
| **Total** | **100** |

---

## 🛠️ How to Compile and Run

```bash
# Compile both files:
javac Sphere.java SphereDemo.java

# Run the demo:
java SphereDemo
```

---

## 📸 Screenshots

Please upload at least one screenshot of your terminal output to your repository (drag and drop into the file explorer on the left).

---

## ✅ Submitting Your Work

1. Commit and push your changes using the Source Control panel.
2. Verify on GitHub that your latest commit is present and your filenames follow the required naming convention.
3. Submit your repository URL to Blackboard to complete the assignment.

Good luck — you're building your first 3D shape class! 🌐
