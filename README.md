# jenkins-using-terraform
🚀 Automating Jenkins Setup on AWS using Terraform – My DevOps Project Journey 💻⚙️

Recently, I worked on an exciting DevOps automation project — provisioning a Jenkins server on AWS using Terraform.
This project demonstrates how Infrastructure as Code (IaC) can make setting up CI/CD tools like Jenkins fast, repeatable, and scalable.

Here’s a quick walkthrough 👇

🧩 Project Repository

🔗 GitHub: jenkins-using-terraform

Clone the repository:

git clone https://github.com/vishnunimangare/jenkins-using-terraform.git


Inside the repo, I created:

main.tf → Terraform configuration file defining the AWS infrastructure

outputs.tf → For displaying outputs like the Jenkins URL and instance details

⚙️ Step 1: Install Terraform

I installed Terraform using Chocolatey (Windows package manager):

choco install terraform -y


Verify installation:

terraform --version

🏗️ Step 2: Initialize Terraform

Inside the project folder:

E:\Devops Projects\jenkins-using-terraform> terraform init


This initializes Terraform and downloads necessary AWS provider plugins.

🚀 Step 3: Deploy Jenkins Infrastructure

Run the apply command:

E:\Devops Projects\jenkins-using-terraform> terraform apply


Terraform provisions the EC2 instance and other required resources automatically.

Once deployment completes, copy the Jenkins URL displayed in the output, for example:

http://54.157.49.44:8080

🔐 Step 4: Connect to the Jenkins Server

Use your private key to SSH into the EC2 instance:

ssh -i jenkins.pem ec2-user@54.157.49.44


Then, retrieve the initial Jenkins admin password:

sudo cat /var/lib/jenkins/secrets/initialAdminPassword


Example:

285544740e9c42d3a5b6db5627a45aba

🧠 Step 5: Configure Jenkins

Open the Jenkins URL in your browser

Click “Install suggested plugins”

Create your Jenkins admin user (Username, Password, Full name, Email)

Click “Save and Finish”

🎉 Your Jenkins server is now up and running!

🧹 Step 6: Clean Up

After testing, exit from the EC2 instance and destroy the infrastructure to avoid unnecessary costs:

terraform destroy


This removes all AWS resources created by Terraform automatically.

💡 Key Takeaways

✅ Infrastructure as Code (IaC) ensures repeatability and consistency

⚙️ Jenkins setup can be fully automated using Terraform

💰 Helps manage AWS costs efficiently by destroying resources when not in use

🌟 Tech Stack Used

Terraform 🧱

AWS EC2 ☁️

Jenkins ⚙️

SSH 🔐

Windows PowerShell / VS Code 💻

🔖 Conclusion

This project reinforced the power of Terraform in automating DevOps workflows.
With just a few commands, we can bring up a full CI/CD environment, saving hours of manual setup.

If you’re passionate about automation, give it a try! 💪
👉 GitHub Repository

#DevOps #Terraform #AWS #Jenkins #Automation #InfrastructureAsCode #CloudComputing #CICD #LearningByDoing
