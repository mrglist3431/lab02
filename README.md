# lab02
                                                                             ┌──(kali㉿kali)-[~]
└─$ git status
fatal: not a git repository (or any of the parent directories): .git
                                                                             
┌──(kali㉿kali)-[~]
└─$  $ open https://git-scm.com
$: command not found
                                                                             
┌──(kali㉿kali)-[~]
└─$ open https://git-scm.com 
                                                                             
┌──(kali㉿kali)-[~]
└─$ apt-get install git
E: Could not open lock file /var/lib/dpkg/lock-frontend - open (13: Permission denied)
E: Unable to acquire the dpkg frontend lock (/var/lib/dpkg/lock-frontend), are you root?
                                                                             
┌──(kali㉿kali)-[~]
└─$ sudo apt-get install git                          
[sudo] password for kali: 
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following additional packages will be installed:
  git-man
The following packages will be upgraded:
  git git-man
2 upgraded, 0 newly installed, 0 to remove and 1397 not upgraded.
Need to get 11.0 MB of archives.
After this operation, 1,059 kB of additional disk space will be used.
Do you want to continue? [Y/n] y
Get:1 http://kali.download/kali kali-rolling/main amd64 git amd64 1:2.47.2-0.1 [8,788 kB]
Get:2 http://kali.download/kali kali-rolling/main amd64 git-man all 1:2.47.2-0.1 [2,205 kB]
Fetched 11.0 MB in 3s (3,965 kB/s) 
(Reading database ... 405590 files and directories currently installed.)
Preparing to unpack .../git_1%3a2.47.2-0.1_amd64.deb ...
Unpacking git (1:2.47.2-0.1) over (1:2.45.2-1) ...
Preparing to unpack .../git-man_1%3a2.47.2-0.1_all.deb ...
Unpacking git-man (1:2.47.2-0.1) over (1:2.45.2-1) ...
Setting up git-man (1:2.47.2-0.1) ...
Setting up git (1:2.47.2-0.1) ...
Processing triggers for man-db (2.13.0-1) ...
Processing triggers for kali-menu (2024.4.0) ...
                                                                             
┌──(kali㉿kali)-[~]
└─$ export GITHUB_USERNAME=mrglist3431
                                                                             
┌──(kali㉿kali)-[~]
└─$ export GITHUB_EMAIL=pochta
                                                                             
┌──(kali㉿kali)-[~]
└─$ export GITHUB_TOKEN=token
                                                                             
