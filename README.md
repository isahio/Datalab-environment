# Datalab environment


First, open a terminal and run the following command:

<code>conda init bash</code>

This will instruct your terminal to prepare your terminal for running conda commands. Close the terminal, and open a new one. This will restart your terminal and makes sure that everything is initiated correctly.

To verify that the installation has worked, you can check whether your terminal shows something like (base) in front of every line in the terminal.

Now, with your new terminal, run the commands below. (Don’t copy all four lines at once into your terminal, but enter them one line at a time.)

<code>curl https://raw.githubusercontent.com/isahio/trial/main/environment.env?token=GHSAT0AAAAAACO2ABJBLVLURDOMCRF3ECYAZO6AKHA > environment.yml
conda install -n base conda-libmamba-solver
conda config --set solver libmamba
conda env create -f environment.yml
rm environment.yml</code>

This downloads a formatted description of what libraries to download and install, then installs the libraries, and subsequently removes the description (as we no longer need it).

From here on out when you open a terminal we can use the following command to enter the environment, and enable the use of all the libraries we installed:

<code>conda activate datalab</code>

To make sure that the environment we just installed is started every time we start a new terminal, we can run some commands.

To make sure that the <b>datalab</b> environment is activated every time that we start a terminal, we can run the following command:

<code>echo 'conda activate datalag' >> ~/.bash_profile</code>

We now need to perform two more commands, that will ensure that Python and sqlite function as intended on Windows:

<code>echo "alias python='winpty python'" >> ~/.bash_profile</code>

<code>echo "alias sqlite3='winpty sqlite3'" >> ~/.bash_profile</code>

<code>echo "alias checkpy='winpty checkpy'" >> ~/.bash_profile</code>

Now restart your terminal, and check whether it starts into the <b>datalab</b> environment.
