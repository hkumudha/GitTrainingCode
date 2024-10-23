Generate a New SSH Key 
ssh-keygen -t ed25519 -C your_email@example.com

Add the SSH Key to the SSH Agent 
eval "$(ssh-agent -s)“ ssh-add ~/.ssh/id_ed25519

Add SSH Key to GitHub 
clip < ~/.ssh/id_ed25519.pub

Go to GitHub and log into your account. In the top-right corner, click on your profile picture, then go to Settings. In the left sidebar, click SSH and GPG keys. Click New SSH key. In the "Title" field, add a descriptive name for the key. Paste your SSH key into the "Key" field and click Add SSH key.

Test SSH Connection 
ssh -T git@github.com
