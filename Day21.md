# Day 21


## What problem do docker volumes solve?

It prevents the data to be accidentally removed along with container, with a volume, even if container is removed, the data survives.


## Difference between container storage and volume storage?

Container storage: temporary storage in the container. Any files saved here will be wiped out as soon as the container is deleted.

Volume storage: Dedicated storage folders managed by docker on your host machine outside the container. Data survives even when the container is removed.


## What does docker volume create my-volume do?

It created a volume named as my-volume.


## What does -v my-volume:/data mean?

It stored the /data in "my-volume" volume. Anything we do inside /data will automatically saved in volume in our local machine.


## Why was notes.txt still present after deleting the first container?

It survived because notes.txt is in /data which is stored on our local machine by volume storage and not in container, since it is not stored in container, it survived even after first container was removed.


## In real-world application, why would a database use volumes?

Databases holds very important and permanent data. Without a volume, if the container is accidentally removed, all the data stored inside it will be erased with it.
