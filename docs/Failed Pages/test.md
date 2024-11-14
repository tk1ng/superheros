---
title: Test
deprecated: false
hidden: false
metadata:
  robots: index
---

# Adding category links

The last thing we have to do is link the T-shirt to the clothing category. For that we can use a categories element:

```xml Example
<item>
  <id>TSH0123</id>
  <name>Tweakwise T-Shirt</name>
  ...
  <attributes>
    ...
  </attributes>
  <categories>
    <categoryid>234</categoryid>
  </categories>
</item>
```

We added a categories element with ID 234. This is the id of the category 'Clothing' that we created in [chapter 3](doc:generate-an-xml-feed#3-adding-categories).

# Full example

```xml tweakwise-feed.xml
<?xml version="1.0" encoding="utf-8"?>
<tweakwise>
  <items>
    <item>
      <id>TSH0123</id>
      <name>Tweakwise T-Shirt</name>
      <price>24.99</price>
      <stock>10</stock>
      <brand>Tweakwise</brand>
      <groupcode>SHOE-GROUP1</groupcode>
  		<image><![CDATA[https://codesandboxdemostorage.blob.core.windows.net/codesandboxdemostorage/products/tshirt-blauw.jpg]]></image>
  		<url><![CDATA[https://3zbfu.csb.app/#twn|?tn_q=tweakwise%20t-shirt%20blue]]></url>
      <attributes>
        <attribute>
          <name>Size</name>
          <value>Medium</value>
        </attribute>
        <attribute>
          <name>Color</name>
          <value>Blue</value>
        </attribute>
      </attributes>
      <categories>
        <categoryid>234</categoryid>
      </categories>
    </item>
  </items>
</tweakwise> 
```

# Import

In **Tweakwise App \> Connectivity \> Tasks** you should create a new import task with Import type set to **Import items only**.

Make sure this task is executed **after**the **category** import task, using the task chaining option. This is necessary because the product import has a dependency on the category import.

# Good to know

- If you don't have a basic understanding of XML, we recommend reading [XML for the uninitiated](https://support.microsoft.com/en-us/office/xml-for-the-uninitiated-a87d234d-4c2e-4409-9cbc-45e4eb857d44).
- This tutorial will guide you in generating a feed in any programming language or tool, as long as you know how to write text to a file using that language or tool. It will also help you manually create a feed if needed.
- To increase readability, the examples contain different levels of <Glossary>indentation</Glossary> and newlines. This is not required in your feed. Removing tabs and newlines can make the feed size smaller and have impact on the performance of the import.
- It is best practice to apply [CDATA sections](https://www.tutorialspoint.com/xml/xml_cdata_sections.htm) to all fields containing text. For example, image and url elements usually contain characters like an ampersand \(&\). To increase readability in this guide we omit this from some elements.