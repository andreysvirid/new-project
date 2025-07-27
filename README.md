# new-project

## Інструкція для розробників

1. Клонувати репозиторій
2. Створити нову гілку
3. Писати чистий код
4. Робити pull request

# 1. Створіть новий каталог
mkdir new-project
cd new-project

# 2. Ініціалізуйте новий публічний Git-репозиторій
git init -b main  # одразу створює гілку "main"

# 3. Створіть файл README.md з початковим текстом
echo "# New Project" > README.md

# 4. Підготуйте файл до коміту
git add README.md

# 5. Закомітьте з повідомленням “init”
git commit -m "init"

# 6. Створіть нову гілку "development" і перейдіть до неї
git checkout -b development

# 7. Додайте інструкцію до README.md
echo -e "\n## Інструкція для розробників\n\n1. Клонувати репозиторій\n2. Створити нову гілку\n3. Писати чистий код\n4. Робити pull request" >> README.md

# 8. Додайте зміни до коміту
git add README.md

# 9. Коміт у форматі Smart Commit (наприклад, з Jira issue KEY-123)
git commit -m "KEY-123 #comment: додано інструкцію до README.md #done"

# 10. Перейдіть на гілку main і об'єднайте зміни
git checkout main
git merge development

# 11. Перевірте статус
git status

# 12. (Опціонально) Додайте віддалений репозиторій та опублікуйте
# git remote add origin https://github.com/your-username/new-project.git
# git push -u origin main
# git push origin development