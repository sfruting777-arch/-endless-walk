# Бесконечная прогулка

Отдельный проект. Старую игру не изменяем. Основа сада и управления будет перенесена позже из проверенной версии.

- Игрушка для сбора: зелёный поросёнок.
- Собака: исправление геометрии, затем скелет и анимации.
- Хозяин: модель, прогулка, бросание палки.
- Финал: большое дерево, скамейка, совместное фото.
- Рабочие фразы: «Где бы я ни была, моя любимая прогулка — всегда рядом с тобой»; «У каждой прогулки есть конец. Но у настоящей дружбы его нет, пока живёт память»; «Воспоминания — это место, где мы никогда не расстаёмся».
- После финала свободная прогулка.

Мастерская: workshop/index.html. Загружает локальные GLB без отправки файлов на сервер. Для запуска нужен HTTP-хостинг с доступом к CDN Three.js.

## Утверждённая походка
- V5.0 — утверждена пользователем, базовая анимация ходьбы: workshop-v50/index.html.
- V4.8 и V4.9 — резервные прототипы, не изменять.
- Следующий этап: отдельный игровой полигон с джойстиком, переходами покой/ходьба, камерой и FPS.


## Утверждение V5.3
- V5.3 (workshop-v53/index.html) — утверждена пользователем как основная походка с естественным движением позвоночника и лопаток.
- V5.0 — сохранённый резерв без дополнительных движений корпуса.
- Следующий этап: перенос V5.3 на отдельный игровой полигон, P1 оставить нетронутым.


## Утверждение P5 / V5.5
- playground-p5/index.html — утверждённая игровая основа: походка V5.3, наклон головы 7.8° в покое и 5.85° при ходьбе, исправление масштабирования Safari.
- Предыдущие версии сохранены. Следующие эксперименты создавать отдельно.


## Настройки языка
- P10: пользователь утвердил амплитуду 2.0; на скриншоте скорость 1.20, выделено 392 вершины.
- P11: эти значения амплитуды и скорости установлены по умолчанию. Маска языка пока выбирается вручную; точные индексы вершин не получены.


## Утверждение P14 / V5.14
- playground-p14/index.html — пользователь подтвердил автоматическую анимацию языка. Встроенная маска 386 вершин, амплитуда 2.0, скорость 1.20.
- P14 — новая утверждённая игровая основа. Сохранить без изменений.
- Следующий эксперимент: локальная деформация ушей (отдельных костей нет).


## Dog Final P19 / V5.19
- dog-final/index.html: candidate final dog assembly, automatic tongue (2.0), blink (2 calibrated eyes), ears (133+146 vertices, amplitude 4.0), speed 1.20. No manual selection needed.
- P18 and P14 remain intact as backups. Awaiting final visual test of integrated ear masks.


## Хозяин — утверждение H12
- owner-workshop-h12/index.html: пользователь утвердил внешний вид. База H9, модель owner-v2-rig-no-animations.glb, отдельные очки масштаб 0.925, верхняя губа 0.003, узкая маска без пересчёта нормалей. Сохранить H12 неизменной.
- Следующий этап: отдельная версия естественной ходьбы, опора стоп, плавный перенос веса, спокойные руки без подпрыгивания. DOG FINAL не менять.

- Дополнительная задача перед ходьбой: убрать посторонний серый выступ сзади кепки по скриншоту пользователя (H12). Проверить геометрию и текстуру, восстановить волосы/край кепки локально, сохранить остальное лицо и H12 без изменений.


## H15 — утверждена улыбка
- Пользователь подтвердил, что H15 при открытии без дополнительных мазков выглядит хорошо. Сохранить автоматическую ретушь десны, включая UV 0.1919, 0.9541, как есть. Очки 0.925, губа 0.003 (39 вершин). H15 не изменять; последующие эксперименты делать отдельно. Экспорт JSON не требуется для утверждённого состояния по умолчанию.


## H22 — внешность хозяина окончательно утверждена
- owner-workshop-h22/index.html и cap-repair.json: пользователь утвердил ремонт кепки (33 вершины, 4 участка текстуры). H22 сохранить неизменной как финальную базу внешности.
- Следующие тесты: H23 ноги и колени; H24 контакт стоп с землёй; H25 руки, таз, плечи; H26 плавный старт/остановка; H27 повороты. Нумерация предварительная, зависит от тестов. Затем совместная тестовая сцена хозяина и собаки.


## Порядок совместной разработки (обязательный)
- Пользователь — тестировщик и художественный руководитель; ассистент — инженер. Ассистент сам изменяет код, публикует отдельную версию GitHub Pages и даёт ссылку для теста. Не предлагать пользователю править код самостоятельно и не заменять выполнение планом. Сохранять утверждённые версии.
- H27: уменьшено движение таза для проверки деформации правого бедра/штанов; корпус 0.65 по умолчанию. Если дефект сохраняется, проверить веса скиннинга, особенно влияние костей руки на ткань.


## John — approved for park integration
- Approved baseline: `owner-workshop-h40/index.html` (H41 contour experiment rejected as visually insignificant). Preserve H40 unchanged.
- Settings: tempo 0.80, stride 0.36, lift 0.035, torso 0.40, arms 1.0. Narrow stance, neck correction, toe flex, garment repairs retained.
- Re-evaluate gait in park with dog before further changes.
- Park direction: compact circular path around a large illuminated tree; benches, flowers, lights, free camera; walking with leash and toggle for free dog roaming. No scoring or timed tasks.


## Park V7 — approved fetch stick
- User approved branch appearance and size in Park V7. Asset: `models/approved/park_stick_optimized.glb` (582744 bytes, 9993 triangles). Preserve geometry and textures.
- In park: length 0.40 m; cross-section scale 1.35 relative to uniform scaling at 40 cm (1.8× V6 thickness). Preserve local centering and ground alignment.
- Approved park baseline: `park-v7/index.html`, 44 m park, 2.4 m path, John and dog scale retained. Next: fetch interaction (throw, retrieve, return to John); keep V7 intact.


### Park V33
- V32 underhand stick toss approved by user; preserve it.
- V33 treat drop 5.5 cm, 0.23 s; pending visual test.
- Workflow: assistant directly implements changes in GitHub and provides test URL; user tests. Do not send implementation instructions instead of making edits.


### Park V34 — approved
- User approved treat drop: 10.5 cm over 0.32 s. Preserve fingertip placement and treat size from V31, underhand toss from V32.
- Keep `park-v34/index.html` as approved baseline for subsequent development.
