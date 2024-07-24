# JavaRce

By. Whoopsunix

# 0x00 do what?

🚀 对照实战场景梳理较通用的 Java Rce 相关漏洞的利用方式 记录在 [VulnCore](SecVulns/VulnCore) 中，参考 [cwe](https://cwe.mitre.org) 标准构建

🚩 子目录 [VulnCore](SecVulns/VulnCore) 给出 Java 利用方式，具体覆盖量见对应 README.md 文件

⛳️ 配套测试靶场 [SecVulns](SecVulns) 主要针对 DevSecOps 场景构建（IAST、RASP、SAST），采用 [httpREST](SecVulns/SecVulnsREST) 实现批量测试。大多数 Java 靶场都把注意力集中在 Spring、Tomcat 组件上，之后会引入更多组件丰富 Source 点 

🪝 EXP: 反序列化框架 [PPPYSO](https://github.com/Whoopsunix/PPPYSO) 集成了部分内容

🚧 Protection: [PPPRASP](https://github.com/Whoopsunix/PPPRASP) 基于 [jvm-sandbox](https://github.com/alibaba/jvm-sandbox) 对 VulnCore 中的漏洞实现防护（仅实现关键函数的 HOOK，不作进一步处理）

🛰 Detection: 基于 [joern](https://github.com/joernio/joern) 实现漏洞检测

# PS

因为是漏洞测试环境，难免会引入部分没法直接拉取的依赖（太老了中央仓库移除、或者没有魔法上网）

可以到 https://mvnrepository.com/ 手动下载 jar 包到本地 maven 仓库

举个例子 下载 [c3p0 0.9.5.2](https://mvnrepository.com/artifact/com.mchange/c3p0/0.9.5.2) 依赖放到本地的  `/.m2/repository/com/mchange/c3p0/0.9.5.2` 目录下

# Stats

![Alt](https://repobeats.axiom.co/api/embed/818a4d2c0d1562eec751b2637b825b3b0d2cf0e3.svg "Repobeats analytics image")

[//]: # ([![Stargazers over time]&#40;https://starchart.cc/Whoopsunix/JavaRce.svg&#41;]&#40;https://starchart.cc/Whoopsunix/JavaRce&#41;)
