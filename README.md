<div class="Box-sc-g0xbh4-0 bJMeLZ js-snippet-clipboard-copy-unpositioned" data-hpc="true"><article class="markdown-body entry-content container-lg" itemprop="text">
<p align="center" dir="auto">
  <a target="_blank" rel="noopener noreferrer nofollow" href="https://camo.githubusercontent.com/d6a1e3aaf88d197cad43451479e6e996788a9ef4e02ed9cbb5b2d6eb72edef01/68747470733a2f2f616d6f726f2e6e6574656173652e636f6d2f696d672f616d6f726f2d6c6f676f2e737667"><img src="https://camo.githubusercontent.com/d6a1e3aaf88d197cad43451479e6e996788a9ef4e02ed9cbb5b2d6eb72edef01/68747470733a2f2f616d6f726f2e6e6574656173652e636f6d2f696d672f616d6f726f2d6c6f676f2e737667" alt="阿莫罗标志" height="120px" data-canonical-src="https://amoro.netease.com/img/amoro-logo.svg" style="max-width: 100%;"></a>
</p>
<p align="center" dir="auto">
  <a href="https://www.apache.org/licenses/LICENSE-2.0.html" rel="nofollow">
    <img src="https://camo.githubusercontent.com/3e787ad45f0862131e82fe26cfdf93deb2c5fbdd320f047942fa916088cc716e/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f6c6963656e73652d417061636865253230322d3445423142412e737667" data-canonical-src="https://img.shields.io/badge/license-Apache%202-4EB1BA.svg" style="max-width: 100%;">
  </a>
  <a href="https://github.com/NetEase/amoro/actions/workflows/core-hadoop3-ci.yml">
    <img src="https://github.com/NetEase/amoro/actions/workflows/core-hadoop3-ci.yml/badge.svg" style="max-width: 100%;">
  </a>
  <a href="https://github.com/NetEase/amoro/actions/workflows/core-hadoop2-ci.yml">
    <img src="https://github.com/NetEase/amoro/actions/workflows/core-hadoop2-ci.yml/badge.svg" style="max-width: 100%;">
  </a>
  <a href="https://github.com/NetEase/amoro/actions/workflows/trino-ci.yml">
    <img src="https://github.com/NetEase/amoro/actions/workflows/trino-ci.yml/badge.svg" style="max-width: 100%;">
  </a>
</p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Amoro（原名 Arctic）是一个基于开放数据湖格式构建的 Lakehouse 管理系统。 Amoro 与 Flink、Spark 和 Trino 等计算引擎合作，为 Lakehouse 带来可插拔和自我管理的功能，提供开箱即用的数据仓库体验，并帮助数据平台或产品轻松构建基础设施解耦、流式传输和-批量融合和湖泊原生架构。</font></font></p>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">建筑学</font></font></h2><a id="user-content-architecture" class="anchor" aria-label="永久链接：建筑" href="#architecture"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Amoro的架构图如下：</font></font></p>
<p align="center" dir="auto">
  <a target="_blank" rel="noopener noreferrer nofollow" href="https://camo.githubusercontent.com/485392abe59dc851f2733f93669f8770888cdfd6568495a5c7ca82907239996e/68747470733a2f2f616d6f726f2e6e6574656173652e636f6d2f2f696d672f686f6d652d636f6e74656e742e706e67"><img src="https://camo.githubusercontent.com/485392abe59dc851f2733f93669f8770888cdfd6568495a5c7ca82907239996e/68747470733a2f2f616d6f726f2e6e6574656173652e636f6d2f2f696d672f686f6d652d636f6e74656e742e706e67" alt="阿莫罗建筑" height="360px" data-canonical-src="https://amoro.netease.com//img/home-content.png" style="max-width: 100%;"></a>
