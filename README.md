# Postman API Automation Itegration with Github Actions #
This repository is a demonstartion for POC for itegarting Postman tests with github actions. The tests are written in postman and they are executed on the VM with the help of newman and newman-reporter-hrmlextra.
Github actions will trigger the project on every push of main branch. You can also execute the project manually using Workflow_dispatch. The project run on a scheduled time with the help of cron job.
The HTML report is archeived and kept in artifact section for team to download it. Along with that they can view report directly from github pages https://abhijitnaik05.github.io/Phoenix-Inwarrenty-Flow/
The latest report is mailed to team members using Gmail SMTP.

## Testing Coverage ##
1. Happy flow testing
2. Negative testing and edge case testing
3. Token testing
4. Data driven testing with csv
5. Schema validation
6. Scerets management with github scerets 

## Tech Stack ##
1. Postman
2. Node js 22v
3. Newmana
4. Newman-reporter-htmlextra
5. Githun Actions
6. Gmail SMTP
7. Github Pages
8. CSV for data driven testing
9. AWS-EC2 instance for self hosted github runner

## Github Pages ##
You can directly view latest test report of the postman test at the Github pages link : https://abhijitnaik05.github.io/Phoenix-Inwarrenty-Flow/
## HTML Report ##
The HTML report will be created in newman folder 

![Postman Report](https://github.com/AbhijitNaik05/Phoenix-Inwarrenty-Flow/blob/Static_Content/Newman%20report.png)
## Project Structure ##

```
Phoenix  Inwarrenty Flow collection
├─ Inwarranty-flow  collection.postman_collection.json  # collection file
├─ QA.postman_environment.json   # Enviorment file 
└─ testdata.csv  # test data file

```

## How to run the project? ##
You can run the project on local system for that :
1. Clone the the project on local system : https://github.com/AbhijitNaik05/Phoenix-Inwarrenty-Flow.git
2. Install Node js and NPM from https://nodejs.org/en
3. Install Newman using ``` npm install -g newman ```
4. Install Newman-reporter-htmlextra using ``` npm install -g newman-reporter-htmlextra ```
5. Run the newman command 

         ```  newman run 'Inwarranty-flow  collection.postman_collection.json' \
               -e QA.postman_environment.json \
               -d testdata.csv \
               -r cli,htmlextra \
               --reporter-htmlextra-export ./newman/index.html
         ```




