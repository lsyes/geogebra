# 欢迎来到 GeoGebra!

本仓库包含 GeoGebra 数学应用软件的源代码。它托管于 GitLab 私有实例，并镜像至 GitHub。

请阅读 [https://www.geogebra.org/license](https://www.geogebra.org/license) 以了解 GeoGebra 的授权信息。

---

## 🛠️ 构建说明和环境配置 (Loongson/LoongArch64 优化)

**核心要求：**

* **Java SDK 版本：** 建议使用 **OpenJDK 24** 或更高版本，以匹配 GeoGebra 依赖的 Kotlin/Gradle 配置。
* **Kotlin/Gradle 兼容性：** 构建日志显示：`Kotlin does not yet support 25 JDK target, falling back to Kotlin JVM_24 JVM target`。这意味着您应尽量使用 **OpenJDK 24** 或配置 **JVM Toolchain** 以避免潜在的兼容性警告。

### 1. 编译环境配置

在开始编译之前，请确保您的系统已正确配置了 OpenJDK 24。


### 2. 核心构建命令

请使用 Gradle 包装器 (Gradle Wrapper) 进行构建。

| 目标平台 | 命令 | 说明 |
| :--- | :--- | :--- |
| **桌面版 (Classic 5)** | `./gradlew :desktop:desktop:run` | **推荐：** 启动桌面应用程序 (GeoGebra 5)。 |
| **网页版** | `./gradlew :web:run` | 启动开发服务器（默认端口 8888）。 |

---

## 💻 运行桌面版 (GeoGebra Classic 5)

运行桌面版的最简单方式是使用 Gradle 命令：

```bash
./gradlew :desktop:desktop:run
