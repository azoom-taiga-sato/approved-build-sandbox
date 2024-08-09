# approved-build-sandbox

1. Coder) Coding in your own branch

2. Coder) Rebase your branch based on the main branch
    ```bash
    $ git checkout main

    $ git pull

    $ git checkout your branch

    $ git rebase main

    ```

3. Coder) Push your commits into a remote repository

4. Coder) Make a PR and ask a reviewer for their review/approval

5. *Reviewer) Approve the PR (*NOT merge it into the main branch at this point)

6. Coder) Update the version and create a new tag IN YOUR WORKING BRANCH and push again
    ```bash
    $ yarn version
    👇
    yarn version v1.22.22
    info Current version: 1.0.3
    question New version: 1.0.4
    info New version: 1.0.4
    ✨  Done in 4.05s.
    ```

8. *Reviewer) Do the final check and merge it into the main branch

9. Github actions AUTOMATICALLY pushes the new tag into remote repository and, accordingly, Cloud build gets prepared its build along with the new tag creation.

10. *Reviewer) Go to the Cloud Build and approve the prepared build
![alt text](image.png)