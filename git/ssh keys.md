
#SSH Keys

##moving
####you can move your ssh keys from one environment to another.



##You will need to reset the permissions within the new environment
    chmod 600 ~/.ssh/id_rsa
    chmod 600 ~/.ssh/id_rsa.pub

##You may have to use sudo
    sudo chmod 600 ~/.ssh/id_rsa
    sudo chmod 600 ~/.ssh/id_rsa.pub