┌──(kali㉿kali)-[~]
└─$ alias edit=<nano|vi|vim|subl>
zsh: parse error near `\n'
                                                                             
┌──(kali㉿kali)-[~]
└─$ alias edit=nano              
                                                                             
┌──(kali㉿kali)-[~]
└─$ cd ${GITHUB_USERNAME}/workspace
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace]
└─$ source scripts/activate
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace]
└─$ mkdir ~/.config        
mkdir: cannot create directory ‘/home/kali/.config’: File exists
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace]
└─$ mkdir .config  
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace]
└─$ source scripts/activate
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace]
└─$ cat > ~/.config/hub <<EOF
heredoc> github.com:
- user: ${GITHUB_USERNAME}
  oauth_token: ${GITHUB_TOKEN}
  protocol: https
EOF
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace]
└─$ git config --global hub.protocol https
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace]
└─$ mkdir projects/lab02 && cd projects/lab02
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/projects/lab02]
└─$ get init                              
Command 'get' not found, did you mean:
  command 'eet' from deb libeet-bin
  command 'gen' from deb multimon
  command 'geg' from deb geg
  command 'gt' from deb genometools
  command 'bget' from deb ax25-tools
  command 'git' from deb git
  command 'fet' from deb fet
  command 'gpt' from deb gpt
  command 'dget' from deb devscripts
  command 'gmt' from deb gmt
  command 'net' from deb samba-common-bin
  command 'kget' from deb kget
  command 'got' from deb got
  command 'wget' from deb wget
  command 'gem' from deb ruby-rubygems
Try: sudo apt install <deb name>
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/projects/lab02]
└─$ git init                              
hint: Using 'master' as the name for the initial branch. This default branch name                                                                         
hint: is subject to change. To configure the initial branch name to use in all                                                                            
hint: of your new repositories, which will suppress this warning, call:
hint:
hint:   git config --global init.defaultBranch <name>
hint:
hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and
hint: 'development'. The just-created branch can be renamed via this command:
hint:
hint:   git branch -m <name>
Initialized empty Git repository in /home/kali/mrglist3431/workspace/projects/lab02/.git/
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/projects/lab02]
└─$ git config --global user.name ${GITHUB_USERNAME}
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/projects/lab02]
└─$ git config --global user.email ${GITHUB_EMAIL}
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/projects/lab02]
└─$ git config -e --global
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/projects/lab02]
└─$ git remote add origin https://github.com/${GITHUB_USERNAME}/lab02.git
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/projects/lab02]
└─$ git pull origin master
Username for 'https://github.com': mrglist3431
Password for 'https://mrglist3431@github.com': 
remote: Support for password authentication was removed on August 13, 2021.
remote: Please see https://docs.github.com/get-started/getting-started-with-git/about-remote-repositories#cloning-with-https-urls for information on currently recommended modes of authentication.
fatal: Authentication failed for 'https://github.com/mrglist3431/lab02.git/'
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/projects/lab02]
└─$ git pull origin master
Username for 'https://github.com': mrglist3431
Password for 'https://mrglist3431@github.com': 
remote: Support for password authentication was removed on August 13, 2021.
remote: Please see https://docs.github.com/get-started/getting-started-with-git/about-remote-repositories#cloning-with-https-urls for information on currently recommended modes of authentication.
fatal: Authentication failed for 'https://github.com/mrglist3431/lab02.git/'
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/projects/lab02]
└─$ git pull origin master
Username for 'https://github.com': mrglist3431
Password for 'https://mrglist3431@github.com': 
remote: Invalid username or password.
fatal: Authentication failed for 'https://github.com/mrglist3431/lab02.git/'
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/projects/lab02]
└─$ touch README.md                      
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/projects/lab02]
└─$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md

nothing added to commit but untracked files present (use "git add" to track)
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/projects/lab02]
└─$ git add README.md
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/projects/lab02]
└─$ git commit -m"Добавлен README.md"
[master (root-commit) 1df55cd] Добавлен README.md
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 README.md
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/projects/lab02]
└─$ git push origin master           
Username for 'https://github.com': mrglist3431
Password for 'https://mrglist3431@github.com': 
remote: Invalid username or password.
fatal: Authentication failed for 'https://github.com/mrglist3431/lab02.git/'
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/projects/lab02]
└─$ git push -u           
fatal: The current branch master has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin master

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/projects/lab02]
└─$ git pull origin master
Username for 'https://github.com': mrglist3431
Password for 'https://mrglist3431@github.com': 
remote: Support for password authentication was removed on August 13, 2021.
remote: Please see https://docs.github.com/get-started/getting-started-with-git/about-remote-repositories#cloning-with-https-urls for information on currently recommended modes of authentication.
fatal: Authentication failed for 'https://github.com/mrglist3431/lab02.git/'
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/projects/lab02]
└─$ git pull origin master
Username for 'https://github.com': mrglist3431
Password for 'https://mrglist3431@github.com': 
remote: Invalid username or password.
fatal: Authentication failed for 'https://github.com/mrglist3431/lab02.git/'
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/projects/lab02]
└─$ git pull origin master
Username for 'https://github.com': name
Password for 'https://@github.com': 
remote: Invalid username or password.
fatal: Authentication failed for 'https://github.com/mrglist3431/lab02.git/'
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/projects/lab02]
└─$ git pull origin master
Username for 'https://github.com': ^C
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/projects/lab02]
└─$ git pull origin master
Username for 'https://github.com': mrglist3431
Password for 'https://mrglist3431@github.com': 
remote: Invalid username or password.
fatal: Authentication failed for 'https://github.com/mrglist3431/lab02.git/'
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/projects/lab02]
└─$ git pull origin master
Username for 'https://github.com': mrglist3431
Password for 'https://mrglist3431@github.com': 
remote: Support for password authentication was removed on August 13, 2021.
remote: Please see https://docs.github.com/get-started/getting-started-with-git/about-remote-repositories#cloning-with-https-urls for information on currently recommended modes of authentication.
fatal: Authentication failed for 'https://github.com/mrglist3431/lab02.git/'
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/projects/lab02]
└─$ git pull origin master
Username for 'https://github.com': mrglist3431
Password for 'https://mrglist3431@github.com': 
remote: Invalid username or password.
fatal: Authentication failed for 'https://github.com/mrglist3431/lab02.git/'
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/projects/lab02]
└─$ git pull origin master
Username for 'https://github.com': mrglist3431
Password for 'https://mrglist3431@github.com': 
remote: Repository not found.
fatal: repository 'https://github.com/mrglist3431/lab02.git/' not found
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/projects/lab02]
└─$ git remote add origin https://github.com/${GITHUB_USERNAME}/lab02.git
error: remote origin already exists.
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/projects/lab02]
└─$ mkdir projects/lab02 && cd projects/lab02
mkdir: cannot create directory ‘projects/lab02’: No such file or directory
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/projects/lab02]
└─$ mkdir lab02 && cd lab02          
                                                                             
┌──(kali㉿kali)-[~/…/workspace/projects/lab02/lab02]
└─$ ..
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/projects/lab02]
└─$ ..
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/projects]
└─$ ..
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace]
└─$ mkdir projects/lab02                     
mkdir: cannot create directory ‘projects/lab02’: File exists
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace]
└─$ mkdir lab02                              
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace]
└─$ cd lab02                       
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git remote add origin https://github.com/${GITHUB_USERNAME}/lab02.git
fatal: not a git repository (or any of the parent directories): .git
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git init                                                             
hint: Using 'master' as the name for the initial branch. This default branch name                                                                         
hint: is subject to change. To configure the initial branch name to use in all                                                                            
hint: of your new repositories, which will suppress this warning, call:
hint:
hint:   git config --global init.defaultBranch <name>
hint:
hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and
hint: 'development'. The just-created branch can be renamed via this command:
hint:
hint:   git branch -m <name>
Initialized empty Git repository in /home/kali/mrglist3431/workspace/lab02/.git/
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git config --global hub.protocol https
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git config --global user.name ${GITHUB_USERNAME}
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git config --global user.email ${GITHUB_EMAIL}
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git config -e --global
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git remote add origin https://github.com/${GITHUB_USERNAME}/lab02.git
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git pull origin master                                               
Username for 'https://github.com': mrglist3431
Password for 'https://mrglist3431@github.com': 
remote: Repository not found.
fatal: repository 'https://github.com/mrglist3431/lab02.git/' not found
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git pull origin master
fatal: couldn't find remote ref master
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git pull origin master
fatal: couldn't find remote ref master
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git remote add origin https://github.com/${GITHUB_USERNAME}/lab02.git

error: remote origin already exists.
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git pull origin master                                               
fatal: couldn't find remote ref master
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ touch README.md
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git status            
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md

nothing added to commit but untracked files present (use "git add" to track)
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git commit -m"Добавлен README.md"
On branch master

Initial commit

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md

nothing added to commit but untracked files present (use "git add" to track)
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git add README.md                
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git commit -m"Добавлен README.md"
[master (root-commit) 7cc64a9] Добавлен README.md
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 README.md
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git pull origin master           
fatal: couldn't find remote ref master
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git push origin master
Username for 'https://github.com': mrglist3431
Password for 'https://mrglist3431@github.com': 
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 240 bytes | 240.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote: 
remote: Create a pull request for 'master' on GitHub by visiting:
remote:      https://github.com/mrglist3431/lab02/pull/new/master
remote: 
To https://github.com/mrglist3431/lab02.git
 * [new branch]      master -> master
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git pull origin master
From https://github.com/mrglist3431/lab02
 * branch            master     -> FETCH_HEAD
Already up to date.
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git log               
commit 7cc64a9dd651298df9a31c43dab70e0aee20bb24 (HEAD -> master, origin/master)
Author: mrglist3431 <ifedotov236@gmail.com>
Date:   Mon Mar 31 20:19:27 2025 +0300

    Добавлен README.md
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ mkdir sources
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ mkdir include
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ mfdir examples
Command 'mfdir' not found, did you mean:
  command 'mkdir' from deb coreutils
  command 'mdir' from deb mtools
Try: sudo apt install <deb name>
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ cat > sources/print.cpp <<EOF
#include <print.hpp>

void print(const std::string& text, std::ostream& out)
{
  out << text;
}

void print(const std::string& text, std::ofstream& out)
{
  out << text;
}
EOF
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ cat > include/print.hpp <<EOF
#include <fstream>
#include <iostream>
#include <string>

void print(const std::string& text, std::ofstream& out);
void print(const std::string& text, std::ostream& out = std::cout);
EOF
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ cat > examples/example1.cpp <<EOF
#include <print.hpp>

int main(int argc, char** argv)
{
  print("hello");
}
EOF
zsh: no such file or directory: examples/example1.cpp
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ cat > examples/example1.cpp <<EOF
#include <print.hpp>

int main(int argc, char** argv)
{
  print("hello");
}
EOF
zsh: no such file or directory: examples/example1.cpp
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ mkdir examples
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ cat > examples/example1.cpp <<EOF
#include <print.hpp>

int main(int argc, char** argv)
{
  print("hello");
}
EOF
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ cat > examples/example2.cpp <<EOF
#include <print.hpp>

#include <fstream>

int main(int argc, char** argv)
{
  std::ofstream file("log.txt");
  print(std::string("hello"), file);
}
EOF
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ edit README.md                                              
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        examples/
        include/
        sources/

nothing added to commit but untracked files present (use "git add" to track)
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git add .        
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git commit -m"added sources"     
[master 917ece0] added sources
 4 files changed, 32 insertions(+)
 create mode 100644 examples/example1.cpp
 create mode 100644 examples/example2.cpp
 create mode 100644 include/print.hpp
 create mode 100644 sources/print.cpp
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git push origin master      
Username for 'https://github.com': mrglist3431
Password for 'https://mrglist3431@github.com': 
Enumerating objects: 10, done.
Counting objects: 100% (10/10), done.
Delta compression using up to 16 threads
Compressing objects: 100% (7/7), done.
Writing objects: 100% (9/9), 898 bytes | 898.00 KiB/s, done.
Total 9 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/mrglist3431/lab02.git
   7cc64a9..917ece0  master -> master
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ cd ~/workspace/                  
cd: no such file or directory: /home/kali/workspace/
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ ..
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace]
└─$ export LAB_NUMBER=02                                        
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace]
└─$ git clone https://github.com/tp-labs/lab${LAB_NUMBER} tasks/lab${LAB_NUMBER}
Cloning into 'tasks/lab02'...
remote: Enumerating objects: 96, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 96 (delta 0), reused 1 (delta 0), pack-reused 93 (from 1)
Receiving objects: 100% (96/96), 1.29 MiB | 434.00 KiB/s, done.
Resolving deltas: 100% (28/28), done.
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace]
└─$ mkdir reports/lab${LAB_NUMBER}
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace]
└─$ cp tasks/lab${LAB_NUMBER}/README.md reports/lab${LAB_NUMBER}/REPORT.md
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace]
└─$ cd reports/lab${LAB_NUMBER}                                           
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/reports/lab02]
└─$ edit REPORT.md      
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/reports/lab02]
└─$ gist REPORT.md
