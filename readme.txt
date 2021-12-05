 1. download java minecraft server.jar from https://www.minecraft.net/en-us/download/server
 2. put it into directory with corresponding Dockerfile
 3. run: docker build <ARCH_FOLDER> -t my-minecraft-server

example (":18" is a version tag):
 docker build x86_64/ -t my-minecraft-server:18
 docker run -d -it -p 25565:25565 --restart unless-stopped -v mc-server-data:/opt/minecraft/ my-minecraft-server:18

upgrade:
    In order to upgrade the server you don't need to re-build an image (if you use persistent volume). In the
    example above the "mc-server-data" volume is used. So you can just replace server.jar file in the volume
    directory and restart the server.