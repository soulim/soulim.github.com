---
layout: post
title: "Книга \"The SPDY Book: Making Websites Fly\""
published: true
thumb: spdy.png
thumb_url: http://pragprog.com/book/csspdy/the-spdy-book
---

Узнал о  протоколе SPDY, слушая шоу [Hypercritical от 5by5](http://5by5.tv/hypercritical). Одна из тем [эпизода #36](http://5by5.tv/hypercritical/36) была посвящена новым Amazon Kindle Fire. Браузер этих планшетов использует SPDY для получении контента от сервисов Amazon.

Если в нескольких словах, то SPDY - это протокол созданный для того, чтобы сделать интернет быстрее.

### The SPDY Book: Making Websites Fly

Книгу написал Крис Шторм (Chris Strom), а издали чудесные The Pragmatic Programmers.

The SPDY Book начинается с рассмотрения основных проблем протокола HTTP. Рассказывает почему простое увеличение пропускной способности канала мало влияет на скорость загрузки сайтов и веб-приложений. Тем самым подводит читателя к объяснению техник, которые используются в SPDY для устранения этих проблем:

- использование одного постоянного TCP-соединения,
- Server Push,
- сжатие заголовков с помощью zlib,
- обязательное использование SSL,
- обратная совместимость с HTTP/1.1.

The SPDY Book можно использовать как справочник по протоколу. Она подробно описывает потоки данных и их структуру (вплоть до битов).

На протяжении всего повествования рассматривается пример приложения (на базе Node.js). Этот пример становится сложнее по мере того, как читатель узнает больше о самом протоколе.

Поскольку SPDY пока не является стандартизованным протоколом, то многое может быть изменено и улучшено. Но если вы работаете с сервисами Google с помощью их Chrome, то уже сейчас пользуетесь протоколом SPDY.

### Ссылки по теме

- Книга [The SPDY Book: Making Websites Fly](http://pragprog.com/book/csspdy/the-spdy-book)
- Шоу [Hypercritical](http://5by5.tv/hypercritical). Еженедельные беседы о событях из мира Apple. Ведущие - Дэн Бенжамин (Dan Benjamin) и Джон Сиракьюса (John Siracusa)
- [SPDY Whitepaper](http://www.chromium.org/spdy/spdy-whitepaper)
- [Google Tech Talk: SPDY Essentials](http://www.youtube.com/watch?v=TNBkxA313kk)

Жду комментарии по электронной почте <soulim@gmail.com>, а также в Twitter [@soulim](http://twitter.com/soulim)