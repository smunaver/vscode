BUILDING FRAPPE

PS D:\sultan-development\school_frappe-app> git clone https://github.com/frappe/frappe_docker.git
Cloning into 'frappe_docker'...
remote: Enumerating objects: 11721, done.
remote: Counting objects: 100% (365/365), done.
remote: Compressing objects: 100% (123/123), done.
remote: Total 11721 (delta 282), reused 246 (delta 242), pack-reused 11356 (from 3)
Receiving objects: 100% (11721/11721), 10.38 MiB | 5.58 MiB/s, done.
Resolving deltas: 100% (5963/5963), done.
PS D:\sultan-development\school_frappe-app> 


# 1. Move back to your main project folder
cd D:\sultan-development\school_frappe-app

# 2. Copy the example devcontainer folder to a new folder named .devcontainer
# (Since we are in PowerShell, we use Copy-Item)
Copy-Item -Recurse ".\frappe_docker\devcontainer-example\*" ".\.devcontainer\"

# 1. Move out of the frappe_docker folder and back to the project root
cd ..

# 2. Move the .devcontainer folder from the subfolder to the root
mv frappe_docker/.devcontainer .


VS Code scans for the .devcontainer folder only when it first opens a project. Since you just moved the folder into place, VS Code doesn't know it's there yet.

Follow these steps:
Close VS Code completely.
Open VS Code again.
Go to File $\rightarrow$ Open Folder... $\rightarrow$ Select D:\sultan-development\school_frappe-app.
Wait a few seconds. The popup should appear in the bottom right corner.
