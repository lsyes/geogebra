# Welcome to GeoGebra!


This repository contains source code of [GeoGebra](https://www.geogebra.org)'s math apps.
It is available on a private GitLab instance and mirrored to GitHub.

Please read https://www.geogebra.org/license about GeoGebra's
licensing.

## Running the web version
To start the web version from command line, run

```
./gradlew :web:run
```

This will start a development server on your machine where you can test the app. 
If you need to access the server from other devices, you can specify a binding address

```
./gradlew :web:run -Pgbind=A.B.C.D
```

where `A.B.C.D` is your IP address. 
Then you can access the dev server through `http://A.B.C.D:8888`.
You can also run `./gradlew :web:tasks` to list other options.

## Running the desktop version (Classic 5)
To start the desktop version from command line, run

```
./gradlew :desktop:run
```
You can also run `./gradlew :desktop:tasks` to list other options.

## Setup the development environment

* Open IntelliJ. If you don't have IntelliJ on your computer yet 
then you can download and install it from [here](https://www.jetbrains.com/idea/download)
* In the menu select File / New / Project from Version Control / Git
* In the new window add the following path: `https://git.geogebra.org/ggb/geogebra.git`
* Click on ‘Checkout’, select your preferred destination folder, select Java 1.8 as the SDK, 
click on OK and wait…
* After the project is checked out, select the root folder of the project, 
open the Run Anything tool (Double ^ on Mac) and run the following command: 
`./gradlew :web:run`
* After a minute or two the GWT UI will appear
* After the Startup URLs are loaded on the UI, select the app that you wish start. For example, 
if you select `graphing.html` and click on Launch Default Browser 
then the Graphing Calculator app with the newest features 
will load and start in your default browser
构建说明：
首先，配置好我的世界中用七根木棍合成的东西，然后用我改过的这个仓库（安同应改为使用openjdk24）
编译过程：lsyes@lsyes-loongsonls3a60007a20001wv01crb:~/geogebra$ ./gradlew :desktop:run
Starting a Gradle Daemon (subsequent builds will be faster)

> Configure project :shared
Kotlin does not yet support 25 JDK target, falling back to Kotlin JVM_24 JVM target

> Task :build-logic:convention:checkKotlinGradlePluginConfigurationErrors SKIPPED
> Task :build-logic:convention:generateExternalPluginSpecBuilders
> Task :build-logic:convention:extractPrecompiledScriptPluginPlugins
> Task :build-logic:convention:generateScriptPluginAdapters
> Task :build-logic:convention:pluginDescriptors
> Task :build-logic:convention:processResources
> Task :build-logic:convention:compilePluginsBlocks
> Task :build-logic:convention:generatePrecompiledScriptPluginAccessors

> Task :build-logic:convention:compileKotlin
Kotlin does not yet support 25 JDK target, falling back to Kotlin JVM_24 JVM target
w: ⚠ Inconsistent JVM Target Compatibility Between Java and Kotlin Tasks
Inconsistent JVM-target compatibility detected for tasks 'compileJava' (25) and 'compileKotlin' (24).
This will become an error in Gradle 8.0.
Solution:
Consider using JVM Toolchain: https://kotl.in/gradle/jvm/toolchain
Learn more about JVM-target validation: https://kotl.in/gradle/jvm/target-validation


> Task :build-logic:convention:compileJava NO-SOURCE
> Task :build-logic:convention:classes
> Task :build-logic:convention:jar

[Incubating] Problems report is available at: file:///home/lsyes/geogebra/build/reports/problems/problems-report.html

FAILURE: Build failed with an exception.

* What went wrong:
Cannot locate tasks that match ':desktop:run' as task 'run' not found in project ':desktop'.

* Try:
> Run gradlew tasks to get a list of available tasks.
> For more on name expansion, please refer to https://docs.gradle.org/9.2.1/userguide/command_line_interface.html#sec:name_abbreviation in the Gradle documentation.
> Run with --stacktrace option to get the stack trace.
> Run with --info or --debug option to get more log output.
> Run with --scan to generate a Build Scan (powered by Develocity).
> Get more help at https://help.gradle.org.

BUILD FAILED in 53s
9 actionable tasks: 9 executed
lsyes@lsyes-loongsonls3a60007a20001wv01crb:~/geogebra$ ./gradlew :desktop:desktop:run
> Task :build-logic:convention:checkKotlinGradlePluginConfigurationErrors SKIPPED
> Task :build-logic:convention:generateExternalPluginSpecBuilders UP-TO-DATE
> Task :build-logic:convention:extractPrecompiledScriptPluginPlugins UP-TO-DATE
> Task :build-logic:convention:compilePluginsBlocks UP-TO-DATE
> Task :build-logic:convention:generatePrecompiledScriptPluginAccessors UP-TO-DATE
> Task :build-logic:convention:generateScriptPluginAdapters UP-TO-DATE

> Task :build-logic:convention:compileKotlin UP-TO-DATE
Kotlin does not yet support 25 JDK target, falling back to Kotlin JVM_24 JVM target

> Task :build-logic:convention:compileJava NO-SOURCE
> Task :build-logic:convention:pluginDescriptors UP-TO-DATE
> Task :build-logic:convention:processResources UP-TO-DATE
> Task :build-logic:convention:classes UP-TO-DATE
> Task :build-logic:convention:jar UP-TO-DATE

> Configure project :shared
Kotlin does not yet support 25 JDK target, falling back to Kotlin JVM_24 JVM target

> Task :desktop:canvas-desktop:processResources NO-SOURCE
> Task :desktop:editor-desktop:processResources NO-SOURCE
> Task :shared:renderer-base:processResources NO-SOURCE
> Task :desktop:renderer-desktop:processResources
> Task :desktop:desktop:processResources
> Task :shared:common-jre:processResources

> Task :shared:editor-base:compileJavacc
Java Compiler Compiler Version 8.1.0 (Parser Generator)
(type "javacc" with no arguments for help)

Reading from file /home/lsyes/geogebra/source/shared/editor-base/src/main/javacc/org/geogebra/editor/share/io/latex/Parser.jj . . .
Warning: Output directory "/home/lsyes/geogebra/source/shared/editor-base/build/generated/javacc/tmp/org/geogebra/editor/share/io/latex" does not exist. Creating the directory.
Note: UNICODE_INPUT option is specified. Please make sure you create the parser/lexer using a Reader with the correct character encoding.
Warning: Choice conflict in [...] construct at line 251, column 19.
         Expansion nested within construct and expansion following construct
         have common prefixes, one of which is: "^"
         Consider using a lookahead of 2 or more for nested expansion.
File "Parser.java" does not exist.  Will create one.
File "ParserTokenManager.java" does not exist.  Will create one.
File "Token.java" does not exist.  Will create one.
File "TokenMgrException.java" does not exist.  Will create one.
File "ParseException.java" does not exist.  Will create one.
File "ParserConstants.java" does not exist.  Will create one.
File "SimpleCharStream.java" does not exist.  Will create one.
File "Provider.java" does not exist.  Will create one.
File "StringProvider.java" does not exist.  Will create one.
File "StreamProvider.java" does not exist.  Will create one.
Parser generated with 0 errors and 2 warnings.

> Task :shared:editor-base:processResources NO-SOURCE
> Task :shared:giac-jni:compileJava
> Task :shared:giac-jni:processResources NO-SOURCE
> Task :shared:giac-jni:classes
> Task :shared:giac-jni:jar
> Task :desktop:jogl2:compileJava
> Task :desktop:jogl2:processResources NO-SOURCE
> Task :desktop:jogl2:classes
> Task :desktop:jogl2:jar
> Task :shared:canvas-base:compileJava
> Task :shared:canvas-base:processResources NO-SOURCE
> Task :shared:canvas-base:classes
> Task :shared:canvas-base:jar

> Task :shared:common:compileJavacc
Java Compiler Compiler Version 8.1.0 (Parser Generator)
(type "javacc" with no arguments for help)

Reading from file /home/lsyes/geogebra/source/shared/common/src/main/javacc/org/geogebra/common/kernel/prover/polynomial/PolynomialParser.jj . . .
Warning: Output directory "/home/lsyes/geogebra/source/shared/common/build/generated/javacc/tmp/org/geogebra/common/kernel/prover/polynomial" does not exist. Creating the directory.
File "PolynomialParser.java" does not exist.  Will create one.
File "PolynomialParserTokenManager.java" does not exist.  Will create one.
File "Token.java" does not exist.  Will create one.
File "TokenMgrException.java" does not exist.  Will create one.
File "ParseException.java" does not exist.  Will create one.
File "PolynomialParserConstants.java" does not exist.  Will create one.
File "SimpleCharStream.java" does not exist.  Will create one.
File "Provider.java" does not exist.  Will create one.
File "StringProvider.java" does not exist.  Will create one.
File "StreamProvider.java" does not exist.  Will create one.
Parser generated with 0 errors and 1 warnings.
Java Compiler Compiler Version 8.1.0 (Parser Generator)
(type "javacc" with no arguments for help)

Reading from file /home/lsyes/geogebra/source/shared/common/src/main/javacc/org/geogebra/common/kernel/parser/Parser.jj . . .
Warning: Output directory "/home/lsyes/geogebra/source/shared/common/build/generated/javacc/tmp/org/geogebra/common/kernel/parser" does not exist. Creating the directory.
File "Parser.java" does not exist.  Will create one.
Warning: Line 313, Column 10: Non-ASCII characters used in regular expression.
Please make sure you use the correct Reader when you create the parser, one that can handle your character set.
File "ParserTokenManager.java" does not exist.  Will create one.
File "Token.java" does not exist.  Will create one.
File "TokenMgrException.java" does not exist.  Will create one.
File "ParseException.java" does not exist.  Will create one.
File "ParserConstants.java" does not exist.  Will create one.
File "SimpleCharStream.java" does not exist.  Will create one.
File "Provider.java" does not exist.  Will create one.
File "StringProvider.java" does not exist.  Will create one.
File "StreamProvider.java" does not exist.  Will create one.
Parser generated with 0 errors and 2 warnings.

> Task :shared:keyboard-base:compileJava
注: /home/lsyes/geogebra/source/shared/keyboard-base/src/main/java/org/geogebra/keyboard/base/impl/ButtonImpl.java使用或覆盖了已过时的 API。
注: 有关详细信息, 请使用 -Xlint:deprecation 重新编译。

> Task :shared:keyboard-base:processResources NO-SOURCE
> Task :shared:keyboard-base:classes
> Task :shared:keyboard-base:jar
> Task :desktop:canvas-desktop:compileJava
> Task :desktop:canvas-desktop:classes
> Task :desktop:canvas-desktop:jar
> Task :shared:common:processResources

> Task :shared:renderer-base:compileJava
注: /home/lsyes/geogebra/source/shared/renderer-base/src/main/java/com/himamis/retex/renderer/share/FencedAtom.java使用了未经检查或不安全的操作。
注: 有关详细信息, 请使用 -Xlint:unchecked 重新编译。

> Task :shared:renderer-base:classes
> Task :shared:renderer-base:jar

> Task :desktop:renderer-desktop:compileJava
注: /home/lsyes/geogebra/source/desktop/renderer-desktop/src/main/java/com/himamis/retex/renderer/desktop/graphics/GraphicsFactoryDesktop.java使用或覆盖了已过时的 API。
注: 有关详细信息, 请使用 -Xlint:deprecation 重新编译。

> Task :desktop:renderer-desktop:classes
> Task :desktop:renderer-desktop:jar
> Task :shared:editor-base:compileJava
> Task :shared:editor-base:classes
> Task :shared:editor-base:jar

> Task :desktop:editor-desktop:compileJava
注: /home/lsyes/geogebra/source/desktop/editor-desktop/src/main/java/org/geogebra/editor/desktop/event/KeyListenerAdapter.java使用或覆盖了已过时的 API。
注: 有关详细信息, 请使用 -Xlint:deprecation 重新编译。

> Task :desktop:editor-desktop:classes
> Task :desktop:editor-desktop:jar

> Task :shared:common:compileJava
注: 某些输入文件使用或覆盖了已过时的 API。
注: 有关详细信息, 请使用 -Xlint:deprecation 重新编译。
注: 某些输入文件使用了未经检查或不安全的操作。
注: 有关详细信息, 请使用 -Xlint:unchecked 重新编译。

> Task :shared:common:classes
> Task :shared:common:jar

> Task :shared:common-jre:compileJava
注: /home/lsyes/geogebra/source/shared/common-jre/src/main/java/org/geogebra/common/jre/headless/AppCommon.java使用或覆盖了已过时的 API。
注: 有关详细信息, 请使用 -Xlint:deprecation 重新编译。

> Task :shared:common-jre:classes
> Task :shared:common-jre:jar

> Task :desktop:desktop:compileJava
注: 某些输入文件使用或覆盖了已过时的 API。
注: 有关详细信息, 请使用 -Xlint:deprecation 重新编译。
注: 某些输入文件使用了未经检查或不安全的操作。
注: 有关详细信息, 请使用 -Xlint:unchecked 重新编译。

> Task :desktop:desktop:classes

> Task :desktop:desktop:run
GeoGebra 5.2.909.1 04 December 2025 Java 25.0.1-loongarch64

19:37:40.404 DEBUG: org.geogebra.desktop.main.AppD.<init>[401]: runningFromJar=false
19:37:40.407 DEBUG: org.geogebra.desktop.main.AppD.<init>[406]: Not setting up logging via LogManager
19:37:41.134 DEBUG: org.geogebra.common.kernel.Kernel.printAttachedViews[3596]: Number of registered views = 1
 * class org.geogebra.desktop.geogebra3D.euclidianFor3D.EuclidianViewFor3DD
19:37:41.172 DEBUG: org.geogebra.common.gui.Layout.initializeDefaultPerspectives[76]: CAS support: true
19:37:41.304 DEBUG: org.geogebra.common.kernel.Kernel.printAttachedViews[3596]: Number of registered views = 2
 * class org.geogebra.desktop.geogebra3D.euclidianFor3D.EuclidianViewFor3DD
 * class org.geogebra.common.plugin.EventDispatcher
19:37:41.551 DEBUG: org.geogebra.common.kernel.Kernel.printAttachedViews[3596]: Number of registered views = 3
 * class org.geogebra.desktop.geogebra3D.euclidianFor3D.EuclidianViewFor3DD
 * class org.geogebra.common.plugin.EventDispatcher
 * class org.geogebra.desktop.gui.view.algebra.AlgebraViewD
19:37:41.578 WARN: org.geogebra.desktop.main.AppD.setVersionCheckAllowed[843]: Option versionCheckAllow not recognized : 
19:37:41.578 INFO: org.geogebra.desktop.main.GeoGebraPreferencesD.loadVersionCheckAllow[206]: No system preferences
19:37:42.013 DEBUG: org.geogebra.desktop.gui.menubar.GeoGebraMenuBar.updateMenubar[134]: update menu
19:37:42.148 DEBUG: org.geogebra.desktop.gui.app.GeoGebraFrame$AppThread.checkVersion[586]: Checking version
19:37:42.148 DEBUG: org.geogebra.desktop.gui.app.GeoGebraFrame$AppThread.checkVersion[602]: major version check needed: no check was done yet
19:37:42.542 DEBUG: org.geogebra.desktop.euclidian.event.MouseEventD.<init>[17]: possible missing release()
19:37:44.278 DEBUG: org.geogebra.desktop.gui.app.GeoGebraFrame$AppThread.checkVersion[656]: current=5002909001 newest=5002000000
java.io.FileNotFoundException: https://download.geogebra.org/installers/5.4/version.txt?ver=5.2.909.1&os=linux&java=25.0.1-loongarch64
        at java.base/sun.net.www.protocol.http.HttpURLConnection.getInputStream0(HttpURLConnection.java:1696)
        at java.base/sun.net.www.protocol.http.HttpURLConnection.getInputStream(HttpURLConnection.java:1302)
        at java.base/sun.net.www.protocol.https.HttpsURLConnectionImpl.getInputStream(HttpsURLConnectionImpl.java:223)
        at org.geogebra.desktop.util.HttpRequestD.sendRequestPostSync(HttpRequestD.java:95)
        at org.geogebra.desktop.util.HttpRequestD.sendRequestGetResponseSync(HttpRequestD.java:166)
        at org.geogebra.desktop.gui.app.GeoGebraFrame$AppThread.checkVersion(GeoGebraFrame.java:685)
        at org.geogebra.desktop.gui.app.GeoGebraFrame$AppThread.run(GeoGebraFrame.java:522)
19:37:44.754 ERROR: org.geogebra.desktop.util.HttpRequestD.sendRequestPostSync[117]: https://download.geogebra.org/installers/5.4/version.txt?ver=5.2.909.1&os=linux&java=25.0.1-loongarch64
19:37:44.755 DEBUG: org.geogebra.desktop.gui.app.GeoGebraFrame$AppThread.checkVersion[695]: newest_minor=5002000000

[Incubating] Problems report is available at: file:///home/lsyes/geogebra/build/reports/problems/problems-report.html

BUILD SUCCESSFUL in 1m 26s
39 actionable tasks: 30 executed, 9 up-to-date
Consider enabling configuration cache to speed up this build: https://docs.gradle.org/9.2.1/userguide/configuration_cache_enabling.html
lsyes@lsyes-loongsonls3a60007a20001wv01crb:~/geogebra$ 

