 1. download java minecraft server.jar from https://www.minecraft.net/en-us/download/server
 2. put it into directory with corresponding Dockerfile
 3. run: docker build <ARCH_FOLDER> -t my-minecraft-server

 example:
 docker build x86_64/ -t my-minecraft-server
 docker run -d -it -p 25565:25565 my-minecraft-server