# ml_engineering_practices
## установка пакетного менеджера
curl -fsSL https://pixi.sh/install.sh | bash
## Установить линтеры и форматтеры разобранные на прошлом занятии.
pixi global install autopep8
pixi global install flake8

## Зафиксировать настройки форматера и линтера в .toml
pixi add autopep8
pixi add flake8

## Отформатировать код с помощью isort и black/autopep8/yapf и т.д.
autopep8 calibrate.py

## Провести анализ кода с помощью выбранных линтеров и зафиксировать проблемы в файле linting.md
flake8 calibrate.py >>  linting.md

## Провести рефакторинг выявленных проблем.
autopep8 --in-place --aggressive --aggressive calibrate.py > linting.md

