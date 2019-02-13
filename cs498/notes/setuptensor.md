The following steps assumes you use a Linux workstation in the Linux Lab in HT 319.

# Instllation of Anaconda in your local directory on tensor.hood.edu:

1. Open a terminal window, and ssh to your account at tensor.hood.edu

2. I placed a copy of freshly downloaded anaconda installation file on the tensor.  You may start the installation process by

`bash ~cs498h00/Anaconda3-2018.12-Linux-x86_64.sh`

Agree/Yes with all questions.

3. Activate anaconda environment with 

either `source ~/.bashrc` or logout tensor.hood.edu then login again

4. Continue to install tensorflow and keras with following commands:

`conda install tensorflow`

`conda install keras`

# Launch Jupyter notebook from tensor.hood.edu:

`jupyter notebook --no-browser --ip=0.0.0.0`

```
(base) xliu@tensor:~$ jupyter notebook --no-browser --ip=0.0.0.0
[I 07:39:44.522 NotebookApp] The port 8888 is already in use, trying another port.
[I 07:39:44.581 NotebookApp] JupyterLab extension loaded from /home/xliu/anaconda3/lib/python3.6/site-packages/jupyterlab
[I 07:39:44.581 NotebookApp] JupyterLab application directory is /home/xliu/anaconda3/share/jupyter/lab
[I 07:39:44.583 NotebookApp] Serving notebooks from local directory: /home/xliu
[I 07:39:44.584 NotebookApp] The Jupyter Notebook is running at:
[I 07:39:44.584 NotebookApp] http://(tensor or 127.0.0.1):8889/
[I 07:39:44.584 NotebookApp] Use Control-C to stop this server and shut down all kernels (twice to skip confirmation).
```
Find and write down the port number used by the notebook, in this case **8889**.  The port number could change each time.  Keep this window open.  In the next step you will need a *token* number which is not displayed here because I set up a password earlier.

# Connect to tensor.hood.edu through SSH tunneling

Open another terminal window, assign a local port number.  The example uses **8888**, but other *allowed* numbers should also work.  

`ssh -N -f -L 8888:tensor.hood.edu:8889 xliu@tensor.hood.edu`

Type your password for your account on tensor.hood.edu when prompted.

Windows 10 comes with a native SSh client.  You will need to enable it because it is optional.  Use [Google](http://bfy.tw/MHzu) to find up to date instructions on how to enable SSH on Windows 10.  Type in the same `ssh` command from Windows command line window (type `CMD` in Windows search bar).

# Use the Notebook:

Launch any web browser, type `localhost:8888` in the address bar.

You will be prompted for either a password or a token number.  You are all set.
