# Ch9-Software Evolution
## Handover Problems
1. 开发团队已经使用了敏捷方法，但是演进团队不熟悉敏捷方法，更喜欢基于计划的方法。（演进团队期望更多细节的文档，敏捷开发不提供）
2. 开发团队使用基于计划的方法，演进团队更喜欢敏捷方法。（演进团队要重新开发，***自动测试***和代码没有按照敏捷方法的要求***重构和简化***）

## Legacy Systems

**选择遗留系统管理策略**取决于系统的质量和其业务价值(system quality and business value)。

具体策略如下：

1. **废弃系统**：当遗留系统的质量差、已无法满足现代需求，且继续使用它不再有业务价值时，可以选择完全废弃系统，并修改业务流程，使其不再依赖该系统。( Scrap the system completely and modify business processes so 
that it is no longer required)
   
2. **继续维护系统**：如果系统依然满足业务需求，并且维护成本较低，或者没有可行的替代方案，可以选择继续维护该系统。(Continue maintaining the system;)
   
4. **重新设计系统（Re-engineering）**：当系统质量较差，但仍然具有一定的业务价值时，可以通过重构或重新设计来提高系统的可维护性，延长其使用寿命。( Transform the system by re-engineering to improve its maintainability)

5. **替换系统**：如果系统过时且无法通过维护或重构满足现代需求，或者替代方案更具业务价值，可以选择用新的系统替代遗留系统。(Replace the system with a new system.)

   
## Software Maintenance
### Types of Maintenance

- Fault repairs (故障修复): 修改系统以修复漏洞/缺陷，并纠正系统未能满足要求的地方。

- Environmental adaptation (环境适应): 修改系统使其能够在不同的环境中运行（如不同的计算机、操作系统等）。

- Functionality addition and modification (功能添加与修改): 修改系统以满足新的需求。

### Reengineering
>Restructuring or rewriting part or all of a legacy system without changing its functionality.

Advantages:
- Reduced risk
- Reduced cost

### Refactoring 
>The process of making improvements to a program to slow down degradation through change.

### Refactoring VS Reengineering
**Reengineering:**

Re-engineering takes place after a system has been maintained for some time. 

在系统维护了一段时间后，维护成本在提升时，

Use automated tools to process and reengineer a legacy system to create a new system that is more maintainable.

使用自动化工具创建新系统。

**Refactoring:**

Refactoring is a continuous process of improvement throughout the development and evolution process.

重构是贯穿开发和演化过程的持续改进过程。

It is intended to avoid the structure and code degradation that increases the costs and difficulties of maintaining a system.

它的目的是避免结构和代码退化，从而增加维护系统的成本和困难。
