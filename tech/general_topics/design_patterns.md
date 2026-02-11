# *Design Patterns: Elements of Reusable Object-Oriented Software* by Erich Gamma, Richard Helm, Ralph Johnson, John Vlissides (Gang of Four - GoF)

## Introduction  
The *Design Patterns* book by the Gang of Four (GoF) introduces **23 reusable design patterns** that help solve common software design problems. These patterns promote **flexibility, maintainability, and reusability** in object-oriented systems.  

The book categorizes patterns into **three types**:  
1. **Creational Patterns** – Manage object creation.  
2. **Structural Patterns** – Define object composition and relationships.  
3. **Behavioral Patterns** – Govern communication between objects.  

---

## **1. Creational Patterns** (Handling Object Creation)  
These patterns provide **flexible and efficient ways to instantiate objects** while promoting loose coupling.  

### 1. **Factory Method**  
- Defines an **interface** for creating objects but lets **subclasses decide** which class to instantiate.  
- **Use case**: When a class **cannot predict** what type of objects it will need.  
- **Example**: `LoggerFactory.createLogger("file")` returns either a `FileLogger` or `ConsoleLogger`.  

### 2. **Abstract Factory**  
- Provides an interface for creating **families of related objects** without specifying concrete classes.  
- **Use case**: When an application **must support multiple environments** (e.g., Windows vs. Mac UI).  
- **Example**: `GUIFactory` creates either `WindowsButton` or `MacButton`.  

### 3. **Builder**  
- Separates **object construction from representation**, allowing step-by-step object creation.  
- **Use case**: When constructing **complex objects with many optional parameters**.  
- **Example**: `CarBuilder.setWheels(4).setColor("Red").build()`.  

### 4. **Prototype**  
- Creates objects by **cloning an existing instance** instead of instantiating new ones.  
- **Use case**: When object creation is expensive, but copying is cheap.  
- **Example**: Duplicating a graphical object in a drawing application.  

### 5. **Singleton**  
- Ensures **only one instance** of a class exists and provides a global access point.  
- **Use case**: Managing shared resources like a **database connection** or a **logging system**.  
- **Example**: `Database.getInstance()`.  

---

## **2. Structural Patterns** (Managing Object Relationships)  
These patterns define **how classes and objects are composed to form larger structures**.  

### 6. **Adapter**  
- Converts the **interface of one class into another** expected by clients.  
- **Use case**: When integrating incompatible APIs.  
- **Example**: A `USBtoEthernetAdapter` allows USB devices to work with Ethernet ports.  

### 7. **Bridge**  
- **Decouples abstraction from implementation**, allowing them to evolve independently.  
- **Use case**: When a system needs to support **multiple implementations** of an abstraction.  
- **Example**: A `RemoteControl` (`Abstraction`) that works with both `TV` and `Radio` (`Implementation`).  

### 8. **Composite**  
- Treats **individual objects and groups of objects** uniformly.  
- **Use case**: Representing **hierarchical structures** like trees (e.g., file systems, GUI components).  
- **Example**: A `Folder` can contain `Files` or other `Folders`.  

### 9. **Decorator**  
- Adds behavior **dynamically to objects** without modifying their code.  
- **Use case**: Extending functionality without subclassing.  
- **Example**: A `Coffee` object can be decorated with `Milk` and `Sugar`.  

### 10. **Facade**  
- Provides a **simplified interface** to a complex subsystem.  
- **Use case**: When working with **complicated APIs**.  
- **Example**: A `CarFacade` simplifies starting a car by hiding complex ignition steps.  

### 11. **Flyweight**  
- Reduces memory usage by **sharing common object data**.  
- **Use case**: When an application requires **a large number of similar objects**.  
- **Example**: A text editor sharing font objects instead of creating new ones for each character.  

### 12. **Proxy**  
- Provides a **placeholder for another object**, controlling access to it.  
- **Use case**: Adding security, lazy loading, or caching.  
- **Example**: A `VirtualProxy` delays object loading until needed.  

---

## **3. Behavioral Patterns** (Managing Object Communication)  
These patterns define **how objects interact and distribute responsibilities**.  

### 13. **Chain of Responsibility**  
- Passes requests along a **chain of handlers** until one handles it.  
- **Use case**: Implementing flexible request-processing workflows.  
- **Example**: A support ticket system escalating issues through different levels.  

### 14. **Command**  
- Encapsulates requests as objects, allowing **undoable operations**.  
- **Use case**: Implementing **transactional actions** in UI frameworks.  
- **Example**: `Undo/Redo` in a text editor.  

### 15. **Interpreter**  
- Defines a language grammar and **evaluates expressions**.  
- **Use case**: Building simple interpreters or scripting engines.  
- **Example**: SQL or regex parsing.  

### 16. **Iterator**  
- Provides **sequential access** to elements without exposing the underlying structure.  
- **Use case**: Iterating over collections.  
- **Example**: `ArrayList.iterator()`.  

### 17. **Mediator**  
- Centralizes communication between objects to **reduce dependencies**.  
- **Use case**: Managing UI components that interact dynamically.  
- **Example**: A `ChatRoom` where participants don’t communicate directly but through a mediator.  

### 18. **Memento**  
- Captures an object's state for **restoring it later**.  
- **Use case**: Implementing **undo/rollback functionality**.  
- **Example**: A game save system.  

### 19. **Observer**  
- Notifies dependent objects when a subject’s state changes.  
- **Use case**: Implementing event-driven programming.  
- **Example**: GUI event listeners or real-time stock updates.  

### 20. **State**  
- Allows an object’s behavior to change when its state changes.  
- **Use case**: Replacing long `if-else` chains.  
- **Example**: A traffic light with different states (`Red`, `Green`, `Yellow`).  

### 21. **Strategy**  
- Defines a **family of algorithms** and selects one at runtime.  
- **Use case**: Implementing multiple sorting strategies.  
- **Example**: A `PaymentProcessor` choosing between `CreditCard` and `PayPal`.  

### 22. **Template Method**  
- Defines a **skeleton of an algorithm** but lets subclasses implement details.  
- **Use case**: Ensuring a **common structure** across implementations.  
- **Example**: A `Game` class with `play()` but different rules for `Chess` and `Football`.  

### 23. **Visitor**  
- Allows adding new operations to objects **without modifying them**.  
- **Use case**: When extending functionality across a **hierarchy of objects**.  
- **Example**: A tax calculator visiting different product types.  

---

## **Conclusion**  
The *Design Patterns* book provides **proven solutions** to recurring software problems. The key takeaways include:  
- **Encapsulate change** using abstraction.  
- **Prefer composition over inheritance**.  
- **Loosely couple objects** to increase flexibility.  
- **Use patterns wisely**—don’t overcomplicate simple problems.  

By applying these patterns, developers can **write maintainable, scalable, and reusable software**.  

