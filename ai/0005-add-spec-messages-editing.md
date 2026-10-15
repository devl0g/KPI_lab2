# Оновлення models/usecases/model.mmd

## Промпт

`📌 Додано вміст models/usecases/model.mmd`

```in
Онови usecases модель з урахуванням нового REQ-026

| ID вимоги | Текст вимоги (EARS Syntax) |
| --- | --- |
| **REQ-001** | `WHEN` користувач надсилає запит на створення спільноти, система `SHALL` створити запис у сутності `community` та автоматично додати цього користувача до `membership` із роллю `owner`. |
| **REQ-002** | `WHILE` статус акаунту користувача є `active`, `WHEN` користувач надсилає текстове повідомлення в особистий чат чи чат спільноти, система `SHALL` зберегти новий запис у `personal message` або `community message` із прив'язкою до `author_id`. |
| **REQ-003** | `WHILE` статус акаунту користувача є `deactivated`, система `SHALL` забороняти будь-які дії в системі, окрім запитів на повторну активацію акаунту або його остаточне видалення. |
| **REQ-004** | `WHILE` статус акаунту користувача є `banned`, система `SHALL` повністю блокувати доступ до функціоналу платформи. |
| **REQ-005** | `IF` користувач є `owner` спільноти, `THEN` система `SHALL` забороняти йому виконання операції виходу (`leave`) із цієї спільноти. |
| **REQ-006** | `WHEN` модератор спільноти надсилає запит на видалення повідомлення, `IF` автор повідомлення має роль `owner` або `moderator` у цій спільноті, `THEN` система `SHALL` відхилити запит та повернути помилку доступу. |
| **REQ-007** | `WHEN` модератор спільноти надсилає запит на вигнання учасника, `IF` цільовий учасник має роль `owner` або `moderator`, `THEN` система `SHALL` блокувати цю дію. |
| **REQ-008** | `WHEN` власник спільноти призначає учасника модератором, система `SHALL` оновити атрибут `community_role` відповідного запису у сутності `membership`. |
| **REQ-009** | `WHEN` адмін платформи або користувач надсилає запит на видалення акаунту, система `SHALL` виконати каскадне видалення користувача (`user_id`), його повідомлень, фактів членства (`membership`) та створених ним спільнот. |
| **REQ-010** | `WHEN` Бот модерації надсилає API-запит на отримання нових повідомлень спільноти, система `SHALL` повернути повідомлення з `message_id` більшим за `bot_last_message_received` та оновити цей атрибут у `community`. |
| **REQ-011** | `WHEN` Бот модерації надсилає запит на видалення повідомлення в спільноті, `IF` автор повідомлення має роль `owner` або `moderator`, `THEN` система `SHALL` відхилити запит бота. |
| **REQ-012** | `WHERE` повідомлення створюється як відповідь (`replies_to_id`), система `SHALL` перевіряти, що оригінальне повідомлення належить тому самому чату (`recipient_id` або `community_id`). |
| **REQ-013** | `WHEN` користувач надсилає запит на вступ до спільноти, система `SHALL` створити новий запис у сутності `membership` із роллю `member`. |
| **REQ-014** | `WHEN` учасник (`member`) спільноти надсилає запит на вихід (`leave`), система `SHALL` видалити відповідний запис із сутності `membership`. |
| **REQ-015** | `WHEN` користувач надсилає запит на видалення власного повідомлення, система `SHALL` видалити цей запис із бази даних. |
| **REQ-016** | `WHEN` користувач надсилає запит на деактивацію власного акаунту, система `SHALL` змінити статус акаунту на `deactivated`. |
| **REQ-017** | `WHEN` деактивований або заблокований користувач (або модератор/адмін платформи) надсилає запит на активацію чи розблокування акаунту, система `SHALL` змінити статус акаунту на `active`. |
| **REQ-018** | `WHEN` модератор спільноти надсилає запит на видалення повідомлення звичайного учасника або вигнання звичайного учасника, система `SHALL` успішно виконати відповідну операцію. |
| **REQ-019** | `WHEN` власник спільноти надсилає запит на оновлення інформації своєї спільноти, система `SHALL` оновити атрибути `title`, `description`, `slug` та `avatar_url` з перевіркою унікальності `slug`. |
| **REQ-020** | `WHEN` власник спільноти надсилає запит на видалення своєї спільноти, система `SHALL` виконати каскадне видалення спільноти та пов'язаних із нею повідомлень і членств. |
| **REQ-021** | `WHEN` власник спільноти надсилає запит на позбавлення учасника прав модератора, система `SHALL` змінити атрибут `community_role` у сутності `membership` з `moderator` на `member`. |
| **REQ-022** | `WHEN` модератор платформи надсилає запит на зміну статусу будь-якої спільноти, видалення спільноти, видалення будь-якого повідомлення, деактивацію або блокування користувача, система `SHALL` виконати відповідну дію. |
| **REQ-023** | `WHEN` адмін платформи надсилає запит на призначення або позбавлення користувача ролі модератора платформи (`platform_role`), система `SHALL` оновити відповідний атрибут користувача. |
| **REQ-024** | `WHEN` адмін платформи надсилає запит на надання або позбавлення користувача ролі адміна платформи (`platform_role`), система `SHALL` оновити відповідний атрибут користувача. |
| **REQ-025** | `WHILE` статус акаунту користувача є `active`, `WHEN` користувач надсилає запит на перегляд повідомлень особистого або спільнотного чату, система `SHALL` повернути історію повідомлень відповідного чату. |
| **REQ-026** | `WHEN` користувач надсилає запит на редагування власного повідомлення, система `SHALL` змінити значення `text_content` повідомлення на оновлений текст та встановити теперішній час як значення поля `edited_at` повідомлення у базі даних. |
```

