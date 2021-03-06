======================================
课题D：管理账户
======================================

组织为用户和组织中的其他实体分配账户，以便能够更密切地管理这些实体在整个IAM过程中地识别、认证和授权方式。在本章课题中，你将应用最佳实践来维护这些账户的安全性。

账户管理
--------------

账户管理（Account management）是用来指代有效管理组织内用户账户的过程，功能和策略的通用术语。账户管理是IAM中的一项特定功能，使管理员能创建、更新、修改和删除于特定身份相关的账户和配置文件。用户账户可以被允许或拒绝访问组织的信息系统和资源；因此，只有在合适的控制下，组织才能合理地管理账户。

账户权限
--------------------

账户权限是授予用户允许执行各种操作的许可，如创建、删除和编辑文件，以及访问网络上的系统和服务。

权限可以由用户或组分配。用户分配的权限对每个系统用户都是唯一的，并且可以为满足特定工作职能或任务的需求而进行配置。基于组的权限被分配给组织内的整个用户组。组中的每个用户将拥有相同的权限。对有着许多用户的大型组织来说，这是一种有效方式，这些用户的权限可以以部门为单位进行分配，如RBAC模型。按组分配权限是一种通用的最佳实践。具有特殊用户分配权限的用户如果同时也是组成员，就会被授予这两组权限。

用户和组权限应在组织的账户策略中详细记录。

账户类型
--------------------------

账户可以包含大量的自定义功能，以适应组织的业务和安全需求。被附加到这些账户上的身份信息和权限可以包含许多维度和特征。但是，大多数账号只适合几种一般类型或类被之一。

.. csv-table:: 账户类型
    :header: "账户类型", "描述"
    :widths: 5 30

    "用户账户", "用户账户只是组织中一般用户的标准账户类型。这些账户几乎总是受限于权限，特别是为IT成员保留的权限（例如，对服务器的完全管理性访问）。组织中的大多数非IT人员将使用这种类型的账户。因此，可能会限制标准账户修改敏感数据或配置超出其工作职能的系统。"
    "特权账户", "与标准账户相比，特权账户对组织中的数据和系统具有更大的访问权限。大多数管理员账户属于此类别，因为需要提升权限才能访问域控制器等关键基础架构。同样，向数据库管理员这样的工作角色也需要提升权限才能修改和删除敏感数据。虽然特权账户通常保留给IT或管理人员，但一些普通用户也需要对他们自己的工作站进行管理级别的访问，因此此类账户可能会被视为特权账户。"
    "访客账户", "访客账户被提供给可能需要有限网络访问的非工作人员。例如，公司可以允许客户或其他公共访问信息显示台或其他面向公众的终端。信息显示台或终端将允许这些人以访客的身份登录，而不是要求他们注册一个可能只能使用一次的账户。访客账户上没有密码或其他主要识别信息，以访客身份登录的用户几乎无法创建、修改或删除文件。尽管访问权限有限，但在大多数环境中禁用访客账户通常是一种很好的做法。"
    "计算机和服务账户", "人类用户并非IAM系统中使用账户的唯一实体。一些计算机在组织中扮演者特定角色，并且必须访问文件和其他系统来履行职责。例如，一个Web服务器可能需要将产品信息存储在网络另一网段上的单独数据库中。你不必授予Web服务器对数据库的完全访问权限，只要设置拥有特定权限的账户，使Web服务器只能访问与数据库相关的所需内容。"

账户策略
------------------

账户策略(account policy)是一种包含组织对账户创建，账户监控和账户删除的要求的文档。策略可以包括针对用户的要求或组管理要求。用户账号策略会有所不同，可以进行自定义并根据业务需求来执行。作为安全专业人员，你需要根据业务需要调研并分析组织的策略要求。一些常见的政策声明包括：

* 谁可以批准账户创建。
* 谁被允许使用资源。
* 用户是否可以共享账户或拥有多个账户。
* 审核用户访问后，何时以及如何禁用和修改账户。
* 用户账号在一段时间的不适用后是否应该终止，以及何时终止。
* 何时执行一般账户的禁用。
* 应对密码历史，密码强度和密码重用执行哪些规则。
* 在发生任何可疑事件或劫持尝试时，何时锁定账户。
* 在账户遭到入侵或被删除后，何时以及如何恢复账号。

