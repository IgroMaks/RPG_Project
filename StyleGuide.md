# Руководство стиля *(Style-Guide)* для RPG Project

## **Важно!** Все участники должны внимательно изучить это руководство и следовать ему!

### 1. Соглашение о наименованиях

### 1.1 ДельфиСтиль
Все ассеты проекта должны называться по принципу ДельфиСтиля. Каждое слово начинается с заглавной буквы, не используются пробелы и нижние дефисы
Примеры:
> * SmallRock
> * EvilAxe
> * UnbeatableHighLevelMonster

### 1.2 Русский язык
Использование кириллицы или транслита строго запрещено! _Использование переводчика разрешено_. Лучше чудаковатое название на английском, нежели написанное транслитом слово "Pchela", или, того хуже, так и оставленное на русском "Пчела".

### 1.3 Наименивания ассетов
У каждого ассета должно быть своё базовое название. Любой ассет, являющийся частью определённой логической группы, должен следовать стандарту Префикc_БазовоеНазвание_Вариация_Суффикс.
* Префикс и Суффикс задаются исходя из типа ассета (все типы ассетов и их префиксы и суффиксы приведены в таблице ниже)
* Вариант используется для нумерации или уникализации ассета. Примеры:
> * SmallRock_01, CityWall_04 Statue_Full, Statue_Broken

### 1.3 Таблица имён ассетов
### 1.3.1 Часто используемые
| Тип ассета (EN)    | Префикс      | Суффикс    |
| ------------------ | ------------ | ---------- |
| Level / Map        |Не требуется, находятся в папке Maps|
| Level (Persistent) |              | _P         |
| Level (Audio)      |              | _Audio     |
| Level (Lighting)   |              | _Lighting  |
| Level (Geometry)   |              | _Geo       |
| Level (Gameplay)   |              | _Gameplay  |
| Blueprint          | BP_          |            |
| Material           | M_           |            |
| Static Mesh        | S_           |            |
| Skeletal Mesh      | SK_          |            |
| Texture            | T_           |См. таблицу [Текстуры]|
| Particle System    | PS_          |            |
| Widget Blueprint   | WBP_         |            |

### 1.3.2 Анимация
| Тип ассета (EN)       | Префикс    | Суффикс    |
| --------------------- | ---------- | ---------- |
| Aim Offset            | AO_        |            |
| Aim Offset 1D         | AO_        |            |
| Animation Blueprint   | ABP_       |            |
| Animation Composite   | AC_        |            |
| Animation Montage     | AM_        |            |
| Animation Sequence    | A_ or AS_  |            |
| Blend Space           | BS_        |            |
| Blend Space 1D        | BS_        |            |
| Level Sequence        | LS_        |            |
| Morph Target          | MT_        |            |
| Paper Flipbook        | PFB_       |            |
| Rig                   | Rig_       |            |
| Skeletal Mesh         | SK_        |            |
| Skeleton              | SKEL_      |            |

### 1.3.3 Искусственный интеллект
| Тип ассета (EN)   | Префикс      | Суффикс    |
| ----------------- | ------------ | ---------- |
| AI Controller     | AIC_         |            |
| Behavior Tree     | BT_          |            |
| Blackboard        | BB_          |            |
| Decorator         | BTDecorator_ |            |
| Service           | BTService_   |            |            
| Task              | BTTask_      |            |            

### 1.3.4 Блупринты
| Тип ассета (EN)            | Префикс       | Суффикс |
| -------------------------- | ------------- | ------- |
| Blueprint                  | BP_           |         |
| Blueprint Function Library | BPFL_         |         |                                  
| Blueprint Interface        | BPI_          |         |                                  
| Blueprint Macro Library    | BPML_         |         |
| Enumeration                | E             |         |
| Structure                  | Str           |         |
| Widget Blueprint           | WBP_          |         |

