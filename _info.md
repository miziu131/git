

|Komenda git|			opis|
|-|---|
|git pull origin master| 		załodowanie lokalnego folderu stanem z serwera|
|git remote show origin|		wyświetlenie aktualnej ścieżki ustawionego domyśnej lokalizacji na serwerze |
|||


	git init
	git clone <url>

# Commit
	git add --all
	git commit -am "<message>"
	git push origin master

# Remote
	git remote -v
	git remote add origin <url>
	git remote set-url origin <url>   //?

# Ignore
	git config core.excludesfile C:\Users\frank\.gitignore_global   		#Ignore files across all repos on your system
	git rm --cached <file> 
	
https://docs.microsoft.com/en-us/azure/devops/repos/git/ignore-files?view=azure-devops&tabs=visual-studio#ignore-files-across-all-repos-on-your-system

# Branches
	git branch
	git branch <name>
	git checkout <name>
	git checkout -b <name>
	git pull origin <branch> 	**to pull the most recent changes from that remote branch.**

## Start a new feature
	git checkout -b new-feature master
	git add <file>					# Edit some files
	git commit -m "Start a feature"
	git add <file> 					# Edit some files
	git commit -m "Finish a feature"

## Merge in the new-feature branch
	git checkout master
	git merge new-feature
	git branch -d new-feature


## 3-way merge
	Start a new feature
	git checkout -b new-feature master
	git add <file>						# Edit some files
	git commit -m "Start a feature"
	git add <file> 						# Edit some files
	git commit -m "Finish a feature"
	
	git checkout master					# Develop the master branch
	git add <file>						# Edit some files
	git commit -m "Make some super-stable changes to master"

	git merge new-feature			# Merge in the new-feature branch
	git branch -d new-feature
