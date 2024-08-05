<b>Automated Deployment on EC2 Machines using Ansible and Jenkins</b></n>
This project automates the entire deployment process on EC2 machines using an Ansible playbook executed by Jenkins. The automation includes the creation of an AMI and the updating of the launch template within an Auto Scaling group.

Overview
Auto Scaling Group Management: Automatically manages EC2 instances within an Auto Scaling group.
AMI Creation: Creates an AMI from an on-demand instance within the Auto Scaling group.
Launch Template Update: Updates the launch template with new AMI, spot instance configuration, security group, subnets, and other necessary settings.
Jenkins Integration: Uses Jenkins to run the Ansible playbook for end-to-end automation.
Workflow
AMI Creation:

An Ansible playbook creates an AMI from an existing on-demand instance within the Auto Scaling group.
Launch Template Update:

The playbook updates the launch template with the newly created AMI.
Configures the launch template to use spot instances.
Updates security groups, subnets, and other configurations as needed.
Auto Scaling Group Update:

The updated launch template is applied to the Auto Scaling group to ensure new instances are launched with the updated configuration.
Prerequisites
Ansible: Ensure Ansible is installed and configured.
Jenkins: A running Jenkins instance with the necessary permissions and plugins.
AWS CLI: Configure AWS CLI with appropriate access credentials.
Git: For version control and repository management.
Setup Instructions
Clone the Repository:

bash
Copy code
git clone <repository_url>
cd <repository_directory>
Configure Ansible:

Update the Ansible playbook with your specific configurations (e.g., instance IDs, security group IDs, subnet IDs).
Jenkins Job Configuration:

Create a Jenkins job to execute the Ansible playbook.
Set up the job to trigger automatically based on your deployment schedule or other criteria.
Run the Job:

Trigger the Jenkins job to start the automation process.
Monitor the Jenkins job console for progress and completion.
Benefits
Automation: Eliminates manual intervention in the deployment process.
Consistency: Ensures consistent configuration across all instances.
Efficiency: Reduces time and effort required for AMI creation and launch template updates.
Scalability: Easily scales to accommodate changes in your Auto Scaling group configuration.
Contribution
Feel free to contribute by opening issues or submitting pull requests. Ensure your contributions align with the project’s goals and coding standards.

By following these instructions and using the provided Ansible playbook and Jenkins configuration, you can automate the deployment process for EC2 instances within your Auto Scaling groups, ensuring efficiency and consistency.
