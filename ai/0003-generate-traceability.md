# Початковий запит

## Промпт

`📌 Прикріплено models/usecases/model.mmd`
`📌 Прикріплено requirements.md`

```in
Прономеруй та поверни всі usecases у діаграмі (UC1, UC2).
Зроби матрицю трасування (горизонтально - UC, вертикально REQ, відповідність символом 'x').
Познач непокриті вимоги/UC емодзі 🏳️ у комірці таблички.
```

## Відповідь

```out
Ось пронумерований список усіх Use Cases (UC) із діаграми, а також таблиця матриці трасування (Traceability Matrix) між вимогами (REQ-001 — REQ-024) та Use Cases. Непокриті вимоги та Use Cases відзначено емодзі 🏳️.

---

### Список Use Cases (UC)

1. **UC1**: `SendMessageCommunity` — Відправити повідомлення у спільноту
2. **UC2**: `SendMessageUser` — Відправити повідомлення користувачу
3. **UC3**: `ReplyMessage` — Відповісти на повідомлення
4. **UC4**: `DeleteOwnMessage` — Видалення власного повідомлення
5. **UC5**: `DeleteCommunityMessage` — Видалення повідомлення спільноти
6. **UC6**: `CheckMessageExistance` — Перевірити існування повідомлення
7. **UC7**: `JoinCommunity` — Вступ у спільноту
8. **UC8**: `LeaveCommunity` — Вихід з чужої спільноти
9. **UC9**: `SuspendCommunity` — Призупинення спільноти 🏳️
10. **UC10**: `UnsuspendCommunity` — Відновлення спільноти 🏳️
11. **UC11**: `DeleteCommunity` — Видалення спільноти
12. **UC12**: `CreateCommunity` — Створення спільноти
13. **UC13**: `RetrieveNewMessages` — Агрегація нових повідомлень
14. **UC14**: `KickMemberCommunity` — Вигнання користувача з спільноти
15. **UC15**: `EditCommunityInfo` — Редагування інформації про спільноту
16. **UC16**: `AddModeratorCommunity` — Призначення модераторів спільноти
17. **UC17**: `RemoveModeratorCommunity` — Позбавлення ролі модератора спільноти
18. **UC18**: `CheckCommunityStatus` — Перевірити статус спільноти
19. **UC19**: `CheckMembership` — Перевірити членство у спільноті
20. **UC20**: `CheckCommunityOwnership` — Перевірити власність спільноти
21. **UC21**: `CheckCommunityModerationship` — Перевірити статус модератора спільноти або вище
22. **UC22**: `VerifyBotToken` — Веріфікувати токен бота 🏳️
23. **UC23**: `DeactivateOwnAccount` — Деактивація власного акаунту
24. **UC24**: `DeactivateAccount` — Деактивація акаунтів
25. **UC25**: `ActivateOwnAccount` — Активація власного акаунту
26. **UC26**: `ActivateAccount` — Активація акаунтів
27. **UC27**: `DeleteAccount` — Видалення акаунту
28. **UC28**: `BanAccount` — Блокування користувача
29. **UC29**: `UnbanAccount` — Розблокування користувача
30. **UC30**: `AddModeratorPlatform` — Призначення модераторів платформи
31. **UC31**: `RemoveModeratorPlatform` — Позбавлення ролі модератора платформи
32. **UC32**: `AddAdminPlatform` — Призначення адмінів платформи
33. **UC33**: `RemoveAdminPlatform` — Позбавлення ролі адміна платформи
34. **UC34**: `CheckAccountStatus` — Отримати статус акаунту
35. **UC35**: `CheckPlatformAdmin` — Перевірити статус адміна платформи
36. **UC36**: `CheckPlatformModerationship` — Перевірити статус модератора платформи або вище

*(А також додаємо умоглядні колонки для непокритих UC, якщо такі є у вимогах, але відсутні на діаграмі).*

---

### Матриця трасування (Traceability Matrix)

У таблиці рядки відповідають вимогам (**REQ**), а стовпці — Use Cases (**UC1** — **UC36**). Знак 'x' позначає відповідність. Якщо вимога або Use Case не покриті жодними зв'язками у проєкті, у відповідній комірці вказано емодзі **🏳️**.

| Вимоги \ UC | UC1 | UC2 | UC3 | UC4 | UC5 | UC6 | UC7 | UC8 | UC9 | UC10 | UC11 | UC12 | UC13 | UC14 | UC15 | UC16 | UC17 | UC18 | UC19 | UC20 | UC21 | UC22 | UC23 | UC24 | UC25 | UC26 | UC27 | UC28 | UC29 | UC30 | UC31 | UC32 | UC33 | UC34 | UC35 | UC36 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| **REQ-001** |  |  |  |  |  |  |  |  |  |  |  | x |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-002** | x | x |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-003** |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | x |  | x |  | x |  |  |  |  |  |  | x |  |  |
| **REQ-004** |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | x |  |  |  |  |  |  |  |  |
| **REQ-005** |  |  |  |  |  |  | x |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-006** |  |  |  |  | x |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | x |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-007** |  |  |  |  |  |  |  |  |  |  |  |  |  | x |  |  |  |  |  |  | x |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-008** |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | x |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-009** |  |  |  |  |  |  |  |  |  |  | x |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | x |  |  |  |  |  |  |  |  |  |
| **REQ-010** |  |  |  |  |  |  |  |  |  |  |  |  | x |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-011** |  |  |  |  | x |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-012** |  |  | x |  |  | x |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-013** |  |  |  |  |  |  | x |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-014** |  |  |  |  |  |  |  | x |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-015** |  |  |  | x |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-016** |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | x |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-017** |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | x |  | x |  | x | x |  |  |  |  | x |  |  |
| **REQ-018** |  |  |  |  | x |  |  |  |  |  |  |  |  | x |  |  |  |  |  |  | x |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-019** |  |  |  |  |  |  |  |  |  |  |  |  |  |  | x |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-020** |  |  |  |  |  |  |  |  |  |  | x |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-021** |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | x |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-022** |  |  |  |  | x |  |  |  | x | x | x |  |  | x |  |  |  |  |  |  |  |  |  | x |  | x |  | x | x |  |  |  |  |  |  |  |
| **REQ-023** |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | x | x |  |  |  |  |  |
| **REQ-024** |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | x | x |  |  |  |

---

*Примітка щодо непокритих елементів (🏳️):*

* **Непокриті Use Cases** (на діаграмі є, але в жодній вимозі явно не згадані як основний прояв): `SuspendCommunity` (UC9), `UnsuspendCommunity` (UC10), `VerifyBotToken` (UC22). Вони відзначені у списку вище. У самій таблиці рядки вимог для них відсутні, оскільки всі 24 вимоги із завдання вдалось зіставити з наявними функціями, проте самі UC 9, 10 та 22 не знайшли відповідності в жодному REQ (тому для них зазвичай ставиться статус 🏳️ як для неасоційованих функцій).
```

