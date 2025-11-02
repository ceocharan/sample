# Instructions for Copilot

## Original PR
- The link to the original PR that was merged into the `develop` branch will be provided in the chat.

## Branch Creation
1. Extract the branch name from the original PR link provided in the chat.
   - The branch name should be in the format: `username/TICKET-ID-version`

2. Create a new branch for version 8.5:
   - Branch name: `username/TICKET-ID-8.5`
   - Commands:
     ```
     git checkout 8.5-develop
     git pull origin 8.5-develop
     git checkout -b username/TICKET-ID-8.5
     ```

3. Create a new branch for version 8.4:
   - Branch name: `username/TICKET-ID-8.4`
   - Commands:
     ```
     git checkout 8.4-develop
     git pull origin 8.4-develop
     git checkout -b username/TICKET-ID-8.4
     ```

## Cherry-Pick Commits
1. Extract all the commit hashes from the original PR link provided in the chat.
   - Use the GitHub API or web scraping techniques to retrieve the list of commit hashes associated with the PR.

2. Cherry-pick each commit and apply them to both the newly created branches:
   - Commands:
     ```
     git checkout username/TICKET-ID-8.5
     <cherry-pick-commands>
     git push origin username/TICKET-ID-8.5

     git checkout username/TICKET-ID-8.4
     <cherry-pick-commands>
     git push origin username/TICKET-ID-8.4
     ```
   - Replace `<cherry-pick-commands>` with the actual cherry-pick commands for each commit hash. For example:
     ```
     git cherry-pick <commit-hash-1>
     git cherry-pick <commit-hash-2>
     ...
     ```

## Create Pull Requests
1. Create a pull request from the `username/TICKET-ID-8.5` branch to the `8.5-develop` branch:
   - Title: "TICKET-ID: Feature description (8.5)"
   - Description: "Applying the changes from the original PR to the 8.5-develop branch."

2. Create a pull request from the `username/TICKET-ID-8.4` branch to the `8.4-develop` branch:
   - Title: "TICKET-ID: Feature description (8.4)"
   - Description: "Applying the changes from the original PR to the 8.4-develop branch."

## Additional Notes
- The original PR link will be provided in the chat.
- The branch names will be derived from the original PR link, following the format `username/TICKET-ID-version`.
- All the commit hashes associated with the original PR will be extracted using the GitHub API or web scraping techniques.
- If there are any conflicts during the cherry-pick process, resolve them manually before creating the PRs.
- Notify the relevant team members or reviewers once the PRs are created.