</p>
<ul dir="auto">
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">AMS：Amoro管理服务提供Lakehouse管理功能，如自优化、数据过期等。它还为所有计算引擎提供统一的目录服务，也可以与现有的元数据服务结合。</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">插件：Amoro 提供了多种外部插件可供选择，以满足不同的场景。
</font></font><ul dir="auto">
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">优化器：自优化执行引擎插件对所有类型表格式表异步执行合并、排序、去重、布局优化等操作。</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Terminal：SQL命令行工具，提供本地Spark、Kyuubi等多种实现。</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">LogStore：基于Kafka、Pulsar等消息队列，提供毫秒级到秒级的SLA，用于实时数据处理。</font></font></li>
</ul>
</li>
</ul>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持的表格格式</font></font></h2><a id="user-content-supported-table-formats" class="anchor" aria-label="永久链接：支持的表格格式" href="#supported-table-formats"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Amoro可以管理不同表格式的表，类似于MySQL/ClickHouse可以选择不同的存储引擎。 Amoro通过使用不同的表格格式来满足不同的用户需求。目前，Amaro 支持四种表格格式：</font></font></p>
<ul dir="auto">
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Iceberg格式：用户可以直接将自己的Iceberg表委托给Amoro进行维护，这样用户不仅可以使用Iceberg表的所有功能，还可以享受Amoro带来的性能和稳定性提升。</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">混合Iceberg格式：Amoro在Iceberg格式之上为流式更新场景提供了一组更优化的格式。如果用户对流式更新性能要求较高，或者对CDC增量数据读取功能有需求，可以选择使用Mixed-Iceberg格式。</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">混合Hive格式：很多用户在使用数据湖的同时，不希望影响原本建立在Hive上的业务。因此，Amoro提供了Mixed-Hive格式，只需通过元数据迁移即可将Hive表升级为Mixed-Hive格式，而原有的Hive表仍然可以正常使用。这样保证了业务的稳定性，并受益于数据湖计算的优势。</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Paimon 格式：Amoro 支持以 Paimon 格式显示元数据信息，包括 Schema、Options、Files、Snapshots、DDL 和 Compaction 信息。</font></font></li>
</ul>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">支持的引擎</font></font></h2><a id="user-content-supported-engines" class="anchor" aria-label="永久链接：支持的引擎" href="#supported-engines"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">冰山格式</font></font></h3><a id="user-content-iceberg-format" class="anchor" aria-label="永久链接：冰山格式" href="#iceberg-format"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Iceberg格式表使用Iceberg社区提供的引擎集成方法。详情请参考：</font></font><a href="https://iceberg.apache.org/docs/latest/" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Iceberg Docs</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></p>
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">混合格式</font></font></h3><a id="user-content-mixed-format" class="anchor" aria-label="永久链接：混合格式" href="#mixed-format"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Amoro 支持混合格式的多种处理引擎，如下所示：</font></font></p>
<table>
<thead>
<tr>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">处理引擎</font></font></th>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">版本</font></font></th>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">批量读取</font></font></th>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">批量写入</font></font></th>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">批量覆盖</font></font></th>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">流式阅读</font></font></th>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">流式写入</font></font></th>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">创建表</font></font></th>
<th><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">修改表</font></font></th>
</tr>
</thead>
<tbody>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">弗林克</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">1.15.x、1.16.x、1.17.x</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">✔</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">✔</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">✖</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">✔</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">✔</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">✔</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">✖</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">火花</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">3.1、3.2、3.3</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">✔</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">✔</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">✔</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">✖</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">✖</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">✔</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">✔</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">蜂巢</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">2.x、3.x</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">✔</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">✖</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">✔</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">✖</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">✖</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">✖</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">✔</font></font></td>
</tr>
<tr>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">特里诺</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">406</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">✔</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">✖</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">✔</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">✖</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">✖</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">✖</font></font></td>
<td><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">✔</font></font></td>
</tr>
</tbody>
</table>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">特征</font></font></h2><a id="user-content-features" class="anchor" aria-label="永久链接：特点" href="#features"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<ul dir="auto">
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">自我优化——持续优化表，包括压缩小文件、更改文件、定期删除过期文件，以保持较高的查询性能并降低存储成本。</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">多种格式——支持Iceberg、Mixed-Iceberg、Mixed-Hive等不同表格式，满足不同场景需求，并提供统一管理能力。</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">目录服务 - 为所有计算引擎提供统一的目录服务，该服务也可以与现有的元数据存储服务（例如 Hive Metastore 和 AWS Glue）一起使用。</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">丰富的插件 - 提供各种插件与其他系统集成，例如使用 Flink 进行持续优化以及使用 Spark 和 Kyuubi 进行数据分析。</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">管理工具 - 提供多种管理工具，包括WEB UI和标准SQL命令行，帮助您更快上手并更轻松地与其他系统集成。</font></font></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">基础设施独立——可以在私有环境、云环境、混合云环境、多云环境中轻松部署和使用。</font></font></li>
</ul>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">模块</font></font></h2><a id="user-content-modules" class="anchor" aria-label="永久链接：模块" href="#modules"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Amoro包含以下模块：</font></font></p>
<ul dir="auto">
<li><code>amoro-core</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">包含其他模块的核心抽象和通用实现</font></font></li>
<li><code>amoro-ams</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">是amoro管理服务模块
</font></font><ul dir="auto">
<li><code>ams-api</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">包含 ams thrift api 和常用接口</font></font></li>
<li><code>ams-dashboard</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">是 ams 的仪表板前端</font></font></li>
<li><code>ams-server</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">是ams的后端服务器</font></font></li>
<li><code>ams-optimizer</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">提供默认优化器实现</font></font></li>
</ul>
</li>
<li><code>amoro-mixed-format</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">提供混合格式实现
</font></font><ul dir="auto">
<li><code>amoro-hive</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">与 Apache Hive 集成并实现混合 Hive 格式</font></font></li>
<li><code>amoro-flink</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">为混合格式表提供 Flink 连接器（使用 amoro-flink-runtime 作为阴影版本）</font></font></li>
<li><code>amoro-spark</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">为混合格式表提供 Spark 连接器（使用 amoro-spark-runtime 作为阴影版本）</font></font></li>
<li><code>amoro-trino</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">为混合格式表提供 Trino 连接器</font></font></li>
</ul>
</li>
</ul>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">建筑</font></font></h2><a id="user-content-building" class="anchor" aria-label="永久链接： 建筑" href="#building"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Amoro 是使用 Maven 和 Java 1.8 和 Java 17（仅适用于</font></font><code>mixed-format/trino</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">模块）构建的。</font></font></p>
<ul dir="auto">
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">构建 Trino 模块需要</font></font><code>toolchains.xml</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">在</font></font><code>${user.home}/.m2/</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">目录中进行配置，内容为</font></font></li>
</ul>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>&lt;?xml version="1.0" encoding="UTF-8"?&gt;
&lt;toolchains&gt;
    &lt;toolchain&gt;
        &lt;type&gt;jdk&lt;/type&gt;
        &lt;provides&gt;
            &lt;version&gt;17&lt;/version&gt;
            &lt;vendor&gt;sun&lt;/vendor&gt;
        &lt;/provides&gt;
        &lt;configuration&gt;
            &lt;jdkHome&gt;${YourJDK17Home}&lt;/jdkHome&gt;
        &lt;/configuration&gt;
    &lt;/toolchain&gt;
