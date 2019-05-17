

|Komenda git|			opis|
|-|---|
|git pull origin master| 		załodowanie lokalnego folderu stanem z serwera|
|git remote show origin|		wyświetlenie aktualnej ścieżki ustawionego 
domyśnej lokalizacji na serwerze |
|||

# Branches
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
