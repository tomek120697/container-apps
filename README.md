## **THIS IS A FORK ONLY FOR arm32v7 PROCESSOR**
#### Addition test of other docker containers and lxc containers for arm32v7 architecture
Tested on TS-231P, but 99% will work on others based on this architecture.

The list with containers is updated by me from time to time. Not everything can be loaded due to the version of docker itself in qnap. Dockers based on newer ubuntu, debian etc distributions may not work. I try to test new dockers as much as possible.

---
**Instructions for LXC Containers:**
1. You need to enable SSH.
2. Log in to your administrator account and exit the Management Console if you have it enabled.
3. to start the download and load the lxc container type the command:
    ```sh
    lxc-create -n name -t /usr/share/lxc/templates/lxc-download
    ```
    1. In the **name** field, enter a name for the container.
    2. -t refers to the template. There are several templates but I recommend using the one above.
    3. You can find additional information by typing.
    ```sh
    lxc-create --help
    ```
4. The installer will then ask you for the distribution, release, and architecture (for the TS-231P model tested, this will be armhf).
5. Done! The rest of the parameters can be set in the Container Station.

A list of LXC images can be found:
- [Linux Containers](http://uk.images.linuxcontainers.org/)
- [On my website (the list includes only armhf)](https://tomek120697.pl/qnap/lxc.html)

# Important

After installation, some applications may be missing from the container and errors will pop up when you try to change them. __DO NOT PANIC!__ Read the warning calmly. This will usually be an error that some application or script cannot be found.

For example: after installing the ubuntu (dist:focal) container, you may not be able to switch NAT to Bridge. An error will pop up due to resolvconf not being found. Just issue the install command "apt-get install resolvconf".

---

### Things I plan to do at a later date:
- Add lxc containers to the list in container station
- Add more docker images
- Make new icons for docker images
- Instructions for docker containers
