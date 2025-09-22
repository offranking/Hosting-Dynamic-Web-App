# Hosting-Dynamic-Web-App
Hosting a Dynamic web-app on AWS with terraform module Docker ECR and ECS

### Login to your Aws console and SSH to your terminal.

<img width="1436" height="813" alt="Screenshot 2025-09-19 at 5 32 21 pm" src="https://github.com/user-attachments/assets/984fdaa4-ad56-4509-994f-982925dc80fe" />

### make a directory and name it mkdir terraform-ecs-webapp
<img width="871" height="97" alt="Screenshot 2025-09-19 at 4 53 34 pm" src="https://github.com/user-attachments/assets/97e0925c-be07-4082-a8ed-e552ab08cbeb" />

### cd terraform-ecs-webapp and creat a directory mkdir -p modules/ecr and mkdir -p modules/ecs
<img width="909" height="100" alt="Screenshot 2025-09-19 at 4 56 51 pm" src="https://github.com/user-attachments/assets/5460e60f-a097-4918-9384-7020514d16be" />

### On this part we need to install docker and before you install we need to update
sudo apt update
sudo apt install -y docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
sudo systemctl start docker
sudo systemctl enable docker

<img width="1300" height="634" alt="Screenshot 2025-09-19 at 4 59 04 pm" src="https://github.com/user-attachments/assets/bf605cad-9b74-490a-aa6d-fe032ceb0e4c" />

### now install docker

<img width="1417" height="449" alt="Screenshot 2025-09-19 at 5 00 59 pm" src="https://github.com/user-attachments/assets/fde622ff-2447-424e-be02-10e59fc5cd0e" />

### after that we need to start the docker and enable docker
<img width="985" height="103" alt="Screenshot 2025-09-19 at 5 02 19 pm" src="https://github.com/user-attachments/assets/ef867f4a-3b0f-4df3-ae04-bd0c8edefa87" />

### Make sure you are inside the folder where you want to create the Dockerfile "vim Dockerfile"

<img width="934" height="110" alt="Screenshot 2025-09-19 at 7 31 19 pm" src="https://github.com/user-attachments/assets/9bb01d28-7cad-41aa-852a-cc66b4a3b3e8" />

### Open in the file and past in your code 
<img width="1436" height="899" alt="Screenshot 2025-09-19 at 5 14 24 pm" src="https://github.com/user-attachments/assets/091e302f-d51c-48e1-a612-2ebe0b173353" />

### builds a Docker image from the Dockerfile in your current directory and names it my-node-app sudo docker run -p 3000:3000 my-node-app

<img width="934" height="400" alt="Screenshot 2025-09-19 at 5 18 45 pm" src="https://github.com/user-attachments/assets/356ed34d-0235-44bf-9b25-3d28a4e8e3bd" />

### To continue with your application setup, you need to install npm, which comes bundled with Node.js
sudo apt update
sudo apt install -y nodejs npm
sudo apt install -y nodejs npm
npm -v

<img width="893" height="466" alt="Screenshot 2025-09-19 at 5 29 58 pm" src="https://github.com/user-attachments/assets/d242f0ca-6371-4af6-9884-6fb82089ff79" />

###Now node -v

### We have our NPM running 

<img width="910" height="566" alt="Screenshot 2025-09-20 at 10 16 03 pm" src="https://github.com/user-attachments/assets/34cbf242-e540-475f-97d4-90797b342450" />

### Sudo systemctl start docker systemctl is the command used to manage system services on Linux systems that use systemd (like Ubuntu, Debian, CentOS, Fedora).
It allows you to start, stop, restart, enable, disable, and check the status of services.

<img width="1002" height="242" alt="Screenshot 2025-09-20 at 9 47 58 pm" src="https://github.com/user-attachments/assets/0136be82-1bf5-42ab-9edb-1bddcd4c6238" />

### Process of Running docker ps -a

<img width="1354" height="178" alt="Screenshot 2025-09-20 at 9 48 45 pm" src="https://github.com/user-attachments/assets/32c5f4b3-a2d3-4ac5-867e-7e9aa1c7400e" />


### Once you make sure your docker is running then you can run this http://34.228.62.57:3000

<img width="1416" height="569" alt="Screenshot 2025-09-20 at 10 14 07 pm" src="https://github.com/user-attachments/assets/5a462d86-33f6-4563-ad4d-cbdbb89a9c50" />

### Now we need to cd in to the module/ecr/main.tf


<img width="1128" height="85" alt="Screenshot 2025-09-20 at 10 06 04 pm" src="https://github.com/user-attachments/assets/48968ce6-6402-441f-b0ab-fd79e8a1fb82" />

### open the file in there which is main.tf

<img width="1262" height="787" alt="Screenshot 2025-09-20 at 10 10 29 pm" src="https://github.com/user-attachments/assets/6bdced2f-e0b6-4c4c-85d8-f3c2bf08d69a" />

