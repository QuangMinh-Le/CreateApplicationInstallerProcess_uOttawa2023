# Process to create an Application Installer Package

---

### ** 📝 Essential terminologies before getting start: **
| Terminology | Definition |
| :---: | --- |
| <b>Group <br> --- <br> Subgroup <br> --- <br> Project</b> |  The relationship between these entities is hierarchical. A **group** can contain multiple subgroups, and each **subgroup** can contain multiple **projects** (similar to repositories in github). |
| **Fork** | <b>Forking</b> is the process of creating a copy of a project under your own account or namespace. It allows you to make changes to the codebase without affecting the original project. Forks are often used for contributing to open-source projects or experimenting with modifications. |
| **Merge** | <b>Merging</b> is the process of combining changes from one project into another. In GitLab, you can merge projects to consolidate code changes. For example, merging a fork project into the original project incorporates the new feature into the original codebase. |
| **Merge Request** |  A <b>merge request</b> (also known as a pull request) is a proposal to merge changes from one project into another. It is a way to review and discuss code changes before they are merged. Merge requests provide a collaborative workflow, allowing team members to review, comment, and suggest modifications. |


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

## ***`Let's say you want to create an Installer for Office365. Here are how to do it!`***

### A. 🧰 Set-up Environment

<br>
**`Step 1:`**
<br/>
From the Homepage, on the left most navigation column, click on button <code><b>Groups</b></code> (3th button from top).

**`Step 2:`**
<br/>
Select Group <code>[SCCM-Applications-Scripts]</code>

**`Step 3:`**
<br/>
Select Subgroup <code>[Applications]</code>
<br/>
<sub><i>Subgroup has 3 dots at the begining, Project does not.</i></sub>

**`Step 4:`**
<br/>
Select the Subgroup named <code>[your-desired-application]</code>
<br/>
<code><i>(ex: Subgroup [Notepad++])</i></code>

**`Step 5:`**
<br/>
Click on button <code><b>New Subgroup</b></code> (on the top right corner, next to button <code><b>New project</b></code>), create Subgroup named <code>[your-desired-application|your work account name]</code>
<br/>
<code><i>(ex: Subgroup [Notepad++|qle2])</i></code>
<br/>
<sub><i>*This Subgroup is where you gonna store your Application Installer later</i></sub>

### B. 🛠️ Create your own Application Installer from template:

**`Step 1:`**
<br/>
Go back to Subgroup <code>[your-desired-application]</code>

**`Step 2:`**
<br/>
Select Project <code>[your-desired-application|original]</code>
<br/>
<code><i>(ex: Project [Notepad++|original])</i></code>

**`Step 3:`**
<br/>
Click on button <code><i><b>Fork</b> (on the top right corner, on the right of project's name)</i></code>
<br/>
<sub><i>*You will be redirected to the Forking window</i></sub>

**`Step 4:`**
<br/>
Name your project (porject's name must be in this format <code>[Installer|...]</code>, you can put a specific version or date in the blank)
<br/>
<code><i>(ex: Project [Installer|ver.10.0])</i></code>

**`Step 5:`**
<br/>
Click on button <code><i><b>Select a namespace</b></i> under the section Project URL.</code>
<br/>
Then select the path to the Subgroup (from the dropdown menu) that you have just created earlier. 
<br/>
<code><i>(ex: Path [sccm-applications-scripts/applications/Notepadd++/Notepadd++|qle2])</i></code>

**`Step 6: (optional)`**
<br/>
Give your project a short description

### C. 🔭 Modify the Application Installer:
