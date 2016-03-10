<h1> Portfolio Deployment Plan </h1>

<h2> Production </h2> 

1. Create new local dev directory 
	<ul>
		<li> Access this directory by typing cd ~/Directory within Terminal </li>
		<li> Create a directory by typing $ mkdir 'newDirectoryName' inside the parent directory and use this directory to access your production/staging servers </li>
	</ul>
	
2. Once accessed, type $ git init --bare to create an empty repository
	<ul>
		<li> You will use this repository to access your live server </li>
	</ul>	

3. Create an index.html file by typing $ touch index.html
	<ul>
		<li> You will then be presented with an input field. Just type 'Hello, world' and save the file for now. </li>
	</ul>

4. In order for this file to be pushed to your live server, you will need to type $ git add -A into the Terminal
	<ul>
		<li> This will tell the Terminal that you want to add a file to your remote repo </li>
	</ul>
	
5. After adding the file, you will need to commit the file by typing $ git commit -m 'commit message goes here' 
	<ul>
		<li> This line will commit the file, but will not be pushed to your live server just yet </li>
	</ul>	

6. In order for the file to be pushed to your live server, you will need to add your remote server within the directory by typing $ git remote add prodServer ssh://UserName@IPAddress/var/repos/SiteName.git
	<ul>
		<li> prodServer is the alias name for your production server, it can be called anything of your choosing </li>
		<li> UserName is the username created for your live server, (ex: Digital Ocean) and the IP Address can either be your IP Address of the live server or your domain name </li>
	</ul>
	
7. Type $ git push prodServer master into your Terminal. If successful, you should receive no error messages
	
8. After following these steps, you should see your index.html file on your live server

9. Now you need to push your files to your local Github repo by adding a new repository on Github.com
	<ul>
		<li> This repo can be called anything, for ex: 'dwp' </li>
	</ul>	
	
10. After creating your repo, you will see a section with the heading 'Create a New Repository On the Command Line'
	<ul>
		<li> Copy the line $ git remote add yourGithubAliasName https://github.com/yourgithubusername/nameofyourlocalrepo.git </li>
		<li> Paste the line into your Terminal. Your new alias name will be used to access your local repo from your remote repo </li>
	</ul>
	
11. Finally, push the files created within your remote repo to your local repo by typing $ git push yourGithubAliasName master into the Terminal

<h2> Staging </h2> 

1. Copy the steps from 1-8. Do not copy the steps from 9-11 since this server is only meant to be accessed by you and not by the public
