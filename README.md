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





