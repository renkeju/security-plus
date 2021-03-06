=========================
课题A：分析组织风险
=========================

在计划周全的安全架构中，其中一部分内容就是知道什么资产需要进行维护，以及保护的等级。这一过程包括确定哪些部分允许出现错误，在本章课题中，你将评估组织机构中的风险。

如何才能知道需要保护组织免受哪些风险？是什么造成了风险？你需要找出什么能帮助你确定系统或网络中存在哪些风险。如果你可以预见并分析其中的这些风险，那么就能避免以后可能出现的一些主要问题。风险分析可以帮助你实现这一目标。

风险管理
-------------

在信息管理领域中，风险会以许多不同的形式展现出来。如果不能正确地管理风险，就可能引起重要资产的泄露、篡改、丢失、破坏或干扰。风险管理（Risk management）是一种周期性过程，包括四个阶段：

* 确定并评估系统中存在的风险
* 分析风险对系统产生潜在影响
* 规划如何响应风险的策略
* 缓解风险对未来安全造成的不良影响

.. note:: 请记住，漏洞是指安全策略中的缺陷或弱点；威胁是指可能会利用漏洞的实体；风险是指如果威胁确实利用漏洞，可能造成的损失、危害或破坏。

风险分析的组成
-----------------------

风险是指威胁利用漏洞引起某种损害的可能性。因此，当你进行分析，确定风险是否存在时，不仅要确定潜在的威胁，还要确定系统中是否存在这些威胁可以利用的漏洞。一旦确认风险存在，根据风险可能引起的损害及其发生概率就能确定该风险的严重程度。

评估漏洞的威胁
^^^^^^^^^^^^^^^^^^^^

一些有关评估漏洞的威胁的案例可能包括：

* 如果一家企业位于铁路轨道附近，一辆列车脱轨导致泄露了有毒液体，那么在清理过程中，企业可能就不得不停工数天或数周。
* 如果重要位置上的生产工人表示了他们罢工的意愿，他们可能会事先威胁破坏设备，扩大他们后续行动的影响。
* 重要的供应商可能无法为组织主要产品的生产提供原材料。

风险分析的阶段
---------------------------

确定如何保护计算机网络，计算机安装和信息时，风险分析（risk analysis）这一安全过程能够评估可能影响整个组织的风险危害。

.. csv-table:: 风险分析过程的六个阶段
    :header: "风险分析流程的阶段", "描述"
    :widths: 5 30

    "1. 资产确定", "确定需要保护的资产并确定资产的价值。"
    "2. 漏洞确定", "确定漏洞，使分析师能确认资产保护过程中什么地方存在问题。确定了缺陷的位置也就显示了最容易受漏洞影响的关键区域。漏洞扫描时一种用于确定系统内缺陷的方法。但这种方式可能会产生错误警报，引起关注，即使系统中并没有实际的错误或缺陷。"
    "3. 威胁评估", "一旦了解到漏洞所在，就能确定可能会利用这些漏洞的威胁。"
    "4. 可能性量化", "量化威胁利用漏洞的可能性或概率。"
    "5. 影响分析", "一旦确定了可能性，这些潜在威胁可能造成的影响就需要评估。包括从损坏中恢复的影响，以及实施预防措施带来的影响。"
    "6. 应对措施的确定", "确定并开发应对措施消除或降低风险。应对措施必须在经济上有效可行，并提供符合预期的保护强度。换句话说，应对措施的成本必须小于威胁利用漏洞造成的预计损失。"

威胁类型的分类
----------------------

根据安全威胁的来源，通常被分为自然、人为或系统威胁。当你执行风险分析和影响时，知道其来源将会很有帮助。下面列举了每种威胁的例子。

* 自然

    自然威胁与天气或其余自然活动造成的其他不可控事件有关。不同的自然灾害类型有：

    * 地震
    * 野火
    * 洪灾
    * 暴风雪
    * 海啸
    * 飓风
    * 龙卷风
    * 滑坡

* 人为

    人为威胁是指由个人或集体的人为活动造成的其余事件。人为威胁事件可能是有意或无意引起的。

    有意的人为威胁包括：

    * 纵火
    * 恐怖袭击
    * 政治动荡
    * 强行闯入
    * 设备和/或数据被盗
    * 设备损坏
    * 文件损坏
    * 信息泄漏

    无意的人为威胁包括：

    * 用户计算错误
    * 社交网络和云计算
    * 过多员工生病或患上流行病
    * 信息泄露

