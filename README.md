# JIMRIC-ProcessingSoftwares
Collection of software packages installed in the JIMRIC 

This guide provides instructions for installing the following neuroimaging software on Ubuntu 22.04 LTS:

- FSL (https://fsl.fmrib.ox.ac.uk/fsl/fslwiki/FslInstallation)
- FreeSurfer (https://surfer.nmr.mgh.harvard.edu/registration.html)
- ANTs Toolbox (https://sourceforge.net/projects/advants/)
- MRtrix (https://mrtrix.readthedocs.io/en/latest/installation/package_install.html)
- ITK-SNAP (http://www.itksnap.org/pmwiki/pmwiki.php?n=Downloads.SNAP3)
- MATLAB (https://www.mathworks.com/products/matlab.html)

## FSL 
```bash
wget https://fsl.fmrib.ox.ac.uk/fsldownloads/fslinstaller.py && sudo python3 fslinstaller.py && echo '. /usr/local/fsl/etc/fslconf/fsl.sh' >> ~/.bashrc && source ~/.bashrc
```
## Freesurfer 
```
wget -N https://surfer.nmr.mgh.harvard.edu/pub/dist/freesurfer/7.2.0/freesurfer-linux-ubuntu_v20.04.2-7.2.0.tar.gz && tar -xzvf freesurfer-linux-ubuntu_v20.04.2-7.2.0.tar.gz && sudo mv freesurfer /opt/ && echo 'export FREESURFER_HOME=/opt/freesurfer' >> ~/.bashrc && echo 'source $FREESURFER_HOME/SetUpFreeSurfer.sh' >> ~/.bashrc && source ~/.bashrc
```
Copy your FreeSurfer license file to the FreeSurfer installation directory:
```
cp <path_to_license>/license.txt /opt/freesurfer/.license
```
## ANTs Toolbox 
```
sudo apt-get install -y ants
```
## MRtrix 
```
sudo apt-get install -y python3-numpy python3-scipy python3-matplotlib libeigen3-dev zlib1g-dev libqt5opengl5-dev python3-pyqt5.qtopengl && git clone https://github.com/MRtrix3/mrtrix3.git && cd mrtrix3 && ./configure && ./build && echo 'export PATH=$PWD/bin:$PATH' >> ~/.bashrc && source ~/.bashrc
```

