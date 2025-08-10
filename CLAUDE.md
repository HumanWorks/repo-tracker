# Git repo tracker

This projects hosts a collection of git repos that have interesting projects that I like
You are responsible for maintaining this, and bellow are the things you are supposed to do:

## Adding a repo
<prerequisite>
Make sure that the repo I ask you to add, does not already exists by comparing the remote repository urls. If that is the case stop and give an error to the user
</prerequisite>

When I give you a repo (eg. https://github.com/zhsama/claude-sub-agent/) you should:
1. create a directory after the repo's name (eg. claude-sub-agent/)
2. pull the repository in this directory
3. Use the Task tool and read the repo's README.md to create a summary of what it does
4. Update the @REPOS.md file with the summary. 

The repo's mention in @REPOS.md should have this form:
<repo_mention>
### {Repo name}
*URL*: {github_url}
*Name*: {repo_name}
*Description*: {description}
*Last update*: {YYYY-MM-DD}
</repo_mention>
4. Always cd back to the project root directory after adding the repo
5. Display ONLY what you wrote in the repo mention to the user

## Updating repos - DEFAULT BEHAVIOUR
When I ask you to check for updates or even if I say hi to you, you should do this for each repo:
1. git pull, but MAKE SURE that this will run in the background so that we can update all repos in parallel
2. Create a summary of what is changed since the previous update
3. Show me the changes for each repo in list format. Eg:
<change_log>
### {Repo_name}
1. {change_1}
2. {change_2}
...
</change_log>
4. Make sure to update *Last update* section of @REPOS.md with the latest update date and make changes to Name and Description if applicable

## Deleting repos
When I ask you to delete a repo make sure to:
1. Make sure you understand which repo I refer to, ask followup questions if I haven't provided the remote URL in my request
2. rm -rf the directory of the repo
3. Remove the repo mention from the list of repos in @REPOS.md
