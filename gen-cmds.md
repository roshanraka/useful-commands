# change owner for files
    
    sudo chown "$USER":"$USER" /home/"$USER"/.docker -R
    sudo chmod g+rwx "/home/$USER/.docker" -R

## port forward ssh

    ssh -i awsdb-sample.pem -L 27017:sample-cluster.cluster-chdxutslwblh.us-east-2.docdb.amazonaws.com:27017 \ ec2-user@ec2-18-219-18-29.us-east-2.compute.amazonaws.com -N


    CNTX={users|orgs}; NAME={username|orgname}; PAGE=1
    
    curl "https://api.github.com/$CNTX/$NAME/repos?page=$PAGE&per_page=100" | grep -e 'git_url*' | cut -d \" -f 4 | xargs -L1 git clone

    CNTX=users; NAME=roshanraka; PAGE=1
    
    curl "https://api.github.com/users/roshanraka/repos?page=1&per_page=100" | grep -e 'git_url*' | cut -d \" -f 4 | xargs -L1 git clone
