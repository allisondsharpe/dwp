<h1> Portfolio Deployment Plan </h1>

<h2> Production </h2> 

1. Create new local dev directory 
	<ul>
		<li> Access this directory using cd ~/Directory folder within Terminal </li>
		<li> Create a directory using $ mkdir 'newDirectoryName' inside the parent directory and use this directory to access production/staging servers </li>
	</ul>
	
2. Once accessed, use $ git init --bare to create an empty repository
	<ul>
		<li> You will use this repository to access your live server </li>
	</ul>	

3. Create index.html file by typing $ touch index.html
	<ul>
		<li> You will then be presented with an input field. Just type 'Hello, world' for now. </li>
	</ul>

4. In order for this file to be pushed to your live server, you will need to type $ git add -A into the Terminal
	<ul>
		<li> This will tell the Terminal that you want to add a file to the Github remote repo <li>
	</ul>
	
5. After adding the file, you will need to commit the file by typing $ git commit -m 'commit message goes here' 
	<ul>
		<li> This line will commit the file, but will not be pushed to your live server just yet </li>
	</ul>	

6. In order for the file to be pushed to your live server, you will need to add your remote server within the directory by typing $ git remote add prodServer ssh://UserName@IPAddress/var/repos/SiteName.git
	<ul>
		<li> prodServer is the alias name for your production server, it can be called anything </li>
		<li> UserName is the username created for your live server, (ex: Digital Ocean) and the IP Address can either be your IP Address of the live server or your domain name </li>
	</ul>
	
7. Type $ git push prodServer master into your Terminal. You should see a message stating that this was successful 	
	
8. After following these steps, you should see your index.html file on your live server

9. Now you need to access your local Github repo by adding a new repository on Github.com
	<ul>
		<li> This repo can be called anything, for ex: 'dwp' </li>
	</ul>	
	
10. After creating your repo, you will see a section with a title reading 'Create a New Repository On the Command Line'
	<ul>
		<li> Copy the line $ git remote add yourGithubAliasName https://github.com/yourgithubusername/nameofyourlocalrepo.git </li>
		<li> Paste the line into your Terminal. Your new alias name will be used to access your local repo from your remote repo </li>
	</ul>
	
11. Finally, push the files created within your remote repo to your local repo by typing $ git push yourGithubAliasName master into your terminal	

<h2> Staging </h2> 

1. Copy the steps from 1-8. Do not copy the steps from 9-11 since this server is only meant to be used locally and not publicly