## Відповідь

```out
Оновлена Use-Case модель та зв'язки з урахуванням нової вимоги **REQ-026** (редагування власного повідомлення).

---

### Зміни та доповнення:

1. **Новий Use Case:** Додано `EditOwnMessage("UC39: Редагування власного повідомлення")` у межі системи **'Чат'** (`systemBoundary 'Чат'`).
2. **Зв'язок (Include):** Додано обов'язкову перевірку статусу акаунту: `EditOwnMessage ..> : include CheckAccountStatus`.
3. **Актори:** Додано зв'язок для головного користувача (`User`), який може виконувати цю дію: `User --> EditOwnMessage`.

---

### Повний оновлений опис моделі (Mermaid / PlantUML-сумісний формат)

usecase-beta
direction LR

actor User('Користувач')
actor CommunityModerator('Модератор спільноти')
actor CommunityOwner('Власник спільноти')
actor PlatformModerator('Модератор платформи')
actor PlatformAdmin('Власник платформи')
actor Bot('Бот модерації')

CommunityModerator --|> User
CommunityOwner --|> CommunityModerator
PlatformModerator --|> User
PlatformAdmin --|> PlatformModerator

systemBoundary 'Чат'
    SendMessageCommunity("UC1: Відправити повідомлення у спільноту")
    SendMessageUser("UC2: Відправити повідомлення користувачу")
    ReplyMessage("UC3: Відповісти на повідомлення")
    DeleteOwnMessage("UC4: Видалення власного повідомлення")
    DeleteCommunityMessage("UC5: Видалення повідомлення спільноти")
    GetCommunityMessages("UC6: Перегляд повідомлень спільнотного чату")
    GetPersonalMessages("UC7: Перегляд повідомлень особистого чату")
    CheckMessageExistance("UC8: Перевірити існування повідомлення")
    EditOwnMessage("UC39: Редагування власного повідомлення")
end

systemBoundary 'Спільнота'
    JoinCommunity("UC9: Вступ у спільноту")
    LeaveCommunity("UC10: Вихід з чужої спільноти")
    SuspendCommunity("UC11: Призупинення спільноти")
    UnsuspendCommunity("UC12: Відновлення спільноти")
    DeleteCommunity("UC13: Видалення спільноти")
    CreateCommunity("UC14: Створення спільноти")
    RetrieveNewMessages("UC15: Агрегація нових повідомлень")
    KickMemberCommunity("UC16: Вигнання користувача з спільноти")
    EditCommunityInfo("UC17: Редагування інформації про спільноту")
    AddModeratorCommunity("UC18: Призначення модераторів спільноти")
    RemoveModeratorCommunity("UC19: Позбавлення ролі модератора спільноти")

    CheckCommunityStatus("UC20: Перевірити статус спільноти")
    CheckMembership("UC21: Перевірити членство у спільноті")
    CheckCommunityOwnership("UC22: Перевірити власність спільноти")
    CheckCommunityModerationship("UC23: Перевірити статус модератора спільноти або вище")
    VerifyBotToken("UC24: Веріфікувати токен бота")
end

systemBoundary 'Акаунт'
    DeactivateOwnAccount("UC25: Деактивація власного акаунту")
    DeactivateAccount("UC26: Деактивація акаунтів")
    ActivateOwnAccount("UC27: Активація власного акаунту")
    ActivateAccount("UC28: Активація акаунтів")
    DeleteAccount("UC29: Видалення акаунту")
    BanAccount("UC30: Блокування користувача")
    UnbanAccount("UC31: Розблокування користувача")
    AddModeratorPlatform("UC32: Призначення модераторів платформи")
    RemoveModeratorPlatform("UC33: Позбавлення ролі модератора платформи")
    AddAdminPlatform("UC34: Призначення адмінів платформи")
    RemoveAdminPlatform("UC35: Позбавлення ролі адміна платформи")

    CheckAccountStatus("UC36: Отримати статус акаунту")
    CheckPlatformAdmin("UC37: Перевірити статус адміна платформи")
    CheckPlatformModerationship("UC38: Перевірити статус модератора платформи або вище")
end

%%% Chat
ReplyMessage ..> : extend SendMessageCommunity
ReplyMessage ..> : extend SendMessageUser
DeleteCommunityMessage ..> : extend DeleteOwnMessage
SendMessageCommunity ..> : include CheckCommunityStatus
SendMessageCommunity ..> : include CheckMembership
SendMessageCommunity ..> : include CheckAccountStatus
SendMessageUser ..> : include CheckAccountStatus
ReplyMessage ..> : include CheckMessageExistance
DeleteOwnMessage ..> : include CheckAccountStatus
DeleteCommunityMessage ..> : include CheckCommunityStatus
DeleteCommunityMessage ..> : include CheckCommunityModerationship
GetCommunityMessages ..> : include CheckAccountStatus
GetPersonalMessages ..> : include CheckAccountStatus
EditOwnMessage ..> : include CheckAccountStatus

%%% Community
JoinCommunity ..> : include CheckAccountStatus
LeaveCommunity ..> : include CheckCommunityOwnership
CreateCommunity ..> : include CheckAccountStatus
EditCommunityInfo ..> : include CheckCommunityOwnership
AddModeratorCommunity ..> : include CheckCommunityOwnership
RemoveModeratorCommunity ..> : include CheckCommunityOwnership
KickMemberCommunity ..> : include CheckCommunityModerationship
DeleteCommunity ..> : include CheckCommunityOwnership
RetrieveNewMessages ..> : include VerifyBotToken

%%% Account
DeactivateOwnAccount ..> : include CheckAccountStatus
ActivateOwnAccount ..> : include CheckAccountStatus
DeleteAccount ..> : include CheckAccountStatus
BanAccount ..> : include CheckPlatformModerationship
UnbanAccount ..> : include CheckPlatformModerationship
DeactivateAccount ..> : include CheckPlatformModerationship
ActivateAccount ..> : include CheckPlatformModerationship
AddModeratorPlatform ..> : include CheckPlatformAdmin
RemoveModeratorPlatform ..> : include CheckPlatformAdmin
AddAdminPlatform ..> : include CheckPlatformAdmin
RemoveAdminPlatform ..> : include CheckPlatformAdmin

%%% Actors
User --> SendMessageCommunity
User --> SendMessageUser
User --> ReplyMessage
User --> DeleteOwnMessage
User --> EditOwnMessage
User --> JoinCommunity
User --> LeaveCommunity
User --> CreateCommunity
User --> DeactivateOwnAccount
User --> ActivateOwnAccount
User --> DeleteAccount
User --> GetCommunityMessages
User --> GetPersonalMessages

CommunityModerator --> DeleteCommunityMessage
CommunityModerator --> KickMemberCommunity

CommunityOwner --> EditCommunityInfo
CommunityOwner --> AddModeratorCommunity
CommunityOwner --> RemoveModeratorCommunity
CommunityOwner --> DeleteCommunity

PlatformModerator --> SuspendCommunity
PlatformModerator --> UnsuspendCommunity
PlatformModerator --> DeleteCommunity
PlatformModerator --> BanAccount
PlatformModerator --> UnbanAccount
PlatformModerator --> DeactivateAccount
PlatformModerator --> ActivateAccount

PlatformAdmin --> AddModeratorPlatform
PlatformAdmin --> RemoveModeratorPlatform
PlatformAdmin --> AddAdminPlatform
PlatformAdmin --> RemoveAdminPlatform
PlatformAdmin --> DeleteAccount

Bot --> RetrieveNewMessages
Bot --> DeleteCommunityMessage
```

