## How To Login To Course-specific Account on ieng6 <br>

**Step 1: Installing VSCode** <br>
---

Go to the Visual Studio Code website https://code.visualstudio.com/, and follow the instructions to download and install it on your computer. VSC supports both MacOS and Windows.<br>
<br>
After installing and launching VSCode, you should be able to open the VSCode application and see a window that looks something like this:<br>
<p align="center">
  <img src="https://user-images.githubusercontent.com/99768694/162289848-79e42961-ef43-4466-b51a-0f35f0fecbe1.png" alt="image" width="600"/>
</p>
Note: Your VSC may look different depending on your operating system, menu bar, system settings, or color scheme.

---

**Step 2: Remotely Connecting** <br>
---

If you are on Windows, you will need to install a program called OpenSSH. OpenSSH will allow your computer to remotely connect to other computers. OpenSSH can be found here:<br>
**[Install OpenSSH](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse)**<br>
<br>
Everyone in CSE 15L has a course-specific account. Your account will have a name similar to **cs15lsp22abc@ieng6.ucsd.edu**. This can be accessed here:<br>
**[CSE 15L Account Lookup](https://sdacs.ucsd.edu/~icc/index.php)**<br>
<br>
Then, by using VSCode's remote option, you will be connecting to a remote computer. Start by opening a new terminal in VSCode, and type the following command with _your_ CSE 15L course-specific account.

```
$ ssh cs15lsp22abc@ien6.ucsd.edu
```
Because this may be the first time thath you have connected to the server, you should see a message in the terminal that looks something like this:

```
The authenticity of host 'ieng6.ucsd.edu (128.54.70.227)' can't be established.
RSA key fingerprint is 
SHA256:ksruYwhnYH+sySHnHAtLUHngrPEyZTDl/1x99wUQcec.

Are you sure you want to continue connecting
(yes/no/[fingerprint])?
```

After inputing `yes` into the terminal, provide your password. Once logged in, you should see a message that looks something like this:

```
Password:

Last login: Sun Jan  2 14:03:05 2022 from 107-217-10-235.lightspeed.sndgca.sbcglobal.net
quota: No filesystem specified.
Hello cs15lsp22zz, you are currently logged into ieng6-203.ucsd.edu

You are using 0% CPU on this system

Cluster Status
Hostname     Time    #Users  Load  Averages
ieng6-201   23:25:01   0  0.08,  0.17,  0.11
ieng6-202   23:25:01   1  0.09,  0.15,  0.11
ieng6-203   23:25:01   1  0.08,  0.15,  0.11

Sun Jan 02, 2022 11:28pm - Prepping cs15lsp22
```
<p align="center">
  <img src="https://user-images.githubusercontent.com/99768694/162544709-2b6ca85d-fc03-4cc2-87ab-bf087908d2d3.png" alt="image" width="600"/>
</p>

---

**Step 3: Trying Some Commands** <br>
---

---

**Step 4: Moving Files with scp** <br>
---

---

**Step 5: Setting an SSH Key** <br>
---

---

**Step 6: Optimizing Remote Running** <br>
---

---
