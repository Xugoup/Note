# Ch4-Requirements Engineering
## User/System requirements
### User requirements
- Statements in natural language plus diagrams of the services the system provides and its operational constraints
### System requirements
- A structured document setting out detailed descriptions of the system’s functions, services and operational constraints. Defines what should be implemented so may be part of the contract between the system buyer and the software developers.

## Functional/Non-functional Requirements
### Functional Requirements
- Describe functionality or system services.
- Depend on the type of software, expected users and the type of system where the software is used.
- **Functional user requirements** may be high-level statements of what the system should do.
- **Functional system requirements** should describe the system services in detail.

### Non-functional Requirements
- Non-functional requirements usually specify or constrain characteristics of the system as a whole. (Properties和Constraints)
- Non-functional requirements **may be more critical** than functional requirements. If these are not met, the system may be useless.

### Functional vs Non-functional
![](./Pic/屏幕截图%202024-12-22%20164258.png)
![image](https://github.com/user-attachments/assets/62f10776-6a93-4414-ba48-5464da4293b7)


## Requirements Engineering Processes (三个主要活动)
Requirements engineering involves **three key activities**:
1. Discovering requirements by interacting with stakeholders **(elicitation and analysis)**
2. Converting these requirements into a standard form **(specification)**
3. Checking that the requirements actually define the system that the customer want **(validation)**

## 需求获取技术（Requirements Elicitation Techniques
1. **访谈（Interview）**  
2. **问卷调查（Questionnaire）**  
3. **焦点小组（Focus Group）**  
4. **观察（Observation）**  
5. **文档审查（Document Review）**  
6. **头脑风暴（Brainstorming） / 调查（Survey） / 人种学（Ethnography）**  
7. **原型制作/模型展示（Prototyping/Mockup）**  

### Technique Selection
![](./Pic/屏幕截图%202024-12-22%20164743.png)

## Use case diagram
![image](https://github.com/user-attachments/assets/668d66db-9b38-4f3e-afce-1feea73cb2e4)

## IEEE 830与用户故事

1. **焦点不同**：
   - **IEEE 830** 需求规范侧重于描述解决方案的属性，即系统的功能和技术细节。
   - **用户故事** 聚焦于用户的目标和需求，强调用户如何使用产品实现自己的目标。

2. **编写方式**：
   - **IEEE 830** 鼓励团队一次性写出所有需求，而不是像用户故事那样采用迭代的方式逐步定义需求。
   例如，IEEE 830式的需求：
   - 产品应具有一台汽油发动机。
   - 产品应有四个轮子。
   - 产品应在每个轮子上安装橡胶轮胎。
   - 产品应配有方向盘。
   - 产品应具有钢制车身。

   与用户故事的需求：
   - 该产品使我能快速且轻松地修剪我的草坪。
   - 我在使用该产品时感到舒适。

  ## 用户故事与用例(User Stories and Use Cases)
  
1. **范围和细节**：
   - **用户故事** 通常涵盖的范围较小，细节较少，更多的是描述用户需求和目标。
   - **用例** 涵盖更广泛的系统行为和交互，包含更多的细节，详细描述了系统如何响应用户的每个动作。

2. **持续性**：
   - **用例** 是开发过程中长期存在的文档，通常在整个开发生命周期内都会参考。
   - **用户故事** 更具临时性，通常在迭代结束后不再使用，其主要作用是在当前迭代中帮助团队完成功能交付。

3. **编写目的**：
   - **用例** 的目的是让开发者与客户共同讨论和确认系统功能，通过详细描述帮助团队理解需求。
   - **用户故事** 主要用于发布规划，并作为提醒，帮助团队在实际开发过程中与客户沟通和填充需求细节。
  
## 需求检查(Requirements Checking)：
1. **有效性（Validity）**：
   - 系统是否提供了最能支持客户需求的功能？

2. **一致性（Consistency）**：
   - 需求之间是否存在冲突？

3. **完整性（Completeness）**：
   - 客户要求的所有功能是否都包含在需求中？

4. **现实性（Realism）**：
   - 鉴于现有的预算和技术，需求是否可行？

5. **可验证性（Verifiability）**：
   - 需求是否可以被检查和验证？

## 需求验证技术（Requirements Validation Techniques)
1. **需求评审（Requirements Reviews）**  
   - 评审人员（包括客户和承包商的工作人员）系统地分析**SRS文档**（Software Requirements Specification），检查其中的错误和模糊性。
2. **原型制作（Prototyping）**  
   - 在最终用户或客户面前展示系统的原型，让他们实验展示的模型，并检查其是否符合他们的需求。此类模型通常用于收集关于用户需求的反馈。
3. **测试用例生成（Test Case Generation）**  
   - **SRS文档**中提到的需求应该是可测试的。通常认为，如果测试设计困难或不可能进行，通常意味着需求很难实现，需要重新考虑。
