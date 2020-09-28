## Install Anaconda  

reference: https://www.digitalocean.com/community/tutorials/how-to-install-anaconda-on-ubuntu-18-04-quickstart
- Download the file from Anaconda website
   ```
   bash Anaconda3-latest-Linux-x86_64.sh
   ```
- Activate Conda
   ```
   source ~/.bashrc
   ```
- New conda env
   ```
   conda create --name my_env python=3.8
   conda activate my_env
   ```

- Check which python in use  

   Anaconda has been installed in the server with pkgs. However, the default python version is in `/usr/bin/python` 
   Command `which python` could check which python we are using   

- Set the environment variable  
   ```
   vim ~/.bash_profile (or ~/.bashrc)
   Add export PATH="/home/name/Anaconda3/bin:$PATH" in the end of .bashrc
   source ~/.bash_profile
   ```
   
- Check the added path: `echo $PATH`  

   * folder in front of the PATH would be taken as the default version  



## Jupyter notebook on server
   - Set up a SSL tunnel: `ssh -L port_number:localhost:8888 me@remote.address`  
   - Switch to my_env: `source activate my_env`  
   - Start Jupyter: `$ jupyter notebook`  
   - Visit the server by: http://localhost:port_number
