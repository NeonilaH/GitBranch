1. На локальном репозитории сделать ветки для: Postman, Jmeter, CheckLists, Bug Reports, SQL, Charles, Mobile testing
	git branch Postman
	git branch Jmeter
	git branch CheckLists
	git branch bug_reports
	git branch SQL
	git branch Charles
	git branch Mobile_Testing
2. Запушить все ветки на внешний репозиторий 
	git push origin --all
3. В ветке Bag Reports сделать текстовый документ со структурой баг репорта
	git checkout bug_reports 
	touch bug_report.txt
		nano bug_report.txt
		#1) Bug Number/id.
		#2) Bug Title.
		#3) Priority.
		#4) Platform/Environment.
		#5) Description.
		#6) Steps to Reproduce.
		#7) Expected and Actual Result.
		#8) Attachments
	Ctrl+O ---> Enter ---> Ctrl+X
4. Запушить структуру багрепорта на внешний репозиторий 
	git add bug_report.txt 
	git commit -m "add bug report template txt file" 
	git push  --set-upstream origin bug_reports
5. Вмержить ветку Bag Reports в Main 
	git checkout main 
	git merge bug_reports
6. Запушить main на внешний репозиторий
	git status
	git push
7. В ветке CheckLists набросать структуру чек листа. 
	git checkout CheckLists 
	cat >> checklist_template.txt
		id
		check description
		check status (not run, pass, fail, skipped, blocked)
		comment
	Enter ---> Ctrl+C
8. Запушить структуру на внешний репозиторий 
	git add checklist_template.txt 
	git commit -m "add checklist txt file" 
	git push --set-upstream origin CheckLists
9. На внешнем репозитории сделать Pull Request ветки CheckLists в main Merge 
	Compare and pull request 
	Create pull request 
	Merge pull request 
	Confirm merge 
	Pull request successfully merged and closed
10. Синхронизировать Внешнюю и Локальную ветки Main 
	git fetch 
	git pull# GitBranch
