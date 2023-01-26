# Проект: Путешествие по России

### Обзор
* Интро
* Figma
* Методы создания

**Интро**

Это проект о путешествиях по России, созданный с помощью адаптивной верстки. Здесь вы можете увидеть сетку из фотографий, описание различных мест с фото и множество ссылок на яндекс сервисы, которые можно посетить. Проект сделан с использованием макета в Фигме.
* [Ссылка на GitHub Pages](https://chaosyella.github.io/russian-travel/)

**Figma**

* [Ссылка на макет в Figma](https://www.figma.com/file/5S2WSbEFL6awjVWJ0NWL8Q/Sprint-3_-Russia-_-desktop-mobile?node-id=28503%3A0)

**Методы создания**

* Адаптивная верстка


* Grid

```css
.photo-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(284px, 1fr));
    gap: 16px;
}
```

* Медиазапросы

```css
@media screen and (max-width: 320px) {
    .cover__item {
        min-height: 200px;
    }
    .cover__item::before {
        min-height: 200px;
    }
}
```

* Flex

```css
.cover__item {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}
```

* Псевдоклассы

```css
.cover__item::before {
    content: "";
    position: absolute;
    display: block;
    width: 100%;
    min-height: 480px;
    background-color: #2A2C2F;
    opacity: .3;
}
```

* Nested

```css
@import url(./../vendor/normalize.css);
@import url(./../fonts/fonts.css);
@import url(./../blocks/page/page.css);
```

* Подключение шрифтов

```css
@font-face {
    font-family: 'Inter';
    src: url(./Inter-Web/Inter-Regular.woff) format('woof');
    src: url(./Inter-Web/Inter-Regular.woff2) format('woff2');
}
```