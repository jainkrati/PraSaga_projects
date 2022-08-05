# PraSaga_projects


This is the repo for PraSaga training.
PraSaga environment setup as per https://code.prasaga.com/dbeberman/hlfxbom-public , as explained in https://www.youtube.com/watch?v=dNAkDeLpG2Y&list=PLWwdXaokFYJt60Tkf00a-BRAdES0Nu1We&index=1

Setup Instructions:

0. Make an account at xbom.io and understand the inspiration behind PraSaga: https://www.youtube.com/watch?v=GkIPFbS4RDM
1. Setup Amazon Workspaces as per https://www.youtube.com/watch?v=U4V44EFJeLs
2. In Desktop Client for AWS Workspaces, login with any user of the workspace you created.
3. Download Docker in workspace. Register account at hub.docker.com and signin with same cred in desktop Docker. 

3.1. Install git 
3.3. Install curl
3.4. Install specific golang in docker:
Run this on a terminal :
docker pull golang:1.13.14 
Login to Docker desktop and go to Remote repositories. Install specific golang version and then go to Local repo to run the container with that golang version. Go to containers tab and hit CLI button to run terminal with this golang version.

Alternatively in terminal, you can install golang using:
docker ls => get container id for golang version.
docker container ls 
docker exec -it <golang container id> /bin/sh

3.5. Create prasaga folder in home 
mkdir /home/prasaga
cd /home/prasaga

3.6 Execute the bootstrap shell script in same /home/prasaga:

curl -sSL https://code.prasaga.com/dbeberman/hlfxbom-public/-/raw/BoschHackathon/xbombootstrap.sh | bash -s

4. Understand hyperledger (https://hyperledger-fabric.readthedocs.io/en/latest/whatis.html) and understand different scripts for functions of test network (https://github.com/hyperledger/fabric-samples/tree/main/test-network/scripts)
  
5. Get prepared to code in Go (for Smart objects) and Python (for consumer scripts)
Go Notes: https://docs.google.com/document/d/17RohAt0Ut-kNhRClCbty3WvF3dkwIE8F7Xh00r7KjtU/edit?usp=sharing
Python Notes: https://docs.google.com/document/d/13BTxZVr3hvXsIHyPWLsYUGol_Ry-fExBA8J4VbSezqE/edit?usp=sharing

6. Go through example code at https://www.xbom.io/resources/

