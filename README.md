# PraSaga_projects


This is the repo for PraSaga training I conducted for [HER Dao on 5th August](https://lu.ma/PraSagaDevSession).
PraSaga environment setup as per [instructions](https://code.prasaga.com/dbeberman/hlfxbom-public) explained in [video](https://www.youtube.com/watch?v=dNAkDeLpG2Y&list=PLWwdXaokFYJt60Tkf00a-BRAdES0Nu1We&index=1)

Additional Setup Instructions:

0. Make an account at xbom.io and understand the [inspiration behind PraSaga](https://www.youtube.com/watch?v=GkIPFbS4RDM)
1. Setup Amazon Workspaces as per [link](https://www.youtube.com/watch?v=U4V44EFJeLs)
2. In Desktop Client for AWS Workspaces, login with any user of the workspace you created.
3. Install git, curl, 1.13.14 version of golang, docker and docker-compose:
     - sudo yum install golang-1.13.14
     - sudo yum install docker
     - sudo yum install git
     - sudo yum install curl
     - curl -L https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m) -o /usr/local/bin/docker-compose

(if error: Got permission denied while trying to connect to the Docker)
   - sudo chmod -x /var/run/docker.sock
   - sudo chmod 666 /var/run/docker.sock

   - Create prasaga folder in home in terminal: 
      - mkdir /home/prasaga
      - cd /home/prasaga

   - Execute the bootstrap shell script in same /home/prasaga:
     `curl -sSL https://code.prasaga.com/dbeberman/hlfxbom-public/-/raw/BoschHackathon/xbombootstrap.sh | bash -s`
   - cd /home/prasaga/fabric-samples/chaincode/classmanager
   - ./maketgz

   - GOPATH environment variable must include /home/prasaga/xbom/classmanagerchaincode
         - nano .bashrc
         - export GOPATH=$GOPATH:/home/prasaga/xbom/classmanagerchaincode
         - source .bashrc

   - Move to test-network in fabric-samples and execute 
         - ./network up
         - ./network.sh createChannel
         
4. Understand [hyperledger](https://hyperledger-fabric.readthedocs.io/en/latest/whatis.html) and learn to do different operations on [test network](https://github.com/hyperledger/fabric-samples/tree/main/test-network/scripts)
  
5. Get prepared to code in Go (for Smart objects) and Python (for transaction scripts)
   - [Go Notes](https://docs.google.com/document/d/17RohAt0Ut-kNhRClCbty3WvF3dkwIE8F7Xh00r7KjtU/edit?usp=sharing)
   - [Python Notes](https://docs.google.com/document/d/13BTxZVr3hvXsIHyPWLsYUGol_Ry-fExBA8J4VbSezqE/edit?usp=sharing)

6. Go through [example prasaga transaction code](https://www.xbom.io/resources/)

