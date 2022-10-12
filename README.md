# one2onetool

Create a CI/CD pipeline (bash script or any CI/CD tool that you are most comfortable 
with) that monitors the “release” and “staging” branches of the repository. The pipeline 
should be triggered on new commits and perform at least the following: 
1. The pipeline should build and run tests on the application 
2. Containerise and deploy the application on a public cloud instance 
Utilized azure pipeline to build the docker file push to docker hub, and use azure pipeline to create a release to a azure web app. 

3. There are two branches, “staging” and “release”: 

a. The “staging” branch should use “Questions-test.json” as its input data file 
b. The “release” branch should use “Questions.json” as its input data file 
done using sed bash script. 

4. Consider how versioning can be done to differentiate the builds 
Added branch names to docker file tags to differentiate the builds. 

If any of the tasks fails at any point, the pipeline should be stopped and an email alert 
should be sent with relevant information

Email alerts are handled naturally by Azure pipelines. 