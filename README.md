# Process to create an Application Installer Package

---
### A. Set-up Environment

**`Step 1:`**
<br/>
Go to Group <code>[SCCM-Applications-Scripts]</code>

**`Step 2:`**
<br/>
Go to Sub-Group <code>[Applications]</code>
<br/>
<sub><i>*There are 2 types of sections under Group (Sub-Group & Project).
<br>Sub-Group has 3 dots at the begining, Project does not.</i></sub>

**`Step 3:`**
<br/>
Select the Sub-Group named <code>[your-desired-application]</code>
<br/>
<code><i>(ex: a Sub-Group [Notepad++])</i></code>

**`Step 4:`**
<br/>
Create Sub-Group named <code>[your-desired-application|your work account name]</code>
<br/>
<code><i>(ex: Sub-Group [Notepad++|qle2])</i></code>
<br/>
<code><i>(Click on button <b>New Subgroup</b> on the top right corner, next to button <b>New project</b>)</i></code>
<br/>
<sub><i>*This Sub-Group is where you gonna store your Application Installer later</i></sub>

### B. Create your own Application Installer from template:

**`Step 1:`**
<br/>
Go back to Sub-Group <code>[your-desired-application]</code>

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
Then select the path to the Sub-Group (from the dropdown menu) that you have just created earlier. 
<code><i>(ex: Path [sccm-applications-scripts/applications/Notepadd++/Notepadd++|qle2])</i></code>

**`Step 6: optional`**
<br/>
Give your project a short description

### C. Modify the Application Installer:
