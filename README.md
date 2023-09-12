**Щоб створити базову структуру html, напишіть символ !і натисніть клавішу Tab. В результаті файл заповниться таким вмістом:**
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body></body>
</html>

_Оператори вкладеності використовують для позиціонування елементів усередині згенерованого дерева._

Дочірній елемент
**Оператор > дозволяє вкладати один елемент в інший:**

div>ul>li→

<div> 
  <ul>
    <li></li>
  </ul>
</div>

Сусідний елемент
**Оператор + дозволяє розмістити елементи поряд один з одним на одному рівні:**

div+p+bq→

<div></div>
<p></p>
<blockquote></blockquote>

Повторення
**Оператор * дозволяє визначити, скільки разів повинен виводитись елемент:**

ul>li*3→

<ul>
  <li></li>
  <li></li>
  <li></li>
</ul>

Угруповання
**Круглі дужки дозволяють виділити в абревіатурі окремі піддерев'я:**

div>(header>ul>li*2>a)+footer>p→

<div>
  <header>
    <ul>     
      <li><a href=""></a></li>   
      <li><a href=""></a></li>
    </ul>
  </header>
  <footer>
    <p></p>
  </footer>
</div>

_Можна вкладати групи одна в одну та повторювати їх за допомогою оператора множення:_

(div>dl>(dt+dd)*3)+footer>p→

<div>
  <dl>
    <dt></dt>
    <dd></dd>
    <dt></dt>
    <dd></dd>
    <dt></dt>
    <dd></dd>
  </dl>
</div>
<footer>
  <p></p>
</footer>

Атрибути операторів
**Ви можете вказати атрибути для елементів, що виводяться.**

Вказівка ​​класу та id
**Оператор . дозволяє вказати клас. Оператор # призначений для вказівки ID:**

div#header+div.page+div#footer.class1.class2.class3→

<div id="header"></div>
<div class="page"></div>
<div id="footer" class="class1 class2 class3"></div>

Довільні атрибути
**Квадратні дужки дозволяють задавати елементу довільні атрибути:**

td[title="Hello world!" colspan=3]→

<td title="Hello world!" colspan="3"></td>

_Довільні атрибути мають такі особливості:_
- Для розділення атрибутів використовується пробіл.
- Якщо не вказано значення атрибута, то його значенням стане порожній рядок із міткою для табуляції (якщо ваш редактор підтримує мітки табуляції).
- Можна використовувати одинарні та подвійні лапки для вказівки значень атрибутів.
- Якщо значення атрибута не містить прогалин, його не обов'язково укладати в лапки.

Нумерація
**Оператор $ дозволяє створювати нумерацію. Для цього помістіть оператор після імені елемента, імені атрибута або значення атрибута:**

ul>li.item$*3→

<ul>
  <li class="item1"></li>
  <li class="item2"></li>
  <li class="item3"></li>
</ul>

_Оператор $ можна помістити в будь-якому місці імені:_

ul>li.ite$m*2→

<ul>
  <li class="ite1m"></li>
  <li class="ite2m"></li>
</ul>

_Ви можете використовувати кілька операторів $ поспіль, щоб доповнити номер нулями:_

ul>li.item$$$*3→

<ul>
  <li class="item001"></li>
  <li class="item002"></li>
  <li class="item003"></li>
</ul>

Початкове значення та напрям нумерації
**Модифікатор @ дозволяє змінити початкове значення та напрямок нумерації (за зростанням або зменшенням). Щоб змінити напрям нумерації, додайте модифікатор @-після оператора $:**

ul>li.item$@-*3→

<ul>
  <li class="item3"></li>
  <li class="item2"></li>
  <li class="item1"></li>
</ul>

_Щоб змінити початкове значення лічильника, додайте модифікатор @N до оператора $:_

ul>li.item$@3*5→

<ul>
  <li class="item3"></li>
  <li class="item4"></li>
  <li class="item5"></li>
  <li class="item6"></li>
  <li class="item7"></li>
</ul>

_Ви можете змінити початкове значення лічильника та напрямок нумерації одночасно:_

ul>li.item$@-3*5→

<ul>
  <li class="item7"></li>
  <li class="item6"></li>
  <li class="item5"></li>
  <li class="item4"></li>
  <li class="item3"></li>
</ul>

Додавання тексту
**Фігурні дужки дозволяють додати текст до елемента:**

a{Перейти}→

<a href="">Перейти</a>

Неявні імена тегів
_У багатьох випадках не можна писати ім'я тега. Наприклад, замість цього div.contentви можете написати .content, що перетворюється на <div class="content"></div>. Emmet дивиться на батьківський тег щоразу, коли ви розширюєте абревіатуру без імені тега. Якщо батьківський елемент є блоковим , то вибрати тег div, в іншому випадку - span. При цьому є кілька винятків:_
- li для ul та ol.
- tr для table, tbody, thead і tfoot.
- td для tr.
- option для select та optgroup.

Генератор "Lorem Ipsum"
_Абревіатури "lorem" та "lipsum" генерують випадковий текст. Щоразу, коли ви виконуєте перетворення даних абревіатур, генерується текст із 30 слів, розбитий на кілька речень._

**lorem→**

Lorem ipsum dolor sit amet consectetur adipisicing elit. Et hic incidunt repellat, quos veritatis a tenetur deserunt accusantium ab ad adipisci ex rerum distinctio corrupti omnis asperiores, numquam exercitationem sapiente.

_Ви можете вказати кількість слів, що генеруються. Наприклад, lorem10згенерує текст із 10 слів. Також можна використовувати оператор повторення *, щоб створити кілька елементів з випадковим текстом:_

ul>li*3>lorem10→

<ul>
  <li>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ad, temporibus.</li>
  <li>Earum totam eius repudiandae sit optio, consectetur ipsum officiis enim?</li>
  <li>Ex, molestias. Minima ducimus quaerat et earum commodi natus autem?</li>
</ul>

Додавання абревіатур та фрагментів
_Деякі абревіатури перетворюються на елементи з встановленими атрибутами. Список таких абревіатур для різних мов ви можете переглянути в офіційному репозиторії в каталозі snippets . Наприклад, абревіатури для html знаходяться у файлі html.json._

Спосіб додавання абревіатур можна дізнатися в документації плагіна, який використовуєте в текстовому редакторі. Якщо використовується Visual Studio Code, вам потрібно створити файл snippets.json. Таких файлів може бути кілька, наприклад, один із глобальними налаштуваннями, а інший з локальними на рівні проекту. Потім у файлі налаштувань VSCode додайте параметр emmet.extensionsPath, що містить масив шляхів до каталогів, що містить файл snippets.json. Розглянемо з прикладу: створіть каталог .vscodeу поточному проекті. У каталозі .vscode створіть файли settings.json та snippets.json.
**Ось як це зробити через термінал:**

mkdir .vscode && cd .vscode
touch settings.json && touch snippets.json

У файл settings.jsonдодайте наступне налаштування:

{"emmet.extensionsPath": ["./.vscode"]}

_У файлі snippets.json для кожної мови записуються його псевдоніми та фрагменти. На даний момент у VSCode використовується Emmet 2.0. У цій версії абревіатури та фрагменти задаються через один параметр snippets. Створимо кілька абревіатур для html:css_

{
  "html": {
    "snippets": {
      "abbr1": "ul>li*3",
      "abbr2": "ol>li*3"
    }
  },
  "css": {
    "snippets": {
      "clw": "color: white",
      "clb": "color: black"
    }
  }
}
