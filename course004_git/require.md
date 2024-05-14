# require

1. you need a VM & ssh conn to the VM , the VM need be linux (recommand Ubuntu)
1. new a bare mode git repo at the VM , like `testBare.git`
1. clone the `testBare.git` as new normal git `testBare/` , add new file name `README.md` and file body same as name , and commit & push first commit
1. make client and VM ssh without password
1. clone the `testBare.git` to local by like `ssh://{YOUR_VM_IP}/home/{YOUR_VM_USER}/testBare.git`
1. fix local `testBare/` and make new commit and push to VM `testBare.git`
1. just PR a file `answer.md` and file body as `OK` for finish this course