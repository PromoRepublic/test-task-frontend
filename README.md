# Frontend engineer test task

Привет 👋

![image](https://user-images.githubusercontent.com/22681040/112503899-faa8af80-8d93-11eb-8116-1c489ce3b3b9.png)

Есть [макет](https://www.figma.com/file/m0KFM5S4TC5EYHl7bNJEHa/PromoRepublic-Test-Task)

Тебе говорят, что нужно сделать рабочий фронт, однако backend еще не готов, так что вот пока файл с коллекцией [mock-данных](https://github.com/PromoRepublic/test-task-frontend/blob/main/data.json) в том же формате, что будет возвращать backend в будущем

В коллекции 6 типов объектов:

```
const ASSET_TYPES = {
  TEMPLATE: 0,
  IMAGE: 1,
  VIDEO: 2,
  PDF: 3,
  GIF: 4,
  ARTICLE: 5,
};
```

Каждый объект может содержать следующие типы аттрибутов,

**обязательные:**

```
id: number,
type: number,
title: string,
used-total-count: number,
created-at: number,
```
**и необязательные**

```
description?: string,
tags?: arrayOf(string),
preview-image?: string,
external-link?: shape({ 
  href: string, 
  title: string 
}),
original-file-src?: string,
```

**Твои задачи:**

1) Все необходимо сделать на [Ember.js](https://emberjs.com/). Это технология, которая используется у нас, и нам важно найти человека, который быстро и самостоятелльно сможет разбираться с новыми штуками.
2) Верстка, верстка, верстка. Последние браузеры. Можно использовать все что хочешь, кроме библиотек готовых компонентов (bootstrap etc). + базовое адаптивное поведение от тебя.
3) Левый бар должен применять фильтры по типам объектов.
4) По дефолту сортировка должна быть по аттрибуту `used-total-count` в порядке убывания.
5) Нужно вывести не более чем **50** объектов, попадающих под условия фильтрации и в соответствующем сортировке порядке.
6) При клике на иконку **bookmark** объект должен помечаться как сохраненный, иконка должна меняться на зеленую. Достаточно хранить это состояние до обновления страницы.

![image](https://user-images.githubusercontent.com/22681040/112619215-b79c1a00-8e2f-11eb-9788-88c90c6da57e.png)
 => ![image](https://user-images.githubusercontent.com/22681040/112619263-c7b3f980-8e2f-11eb-8fec-91d50c8b0495.png)

7) Если список тегов не помещается в одну строку - появляется тег с текстом "`+ n`", открывающий список остальных тегов: 

![image](https://user-images.githubusercontent.com/22681040/112619170-ae12b200-8e2f-11eb-956d-020e5f2c4e27.png)

8) Действие кнопки **use** на карточке должно быть контроллируемым снаружи нашего модуля с фильтрами и списком (например из родительского компонента, в который этот модуль вставляется)


**Дополнительно (если основые задачи показались легкими):**

9*) если в url будет указан get-параметр sort-by=created-at - сортировать по аттрибуту `created-at` в порядке убывания

**Пояснения**

Аттрибут `external-link` содержится только в объектах типа `ARTICLE`, в дизайне это футер с ссылкой:

![image](https://user-images.githubusercontent.com/22681040/112619096-91767a00-8e2f-11eb-83ef-c1aecd100ed6.png)



Аттрибут `original-file-src` содержится только в объектах типа `PDF`, это ссылка которая открывается в новом окне, когда пользователь нажимает на кнопку **download**. Кнопки **use** у `PDF` нет:

![image](https://user-images.githubusercontent.com/22681040/112619124-9f2bff80-8e2f-11eb-9548-b0d51678db42.png)


Удачи! 💪

Если будут возникать вопросы - пиши vitaliy@promorepublic.com, mike@promorepublic.com
✨
