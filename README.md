# PraSaga_projects


This is the repo for PraSaga training I conducted for [HER Dao on 5th August](https://lu.ma/PraSagaDevSession).
PraSaga environment setup as per [instructions](https://code.prasaga.com/dbeberman/hlfxbom-public) explained in [video](https://www.youtube.com/watch?v=dNAkDeLpG2Y&list=PLWwdXaokFYJt60Tkf00a-BRAdES0Nu1We&index=1)

Additional Setup Instructions:

0. Make an account at xbom.io and understand the [inspiration behind PraSaga](https://www.youtube.com/watch?v=GkIPFbS4RDM)
1. Setup Amazon Workspaces as per [link](https://www.youtube.com/watch?v=U4V44EFJeLs)
2. In Desktop Client for AWS Workspaces, login with any user of the workspace you created.
3. Download Docker in workspace. Register account at hub.docker.com and signin with same cred in desktop Docker. 
   - Install git 
   - Install curl
   - Install specific golang in docker:
   - Login to Docker desktop and go to Remote repositories. Install specific golang version and then go to Local repo to run the container with that golang      version. Go to containers tab and hit CLI button to run terminal with this golang version.
     Alternatively in terminal, you can install golang using:
     docker ls => get container id for golang version.
     docker container ls 
     docker exec -it <golang container id> /bin/sh

   - Create prasaga folder in home in terminal: 
      - mkdir /home/prasaga
      - cd /home/prasaga

   - Execute the bootstrap shell script in same /home/prasaga:
     `curl -sSL https://code.prasaga.com/dbeberman/hlfxbom-public/-/raw/BoschHackathon/xbombootstrap.sh | bash -s`

4. Understand [hyperledger](https://hyperledger-fabric.readthedocs.io/en/latest/whatis.html) and learn to do different operations on [test network](https://github.com/hyperledger/fabric-samples/tree/main/test-network/scripts)
  
5. Get prepared to code in Go (for Smart objects) and Python (for transaction scripts)
   - [Go Notes](https://docs.google.com/document/d/17RohAt0Ut-kNhRClCbty3WvF3dkwIE8F7Xh00r7KjtU/edit?usp=sharing)
   - [Python Notes](https://docs.google.com/document/d/13BTxZVr3hvXsIHyPWLsYUGol_Ry-fExBA8J4VbSezqE/edit?usp=sharing)

6. Go through [example prasaga transaction code](https://www.xbom.io/resources/)

