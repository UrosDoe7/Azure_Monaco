install-Monaco


download the lab
Copy the command with the copy button in the left corner.
Paste the command on you VM.

cd;
git clone https://github.com/dynatrace-ace-services/easy-dynatrace-with-monaco.git
download monaco (monaco-linux-amd64 -more distrib here)

cd;cd easy-dynatrace-with-monaco;
wget https://github.com/dynatrace-oss/dynatrace-monitoring-as-code/releases/latest/download/monaco-linux-amd64;
mv monaco-linux-amd64 monaco;
chmod +x monaco
new version NEW_CLI=1
In this lab we will use only the new cli version of monaco.
click here for documentation

export NEW_CLI=1;
cd;cd easy-dynatrace-with-monaco;
./monaco --version
expected result image

to have more help

cd;cd easy-dynatrace-with-monaco;
./monaco -h
image

create your token
Go to your Dynatrace environment : Settings > Integration > Dynatrace API > Generate Token
with these privileges (more info about token permission for monaco here:


tip: keep the value of the token you will not be able to display it afterwards 
the environment.yaml contains the configuration of your dynatrace tenants


export MyTenant="1234.live.dynatrace.com"
export MyToken=<your token> 
dynatrace saas tenant (and free trial) : "1234.live.dynatrace.com" (without https:// and / at the end of the line)
dynatrace managed tenant : "1234.dynatrace-managed.com/e/abc123etc" (without https:// and / at the end of the line)

validate the main variables for monaco

echo "NEW_CLI="$NEW_CLI;echo "MyTenant=https://"$MyTenant;echo "MyToken="$MyToken
start with a backup of the configuration
monaco will backups your main Dynatrace configuration
the directory free_trial is created localy (lab_monaco/free_trial) with all you json configuration files exported.

cd;cd easy-dynatrace-with-monaco;
./monaco download -e=environments.yaml mydownload
look at the configuration types backuped by monaco

cd;cd easy-dynatrace-with-monaco;
ls -lrt mydownload/free_trial
