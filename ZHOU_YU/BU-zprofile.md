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

# List all files colorized in long format
alias l="ls -lF ${colorflag}"
alias ll="ls -alF ${colorflag}"

# List all files colorized in long format, excluding . and ..
alias la="ls -lAF ${colorflag}"

# List only directories
alias lsd="ls -lF ${colorflag} | grep --color=never '^d'"

# Always use color output for `ls`
alias ls="command ls ${colorflag}"

# Always enable colored `grep` output
# Note: `GREP_OPTIONS="--color=auto"` is deprecated, hence the alias usage.
alias grep='grep --color=auto'
alias fgrep='fgrep --color=auto'
alias egrep='egrep --color=auto'

# Print each PATH entry on a separate line
alias path='echo -e ${PATH//:/\\n}'

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

# 🥇Workflow - Start with Pull & Create & Work on your feature branch with new creation

alias p="git pull" # Routine Git Pull

alias B="git pull && git branch CVSAI_JosephYu && git checkout CVSAI_JosephYu"
alias s="git status" # Quick check on the current status
alias d="git diff" # Review the difference. NOTE: diff will ALWAYS work once you SAVE your file (It is on your "Working Directory"! No need to commit)
alias a="git add -A" # Add ALL files to the "Staging Area" NOTE: Once you +ADD your files, you "Working Directory" is clean
alias C="git commit -m" # ✅NOTE: commit will materialize your IDE with visual update! 🎯

alias up="git push --set-upstream origin CVSAI_JosephYu" # #️⃣One-Time ONLY - Set upstream association with remote origin 🎯
alias P="git pull && git push" # ✅PUSH local branch into remote origin 🎯

# STEP - Wrap up & Clean
alias D="git checkout master && git branch -D CVSAI_JosephYu && git fetch -p && git branch -a" # ✅Deletion of local feature branch & Sync with remote origin
alias DM="git checkout main && git branch -D CVSAI_JosephYu && git fetch -p && git branch -a" # ️#️⃣OptionalAlias ✅Deletion of local feature branch & Sync with remote origin

alias DD="git push origin -d CVSAI_JosephYu" # #️⃣Optional - Deletion of remote feature branch

# STEP - Switch back and forth between Master/Main and your feature branch
alias b="git branch -a" # Viewing Information about ALL available branches

alias m="git checkout master" # GitLab - Checkout Local Master Branch
alias mm="git checkout main" # #️⃣OptionalAlias - GitHub - Checkout Local Main Branch #️⃣*ONLY for Default Main {remotes/origin/main}

alias f="git checkout CVSAI_JosephYu" # Checkout Local Feature branch
alias F="git fetch -p && git branch -a" # 'git fetch --prune': House keeping utility to clean outdated branches

# git reset # Remove ALL from the "Staging Area"
# git log # Check out the Hash Number of each commit

# Quick: ALL-in-One Push - use with caution!
alias PP="git add -A && git commit -m 'CVSAI_JosephYu' && git pull origin && git push origin" # ✅Complete Cylcle ALl-in-One

# Easier navigation: .., ..., ...., ....., ~ and -
alias ..="cd .."
alias ...="cd ../.."
alias ....="cd ../../.."
alias .....="cd ../../../.."

# Quick DevOps

alias A="code ~/.zprofile" # Update user-defined aliases which can be modified w/o Admin Access
# alias A="code /c/Users/CVSAI/.bash_aliases" # Update user-defined aliases which can be modified w/o Admin Access

# Covestro Windows 11 Reference ONLY - intended for Corporate Usage NOT for indivisual account settings
# alias AC="cd /c/Users/CVSAI/.aws && code ." # AWS - Update AWS Config Profiles with the latest SSO credentials in a NEW window

# Quick Access

alias pri="cd /c/JosephYu/PRIVATE/"
alias cov="cd /c/JosephYu/COVESTRO/"

alias dl="cd ~/Downloads/"
alias dk="cd /c/Users/CVSAI/'OneDrive - Covestro'/Desktop/"

alias h='history'

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
