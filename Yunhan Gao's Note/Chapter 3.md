# Ch3-Agile Software Development 
![image](https://github.com/user-attachments/assets/c1e68378-c129-4585-b204-b078d3a7ce8d)

## 目的
**Reduce overheads** in the software process (e.g., by limiting documentation) and to be able to **respond quickly to changing requirements** without excessive rework

## Agile Manifesto (敏捷宣言：IWCR)
- Individuals and interactions over processes and tools (个人和交互优于过程和工具)
- Working software over comprehensive documentation (可以工作的软件胜过全面的文档)
- Customer collaboration over contract negotiation (客户协作优先于合同谈判)
- Responding to change over following a plan (对变化做出反应由于跟随计划)

## Agile Method Applicability (敏捷方法适应情况)
- 需求不确定或频繁变化
- 客户和开发团队之间的紧密合作
- 快速交付和早期反馈
- 团队规模较小
- 技术创新或探索性项目
- 高频繁的发布需求
- 对质量有较高要求
- Development of a **small** or **medium-sized** product
- **Custom system development** within an organization, where there is a clear commitment from the **customer to become involved in the development process** and where there are ***few external rules and regulations that affect the software***.

## Agile Development Techniques(理解)

### Extreme Programming(XP)
Extreme Programming (XP) takes an ‘extreme’ approach to iterative development.

![](./Pic/屏幕截图%202024-12-21%20214710.png)

**Key Practices**:
- User stories for specification
- Refactoring
- Test-first development
- Pair programming

**User Stories for Requirements**

在XP中，客户或用户是XP团队的一部分，负责对需求做出决策。

用户需求表示为用户故事或场景。

这些都写在卡片上，开发团队将它们分解为实现任务。这些任务是进度和成本估算的基础。

客户根据他们的优先级和进度估计来选择要包含在下一个版本中的故事。

![image](https://github.com/user-attachments/assets/fe500596-dd75-4ac7-a791-4d1f57b0e744)

## Planning Poker：
1. **任务描述**：产品负责人介绍要估算的用户故事或特性。
2. **选择卡片**：每个估算者根据自己的理解，私下选择一张代表任务工作量的卡片。
3. **公开展示**：所有估算者同时展示选择的卡片，如果一致，则确定估算值。
4. **讨论差异**：如果估算值不一致，团队讨论高估算和低估算者的理由，澄清任务复杂度。
5. **重新估算**：经过讨论后，估算者重新选择卡片，再次展示。
6. **达成共识**：这个过程反复进行，直到达成共识，或者推迟估算直到获取更多信息。
通过这种方式，团队可以更准确地估算任务的复杂度。

## 重构（Refactoring） 
一种持续改善代码结构的过程，旨在使代码更易于理解和修改，即使没有立即的需求。其核心思想是通过不断重构，减少未来修改的成本。

1. **XP观点**：与传统的“为变更设计”不同，XP认为无法准确预测变更，因此提倡通过**持续重构**来应对变化。
2. **优势**：重构使代码结构更加清晰，减少文档需求，简化未来的修改。
3. **缺点**：有些变更可能涉及架构重构，成本较高。

**重构示例**：
- 重组类层次以去除重复代码。
- 清理和重命名属性、方法，使其更易懂。
- 用库函数替换内联代码。

## 测试优先开发（Test-first Development）
是XP中的核心实践，强调在每次代码变更后立即进行测试。其特点包括：

1. **先写测试**：先编写测试用例，明确要实现的功能需求。
2. **增量测试**：从场景出发逐步编写测试，确保每个功能块逐步验证。
3. **用户参与**：用户参与测试开发和验证，确保需求得到准确实施。
4. **自动化测试**：使用自动化测试框架（如Junit）每次构建新版本时自动运行所有测试，确保新功能没有引入错误。

**测试驱动开发（TDD）**：测试作为程序的一部分进行编写，自动执行并检查结果，确保代码的正确性。

**自动化测试**：测试代码在任务实现前编写，独立且可执行，用于验证输入输出是否符合要求，并能快速执行，帮助及时发现新代码引入的问题。

### 问题：
- 程序员可能会偷懒，编写不完整的测试。
- 某些测试（如复杂界面）难以逐步编写。
- 难以判断测试的完整性，可能无法覆盖所有情况。

## 结对编程（Pair Programming）
两位程序员共同合作开发代码的方式。

1. **共同开发**：两位程序员坐在同一台电脑前合作编程，动态配对，确保团队成员之间的知识共享。
2. **共享代码所有权**：通过共同编写代码，团队成员共享代码的所有权，提升代码质量。
3. **非正式审查**：每行代码都由两人检查，起到自然的代码审查作用。
4. **促进重构**：团队可以共同优化系统代码，提升整体质量。
5. **效率与风险**：结对编程的效率并不低，能降低团队成员离职时的风险，因为知识在团队间得到了共享。


## Scrum
- A lightweight, simple to understand and difficult to master framework within which people can address complex adaptive problems, while productively and creatively delivering products of the highest possible value.
- A framework within which you can employ various processes and techniques.
  
**Scrum的优势**：

1. **可管理的任务**：产品被拆分为一组易于管理和理解的小块，方便开发团队逐步推进。
2. **不受不稳定需求影响**：不稳定的需求不会阻碍项目进展，灵活应对变化。
3. **团队透明度**：整个团队对项目进展有清晰的了解，促进了团队之间的沟通与协作。
4. **按时交付与反馈**：客户能够看到增量的按时交付，并获得关于产品功能的反馈。
5. **建立信任**：客户与开发人员之间建立了信任，形成了一个积极的文化氛围，大家共同期待项目的成功。


**Scrum中三种角色：**
- **Product Owner** (green figure):
The “What”: with a focus on value, time to market, return on investment.
- **Development Team** (red figures)
The "How”: focus on building something that is useable and potentially releasable.
- **Scrum Master** (blue figure)
A facilitator who arranges daily meetings, tracks the backlog of work to be done, records decisions, measures progress against the backlog.

**Scrum 的三种 Artifacts:**

**Product Backlog,  Sprint Backlog,  Working Software**

- The Product Backlog is an ordered list of everything that is known to be needed in the product. 
- The Sprint Backlog is the set of Product Backlog items selected for the Sprint, plus a plan for delivering the product Increment and realizing the Sprint Goal. 


**Formal events for inspection and adaptation**(四种调整/检查事件)：
- Sprint Planning
- Daily Scrum
- Sprint Review
- Sprint Retrospective


## Visual Management
剩余工作燃尽图是剩余工作相对于时间的图形表示。未完成的工作（或待办事项）通常在垂直轴上，时间在水平轴上。
![image](https://github.com/user-attachments/assets/5bb699e5-1c4f-4d5b-9175-8d22141a9dd1)


### Scrum VS XP

| Scrum                                                        | XP                                                           |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| Typically from two weeks to one month long.                  | Typically one or two weeks long.                             |
| Do not allow changes in their timelines.                     | Allow changes in their set timelines.                        |
| Scrum emphasizes self-organization.                          | Extreme Programming emphasizes strong engineering practices  |
| In Scrum framework, team determines the sequence in which the product will be developed. | In Extreme Programming, team have to follow a strict priority order or pre-determined priority order. |
| Scrum framework is not fully described. If you want to adopt it then you need to fill the framework with your own frameworks method like XP or Kanban. | Extreme Programming can be directly applied to a team. XP is also known for its ready-to-apply features. |

![](./Pic/屏幕截图%202024-12-21%20154413.png)