### do the same module/ecs/main.tf

<img width="1128" height="85" alt="Screenshot 2025-09-20 at 10 06 04 pm" src="https://github.com/user-attachments/assets/41807f21-fec2-424b-ace3-f4ea877701a5" />

## Open the main.tf

<img width="1262" height="900" alt="Screenshot 2025-09-20 at 10 12 26 pm" src="https://github.com/user-attachments/assets/7a1946d2-0cb5-4dfc-8605-466afdae4bb2" />


### Terraform is an Infrastructure as Code (IaC) tool that allows you to:
Automate the creation and management of cloud infrastructure (AWS, Azure, GCP, etc.).
Keep infrastructure consistent and repeatable using configuration files (like main.tf).
Manage infrastructure lifecycle — create, update, and destroy resources safely.
Share infrastructure setups with your team by simply sharing .tf files.
Now we have to install terraform. to do this we need to update 
### sudo apt update 

<img width="1153" height="497" alt="Screenshot 2025-09-22 at 5 48 08 pm" src="https://github.com/user-attachments/assets/fd743b86-92fc-4e8a-90ef-642c4321149a" />


<img width="1008" height="344" alt="Screenshot 2025-09-22 at 5 48 40 pm" src="https://github.com/user-attachments/assets/ac4c5101-f72a-4072-a6d6-39cbf039a5d6" />

### we need to run the command sudo apt install -y gnupg software-properties-common curl
<img width="1255" height="157" alt="Screenshot 2025-09-22 at 5 49 12 pm" src="https://github.com/user-attachments/assets/eb5d2937-147a-4ea7-9598-707235b01ff7" />

we need to add the repository name sudo apt-add-repository "deb [arch=amd64] https://apt.releases.hashicorp.com $(lsb_release -cs) main"

<img width="1392" height="383" alt="Screenshot 2025-09-22 at 5 52 46 pm" src="https://github.com/user-attachments/assets/3e9f701f-920b-4fa8-bf2d-6ac1b26afe08" />

### Sudo apt update
<img width="1439" height="248" alt="Screenshot 2025-09-22 at 5 53 29 pm" src="https://github.com/user-attachments/assets/a56b665c-83ca-4816-a10b-b76a2f29bd36" />

### the last command will install the terraform
"sudo apt install terraform -y"


<img width="905" height="120" alt="Screenshot 2025-09-22 at 5 54 03 pm" src="https://github.com/user-attachments/assets/583e5b8a-a6c7-4664-976d-06f76be309af" />


### terraform -version to get check 

<img width="686" height="61" alt="Screenshot 2025-09-22 at 5 54 38 pm" src="https://github.com/user-attachments/assets/3a47084d-f2a0-4ea0-b08e-4e1578b8cccf" />

### now we need to install the "AWS CLI"


### run this comman curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"

<img width="1353" height="74" alt="Screenshot 2025-09-22 at 6 00 27 pm" src="https://github.com/user-attachments/assets/1f8bbc81-fd18-406b-9dc6-d022c9aec99c" />

### after installing the "AWS CLI" we need to run "terraform init"

<img width="927" height="426" alt="Screenshot 2025-09-22 at 5 55 45 pm" src="https://github.com/user-attachments/assets/0c4ac2f6-17c8-4188-9f41-14723d34fe2f" />

### The next step is to run Terraform’s validation command to make sure your configuration files are written correctly

<img width="1280" height="67" alt="Screenshot 2025-09-22 at 8 50 14 pm" src="https://github.com/user-attachments/assets/e85a6a84-fd38-411d-b47f-dc3be925a3ba" />


### After validating the configuration, the next step is to generate an execution plan with Terraform. This allows you to preview the infrastructure changes before applying them.
"terraform plan"

<img width="1262" height="900" alt="Screenshot 2025-09-22 at 6 02 00 pm" src="https://github.com/user-attachments/assets/44a3c5f6-6c65-4c8c-bd6b-2675521c9a53" />

run terraform apply and type "yes"
<img width="1262" height="861" alt="Screenshot 2025-09-22 at 6 02 40 pm" src="https://github.com/user-attachments/assets/3a9f5383-ec9d-4c4c-a42d-5bf69a3cb9cf" />

### Wait for provisioning:

Terraform will provision the resources in your cloud provider (e.g., AWS).

When complete, it will display important outputs, such as the public IP address of your EC2 instance or other resource details.

<img width="1381" height="757" alt="Screenshot 2025-09-22 at 6 07 37 pm" src="https://github.com/user-attachments/assets/eb2c731a-6de4-4c92-aa30-bbca7a148c12" />

### Now we have to check the public ip on the broser IP: http://107.23.163.173/

<img width="1262" height="812" alt="Screenshot 2025-09-22 at 4 41 05 pm" src="https://github.com/user-attachments/assets/6911dd62-88af-4f5f-90a4-53c2d165dbf9" />





