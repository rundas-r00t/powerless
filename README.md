# powerless
a stand-alone powershell interpreter that you can use to circumvent group policies preventing powershell

full credit to the original unknown author: https://decoder.cloud/2017/11/02/we-dont-need-powershell-exe/

basically the way this works is that the c# code creates a stand-alone intepreter that you can use with cmd prompt. why does this work? because powershell itself is a .NET interpreter/scripting engine for the front-end. so we can do this same .NET interpretation via C# instead of powershell.

the powerless.cs files is the source to create the intepreter. compile the source with this command: 

`C:\Windows\Microsoft.NET\Framework64\v4.0.30319\csc.exe /reference:C:\Windows\Microsoft.NET\assembly\GAC_MSIL\System.Management.Automation\v4.0_3.0.0.0__31bf3856ad364e35\system.management.automation.dll /out:c:\YOURPATHHERE\powerless.exe c:\YOURPATHHERE\powerless.cs`

and this will create the `powerless.exe` file in the file list above. (or you can just download powerless.exe and trust that i compiled it correctly.)
