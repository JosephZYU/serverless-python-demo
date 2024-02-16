# Setting PATH manually for Python 3.9 ✅
# The original version is saved in .zprofile.pysave
# Ref - https://youtu.be/PUIE7CPANfo?t=595
# 👀 MAKE sure to update Versions/3.9/ for future versions

# PATH="/Library/Frameworks/Python.framework/Versions/3.9/bin:${PATH}"
# export PATH

# Setting Alias for python3 as default python by Joseph ✅
alias python=python3

# Setting Alias for pip3 as default pip by Joseph ✅
alias pip=pip3

# Setting custom-built module by Joseph ✅
# Ref - https://youtu.be/CqvZ3vGoGs0?t=660
export PYTHONPATH="/Users/josephyu/Documents/GitHub/My-Modules"

# Setting environment variable for Database by Joseph
# export DB_USER="my_db_user"
# export DB_PASS="my_db_password_123"

# Setting Alias for shortcut to Desktop ✅
# Ref - https://youtu.be/0liXeoADU6A?t=95
alias dt='cd ~/Desktop/'

# Practice-ONLY (Functional BUT not intended for real-production) ✅
# Ref - https://youtu.be/0liXeoADU6A?t=480
# alias tutMode='rm -rf ~/.Trash/*; rm -rf ~/Downloads/*'

# Shortcuts
alias gh="~/Documents/GitHub"
alias d="cd ~/Downloads"
alias n="code ~/Documents/GitHub/Python-0-Automation/GEN_NOTES/"

alias pip='pip3'
alias python='python3'

alias hc='history | grep "git commit"'
alias hg='history | grep'

# alias dt="cd ~/Desktop"
# alias p="cd ~/projects"

# Detect which `ls` flavor is in use
if ls --color > /dev/null 2>&1; then # GNU `ls`
	colorflag="--color"
	export LS_COLORS='no=00:fi=00:di=01;31:ln=01;36:pi=40;33:so=01;35:do=01;35:bd=40;33;01:cd=40;33;01:or=40;31;01:ex=01;32:*.tar=01;31:*.tgz=01;31:*.arj=01;31:*.taz=01;31:*.lzh=01;31:*.zip=01;31:*.z=01;31:*.Z=01;31:*.gz=01;31:*.bz2=01;31:*.deb=01;31:*.rpm=01;31:*.jar=01;31:*.jpg=01;35:*.jpeg=01;35:*.gif=01;35:*.bmp=01;35:*.pbm=01;35:*.pgm=01;35:*.ppm=01;35:*.tga=01;35:*.xbm=01;35:*.xpm=01;35:*.tif=01;35:*.tiff=01;35:*.png=01;35:*.mov=01;35:*.mpg=01;35:*.mpeg=01;35:*.avi=01;35:*.fli=01;35:*.gl=01;35:*.dl=01;35:*.xcf=01;35:*.xwd=01;35:*.ogg=01;35:*.mp3=01;35:*.wav=01;35:'
else # macOS `ls`
	colorflag="-G"
	export LSCOLORS='BxBxhxDxfxhxhxhxhxcxcx'
fi



###################################################
# Custom aliases for Git Bash by JosephYu - START #
###################################################

# Working Directory >>> Staging Area >>> Repo

# STEP - Initial Setup
# git config --global user.name “JosephYu”
# git config --global user.email “josephyu.careers@outlook.com”
# git config --list
# git init # intialize an empty git repo with .git file 
# git clone <url> # Cloning a remote repo including the HOME Folder
# git clone <url> . # Cloning a remote repo without the HOME Folder - NOT recommended!
# git remote -v # Viewing Information about the remote repo - origin URL



# git reset # Remove ALL from the "Staging Area"
# git log # Check out the Hash Number of each commit


# alias A="code /c/Users/CVSAI/.bash_aliases" # Update user-defined aliases which can be modified w/o Admin Access

# Covestro Windows 11 Reference ONLY - intended for Corporate Usage NOT for indivisual account settings
# alias AC="cd /c/Users/CVSAI/.aws && code ." # AWS - Update AWS Config Profiles with the latest SSO credentials in a NEW window



# alias git-commit-history="git log --since='7 days ago' --grep='commit'"
# alias git-commit-history="git log --since='7 days ago'"

# alias dk="cd /c/Users/JosephYu/Desktop/"
# alias dl="cd /c/Users/JosephYu/Downloads/"

# alias win='cd /mnt/c/Users/JosephYu/Desktop'
# alias pip='pip3'
# alias python='python3'

# AWS Sample
# alias ec2='chmod 400 WSL.pem; ssh -i WSL.pem ec2-user@3.237.181.112 -y'

#################################################
# Custom aliases for Git Bash by JosephYu - END #
#################################################
# Setting PATH for Python 3.12
# The original version is saved in .zprofile.pysave
# PATH="/Library/Frameworks/Python.framework/Versions/3.12/bin:${PATH}"
# export PATH
