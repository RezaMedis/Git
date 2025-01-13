----------------------------------------------------------------------------------------
|                     Connect GitHub account with Git using VS Code                    |
----------------------------------------------------------------------------------------
First Install Git and VS Code (if not already installed).

---------------------------------------------------------------------------------------
Configure Git
Open a terminal or Git Bash and run the following commands to set up your Git username and email (these will be associated with your commits):
	# git config --global user.name "Your GitHub Username"
	# git config --global user.email "your-email@example.com"
Set VS Code as your default editor for Git:
	# git config --global core.editor "code --wait"

---------------------------------------------------------------------------------------
Authenticate with GitHub Using SSH (Recommended)

Generate an SSH Key:
	# ssh-keygen -t ed25519 -C "your-email@example.com"

Press Enter to accept the default file location and optionally set a passphrase.

Start the SSH Agent:
	# eval "$(ssh-agent -s)"

Add the key to the SSH agent:
	# ssh-add ~/.ssh/id_ed25519

Copy the SSH public key:
	# clip < ~/.ssh/id_ed25519.pub

*This copies your key to the clipboard.

Add the SSH Key to GitHub:
-Go to Settings > SSH and GPG keys > New SSH key.
-Paste the key and save.

---------------------------------------------------------------------------------------
Test SSH Configuration
If you're using SSH (git@github.com:), test the SSH connection:
	# ssh -T git@github.com

If it's successful, you’ll see a message similar to:
	# Hi GitUserName! You've successfully authenticated, but GitHub does not provide shell access.

---------------------------------------------------------------------------------------
Add GitHub Repository as Remote
Use the repository URL from GitHub For SSH:
	# git remote add origin git@github.com:YourUsername/YourRepo.git

---------------------------------------------------------------------------------------
to create a new repository on the git bash:

user@PC ~ (master):
	$ echo "# RepoName" >> README.md
user@PC ~ (master):
	$ git init
user@PC ~ (master):
	$ git add README.md
user@PC ~ (master):
	$ git commit -m "first commit"
user@PC ~ (master):
	$ git branch -M main
user@PC ~ (master):
	$ git remote add origin git@github.com:GitAccountName/RepoName.git
user@PC ~ (master):
	$ git push -u origin main

---------------------------------------------------------------------------------------
Clone a GitHub Repository:

	$ mkdir Config.git
	$ cd Config.git
	$ git clone git@github.com:RezaMedis/Config.git
	$ cd Config.git
---------------------------------------------------------------------------------------
to push an existing repository from the git bash:

user@PC ~ (master):
	$ git remote add origin git@github.com:GitAccountName/RepoName.git
user@PC ~ (master):
	$ git branch -M main
user@PC ~ (master):
	$ git push -u origin main

---------------------------------------------------------------------------------------
to push an existing repository In VS Code terminal:
	# git clone git@github.com:GitAccountName/RepoName.git
	# cd RepoName

---------------------------------------------------------------------------------------
Stage Your Files
Stage all files for commit:
	# git add .

---------------------------------------------------------------------------------------

Commit Your Changes
Create a commit with a message describing your changes:
	# git commit -m "Your commit message"

---------------------------------------------------------------------------------------
Push Your Code to GitHub
Push the code to the remote repository:
	# git push -u origin main

If the default branch is named master instead of main, use:
	# git push -u origin master

Using VS Code Git Integration:
-Open the repository folder in VS Code.
-Click the Source Control icon in the Activity Bar.
-Use the interface to stage, commit, and push changes.
-You're now set up to manage your code on GitHub using Git and Visual Studio Code!

---------------------------------------------------------------------------------------
|                              Additional Commands                                    |
---------------------------------------------------------------------------------------
Check Status:
	# git status

Pull Latest Changes:
	# git pull origin main

To push your code, run:
	# git push -u origin main

*origin: The remote name for your GitHub repository.
*main: The branch name (adjust to master if your default branch is named that).

---------------------------------------------------------------------------------------
Check and Confirm Remote
Ensure you have the correct remote repository set:
	# git remote -v

If it doesn't show your GitHub repository, add it:
	# git remote add origin git@github.com:YourUsername/Config.git

---------------------------------------------------------------------------------------
Check Branch Name
Verify the current branch name:
	# git branch

If the branch isn't main, rename it or adjust the push command
To rename the branch to main:
	# git branch -M main

---------------------------------------------------------------------------------------
Final Push
Now push the code:
	# git push -u origin main

After doing this once, future pushes can simply be:
	# git push



<-- END OF FILE -->