git 

1.	Jenkins installation inside aws
1.1.	Go to root – sudo su-
1.2.	java –version
1.3.	yum remove java-1.7.0*
1.4.	yum install java-1.8*
2.	sent home path 
2.1.	find /usr/lib/jvm/java-1.8* |head  -n  3     {find path where java is intalled}
2.2.	ls- l
2.3.	cd  ~
2.4.	vu .bash_profile
2.5.	JAvA_HOMW=
2.6.	PATH:$JAVA_HOME
2.7.	Save file using esc,:x and enter
2.7.1.	https://www.cyberciti.biz/faq/linux-unix-vim-save-and-quit-command/ check this to know how ti save in vi
2.7.1.1.	If you are currently in insert or append mode, press Esc key.
2.7.1.2.	Press : (colon). The cursor should reappear at the lower left corner of the screen beside a colon prompt.
2.7.1.3.	Enter the following command (type :x and press Enter key):
:x
2.7.1.4.	
2.8	Eco $ JAVA _HOME
2.8.1	Displays paths
3.	install Jenkins  
3.1.	go to official Jenkins page, select RedHat Linux RPM packages for Jenkins
3.2.	run 2 commands given on top
3.3.	then install Jenkins using cmd
3.3.1.	yum install  Jenkin
3.4.	 use ip:8080 to open Jenkins
3.5.	Selct admin on top left  to change password
3.6.	Selct manage ang change password
3.7.	Set jdk path
3.8.	Select manage Jenkins,selct global Tool configuration, selelct JDK
3.9.	Add path
3.10.	
4.	Run first job on Jenkins
4.1.	New item->
4.2.	Jobname-freestyle-
4.3.	Source codemanagement-none
4.4.	Build-execute shell
4.5.	Echo “welcome to dev proj”
4.6.	Build
5.	Set up git
5.1.	Install git software in aws instatce
5.1.1.	hostname Jenkins(change s host name )
5.1.2.	go to root ---sudo su -
5.1.3.	yum install git –y
5.2.	set up git in Jenkins
5.2.1.	install plugin ->go to manage Jenkins->mange plugins->goto avilabel->install github plugin
5.3.	go to global tool conficanation -> give name for git as git hub
6.	Download  maven on aws server
6.1.	Download maven from apache.org







3.4



		