密码策略
--------------------

下面列出了组成账户了策略的密码部分或离散密码策略的一些要求：

* 密码长度
    为了防止暴力破解，密策略通常对最短长度做出强制要求。暴力破解密码的事件随着引入每个额外字符而呈指数增长。例如，现代计算机将花费几分钟的事件破解随机密码“amsnp”；将密码长度增加一倍变成“amsnpcjnyk”，破解事件就会增加到几年。

* 密码复杂性

    与密码长度一样，通常强制要求复杂性以保护用户免受密码破解尝试。复杂性通常由所有字符的类型和这些字符的格式定义。例如，一个复杂的密码可能需要使用一个特殊字符（如感叹号、问号等）， 并且至少要有一个小写字母和一个大写字母，以及一个数字。以前面的“amsnpcjnyk”为例，复杂性要求在每次尝试中添加特殊字符，数字和大写字母，这将大大增加破解密码所需的时间。

* 密码历史

    许多密码政策规定，每隔一段时间，用户都必须更改密码。这有助于创建一个移动目标，使攻击者需要跟上不断变化的证书，才能成功破解账户。与此同时，许多策略会要求用户选择以前没有使用过或长时间未使用的密码。记住密码可疑确保用户每次被迫改变密码时都不会重复使用相同的密码。

* 密码重用

    使用密码的一个常见危险时人们在多个账户上使用相同的密码。如果一个账户的证书收到损害，则使用相同密码的其他账户也将面临风险。因此，密码策略可能会规定工作人员不应在多个系统中重复使用相同的密码。与前面的要求不同，密码重用在技术层面上不要求强制执行。用户可以在他们自己的个人账户上重复使用密码，这些账户由你无法控制的系统管理。

多账户
--------------

当一个人拥有系统或资源的几个账户时，会出现多用户账户。根据应用的访问级别，账户可能会有所不同，如用户级别账户与管理员账户。在一个组织内，单个用户拥有多个系统的多个账户时很常见的。与分配和管理多账户相关的问题如下：

* 用户缺乏对各种账户的了解。
* 为相应账户分配数据访问和许可的合适级别。
* 管理每个单独账户的权限、许可和数据复制。

多账户的一种常见用例时具有用户级别账户的系统管理员使用的账户，这些账户具有用于进行日常工作的典型用户权限，如准备文档，使用互联网和发送电子邮件；还有一个管理员级别的账户，仅用于执行系统程序，如管理用户或配置服务器。在这种情况下，当用户在账户之间切换时，通常更愿意能够使用相同的环境配置，例如Windows桌面设置、文档历史和Web浏览器收藏夹列表。管理方面的挑战是要能确保用户可以按需访问管理账户的提升特权，同时不会丢失支持生产力所需的其他环境设置。

共享账户
------------------

共享账户可以由多个用户或资源访问，与传统的非共享账户不同，它们不与任何个体相关联。共享账户通常与许多用户可以共享特定角色或目的相关联：

* 匿名，访客和其他通用账户可作为访问者访问系统的一种方式。
* 临时账户对于不在公司中连续工作的员工或承包商非常有用。
* 管理账户允许多名讲过授权的专业用户访问更高权限。
* 批处理账户可以轻松自动执行许多不同类型的任务。

共享账户本身就存在安全风险。由于许多不同的人会使用一个账户，因此在发生违规时要让特定的个人负责是非常困难的，而且往往是不可能的。同样，用户自己可能也认识到了这一点，并且不在意安全性，在他们登录到自己的个人账户时可能会避免这种情况。另一个主要风是对账户密码的更改，在他们登录到自己的个人账户是可能会避免这种情况。另一个主要风险是对账户密码的更改。由于频繁更换密码是一项常用策略，因此组织需要确保每个有权访问账户的人都知道密码何时会更改，以及新密码会是什么。这就需要将密码分配给一大群人，这对安全性来说本身就是一种重大挑战。

