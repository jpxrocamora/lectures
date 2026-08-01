**Commands:**



**git init** 

**git add .** 

**git commit -m "comment"**

**git clone <repo url>**

**git pull**

**git checkout <commit hashed-key>**

**git branch -d <name of the branch>**

**git switch -c <branchName>**





**git push origin main** 

&#x09;**this command would push the changes on the main (not the usual git push)**



**FETCH - Good practice, check first if there are changes on the repo**

**THESE 2 commands are use to check if there are changes made on the repo by other teammate**

&#x09;**git fetch origin**

&#x09;**get status**

**OR THESE**

&#x09;**git fetch origin**

&#x09;**git diff main origin/main**

**IF there are changes then run the command** 

&#x09;**git pull**





**Scenario: For instance you wanna use a different GitHub account but your terminal requires you to global config. Now, instead of doing it, you may fallow these steps**

**1. Click your GitHub profile icon on the upper right corner and look for settings**

**2. On the left sidebar menu, look for "Developer settings" which is located at the bottom part of the list**

**3. Choose the "Personal Access Tokens" and choose the Tokens(classic) and name your API and generate the token**

**4. on your initialized (or cloned) project type this: git remote set-url origin https://USERNAME:TOKEN@github.com/USERNAME/REPOSITORY.git** 

&#x09;**Note: replace the username and token.**





**NOTE: the "main" branch is the stable collective codes pushed by all the team members. It is a best practice not to work on main but create a local branch on your local device.** 



**Team GitHub Workflow**

**1. Clone the repository (maybe created by the programmer or project manager. Each team member clones the repository only once.)**

&#x09;**git clone https://github.com/company/project.git**

&#x09;**cd project**

**2. Update the main branch. Before starting work, get the latest changes.**

&#x09;**git checkout main**

&#x09;**git pull origin main**

&#x09;



**3. Create your own branch. Never work directly on main. For example, if you are implementing the login page:**

&#x09;**git checkout -b feature/login or git checkout -b feature-login (depends on the naming convention of the team**

&#x09;**git checkout -b feature-registration**



&#x09;**git checkout -b feature-dashboard**

&#x09;

&#x09;**git checkout -b fix-navbar**



&#x09;**NOTE THAT THE ABOVE ARE THE OLD WAYS OF SWITCHING TO THE CREATED BRANCH, BELOW IS THE NEW ONE:**



&#x09;**git switch -c feature/login**







**4. Step 4: Write your code. Modify files. For example:**



&#x09;**login.js**

&#x20;   	**dashboard.js**

&#x20;   	**navbar.js**

&#x09;**These might be created in different branches like git checkout -b feature/login**



**5. Commit your changes**

&#x09;**git add .**



&#x09;**git commit -m "Add login functionality"**



**6. Push your branch**

&#x09;**git push origin feature-login**



**7. Open a pull request on GitHub:**

&#x09;**example output:**



&#x09;**Enumerating objects: 12, done.**

&#x09;**Counting objects: 100% (12/12), done.**



&#x09;**To github.com/company/project.git**



&#x09;**\* \[new branch]      feature-login -> feature-login**



**8. The user who would make a PR must go to GitHub**



&#x09;**https://github.com/company/project**

&#x09;

&#x09;**see the button**



&#x09;**feature-login had recent pushes.**



&#x09;**\[Compare \& pull request]**

**9 fills in the pull request**



&#x09;**Base branch:**

&#x09;	**main**

&#x09;**Compare branch:**

&#x09;	**feature-login**

**10. Add title**

&#x09;	**Add login functionality**

&#x09;**Add description**

&#x09;	**added login page**

**11. Hit the Create pull request button**



**12. The repository owner reviews the pull request**

&#x09;**You can review the code, leave comments, and click "Merge pull request"**



&#x09;**GitHub merges: feature-login -> main**



**13. Team members update their local repository**

&#x09;**After the pull request is merged:**

&#x09;**git checkout main**



&#x09;**git pull origin main**



**14. If the branch is no longer needed, you can delete it:**

&#x09;**git branch -d feature-login**

&#x09;**And remove the remote branch:**

&#x09;**git push origin --delete feature-login**



