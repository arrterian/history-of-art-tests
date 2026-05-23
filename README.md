# Тести з історії мистецтва (ЄФВВ)

Self-contained HTML quiz player для підготовки до єдиного фахового вступного випробування з історії мистецтва.

- **545 питань** у 8 розділах (385 згенерованих з конспекту [magistratura.in.ua](https://magistratura.in.ua/) + 160 реальних ЗНО з [zno.osvita.ua](https://zno.osvita.ua/master/mystectvo/list.html))
- Питання та варіанти відповідей перемішуються щоразу
- При неправильній відповіді показує сніпет з конспекту, де є правильна відповідь
- Прогрес НЕ зберігається між сесіями (свідомо)
- Тільки один файл `index.html`, працює офлайн після першого завантаження

Запускається тут: <https://arrterian.github.io/history-of-art-tests/>

## Як оновити

```bash
# в основному проекті
python3 build_tests.py && python3 find_snippets.py && python3 embed_tests.py
cp quiz/tests.html deploy/index.html
cd deploy && git add index.html && git commit -m "Update quiz" && git push
```
