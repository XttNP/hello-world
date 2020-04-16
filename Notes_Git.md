# Notes on Git
I'll record some random notes on git here, most of which are the answers from official documents, stackoverflow, etc, 
when I tried to troubleshoot issues for my daily work.  
It's almost all git bash command line, because I just hate SourceTree. 
Just kidding, I first learned Git from a previous colleague who happened to know bash well. 
And yes, using command line feels more like a pro, say to speak.
Similarly, taking notes by Markdown also feels more like a pro.
### "x509: certificate signed by unknown authority"
git config --global http.sslVerify false  
(SourceTree answer) Find the "Disable SSL certificate validation (note: potentially insecure)" checkbox and check it.
### “Remote branch created but not appearing”
git remote update
### "Remote branch deleted but still appears"
git remote prune origin
### "Checkout from remote branch"
git checkout -b ['local branch name'] [origin/'remote branch name']  
git pull origin 'remote branch name'
### “Clean up”
git reset --hard  
git clean -fx  
git clean -fd  
git clean -fXd  
### "Unlink of file '.git/objects/pack/pack-***.pack' failed"
git gc --auto  
git repack -d -l
### "LFS Related"
Sometimes I follow all the instructions of Git LFS, but still large files are not pulled. The below may work.  
git lfs install --skip-smudge  
This skips automatic downloading of objects on clone or pull. So probably need to do "git pull" and "git lfs pull" manually for future commits.
### "Rebase and Squash"
First of all, [the official docs on rebase in Chinese](https://git-scm.com/book/zh/v2/Git-%E5%88%86%E6%94%AF-%E5%8F%98%E5%9F%BA) is so fun to read.  
To be updated..  
