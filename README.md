# Process to create an Application Installer Package

---

### ** 📝 Essential terminologies before getting start: **
| Terminology | Definition |
| :---: | --- |
| <b>Group <br> --- <br> Subgroup <br> --- <br> Project</b> | The relationship between these entities is hierarchical. A **project** (similar to repositories in GitHub) represents an individual repository within a **subgroup**, and each **subgroup** can contain multiple projects. Furthermore, a **subgroup** can be a part of a larger **group**, which can also contain multiple subgroups. |
| **Branch** | **Branch** is a separate line of development within a project. Branches are typically used for parallel development, where different features, bug fixes, or experiments can be worked on simultaneously without affecting the main codebase. Each branch contains its own set of commits, which are changes made to the code. |
| **Fork** | **Forking** is the process of creating a copy of a project under your own account or namespace. It allows you to make changes to the codebase without affecting the original project. Forks are often used for contributing to open-source projects or experimenting with modifications. |
| **Merge** | **Merging** is the process of combining changes from one project into another. In GitLab, you can merge projects to consolidate code changes. For example, merging a fork project into the original project incorporates the new feature into the original codebase. |
| **Merge Request** |  A **merge request** (also known as a pull request) is a proposal to merge changes from one project into another. It is a way to review and discuss code changes before they are merged. Merge requests provide a collaborative workflow, allowing team members to review, comment, and suggest modifications. |
| ***Merge Request*** *from parent project to forked project* |  Admin who own the parent project can make changes to the project. Then, they create **merge requests** to all the forks of that project to keep all the forks updated with the new changes. |
| ***Merge Request*** *from forked project to parent project* |  User who own the forked project can make changes to the project. If they want to contribute their work to the parent project, they need to create a **merge request** to the parent project. The admin will then review and decide to accept the changes or not. |


### 0. 💡 Pre-setup Environment: Check if there is any merge request from admin (Optional)
<sub><i>*These steps are only for comeback user who want to modify or update their existed Application Installer</i></sub>

**`Step 1:`**
<br/>
On the left most navigation column, click on button <code><b>Merge Request</b></code> (4th button from top).

**`Step 2:`**
<br/>
If there is not any merge request, you are good to go. You can skip the steps below and start modifying your Installer.
<br/>
If there is a merge request, follow these steps below:
<br/>

***`Step 2.1:`***
<br/>
If there is a conflict, you can click on button <code><b>Changes</b></code>(the right most button under the title of the merge request) to review the changes from the merge request and resolve it. 
<br/>
If there is no conflict ("Ready to merge!"), you can click on the button <code><b>Merge</b></code> to accept the merge request.
<br/> 
<sub><i>*You still can review the changes by clicking on button <code><b>Changes</b></code></i></sub>

***`Step 2.2:`***
Everything is set, you start modifying your Installer

## **Let's say you want to create an Installer for Office365. Here are how to do it!**

### A. 🧰 Set-up Environment

**`Step 1:`**
<br/>
From the Homepage, on the left most navigation column, click on button <code><b>Groups</b></code> (3th button from top).

**`Step 2:`**
<br/>
Select Group <code>[SCCM-Applications-Scripts]</code>.

**`Step 3:`**
<br/>
Select Subgroup <code>[Applications]</code>.
<br/>
<sub><i>Subgroup has 3 dots at the begining, Project does not.</i></sub>

**`Step 4:`**
<br/>
Select the Subgroup named <code>[Office365]</code>.
<br/>

**`Step 5:`**
<br/>
Click on button <code><b>New subgroup</b></code> (on the top right corner, next to button <code><b>New project</b></code>), create Subgroup named <code>[Office365|qle2]</code>.
<br/>
<i>Add work account at the end.</i>
<br/>
<sub><i>*This Subgroup is where you gonna store your Application Installer later.</i></sub>

### B. 🛠️ Create your own Application Installer from template:

**`Step 1:`**
<br/>
Go back to Subgroup <code>[Office365]</code>.

**`Step 2:`**
<br/>
Select Project <code>[Office365_original]</code>.
<br/>

**`Step 3:`**
<br/>
Click on button <code><b>Fork</b></code> (on the top right corner, on the right of project's name).
<br/>
<sub><i>*You will be redirected to the Forking window.</i></sub>

**`Step 4:`**
<br/>
Name your project.
<br/>
(Project's name must be in this format <code>[Installer_...]</code>, you can put a specific version or date in the blank).
<br/>
<code><i>(ex: Project [Installer_v10.0]).</i></code>

**`Step 5:`**
<br/>
Under the section Project URL, click on button <code><b>Select a namespace</b></code>.
<br/>
Then select the path to the Subgroup (from the dropdown menu) that you have just created earlier. 
<br/>
<i>(ex: Path <code>[sccm-applications-scripts/applications/Office365/Office365_qle2])</code>.</i>

**`Step 6: (optional)`**
<br/>
Give your project a short description.

### C. 🔭 Modify the Application Installer:

#### Method 1: Online 🌎

**`Step 1:`**
</br>
Go to the project where you have just forked from the template.
</br>
<i>(ex: <code>[SCCM-Applications-Scripts/Applications/Office365/Office365_qle2/Installer_v10.0]</code>)</i>

**`Step 2:`**
</br>
Under button <code><b>Fork</b></code>, click on button <code><b>Web IDE</b></code>
<sub><i>*You will be redirected to the online IDE.</i></sub>

**`Step 3:`**
</br>
Make any modification to the files.

**`Step 4: Save the changes`**

***`Step 4.1:`***
</br>
After modification, on the left most navigation column, click on button <code><b>Source Control</b></code>.

***`Step 4.2:`***
</br>
Write a commit message. 
</br>
Then, click on <code><b>Commit & Push</b></code>.
</br>
Then, you will see a pop-up, select <code>No. Use the current branch "main"</code> option.

***`Step 4.3:`***
</br>
All the changes you made is now saved. 
</br>
You can close the online IDE window, and go back to project window.
</br>
<sub><i>*Reload the page to see changes.</i></sub>

#### Method 2: Offline, locally (Recommended if you are familiar with Git)🏠

**`Step 1:`**
Follow [Gitlab.uottawa setup instructions](https://www.uottawa.ca/uoweb/en/development/working-with-git).
<br/>
Login here: https://gitlab.uottawa.ca

**`Step 2:`**
<br/>
On your local machine, create a folder as the workspace.

**`Step 3:`**
<br/>
Go back to your project window, click on <code><b>Clone</b></code>. 
Then, copy the path under <b>Clone with SSH</b>.

**`Step 4:`**
<br/>
Open terminal at the folder you have just created.
<br/>
Then type <code>git clone <i>"the copied path"</i></code> in the terminal.

**`Step 5:`**
<br/>
The codebase should be downloaded to your local machine. 
<br/>
You can modifying the code with any code editor. 

**`Step 6: Save and Commit the change to Gitlab`**

***`Step 6.1:`***
</br>
After modification, you have to firstly save you changes.

***`Step 6.2:`***
</br>
In the terminal at your folder, type <code>git add .</code>. 
</br>
Then, type <code>git commit -m"<i>Give a commit message</i>".</code>. 
</br>
Then, type <code>git push</code>. 

***`Step 4.3:`***
</br>
All the changes you made should be now saved to Gitlab. 
</br>
You can close the IDE, and go back to project window.
</br>
<sub><i>*Reload the page to see changes.</i></sub>

