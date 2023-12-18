# trial


First, open a terminal and run the following command:

conda init bash

This will instruct your terminal to prepare your terminal for running conda commands. Close the terminal, and open a new one. This will restart your terminal and makes sure that everything is initiated correctly.

To verify that the installation has worked, you can check whether your terminal shows something like (base) in front of every line in the terminal.

Now, with your new terminal, run the commands below. (Don’t copy all four lines at once into your terminal, but enter them one line at a time.)

curl [https://raw.githubusercontent.com/spcourse/sp1-python/main/en/installing/computer/environment.env](https://raw.githubusercontent.com/isahio/trial/main/environment.env?token=GHSAT0AAAAAACLYIGHQ2RRJIMXWEQNDGIIOZMAU57Q) > environment.yml
conda install -n base conda-libmamba-solver
conda config --set solver libmamba
conda env create -f environment.yml
rm environment.yml

This downloads a formatted description of what libraries to download and install, then installs the libraries, and subsequently removes the description (as we no longer need it).

From here on out when you open a terminal we can use the following command to enter the environment, and enable the use of all the libraries we installed:

conda activate datalab  
