# QCaD Workshops

A single repository for all Quantum Computing at Davis (QCaD) workshops.

## Contents
* 1 __Single Qubit Gates__
  * A gentle introduction to the qubit and its manipulation through single gates
* 2 __Multiple Qubit Gates__
  * Framework of knowledge for multiple qubit operations is introduced
* 3 __Intro to Qiskit__
  * First introduction to using IBM's Quantum Information Science Kit for Quantum Computing

## Usage

All the workshops are designed to be run in the __[Hephaestus](https://github.com/Quantum-Computing-at-Davis/Hephaestus)__ environment which contains all dependencies and tools needed for each workshop.

### Dependencies
Ensure that the following are installed on your machine:
* [git](https://git-scm.com/downloads)
* [Docker](https://www.docker.com/products/docker-desktop)

Make sure that `git` is properly installed on your computer by opening your terminal and typing
```
git --version
```
You should see some output about the version of git installed.

Also make sure that Docker is running in the background while all this is happening.

#### Windows 10 Home Edition User Warning

Unfortunately, Docker is not compatible with computers running Windows 10 Home Edition.

There are two options to work around this.

The first method is to install [Docker Toolbox](https://github.com/docker/toolbox/releases). Although this is the easiest way to get things working, keep in mind that Docker Toolbox is considered legacy software and will lose support over time. 

A safer alternative is to create a Virtual Machine on your computer running Linux (Ubuntu is a safe choice) and then install Docker for Linux inside THAT virtual machine. 

As long as the virtual machine has `git` as well as a browser of some sort (Firefox, Chrome, etc.), you can follow along with the instructions below and run the workshops.


### Running in Hephaestus
1. Create a folder on your computer through the terminal and inside the folder run:
```
git clone https://github.com/Quantum-Computing-at-Davis/Hephaestus.git .
```
2. Then clone the notebooks in like so:
```
git clone https://github.com/Quantum-Computing-at-Davis/Workshops.git
```
3. Fire up the environment with the following command:
```
docker-compose up
```
You should see output on the terminal that looks like this:
```
WARNING: The Docker Engine you're using is running in swarm mode.

Compose does not use swarm mode to deploy services to multiple nodes in a swarm. All containers will be scheduled on the current node.

To deploy your application across the swarm, use `docker stack deploy`.

Starting experimental_hephaestus_1 ... done
Attaching to experimental_hephaestus_1
hephaestus_1  | [W 07:28:38.255 NotebookApp] WARNING: The notebook server is listening on all IP addresses and not using encryption. This is not recommended.
hephaestus_1  | [I 07:28:38.261 NotebookApp] Serving notebooks from local directory: /home
hephaestus_1  | [I 07:28:38.261 NotebookApp] The Jupyter Notebook is running at:
hephaestus_1  | [I 07:28:38.261 NotebookApp] http://4f50d1cc4cb1:8888/?token=cd63635511cd3546da621c0420dc4a3725f1f8e7fdbe99d8
hephaestus_1  | [I 07:28:38.261 NotebookApp]  or http://127.0.0.1:8888/?token=cd63635511cd3546da621c0420dc4a3725f1f8e7fdbe99d8
hephaestus_1  | [I 07:28:38.261 NotebookApp] Use Control-C to stop this server and shut down all kernels (twice to skip confirmation).
hephaestus_1  | [C 07:28:38.267 NotebookApp]
hephaestus_1  |
hephaestus_1  |     To access the notebook, open this file in a browser:
hephaestus_1  |         file:///root/.local/share/jupyter/runtime/nbserver-1-open.html
hephaestus_1  |     Or copy and paste one of these URLs:
hephaestus_1  |         http://4f50d1cc4cb1:8888/?token=cd63635511cd3546da621c0420dc4a3725f1f8e7fdbe99d8
hephaestus_1  |      or http://127.0.0.1:8888/?token=cd63635511cd3546da621c0420dc4a3725f1f8e7fdbe99d8
```
Copy the URL from your terminal with the `127.0.0.1` option into any browser on your computer.

You should be greeted by what looks like a file navigator in your browser. You should see a *Workshops* folder that you can click on with subdirectories that contain a jupyter notebook for each workshop.

To stop the environment, hit `Ctrl-C` in your terminal. To start it again, just run `docker-compose up`. 

### Staying Up-To-Date

Hephaestus may be subject to updates and new workshops frequently come out.

To update Hephaestus, run the following:
```
docker-compose rm -f
docker-compose pull hephaestus
```
And to update notebooks, navigate to the *Workshop* directory in your terminal and run:
```
git pull
```
A text editor may appear in your terminal or window with some text about accepting a merge. Just save the file and close it.
