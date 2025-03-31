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









                                                                             ┌──(kali㉿kali)-[~]
└─$ cd mrglist3431             
                                                                             
┌──(kali㉿kali)-[~/mrglist3431]
└─$ ls
workspace
                                                                             
┌──(kali㉿kali)-[~/mrglist3431]
└─$ workspace                                                         
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace]
└─$ ls
lab02  node  projects  reports  scripts  tasks
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace]
└─$ lab02
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ ls   
examples  include  README.md  sources
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git checkout patch01
error: pathspec 'patch01' did not match any file(s) known to git
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git checkout master 
Already on 'master'
Your branch is up to date with 'origin/master'.
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git checkout patch1 
Switched to branch 'patch1'
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git commit -m "JJJ"
On branch patch1
nothing to commit, working tree clean
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git add .          
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git commit -m "Восстановление"
On branch patch1
nothing to commit, working tree clean
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git add homework.cpp          
fatal: pathspec 'homework.cpp' did not match any files
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ nano homework.cpp
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ nano helloworld.cpp
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git add helloworld.cpp
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git commit -m "Update"        
[patch1 8d42998] Update
 1 file changed, 1 insertion(+), 1 deletion(-)
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git pull origin patch1
From https://github.com/mrglist3431/lab02
 * branch            patch1     -> FETCH_HEAD
Current branch patch1 is up to date.
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git push origin patch1
Username for 'https://github.com': mrglist3431
Password for 'https://mrglist3431@github.com': 
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 16 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 277 bytes | 277.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/mrglist3431/lab02.git
   7a2e136..8d42998  patch1 -> patch1
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git mkdir ttt         
git: 'mkdir' is not a git command. See 'git --help'.
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ mkdir ttt  
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ ls
helloworld.cpp  ttt
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git add ttt           
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git commit -m "TTT"   
On branch patch1
nothing to commit, working tree clean
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git push origin patch1
Username for 'https://github.com': mrglist3431
Password for 'https://mrglist3431@github.com': 
Everything up-to-date
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ mkdir ttt.txt
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ nano ttt.txt       
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git add ttt.txt       
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git commit -m "TTT"
On branch patch1
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        dddd

nothing added to commit but untracked files present (use "git add" to track)
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git add dddd       
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git commit -m "TTT"
[patch1 dfaf018] TTT
 1 file changed, 2 insertions(+)
 create mode 100644 dddd
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git push origin patch1
Username for 'https://github.com': mrglist3431 
Password for 'https://mrglist3431@github.com': 
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 16 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 273 bytes | 273.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/mrglist3431/lab02.git
   8d42998..dfaf018  patch1 -> patch1
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git checkout main     
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git pull origin main  
From https://github.com/mrglist3431/lab02
 * branch            main       -> FETCH_HEAD
Already up to date.
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git log             
commit 5301270edb56774d652d6c04650c2165acfaa047 (HEAD -> main, origin/main)
Author: mrglist3431 <ifedotov236@gmail.com>
Date:   Mon Mar 31 22:47:03 2025 +0300

    deleted

commit ef14782b71fdfac8eb8367099da67b7074d83e80
Author: mrglist3431 <ifedotov236@gmail.com>
Date:   Mon Mar 31 22:39:58 2025 +0300

    deleted

commit 873779900180b73efd9e10a6a7fe13d878aa9b1c
Author: mrglist3431 <ifedotov236@gmail.com>
Date:   Mon Mar 31 22:32:57 2025 +0300

    name  hello

commit 206a2aecab843224ab1157eb8f27577dee7974eb
Author: mrglist3431 <ifedotov236@gmail.com>
Date:   Mon Mar 31 22:29:39 2025 +0300

    added hello

commit 778956861c94bb8065e78678904a5f9201ac5d54
Author: mrglist3431 <ifedotov236@gmail.com>
Date:   Mon Mar 31 20:32:25 2025 +0300

    added sources

commit a3c0af53746a0d0a3a27549201c0aed6426ec243
Author: mrglist3431 <ifedotov236@gmail.com>
Date:   Mon Mar 31 21:45:16 2025 +0300

    Create homework

commit 0bbb1c3eeb8f287cf742b800336b43cf4c11dfe0
Author: mrglist3431 <ifedotov236@gmail.com>
Date:   Mon Mar 31 21:43:24 2025 +0300

    Update README.md

