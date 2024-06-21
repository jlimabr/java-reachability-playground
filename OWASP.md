Homework:

Very Important: Debug Issues with OWASP ZAP scan
GitHub Actions have introduced some recent changes because of which, OWASP ZAP scan is failing in public and private repos.

----------------------1st issue that users faced while integrating DAST scan-------------------------
Error: Validation Failed: {"message":"The listed users and repositories cannot be searched either because the resources do not exist or you do not have permission to view them.","resource":"Search","field":"q","code":"invalid"}

Then follow the following steps for fixing this error:
1) Go to Settings of the repo
2) Click on Actions drop down on the left hand side of the web page
3) From the Actions drop down, Click on General
4) Scroll down, Under Workflow Permissions, see the permission
5) Make sure to Select Read and write permissions

6) Click on Save button to save your changes

Rerun ZAP scan and this will fix your error. Thanks!!

--------------------------2nd Issue that users faced while integrating ZAP scan-----------------
                                 The process '/usr/bin/git' failed with exit code 1


Solution:
Make sure that your Github repo branch name is matching with the branch name defined in actions yml file.
For example:
      If your Github repo's branch name is master:

     Then ensure that your owasp-zap-scan.yml file is referring to master branch as well:


--------------------------3rd Issue that users faced while integrating ZAP scan-----------------
            Issues are disabled for this repo


Solution:
Ensure that you have not cloned your repo in Github. Instead, create a new empty Github repo, then push your code along with actions file in Github repo and then run DAST scan and it will fix this error.

Please ask Questions via Q&A section if you still face any issue. We will review the error in your repo to fix the issue.
