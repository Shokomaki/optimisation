# optimisation
Fichiers optimisé pour la version 1.16.5 de minecraft

N'oubliez pas de modifier si possible la commande "Startup" de votre serveur minecraft pour avoir des performances optimales !
Utilisez Java 11 pour lancer le serveur minecraft.

Remplacez seulement "SERVEUR.JAR" par le nom de votre lanceur 1.16.X, et "RAM" par la mémoire que vous souhaitez allouer à minecraft.
Les deux valeurs RAM doivent êtres identiques, pour un meilleur fonctionnement.
Laissez égallement 4 go de marge à la ram. (2go au système et 2go au serveur)

                Exemple:

J'ai un serveur avec 16go de ram
Je dois donc allouer 12 go de ram à mon serveur.

             Les java argument:


Java argument si vous utilisez moin de 12 go de ram:

java -XmsRAMG -XmxRAMG -Duser.timezone=Europe/Paris -XX:+UseG1GC -XX:+ParallelRefProcEnabled -XX:MaxGCPauseMillis=200 -XX:+UnlockExperimentalVMOptions -XX:+DisableExplicitGC -XX:+AlwaysPreTouch -XX:G1NewSizePercent=30 -XX:G1MaxNewSizePercent=40 -XX:G1HeapRegionSize=8M -XX:G1ReservePercent=20 -XX:G1HeapWastePercent=5 -XX:G1MixedGCCountTarget=4 -XX:InitiatingHeapOccupancyPercent=15 -XX:G1MixedGCLiveThresholdPercent=90 -XX:G1RSetUpdatingPauseTimePercent=5 -XX:SurvivorRatio=32 -XX:+PerfDisableSharedMem -XX:MaxTenuringThreshold=1 -Dusing.aikars.flags=https://mcflags.emc.gs -Daikars.new.flags=true -jar SERVER.JAR nogui

Java argument si vous utilisez plus de 12 go de ram:

java -XmsRAMG -XmxRAMG -Duser.timezone=Europe/Paris -XX:+UseG1GC -XX:+ParallelRefProcEnabled -XX:MaxGCPauseMillis=200 -XX:+UnlockExperimentalVMOptions -XX:+DisableExplicitGC -XX:+AlwaysPreTouch -XX:G1NewSizePercent=40 -XX:G1MaxNewSizePercent=50 -XX:G1HeapRegionSize=16M -XX:G1ReservePercent=15 -XX:G1HeapWastePercent=5 -XX:G1MixedGCCountTarget=4 -XX:InitiatingHeapOccupancyPercent=20 -XX:G1MixedGCLiveThresholdPercent=90 -XX:G1RSetUpdatingPauseTimePercent=5 -XX:SurvivorRatio=32 -XX:+PerfDisableSharedMem -XX:MaxTenuringThreshold=1 -Xlog:gc*:logs/gc.log:time,uptime:filecount=5,filesize=1M -Dusing.aikars.flags=https://mcflags.emc.gs -Daikars.new.flags=true -jar SERVER.JAR nogui

Je vous conseil égallement d'évité les plugins de type clear lag, ou les plugins de la team songoda qui sont très mal optimisé.

Des questions ?

Contactez moi via le discord de KingPerf par ticket, ou par message privé.
Je répond au demandes quand j'ai le temps donc merci de ne pas me spamer.
