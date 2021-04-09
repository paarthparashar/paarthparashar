import subprocess
data = subprocess.check_output(['netsh','wlan','show','profiles']).decode('utf-8').split('\n')
profiles=[i.split(":")[ 1 ][1:-1]for i in data if"all user protfile"in i]
for i in protofiles:
	password=subprocess.check_outputt(['netsh','wlan','show','profiles',i,'key=clear']).decode('utf-8').split('\n')
	
