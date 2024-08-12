# Run Forge installer
java -jar forge-1.21-51.0.33-installer.jar --installServer=/home/minecraft/multicraft/jar/forge/
# Copy unix_args.txt to jar/forge folder
find /home/minecraft/multicraft/jar/forge/libraries/ -name 'unix_args.txt' -exec cp "{}" /home/minecraft/multicraft/jar/forge/ \;
# Adapt paths in unix_args.txt to load libraries from the daemon "jar" directory
sed -i 's,libraries,/home/minecraft/multicraft/jar/forge/libraries,g' /home/minecraft/multicraft/jar/forge/unix_args.txt
