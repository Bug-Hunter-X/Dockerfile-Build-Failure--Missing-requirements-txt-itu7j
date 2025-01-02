# Dockerfile Bug: Missing requirements.txt
This repository demonstrates a common error in Dockerfiles: attempting to use a file that isn't present in the build context.
The original Dockerfile attempts to copy `requirements.txt` and run `pip install`, but this file is not included.  This leads to a build failure.
The `Dockerfile.fixed` shows the corrected version, including the missing file. 

## To Reproduce
1. Clone this repository
2. Try to build the original `Dockerfile` using `docker build -t my-app .`
3. Observe the build error.
4. Build the fixed `Dockerfile.fixed` to see the successful build.