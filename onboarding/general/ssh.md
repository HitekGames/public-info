# Creating and Connecting SSH Keys to GitHub
If you already have Git installed, right-click anywhere to see a 
context menu with an option to launch Git Bash.

- Open Git Bash through this context menu.
- In the open console, enter the following command to generate an SSH key (don't forget to replace your_email@example.com with your actual email):
  `ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`
- When prompted to enter the file path to save the key, simply press Enter to accept all default values (unless you need something specific).
- Continue pressing Enter to skip the passphrase entry for the key.

After these steps, your key will be created, and you can verify it by running the following command:
`cat ~/.ssh/id_rsa.pub`  
This command will output your public SSH key, which you need to copy and add to the SSH settings on servers or services where you plan to use SSH connections.

Example:
`ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQC4dWKfEY+j7B+G5ANUJ20kS5AQYFltNlkvBnlyKkSFGFpI5aU/B8FjSUD2UD7Ebn4M6sChlZVqOs2P+tAhtibefnx1HU8jwKj+2+KkfvJ5Vnt7q0LdP2s/YZttQFWT9D+kW6DGPQx6zhw6quPT0WnCvbZOu7NF3qCfX3tJLj8x8XHCzGqIcikQ/nlBqhK6vG8UY2hMifF0sDRtgy6Zr6lSM7/cK+d6GsoJKZM9xlhPHE+zicNXWmrfCI8hcR3D/xG6FGoLkEHpsw98XVHz0D7K0dF5ALxpW0OJut1rk2BWpKbqPlG5y9aTw2MSKeYTxRWW5QeR4cGHsifYhHtqLjF example@example.com`

## Connecting to GitHub
To add your public SSH key to GitHub, follow these steps:

- Go to GitHub and log into your account.
- Navigate to settings
- Click on your avatar in the top right corner and select "Settings."
- In the left sidebar, select "SSH and GPG keys."
- Click the "New SSH key" or "Add SSH key" button if you already have saved keys.
- In the "Title" field, enter a name for the key that makes it easy for you to identify.
- In the "Key" field, paste your public SSH key that you copied earlier using the command `cat ~/.ssh/id_rsa.pub`.
- Click the "Add key" button.

After these steps, your SSH key will be added to your GitHub account, and you can use SSH to interact with repositories on GitHub.