## Аудит

- ШІ повернуло нумерацію окремим списком, хоча я мав на увазі зміну діаграми.
- Він прапорцями позначив пункти списку, зоча я хотів, щоб він це робив прямо у діаграмі.
- Єдиним продуктом відпові хочу матрицю у вигляді таблички md та оновлену діаграму.

# Правка 1

## Промпт

`📌 Прикріплено models/usecases/model.mmd`
`📌 Прикріплено requirements.md`

```in
Прономеруй usecases прямо у діаграмі (UC1, UC2). Оновлену діаграму поверни.
Зроби матрицю трасування (горизонтально - UC, вертикально REQ, відповідність символом 'x').
Познач непокриті вимоги/UC емодзі 🏳️ прямо у комірці таблички (в крайніх, перший стовпець чи перший рядок).
```

## Відповідь

```out
Ось оновлена діаграма `usecase-beta` з пронумерованими use case'ами (від `UC1` до `UC31`) та матриця трасування вимог (REQ) до use case'ів із позначками непокритих елементів (`🏳️`).

---

## 1. Оновлена діаграма Use Case

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

    CheckMessageExistance("UC6: Перевірити існування повідомлення")
end

systemBoundary 'Спільнота'
    JoinCommunity("UC7: Вступ у спільноту")
    LeaveCommunity("UC8: Вихід з чужої спільноти")
    SuspendCommunity("UC9: Призупинення спільноти")
    UnsuspendCommunity("UC10: Відновлення спільноти")
    DeleteCommunity("UC11: Видалення спільноти")
    CreateCommunity("UC12: Створення спільноти")
    RetrieveNewMessages("UC13: Агрегація нових повідомлень")
    KickMemberCommunity("UC14: Вигнання користувача з спільноти")
    EditCommunityInfo("UC15: Редагування інформації про спільноту")
    AddModeratorCommunity("UC16: Призначення модераторів спільноти")
    RemoveModeratorCommunity("UC17: Позбавлення ролі модератора спільноти")

    CheckCommunityStatus("UC18: Перевірити статус спільноти")
    CheckMembership("UC19: Перевірити членство у спільноті")
    CheckCommunityOwnership("UC20: Перевірити власність спільноти")
    CheckCommunityModerationship("UC21: Перевірити статус модератора спільноти або вище")
    VerifyBotToken("UC22: Веріфікувати токен бота")
end

systemBoundary 'Акаунт'
    DeactivateOwnAccount("UC23: Деактивація власного акаунту")
    DeactivateAccount("UC24: Деактивація акаунтів")
    ActivateOwnAccount("UC25: Активація власного акаунту")
    ActivateAccount("UC26: Активація акаунтів")
    DeleteAccount("UC27: Видалення акаунту")
    BanAccount("UC28: Блокування користувача")
    UnbanAccount("UC29: Розблокування користувача")
    AddModeratorPlatform("UC30: Призначення модераторів платформи")
    RemoveModeratorPlatform("UC31: Позбавлення ролі модератора платформи")
    AddAdminPlatform("UC32: Призначення адмінів платформи")
    RemoveAdminPlatform("UC33: Позбавлення ролі адміна платформи")

    CheckAccountStatus("UC34: Отримати статус акаунту")
    CheckPlatformAdmin("UC35: Перевірити статус адміна платформи")
    CheckPlatformModerationship("UC36: Перевірити статус модератора платформи або вище")
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
User --> JoinCommunity
User --> LeaveCommunity
User --> CreateCommunity
User --> DeactivateOwnAccount
User --> ActivateOwnAccount
User --> DeleteAccount

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

---

## 2. Матриця трасування (REQ vs Use Cases)

> У таблиці рядок — це вимога (REQ), стовпець — це use case (UC1–UC36). Непокриті вимоги або use case'и позначені символом **🏳️** у відповідних крайніх комірках (перший стовпець/перший рядок).

| REQ / UC | UC1 | UC2 | UC3 | UC4 | UC5 | UC6 | UC7 | UC8 | UC9 | UC10 | UC11 | UC12 | UC13 | UC14 | UC15 | UC16 | UC17 | UC18 | UC19 | UC20 | UC21 | UC22 | UC23 | UC24 | UC25 | UC26 | UC27 | UC28 | UC29 | UC30 | UC31 | UC32 | UC33 | UC34 | UC35 | UC36 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| **REQ-001** |  |  |  |  |  |  |  |  |  |  |  | x |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-002** | x | x | x |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-003** 🏳️ |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-004** 🏳️ |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-005** |  |  |  |  |  |  |  | x |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-006** |  |  |  |  | x |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-007** |  |  |  |  |  |  |  |  |  |  |  |  |  | x |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-008** |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | x |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-009** |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | x |  |  |  |  |  |  |  |  |  |
| **REQ-010** |  |  |  |  |  |  |  |  |  | x |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-011** |  |  |  |  | x |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-012** |  |  | x |  |  | x |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-013** |  |  |  |  |  |  | x |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-014** |  |  |  |  |  |  |  | x |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-015** |  |  |  | x |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-016** |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-017** 🏳️ |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-018** |  |  |  |  | x |  |  |  |  |  |  |  |  | x |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-019** |  |  |  |  |  |  |  |  |  |  |  |  |  |  | x |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-020** |  |  |  |  |  |  |  |  |  |  | x |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-021** |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | x |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-022** |  |  |  |  | x |  |  |  | x |  | x |  |  | x |  |  |  |  |  |  |  |  |  |  | x | x | x | x |  |  |  |  |  |  |  |  |
| **REQ-023** |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | x | x |  |  |  |  |  |  |  |  |  |  |  |  |
| **REQ-024** |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | x | x |  |  |
```

## Аудит

- Результат задовільний
