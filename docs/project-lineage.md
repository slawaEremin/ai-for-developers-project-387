# Происхождение календаря и согласованные решения

Приложение перенесено из
[slawaEremin/ai-for-developers-project-386](https://github.com/slawaEremin/ai-for-developers-project-386)
в [slawaEremin/ai-for-developers-project-387](https://github.com/slawaEremin/ai-for-developers-project-387).
Исходная версия кода — коммит
[`b9a9cc55ecffea3db2504df260be925c2e5c8044`](https://github.com/slawaEremin/ai-for-developers-project-386/commit/b9a9cc55ecffea3db2504df260be925c2e5c8044).
[Глоссарий](../GLOSSARY.md) сохранён с локальными уточнениями исходного проекта.
Отдельного каталога `docs/adr/` на момент переноса не было; принятые решения
записаны в GitHub Issues первого проекта.

## Спецификация

- [Полная спецификация реализации, 386#10](https://github.com/slawaEremin/ai-for-developers-project-386/issues/10),
  включая разделы Implementation Decisions и Testing Decisions.
- [Карта решений, 386#1](https://github.com/slawaEremin/ai-for-developers-project-386/issues/1)
  и [итог завершённого планирования](https://github.com/slawaEremin/ai-for-developers-project-386/issues/1#issuecomment-6809569954).
- [Исходные требования Hexlet](https://ru.hexlet.io/projects/386/members/52904?step=1).

## Решения первого проекта

| Область | Согласованное решение |
| --- | --- |
| Данные типа встречи и записи | [386#2: данные и ограничения](https://github.com/slawaEremin/ai-for-developers-project-386/issues/2#issuecomment-6808703749) |
| Выбор слота и результат записи | [386#3: гостевой сценарий](https://github.com/slawaEremin/ai-for-developers-project-386/issues/3#issuecomment-6808826317) |
| Создание типов и предстоящие встречи | [386#4: сценарий владельца](https://github.com/slawaEremin/ai-for-developers-project-386/issues/4#issuecomment-6808903098) |
| Постоянное хранение и запуск | [386#5: PostgreSQL и модель запуска](https://github.com/slawaEremin/ai-for-developers-project-386/issues/5#issuecomment-6809016527) |
| Общая занятость и идемпотентность | [386#6: защита бронирования и повторы](https://github.com/slawaEremin/ai-for-developers-project-386/issues/6#issuecomment-6809224867) |
| API, ошибки, заголовки и генерация | [386#7: контракт календарного API](https://github.com/slawaEremin/ai-for-developers-project-386/issues/7#issuecomment-6809450702) |
| Приёмка и доказательства | [386#8: матрица из 40 критериев](https://github.com/slawaEremin/ai-for-developers-project-386/issues/8#issuecomment-6809555409) |

Текущее описание запуска находится в [README](../README.md) и
[документации инфраструктуры](../apps/infra/README.md): после первоначального
решения о запуске в проекте появился автономный контейнер со встроенным
PostgreSQL. Исторические решения читаются вместе с последующими изменениями кода
и документации.

## Реализация и приёмка

- [Протокол и соответствие тестов критериям](acceptance-calendar.md) перенесены
  вместе с приложением; указанный там прогон относится к первому проекту.
- [Итог реализации спецификации](https://github.com/slawaEremin/ai-for-developers-project-386/issues/10#issuecomment-6820852571)
  и [проверка release-please](https://github.com/slawaEremin/ai-for-developers-project-386/issues/10#issuecomment-6821539291)
  остаются свидетельствами первого проекта.
- [CHANGELOG](../CHANGELOG.md) сохраняет ссылки на исходные коммиты.

## Работа в новом репозитории

[Текущий трекер](https://github.com/slawaEremin/ai-for-developers-project-387/issues)
и [инструкции агента](agents/issue-tracker.md) относятся к репозиторию 387.
Задачи и комментарии 386 остаются по исходным адресам. Номер `#10` в новом
репозитории не обозначает прежнюю спецификацию: для унаследованных материалов
используй полные ссылки из этого документа.
