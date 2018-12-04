Docker:

It is a containerization platform which packages applicationan and all its dependencies together in the form of container.
docker client use RestAPI, SocketIO and TCP to interect with the Docker daemon.

Docker Image:
It is the read ony template used to create containers by using RUN command. It is stored in Docker HUB or in local registry.

Docker registry:
Docker registry is a storage component for docker images.

Steps to install Docker:

Step1: Install Oracle virtual box.

Step 2: install Chocolatey packgae incase you are using 32 bit OS

To install it through administrative Powershell session run:

iex ((new-object net.webclient).DownloadString('https://chocolatey/install.ps1'))

To install it through administrative command line RUN:

@powershell -NoProfile -ExecutionPolicy Bypass -Command "iex ((new-object net.webclient).DownloadString
('https://chocolatey.org/install.ps1'))" && SET PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin

Step 3:Run  Choco install docker-machine -y

Step-4:Run docker-machine enc default (need to tell docker to talk to the new machine).

Step 5:Connect your shell to the new machine run:
eval "$(docker-machine env default)"

In case if you used chocolatey to run docker machine,run below command:
Run this command to configure your shell:
# & "C:\ProgramData\chocolatey\lib\docker-machine\bin\docker-machine.exe" env default | Invoke-Expression

Step 6: docker-machine ssh (log into or run a command on machine with SSH).