### 1.3.5 Материалы
| Тип ассета (En)               | Префикс      | Суффикс |
| ----------------------------- | ------------ | ------- |
| Material                      | M_           |         |
| Material (Post Process)       | PP_          |         |                           
| Material Function             | MF_          |         |                           
| Material Instance             | MI_          |         |                           
| Material Parameter Collection | MPC_         |         |                           
| Subsurface Profile            | SP_ или SSP_ |         |
| Physical Materials            | PM_          |         |  

### 1.3.6 Текстуры
| Тип ассета (EN)             | Префикс      | Суффикс    |
| --------------------------- | ------------ | ---------- |
| Texture                     | T_           |            |                                  
| Texture (Albedo/Base Color) | T_           | _BC        |                                  
| Texture (Normal)            | T_           | _N         |
| Texture (Roughness)         | T_           | _R         |
| Texture (Alpha/Opacity)     | T_           | _A         |
| Texture (Ambient Occlusion) | T_           | _O         |
| Texture (Bump)              | T_           | _B         |                                  
| Texture (Emissive)          | T_           | _E         |                                  
| Texture (Mask)              | T_           | _M         |                                  
| Texture (Specular)          | T_           | _S         |                                  
| Texture (Packed)            | T_           |См. об упаковке текстур ниже         |
| Texture Cube                | TC_          |            |                                  
| Media Texture               | MT_          |            |                                  
| Render Target               | RT_          |            |
| Cube Render Target          | RTC_         |            |                                  
| Texture Light Profile       | TLP          |            |

#### 1.3.6.1 Об упаковке текстур
Тут всё просто. Несколько текстур могут быть объединены в один файл в разных каналах(красный, зелёный, синий), тогда суффиксом данного файла будет объединение названий текстур из таблицы выше. Пример:
* _RMO, _EMS

### 1.3.7 Разное
| Тип ассета (EN)         | Префикс    | Суффикс    |
| ----------------------- | ---------- | ---------- |
| Animated Vector Field   | VFA_       |            |                                  
| Camera Anim             | CA_        |            |                                  
| Color Curve             | Curve_     | _Color     |                                  
| Curve Table             | Curve_     | _Table     |                                  
| Data Asset              | Основывается на классе        |            |
| Data Table              | DT_        |            |                                  
| Float Curve             | Curve_     | _Float     |                                  
| Foliage Type            | FT_        |            |                                  
| Force Feedback Effect   | FFE_       |            |                                  
| Landscape Grass Type    | LG_        |            |                                  
| Landscape Layer         | LL_        |            |                                  
| Matinee Data            | Matinee_   |            |                                  
| Media Player            | MP_        |            |                                  
| Object Library          | OL_        |            |                                  
| Sprite Sheet            | SS_        |            |                                  
| Static Vector Field     | VF_        |            |                                  
| Touch Interface Setup   | TI_        |            |                                  
| Vector Curve            | Curve_     | _Vector    |        

### 1.3.8 Физика
| Тип ассета (EN)         | Префикс    | Суффикс    |
| ----------------------- | ---------- | ---------- |
| Physical Material       | PM_        |            |                                  
| Physical Asset          | PHYS_      |            |                                  
| Destructible Mesh       | DM_        |            |     

### 1.3.9 Звуки
| Тип ассета (EN)         | Префикс    | Суффикс    |                   
| ----------------------- | ---------- | ---------- |
| Dialogue Voice          | DV_        |            |                                  
| Dialogue Wave           | DW_        |            |                                  
| Media Sound Wave        | MSW_       |            |                                  
| Reverb Effect           | Reverb_    |            |                                  
| Sound Attenuation       | ATT_       |            |                                  
| Sound Class             | Должен быть в отдельной папке `SoundClasses`           |            |
| Sound Concurrency       | Должен быть назван на основе `SoundClass`           | _SC        |  
| Sound Cue               | A_         | _Cue       |                                  
| Sound Mix               | Mix_       |            |                                 
| Sound Wave              | A_         |            |                                  

