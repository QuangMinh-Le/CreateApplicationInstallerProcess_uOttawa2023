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

## **Let's say you want to create an Installer for Office365. Here are how to do it!**

### Step 1. 🧰 Set-up Application Installer (Create your own Application Installer from template)

**`Step 1.1:`**
<br/>
From the Homepage, on the left most navigation column, click on button <code><b>Groups</b></code> (3th button from top).

**`Step 1.2:`**
<br/>
Select Group <code>[SCCM Applications and Scripts]</code>.

**`Step 1.3:`**
<br/>
Select Project <code>[PSAppDeployToolKit]</code>.
<br/>
<sub><i>*Subgroup has 3 dots at the begining, Project does not.</i></sub>

**`Step 1.4:`**
<br/>
Click on button <code><b>Fork</b></code> (on the top right corner, to the right of project's name).
<br/>
<sub><i>*You will be redirected to Forking window.</i></sub>

**`Step 1.5:`**
<br/>
Name your project after Application's name <code>[Office365]</code>.
<br/>
(Sometime, it is necessary to give the app's version, you can name your project with the version - ex: <code>[Office365_2023]</code>).

**`Step 1.6:`**
<br/>
Under the section Project URL, click on button <code><b>Select a namespace</b></code>.
<br/>
Then select the path <code>"sccm-applications-and-scripts/applications"</code>.</i>

**`Step 1.7: (optional)`**
<br/>
Give your project a short description.

**`Step 1.8:`**
<br/>
Select <code><b>Internal</b></code> for Visibility level.
Then, click on <code><b>Fork project</b></code> (your project will now located in group <code>Applications</code>).
<sub><i>*You will be redirected to forked project's window.</i></sub>

### Step 2. 🛠️ Modify the Application Installer:

#### Method 1: Online 🌎

**`Step 2.1:`**
</br>
In your project's window, under button <code><b>Fork</b></code>, click on button <code><b>Web IDE</b></code>
</br>
<sub><i>*You will be redirected to the online IDE.</i></sub>

**`Step 2.2:`**
</br>
Make any modification to the files.

**`Step 2.3: Save the changes`**

***`Step a:`***
</br>
After modification, on the left most navigation column, click on button <code><b>Source Control</b></code>.

***`Step b:`***
</br>
Write a commit message. 
</br>
Then, click on <code><b>Commit & Push</b></code>.
</br>
Then, you will see a pop-up, select <code>No. Use the current branch "main"</code> option.

***`Step c:`***
</br>
All the changes you made is now saved. 
</br>
You can close the online IDE window, and go back to project window.
</br>
<sub><i>*Reload the page to see changes.</i></sub>

#### Method 2: Offline 🏠, locally (Recommended if you are familiar with Git)

**`Step 2.1:`**
<br/>

Follow [Gitlab.uottawa setup instructions](https://www.uottawa.ca/uoweb/en/development/working-with-git).
<br/>
Login here: https://gitlab.uottawa.ca

**`Step 2.2:`**
<br/>
On your local machine, create a folder as the workspace.

**`Step 2.3:`**
<br/>
Go back to your project window, click on <code><b>Clone</b></code>. 
Then, copy the path under <b>Clone with SSH</b>.

**`Step 2.4:`**
<br/>
Open terminal at the folder you have just created.
<br/>
Then type <code>git clone <i>"the copied path"</i></code> in the terminal.

**`Step 2.5:`**
<br/>
The codebase should be downloaded to your local machine. 
<br/>
You can modifying the code with any code editor. 

**`Step 2.6: Save and Commit the change to Gitlab`**

***`Step a:`***
</br>
After modification, you have to firstly save you changes.

***`Step b:`***
</br>
In the terminal at your folder, type <code>git add .</code>. 
</br>
Then, type <code>git commit -m"<i>Give a commit message</i>".</code>. 
</br>
Then, type <code>git push</code>. 

***`Step c:`***
</br>
All the changes you made should be now saved to Gitlab. 
</br>
You can close the IDE, and go back to project window.
</br>
<sub><i>*Reload the page to see changes.</i></sub>


### Step 3. 🛠️ Download Application Installer and Prepare for SCCM:

**`Step 3.1:`**
</br>
In your project's window, to the left of blue button<code><b>Clone</b></code>, click on button <img alt="TypeScript" width="20px" style="padding-right:10px; cursor: none;" src="https://raw.githubusercontent.com/QuangMinh-Le/CreateApplicationInstallerProcess_uOttawa2023/main/download%20(1).svg" /> to download the whole project to your local machine.
</br>

**`Step 3.2:`**
</br>
Rename the file <code>[Deploy-Application.ps1]</code> to <code>[Office365_2023.ps1]</code>. 

**`Step 3.3:`**
</br>
Put the installer to the folder <code>Files</code> and any customized support file in folder <code>SupportFiles</code>. 

**`Step 3.4:`**
</br>
Everything should be ready for deployment on SCCM.



### **Bonus 1.💡 Upon each login recommended process:
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
<sub><i>*You still can review the changes by clicking on button <code><b>Changes</b></code></i></sub>.

***`Step 2.2:`***
Everything is set, you start modifying your Installer.


### **Bonus 2.💡 You forked a project, modify it, and then you want to recommend those changes to the original project. Here is how to do it:

**`Step 1:`**
<br/>
Go to the project that you made changes, on the left most navigation column, click on button <code><b>Merge Request</b></code> (4th button from top).

**`Step 2:`**
<br/>
Click on button <code><b>New merge request</b></code>.
<br/>

**`Step 3:`**
<br/>

Under **Source branch**, click on<code><b>Select source branch</b></code>, then select <code>main</code>.
<br/>

**`Step 4:`**
<br/>

Under **Target branch**, select the path to the original project where you want to contribute your work to, then select <code>main</code>.
<br/>

**`Step 5:`**
<br/>
Click on<code><b>Compare branches and continue</b></code>.
<br/>
<sub><i>*You will be redirected to the marge request window.</sub></i>

**`Step 6:`**
<br/>
Make sure to give a clear tilte and a detailed description for the merge request.
<br/>
Then select admin account as the <b>Reviewer</b>.

**`Step 7:`**
<br/>
Click on<code><b>Create merge request</b></code>.
<br/>
Good job, thank you for your contribution, admin will review you recommendation and choose to accept or not.