账户管理安全控制
-----------------------------

为了维护组织的安全需求，你应该实施并执行严格的账户管理安全控制。下表介绍了其中一些控制方法。

.. csv-table:: 账户管理安全控制
    :header: "安全控制", "描述"
    :widths: 5 30

    "标准命名惯例", "为了减少混淆，账户应该以一致的方式命名。这有助于加强账户的管理，尤其是通过使用脚本和命令行。例如，如果你的惯例是在域中“姓氏.名字”的形式进行命名，那么不要将Nathan Davids的账户命名为Dnathan。你还应该避免根据昵称或常用词命名账户，避免用户身份被隐藏。"
    "账户维护", "根据组织的规模和结构，你可能需要疆场修改现有账户或删除不再使用账户。你应该制定一个维护计划，以确保不会遗漏任何必要的更改，也不会过早地移除账户。"
    "入职\离职", "随着新员工进入组织，你需要为他们创建新账户。同样，对于离开组织地员工，必须禁用他们的账户并将其从系统中删除。入职和离职计划有助于指导你完成这一过程，从而最大限度地减少干扰并防止已终止的员工账户被作为攻击媒介。"
    "访问权限重新鉴定（Access recertification）", "账户应当经历许多审计和审查，以确定它们是否仍然遵守最小特权原则。一些账户随着时间的推移积累了太多的权限——一种被称为许可蠕变（permissions creep）的过程。重新认证将帮助你确定不必要的权限，以便可以修改账户使之更加符合用户或资源的实际需求。"
    "使用情况审计", "除了审核许可之外，你还应该监控用户账户在组织中的使用方式。这可以帮助你找出权限扩大攻击，或知识提醒你特定账户不应涉及的行为。例如，如果某个账户在反常的时间使用或正在从未知来源地址使用，这些伊苏可能代表该账户已经被劫持。"
    "基于组的访问控制", "如前所述，将用户安排到组中会减轻管理单独账号的一些负担。当用户分到组中时，就能轻松地为多人添加或撤销许可，从而为你节省时间和精力.如果它们时某个组中地成员，也就能更容易地了解每个用户在组织中的工作智能。"
    "基于位置的策略", "为了更好地控制组织中地账户使用情况，你可能需要考虑实施一定策略，限制用户可以中进行访问的物理和虚拟位置。基于位置的限制可以防止恶意或未知来源上的远程攻击。"
    "一天中的时刻限制", "除了一些例外情况，你预期大多数用户会在每天的特定时间工作。为了避免被发现，攻击者会在非工作时间使用账户来获取访问权限。缓解这种风险的一种方法就是简单地将账户地访问权限限制为只有当员工正在工作地特定时间才能访问。"

凭证管理
------------------

创建凭证管理器（Credential manager）是为了帮助用户和组织更轻松地存储和管理账户用户名和密码。这些应用程序通常将凭证存储再本地计算机上的加密数据库中。通过认证的用户可以从中检索正确凭证用于相关系统。这对于在多个系统中拥有多账户的用户来所特别有用，并且由于凭证管理器可以自动在表单中填写用户名和密码，因此可以抵御击键记录恶意软件。

但是，凭证管理器的强度只能与他们存储的凭证相同。简单的或容易猜到密码为攻击者提供访问账户的便利，无论密码存储的安全程度如何。此外，如果凭证管理器通过从主密码生成密钥来加密密码数据库，那么发现主密码的攻击者将危及整个凭证数据库。使用多因素认证的凭证管理器在发生此类攻击时更安全。

.. note:: 凭证管理软件的例子包括跨平台的应用程序LastPass，KeePass和1Password；适用于iOS和macOS的Keychain；适用于Windows的Credential Manager。

组策略
--------------

Windows系统中的组策略服务为跨域管理账号安全提供了几种不同的方法。这样的例子包括：

* 优化账户密码的属性，如长度、复杂性和寿命。
* 优化账户的锁定阈值和持续时间。
* 使用可逆的加密技术存储账户密码。
* 执行Kerberos登录限制和票据生命周期。
* 审计账户管理事件。
* 为个人或组账户分配特定的权限和控制。

