To get running, I ran the  mysql_db_struct.sql ddl in a client
then the 'package' goal on maven

drop the war in apache/webapps
run http://localhost:8080/jforum/install.jsp to set it up

then in the installed app, 
Remove the line "install = net.jforum.view.install.InstallAction" from the file WEB-INF/config/modulesMapping.properties

The directory "images", "tmp", "upload" and "WEB-INF" (and their sub-directories) should have write permission for the user who started the app

Open the file WEB-INF/config/SystemGlobals.properties and search for a key named user.hash.sequence. - change it a bit




--

tips

If you want to deny anonymous post in JForum, just go to Admin Control Panel > Group Managment > General > Permission
Choose all boards in the deny anonymous post section. 