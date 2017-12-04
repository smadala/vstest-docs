# Troubleshoot vstest
Note
This document helps to figure out root cause of unexpected behavior of vstest a.k.a Testplatform. Testplatform has many clients (IDEs, `dotnet test`, VSTest Task, etc ..) and extentions (Adapters, Loggers, Data collectors, etc..). Unexpected behavior can occurs due to issue in vstest, clients, adapters and tests itself.


## FAQ's
### How to collect vstest logs from Visual Studio?
 To Run/Discover tests from VS, involves vstest client(Test Explorer) and Testplatform. 
 - **Test Explorer Logs:** <br>
 >  To collect the Test Explorer logs enable Test logging level to Diagnostic(`Options -> Test -> Logging -> Logging Level -> Diagnostic` for VS >=15.3, set environment variable VS_UTE_DIAGNOSTICS to 1 for VS < 15.3). Logs appears in Output window -> Tests pane.
 - **Testplatform Logs:** <br>
  > For VS >= 15.5 or .NET Core test projects

  Enable [Collect trace using config file](diagnose.md#collect-trace-using-config-file) restart VS, vstest.console logs logged to given file in config file and testhost log file name appears in Output window -> Tests pane(E.g: Logging TestHost Diagnostics in file: C:\Users\samadala\AppData\Local\Temp\vstest.console.32920.TpTrace.host.17-12-04_14-56-24_68960_9.log)

  > For VS < 15.5

  Follow blog [here](https://blogs.msdn.microsoft.com/aseemb/2012/03/01/how-to-enable-ute-logs/).
### How to collect vstest logs from command line?
Follow [Collect traces using command line](diagnose.md#collect-traces-using-command-line). Log file names appears on console like below example. 
> Logging Vstest Diagnostics in file: C:\Users\samadala\src\vstest\test\TestAssets\SimpleTestProject3\log.txt
Logging TestHost Diagnostics in file: C:\Users\samadala\src\vstest\test\TestAssets\SimpleTestProject3\log.host.17-12-04_15-17-09_11057_4.txt