### 1.3.10 Графический интерфейс пользователя
| Тип ассета (EN)         | Префикс      | Суффикс    |
| ----------------------- | ------------ | ---------- |
| Font                    | Font_        |            |
| Slate Brush             | Brush_       |            |
| Slate Widget Style      | Style_       |            |
| Widget Blueprint        | WBP_         |            |

### 1.3.11 Эффекты
| Тип ассета (EN)         | Префикс    | Суффикс    |          
| ----------------------- | ---------- | ---------- |
| Particle System         | PS_        |            |                                  
| Material (Post Process) | PP_        |            |                                  

### 2. Структура папок проекта
Структура папок также должна восприниматься как закон. Она проекта так же важна, как и соглашение о наименованиях. Они тесно связаны, и нарушение правил любого из них приводит к ненужному хаосу в проекте.

### 2.1 Пример организации папок проекта
<pre>
|-- Content
    |-- RPGProject
        |-- Environment
        |   |-- Props
        |   |   |-- City
        |   |   |-- Country
        |   |   |-- Common
        |   |-- Nature
        |   |   |-- Foliage
        |   |   |-- Rocks
        |   |   |-- Trees
        |   |-- Buildings
        |   |   |-- Modules
        |   |   |-- Full
        |-- Characters
        |   |-- Bob
        |   |-- Common
        |   |   |-- Animations
        |   |   |-- Audio
        |   |-- Jack
        |   |-- Steve
        |   |-- Zoe
        |-- Core
        |   |-- Characters
        |   |-- Engine
        |   |-- GameModes
        |   |-- Interactables
        |   |-- Pickups
        |   |-- Weapons
        |-- Effects
        |   |-- Electrical
        |   |-- Fire
        |   |-- Weather
        |-- Maps
        |   |-- Global
        |   |-- CityInaella
        |   |-- FortRavenfort
        |-- MaterialLibrary
        |   |-- Debug
        |   |-- Metal
        |   |-- Paint
        |   |-- Utility
        |   |-- Weathering
        |-- Placeables
        |   |-- Pickups
        |-- Weapons
            |-- Swords
            |   |-- ChaosSeed
            |   |-- Chopper
            |-- Spears
            |-- Axes
   |-- Developers            
</pre>

### 2.2 Папка Developers
Используется для локального тестирования и отладки ещё не готовых ассетов, будь это меш, материал или блупринт. По сути, это экспериментальная зона ассетов перед их отправкой в основную папку проекта.
_**Не использовать ассеты из папки Developers в основной папке проекта ни в коем случае!**_

### 2.3 Папка Maps
Все уровни должны находится в папке Maps в отведённых для них подпапках вместе с файлов о сгенерированной геометрии, лайтмапы и путей.

### 2.4 Папка Core
Используйте папку _Core_ для тех ассетов, которые являются основой разработки проекта. Например, основные GameMode, Character, PlayerController, GameState, PlayerState и связанные блупринты должны находиться именно здесь.
Левел-дизайнеры должны использовать заранее приготовленные блупринты в специально отведенных папках, вместо того, чтобы всё время использовать и модифицировать базовые классы.

Например, если в проекте есть пикапы, которые могут быть расположены в уровне, для них должен быть базовый класс в папке Core/Pickups. Такой класс будет описывать базовое поведение пикапа. Конкретные пикапы, вроде аптечки или патронов уже будут располагаться в папке /Content/Project/Placeables/Pickups/. Гейм-дизайнеры могут спокойно редактировать эти пикапы по своему желанию, но они не должны трогать папку Core/Pickups, т.к. это косвенно может повредить работоспособность всех пикапов вообще.

### 2.5 Папка MaterialLibrary
Все Мастер-материалы, материалы ландшафта, пост-обработки должны хранится в папке MaterialLibrary. Уникальные материалы должны хранится вместе со своими текстурами и мешами, к примеру, материалы оружий и персонажей.
MaterialLibrary может содержать также и общие текстуры объединённые в своей папке.

#### 2.5.1 Папка MaterialLibrary/Debug
Содержит материалы предназначенные для тестирования и/или отладки
