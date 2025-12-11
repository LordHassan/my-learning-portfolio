# MarkDown 進階語法

> ### Table 表格

Example01:

```markdown
code:

| Syntax    | Description |
| --------- | ----------- |
| Header    | Title       |
| Paragraph | Text        |
```

<div class="renderBox">

render:

| Syntax    | Description |
| --------- | ----------- |
| Header    | Title       |
| Paragraph | Text        |

</div>

Example02: 靠左 置中 靠右

```markdown
code:

| Syntax    | Description |   Test Text |
| :-------- | :---------: | ----------: |
| Header    |    Title    | Here's this |
| Paragraph |    Text     |    And more |
```

<div class="renderBox">

render:

| Syntax    | Description |   Test Text |
| :-------- | :---------: | ----------: |
| Header    |    Title    | Here's this |
| Paragraph |    Text     |    And more |

</div>

---

> ### Fenced Code Blocks 圍欄代碼區塊

````
code:

    ```

    function(){
        console.log(Hello world!);
    }

    ```

````

<div class="renderBox">

render:

```
function(){
    console.log(Hello world!);
}
```

</div>

語法高亮:

````
code:

    ```js

    function(){
        console.log(Hello world!);
    }

    ```

````

<div class="renderBox">
    render:

```js
function(){
    console.log(Hello world!);
}
```

</div>

---

> ### Strikethrough 刪除線

```
code:

~~The world is flat.~~
```

<div class="renderBox">

render:

~~The world is flat.~~

</div>

---

> ### Task List 任務清單

    code:

    - [x] Write the press release
    - [ ] Update the website
    - [ ] Contact the media

<div class="renderBox">

render:

- [x] Write the press release
- [ ] Update the website
- [ ] Contact the media
</div>

---

> ### Emoji 表情符號

在大多數情況下，你可以直接從像 [Emojipedia](https://emojipedia.org/) 這類來源複製表情符號並貼到你的文件中。許多 Markdown 應用程式會自動顯示 Markdown 格式文字中的表情符號。你從 Markdown 應用程式匯出的 HTML 和 PDF 檔案應該會顯示表情符號。
也可使用短碼清單: <https://gist.github.com/rxaviers/7360908>

:bulb: 提示：如果你使用靜態網站產生器，務必將 HTML 頁面編碼為 UTF-8。
