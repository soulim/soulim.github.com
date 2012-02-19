---
layout: post
title: "Быстрый совет: изменение стиля вывода ошибок в формах Rails-приложения"
published: true
---

По умолчанию в Rails-приложении поля формы, содержащие ошибки, выводятся внутри элемента `<div>` с классом `.field_with_errors`. Вот так:

    <div class="field_with_errors">
      <input type="text" value="...">
    </div>

Но что если добавление элемента `<div class="field_with_errors">` только мешает? 

Все можно исправить переопределив метод вывода полей с ошибкой `ActionView::Base.field_error_proc`.

Рассмотрим пример, в котором поле с ошибками выводится без всякой дополнительной обертки.

    # config/initializers/field_error_proc.rb
    #
    # Customize the error messages HTML
    # There will be no div element enclosing the input element
    ActionView::Base.field_error_proc = Proc.new do |html_tag, instance|
      html_tag
    end

Использовал такой подход в формах созданных на базе [Twitter Bootstrap](http://twitter.github.com/bootstrap/), который имеет CSS-класс `.error`, задающий все нужные аттрибуты для отображения поля с ошибкой. При этом структура дерева элементов не меняется, а значит, добавляемый Rails, `<div class="fields_with_error">` только мешает.

Ссылки по теме:

- [Rails Guides: Customizing the Error Messages HTML](http://guides.rubyonrails.org/active_record_validations_callbacks.html#customizing-error-messages-css)
- 