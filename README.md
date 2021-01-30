# Final-Project
Using the Playbook
In order to use the playbook, you will need to have an Ansible control node already configured. Assuming you have such a control node provisioned:
SSH into the machine and follow the steps below:
Copy the src file to etc/ansible/files.
Update the hosts file to include the Raven Security ip address 192.168.1.110

Commands: 

To install docker: sudo apt install docker.io 

To install a ubuntu server on your docker machine: sudo docker run -ti cyberxsecurity/ubuntu:bionic bash 

To install ansible: sudo docker run -ti cyberxsecurity/ansible 

To view your new ansible machine name: sudo docker container list -a TO view running containers: sudo docker ps 

To start your ansible machine: sudo docker start {machine name} 

To attach you ansible machine: sudo docker attach {machine name} To run the playbook: ansible-playbook {playbookname.yml}


We can use the firewalld service to block off the ports from nmap scans as this shuts the ports down from the public  
        Commands:
        sudo systemctl enable firewalld 
        sudo systemctl status firewalld
        As our Scan revealed that port 22 was open we can run the command:
        sudo firewalld-cmd --add-port=22/tcp --permanent 

Update RWX Permissions on the Wordpress file to root only with the command chmod 700 this command will give access to root only   

   Encrypt The Wordpress File using a hashing algorithm such as MD5 
   Run the command md5sum on the entire wordpress file and it will encrypt the entire file 
   so even if the hacker is able to escalate to root they will not be able to view the information


Type gpedit.msc and gpedit will launch and you can update your password rules to include:  
                         Maximum Password Age
                         Minimum Password Length 
                         And Ensure Password Complexity is Enabled which will require you to use special characters such as !%&

