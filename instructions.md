

# Pre-work for Git Tutorial 
This pre-work needs to be complete before 11am PT on Wednesday, January 27th. The istructions below will help you install and download certain tools you need to complete both hands-on activites. 

When you type in a command in your terminal, do not add the ```$``` sign. The dollar sign is the symbol used to signify where you can begin typing in commands.

If you run into any issues, please let me know soon so we can work together to make sure everyone is set up for success next week.

I'm looking forward to working with everyone!

## Installing your text editor
Install VScode on your computer. If you have a Mac, open up the Command Palette with **cmd+shift+p** or go to ```view > command palette``` in VScode and type in ```Shell Command: Install 'code' command in PATH```. This will allow you to open up VScode from the terminal in Mac.

## Installing Git through Homebrew
First, we need to make sure you have git installed on your computer.

Open up your terminal (you can do a spotlight search on your mac for “terminal”)

> **Learning Note:** The Terminal, also known as the command line or a Terminal emulator, is an essential component of any useful operating system. The Terminal provides an efficient interface to access the true power of a computer better than any graphical interface.

> **Learning Note:** You can’t use a mouse or trackpad in Terminal, but you can navigate using the arrow keys. If you want to re-run a command, tap the up arrow key until you reach it, then press Return. To interrupt a command that’s already running, type Control-C.

First, check to see if you have git installed by typing in the command 

    $ git --version

If you do you'll see something like

    $ git version 2.20.1 (Apple Git-117)

If not, you might see something like

To install git, first install [Homebrew](https://brew.sh/) with 

    $ /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

> Homebrew is a free and open-source software package management system that simplifies the installation of software on Apple's macOS operating system and Linux.

Once you've installed homebrew, you can install git with
    
    $ brew install git

Now let's set your Git username in your Terminal


## Adding your SSH Keys
Let's add your SSH keys to your GitHub account

1. Open Terminal.

2. Paste the text below, substituting in your GitHub email address.
```
$ ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
    
To delete ssh keys (don't do this without speaking to me first)
$ cd ~/.ssh
$ rm ~/.ssh/github_rsa.pub
```
3. When you're prompted to **"Enter a file in which to save the key,"** press Enter. This accepts the default file location.

4. At the prompt, type a secure passphrase.

5. Copy the SSH key to your clipboard. To do that type this command
```
$ pbcopy < ~/.ssh/id_rsa.pub
```
**Note** Once you type in the above command, the key will be copied to your clipboard. You can test it my pasting the key into a notepad.

6. In the upper-right corner of any page in GitHub, click your profile photo, then click Settings.

7. In the user settings sidebar, click SSH and GPG keys.

8. Click New SSH key or Add SSH key.

9. In the "Title" field, add a descriptive label for the new key. For example, if you're using a personal Mac, you might call this key "Personal MacBook Air".

10. Paste your key into the "Key" field.

11. Click Add SSH key

> **Learning Note:** An SSH key is an alternate way to identify yourself that doesn't require you to enter you username and password every time.

Next, lets set up your Git username for every repository on your computer

1. Open terminal if it's not already open
2. Set a Git username:
````
$ git config --global user.name "Radhika Gulati"
````
## Add email address to GitHub for commits
Next lets set your commit email address on GitHub. To do so, follow the instructions [here](https://docs.github.com/en/free-pro-team@latest/github/setting-up-and-managing-your-github-user-account/setting-your-commit-email-address#setting-your-commit-email-address-on-github).

Next, lets set up your commit email address in Git (on your local machine). 

1. Open terminal if it's not already open
2. Set an email address in Git. You can use your GitHub-provided no-reply email address or any email address (this will most likely be your CircleCI email address).
````
$ git config --global user.email "email@example.com"
````
3. Confirm that you have set the email address correctly in Git:
```
$ git config user.email
email@example.com
```

# Pre-work for Hands-on Project

<h2> Install node and npm </h2> 

We need to install node on our computers so we have access to npm, which will let us install Cypress. 

In your terminal type

    $ brew install node

Check to make sure node was installed by typing

    $ node -v

You should see something like

     $ v14.15.3

Check to make sure npm was installed by typing

    $ npm -v

You should see something like

    $ 6.14.9

<h2> Create a Netlify account </h2>

You are going to create a [Netlify](https://www.netlify.com/) account. Sign up with GitHub.

