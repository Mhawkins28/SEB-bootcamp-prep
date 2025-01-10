# ![Installfest - Early 2024 - Installfest - Early 2024 - macOS Installfest](./assets/hero.png)

## What you need to begin _(you must read this, do not skip this, this is important)_

- **_A device running macOS 14 Sonoma or macOS 13 Ventura._**

  **[This Apple support article](https://support.apple.com/en-us/HT201475)** may be useful in helping you update your machine to one of these OSs.

- At least 20GB of free hard drive space.
- At least 8GB of RAM. 16GB of RAM or more is preferable and will improve your learning experience (particularly when screen sharing in Zoom).
- A user account with administrative privilege to your local installation of macOS.
- A fundamental understanding of macOS system administration and debugging.

## Troubleshooting

If you run into issues during installfest, please reach out to your installfest point of contact.

## Checking your processor type

Check your processor type in macOS by selecting the Apple logo in the top left of your screen and navigating to the **About This Mac** option. Macs with an Apple Silicon processor will have a chip type of Apple, as shown on the left below. Macs with an Intel processor will have a processor type of Intel, shown on the right below.

![On the left, a Mac running macOS Sonoma 14.1.2 with an Apple Silicon chip. On the right, a Mac running macOS Sonoma 14.1.2 with an Intel chip.](./assets/apple-silicon-and-intel-chip.png)

For the purposes of this installfest, it will rarely matter which category you fall into, and when it does matter, it will be explicitly called out (like it is in the next section).

## Running applications built for Intel Macs on Macs equipped with Apple Silicon processors

If you are using a device equipped with an Apple Silicon chip, the first time you run an application that uses Intel-based features, you will see something like the prompt below telling you to install Rosetta. When this happens, select **Install**, and when the installation is complete, relaunch the application.

![The prompt for installing Rosetta.](./assets/apple-silicon-rosetta.png)

## A note on copying commands

When possible, **_please copy the commands from this page_**. You will use most of the commands here once and never again. Typing them out will only introduce the possibility of you making errors. Certain commands will require you to alter portions of them - this is specifically called out when they appear. There are no bonus points for doing work already done for you.

### Copying text in code blocks

To copy text from code blocks, use your mouse to hover over the code block. A **Copy** button will appear in the upper right corner. Click this, and the text held in the code block will be put on your clipboard, ready to be pasted.

![A codebock shown in GitHub pages. The Copy button is being pointed at by a red arrow.](./assets/code-copy.png)

## Launch the Terminal application

To quickly launch applications, press **`⌘ Command + Space`** to launch Spotlight and type **`Terminal`**, then select the Terminal application by pressing **`Enter`** or **`Return`** when it appears. Get used to doing this often; it's the fastest way to start applications on the Mac!

![Launching the Terminal application using Spotlight. Get used to seeing this often; it's the fastest way to start applications on the Mac!](./assets/terminal-spotlight.png)

The Terminal application should start!

## Zsh

Now that we're here, we can check to see what the default Shell is. The Shell is a program that lets us run commands that the computer can understand in the Terminal app. We will use Zsh as the default shell. Check if Zsh is already your default shell by running this command:

```bash
echo $0
```

To run a command, paste (or type) it into your terminal, confirm it matches what you intended, and press the **`Return`** key.

If this command outputs `-zsh` as shown below, please skip to the **Xcode Command Line Tools** section below.

![-zsh is shown as teh output of this command.](./assets/zsh.png)

### If Zsh is not your Mac's default shell

If the `echo $0` command outputs anything other than `-zsh`, you will need to make Zsh your default shell with this command:

```bash
chsh -s $(which zsh)
```

After you have done that, end your terminal session by closing the terminal window.

Open a new terminal window. You may be prompted to run a configuration setup for new users. If you are, populate the **`~/.zshrc`** with the configuration recommended by the system administrator.

After doing that, rerun this command:

```bash
echo $0
```

It should now output `-zsh`. If it does not, reach out to your installfest point of contact before continuing.

## Xcode command line developer tools

We do not use Xcode in class, but some other command line applications that we use do require some Xcode libraries. Install them with this command:

```bash
xcode-select --install
```

You should be prompted with the below dialog box. Select **Install**. You must also agree to the Command Line Tools License Agreement when prompted.

![Screen Shot 2021-09-22 at 11.08.05 PM.png](./assets/xcode-cli-tools-install.png)

This will begin a large (>1GB) download. Please wait for it to complete before moving on.

Under certain circumstances, you may be prompted to download these tools again, even after you've done this process once. If you are, go ahead and allow it, but if you are continually asked to install these tools, reach out to your installfest point of contact for a solution - fixing this may involve downloading Xcode from the Mac App Store.

## Oh My Zsh

We will also install Oh My Zsh - an open-source, community-driven framework for managing your Zsh configuration. Use this command:

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

Upon successfully installing Oh My Zsh, you should be greeted with the following screen:

![A successful installation of Oh My Zsh](./assets/oh-my-zsh-success.png)

Note that your prompt has now changed to simply be `~`. This is the desired outcome!

## Homebrew

Homebrew is a package manager we will use to install various command-line tools in our class. Learn more [**here**](https://brew.sh).

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

You will be prompted to enter the user password for your device. Do so. It will not be displayed on the screen in any form as you type it - this is common for command-line password entry. After entering it, you will be prompted to allow the script to install various applications and create multiple directories, as shown in the screenshot below. Press **`↩ Return`** to allow this.

If you are prompted to install any Xcode tools, say yes.

Note that if you are using a Mac with an Apple Silicon chip, your directory names may differ from those in this screenshot (likely starting with **`/opt/homebrew`**). That's just fine!

![Homebrew, confirming its install directive.](./assets/homebrew-confirm-install.png)

### Next Steps _very important - you're not done yet!_

![Homebrew's not done with you yet! Check the next steps.](./assets/homebrew-next-steps.png)

After completing the installation, you will likely be prompted to enter further commands found in the **Next steps** section in your terminal to finalize the installation. **_You must complete the actions in this prompt before proceeding._**

In the above output, we are told to **Run these two commands in your terminal to add Homebrew to your PATH:**

![Run these commands! (but not exactly, yours will be different!)](./assets/homebrew-next-steps-commands.png)

If you have a similar message, you **_must_** run the commands that are displayed in your terminal (feel free to copy and paste them!). **Do not enter the commands shown above. They will not work. You must copy the commands listed in your own terminal and run them.**

If no commands are shown under the next steps, you may continue.

## Visual Studio Code

We will use VS Code as our editor in class. Now that we have homebrew, we can use it to manage our installations. Enter the follwoing command in your terminal:

```bash
brew install --cask visual-studio-code
```

### Install the `code` Command in your PATH

If you previously installed VS Studio Code without using Homebrew, you may need to configure the path in order to open your editor via the terminal. To do so:

1. Launch VS Code using spotlight (**`⌘ Command + Space`** - then start typing **Visual Studio Code** until you see the app, then press `↩ Return`). When the app launches, you'll be prompted to confirm the action since you downloaded it from the internet.
2. Type **`⌘ Command  + Shift + P`** to open the command palette.
3. Start typing **shell command**, and when you see the **Shell Command: Install 'code' command in PATH** command, select it! Here's an example of what this will look like:

   ![The command palette, with the Shell Command: Install 'code' command in PATH option highlighted.](./assets/vsc-code-command.png)

4. You may see a dialog box that reads, "Code will now prompt with 'osascript' for Administrator privileges to install the shell command." Select **OK** if you are.
5. You may be prompted to enter your user account password to continue. Do so if you are.
6. You'll be shown: **Shell command 'code' successfully installed in PATH.** Select **OK**.
7. Quit both VS Code and the Terminal application.
8. Relaunch Terminal

Check [**this link**](https://code.visualstudio.com/docs/setup/mac) for troubleshooting if you run into issues.

## GitHub (GH)

At its core, GitHub (commonly abbreviated as GH) is a service for hosting Git repositories (which we'll talk about soon) in the cloud, but it also enables developers to collaborate on projects much more effectively. It might help to think of it as a social media platform for you and more than 100 million developers worldwide.

If you don't have an account there, create one now. Visit **[`https://github.com`](https://github.com)** and sign up. While there are paid account tiers, GitHub offers a very generous free tier that offers more than you need for the course.

## Git

Git is the version control software we will be using - it's an extremely popular tool among developers used to track changes to work (done in repositories) through time. We'll be covering Git much more in-depth later,

```bash
brew install git
```

### Git Config

With Git installed, we can now make some configuration changes to make it a more effective tool. Complete all of the following configuration steps.

Use the below command to add a user name to Git, which will be used to identify your commits. Replace `User Name` with a name of your choice. Make sure you leave the quotes surrounding your username. Keep the name somewhat professional, or just use your name - this will be used to identify your commits on GitHub. There will not be any output from this command.

```bash
git config --global user.name "User Name"
```

Next, use the below command to add an email to Git, which will be used to identify your commits. Replace `user@email.com` with the email address associated with your **[`https://github.com`](https://github.com)** account (**_NOT your GitHub Enterprise account at [`https://git.generalassemb.ly`](https://git.generalassemb.ly)_**). **The email you provide MUST match the email address associated with your GitHub account.** Ensure you leave the quotes surrounding your email. There will not be any output from this command. If you don't have a **[`https://github.com`](https://github.com)** account yet, create one before you run this.

```bash
git config --global user.email "user@email.com"
```

Set the default branch name to `main` with the below command. There will not be any output from this command.

```bash
git config --global init.defaultBranch main
```

Set the default Git editor to VS Code with the below command. There will not be any output from this command.

```bash
git config --global core.editor "code --wait"
```

By default, Git will ask for a new commit message when commits are brought into a Git repo. The following command will force the default commit message for all those commits instead of prompting you to add a commit message. While this isn't a Git command, we're still tackling it as part of this section since it changes Git's behavior. There will not be any output from this command.

```bash
echo "export GIT_MERGE_AUTOEDIT=no" >> ~/.zshrc
```

Turn off rebasing as the default behavior when pulling from a repo with the below command. There will not be any output from this command.

```bash
git config --global pull.rebase false
```

## Node.js

Use this command to install `nvm`, which we will use to install Node.js. `nvm` stands for [Node Version Manager](https://github.com/nvm-sh/nvm) and can be used to swap between different versions of Node.js quickly. We won't swap between different versions in the course, but it's still a handy tool for managing our Node.js install and can help you manage your Node.js installation post-course. Get `nvm` with this command:

```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
```

You may see this prompt part way through the install process:

![Error message reads: (Head detached at FETCH_HEAD). That can't be good!](./assets/nvm-head-detached.bmp)

If you do, just hit **`q`** - that will exit this screen and return you to the below install process. If you don't get this error, that's great; continue until you see the completed installation of `nvm`:

![The completed installation of `nvm`.](./assets/nvm-install-complete.png)

**Restart the Terminal application now.**

After starting up the Terminal again, run this command to check the version of `nvm`:

```bash
nvm --version
```

If you do not get a version number, check out the **Handling errors 💔** subsection below; otherwise, continue.

Use nvm to install node version 20 with this command:

```bash
nvm install 20
```

![A successful install of node v20.11.0](./assets/node-install-complete.png)

A successful install of node v20.11.0. Your version may be slightly different from this, but as long as it starts with 20 everything is ok!

### Handling errors 💔

#### command not found: nvm error

Copy this command block and run it in the terminal, which will point to the nvm directory in your **`~/.zshrc`** file:

```bash
cat << EOF >> ~/.zshrc

export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \\. "$NVM_DIR/nvm.sh"  # This loads nvm
[ -s "$NVM_DIR/bash_completion" ] && \\. "$NVM_DIR/bash_completion"  # This loads nvm bash_completion
EOF

```

Restart your terminal. You should now be able to run the `nvm --version` command and get a version number in response. If you do not, alert your installfest point of contact.

### NPM config

Run this command to disable `npm` update notifications since this process is managed by `nvm`:

```bash
npm config set update-notifier false
```

There will be no output after running this command.

### nodemon

With Node.js installed, install `nodemon` globally with this command:

```bash
npm i -g nodemon
```

If nodemon has successfully installed, this should be the output:

![nodemon successfully installed!](./assets/nodemon-install-complete.png)

## OH WOW YOU DID IT!

You are now set up to start developing in macOS! Be very proud of yourself; that was quite the process!
