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
<i font-weight="smaller">*There are 2 types of sections under Group (Sub-Group & Project).
<br>Sub-Group has 3 dots at the begining, Project does not.</i>

**`Step 3:`**
<br/>
Select the Sub-Group named [your-desired-application] 
<br/>
<code><i>(ex: a Sub-Group [Notepad++])</i></code>

**`Step 4:`**
<br/>
Create Sub-Group named [your-desired-application|your work account name]
<br/>
<code><i>(Click on button <b>New Subgroup</b> on the top right corner, next to button <b>New project</b>)</i></code>
<br/>
<code><i>(ex: Sub-Group [Notepad++|qle2])</i></code>
<br/>
<i>*This Sub-Group is where you gonna store your Application Installer later</i>

### B. Create your own Application Installer from template:

**`Step 1:`**
<br/>
Go back to Sub-Group [your-desired-application]

**`Step 2:`**
<br/>
Select Project [your-desired-application|original]
<br/>
(ex: Project [Notepad++|original])

**`Step 3:`**
<br/>
Click on button <code><i><b>Fork</b> (on the top right corner, on the right of project's name)</i></code>
<br/>
<i>*You will be redirected to the Forking window</i>

**`Step 4:`**
<br/>
Name your project
<br/>
(Porject's name must be in this format [Installer|...], you can put a specific version or date in the blank)
<br/>
(ex: [Installer|ver. 10.0])

**`Step 5:`**
<br/>
Click on<code><i>button <b>Select a namespace</b></i> under the section Project URL.</code>
<br/>
Then select the path to the Sub-Group that you have just created earlier. 

**`Step 6: optional`**
<br/>
Give your project a short description
