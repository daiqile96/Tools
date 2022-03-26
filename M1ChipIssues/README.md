# Solutions for issues with using Apple silicon Macs

## Installation Issues 

 - Macfuse: 
   - To install [macFUSE](https://osxfuse.github.io), we need reduced security by following the steps provided by  Parvez Shaikh [here](https://techstuffer.com/fuse-for-macos-apple-silicon-m1/):
      - Turn off your Mac. 
      - Press and hold the power button until you see ‘loading startup options’ under Apple logo. 
      - Select Options and click Continue. Choose an administrator account and enter its password.
      - Utilities > Startup Security Utility and choose Reduced Security. Turn on both checkboxes underneath and click OK.
  
 - R:
   - Download the R with Apple silicon arm64 build
   - Follow the steps in [this page](https://mac.r-project.org/tools/) to install Xcode and GNU Fortran compiler
   - For GNU Fortran compiler, please choose the version that matches your R version. 
     - Download  GNU Fortran from the page shown above.
     - Move it into /opt/R/arm64/
     - Unpack it
     - export PATH=$PATH:/opt/R/arm64/gfortran/bin
     - Remember to prefix with sudo if you require admin permissions.
   - If the Xcode and GNU Fortran compiler are not installed, many R packages could not be installed successfully.
