# <https://github.com/sbt/sbt/issues/8198>

```
[sbt_options] declare -a sbt_options=()
[debug] running native client
# Executing command line:
/opt/hostedtoolcache/sbt/1.11.2/sbt/bin/sbtn-x86_64-pc-linux
--sbt-script=/opt/hostedtoolcache/sbt/1.11.2/sbt/bin/sbt
-v
"compile ; reload ; compile"

[info] entering *experimental* thin client - BEEP WHIRR
[info] server was not detected. starting an instance
[sbt_options] declare -a sbt_options=()
[process_args] java_version = '8'
# Executing command line:
java
-Dfile.encoding=UTF-8
-Dsbt.io.virtual=true
-Dsbt.script=/opt/hostedtoolcache/sbt/1.11.2/sbt/bin/sbt
-Xms1024m
-Xmx1024m
-Xss4M
-XX:ReservedCodeCacheSize=128m
-jar
/opt/hostedtoolcache/sbt/1.11.2/sbt/bin/sbt-launch.jar
--detach-stdio

[info] [launcher] getting org.scala-sbt sbt 2.0.0-M5  (this may take some time)...
[info] [launcher] getting Scala 3.7.2 (for sbt)...
[info] welcome to sbt 2.0.0-M5 (Temurin Java 1.8.0_462)
[info] loading project definition from /home/runner/work/sbt-2-0-0-M5-autoImport-not-found-error/sbt-2-0-0-M5-autoImport-not-found-error/project
[info] set current project to sbt-2-0-0-m5-autoimport-not-found-error (in build file:/home/runner/work/sbt-2-0-0-M5-autoImport-not-found-error/sbt-2-0-0-M5-autoImport-not-found-error/)
[info] sbt server started at local:///home/runner/.sbt/2.0.0-M5/server/a69a79090680c63e0111/sock
[info] started sbt server
[info] terminate the server with `shutdown`
> compile ; reload ; compile
[info] welcome to sbt 2.0.0-M5 (Temurin Java 1.8.0_462)
[info] loading project definition from /home/runner/work/sbt-2-0-0-M5-autoImport-not-found-error/sbt-2-0-0-M5-autoImport-not-found-error/project
java.lang.NoClassDefFoundError: wartremover/WartRemover$autoImport$
	at $Wrapfbaf9664ce$.$sbtdef(build.sbt:1)
	at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)
	at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.lang.reflect.Method.invoke(Method.java:498)
	at sbt.internal.Eval$.getValue(Eval.scala:411)
	at sbt.internal.Eval.$anonfun$1(Eval.scala:122)
	at sbt.internal.EvaluateConfigurations$.evaluateDslEntry$$anonfun$1(EvaluateConfigurations.scala:250)
	at sbt.internal.EvaluateConfigurations$.$anonfun$7(EvaluateConfigurations.scala:178)
	at scala.collection.immutable.List.map(List.scala:247)
	at scala.collection.immutable.List.map(List.scala:79)
	at sbt.internal.EvaluateConfigurations$.evaluateSbtFile$$anonfun$1(EvaluateConfigurations.scala:178)
	at sbt.internal.Load$.loadSettingsFile$1(Load.scala:1271)
	at sbt.internal.Load$.memoLoadSettingsFile$1$$anonfun$1(Load.scala:1281)
	at scala.collection.mutable.HashMap.getOrElse(HashMap.scala:451)
	at sbt.internal.Load$.memoLoadSettingsFile$1(Load.scala:1284)
	at sbt.internal.Load$.loadFiles$1$$anonfun$2(Load.scala:1291)
	at scala.collection.immutable.List.map(List.scala:247)
	at scala.collection.immutable.List.map(List.scala:79)
	at sbt.internal.Load$.loadFiles$1(Load.scala:1291)
	at sbt.internal.Load$.discoverProjects(Load.scala:1311)
	at sbt.internal.Load$.discover$1(Load.scala:1001)
	at sbt.internal.Load$.loadTransitive(Load.scala:1067)
	at sbt.internal.Load$.loadProjects$1(Load.scala:817)
	at sbt.internal.Load$.$anonfun$47(Load.scala:820)
	at sbt.internal.Load$.timed(Load.scala:1579)
	at sbt.internal.Load$.loadUnit$$anonfun$1(Load.scala:821)
	at sbt.internal.Load$.timed(Load.scala:1579)
	at sbt.internal.Load$.loadUnit(Load.scala:871)
	at sbt.internal.Load$.$anonfun$32$$anonfun$1(Load.scala:552)
	at sbt.internal.BuildLoader$.componentLoader$$anonfun$1$$anonfun$2$$anonfun$1$$anonfun$1(BuildLoader.scala:180)
	at sbt.internal.BuildLoader.apply(BuildLoader.scala:246)
	at sbt.internal.Load$.loadURI$1(Load.scala:619)
	at sbt.internal.Load$.loadAll(Load.scala:635)
	at sbt.internal.Load$.loadURI(Load.scala:565)
	at sbt.internal.Load$.load(Load.scala:538)
	at sbt.internal.Load$.$anonfun$10(Load.scala:266)
	at sbt.internal.Load$.timed(Load.scala:1579)
	at sbt.internal.Load$.apply(Load.scala:266)
	at sbt.internal.Load$.defaultLoad(Load.scala:60)
	at sbt.BuiltinCommands$.doLoadProject(Main.scala:958)
	at sbt.BuiltinCommands$.loadProjectImpl$$anonfun$2(Main.scala:912)
	at sbt.Command$.applyEffect$$anonfun$2$$anonfun$1(Command.scala:151)
	at sbt.Command$.applyEffect$$anonfun$1$$anonfun$1(Command.scala:146)
	at sbt.Command$.process(Command.scala:192)
	at sbt.MainLoop$.$anonfun$12(MainLoop.scala:261)
	at scala.Option.getOrElse(Option.scala:201)
	at sbt.MainLoop$.process$1(MainLoop.scala:261)
	at sbt.MainLoop$.processCommand(MainLoop.scala:306)
	at sbt.MainLoop$.next$$anonfun$1$$anonfun$1(MainLoop.scala:165)
	at sbt.State$StateOpsImpl$.runCmd$1(State.scala:270)
	at sbt.State$StateOpsImpl$.process$extension(State.scala:306)
	at sbt.MainLoop$.next$$anonfun$1(MainLoop.scala:165)
	at sbt.internal.util.ErrorHandling$.wideConvert(ErrorHandling.scala:24)
	at sbt.MainLoop$.next(MainLoop.scala:166)
	at sbt.MainLoop$.runLoop(MainLoop.scala:147)
	at sbt.MainLoop$.run(MainLoop.scala:142)
	at sbt.MainLoop$.runWithNewLog$$anonfun$1(MainLoop.scala:120)
	at sbt.io.Using.apply(Using.scala:41)
	at sbt.MainLoop$.runWithNewLog(MainLoop.scala:113)
	at sbt.MainLoop$.runAndClearLast(MainLoop.scala:69)
	at sbt.MainLoop$.runLoggedLoop(MainLoop.scala:52)
	at sbt.MainLoop$.runLogged(MainLoop.scala:45)
	at sbt.StandardMain$.runManaged(Main.scala:230)
	at sbt.xMain$.run$$anonfun$3(Main.scala:141)
	at scala.util.DynamicVariable.withValue(DynamicVariable.scala:59)
	at scala.Console$.withIn(Console.scala:227)
	at sbt.internal.util.Terminal$.withIn(Terminal.scala:643)
	at sbt.internal.util.Terminal$.withStreams$$anonfun$1(Terminal.scala:421)
	at scala.util.DynamicVariable.withValue(DynamicVariable.scala:59)
	at scala.Console$.withOut(Console.scala:164)
	at sbt.internal.util.Terminal$.withOut$$anonfun$2(Terminal.scala:633)
	at scala.util.DynamicVariable.withValue(DynamicVariable.scala:59)
	at scala.Console$.withErr(Console.scala:193)
	at sbt.internal.util.Terminal$.withOut(Terminal.scala:633)
	at sbt.internal.util.Terminal$.withStreams(Terminal.scala:421)
	at sbt.xMain$.withStreams$1(Main.scala:92)
	at sbt.xMain$.run(Main.scala:143)
	at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)
	at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.lang.reflect.Method.invoke(Method.java:498)
	at sbt.internal.XMainConfiguration.run(XMainConfiguration.java:68)
	at sbt.xMain.run(Main.scala:49)
	at xsbt.boot.Launch$.$anonfun$run$1(Launch.scala:149)
	at xsbt.boot.Launch$.withContextLoader(Launch.scala:176)
	at xsbt.boot.Launch$.run(Launch.scala:149)
	at xsbt.boot.Launch$.$anonfun$apply$1(Launch.scala:44)
	at xsbt.boot.Launch$.launch(Launch.scala:159)
	at xsbt.boot.Launch$.apply(Launch.scala:44)
	at xsbt.boot.Launch$.apply(Launch.scala:21)
	at xsbt.boot.Boot$.runImpl(Boot.scala:78)
	at xsbt.boot.Boot$.run(Boot.scala:73)
	at xsbt.boot.Boot$.main(Boot.scala:21)
	at xsbt.boot.Boot.main(Boot.scala)
Caused by: java.lang.ClassNotFoundException: wartremover.WartRemover$autoImport$
	at java.net.URLClassLoader.findClass(URLClassLoader.java:387)
	at java.lang.ClassLoader.loadClass(ClassLoader.java:418)
	at java.lang.ClassLoader.loadClass(ClassLoader.java:351)
	... 95 more
[error] java.lang.NoClassDefFoundError: wartremover/WartRemover$autoImport$
[error] Use 'last' for the full log.
[warn] Project loading failed: (r)etry, (q)uit, (l)ast, or (i)gnore? (default: r)
[error] sbt server disconnected
```
