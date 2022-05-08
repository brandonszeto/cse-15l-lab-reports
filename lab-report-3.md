## Streamlining SSH Configuration:<br><br>

By modifying the ssh/config, one can set an alias to use rather than typing out their full username. This can later be used in relevant ssh and scp commands.<br><br>

My .ssh/config file:
<p align="center">
  <img src="https://user-images.githubusercontent.com/99768694/167228670-01703dde-ffa2-4531-99f4-1d956b16629c.png" alt="image" width="800"/>
</p>
Logging into account with alias:
<p align="center">
  <img src="https://user-images.githubusercontent.com/99768694/167228710-cbfb6612-f5cb-414a-b3b6-702e64f7aead.png" alt="image" width="800"/>
</p>
Scp command usng alias:
<p align="center">
  <img src="https://user-images.githubusercontent.com/99768694/167228766-da1bc48c-21cf-46c4-bee2-74237518e6eb.png" alt="image" width="800"/>
</p>

## Setup GitHub Access from ieng6:<br><br>

By creating a public and private key stored on the ieng6 account, one can easily run git commands on the remote ieng6 account. This process can be accomplished by storing a key on Github and a key is the .ssh/ directory of the ieng6 account.<br><br>

Key stored on GitHub:
<p align="center">
  <img src="https://user-images.githubusercontent.com/99768694/167229767-1c5e6e7a-0ce8-422d-a5fd-187d680078ae.png" alt="image" width="800"/>
</p>

Public/Private key stored on ieng6 Account:
<p align="center">
  <img src="https://user-images.githubusercontent.com/99768694/167231767-e6044658-5b28-4232-86a0-a6bed9fd7c7d.png" alt="image" width="800"/>
</p>

Successfully running git push origin main on ieng6 Account:
<p align="center">
  <img src="https://user-images.githubusercontent.com/99768694/167278851-276a67a0-bb9d-40f8-a517-50d52c98baaa.png" alt="image" width="800"/>
</p>

## Copy Whole Directories with scp -r:<br><br>

Using the command scp -r, a whole directory, rather than a single file can be copied from the local machine to the ssh directory. This command can additionally be used in accordance with other commands in the same line to execute everything in one input. <br><br>

Copying markdown-parser onto ieng6:
<p align="center">
  <img src="https://user-images.githubusercontent.com/99768694/167232839-fa72b931-cbbe-47fb-83d9-fa0eb6aa2191.png" alt="image" width="800"/>
</p>

Compiling and running tests on ieng6:
<p align="center">
  <img src="https://user-images.githubusercontent.com/99768694/167232906-22895d27-e310-4297-8166-69c2b8a5ef69.png" alt="image" width="800"/>
</p>

Combining scp, ssh, compiling, and running tests:
<p align="center">
  <img src="https://user-images.githubusercontent.com/99768694/167233420-7eae4583-985c-46cf-8754-b6fc85953431.png" alt="image" width="800"/>
</p>
