## How To Login To Course-specific Account on ieng6 <br>

**Step 1: Installing VSCode** <br>
---

Go to the Visual Studio Code website https://code.visualstudio.com/, and follow the instructions to download and install it on your computer. VSC supports both MacOS and Windows.<br>
<br>
After installing and launching VSCode, you should be able to open the VSCode application and see a window that looks something like this:<br>
<p align="center">
  <img src="https://user-images.githubusercontent.com/99768694/162289848-79e42961-ef43-4466-b51a-0f35f0fecbe1.png" alt="image" width="800"/>
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
  <img src="https://user-images.githubusercontent.com/99768694/162544709-2b6ca85d-fc03-4cc2-87ab-bf087908d2d3.png" alt="image" width="800"/>
</p>

Now your terminal is successfully connected to a computer in the CSE basement, and any commands that you input will run on that computer.<br>
<br>

To log out of the remote server in your terminal, you can use the shortcut `ctrl + D` or run the command `exit`.

---

**Step 3: Trying Some Commands** <br>
---

Let's try running some commands. Below are a few commands that you can try.<br>
<br>

Print working directory:

```
$ pwd
```
List Files: (ls[options][names], e.g., ls -l, ls -a, ls -lat)

```
$ ls
```
Copy:

```
$ cp
```
Move or rename:

```
$ mv
```
Change directory:

```
$ cd
```
Make directory:

```
$ mkdir
```
Remove:

```
$ rm
```
Create or view a file:

```
$ cat
```

Create a file:

```
$ touch
```

Display command manual:

```
$ man
```

Here is an example of what your terminal may look like after running some basic commands:
<p align="center">
  <img src="https://user-images.githubusercontent.com/99768694/162545395-6c49dfe7-0ac7-4aed-8da5-66df1fb8e5af.png" alt="image" width="800"/>
</p>
---

**Step 4: Moving Files with scp** <br>
---
Now let's try moving files from your computer to the remote computer. The command `scp`, is used to do just that. This works as following:
```
$ scp filename.txt cs15lsp22abc@ieng6.ucsd.edu:~/
```
Like `ssh`, you will be prompted for your password.<br>
<br>
Now, the file is on the computer in the CSE basement.<br>
<br>
Here is an example of what a successful scp should look like:
<p align="center">
  <img src="https://user-images.githubusercontent.com/99768694/162545917-89aa9946-9107-499a-8635-d221c3c2e067.png" alt="image" width="800"/>
</p>


---

**Step 5: Setting an SSH Key** <br>
---

```
Generating public/private rsa key pair.
Enter file in which to save the key (/Users/vivek/.ssh/id_rsa): 
Enter passphrase (empty for no passphrase): 
Enter same passphrase again: 
Your identification has been saved in /Users/vivek/.ssh/id_rsa.
Your public key has been saved in /Users/vivek/.ssh/id_rsa.pub.
The key fingerprint is:
80:5f:25:7c:f4:90:aa:e1:f4:a0:01:43:4e:e8:bc:f5 vivek@desktop01
The key's randomart image is:
+--[ RSA 2048]----+
| oo    ...+.     |
|.oo  .  .ooo     |
|o .o. . .o  .    |
| o ...+o.        |
|  o .=.=S        |
| .  .Eo .        |
|                 |
|                 |
|                 |
+-----------------+
```

<p align="center">
  <img src="https://user-images.githubusercontent.com/99768694/162584200-4ae2df7f-95ae-418b-9910-30b37916d2ea.png" alt="image" width="800"/>
</p>

<p align="center">
  <img src="https://user-images.githubusercontent.com/99768694/162584184-6bb0a740-a3f5-4bdb-b520-3d8275e41ad4.png" alt="image" width="800"/>
</p>

---

**Step 6: Optimizing Remote Running** <br>
---

---
