# Реестр школ магии карт

В игре **3 основные школы магии** (+ 4 базовые стартовые карты и 1 особое не-наградное проклятие событий).
Актуальный программный реестр в коде находится в `public/necromancer.html` внутри объекта `CardDatabase.SCHOOLS` (методы `CardDatabase.getCardsBySchool(schoolQuery)` и `CardDatabase.getSchoolCardCatalog()`).

> **Важно для ИИ и разработчиков:**
> - Поле `type: "curse"` («Проклятие») — это **тип карты**, а не школа магии. Карты-проклятия относятся к школе **Промантия** (или **Школа крови** в случае `bloodletting`).
> - В коде карты Школы крови используют строковое значение `school: "Кровавая магия"` (алиас `"Школа крови"` поддерживается в `CardDatabase.SCHOOLS.blood`).
> - Четыре стартовые карты (`death_strike`, `bone_armor`, `soul_steal`, `mystic_barrier`) имеют `school: "Базовая"` и `rewardEligible: false` — они не относятся к трём школам магии.
> - Карта `cursed_burden` («Бремя скверны», `school: "Проклятие склепа"`, `rewardEligible: false`) — особое штрафное проклятие событий, не относящееся к трём школам наград.

---

## Базовые / стартовые карты (вне школ, `4` карты)

Значение `card.school`: `"Базовая"` · `rewardEligible: false`

| # | ID карты | Название | Редкость | Тип | Цена |
|---|---|---|---|---|---|
| 1 | `death_strike` | Удар смерти | common | attack | 1 |
| 2 | `bone_armor` | Костяная броня | common | defense | 1 |
| 3 | `soul_steal` | Похищение души | uncommon | attack | 1 |
| 4 | `mystic_barrier` | Мистический барьер | common | defense | 1 |

---

## 1. Некромантия (`necromancy`, `22` карты)

Ключ: `CardDatabase.SCHOOLS.necromancy` · Значение `card.school`: `"Некромантия"`

| # | ID карты | Название | Редкость | Тип | Цена |
|---|---|---|---|---|---|
| 1 | `bone_legion` | Восстание костей | common | skill | 1 |
| 2 | `necromancer_summon` | Призыв некроманта | uncommon | skill | 1 |
| 3 | `bone_resonance` | Костяной резонанс | rare | skill | 1 |
| 4 | `bone_watch` | Костяной дозор | uncommon | skill | 2 |
| 5 | `bone_lord` | Владыка костей | legendary | skill | 3 |
| 6 | `sacrificial_ritual` | Жертвенный ритуал | uncommon | skill | 0 |
| 7 | `bone_shield` | Костяной щит | common | defense | 2 |
| 8 | `curse_of_the_dead` | Проклятие мертвых | common | attack | 1 |
| 9 | `last_stand_guardian` | Страж последнего рубежа | rare | skill | 2 |
| 10 | `final_order` | Последний приказ | uncommon | skill | 1 |
| 11 | `bone_restructuring` | Костяная перестройка | rare | skill | 1 |
| 12 | `march_of_the_dead` | Марш мёртвых | uncommon | skill | 2 |
| 13 | `bone_army_lord` | Повелитель костяной армии | rare | skill | 2 |
| 14 | `immortal_legion` | Бессмертный легион | rare | skill | 3 |
| 15 | `bone_ward` | Костяной оберег | uncommon | defense | 1 |
| 16 | `bone_volley` | Залп костей | common | attack | 1 |
| 17 | `command_attack` | Команда «Фас!» | common | skill | 0 |
| 18 | `undead_vanguard` | Авангард мертвецов | uncommon | skill | 1 |
| 19 | `plague_claws` | Чумные когти | uncommon | skill | 1 |
| 20 | `blood_summon` | Кровавый призыв | uncommon | skill | 0 |
| 21 | `total_mobilization` | Тотальная мобилизация | rare | skill | 3 |
| 22 | `death_reaper` | Пожинатель смерти | rare | power | 2 |

---

## 2. Промантия (`promancy`, `22` карты)

Ключ: `CardDatabase.SCHOOLS.promancy` · Значение `card.school`: `"Промантия"`

