Here's the `README.md` file with the structure you requested:

```markdown
## 1. What are the main principles of Object-Oriented Programming?

### Answer:
The four main principles of OOP are:
1. **Encapsulation**: Wrapping data (attributes) and methods (functions) into a single unit or class, restricting direct access to some of the object’s components, and providing controlled access via methods.
2. **Abstraction**: Hiding the complex implementation details and showing only the essential features of an object.
3. **Inheritance**: Mechanism where one class inherits properties and behaviors (methods) from another class. This promotes code reusability.
4. **Polymorphism**: The ability of objects of different types to be accessed through the same interface. It allows a single method to have different implementations in different contexts.

---

## 2. What is the difference between a class and an object?

### Answer:
- **Class**: A blueprint or template for creating objects. It defines properties and methods but does not hold any values itself.
- **Object**: An instance of a class. It is a concrete entity that holds actual values and can interact with other objects.

Example:
```javascript
class Car {
    constructor(brand, model) {
        this.brand = brand;
        this.model = model;
    }
}

const myCar = new Car("Toyota", "Corolla"); // 'myCar' is an object of the 'Car' class
```

---

## 3. What is the difference between method overloading and method overriding?

### Answer:
- **Method Overloading**: Occurs when two or more methods in the same class share the same name but differ in the number or types of parameters. JavaScript does not natively support method overloading.
- **Method Overriding**: Happens when a subclass provides a specific implementation of a method that is already defined in its superclass. The method in the subclass overrides the method in the superclass.

Example of Method Overriding:
```javascript
class Animal {
    speak() {
        console.log("Animal makes a sound");
    }
}

class Dog extends Animal {
    speak() {
        console.log("Dog barks");
    }
}

const dog = new Dog();
dog.speak(); // Output: "Dog barks"
```

---

## 4. What is a constructor in JavaScript?

### Answer:
A constructor is a special function that is automatically called when an object is created from a class. It is used to initialize the object's properties.

Example:
```javascript
class Person {
    constructor(name, age) {
        this.name = name;
        this.age = age;
    }
}

const person1 = new Person("John", 25); 
console.log(person1.name); // Output: "John"
console.log(person1.age);  // Output: 25
```

---

## 5. What is prototypal inheritance in JavaScript?

### Answer:
In JavaScript, objects can inherit properties and methods from another object. This is known as **prototypal inheritance**. Every object in JavaScript has a prototype, which is another object that it inherits methods and properties from.

Example:
```javascript
const animal = {
    eats: true,
    walk() {
        console.log("Animal walks");
    }
};

const dog = Object.create(animal);
dog.barks = true;

console.log(dog.eats); // true (inherited from 'animal')
dog.walk(); // Output: "Animal walks"
```

---

## 6. What is the difference between classical inheritance and prototypal inheritance?

### Answer:
- **Classical Inheritance**: Found in languages like Java or C#, where classes define blueprints for creating objects, and objects are instances of these classes.
- **Prototypal Inheritance**: Used in JavaScript, where objects inherit directly from other objects. There is no concept of "classes" in a strict sense; instead, inheritance is handled through prototypes.

---

## 7. What is the difference between static and instance methods in JavaScript?

### Answer:
- **Static Methods**: Belong to the class itself and are called on the class, not on instances of the class.
- **Instance Methods**: Belong to the instances of a class and are called on individual objects.

Example:
```javascript
class MathOperations {
    static add(a, b) {
        return a + b;
    }

    subtract(a, b) {
        return a - b;
    }
}

console.log(MathOperations.add(5, 3)); // 8 (static method)
const math = new MathOperations();
console.log(math.subtract(5, 3)); // 2 (instance method)
```

---

## 8. What is the `super` keyword in JavaScript?

### Answer:
The `super` keyword is used to call the constructor or methods of a parent class. It is commonly used in classes that inherit from other classes to invoke the parent class's constructor or methods.

Example:
```javascript
class Animal {
    constructor(name) {
        this.name = name;
    }

    speak() {
        console.log(`${this.name} makes a sound`);
    }
}

class Dog extends Animal {
    constructor(name, breed) {
        super(name); // Calls the parent class constructor
        this.breed = breed;
    }

    speak() {
        console.log(`${this.name} barks`);
    }
}

const dog = new Dog("Buddy", "Golden Retriever");
dog.speak(); // Output: "Buddy barks"
```
```
