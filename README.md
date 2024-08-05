<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Automated Deployment on EC2 Machines using Ansible and Jenkins</title>
</head>
<body>
  <h1>Automated Deployment on EC2 Machines using Ansible and Jenkins</h1>
  <p>This project automates the entire deployment process on EC2 machines using an Ansible playbook executed by Jenkins. The automation includes the creation of an AMI and the updating of the launch template within an Auto Scaling group.</p>

  <h2>Overview</h2>
  <ul>
    <li><strong>Auto Scaling Group Management</strong>: Automatically manages EC2 instances within an Auto Scaling group.</li>
    <li><strong>AMI Creation</strong>: Creates an AMI from an on-demand instance within the Auto Scaling group.</li>
    <li><strong>Launch Template Update</strong>: Updates the launch template with new AMI, spot instance configuration, security group, subnets, and other necessary settings.</li>
    <li><strong>Jenkins Integration</strong>: Uses Jenkins to run the Ansible playbook for end-to-end automation.</li>
  </ul>

  <h2>Workflow</h2>
  <ol>
    <li><strong>AMI Creation</strong>: An Ansible playbook creates an AMI from an existing on-demand instance within the Auto Scaling group.</li>
    <li><strong>Launch Template Update</strong>:
      <ul>
        <li>The playbook updates the launch template with the newly created AMI.</li>
        <li>Configures the launch template to use spot instances.</li>
        <li>Updates security groups, subnets, and other configurations as needed.</li>
      </ul>
    </li>
    <li><strong>Auto Scaling Group Update</strong>: The updated launch template is applied to the Auto Scaling group to ensure new instances are launched with the updated configuration.</li>
  </ol>

  <h2>Prerequisites</h2>
  <ul>
    <li><strong>Ansible</strong>: Ensure Ansible is installed and configured.</li>
    <li><strong>Jenkins</strong>: A running Jenkins instance with the necessary permissions and plugins.</li>
    <li><strong>AWS CLI</strong>: Configure AWS CLI with appropriate access credentials.</li>
    <li><strong>Git</strong>: For version control and repository management.</li>
  </ul>

  <h2>Setup Instructions</h2>
  <ol>
    <li><strong>Clone the Repository</strong>:
      <pre><code>git clone &lt;repository_url&gt;
cd &lt;repository_directory&gt;</code></pre>
    </li>
    <li><strong>Configure Ansible</strong>: Update the Ansible playbook with your specific configurations (e.g., instance IDs, security group IDs, subnet IDs).</li>
    <li><strong>Jenkins Job Configuration</strong>: 
      <ul>
        <li>Create a Jenkins job to execute the Ansible playbook.</li>
        <li>Set up the job to trigger automatically based on your deployment schedule or other criteria.</li>
      </ul>
    </li>
    <li><strong>Run the Job</strong>: 
      <ul>
        <li>Trigger the Jenkins job to start the automation process.</li>
        <li>Monitor the Jenkins job console for progress and completion.</li>
      </ul>
    </li>
  </ol>

  <h2>Benefits</h2>
  <ul>
    <li><strong>Automation</strong>: Eliminates manual intervention in the deployment process.</li>
    <li><strong>Consistency</strong>: Ensures consistent configuration across all instances.</li>
    <li><strong>Efficiency</strong>: Reduces time and effort required for AMI creation and launch template updates.</li>
    <li><strong>Scalability</strong>: Easily scales to accommodate changes in your Auto Scaling group configuration.</li>
  </ul>

  <h2>Contribution</h2>
  <p>Feel free to contribute by opening issues or submitting pull requests. Ensure your contributions align with the project’s goals and coding standards.</p>
</body>
</html>