commit 1dc68e1eb5f54124cb47f305f89f2c60dac3482e
Author: mrglist3431 <ifedotov236@gmail.com>
Date:   Mon Mar 31 20:28:34 2025 +0300

    Create f.gitignore

commit c9e215966e7f1a43de3147c0ac1855b560df26f5
Author: mrglist3431 <ifedotov236@gmail.com>
Date:   Mon Mar 31 20:17:23 2025 +0300

    Initial commit
commit 5301270edb56774d652d6c04650c2165acfaa047 (HEAD -> main, origin/main)
Author: mrglist3431 <ifedotov236@gmail.com>
Date:   Mon Mar 31 22:47:03 2025 +0300

    deleted

commit ef14782b71fdfac8eb8367099da67b7074d83e80
Author: mrglist3431 <ifedotov236@gmail.com>
Date:   Mon Mar 31 22:39:58 2025 +0300

    deleted

commit 873779900180b73efd9e10a6a7fe13d878aa9b1c
Author: mrglist3431 <ifedotov236@gmail.com>
Date:   Mon Mar 31 22:32:57 2025 +0300

    name  hello

commit 206a2aecab843224ab1157eb8f27577dee7974eb
Author: mrglist3431 <ifedotov236@gmail.com>
Date:   Mon Mar 31 22:29:39 2025 +0300

    added hello

commit 778956861c94bb8065e78678904a5f9201ac5d54
Author: mrglist3431 <ifedotov236@gmail.com>
Date:   Mon Mar 31 20:32:25 2025 +0300

    added sources

commit a3c0af53746a0d0a3a27549201c0aed6426ec243
Author: mrglist3431 <ifedotov236@gmail.com>
Date:   Mon Mar 31 21:45:16 2025 +0300

    Create homework

commit 0bbb1c3eeb8f287cf742b800336b43cf4c11dfe0
Author: mrglist3431 <ifedotov236@gmail.com>
Date:   Mon Mar 31 21:43:24 2025 +0300

    Update README.md

commit 1dc68e1eb5f54124cb47f305f89f2c60dac3482e
Author: mrglist3431 <ifedotov236@gmail.com>
Date:   Mon Mar 31 20:28:34 2025 +0300

    Create f.gitignore

commit c9e215966e7f1a43de3147c0ac1855b560df26f5
Author: mrglist3431 <ifedotov236@gmail.com>
Date:   Mon Mar 31 20:17:23 2025 +0300

    Initial commit
...skipping...

    added sources

commit a3c0af53746a0d0a3a27549201c0aed6426ec243
Author: mrglist3431 <ifedotov236@gmail.com>
Date:   Mon Mar 31 21:45:16 2025 +0300

    Create homework

commit 0bbb1c3eeb8f287cf742b800336b43cf4c11dfe0
Author: mrglist3431 <ifedotov236@gmail.com>
Date:   Mon Mar 31 21:43:24 2025 +0300

    Update README.md

commit 1dc68e1eb5f54124cb47f305f89f2c60dac3482e
Author: mrglist3431 <ifedotov236@gmail.com>
Date:   Mon Mar 31 20:28:34 2025 +0300

    Create f.gitignore

commit c9e215966e7f1a43de3147c0ac1855b560df26f5
Author: mrglist3431 <ifedotov236@gmail.com>
Date:   Mon Mar 31 20:17:23 2025 +0300

    Initial commit

    added sources

commit a3c0af53746a0d0a3a27549201c0aed6426ec243
Author: mrglist3431 <ifedotov236@gmail.com>
Date:   Mon Mar 31 21:45:16 2025 +0300

    Create homework

commit 0bbb1c3eeb8f287cf742b800336b43cf4c11dfe0
Author: mrglist3431 <ifedotov236@gmail.com>
Date:   Mon Mar 31 21:43:24 2025 +0300

    Update README.md

commit 1dc68e1eb5f54124cb47f305f89f2c60dac3482e
Author: mrglist3431 <ifedotov236@gmail.com>
Date:   Mon Mar 31 20:28:34 2025 +0300

    Create f.gitignore

commit c9e215966e7f1a43de3147c0ac1855b560df26f5
Author: mrglist3431 <ifedotov236@gmail.com>
Date:   Mon Mar 31 20:17:23 2025 +0300

    Initial commit

    added sources

