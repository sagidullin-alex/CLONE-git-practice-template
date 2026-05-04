# git-practice-template
Создать репозиторий через **Use this template** из шаблона в своём GitHub-аккаунте


1) Клонируем репозиторий

`git clone https://github.com/<username>/<repo>.git`  
`cd <repo>`

2) Первичная настройка Git

`git config --global user.name "Имя Фамилия"`  
`git config --global user.email "email@example.com"`

3) Main - создать файл и сделать коммит

`echo "Первая версия файла" > test.txt`  
`git add test.txt`  
`git commit -m "Первый коммит"`  
`git push -u origin main`

4) Создать ветку feature и сделать коммит в ней

`git switch -c feature`  
`echo "Изменение во второй ветке" >> test.txt`  
`git add test.txt`  
`git commit -m "Изменение в feature"`  
`git push -u origin feature`

5) Вернуться в main, сделать коммит в main и смержить feature

git checkout main  
echo "Изменение в main" >> test.txt  
git add test.txt  
git commit -m "Изменение в main"  
  
git merge feature  
git push

6) README
В `README.md` добавьте/замените строку:

 `STUDENT_TOKEN: TOKEN-<ваш_github_username>`

и закоммитьте:

```
git add README.md
git commit -m "Add student token"
git push
```

Если появился конфликт в `test.txt`, откройте файл и приведите его к такому виду:

```
Первая версия файла
Изменение во второй ветке
Изменение в main
```

Затем выполните:

```
git add test.txt
git commit -m "merge feature"
git push
```
