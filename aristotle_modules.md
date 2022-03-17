# loading the standard modules 

In order to make life easier, load the following default modules: 

``` module load default-modules ```

you could also add the above line into the .bashrc file so it is loaded on startup (actually login).

with this command loaded, running the command

```module list ```
should give 

```
Currently Loaded Modulefiles:
  1) ops-tools/2.0.0               12) nedit/5.6-aug15
  2) gcc-libs/4.9.2                13) dos2unix/7.3
  3) cmake/3.21.1                  14) giflib/5.1.1
  4) flex/2.5.39                   15) emacs/26.3
  5) git/2.32.0                    16) tmux/3.2a
  6) apr/1.7.0                     17) mrxvt/0.5.4
  7) apr-util/1.6.1                18) userscripts/1.4.0
  8) subversion/1.14.1             19) rcps-core/1.0.0
  9) screen/4.8.0-ucl1             20) compilers/intel/2018/update3
 10) gerun                         21) mpi/intel/2018/update3/intel
 11) nano/2.4.2                    22) default-modules/2018
```


# Loading lammps on Aristotle
To run lammps on Aristotle we need to load these special modules: 
```
module load default-modules
module -f unload compilers mpi gcc-libs
module load beta-modules
module use --append /home/ccaabaa/lib/modulefiles/development /home/ccaabaa/lib/modulefiles/bundles /home/ccaabaa/lib/modulefiles/beta
module load gcc-libs/10.2.0
module load compilers/gnu/10.2.0
module load numactl/2.0.12
module load binutils/2.36.1/gnu-10.2.0
module load ucx/1.9.0/gnu-10.2.0
module load mpi/openmpi/4.0.5/gnu-10.2.0
module load python3/3.9-gnu-10.2.0-aristotle
module load lammps/29sep21up2/basic/gnu-10.2.0-aristotle
```
