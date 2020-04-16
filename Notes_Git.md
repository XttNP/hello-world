# "Notes on Git"
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