&lt;/toolchains&gt;
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="<?xml version=&quot;1.0&quot; encoding=&quot;UTF-8&quot;?>
<toolchains>
    <toolchain>
        <type>jdk</type>
        <provides>
            <version>17</version>
            <vendor>sun</vendor>
        </provides>
        <configuration>
            <jdkHome>${YourJDK17Home}</jdkHome>
        </configuration>
    </toolchain>
</toolchains>" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<ul dir="auto">
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">要调用构建并运行测试：</font></font><code>mvn package -P toolchain</code></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">要跳过测试：</font></font><code>mvn -DskipTests package -P toolchain</code></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">要在没有 trino 模块和 JAVA 17 依赖的情况下进行打包：</font></font><code>mvn clean package -DskipTests -pl '!mixed-format/trino'</code></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">使用hadoop 2.x构建（默认为3.x）</font></font><code>mvn clean package -DskipTests -Dhadoop=v2</code></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">指示优化器的 Flink 版本（默认为 1.18.1）：</font></font><code>mvn clean package -Dflink-optimizer.flink-version=1.15.4</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。如果Flink版本在1.15.0以下，还需要添加参数</font></font><code>-Pflink-pre-1.15</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">：</font></font><code>mvn clean package -Pflink-pre-1.15 -Dflink-optimizer.flink-version=1.14.6</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。
</font></font><code>mvn clean package -Pflink-pre-1.15 -Dflink-optimizer.flink-version=1.14.6 -DskipTests</code></li>
</ul>
<blockquote>
<p dir="auto"><font style="vertical-align: inherit;"></font><code>trino</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">模块</font><font style="vertical-align: inherit;">中默认跳过 Spotless 。</font><font style="vertical-align: inherit;">所以如果你想在构建</font></font><code>trino</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">模块时执行checkstyle，你必须在Java 17环境中。</font></font></p>
</blockquote>
<ul dir="auto">
<li><font style="vertical-align: inherit;"></font><code>mixed-format/trino</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">要在 Java 17 环境中</font><font style="vertical-align: inherit;">调用构建包含模块：</font></font><code>mvn clean package -DskipTests -P trino-spotless</code></li>
<li><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">仅在 Java 17 环境中构建</font></font><code>mixed-format/trino</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">及其依赖模块：</font></font><code>mvn clean package -DskipTests -P trino-spotless -pl 'mixed-format/trino' -am</code></li>
</ul>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">快速开始</font></font></h2><a id="user-content-quickstart" class="anchor" aria-label="永久链接：快速入门" href="#quickstart"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">访问</font></font><a href="https://amoro.netease.com/quick-demo/" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">https://amoro.netease.com/quick-demo/</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">快速探索 amoro 的功能。</font></font></p>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">加入社区</font></font></h2><a id="user-content-join-community" class="anchor" aria-label="永久链接：加入社区" href="#join-community"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">如果您对Lakehouse、Data Lake Format感兴趣，欢迎加入我们的社区，我们欢迎任何组织、团队和个人共同成长，并真诚希望通过开源帮助用户更好地使用Data Lake Format。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">加入阿莫罗微信群：添加“ </font></font><code>kllnn999</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">”为微信好友，并注明“阿莫罗爱人”。</font></font></p>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">贡献者</font></font></h2><a id="user-content-contributors" class="anchor" aria-label="永久链接：贡献者" href="#contributors"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">这个项目的存在要感谢所有做出贡献的人。</font></font></p>
<a href="https://github.com/NetEase/amoro/graphs/contributors">
  <img src="https://camo.githubusercontent.com/c8610e9ccc57a1794830e1f239fac9af6a4895ab1ea50cd45a57e189bd49cd39/68747470733a2f2f636f6e747269622e726f636b732f696d6167653f7265706f3d4e6574456173652f616d6f726f" data-canonical-src="https://contrib.rocks/image?repo=NetEase/amoro" style="max-width: 100%;">
</a>
<p dir="auto"><font style="vertical-align: inherit;"></font><a href="https://contrib.rocks" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">用contrib.rocks</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">制作</font><font style="vertical-align: inherit;">。</font></font></p>
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">明星历史</font></font></h2><a id="user-content-star-history" class="anchor" aria-label="永久链接：明星历史" href="#star-history"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><a href="https://star-history.com/#NetEase/amoro&amp;Date" rel="nofollow"><img src="https://camo.githubusercontent.com/e7e0285706f904f17960ec7bbd3208cae17771841cc4d209fde9498367ae43d5/68747470733a2f2f6170692e737461722d686973746f72792e636f6d2f7376673f7265706f733d4e6574456173652f616d6f726f26747970653d44617465" alt="明星历史图" data-canonical-src="https://api.star-history.com/svg?repos=NetEase/amoro&amp;type=Date" style="max-width: 100%;"></a></p>
</article></div>
