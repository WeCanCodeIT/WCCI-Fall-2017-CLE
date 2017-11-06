# Git Branching and Merging
### Git Commits
- Each time there's a code change, we make a commit.
- We can think of a straight line with many dots, each dot representing a commit.

### Benefits of Git
- Allows us to collaborate/work with others.
- `master` is the default branch for any git repository when it is created.
- We have the ability to create other branches.

### Creating Branches
- `testBranch1` or `featureBranch` as demonstrated in class.
- Called branches because they look like branches on a tree. Difference is that they merge back in to master.
- Branches create a copy and allow us to have a separate place to work on something.
- Separate stream of development, separate commits, exist on their own.

### Might want to create a branch ...
- To test something that you're not sure you want to have as a part of your program.
- To work on a specific feature separate from the rest of the project before integrating it back in.

### Merging
- Takes changes and deviations of new branch and merges it back into another branch (usually `master`)
- Git merge takes what you have been working on separate from the project (the changes) and merges them into the branch.
- Where does the merge take place? 
  - One of the advantages of branching is that the rest of your team doesn't have to stop the work they're doing.
  - We don't have to coordinate with anyone, we can make our separate branch, do our separate commits, they can do what they're doing, and then when we're ready, we can merge our changes back in.
- What do you do when two people on a team are working with the same section of code? How do the changes line up?
  - Git is really smart when it comes to merging sets of code. Can track when changes were made. Git does its best to merge things together.
  - Eventually, git will run into some problems. It holds the separate parts of the code in separate places, and asks the developer to choose which changes she or he wants to include and which ones to not include. This is called resolving a *merge conflict*.
  
### Best Practice
- Nobody should be doing all of their work in `master`. `master` should be reserved for working, clean, tested code while all of the members of the team are doing their work in their separate branches.

### Where Can Branches Be Created?
- Branches can be made off of branches OR off of an existing branch.

### Interesting Fact
- Some teams change the name of their `master` branch to something like `stable`. However, `master` is the convention, so changing it from the standard might not be the best idea.

### Best Practice
- A `.gitignore` file goes a long way towards preventing merge conflicts!! *ALWAYS* include a `.gitignore`!

### Remember
- Include your `.gitignore` file in your project before initializing your git repository.

### To Find Your Graph
- In your git repository on Github, click the Insights tab, then choose Network, and you can see the graph as its getting built.

### Ways to Create a Branch
- Easiest command is `git checkout -b branchName` where "branchName" is replaced by whatever you are naming your branch. (You decide on the name) 
  - This command creates the branch and then switches you over to the new branch you've created.
  - Whenever you create a branch, it's taking the most recent code and making a copy for that branch.
  - The branch starts from wherever you currently are when you create your branch.
  
### Branch Naming
- If it's used for testing, call it `testBranch`.
- If it's used for building a feature, name the branch after that feature.
- Give some intention to your branch names.
- NO SPACES in your branch name. 
  - When you have spaces in your branch name, some programs will not function correctly with the branch.

### Knowing what branch you're in
- Git Bash will include the name of your branch in blue in parentheses.

### Pushing your branch to Github
- We've only ever previously done `git push origin master`
- With branches, we'll do `git push origin branchName` where "branchName" is replaced by whatever your branch's name is.

### To Switch Branches
- `git checkout` is the code we use to switch from one branch to another. Example: `git checkout master` from `testBranch`.
- When you switch a branch, Visual Studio will try to revert back your code wherever the code was when the branch was intitiated.

### Command to use sparingly
- `git push origin --all` will push all of your branches to Github. Use sparingly because you don't want to be pushing non-functional branches and you don't want all of the members of your team to have to delete the bad branches.