# Оновлення матриці трасування

## Промпт

`💭 Збережено контекст минулого запиту`
`📌 Додано вміст traceability.md`

```in
Онови матрицю трасування, прапорцями позначаються непокриті UC та REQ
```

## Відповідь

```out
Оновлену матрицю трасування (Requirements Traceability Matrix) доповнено новим прецедентом **UC39 (Редагування власного повідомлення)** відповідно до вимоги **REQ-026**.

### Оновлена матриця трасування (РЕК / Use Cases)

| REQ / UC | UC1 | UC2 | UC3 | UC4 | UC5 | UC6 | UC7 | UC8 🏳️ | UC9 | UC10 | UC11 | UC12 | UC13 | UC14 | UC15 | UC16 | UC17 | UC18 | UC19 | UC20 🏳️ | UC21 🏳️ | UC22 🏳️ | UC23 🏳️ | UC24 🏳️ | UC25 | UC26 | UC27 | UC28 | UC29 | UC30 | UC31 | UC32 | UC33 | UC34 | UC35 | UC36 | UC37 🏳️ | UC38 🏳️ | UC39 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| **REQ-001** |  |  |  |  |  |  |  |  |  |  |  |  |  | x |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-002** | x | x |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | x |  |  |  |
| **REQ-003** 🏳️ |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-004** 🏳️ |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-005** |  |  |  |  |  |  |  |  |  | x |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-006** |  |  |  |  | x |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-007** |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | x |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-008** |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | x |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-009** |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | x |  |  |  |  |  |  |  |  |  |  |
| **REQ-010** |  |  |  |  |  |  |  |  |  |  |  |  |  |  | x |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-011** |  |  |  |  | x |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-012** |  |  | x |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-013** |  |  |  |  |  |  |  |  | x |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-014** |  |  |  |  |  |  |  |  |  | x |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-015** |  |  |  | x |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-016** 🏳️ |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-017** 🏳️ |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-018** |  |  |  |  | x |  |  |  |  |  |  |  |  |  |  | x |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-019** |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | x |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-020** |  |  |  |  |  |  |  |  |  |  |  |  | x |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-021** |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | x |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-022** |  |  |  |  | x |  |  |  |  |  | x | x | x |  |  | x |  |  |  |  |  |  |  |  | x | x | x | x |  | x | x |  |  |  |  |  |  |  |  |
| **REQ-023** |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | x | x |  |  |  |  |  |
| **REQ-024** |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | x | x |  |  |  |
| **REQ-025** |  |  |  |  |  | x | x |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | x |  |  |  |
| **REQ-026** |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | x |
```