* 系统

    系统威胁与网络、服务、应用程序或设备中发现的任何缺陷或漏洞有关。

    系统威胁包括：

    * 不安全的移动设备
    * 不稳定的虚拟环境
    * 不安全的网络设备
    * 电子邮件漏洞，如病毒和垃圾邮件
    * 账户管理的漏洞，如未指定权限

风险分析的方式
---------------------------

.. csv-table:: 可用于风险分析的一些方式。
    :header: "方式", "描述"
    :widths: 5 30

    "定性", "定性分析方法通过描述和文字的方式衡量风险的数量和影响力。例如，根据分析影响力使用的标准，可以将等级分为高、中或低。定性分析通常会根据场景不同而变化。定性风险分析的一个缺点源于其有时比较主观和不可测试的方法论。"
    "定量", "定量分析完全根据数值来进行。使用历史记录、经验、行业最佳实践和记录、统计理论、测试以及实验等方法来对数据进行分析。在风险难以被量化的情况下，这种方法论可能就会显得力不从心。"
    "半定量", "半定量分析方法使用与数值相关的描述来进行。它不是完全定性也不是完全定量。这种方法论尝试在前两种风险分析类型之间找到一个中间位置。"

风险计算
----------------

风险计算侧重于研究财务和运营损失的影响，并在组织中寻找威胁利用的指标。风险计算可以被视作一种公式，用来考虑每种资产价值，计算每种威胁发生的可能性，并衡量缓解系统漏洞的可能成本。组织可以使用这种流程来确定每种已知风险的单一损失预期（single loss expectancty/SLE）或年度损失预期（annual loss expectancy/ALE）。SLE的值代表特定不利事件的财务损失。ALE的值是通过SLE乘以它的年发生率（annual rate of occurrence/ARO）来计算，以确定组织在一年内可能承担的风险总成本。

.. code-block:: none

    ALE = SLE * ARO

计算风险
^^^^^^^^^^^^^^^^^^^

一个公司可能计算出，非军事区（DMZ）中某个系统每天都有几乎90%的可能性会遭受一个端口扫描攻击。但是，虽然这个威胁等级很高，公司也不会认为系统会因为扫描攻击而受到高度的损坏风险。加固系统使之彻底防止扫描攻击的成本远远高出由这种风险造成的潜在损失。

从另一个方面看，公司可能确定了一项高危风险，即服务器机房可能会因为自然灾害彻底丧失功能，对组织来说，这种损失将是灾难性的。虽然自然灾害威胁的发生概率极低，但整体影响力却如此巨大，以至于公司维护了一个昂贵的交替站点，在发生类似紧急事件时可以转移业务。

漏洞表
^^^^^^^^^^^^^^^^^^^

一个简单的漏洞表通常能够成为完成漏洞评估的一种战略性工具。下表列举了于不同漏洞相关的详细信息。

.. csv-table:: 不同漏洞相关的详细信息
    :header: "漏洞", "确定来源", "风险发生概率（1代表低，5代表高）", "影响力估计（美元）", "缓解措施"
    :widths: 5 5 5 5 5

    "洪灾危害", "实际的工厂", "5", "$950,000", "物理上的调整和洪灾保险"
    "电力故障", "实际的工厂", "2", "$100,000", "发电机，不间断电源供应（UPS）"
    "流感传染病", "员工", "4", "$200,000", "流感疫苗"

使用表格可以让规划人员确定威胁或漏洞的发生概率，记录可能的影响，按优先顺序排列相应的缓解措施。缓解措施可以降低被利用漏洞产生的不良影响。电力故障是一种相对较高的风险，其相应的有效缓解措施就是进行一笔一次性支出购买备用发电机。

如果这个表格中还有额外的两列，评估就会更加有用，如下表的例子所示。

.. csv-table:: 额外的漏洞信息
    :header: "漏洞", "缓解的成本"， "漏洞影响后的缓解"
    :widths: 5 10 5

    "电力故障", "用$500购买发电机", "$0"

通过添加这些额外的列，业务连续性规划人员就能评估漏洞，提出缓解措施，并评估执行缓解方案之后的其余风险造成的漏洞。

如表中列出的风险信息记录也被叫做风险登记簿（risk register）。除了以表格形式呈现，通常还能用散点图描绘风险登记簿，其中影响力和可能性分别是散点图的轴线，其中的标绘点展示了于分布风险特性有关的更多信息。

风险响应的技巧
----------------------------

一旦确定了一项风险，就能制定响应策略来确定合适的应对措施。甚至可以结合多种策略来完成一次响应。四种常见的响应技术如下表描述：

