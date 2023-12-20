## Git File
### [medium.com](https://medium.com/@pengcheng1222/mastering-git-part-1-understanding-the-roles-of-gitignore-gitattributes-and-gitkeep-0c1558fcdd1a)

### .gitignore
`.gitignore` is a Git configuration file that tells Git which ==files or folders to ignore== in a project.
- e.g.:
	- Personal configuration files
	- Build output
	- Files containing sensitive information
	- node_modules/
- usage:
	- Create a .gitignore file inside the root directory of the git repository.
	- Use [pattern matching](https://www.w3schools.com/git/git_ignore.asp?remote=github) to exclude the file(s) & folder(s).
### .gitattributes
`.gitattributes` is a Git configuration file that tells Git how to handles file content. It can control various attributes, such as merge strategies and line endings, providing a consistent workflow.
### .gitkeep
`.gitkeep` can be used to commit an empty folder because Git does not track empty folder.
- usage:
	- create an empty file named `.gitkeep` inside the folder.