commit a3c0af53746a0d0a3a27549201c0aed6426ec243
Author: mrglist3431 <ifedotov236@gmail.com>
Date:   Mon Mar 31 21:45:16 2025 +0300

    Create homework

commit 0bbb1c3eeb8f287cf742b800336b43cf4c11dfe0
Author: mrglist3431 <ifedotov236@gmail.com>
Date:   Mon Mar 31 21:43:24 2025 +0300

    Update README.md

commit 1dc68e1eb5f54124cb47f305f89f2c60dac3482e
Author: mrglist3431 <ifedotov236@gmail.com>
Date:   Mon Mar 31 20:28:34 2025 +0300

    Create f.gitignore

commit c9e215966e7f1a43de3147c0ac1855b560df26f5
Author: mrglist3431 <ifedotov236@gmail.com>
Date:   Mon Mar 31 20:17:23 2025 +0300

    Initial commit

zsh: suspended  git log
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git branch patch2
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git checkout patch2
Switched to branch 'patch2'
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ sodo apt install clang-format
Command 'sodo' not found, did you mean:
  command 'todo' from deb devtodo
  command 'solo' from deb solo1-cli
  command 'sudo' from deb sudo
  command 'sudo' from deb sudo-ldap
Try: sudo apt install <deb name>
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ sudo apt install clang-format
[sudo] password for kali: 
Upgrading:                      
  clang
                                                                             
Installing:
  clang-format
                                                                             
Installing dependencies:
  clang-19                libclang-rt-19-dev  llvm-19-linker-tools
  clang-format-19         libclang1-19        llvm-19-runtime                
  libclang-common-19-dev  llvm-19             llvm-19-tools                  
  libclang-cpp19          llvm-19-dev                                        
                                                                             
Suggested packages:
  clang-19-doc  wasi-libc  llvm-19-doc

Summary:
  Upgrading: 1, Installing: 12, Removing: 0, Not Upgrading: 1396
  Download size: 87.4 MB
  Space needed: 611 MB / 336 GB available

