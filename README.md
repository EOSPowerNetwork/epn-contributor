# Intro
Open the EPN System Smart Contract in a docker container along with an installation of EOS that includes the EPN pull-transactions plugin.

# Prerequisites
1. VSCode installed on your development PC
2. [Remote - Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) VSCode extension has been installed

# How to use
1. Clone this repo
2. Open the repo directory in VSCode
3. Run the ```Remote-Containers: Rebuild and Reopen in Container``` command in VSCode

That's it! VSCode will then relaunch, and it will connect to a new docker container that has everything already set up for you. Before it connects to the containier, it will need to build the image. The image includes a full build of the entire EOS project, and therefore generally takes a long time to be ready (over an hour).

# Misc notes
When VSCode closes, the container stops. The data within the container is not accessible, as it's stored in an unnamed volume mounted on your PC, only accessible through the docker container launched by VSCode.

All changes made within the container will persist on that PC (as long as you don't delete the docker volume), and must be pushed to a git repository if you want to work on it on another PC.