.. csv-table:: 四种常见的响应技术
    :header: "响应技巧", "描述"
    :widths: 5 30

    "接受", "这表示如果风险真实发生，承认并接受风险及其带来的后果。但接受并不代表让系统完全地暴露在漏洞之下，而是意识到涉及的风险不能完全避免，或是缓解或避免的成本过高。"
    "转移", "将风险的责任分配给其他机构，或第三方，如保险公司。"
    "避免", "通过消除风险的来源和彻底消除风险。这种技术可能只需要结束出于风险之中的操作或实体，如关闭经常成为攻击目标的服务器。"
    "缓解", "这种技巧能防御可能的攻击并在潜在风险产生重大影响时实施。缓解措施可能以入侵检测系统（IDS）等主动防御措施或备份处于风险中的数据等警示措施的形式出现。"

.. note:: 即使应用了缓解措施，大多数情形仍然存在剩余风险。很少有应对措施能将风险降到0。

风险缓解和控制类型
-------------------------

风险可以通过实施合理的安全控制进行缓解。

.. csv-table:: 主要的控制类型
    :header: "控制类型", "描述"
    :widths: 5 30

    "技术控制（Technical control）", "应用软硬件装置监控和防止计算机系统与服务中的威胁和攻击。例如，安装并配置网络防火墙就是一种技术控制。"
    "管理控制（Management control）", "应用相应流程监控组织安全策略的服从情况。这些控制专门用于控制特定区域的操作效率，并监控安全策略的服从度。例如，年度或定期安全扫描和审计能够检查对安全策略的服从程度。"
    "操作控制（Operational Control）", "用于保护日常业务操作，功能和活动所有方面的安全措施。例如，入口处的门锁和保安仅允许授权员工进入大楼。"
    "损失控制（Loss control）", "也叫损害控制（damage control），这是用于保护关键资产不受侵害的安全措施。包括降低损失发生概率，以及降低发生损失时的严重程度。例如，灭火器和洒水器系统可以降低发生火灾时财产被破坏的程度。"

变更管理
-----------------

变更管理（Change management）是一种批准并执行变更的系统性方法，以便确保信息技术服务达到最佳的安全性、稳定性和可用性。当一个组织变更它的硬件、软件、基础设施或文档时，就会面临引入意外事件的风险。因此，对一个组织来说，合理评估风险、量化培训、支持、维护和实施的成本，合理权衡提议变更带来的复杂性和利益u都是重要的工作。通过维护一个有存档的变更管理流程，组织就能避免因草率变更带来可能的反作用。

例如，Jane发现一个新的服务数据包被发布，用于修正服务器中操作系统的许多安全漏洞。需要使用该服务包的服务器正在运行一个自定义的内部应用程序，不允许出现重大故障停机。公司策略规定必须为所有服务包批准一个变更管理表单。从审批流程中返回该表单，确保服务包在部署到生产服务器之前，必须在实验系统中进行测试。Jane在实验室中应用了这个服务包并发现它会导致自定义的内部应用程序出现故障。在服务包被应用到生产环境之前，应用程序必须被发送回软件开发商进行修正和重新测试。

分析风险的准则
-----------------------

当你分析风险时，可以考虑这些准则：

* 清晰地定义组织对安全性的期望。
* 确定需要进行保护的资产，并确定它们的价值。
* 寻找可能存在的漏洞，如果这些漏洞被利用，可能对组织产生的副作用。
* 确定组织资产的的潜在威胁。
* 确定威胁利用漏洞的可能性或概率。
* 确定潜在威胁的影响，无论是从故障系统中恢复还是实施可降低或消除风险的安全控制。
* 确定最适合组织的风险分析方式。在定量和半定量风险分析的方式中，为每种威胁计算SLE和ARO，然后计算ALE。
* 确定可能的应对措施，确保这些措施有成本效益并且能够按预期执行。
* 清晰记录分析过程中的所有发现和所有决策。

练习 2-1
------------------

场景：最近，Develetech公司一直担心位于总部大楼一楼的服务器机房的安全性。机房中具备高度业务价值的资产包括存储了敏感员工身份数据的人力资源服务器，以及客户财务数据服务器。机房位于主大厅旁边，不包含窗户，并且可以通过数字键盘进行访问控制。你已经确定了需要保护的资产，现在你被要求对服务器机房的物理安全进行全面风险分析。

1. 服务器机房周围i有哪些明显的漏洞，你还会调查哪些其他方面的内容？

2. 根据计算机机房中的已知漏洞，存在哪些潜在威胁？

3. 哪些因素会影响这些威胁成功的可能性？

4. 如果成功地进行了未授权访问，你认为会造成哪些潜在影响？

5. 在这种情况下，可能会使用哪些风险缓解策略来降低服务器机房物理方位周围的风险？

