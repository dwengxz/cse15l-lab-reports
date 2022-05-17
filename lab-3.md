# **Streamlining ssh Configuration**
![Image](https://dwengxz.github.io/cse15l-lab-reports/sshconfig.jpg)

My .ssh/config file, edited in VScode

![Image](https://dwengxz.github.io/cse15l-lab-reports/sshAlias.PNG)

Logging into my remote account using the alias ieng6

![Image](https://dwengxz.github.io/cse15l-lab-reports/scpIeng6.PNG)

Using the alias to scp the file `example.txt` into my remote account

---
# **Setting up Github Access from ieng6**
![Image](https://dwengxz.github.io/cse15l-lab-reports/publickey.PNG)

Public ssh keys stored on Github

![Image](https://dwengxz.github.io/cse15l-lab-reports/privateKey.PNG)

Private key stored on my user account, in the file `id_ed25519.pub`

![Image](https://dwengxz.github.io/cse15l-lab-reports/gitPUSHED.PNG)

Pushing a change to Github from my ieng6 account

![Image](https://dwengxz.github.io/cse15l-lab-reports/gitcommit.PNG)

Commiting the pushed change
[The Resulting Commit](https://github.com/dwengxz/markdown-parser/actions/runs/2336689595)

---
# **Copying Whole Directories with `scp -r`**
![Image](https://dwengxz.github.io/cse15l-lab-reports/scpr1.PNG)
![Image](https://dwengxz.github.io/cse15l-lab-reports/scpr2.PNG)

Copying my whole markdown-parse directory into my ieng6 account

![Image](https://dwengxz.github.io/cse15l-lab-reports/scprrun1.PNG)

Compiling and running a test within my ieng6 account

![Image](https://dwengxz.github.io/cse15l-lab-reports/entering1.PNG)
![Image](https://dwengxz.github.io/cse15l-lab-reports/entering2.PNG)

Combining commands using `;` to copy and enter the directory in one line, and then run all my tests in one line. 