| # | ID карты | Название | Редкость | Тип | Цена |
|---|---|---|---|---|---|
| 1 | `decay_seal` | Печать тлена | common | curse | 1 |
| 2 | `agony_shackles` | Оковы агонии | uncommon | curse | 2 |
| 3 | `time_curse` | Проклятие времени | rare | curse | 2 |
| 4 | `retribution_curse` | Проклятие расплаты | rare | curse | 2 |
| 5 | `plague_blight` | Чумное поветрие | common | curse | 1 |
| 6 | `exhaustion` | Изнурение | common | defense | 1 |
| 7 | `decay_mark` | Печать упадка | uncommon | attack | 1 |
| 8 | `execution_doomed` | Казнь обреченных | rare | attack | 2 |
| 9 | `spores_of_decay` | Споры разложения | common | curse | 1 |
| 10 | `sands_of_oblivion` | Пески забвения | common | attack | 1 |
| 11 | `chains_of_exhaustion` | Цепи истощения | uncommon | curse | 1 |
| 12 | `chain_contagion` | Цепная зараза | uncommon | attack | 2 |
| 13 | `inevitable_decay` | Неизбежное разложение | rare | curse | 2 |
| 14 | `feast_of_rot` | Пиршество гнили | rare | curse | 2 |
| 15 | `eternity_epidemic` | Эпидемия вечности | rare | curse | 3 |
| 16 | `rotting_jab` | Гниющий укол | common | attack | 1 |
| 17 | `accelerate_decay` | Ускорение распада | common | curse | 1 |
| 18 | `contagious_corpse` | Заразный труп | uncommon | curse | 1 |
| 19 | `grim_harvest` | Мрачная жатва | uncommon | skill | 1 |
| 20 | `blood_curse` | Кровавое проклятие | uncommon | curse | 1 |
| 21 | `apotheosis_of_blight` | Апофеоз тлена | rare | curse | 2 |
| 22 | `symphony_of_agony` | Симфония агонии | rare | attack | 2 |

---

## 3. Школа крови / Кровавая магия (`blood`, `22` карты)

Ключ: `CardDatabase.SCHOOLS.blood` · Значение `card.school`: `"Кровавая магия"`

| # | ID карты | Название | Редкость | Тип | Цена |
|---|---|---|---|---|---|
| 1 | `blood_sacrifice` | Кровавая жатва | common | attack | 0 |
| 2 | `blood_thirst` | Кровавая жажда | uncommon | attack | 1 |
| 3 | `blood_ritual` | Кровавый ритуал | rare | skill | 1 |
| 4 | `hemoglobin` | Гемоглобин | common | attack | 1 |
| 5 | `blood_boiling` | Кипение крови | uncommon | attack | 2 |
| 6 | `filth_agony` | Агония скверны | rare | attack | 2 |
| 7 | `blood_barrier` | Кровавый барьер | common | defense | 1 |
| 8 | `blood_mirror` | Кровавое зеркало | uncommon | defense | 1 |
| 9 | `crimson_whisper` | Алый шёпот | uncommon | skill | 1 |
| 10 | `bloodletting` | Кровопускание | common | curse | 1 |
| 11 | `blood_impulse` | Кровавый импульс | common | skill | 1 |
| 12 | `life_siphon` | Перекачка жизни | common | attack | 1 |
| 13 | `blood_slash` | Кровавый разрез | common | attack | 1 |
| 14 | `crimson_shield` | Багровый щит | uncommon | defense | 1 |
| 15 | `battle_lust` | Жажда битвы | uncommon | skill | 0 |
| 16 | `blood_mark` | Кровавая метка | uncommon | skill | 1 |
| 17 | `blood_lord` | Владыка крови | rare | power | 2 |
| 18 | `blood_communion` | Кровавое причастие | rare | attack | 2 |
| 19 | `blood_retribution` | Кровавое возмездие | rare | attack | 2 |
| 20 | `heart_of_blood_god` | Сердце кровавого бога | legendary | attack | 2 |
| 21 | `blood_altar` | Кровавый алтарь | rare | power | 2 |
| 22 | `blood_brand` | Кровавое клеймо | uncommon | curse | 1 |

---

## Особое проклятие событий (вне школ, `1` карта)

| # | ID карты | Название | Редкость | Тип | Цена | Примечание |
|---|---|---|---|---|---|---|
| 1 | `cursed_burden` | Бремя скверны | common | curse | 1 | `school: "Проклятие склепа"`, `rewardEligible: false` |
