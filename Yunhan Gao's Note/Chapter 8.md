# Ch8-Software Testing
## Defect clustering vs Pesticide paradox
### Defect clustering (缺陷往往不均匀分)
- Small number of modules containing most of the defects.
### Pesticide paradox (杀虫剂悖论)
-If the same set of test cases are executed again and again over the period of time then these set of tests are not capable enough to identify new defects in the system.

- The set of test cases needs to be regularly reviewed and revised.

## Static Testing vs Dynamic testing
### Static Testing
>**Walkthroughs (演练):** An informal review method where a small set of paper test cases is mentally executed by a group or individual, walking through the program’s logic without running the actual code.
- 演练是一种非正式的审查方法，准备一小组纸质测试用例，通过小组或个人的思维执行测试数据，走查程序逻辑，无需执行代码。

>**Inspections (检查):** A code inspection involves a group process for detecting anomalies and defects in the source code through detailed examination. It does not require system execution and can be done at any stage of development (requirements, design, configuration, test data).
- 代码检查是一种小组程序，通过详细检查源代码来检测异常和缺陷。它不需要执行系统，可以在开发的任何阶段（如需求、设计、配置数据、测试数据）进行。

**Advantages of Inspections**  
1. **Error masking**: During dynamic testing, one error may hide others. Static inspection avoids this issue as errors are detected without interaction.
   - **错误掩盖**: 动态测试中，一个错误可能掩盖其他错误，而静态检查可以避免这个问题，因为错误是单独发现的。
   
2. **Inspection without completion**: Incomplete systems can be inspected without additional costs, unlike dynamic tests that require specialized test harnesses for incomplete systems.
   - **不完整系统的检查**: 对于不完整的系统，检查可以在没有额外成本的情况下进行，而动态测试则需要为不完整部分开发专门的测试工具。

3. **Broader quality attributes**: Inspections can evaluate quality aspects beyond defects, such as compliance with standards, portability, and maintainability.
   - **更广泛的质量属性**: 检查不仅能发现缺陷，还能评估程序的质量属性，如合规性、可移植性和可维护性。
### Dynamic testing
> A software testing method used to test the dynamic behavior of software code. Aim to test software behavior with dynamic variables and finding weak areas in software runtime environment.
一种软件测试方法，用于测试软件代码的动态行为。目的是用动态变量测试软件的行为，发现软件运行环境中的薄弱环节。

- White box testing
- Black box testing


## Black Box Testing vs White Box Testing
![image](https://github.com/user-attachments/assets/51fbec9c-ab6c-4abb-91d5-736eb112cd46)

### White Box Testing
>White box testing is concerned with the degree to w hich testcases exercise or cover the logic of the program. Focus on internal structure, design and coding of software are tested to verify flow of input-output and to improve design, usability and security.
  
Advantages:
- Forces test developer to reason carefully about implementation.
- Reveals errors in "hidden" code.
- Spots the Dead Code or other issues with respect to best programming practices.
  
Disadvantages:
- Expensive as one has to spend both time and money to perform white box testing.
- In-depth knowledge about the programming language is necessary to perform white box testing.

**Control Flow Graph**
![image](https://github.com/user-attachments/assets/8d2a1d04-df0a-4063-aa21-d7810227e37a)
![image](https://github.com/user-attachments/assets/7b1e19a6-1648-486d-b40e-5a94264ee980)
![image](https://github.com/user-attachments/assets/ace7ac5a-001c-48c4-bb69-b707b0ea87b9)
![image](https://github.com/user-attachments/assets/4195f739-3023-4e35-8635-226a94d6099a)
![image](https://github.com/user-attachments/assets/85cb10ec-a4e5-4511-ba49-4074167e456a)
![image](https://github.com/user-attachments/assets/448a41fd-bd1e-49d0-82e9-a9b00c8e6c9c)

### Black box testing
>Black box testing is a high level of testing that focuses on the behavior of the software. It involves testing from an external or end-user perspective.

- The recommended procedure is to **develop test cases using the black box methods and then develop supplementary test cases with white box methods.**
  黑盒开发测试用例，白盒补充测试用例
  
#### Equivalence Partitioning
识别等效类：识别具有共同特征并应以相同方式处理的输入组。
![image](https://github.com/user-attachments/assets/91c1b52f-e6de-488d-832f-2e46b21f917c)
![image](https://github.com/user-attachments/assets/5b437e74-6a29-435e-b613-b594bb8d5fbc)



## Development Testing VS User Testing

1. **Development Testing**：
   - **目标**：在开发过程中进行测试，发现系统中的 bug 和缺陷。
   - **活动**：
     - **单元测试 (Unit Testing)**：测试单个程序单元或对象类。
     - **集成测试 (Integration Testing)**：将单独的软件模块组合在一起进行测试。
     - **系统测试 (System Testing)**：测试完整的集成系统，评估系统是否符合其指定的要求。

2. **User Testing**：
   - **目标**：用户或潜在用户在自己的环境中测试系统。
   - **重要性**：即使在开发阶段已经进行过全面的系统测试，用户测试依然至关重要，因为用户的工作环境会对系统的可靠性、性能、可用性和健壮性产生重大影响，而这些是无法在测试环境中复制的。

### Integration Testing
A level of software testing where individual units are combined and tested to verify if they are working as they intend to.

软件测试的一种级别，在这种级别中，单个单元被组合并测试，以验证它们是否按预期工作。

The purpose is to expose defects in the interaction between software modules when they are integrated.

其目的是在集成软件模块时暴露软件模块之间交互中的缺陷。

#### Integration Testing Approaches
![image](https://github.com/user-attachments/assets/e0ba6c34-591b-4c28-9b25-3ac7163af2e3)

#### Interface Errors 类型

1. **Interface Misuse** (接口滥用)：  
   - 调用组件在使用另一个组件的接口时发生错误，通常是错误地调用了接口的某些功能或使用了不正确的参数。

2. **Interface Misunderstanding** (接口误解)：  
   - 调用组件对被调用组件的行为做出了错误假设，通常是对接口的功能或预期行为理解不准确。

3. **Timing Errors** (时序错误)：  
   - 调用组件和被调用组件的操作速度不同，导致访问了过时的信息或数据。




### Integration Testing VS System Testing
![image](https://github.com/user-attachments/assets/3d330e87-464f-4fc5-a80e-8ab79fb4affc)


### User Testing Types

1. **Alpha 测试 (Alpha Testing)**：
   - 用户与开发团队合作，在开发者站点进行软件测试。

2. **Beta 测试 (Beta Testing)**：
   - 发布软件版本，允许用户进行试用，并向系统开发人员报告他们发现的问题。

3. **验收测试 (Acceptance Testing)**：
   - 客户测试系统，决定是否接受系统并在客户环境中部署。
