# Deployment Tools

## Overview
In Progress

## Build Properties
| Parameter                  | Description                                                                                                                                                 | 
|----------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------| 
| sf.username.src (Required) | Username of source Salesforce org                                                                                                                           | 
| sf.password.src (Required) | Password of source Salesforce org                                                                                                                           | 
| sf.token.src (Required)    | Security token of source Salesforce org                                                                                                                     | 
| sf.username.merge          | Username of Salesforce org you are merging with. Only necessary when merging source from multiple orgs                                                      | 
| sf.password.merge          | Password of Salesforce org you are merging with. Only necessary when merging source from multiple orgs                                                      | 
| sf.token.merge             | Security token of Salesforce org you are merging with. Only necessary when merging source from multiple orgs                                                | 
| sf.username.tgt (Required) | Username of target Salesforce org                                                                                                                           | 
| sf.password.tgt (Required) | Password of target Salesforce org                                                                                                                           | 
| sf.token.tgt (Required)    | Security token of target Salesforce org                                                                                                                     | 
| sf.server.src (Required)   | Server URL of source org                                                                                                                                    | 
| sf.server.tgt (Required)   | Server URL of target org                                                                                                                                    | 
| sf.server.merge            | Server URL of merge org. Only necessary when merging source from multiple orgs                                                                              | 
| sf.poll.wait               | Specify (in milliseconds) the amount of time to wait between polls on Salesforce deployments. Increase this value on long-running deployments that time out | 
| sf.test.level (Required)   | Specify test level. See the build.properties for test level options                                                                                         | 
| git.username               | Username for your git repository                                                                                                                            | 
| git.password               | Password for your git repository                                                                                                                            | 
| git.name                   | Your name                                                                                                                                                   | 
| git.email                  | Your email                                                                                                                                                  | 
| git.endpoint               | Https endpoint for your git repository                                                                                                                      | 
| git.branch                 | Git branch to interact with (generally origin/[branch])                                                                                                     | 
| git.srcdir                 | Specify the src directory file path relative to your project (generally just “src”)                                                                         | 

## Retrieve Targets
| Target              | Purpose                                                                                                                                                                                          | 
|---------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| 
| retrieve-git-source | Retrieves all of the git source for the branch specified in the build.properties file                                                                                                            | 
| retrieve-src-all    | Retrieve all metadata stored in the “fullPackage.xml” file located in packages folder. Populate this with a package of all of your metadata, and use it to pull down complete images of your org | 
| retrieve-src        | Retrieve all of the source in the package.xml in the src directory from your Salesforce org                                                                                                      | 

## Deploy Targets
| Target                | Purpose                                                                                        | 
|-----------------------|:-----------------------------------------------------------------------------------------------| 
| validate-git-source   | Retrieve source from the specified branch and validate it to your target org                   | 
| validate-cmp-source   | Retrieve source from source org and validate it to your target org directly                    | 
| validate-local-source | Validate the source in your local directory as it stands in the package.xml to your target org | 
| deploy-git-source     | Retrieve source from the specified branch and deploy it to your target org                     | 
| deploy-cmp-source     | Retrieve source from source org and deploy it to your target org directly                      | 
| deploy-local-source   | Deploy the source in your local directory as it stands in the package.xml to your target org   | 


