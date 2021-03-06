==========================
课题B：评估漏洞
==========================

你已经确定了一些常见的漏洞，现在，需要评估组织中的这些漏洞。使用不同的工具和技巧，你就能更快更高效地找到组织地弱点所在。

安全评估
------------------

安全评估（Secutiry asscssment）是指通过一组综合性的技术测试安全控制过程，暴露出你的工具、技术、服务和操作中的任何弱点和差距。这个测试的目的在于为你提供能及时有效地缓解任何漏洞地所需信息。在安全评估中，实际使用的方法差别很大。这些方法会影响测试的性质，决定采用主动还是被动形式，还会影响其他特征。

漏洞评估（vulnerability asscssment）就是其中的一种方法。这一过程会根据系统的配置状态，评估系统的安全性和满足合规性要求的能力。实质上，漏洞评估确定了当前配置是否与理想配置（基线）相符。漏洞评估人通常通过自动的漏洞评估工具完成，它会检测组织的系统，应用程序和设备以确定操作的当前状态和任何安全控制的有效性。典型的漏洞评估结果能去确定常见的错误配置，缺少必要的安全控制，以及其他相关漏洞。

测试授权
^^^^^^^^^^^^^^^^^^

虽然通常不会产生入侵威胁，但是漏洞评估还是可能会对商业操作产生一定影响，因此，在你执行这类测试之前可能需要管理层的授权。

安全评估技巧
---------------------

下表描述了可以用来执行安全评估的常见技术

.. csv-table:: 执行安全评估的常见技术
    :header: "技巧", "描述"
    :widths: 5 30
    
    "审核基线报告（baseline report）", "基线报告是一组被应用到组织中特定系统或网络的安全和配置设置集合。基线报告是一种可以用来比对网络中其他系统的基准。当为特定计算机创建一个基线时，确定需要包含在内的设置取决于它的操作系统及其在组织中的功能，并且应当包含行业的推荐。"
    "执行代码审核（code review）", "在开发过程中，所有应用程序都应当执行常规的代码审查。审查可以由开发人员手动执行，也可以使用源代码分析工具自动进行。两种方式在确定应用程序中的潜在弱点都非常有用，如果这些弱点没有被更正，最中可能会引起攻击。"
    "确定攻击面（attack surface）", "攻击面是指系统或应用程序中所有可能暴露给攻击者并被利用的项目组合。通过减少攻击面中的项目，就能降低潜在攻击产生的影响。"
    "审核安全架构", "安全架构审核（security architecture review）是指对组织当前安全基础架构模型的评估。常规审核在确定当前系统和关键资产是否得到合理保护，潜在威胁和漏洞是否已经得到处理方面有着重要作用。在审核过程中，确定需要关注的领域，进行进一步评估，以确保安全措施符合当前需求。"
    "审核安全设计", "安全设计审核需要在应用安全实施之前完成。使用结构化的审核结果，审核人员就能确定安全方案是否能够满足组织的实际需求。"

漏洞评估工具
---------------------

当你在系统中评估漏洞是，有许多可用的软件工具。通过运行这些工具，你就能知道当潜在攻击者评估你的系统时他们将会看到哪些内容。但是，这些工具对你的效用高低取决于漏洞评估工具产生的结果被你理解的程度。当你能够熟练地知道在工具产生地结果中，希望出现哪些内容，以及哪些需要留意时，你就能容易地消除系统中地任何漏洞。

下表列举了几种可以在你地组织中评估漏洞地不同工具。

.. csv-table:: 评估漏洞的工具
    :header: "工具类型", "应用于"
    :widths: 5 30

    "漏洞扫描器", "评估你的系统，网络和应用程序中的弱点。"
    "端口扫描器", "评估网络中所有端口的当前状态，并检测可能会对组织产生风险的开放端口。"
    "协议/数据包分析", "评估网络上的流量，流量中揭示的内容，以及使用的协议。"
    "指纹识别（Fingerprinting）工具", "确定目标的操作系统信息和运行服务。也叫做标志提取（hanner grabbing）"
    "网络枚举器", "映射网络的逻辑结构，以确定网络上的流氓系统。"
    "密码破解器", "从存储在计算机中或通过计算机传输的数据中恢复密码。"
    "备份工具", "创建被扫描数据的复制版本。"
    "蜜罐", "将可疑活动从合法网络系统中重定向到一个可以安全监控的独立系统中。"

