**Щоб створити базову структуру html, напишіть символ !і натисніть клавішу Tab. В результаті файл заповниться таким вмістом:**
&lt;!DOCTYPE html&gt;
&lt;html lang="en"&gt;
  &lt;head&gt;
    &lt;meta charset="UTF-8" /&gt;
    &lt;meta http-equiv="X-UA-Compatible" content="IE=edge" /&gt;
    &lt;meta name="viewport" content="width=device-width, initial-scale=1.0" /&gt;
    &lt;title&gt;Document&lt;/title&gt;
  &lt;/head&gt;
  &lt;body&gt;&lt;/body&gt;
&lt;/html&gt;

_Оператори вкладеності використовують для позиціонування елементів усередині згенерованого дерева._

Дочірній елемент
**Оператор &gt; дозволяє вкладати один елемент в інший:**

div&gt;ul&gt;li→

&lt;div&gt;
  &lt;ul&gt;
    &lt;li&gt;&lt;/li&gt;
  &lt;/ul&gt;
&lt;/div&gt;

Сусідний елемент
**Оператор + дозволяє розмістити елементи поряд один з одним на одному рівні:**

div+p+bq→

&lt;div&gt;&lt;/div&gt;
&lt;p&gt;&lt;/p&gt;
&lt;blockquote&gt;&lt;/blockquote&gt;

Повторення
**Оператор * дозволяє визначити, скільки разів повинен виводитись елемент:**

ul&gt;li*3→

&lt;ul&gt;
  &lt;li&gt;&lt;/li&gt;
  &lt;li&gt;&lt;/li&gt;
  &lt;li&gt;&lt;/li&gt;
&lt;/ul&gt;

Угруповання
**Круглі дужки дозволяють виділити в абревіатурі окремі піддерев'я:**

div&gt;(header&gt;ul&gt;li*2&gt;a)+footer&gt;p→

&lt;div&gt;
  &lt;header&gt;
    &lt;ul&gt;     
      &lt;li&gt;&lt;a href=""&gt;&lt;/a&gt;&lt;/li&gt;   
      &lt;li&gt;&lt;a href=""&gt;&lt;/a&gt;&lt;/li&gt;
    &lt;/ul&gt;
  &lt;/header&gt;
  &lt;footer&gt;
    &lt;p&gt;&lt;/p&gt;
  &lt;/footer&gt;
&lt;/div&gt;

_Можна вкладати групи одна в одну та повторювати їх за допомогою оператора множення:_

(div&gt;dl&gt;(dt+dd)*3)+footer&gt;p→

&lt;div&gt;
  &lt;dl&gt;
    &lt;dt&gt;&lt;/dt&gt;
    &lt;dd&gt;&lt;/dd&gt;
    &lt;dt&gt;&lt;/dt&gt;
    &lt;dd&gt;&lt;/dd&gt;
    &lt;dt&gt;&lt;/dt&gt;
    &lt;dd&gt;&lt;/dd&gt;
  &lt;/dl&gt;
&lt;/div&gt;
&lt;footer&gt;
  &lt;p&gt;&lt;/p&gt;
&lt;/footer&gt;

Атрибути операторів
**Ви можете вказати атрибути для елементів, що виводяться.**

Вказівка ​​класу та id
**Оператор . дозволяє вказати клас. Оператор # призначений для вказівки ID:**

div#header+div.page+div#footer.class1.class2.class3→

&lt;div id="header"&gt;&lt;/div&gt;
&lt;div class="page"&gt;&lt;/div&gt;
&lt;div id="footer" class="class1 class2 class3"&gt;&lt;/div&gt;

Довільні атрибути
**Квадратні дужки дозволяють задавати елементу довільні атрибути:**

td[title="Hello world!" colspan=3]→

&lt;td title="Hello world!" colspan="3"&gt;&lt;/td&gt;

_Довільні атрибути мають такі особливості:_
- Для розділення атрибутів використовується пробіл.
- Якщо не вказано значення атрибута, то його значенням стане порожній рядок із міткою для табуляції (якщо ваш редактор підтримує мітки табуляції).
- Можна використовувати одинарні та подвійні лапки для вказівки значень атрибутів.
- Якщо значення атрибута не містить прогалин, його не обов'язково укладати в лапки.

Нумерація
**Оператор $ дозволяє створювати нумерацію. Для цього помістіть оператор після імені елемента, імені атрибута або значення атрибута:**

ul&gt;li.item$*3→

&lt;ul&gt;
  &lt;li class="item1"&gt;&lt;/li&gt;
  &lt;li class="item2"&gt;&lt;/li&gt;
  &lt;li class="item3"&gt;&lt;/li&gt;
