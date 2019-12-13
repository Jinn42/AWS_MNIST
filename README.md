# AWS_MNIST

## 1. TRAINMACHINE

### (1) Lunch an instance

You choose Amazon Linux 2 AMI (HVM) or Ubuntu.

Public Subnet → Enable Auto-assign Public IP → Size (GiB): 15 → SG_Ubuntu → Key.pem

### (2) Set up machine through PuTTY

Save sessions: MNIST → click on the botton "Save"

Install [Anaconda](https://www.anaconda.com/distribution/) by copy the download URL for Linux

    wget https://repo.anaconda.com/archive/Anaconda3-2019.10-Linux-x86_64.sh

    sudo bash Anaconda3-2019.10-Linux-x86_64.sh 

Answer yes to all questions, or just keep pressing SPACE then type yes.

Check if conda works. When getting command is not found after installation, try the following code.

    export PATH=~/anaconda3/bin:$PATH

!()[]

Install jupyter notebook

    jupyter notebook --ip=0.0.0.0 --no-browser

Go to Jupyter page you just linked. Click NEW → Terminal

Creat a new virtual environment

    conda install nb_conda  #This needs to be done outside your virtual env
    
    conda create -n MNIST python=3.6  #MNIST can replace by any name of env you like
    conda activate MNIST
    
    conda install ipykernel
    ipython kernel install --user --name=MNIST    #MNIST can replace by any name you want to display
    
Train MNIST model

    conda install keras
    conda install opencv
    
If you get the following command, try the following code and do it again.

    sudo chown -R $USER:$USER anaconda3

!()[]

Copy [TRAINMACHINE](https://github.com/wulinghsuan/AWS_MNIST/tree/master/TRAINMACHINE) folder to the env

    sudo apt install git
    git clone https://github.com/wulinghsuan/AWS_MNIST/tree/master/TRAINMACHINE

## 2. FRONTEND Server



## 3. BACKEND Server
