# This is an Example Repository	
Learn Git - this Repo is dedicated to learn Git and GitHub.

 had Two-Factor Authentication enabled on Github, this makes is so you will fail when entering your username and password even when they are correct.

Here is what I had to do:

git config --global --unset user.password

Then run your git command (ex. git push) and enter your username. For the password you need to generate a Personal Access Token.

Go to https://github.com/settings/profile 
select the Developer Settings on the right. 
Select Personal Access Token Generate new token. 
Copy the generated token and use it as the password in terminal.

#Caching your GitHub credentials in Git
You can tell Git to remember your credentials by using a credential helper, so that you don’t have to enter your username and password every time you clone a GitHub repository.

On Mac, you can use osxkeychain helper .

Use the following command on your terminal:

git config --global credential.helper osxkeychain
This tells Git to use the osxkeychain credentials helper.

Once you have authenticated successfully, your credentials will be stored in the MacOS keychain and will be used every time you clone your GitHub repository.

From this point on, you won’t have to re-enter your credentials unless you change your credentials (username, password) on GitHub.