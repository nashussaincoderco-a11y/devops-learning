# DevOps Learning Journey 🚀

This repository documents my transition into Cloud Engineering and DevOps through CoderCo.

## 📂 Current Module: Networking

### My Assignment:
* Through this module, I have successfully mastered the end-to-end process of cloud hosting by provisioning an AWS EC2 instance, managing DNS records via Cloudflare to link my domain naseemnginx.co.uk, and using SSH to remotely configure a secure Nginx web server with SSL encryption. 


### Buying a Domain from Cloudfare
What I first done was purchase a domain from Cloudfare. Purpose of buying a domain was so that I am able to map my domain, "naseemginx.co.uk" to my server's IP. 

<img width="940" height="453" alt="image" src="https://github.com/user-attachments/assets/6b9caaba-411a-4130-b2c1-3c37ac21dfb1" />


### Setting up the EC2 instance
After purchasing the domain from cloudfare, I deployed a t3.micro EC2 instance named "NaseemAWS2" to serve as the remote host for my website. The instance provided me with the IP 13.49.248.203 and I set up an elastic IP to keep the address static preventing it from constantly changing. 


<img width="1899" height="888" alt="image" src="https://github.com/user-attachments/assets/079fcd48-7416-4741-99c3-f3d5fcfbe8d7" />



### Downloading the keyfile and moving it to me local Linux environment. 
Once I set up the domain and EC2 instance, I proceeded to install my AWS key file which downloaded to my Windows folder.  


I named the key file use.pem and moved the file over to my local Linux environment. 


<img width="1262" height="27" alt="image" src="https://github.com/user-attachments/assets/539a12d5-1c34-4e1b-8ffd-d9cd9918adc9" />  




### Establishing a secure remote connection to your Ubuntu 24.04.3 LTS EC2 instance via SSH  



After obtaining the key file and moving it to my Linux directory in the keys folder, I set the permissions for file to chmod 400 making it a readable file for the owner only. I then ran the command:   

ssh -i "use.pem" ubuntu@ec2-13-49-248-203.eu-north-1.compute.amazonaws.com  

It then successfully connected me to the remote AWS environment with the terminal. Using SSH with the use.pem key, I was logged into an Ubuntu 24.04.3 LTS instance. The terminal was then showing that I was operating as the Ubuntu user with the internal IP, 172.31.22.71.  


<img width="1122" height="697" alt="image" src="https://github.com/user-attachments/assets/28a0c994-a060-4264-aa60-ac0dfe6c8c70" />  



### Installing and setting up nginx  

1. First update and refresh your Linux system's local package index that updates the list of avaiable packages and thier versions from repositories. Run the following command in the terminal:
sudo apt update  


2. Install Nginx:
sudo apt install nginx  



3. Start the service:
sudo service nginx start  



### Launching and editing my website
Once the following commands were inputted, I was able to launch my domain by typing naseemnginx.co.uk. But first I wanted to edit it where it included my name on the webpage. I ran the following command in the screenshot below:   



  <img width="445" height="27" alt="image" src="https://github.com/user-attachments/assets/d36b4475-fcc9-4502-b593-e51587ba4b05" />  



I used vim to edit the contexts of the website as you can see on the screenshot below:  

<img width="599" height="580" alt="image" src="https://github.com/user-attachments/assets/50819123-8bc8-42a1-ba3c-7fd085b16b59" />  



## Final output: 
My domain: naseemnginx.co.uk  


<img width="1920" height="1076" alt="image" src="https://github.com/user-attachments/assets/55aa637f-659b-4fa3-8d4b-3dec0503e23a" />





