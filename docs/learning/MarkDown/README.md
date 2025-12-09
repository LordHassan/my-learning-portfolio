# MarkDown 語法

🌐[MarkDown 官網](https://www.markdownguide.org/)

:bulb:**提示:** 使用`ctrl + f`也可幫你快速搜尋到需求語法

<a id="directory"></a>

> ## 目錄：

| 基礎語法                             | 進階語法 | 其他 |
| ------------------------------------ | -------- | ---- |
| [Heading 標題](#heading)             |          |      |
| [Paragraphs 段落](#paragraphs)       |          |      |
| [Emphasis 強調](#emphasis)           |          |      |
| [Blockquotes 引用區塊](#blockquotes) |          |      |
| [Lists 清單](#lists)                 |          |      |
| [Code 代碼](#code)                   |          |      |

<a id="heading"></a>

> ### Heading 標題

| 標題大小 | HTML 表現       | MarkDown 語法 |
| -------- | --------------- | ------------- |
| h1       | `<h1>Text</h1>` | `# Text`      |
| h2       | `<h2>Text</h2>` | `## Text`     |
| h3       | `<h3>Text</h3>` | `### Text `   |
| h4       | `<h4>Text</h4>` | `#### Text`   |
| h5       | `<h5>Text</h5>` | `##### Text ` |
| h6       | `<h6>Text</h6>` | `###### Text` |

```markdown
...code

# ...code

...code
```

:warning: 注意 code 與"#"符號保持空格

:warning: 為了保持相容性，標題前後也應該留空行。

---

<a id="paragraphs"></a>

> ### Paragraphs 段落

若要建立段落，請使用空白行分隔一行或多行文字，

使用`Enter`鍵即可，並保持段落末尾空白。

---

<a id="emphasis"></a>

> ### Emphasis 強調

| 字體                  | HTML 表現                                                     | MarkDown 語法                             | render 渲染                             |
| --------------------- | ------------------------------------------------------------- | ----------------------------------------- | --------------------------------------- |
| 粗體 Bold             | `<strong>cat</strong>`                                        | `**cat** `                                | **cat**                                 |
| 粗體 Bold             | `A<strong> cat </strong>meow`                                 | `A **cat** meow`                          | A **cat** meow                          |
| 粗體 Bold             | `A<strong> cat </strong>meow`                                 | `A cat **meow**`                          | A cat **meow**                          |
| 粗體 Bold             | `A<strong> cat </strong>meow`                                 | `A cat __meow__`                          | A cat **meow**                          |
| 斜體 Italic           | `<em> cat </em>`                                              | `*cat*`                                   | _cat_                                   |
| 斜體 Italic           | `<em> cat </em>`                                              | `_cat_`                                   | _cat_                                   |
| 斜體 Italic           | `A<em> cat </em>meow`                                         | `A *cat* meow`                            | A _cat_ meow                            |
| 斜體 Italic+粗體 Bold | `This text is <em><strong>really important</strong></em>.`    | `This text is ***really important***.`    | This text is **_really important_**     |
| 斜體 Italic+粗體 Bold | `This text is <em><strong>really important</strong></em>.`    | `This text is ___really important___.`    | This text is **_really important_**.    |
| 斜體 Italic+粗體 Bold | `This text is <em><strong>really important</strong></em>.`    | `This text is **_really important_**.`    | This text is **_really important_**.    |
| 斜體 Italic+粗體 Bold | `This is really<em><strong>very</strong></em>important text.` | `This is really***very***important text.` | This is really**_very_**important text. |

❌ Don't do this : `A _cat_ meow`， Markdown 應用對於如何處理單字中間的底線並不一致。為了相容性，請使用星號將單字中間的部分斜體化以示強調。

❌ Don't do this :`This is really___very___important text.`，Markdown 應用對單字中間的底線處理方式並不一致。為了相容，建議使用星號來加粗或斜體強調單字中間的部分。

---

<a id="blockquotes"></a>

> ### Blockquotes 引用區塊

新增引用區塊，需在段落前添加`>`

下方代碼：

```markdown
> Dorothy followed her through many of the beautiful rooms in her castle.
>
> The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.
```

渲染如下：

<div class="renderBox">

> Dorothy followed her through many of the beautiful rooms in her castle.
>
> The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.

</div>
嵌套引用方法如下：

```markdown
> Dorothy followed her through many of the beautiful rooms in her castle.
>
> > The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.
```

渲染如下：

<div class="renderBox">

> Dorothy followed her through many of the beautiful rooms in her castle.
>
> > The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.

</div>

:warning: 為了保時相容性，請維持上下文空一行，如下：

```markdown
Try to put a blank line before...

> This is a blockquote

...and after a blockquote.
```

---

<a id="lists"></a>

> ### Lists 清單

若要建立<strong><font color=#fe8fdd>有序列表</font></strong>，請新增以數字開頭、後面跟著句點的行項目。數字不必依序排列，但清單必須從數字 1 開始。

假如代碼如下：

```markdown
1.Frist item
8.SecondItem
3.SixthItem
1.IndentedItem
7.IndentedItem
4.FourthItem
```

渲染結果：

<div class="renderBox">

1. Frist item
2. SecondItem
3. SixthItem
   1. IndentedItem
   2. IndentedItem
4. FourthItem

</div>

對應 html 語法：

```html
<ol>
  <li>First item</li>
  <li>SecondItem</li>
  <li>SixthItem</li>
    <ol>
      <li>IndentedItem</li>
      <li>IndentedItem</li>
    </ol>
  </li>
  <li>FourthItem</li>
</ol>
```

若要建立<strong><font color=#3cd466>無序號表</font></strong>，請在每行項目前面新增`-`、`+`、`*`，縮排即可建立嵌套清單。

假如代碼如下：

```markdown
- Frist item
- SecondItem
- SixthItem
  - IndentedItem
- IndentedItem
- FourthItem
```

渲染結果：

<div class="renderBox">

- Frist item
- SecondItem
- SixthItem
  - IndentedItem
- IndentedItem
- FourthItem

</div>

插入程式區塊或是圖片需縮排`tab`或是`space`四格，代碼如下：

```markdown
1.  Open the file.

    <a href="https://images.pexels.com/photos/34341418/pexels-photo-34341418.jpeg">
    <img src="https://images.pexels.com/photos/34341418/pexels-photo-34341418.jpeg" width="300" alt="圖片的替代文字">
    </a>

2.  Find the following code block on line 21:

        <html>
          <head>
            <title>Test</title>
          </head>

3.  Update the title to match the name of your website.
```

渲染如下：

<div class="renderBox">

1.  Open the file.

    <a href="https://images.pexels.com/photos/34341418/pexels-photo-34341418.jpeg"><img src="https://images.pexels.com/photos/34341418/pexels-photo-34341418.jpeg" width="300" alt="圖片的替代文字"></a>

2.  Find the following code block on line 21:

        <html>
          <head>
            <title>Test</title>
          </head>

3.  Update the title to match the name of your website.
</div>

---

<a id="code"><a>

> ### Code 代碼

插入代碼，使用 Backticks`` ` ``

| markdown       | html                  | render                                |
| -------------- | --------------------- | ------------------------------------- |
| `` `hellow` `` | `<code>hellow</code>` | <div class="renderBox">`hellow`</div> |

**Escaping Backticks 反引號跳脫**

若要在 backtick 中建立`` ` ``則需要如下方法：

| markdown                  | html                           | render                                          |
| ------------------------- | ------------------------------ | ----------------------------------------------- |
| ``` ``I `LOVE` YOU``  ``` | `` <code>I `LOVE` YOU</code>`` | <div class="renderBox">`` I `LOVE` YOU ``</div> |

**Code Blocks 代碼區塊**