Continue? [Y/n] y
Get:1 http://http.kali.org/kali kali-rolling/main amd64 libclang-cpp19 amd64 1:19.1.7-1+b1 [13.2 MB]
Get:6 http://mirror.nl.cdn-perfprod.com/kali kali-rolling/main amd64 clang amd64 1:19.0-63 [6,244 B]
Get:8 http://mirror.nl.cdn-perfprod.com/kali kali-rolling/main amd64 clang-format amd64 1:19.0-63 [6,352 B]
Get:2 http://http.kali.org/kali kali-rolling/main amd64 libclang-common-19-dev amd64 1:19.1.7-1+b1 [740 kB]
Get:3 http://http.kali.org/kali kali-rolling/main amd64 llvm-19-linker-tools amd64 1:19.1.7-1+b1 [1,261 kB]
Get:4 http://http.kali.org/kali kali-rolling/main amd64 libclang1-19 amd64 1:19.1.7-1+b1 [7,614 kB]
Get:5 http://http.kali.org/kali kali-rolling/main amd64 clang-19 amd64 1:19.1.7-1+b1 [116 kB]
Get:7 http://http.kali.org/kali kali-rolling/main amd64 clang-format-19 amd64 1:19.1.7-1+b1 [92.8 kB]
Get:9 http://http.kali.org/kali kali-rolling/main amd64 libclang-rt-19-dev amd64 1:19.1.7-1+b1 [3,689 kB]
Get:10 http://http.kali.org/kali kali-rolling/main amd64 llvm-19-runtime amd64 1:19.1.7-1+b1 [551 kB]
Get:11 http://http.kali.org/kali kali-rolling/main amd64 llvm-19 amd64 1:19.1.7-1+b1 [16.4 MB]
Get:12 http://http.kali.org/kali kali-rolling/main amd64 llvm-19-tools amd64 1:19.1.7-1+b1 [511 kB]
Get:13 http://http.kali.org/kali kali-rolling/main amd64 llvm-19-dev amd64 1:19.1.7-1+b1 [43.2 MB]
Fetched 87.4 MB in 57s (1,524 kB/s)                                         
Selecting previously unselected package libclang-cpp19.
(Reading database ... 405609 files and directories currently installed.)
Preparing to unpack .../00-libclang-cpp19_1%3a19.1.7-1+b1_amd64.deb ...
Unpacking libclang-cpp19 (1:19.1.7-1+b1) ...
Selecting previously unselected package libclang-common-19-dev:amd64.
Preparing to unpack .../01-libclang-common-19-dev_1%3a19.1.7-1+b1_amd64.deb ...
Unpacking libclang-common-19-dev:amd64 (1:19.1.7-1+b1) ...
Selecting previously unselected package llvm-19-linker-tools.
Preparing to unpack .../02-llvm-19-linker-tools_1%3a19.1.7-1+b1_amd64.deb ...
Unpacking llvm-19-linker-tools (1:19.1.7-1+b1) ...
Selecting previously unselected package libclang1-19.
Preparing to unpack .../03-libclang1-19_1%3a19.1.7-1+b1_amd64.deb ...
Unpacking libclang1-19 (1:19.1.7-1+b1) ...
Selecting previously unselected package clang-19.
Preparing to unpack .../04-clang-19_1%3a19.1.7-1+b1_amd64.deb ...
Unpacking clang-19 (1:19.1.7-1+b1) ...
Preparing to unpack .../05-clang_1%3a19.0-63_amd64.deb ...
Unpacking clang (1:19.0-63) over (1:16.0-58.1) ...
Selecting previously unselected package clang-format-19.
Preparing to unpack .../06-clang-format-19_1%3a19.1.7-1+b1_amd64.deb ...
Unpacking clang-format-19 (1:19.1.7-1+b1) ...
Selecting previously unselected package clang-format:amd64.
Preparing to unpack .../07-clang-format_1%3a19.0-63_amd64.deb ...
Unpacking clang-format:amd64 (1:19.0-63) ...
Selecting previously unselected package libclang-rt-19-dev:amd64.
Preparing to unpack .../08-libclang-rt-19-dev_1%3a19.1.7-1+b1_amd64.deb ...
Unpacking libclang-rt-19-dev:amd64 (1:19.1.7-1+b1) ...
Selecting previously unselected package llvm-19-runtime.
Preparing to unpack .../09-llvm-19-runtime_1%3a19.1.7-1+b1_amd64.deb ...
Unpacking llvm-19-runtime (1:19.1.7-1+b1) ...
Selecting previously unselected package llvm-19.
Preparing to unpack .../10-llvm-19_1%3a19.1.7-1+b1_amd64.deb ...
Unpacking llvm-19 (1:19.1.7-1+b1) ...
Selecting previously unselected package llvm-19-tools.
Preparing to unpack .../11-llvm-19-tools_1%3a19.1.7-1+b1_amd64.deb ...
Unpacking llvm-19-tools (1:19.1.7-1+b1) ...
Selecting previously unselected package llvm-19-dev.
Preparing to unpack .../12-llvm-19-dev_1%3a19.1.7-1+b1_amd64.deb ...
Unpacking llvm-19-dev (1:19.1.7-1+b1) ...
Setting up libclang1-19 (1:19.1.7-1+b1) ...
Setting up libclang-common-19-dev:amd64 (1:19.1.7-1+b1) ...
Setting up libclang-rt-19-dev:amd64 (1:19.1.7-1+b1) ...
Setting up llvm-19-linker-tools (1:19.1.7-1+b1) ...
Setting up llvm-19-runtime (1:19.1.7-1+b1) ...
Setting up llvm-19-tools (1:19.1.7-1+b1) ...
Setting up libclang-cpp19 (1:19.1.7-1+b1) ...
Setting up clang-format-19 (1:19.1.7-1+b1) ...
Setting up clang-19 (1:19.1.7-1+b1) ...
Setting up clang (1:19.0-63) ...
Setting up llvm-19 (1:19.1.7-1+b1) ...
Setting up clang-format:amd64 (1:19.0-63) ...
Setting up llvm-19-dev (1:19.1.7-1+b1) ...
Processing triggers for libc-bin (2.40-3) ...
Processing triggers for systemd (256.6-1) ...
Processing triggers for man-db (2.13.0-1) ...
Processing triggers for kali-menu (2024.4.0) ...
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ clang-format hello_world.cpp -style=Mozilla -i hello_world.cpp
No such file or directory
No such file or directory
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ clang-format helloworld.cpp -style=Mozilla -i hello_world.cpp 
No such file or directory
No such file or directory
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ clang-format helloworld.cpp -style=Mozilla -i helloworld.cpp 
No such file or directory
No such file or directory
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ ls
f.gitignore  LICENSE  README.md  ttt  ttt.txt
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git checkout patch1
Switched to branch 'patch1'
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ clang-format helloworld.cpp -style=Mozilla -i helloworld.cpp  
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git add helloworld.cpp
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git commit -m "Стиль изменен"
[patch1 b0c0c54] Стиль изменен
 1 file changed, 7 insertions(+), 6 deletions(-)
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ get push origin patch2       
Command 'get' not found, did you mean:
  command 'geg' from deb geg
  command 'kget' from deb kget
  command 'gem' from deb ruby-rubygems
  command 'net' from deb samba-common-bin
  command 'bget' from deb ax25-tools
  command 'got' from deb got
  command 'git' from deb git
  command 'gpt' from deb gpt
  command 'eet' from deb libeet-bin
  command 'gen' from deb multimon
  command 'wget' from deb wget
  command 'gt' from deb genometools
  command 'gmt' from deb gmt
  command 'dget' from deb devscripts
  command 'fet' from deb fet
