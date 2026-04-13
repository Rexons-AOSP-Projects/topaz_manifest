1. Generate the SSH Key

Bash
ssh-keygen -t ed25519 -C "your_email@example.com"



2. Add the Key to the SSH Agent

Bash
eval "$(ssh-agent -s)"
Add your new private key to the agent:

Bash
ssh-add ~/.ssh/id_ed25519


3. Add the Public Key to GitHub

Bash
cat ~/.ssh/id_ed25519.pub


4. Test the Connection

Bash
ssh -T git@github.com
