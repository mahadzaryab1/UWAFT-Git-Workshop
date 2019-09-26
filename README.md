# Initial Setup - Generating SSH Ke
1. Open Git Bash on Windows or Terminal on MacOS
2. Copy and paste the text below replacing it with the email address you used to sign up for github. This will generate a new SSH key for you.   
```
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```
3. When you're prompted to "Enter a file in which to save the key," press Enter. This accepts the default file location.
```
> Enter a file in which to save the key (/c/Users/you/.ssh/id_rsa):[Press enter]
```
4. You will be prompted to enter a passphrase. Press enter to leave this empty. 
```
> Enter passphrase (empty for no passphrase): [Type a passphrase]
> Enter same passphrase again: [Type passphrase again]
```

# Initial Setup - Adding SSH key to the ssh-agent
1. Start the ssh-agent by copying and pasting the following command.
```
eval $(ssh-agent -s)
```
2. Add your SSH private key to the ssh-agent by copying and pasting the following command
```
ssh-add ~/.ssh/id_rsa
```

# Initial Setup - Adding SSH key to your Github account
1. Copy the contents of the ssh key to your clipboard.
```
clip < ~/.ssh/id_rsa.pub
```
2. On Github, Navigate to Settings -> SSH and GPG Keys -> New SSH Key
3. Paste the key you copied and give your key a unique and identifiable title
