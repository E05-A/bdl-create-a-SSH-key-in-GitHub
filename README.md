# SSH Key in GitHub
## To crate an SSH Key in GitHub, you can follow these steps:
1. **Open Terminal:** Launch the Terminal application on your Ubuntu system. You can do this by pressing Ctrl+Alt+T or by searching for "Terminal" in the application launcher.
2. **Generate SSH key:** In the Terminal, enter the following command:

```bash
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```
Replace "your_email@example.com" with your own email address associated with your GitHub account. You can also choose a different file name or location for the SSH key if you prefer.

3. **Enter passphrase (optional):** You have the option to set a passphrase for added security. Press Enter to leave it blank if you don't want to use a passphrase.
4. **Start the SSH agent:** Run the following command to start the SSH agent:
```bash
eval "$(ssh-agent -s)"
```
5. **Add the SSH key to the SSH agent:** Use the following command to add your SSH key to the SSH agent:
```bash
ssh-add ~/.ssh/id_rsa
```
6. **Copy the SSH key:**  Run the following command to copy the contents of the SSH public key to your clipboard:
```bash
cat ~/.ssh/id_rsa.pub
```
7. **Add the SSH key to your GitHub account:** 

- Go to the GitHub website (github.com) and sign in to your account.
- Click on your profile picture in the top-right corner, and select **Settings** from the dropdown menu.
- In the left sidebar, click on SSH and GPG keys.
- Click on the **New SSH key** button.
- Provide a title for the SSH key (e.g., "My SSH Key").
- Paste the contents of your clipboard into the **Key** field.
- Click the **Add SSH key** button.

Congratulations! You have now created an SSH key and added it to your GitHub account. You can use this SSH key to securely authenticate with GitHub repositories and services.

