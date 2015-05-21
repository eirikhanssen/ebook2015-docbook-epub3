# ebook2015-docbook-epub3
guides and tools for tagging a engilsh/chinese manuscript to docbook and later epub3 conversion

## Docbook
For this project we're tagging the manuscript using Docbook 5.1 http://www.docbook.org/tdg51/en/html/docbook.html

### Docbook markup used

#### Paragraphs, sections and titles
If a title applies to several element children such as para, orderedlist, itemized list, table etc,
wrap in a section element with the first element child a title element.

##### Example: section with multiple content
```
<section>
    <title>The first section</title>
    <para>Just a paragraph.</para>
    <orderedlist>
        <listitem>
            <formalpara>
                <title>First list item in the ordered list</title>
                <para>
                    <mediaobject>
                        <imageobject>
                            <imagedata fileref="figs/fig1.svg" format="svg"/>
                        </imageobject>
                    </mediaobject> This formalpara has a title and a mediaobject containing a
                    graphic figure. </para>
            </formalpara>
        </listitem>
        <listitem>
            <para>Second list item</para>
        </listitem>
    </orderedlist>
    <para>Another para</para>
</section>
```

Regular paragraphs are marked up using the ```<para>...</para>``` element.

#### Formalpara
Formalpara is used to represent one paragraph that is associated with one title
- http://www.docbook.org/tdg51/en/html/formalpara.html

##### Example: formalpara
```
<formalpara>
  <title>This Paragraph Has a Title</title>
  <para>This is a test.  This is only a test.  
    Had this been a real example, it would have made more sense.  Or less.
  </para>
</formalpara>
```
