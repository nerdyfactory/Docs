#### Basic workflow
1. Create new branch when you start to work with a new issue.
2. Create PR for the branch when you make some progress. with a description that `close ${url to issue}` so that linked PR will be shown in project board. the cards will be automatically moved to `In progress` section when new PR was created and moved to `Done` when it's merged to master.
3. Please note that you submit PR and push commits even if the job is not done yet, since it's important to share the progress by pushing commits in a remote team.
4. You can add more comments. for me to have a better understanding of the PR.
5. Make sure to make the PR draft if it's not done yet.
6. Request review by adding me to the reviewer.
7. If master was updated, so conflict is raised then rebase your branch and manually resolve the conflicts with `git fetch && git rebase origin/master` instead of doing `git merge master`
