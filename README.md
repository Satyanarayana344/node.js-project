In this automated deployment CI/CD pipeline using github actions what I have learned is :

Step 1:
I created a node.js app on a cloud server EC2 machine in AWS and install all dependies like "npm" install ,git, docker in the machine.
After I created a local git repository in a local machine and created  my directory using mkdir node.jsproject.
And I added the files of what my project needed like node.js,package.json,Dockerfile and write a github actions workflow  in git repo 
Github actions workflow mandatory structure .git/workflows/<project>.yml.
And then local repo push to the github using   " git push -u origin main" command.Successfully all our files in the local repo comes to our github.

Step 2:
In Docker file we use DOCKER_USERNAME and DOCKER_PASSWORD So we need give the Docker Credintials to the github.
In Github Secrets we can add our Docker creditintials for push and deploy the image in a Docker hub.
Github secrets are secured for our sensitive information like PASSWORDS,SERVER_IP,SERVER_KEYS etc.

Step 3:
After giving the credintials in a github secrets we can trigger the pipeline and run the jobs incase issues occured in the workflow.
The workflow automatically shows where the error occured and failed the CI/CD workflow.
After resolving those ERRORS the CI/CD workflow happen with a GREEN TICKMARK .

<img width="1496" height="226" alt="Screenshot 2025-09-24 151426" src="https://github.com/user-attachments/assets/94f6a468-7ef8-4c9b-9c89-0506df73c8d1" />


<img width="1451" height="806" alt="Screenshot 2025-09-24 150452" src="https://github.com/user-attachments/assets/63222f27-b1fa-4f5c-9c71-130974936fcc" />


After Working with this I learn about how github actions work and to how docker is used for push and deploy image.  


