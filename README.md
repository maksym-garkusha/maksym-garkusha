### Максим Гаркуша

Навчаюся в КНУ імені Тараса Шевченка на двох спеціальностях: інженерія програмного забезпечення і політологія. Пишу на C# інструменти на відкритих даних держави: програма забирає реєстр чи API, перевіряє, що в ньому заповнено, і показує результат сторінкою. [In English](#in-english)

[dream-povnota](https://github.com/maksym-garkusha/dream-povnota): наскільки повно заповнені картки проєктів відновлення в системі DREAM. Програма щодня забирає з відкритого API всі 16 тисяч карток і в кожній відкритій перевіряє поля, доречні на її стадії. Опис, місце й документи є в 99% карток. А от серед проєктів у реалізації, де вже є фінансування чи закупівля, картку за останній рік оновлювали лише в кожному четвертому.

- [сторінка](https://maksym-garkusha.github.io/dream-povnota/) з розрізом за областями, секторами й організаціями;
- [перевірка однієї картки](https://dream-povnota.onrender.com/check) за кодом чи посиланням, так само в [Telegram-боті](https://t.me/dream_povnota_bot);
- [щотижневий зріз](https://dream-povnota.onrender.com/digest) у xlsx і PDF для Агентства відновлення та обласних служб;
- історія змін з 18 листопада 2026 року, вивантаження в CSV і Excel, відкритий API.

C#, .NET 11, ASP.NET Core, PostgreSQL 18.

[ukraine-digital-aid](https://github.com/maksym-garkusha/ukraine-digital-aid): хто з донорів фінансує цифровізацію в Україні, через кого і до коли. Дані з міжнародного реєстру IATI зведені в одну [сторінку з пошуком](https://maksym-garkusha.github.io/ukraine-digital-aid/) українською та англійською. Окремо видно, що змінилося за тиждень, які записи стосуються енергетики і які програми завершуються протягом року та хто їх виконує («вікна можливостей»). C#, .NET 10.

[energoreestr](https://github.com/maksym-garkusha/energoreestr): відкриті реєстри НКРЕКП з data.gov.ua, зведені за кодом ЄДРПОУ, з [пошуком](https://maksym-garkusha.github.io/energoreestr/), історією змін і звітом про якість самих файлів. Головний реєстр формально не є CSV, і [ось чому](https://github.com/maksym-garkusha/energoreestr#що-виявилося-у-файлах). C#, .NET 11, ASP.NET Core, EF Core, SQLite.

[ua-codes](https://github.com/maksym-garkusha/ua-codes): бібліотека .NET без залежностей, яка перевіряє ЄДРПОУ, РНОКПП, IBAN, EIC і КАТОТТГ. Виросла з перевірок в energoreestr. Пакет готовий до першого випуску на NuGet: публікація через Trusted Publishing, без ключа в репозиторії, з атестацією і SBOM.

**Безпека і походження даних**

- Файли, які викладаються на сторінки, мають атестацію походження: `gh attestation verify` показує workflow і коміт, з якого їх зібрано.
- Вебсервіс dream-povnota не приймає випуск даних, у якому за раз змінилось набагато більше, ніж буває за день.
- Податкові номери й контакти фізичних осіб програми відкидають ще під час розбору, на це є тести. У кожного з чотирьох проєктів є SECURITY.md з приватним каналом для повідомлень про вразливості.

Усе це незалежні навчальні проєкти на відкритих даних. Вони не пов'язані з державними органами, а їхні числа не є офіційною статистикою.

Ще тут: [cv](https://github.com/maksym-garkusha/cv), мій сайт-резюме [garkusha-cv.vercel.app](https://garkusha-cv.vercel.app), і [path-of-science](https://github.com/maksym-garkusha/path-of-science), сайт наукової спільноти з формою заявок.

Зв'язок: Telegram [@maksym55555](https://t.me/maksym55555)

### In English

I study software engineering and political science at Taras Shevchenko National University of Kyiv and write small C#/.NET tools on Ukrainian open government data.

- [dream-povnota](https://github.com/maksym-garkusha/dream-povnota/blob/main/README.en.md) checks how complete the project records are in DREAM, the system where Ukrainian communities and regional restoration services manage reconstruction projects. It has a daily [page](https://maksym-garkusha.github.io/dream-povnota/), a [web service](https://dream-povnota.onrender.com/check) and a [Telegram bot](https://t.me/dream_povnota_bot) that check one record on request, and a weekly digest for the State Agency for Restoration and the regional services. The interface is in Ukrainian.
- [ukraine-digital-aid](https://github.com/maksym-garkusha/ukraine-digital-aid/blob/main/README.en.md) shows which donors fund Ukraine's digital transformation, through whom and until when, based on IATI data. The [page](https://maksym-garkusha.github.io/ukraine-digital-aid/) has an English version and lists energy-related records and programmes ending within the next twelve months.
- [energoreestr](https://github.com/maksym-garkusha/energoreestr) merges the public registers of Ukraine's energy and utilities regulator (NEURC) by company code, with a [search page](https://maksym-garkusha.github.io/energoreestr/).
- [ua-codes](https://github.com/maksym-garkusha/ua-codes) is a dependency-free .NET library that validates Ukrainian identifiers: EDRPOU, RNOKPP, IBAN, EIC and KATOTTG codes. It and energoreestr are documented in Ukrainian only.

These are independent student projects built on open data. They are not affiliated with any government body or donor, and their figures are not official statistics.
