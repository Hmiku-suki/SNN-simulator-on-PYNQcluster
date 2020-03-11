# SNN-simulator-on-PYNQcluster
A Spiking neural network simulator NEST base on FPGA‘s cluster（LIF NEURON）  
![image](https://github.com/OpenHEC/SNN-simulator-on-PYNQcluster/blob/master/overview.png)
## Quick Start
 * Petalinux
 * Install NEST-14.0-FPGA  
   * Installing PyNN requires:  
    `sudo apt-get install -y \`  
    `cython \`  
    `libgsl-dev \`  
    `libltdl-dev \`  
    `libncurses-dev \`  
    `libreadline-dev \`  
    `python-all-dev \`  
    `python-numpy \`  
    `python-scipy \`  
    `python-matplotlib \`  
    `python-nose \`  
    `openmpi-bin \`  
    `libopenmpi-dev`
   * Configure NEST:  
    `cd NEST-14.0-FPGA`  
    `cmake -Dwith-python=3 -DCMAKE_INSTALL_PREFIX:PATH=./ </path/to/NEST/src>`  
   * Compile and install NEST:  
    `make`  
    `make install`  
    `make installcheck`  
    `source </path/to/nest_install_dir>/bin/nest_vars.sh`  
   * References: https://nest-simulator.readthedocs.io/en/stable/installation/linux_install.html
 * Install PYNN  
   * Installing PyNN requires:    
    `Python (version 2.7, 3.3-3.7)`  
    `a recent version of the NumPy package`  
    `the lazyarray package`  
    `the Neo package (>= 0.5.0)`  
    `at least one of the supported simulators: e.g. NEURON, NEST, or Brian.`  
   * Optional dependencies are:    
    `mpi4py (if you wish to run distributed simulations using MPI)`  
    `either Jinja2 or Cheetah (templating engines)`  
    `the CSA library`  
    * Install PyNN:  
    `pip install pyNN`    
    * References:http://neuralensemble.org/docs/PyNN/installation.html  
## Repo organization
The repo is organized as follows:
 * snn_object：Describes a new biologically plausible mechanism for generating intermediate-level visual representations using an          unsupervised learning scheme.
   * iaf_psc_exp.bin：LIF NEURON bitstream
 * NEST-14.0-FPGA：implemention Spiking neural network simulator NEST on FPGA cluster
## References
### NEST  
NEST is a simulator for spiking neural network models, ideal for networks of any size.  
NEST Simulation:http://www.nest-simulator.org    
NEST-14.0 github：https://github.com/nest/nest-simulator/releases/tag/v2.14.0  

### pyNN  
A Python package for simulator-independent specification of neuronal network models.  
PyNN :http://neuralensemble.org/PyNN/  

### NEST base on GPU  
Implemention Spiking neural network simulator NEST on multi-GPU and distributed GPU  
https://github.com/pnquanganh/opencl-nest  
Nguyen Q A P, Andelfinger P, Cai W, et al. Transitioning Spiking Neural Network Simulators to Heterogeneous Hardware[C]//Proceedings of the 2019 ACM SIGSIM Conference on Principles of Advanced Discrete Simulation. ACM, 2019: 115-126.

### SNN simulator base on FPGA
Paper:A.Podobas,S.Matsuoka,Luk Wayne.Designing and accelerating spiking neural networks using OpenCL for FPGAs[C].//International   Conference on Field Programmable Technology (ICFPT).Melbourne,VIC, Australia: IEEE,2017.  

### snn_object_recognition on PYNN-NEST  
Describes a new biologically plausible mechanism for generating intermediate-level visual representations using an unsupervised learning   scheme.
https://github.com/roberthangu/snn_object_recognition  
Paper:Masquelier, Timothée, Thorpe S J. Unsupervised Learning of Visual Features through Spike Timing Dependent Plasticity[J].PLoS     Computational Biology, 2007, 3(2):e31.  

### others
Paper：Schuman C D , Potok T E , Patton R M , et al. A Survey of Neuromorphic Computing and Neural Networks in Hardware