&lt;/ul&gt;

_Оператор $ можна помістити в будь-якому місці імені:_

ul&gt;li.ite$m*2→

&lt;ul&gt;
  &lt;li class="ite1m"&gt;&lt;/li&gt;
  &lt;li class="ite2m"&gt;&lt;/li&gt;
&lt;/ul&gt;

_Ви можете використовувати кілька операторів $ поспіль, щоб доповнити номер нулями:_

ul&gt;li.item$$$*3→

&lt;ul&gt;
  &lt;li class="item001"&gt;&lt;/li&gt;
  &lt;li class="item002"&gt;&lt;/li&gt;
  &lt;li class="item003"&gt;&lt;/li&gt;
&lt;/ul&gt;

Початкове значення та напрям нумерації
**Модифікатор @ дозволяє змінити початкове значення та напрямок нумерації (за зростанням або зменшенням). Щоб змінити напрям нумерації, додайте модифікатор @-після оператора $:**

ul&gt;li.item$@-*3→

&lt;ul&gt;
  &lt;li class="item3"&gt;&lt;/li&gt;
  &lt;li class="item2"&gt;&lt;/li&gt;
  &lt;li class="item1"&gt;&lt;/li&gt;
&lt;/ul&gt;

_Щоб змінити початкове значення лічильника, додайте модифікатор @N до оператора $:_

ul&gt;li.item$@3*5→

&lt;ul&gt;
  &lt;li class="item3"&gt;&lt;/li&gt;
  &lt;li class="item4"&gt;&lt;/li&gt;
  &lt;li class="item5"&gt;&lt;/li&gt;
  &lt;li class="item6"&gt;&lt;/li&gt;
  &lt;li class="item7"&gt;&lt;/li&gt;
&lt;/ul&gt;

_Ви можете змінити початкове значення лічильника та напрямок нумерації одночасно:_

ul&gt;li.item$@-3*5→

&lt;ul&gt;
  &lt;li class="item7"&gt;&lt;/li&gt;
  &lt;li class="item6"&gt;&lt;/li&gt;
  &lt;li class="item5"&gt;&lt;/li&gt;
  &lt;li class="item4"&gt;&lt;/li&gt;
  &lt;li class="item3"&gt;&lt;/li&gt;
&lt;/ul&gt;

Додавання тексту
**Фігурні дужки дозволяють додати текст до елемента:**

a{Перейти}→

&lt;a href=""&gt;Перейти&lt;/a&gt;

Неявні імена тегів
_У багатьох випадках не можна писати ім'я тега. Наприклад, замість цього div.contentви можете написати .content, що перетворюється на &lt;div class="content"&gt;&lt;/div&gt;. Emmet дивиться на батьківський тег щоразу, коли ви розширюєте абревіатуру без імені тега. Якщо батьківський елемент є блоковим , то вибрати тег div, в іншому випадку - span. При цьому є кілька винятків:_
- li для ul та ol.
- tr для table, tbody, thead і tfoot.
- td для tr.
- option для select та optgroup.

Генератор "Lorem Ipsum"
_Абревіатури "lorem" та "lipsum" генерують випадковий текст. Щоразу, коли ви виконуєте перетворення даних абревіатур, генерується текст із 30 слів, розбитий на кілька речень._

**lorem→**

Lorem ipsum dolor sit amet consectetur adipisicing elit. Et hic incidunt repellat, quos veritatis a tenetur deserunt accusantium ab ad adipisci ex rerum distinctio corrupti omnis asperiores, numquam exercitationem sapiente.

_Ви можете вказати кількість слів, що генеруються. Наприклад, lorem10згенерує текст із 10 слів. Також можна використовувати оператор повторення *, щоб створити кілька елементів з випадковим текстом:_

ul&gt;li*3&gt;lorem10→

&lt;ul&gt;
  &lt;li&gt;Lorem ipsum dolor sit amet consectetur adipisicing elit. Ad, temporibus.&lt;/li&gt;
  &lt;li&gt;Earum totam eius repudiandae sit optio, consectetur ipsum officiis enim?&lt;/li&gt;
  &lt;li&gt;Ex, molestias. Minima ducimus quaerat et earum commodi natus autem?&lt;/li&gt;
&lt;/ul&gt;

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
      "abbr1": "ul&gt;li*3",
      "abbr2": "ol&gt;li*3"
    }
  },
  "css": {
    "snippets": {
      "clw": "color: white",
      "clb": "color: black"
    }
  }
}
