# Programming Fundamentals I — Lab 13

## Sphere

Due date: December 6, 2023 at 11:59 p.m.

---

## Purpose

This lab builds on the Circle class by introducing the Sphere class. This is the most complex ending lab of the semester, so attention to detail is important. This lab focuses on the following concepts:

• Writing your own custom class  
• Constructing an object of a custom class  
• Calling methods on an object

---

## In‑Class 13: The Cube Class

In addition to representing two-dimensional shapes with classes like Circle or Rectangle, we can expand to three-dimensional shapes. Let's consider a Cube class with the following UML class diagram:

```
┌─────────────────┐
│      Cube       │
├─────────────────┤
│ - side: double  │
├─────────────────┤
│ + Cube()        │
│ + Cube(double)  │
│ + getSide(): double │
│ + setSide(double): void │
│ + getSurfaceArea(): double │
│ + getVolume(): double │
└─────────────────┘
```

Every object of Cube will need a \`side\` field to specify the dimensions of that cube. The class has two constructors: a no-args constructor and a parameterized constructor. To get certain properties of Cube objects, the \`getSurfaceArea\` and \`getVolume\` methods have been included. And to set the side of a Cube object after construction, the \`setSide\` method has been included.

### Important: Two-File Structure

Just like the main Lab 13 task, this in-class exercise uses **TWO separate files**:

1. **Cube_FirstName_LastName.java** - Contains the Cube class definition (fields, constructors, and methods)
2. **CubeTester_FirstName_LastName.java** - Contains the main method to test the Cube class

This structure mirrors exactly what you'll do in Lab 13 with \`Sphere.java\` and \`SphereDemo.java\`.

### Instructions

1. In \`Cube_FirstName_LastName.java\`, implement all the fields, constructors, and methods shown in the UML diagram above.
2. In \`CubeTester_FirstName_LastName.java\`, write code in the main method to:
   - Create a Cube object using one of the constructors
   - Call and print the results of \`getSide()\`, \`getSurfaceArea()\`, and \`getVolume()\`
   - Use \`setSide()\` to change the cube's side length
   - Print the new side, surface area, and volume

### How to Compile and Run the In-Class Exercise

```bash
# Compile both files together:
javac Cube_FirstName_LastName.java CubeTester_FirstName_LastName.java

# Run the tester program:
java CubeTester_FirstName_LastName
```

---

## Lab 13 Task: Sphere

Create a project called \`Sphere_FirstName_LastName\` or \`Lab13_FirstName_LastName\`. The program will consist of two files: \`Sphere.java\` and \`SphereDemo.java\`. Remember to include comments summarizing the program in the files that you implement.

### UML Class Diagram for Sphere

Review the UML class diagram provided below for the Sphere class. Keep in mind that this diagram specifies the fields and methods of the class, including the data types of fields and parameters and the return types of methods.

```
┌─────────────────────────┐
│        Sphere           │
├─────────────────────────┤
│ - radius: double        │
├─────────────────────────┤
│ + Sphere()              │
│ + Sphere(double)        │
│ + getRadius(): double   │
│ + setRadius(double): void │
│ + getSurfaceArea(): double │
│ + getVolume(): double   │
└─────────────────────────┘
```

### Step 1 — Declare the radius field

In the \`Sphere.java\` class, declare the \`radius\` field specified in the UML class diagram.

### Step 2 — Implement the constructors

In the \`Sphere.java\` class, write method definitions for both constructors:

- **No-args constructor**: Sets the radius to the value of 1.
- **Parameterized constructor**: Takes one parameter \`newRadius\` and sets the radius to the value of \`newRadius\`.

### Step 3 — Implement the getter and setter methods

Implement the following methods:

- **getRadius()**: Returns the current radius of the sphere.
- **setRadius(double newRadius)**: Sets the radius to the value of \`newRadius\`.

### Step 4 — Implement the calculation methods

Implement the following methods:

- **getSurfaceArea()**: Returns the surface area of the sphere, calculated using the formula:  
  A = 4 × π × r²

- **getVolume()**: Returns the volume of the sphere, calculated using the formula:  
  V = 4/3 × π × r³

### Step 5 — Implement the main method in SphereDemo.java

In the \`main\` method of \`SphereDemo.java\`, do the following:

1. Construct an object of the Sphere class with the radius set to 5.
2. Use the \`getRadius\` method to print the radius of the Sphere object to the console. Include a statement indicating this is the radius.
3. Use the \`getSurfaceArea\` method to print the surface area of the Sphere object to the console. Include a statement indicating this is the surface area.
4. Use the \`getVolume\` method to print the volume of the Sphere object to the console. Include a statement indicating this is the volume.
5. Use the \`setRadius\` method to change the radius to 7.5.
6. Use the \`getRadius\` method to print the new radius.
7. Use the \`getSurfaceArea\` method to print the surface area with the new radius.
8. Use the \`getVolume\` method to print the volume with the new radius.

---

## Example Output

The following is the expected output from the main method:

```
The radius of the sphere is 5.0
The surface area of the sphere is 314.1592653589793
The volume of the sphere is 523.5987755982989
The radius of the sphere is 7.5
The surface area of the sphere is 706.8583470577034
The volume of the sphere is 1767.1458676442585
```

---

## Grading Criteria (100 points)

Make sure you have the following in your program:

• Comments describing this program — 5 points

• The field of the Sphere class — 3 points

• The two constructors of the Sphere class — 16 points
   - No-args constructor — 8 points
   - Parameterized constructor — 8 points

• The getRadius method of the Sphere class — 4 points

• The getSurfaceArea method of the Sphere class — 15 points

• The getVolume method of the Sphere class — 15 points

• The setRadius method of the Sphere class — 4 points

• The main method of the program — 30 points
   - Constructing Sphere object — 5 points
   - Printing initial radius, surface area, and volume — 9 points
   - Setting new radius — 4 points
   - Printing new radius, surface area, and volume — 12 points

---

## How to Run

From a terminal in VS Code (macOS, zsh):

```bash
# Compile both files:
javac Sphere.java SphereDemo.java

# Run the demo program:
java SphereDemo
```

---

## Screenshots

Please upload at least one screenshot of your console output showing the expected output as demonstrated in the example above.

---

## Submitting Your Work

1. Commit and push your changes using Source Control panel.
2. Verify on GitHub that your latest commit is present and your filenames follow the required convention.
3. Submit your repository URL to Blackboard to complete the assignment.

Good luck with the final lab of the semester! 🌐