关于蜜罐的更多信息
^^^^^^^^^^^^^^^^^^^^^^^^^^^

蜜罐（honeypot）是指在追踪攻击者活动时，吸引他们离开合法网站来源的安全工具。虽然蜜罐时以网络的合法组成部分出现并运作的，但实际上还是一种安全的加密箱，安全专家可以锁定入侵并开始记录活动，用作法庭证明，甚至可以发动反向攻击。引诱个人的行为可能会被视为陷阱或反组织的道德规范。这些法律和道德问题让应当组织的法律顾问和人力资源部门进行研讨。

蜜罐可以时软件模拟程序，硬件诱饵，或者就是一个完整的虚假网络，即密网（honeynet）。

漏洞扫描的类型
---------------------

漏洞扫描有多种不同的类型，它们在特定环境中会很有用。比如，一些工具适合扫描无线网络实施过程中的弱点。一些专门用作配置合规性扫描器，评估系统的状态是否符合基线。漏洞扫描还可以按照是否需要凭证来进行区分。

凭证扫描在扫描系统时，会使用安全人员设置的特定许可。这种方式使扫描能够成功（或尝试）与系统进行身份验证。这种理念就是扫描有能力真正地评估系统配置地所有方面，而不是仅评估普通用户看到的内容。另一方面，非凭证扫描只是评估了普通用户看到的内容。可能你倾向于以最大权限运行扫描，以便不会错过任何东西，但是非凭证扫描的优势就是允许你专注于任何用户都能观察到的最明显弱点，不管这些用户的权限高低。非凭证扫描相对凭证扫描有着更小的侵入性，并且消耗更少的资源。

误检
----------

所有的扫描，不论何种类型，都会受到误检率的影响。在安全评估环境中，误检（false ponsitive）就是指扫描器或其他评估工具确定了一项漏洞，而实际上并不是。理解出现误检风险对你来说非常关键，因为通过更改特定配置来尝试解决不存在或错判的问题，可能会对系统的安全性造成重大的负面影响。

例如，假设一次漏洞扫描确定了防火墙上的一个开放端口。因为已知某种品牌的恶意软件可以使用这个端口，工具就会将他标记为一个安全风险，并推荐你关闭这个端口。但是这个端口在你的系统中并没有开放。研究问题需要花费事件和精力，如果漏洞扫描发出了过多的误检，就容易完全忽略扫描，可能导致更大的问题。

漏检
^^^^^^^^^^^

一个相关术语就是漏检（false negative），是指工具确定某个项目不是漏洞，而实际上是漏洞，这可能会导致问题长时间无法被发现，被认为是扫描工具中的灾难性故障。

评估漏洞的准则
-------------------------

当评估漏洞时：

* 考虑主机的操作系统和平台是如何进行配置的。
* 不要依赖默认的主机配置来获得最佳安全性。
* 创建与你的安全需求相对应的自定义主机配置。
* 思考组织开放或使用的应用程序是如何受到不合理输入处理和内存问题等漏洞的影响的。
* 思考使用过时的密码套件是如何危害网络流量加密的。
* 评估你的数字证书中的错误配置，如无效的格式编排。
* 评估加密密钥管理系统中是否存在可能使攻击者更容易访问私钥的弱点。
* 思考你的网络架构是如何使攻击者更容易地获得访问权限或发动拒绝服务状况的。
* 思考错误配置的用户/计算机账户是如何造成威胁的。
* 确定组织中可能极易受到社会工程攻击的任何用户，因此需要对这些人员进行培训。
* 确定任何缺乏有效规划的关键业务流程，如寿命末期（EOL）流程等。
* 思考系统延申和未登记资产是如何使用组织中的所有要素变得更难保护。

