#!/bin/bash

# Проверка пробелов в конце строк
if git diff --cached --check | grep -q 'trailing whitespace'; then
    echo "Ошибка: найдены пробелы в конце строк."
    exit 1  # Остановить коммит
fi

# Дополнительные проверки можно добавить здесь

exit 0  # Успешное завершение
