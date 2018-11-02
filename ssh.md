#### If you are on windows you must install Git Bash or else the ssh-keygen command won't work.
#### https://git-scm.com/download/win

## SSH Keys

An SSH key allows you to establish a secure connection between your computer and GitLab. To generate a new SSH key, use the following command:
```
ssh-keygen -t rsa -C "$your_email"
```

Press enter for default settings for all remaining prompts. Once generated, you need to copy & paste the key to the 'SSH Keys' section under the Settings section from the top right corner of GitLab. To copy your public key to the clipboard, use the code below.

#### Windows:
```
clip < ~/.ssh/id_rsa.pub
```

#### Mac:
```
pbcopy < ~/.ssh/id_rsa.pub
```

#### GNU/Linux (requires xclip):
```
xclip -sel clip < ~/.ssh/id_rsa.pub
```