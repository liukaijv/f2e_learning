# MARKDOWN语法笔记

## Headers标题

    # h1
    ## h2 
    ### h3 
    #### h4
    ##### h5 
    ###### h6

    h1
    ========
    h2
    --------

## Paragraph 段落

    一行或多行空白

## Emphasis 强调

    *斜体* or _斜体_
    **粗体** or __粗体__
    如果*或_两边有空白，会当作普通符号
    直接输入*或_，使用\*或\_转义

##　List 列表

### Unordered 无序列表

    * 子项
    * 子项
    * 子项

    + 子项
    + 子项
    + 子项

    - 子项
    - 子项
    - 子项

### Ordered 有序列表

    1. 第一行
    2. 第二行
    3. 第三行

### 组合

    * 产品特点
        - 特点1
        - 特点2
        - 特点3
    * 产品功能
        1. 功能1
        2. 功能2
        3. 功能3

## Links 链接（title可选）

    inline-style
    [link text](https://www.google.com "title text")

    reference-style
    [link text][id]
    [id]:https://www.google.com "title text"

    relative reference to a repository file
    [link text](../path/file/readme.text "title text")

    also
    [link text][]
    [link text]: http://www.reddit.com

    email
    <example@example.com>

## Images 图片

    inline-style
    [link text](https://www.google.com "title text")

    reference-style
    [link text][id]
    [id]:https://www.google.com "title text"

## Code and Syntax Highlighting 代码和语法高亮

    `code` or ```code```

    ```html
        <div>Syntax Highlighting</div>
    ```

    ```css
        body{font-size:12px}
    ``` 

    ```javascript
        var s = "JavaScript syntax highlighting";
        alert(s);
    ```

    ```php
        <?php
          echo "hello, world!";
        ?>
    ```

    ```python
        s = "Python syntax highlighting"
        print s
    ```

## Block Code 代码分组(代码区块)

    在该行开头缩进4个空格或一个制表符(tab)

## Hard Line Breaks 换行

    在一行的结尾处加上2个或2个以上的空格，也可以使用</br>标签
    第一行文字，
    第二行文字

## Horizontal Rules 水平分割线

    ***
    * * *
    - - -

## Escape character 转义符(反斜杠)

    Markdown 可以利用反斜杠来插入一些在语法中有其它意义的符号，例如：如果你想要用星号加在文字旁边的方式来做出强调效果，你可以在星号的前面加上反斜杠：
    \*literal asterisks\*
    Markdown 支持以下这些符号前面加上反斜杠来帮助插入普通的符号：
    \反斜杠  `反引号  *星号  _下划线  {}花括号  []方括号  ()括弧  #井字号  +加号  -减号  .英文句 !感叹号

## Additional 补充

    Markdown也支持传统的HTML标签。
    比如一个链接，你不太喜欢Markdown的写法，也可以直接写成<a href="http://www.baidu.com">百度</a>