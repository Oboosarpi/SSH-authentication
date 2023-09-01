## About SSH
Using the SSH protocol, you can connect and authenticate to remote servers and services. With SSH keys, you can connect 
to GitHub without supplying your username and personal access token at each visit. 
You can also use an SSH key to sign commits.

You can access and write data in repositories on GitHub.com using SSH (Secure Shell Protocol). When you connect via SSH,
you authenticate using a private key file on your local machine. For more information about SSH, see Secure Shell on
Wikipedia.

When you set up SSH, you will need to generate a new private SSH key and add it to the SSH agent. You must also add the
public SSH key to your account on GitHub before you use the key to authenticate or sign commits. For more information,
see "Generating a new SSH key and adding it to the ssh-agent", "Adding a new SSH key to your GitHub account" and 
"About commit signature verification."

nb: *the above text is from github documentation about ssh. Fully copied, nothing changed*

**Below are the steps to use github ssh **
** also the steps to solve: **
- git@github.com: Permission denied (publickey).
- fatal: Could not read from remote repository.

- Please make sure you have the correct access rights
- and the repository exists.

1. After initializing git, adding necessary files , committing changes, linking local repo to remote repo using 
*ssh* format instead of *https* format and pushing codes to remote repo
2. *you might encounter the above error if you haven't configured ssh* so on terminal, input: 
`ssh-keygen -t ed25519 -C "your_email@example.com"` *replace your_email@example.com with your email you use to register
on github
3. Press 'Enter' key to save it on default file and press 'Enter' again to skip the paraphrasing
4. A private key will be automatically generated, you have to copy it and paste it on SSH agent on Github, by:
`pbcopy < ~/.ssh/id_ed25519.pub`
5. On github, click on your profile, go to settings, scroll down to *SSH and GPG Keys* and head to *New SSH Key* . Then
paste the copied private key at the box provided. The public key will appear automatically
6. Now you are set to push your codes to remote repo anytime , w'out errors😁




**Official documentation about generating ssh key can be found here:** [Generating a new SSH key](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent.com)

