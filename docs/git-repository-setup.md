https://docs.github.com/en/migrations/importing-source-code/using-the-command-line-to-import-source-code/adding-locally-hosted-code-to-github

Open Git Bash.

Navigate to the root directory of your existing project.

There are different levels where you can initialize a git repository(which creates a .git file), but I tend to use the following structure:

```
my_project/
├── .git/                 # Git repository metadata (hidden folder)
├── .gitignore            # Where I tell git what files/folders I NEVER want pushed to a repository (think secret information or large files)
├── LICENSE               # Where you document the license terms of your code
├── requirements.txt      # Save python package dependencies and their versions needed to run your code
├── secrets.json          # (Optional) You may be using resources or APIs that require authentication... this file allows me access
├── README.md             # Project README file where you can document and explain your program
├── src/                  # Source code directory
│   ├── main.py           # Main Python source file
│   └── utils.py          # Utility functions source file
├── data/                 # Data directory
│   ├── dataset.csv       # Example dataset file
│   └── images/           # Directory for images
│       ├── image1.jpg
│       ├── image2.jpg
│       └── ...
└── docs/                 # Documentation directory
    ├── design.md         # Design documentation
    └── usage.md          # Usage instructions
```

This project structure should work well for most analysts. When integrating with other devops or product teams in your organization, ask what kind of structure they use. You may learn something new!

Initialize the local directory as a Git repository. By default, the initial branch is called main.

> $ git init -b main

Add the files in your new local repository. This stages them for the first commit.

> $ git add .

Commit the files that you've staged in your local repository.

> $ git commit -m "First commit"

Create a new repository on GitHub.com. To avoid errors, do not initialize the new repository with README, license, or gitignore files. You can add these files after your project has been pushed to GitHub. For more information, see "Creating a new repository."

At the top of your repository on GitHub.com's Quick Setup page, click  to copy the remote repository URL.

Open Git Bash.

Change the current working directory to your local project.

In the Command prompt, add the URL for the remote repository where your local repository will be pushed.

> $ git remote add origin <REMOTE_URL> 

Sets the new remote

> $ git remote -v

Verifies the new remote URL

Push the changes in your local repository to GitHub.com.

> $ git push origin main