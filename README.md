### Run Nifi

    git clone https://github.com/systemctl-reload/nifi.git

    cd nifi
    
    mkdir input
    
    mkdir output
    
    docker-compose up -d
    
### Download csv file
    
    cd input
    wget https://people.sc.fsu.edu/~jburkardt/data/csv/addresses.csv
  
### Create GetFile Processor

    Input Directory: /opt/input
    File Filter: addresses.csv
    Keep Source File: True

    In Relationships tab select terminate

    APPLY

### Create PutFile Processor

    Directory: /opt/output
    Conflict Resolution Strategy: replace
    Create Missing Directories: false
