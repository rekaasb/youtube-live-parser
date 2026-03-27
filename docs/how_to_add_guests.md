# Как добавить нового гостя

Откройте файл `index.html` в любом текстовом редакторе (Блокнот, VS Code и т.д.).

## Шаг 1. Найти функцию определения гостей

Найдите в коде функцию `getBlockType()` (примерно на строке 100-120).

Там будет примерно такой блок:

```javascript
if (lowerText.includes('быков') && lowerText.includes('с нами на связи')) 
    return { type: 'bykov', label: 'Дмитрий Быков', badge: 'badge-bykov' };
if (lowerText.includes('фаворов') || (lowerText.includes('эпидемиолог') && lowerText.includes('с нами на связи'))) 
    return { type: 'favorov', label: 'Михаил Фаворов', badge: 'badge-favorov' };
if (lowerText.includes('бородкин') || (lowerText.includes('иран') && lowerText.includes('с нами на связи'))) 
    return { type: 'borodkin', label: 'Михаил Бородкин', badge: 'badge-borodkin' };
if (lowerText.includes('кашин')) 
    return { type: 'kashin', label: 'Олег Кашин', badge: 'badge-kashin' };