身份联合
---------------

身份联合（Identity federation）是指将一个身份在多个不同身份管理系统之间进行链接的做法。身份联合包含所有服务于此类身份的策略和协议。这提供了一个集中的身份管理结构，消除了多余身份信息的需求。联合身份不仅可以缓解主机的一些压力，而且用户还发现，在多个用例上精简使用一个账户比需要多个不同账户更加实用和高效。但是，这也为用户的身份创造了一个单一的破坏点。如果联合账户的证书被盗用，攻击者就能在其所有不同的功能和域中使用该账户。

单点登录（SSO）是身份联合的一个子集，消除了多次登录联合系统的必要性。用户将在会话开始时登录到一个系统，如果他们最终转而使用另一个信任其联合身份的系统，则用户不会被强制要求重新进行身份验证。但是，并非所有联合身份都实施SSO；有些需要在不同的地方重新进行认证。

.. note:: Google账户和Microsoft账户就是联合身份的例子。

可信任传递
^^^^^^^^^^^^^^^^^^^

身份联合通常以可传递信任（transitive trust）的原则进行操作。要了解可传递的信任，可以考虑以下示例：

* 实体A和实体B互相信任
* 实体A和实体C互相信任

通过传递信任原则，即使相互之间没有建立正式的信任关系，实体B现在也会隐式地信任实体C，反之亦然。在身份联合领域，如果系统之间互相信任，则由一个系统信息地用户账户可以被另一个系统隐式信任。

身份联合的方法
-------------------------

你可以为联合环境实施集中不同的身份管理方法。下表列出了其中的一些方法。

.. csv-table:: 身份联合的方法
    :header: "身份联合的方法", "描述"
    :widths: 5 30

    "安全声明标记语言[Security Assertion Markup Language(SAML)]", "SAML是一种基于XML的框架，用于交换于安全相关的信息，例如用户认证、授权和属性。这种信息通过安全的HTTP连接以声明的形式进行通讯，传达了有关主体访问级别的主体身份和授权决定。"
    "OpenID", "OpenID是一种使用加入了OpenID系统的特定站点对用户身份验证的方法。这使他们可以为所有参与网站保留一个账户。用户将在给定域中使用OpenID域下的网站会给用户使用这个系统登录的选项。站点会联系其外部OpenID提供商，以验证用户提供的登录证书是否正确。谷歌和亚马逊等互联网公司使用他们自己的OpenID系统。"
    "OAuth", "鉴于OpenID提供了联合身份验证服务，OAuth是可用于补充OpenID的授权协议。在OAuth中，授权服务器代表资源向用户提供访问口令。用户将这些口令提供给资源，组员则确定给予用户的访问级别。Google、Twitter和Facebook等主要网站都支持OAuth。OpenID Direct为最新版本的OAuth 2.0协议添加了认证层。"
    "Shibboleth", "Shibboleth是基于SAML的联合身份方法，通常被大学或公共服务组织采用。在Shibboleth实现中，用户尝试从一个启用了Shibboleth的网站中检索资源，然后网站通过URL查询发送SAML认证信息。然后用户被重定向到一个身份提供器中，他们可用使用此SAML信息于其进行身份验证。随后身份提供器用正确的身份验证信息响应服务提供商（启用了Shibboleth的网站）。网站验证此响应并根据用户的SAML信息授予他们特定资源的访问权限。"

管理账户的准则
-----------------------

管理账户时：

* 在分配用户和账户访问时实施最小权限原则。
* 制定一个账户策略并在其中包含所有账户策略地要求。
* 确认账户请求和批准程序存在并得到执行。
* 确认账户修改程序存在并得到执行。
* 制定密码策略并在其中包含确保密码能够抵御破解尝试的要求。
* 限制多账户和共享账户的使用，防止滥用。
* 实施账户管理安全控制，如维护、审计和基于位置/时间的限制。
* 使用证书管理软件将用户名和密码存储在加密的数据库中。
* 实施组策略进行更加广泛的访问控制。
* 考虑实施身份联合系统以简化系统之间的用户访问。
* 思考联合身份如何成为访问不同系统的单点故障。