Try: sudo apt install <deb name>
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git push origin patch2
Username for 'https://github.com': mrglist3431
Password for 'https://mrglist3431@github.com': 
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote: 
remote: Create a pull request for 'patch2' on GitHub by visiting:
remote:      https://github.com/mrglist3431/lab02/pull/new/patch2
remote: 
To https://github.com/mrglist3431/lab02.git
 * [new branch]      patch2 -> patch2
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git pull origin patch1 --rebase
remote: Enumerating objects: 5, done.
remote: Counting objects: 100% (5/5), done.
remote: Compressing objects: 100% (3/3), done.
remote: Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (3/3), 955 bytes | 955.00 KiB/s, done.
From https://github.com/mrglist3431/lab02
 * branch            patch1     -> FETCH_HEAD
   dfaf018..44d10d3  patch1     -> origin/patch1
Auto-merging helloworld.cpp
CONFLICT (content): Merge conflict in helloworld.cpp
error: could not apply b0c0c54... Стиль изменен
hint: Resolve all conflicts manually, mark them as resolved with
hint: "git add/rm <conflicted_files>", then run "git rebase --continue".
hint: You can instead skip this commit: run "git rebase --skip".
hint: To abort and get back to the state before "git rebase", run "git rebase --abort".                                                                   
hint: Disable this message with "git config advice.mergeConflict false"
Could not apply b0c0c54... Стиль изменен
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ nano helloworld.cpp
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git rebase --continue          
helloworld.cpp: needs merge
You must edit all merge conflicts and then
mark them as resolved using git add
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ nano helloworld.cpp
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git rebase --continue 
helloworld.cpp: needs merge
You must edit all merge conflicts and then
mark them as resolved using git add
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ nano helloworld.cpp  
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git rebase --continue
helloworld.cpp: needs merge
You must edit all merge conflicts and then
mark them as resolved using git add
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git add helloworld.cpp
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git rebase --continue 
[detached HEAD 8b00324] Стиль изменен
 1 file changed, 5 insertions(+), 1 deletion(-)
Successfully rebased and updated refs/heads/patch1.
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git commit -m "Стиль изменен"
On branch patch1
nothing to commit, working tree clean
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git push -f origin patch2      
Username for 'https://github.com': mrglist3431
Password for 'https://mrglist3431@github.com': 
Everything up-to-date
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ 
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ nano helloworld.cpp      
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git push origin patch1   
Username for 'https://github.com': mrglist3431
Password for 'https://mrglist3431@github.com': 

Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 16 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 453 bytes | 453.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/mrglist3431/lab02.git
   44d10d3..8b00324  patch1 -> patch1
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ 
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git commit -m "Стиль изменен"
On branch patch1
nothing to commit, working tree clean
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git checkout patch2                                         
Switched to branch 'patch2'
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ git add helloworld.cpp
fatal: pathspec 'helloworld.cpp' did not match any files
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ nano helloworld.cpp   
                                                                             
┌──(kali㉿kali)-[~/mrglist3431/workspace/lab02]
└─$ 
