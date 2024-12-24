# Ch7-Design and Implementation
## SOLID (给例子问违反了哪个)
### Single Responsibility Principle (每个类只能有一个责任)
- **Each class should have only one responsibility**, meaning it should do one thing and do that thing well.
### Open Closed Principle (向扩展开放，向更改关闭)
- Software components should be open for extension but closed for modification.
### Liskov Substitution Principle (子类型必须能够完全替换其父类型！)
- Subtypes must be substitutable for their base types without having to alter the base type.
### Interface Segregation Principle (使用接口的对象可以自由选择使用的内容)
- Clients should not be forced to depend on properties and methods that they do not use.
### Dependency Inversion Principle (高层模块与底层模块分离，使它们都依赖于抽象，而不是具体实现)
- High-level modules should not depend on low-level modules. Both should depend on abstractions.
- Abstractions should not depend on details. Details should depend on abstractions.

## Design Patterns

![image](https://github.com/user-attachments/assets/331a16d2-f73f-4760-9c7f-986115266876)

### 1. **Singleton（单例模式）**
- **概念**：单例模式确保一个类只有一个实例，并提供全局访问点来访问该实例。

- **适用情况**：当程序中的某个类应该仅有一个实例时，适用于需要共享资源或管理全局状态的情况，例如数据库连接等。

![image](https://github.com/user-attachments/assets/73efd191-1dee-42f9-a4e8-1ba7b82bea60)
![image](https://github.com/user-attachments/assets/1712dcc7-25bd-4e50-9cc2-2838dc98d369)

### 2. **Factory Method（工厂方法模式）**
- **概念**：工厂方法模式为创建对象提供了一个接口，但允许子类决定实例化哪一个类。

- **适用情况**：当一个类无法预见它将要创建哪些类的实例时，或当子类需要改变对象的类型时，可以使用工厂方法模式来封装对象创建逻辑。

![image](https://github.com/user-attachments/assets/083ede68-1284-42a0-9b9f-5575b0458216)
![image](https://github.com/user-attachments/assets/bc53cdff-66f1-4c8f-baab-b17159d96387)
![image](https://github.com/user-attachments/assets/0faee92f-6489-4ca2-ae8c-8af39cfc8a38)


### 3. **Adapter（适配器模式）**
- **概念**：适配器模式是一种结构型设计模式，用于使得接口不兼容的对象可以协作。
  
- **适用情况**：当想要使用某个现有类，但其接口与其他代码不兼容时，适配器模式可以帮助调整接口，使其兼容。
  
![image](https://github.com/user-attachments/assets/638f7495-0f01-4b6c-9df1-1cbc4a6f5775)

### 4. **Facade（外观模式）**
- **概念**：外观模式是一种结构型设计模式，通过提供一个简化的接口来封装复杂系统或多个类的接口。
  
- **适用情况**：当系统变得复杂，包含多个子系统类时，使用外观模式可以提供一个简单的接口，简化客户端的使用。
  
![image](https://github.com/user-attachments/assets/6d720d66-3f51-482e-a506-bdf6e91017b0)

### 5. **Observer（观察者模式）**
- **概念**：观察者模式是一种行为型设计模式，允许定义一种订阅机制，通知多个对象某一事件的发生。
  
- **适用情况**：当多个对象需要同时响应另一个对象的状态变化时，适用于一对多的关系，比如事件监听和通知机制。
  
![image](https://github.com/user-attachments/assets/53965174-ca1e-4a35-8c43-2c347606568f)
![image](https://github.com/user-attachments/assets/3dbc74cd-33ac-4a08-adee-8218c1734171)
![image](https://github.com/user-attachments/assets/f89ad63f-5879-442e-a221-297b88394434)
![image](https://github.com/user-attachments/assets/a7fb50b6-d58b-44de-8861-fc747fde9900)

### 6. **Strategy（策略模式）**
- **概念**：策略模式是一种行为型设计模式，用于定义一系列算法，将每个算法封装在独立的类中，并使得它们可以互换。
  
- **适用情况**：当需要根据不同的情境切换算法时，策略模式允许将算法封装在类中，通过上下文对象来选择执行的算法。
  
![image](https://github.com/user-attachments/assets/405fee9e-d9da-4688-bb51-2257610df1ed)
![image](https://github.com/user-attachments/assets/99ba9a86-9403-473f-8d34-3037db6ea305)

## Refactoring(概念和目的)

A systematic process of improving code without adding new functionality. 

It involves transforming messy code into clean, simple, and more maintainable design.

### Purpose:

- Makes software development more predictable and enhances the quality of the resulting product. 
- Managing technical debt by eliminating poor practices.

## Reuse Levels (四个等级要背)
### The abstraction level
- At this level, you don’t reuse software directly but use knowledge of successful abstractions in the design of your software.
### The object level (复用对象)
- At this level, you directly reuse objects from a library rather than writing the code yourself.
### The component level (复用的对象和对象类的集合)
- Components are collections of objects and object classes that you reuse in application systems.
### The system level (复用整个系统)
- At this level, you reuse entire application systems.

## Open Source Licensing
| **许可证**   | **是否强制开源衍生作品** | **是否允许闭源使用** | **适用场景**                             |
|--------------|--------------------------|---------------------|-----------------------------------------|
| **GPL**      | 是                       | 否                  | 如果你希望保护代码的开源性，并强制所有衍生作品也保持开源            |
| **LGPL**     | 仅库部分强制             | 是                  | 如果你的项目是一个库，想要广泛传播，但又希望允许商业闭源软件使用          |
| **BSD**      | 否                       | 是                  | 如果你想最大限度地推广你的代码，而不关心使用者是否开源          |
