# Collective variables module (Colvars)

A software module for molecular simulation and analysis that provides a high-performance implementation of sampling algorithms defined on a reduced space of continuously differentiable functions (aka collective variables).

The module itself implements a variety of functions and algorithms, including free-energy estimators based on thermodynamic forces, non-equilibrium work and probability distributions.

## Obtaining and using

The easiest way to obtain binary versions of Colvars is via the simulation programs [NAMD](http://www.ks.uiuc.edu/Research/namd/) and [LAMMPS](http://lammps.sandia.gov/) and the visualization program [VMD](http://www.ks.uiuc.edu/Research/vmd/).  Please check [here](https://github.com/colvars/colvars/releases) to see which version of Colvars is included with the round-number versions of VMD and NAMD.  Colvars is integrated with LAMMPS on a near-continuous basis, most often immediately after significant code changes.

## Documentation

The [Colvars webpage](http://colvars.github.io/) includes user documentation for the three codes, as well as a Doxygen-based [developer documentation](http://colvars.github.io/doxygen/html/).

The reference article is:
G. Fiorin, M. L. Klein, and J. Hénin, Molecular Physics 111, 3345 (2013).  
http://dx.doi.org/10.1080/00268976.2013.813594  \[[BibTex file](https://github.com/colvars/colvars/blob/master/doc/ref_Fiorin_2013.bib?raw=true)\] \[[Endnote file](https://github.com/colvars/colvars/blob/master/doc/ref_Fiorin_2013.ciw?raw=true)\]

## Example input

Please see the [examples](https://github.com/colvars/colvars/tree/master/examples?raw=true) folder of this repository.  Configuration options (particularly, the selections of atoms) require minimal changes to reflect the specifics of each simulation.

The [tests](https://github.com/colvars/colvars/tree/master/tests?raw=true) folder also contains functional segments of Colvars configuration, used to build numerical tests of code accuracy and stability.  Feel free to use these segments in your production runs.

## Updating to the latest version

To recompile each program with the most recent version of the module, [download](https://github.com/colvars/colvars/archive/master.zip) the `master` branch of this repository, or clone it via git:
```
git clone https://github.com/colvars/colvars.git
```
and run the provided `update-colvars-code.sh` script against the unpacked source tree of any of the supported programs:
```
./update-colvars-code.sh /path/to/NAMD_X.YY_Source ; # updates NAMD
./update-colvars-code.sh /path/to/vmd-X.Y.Z        ; # updates VMD
./update-colvars-code.sh /path/to/lammps           ; # updates LAMMPS
```
and recompile them.

The `update-colvars-code.sh` script is synchronized with the latest version of each program: [NAMD nightly build](http://www.ks.uiuc.edu/Development/Download/download.cgi?PackageName=NAMD), [VMD CVS](http://www.ks.uiuc.edu/Research/vmd/doxygen/cvsget.html) and the Github repository of [LAMMPS](https://github.com/lammps/lammps).  Earlier versions are not supported.

## Which version is recommended?

All bugfixes are released through the `master` branch, which is to be considered the "*stable*" release at any given time.  The input syntax is *backward-compatible* and output files are *forward-compatible*.  Feel free to download Colvars and update NAMD, VMD or LAMMPS as needed.

Other branches are dedicated to the development of specific features: please use them at your own discretion.

## Feedback

Please use the "Issues" tab of this page to submit new bug reports or to suggest new features.

## License

This software is distributed under the GNU Lesser General Public License, version 3.  See COPYING.LESSER for complete licensing terms.
