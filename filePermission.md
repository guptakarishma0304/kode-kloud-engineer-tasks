There are new requirements to automate a backup process that was performed manually by the xFusionCorp Industries system admins team earlier. To automate this task, the team has developed a new bash script xfusioncorp.sh. They have already copied the script on all required servers, however they did not make it executable on one the app server i.e App Server 2 in Stratos Datacenter.
Please give executable permissions to /tmp/xfusioncorp.sh script on App Server 2. Also make sure every user can execute it.


[steve@stapp02 tmp]$ history
    1  sudo su
    2  ./tmp/xfusioncorp.sh
    3  cd tmp
    4  /tmp/xfusioncorp.sh
    5  ls -ls
    6  ls -la
    7  sudo chmod +x /tmp
    8  ls -la
    9  cd /tmp
   10  ls
   11  xfusioncorp.sh
   12  ./xfusioncorp.sh
   13  ls -la
   14  sudo chmod +x xfusioncorp.sh
   15  ./xfusioncorp.sh
   16  cd ..
   17  ./xfusioncorp.sh
   18  /tmp/xfusioncorp.sh
   19  cd /tmp
   20  ls -lrt
   21  ls -ld /tmp
   22  sudo chmod +r xfusioncorp.sh
   23  ls -la
   24  history
   
Hello,

Thank you for reporting this. Since its a bash script not a normal file so it is asked to give it executable permission so that server users can run the script later whenever needed.

Please note that in case of bash script bash is the interpreter that is actually going to execute the script and the interpreter needs to read the script so even if you have given it only executable permission the interpreter i.e bash will not be able to execute it so you had to give it read permission as well along with execute permission.

Just for reference: https://unix.stackexchange.com/questions/34202/can-a-script-be-executable-but-not-readable 11

I hope it clears your doubt :slight_smile:
