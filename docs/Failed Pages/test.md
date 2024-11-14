---
title: Test
deprecated: false
hidden: false
metadata:
  robots: index
---
If you want to transfer a large amount of product information between your platform and Tweakwise, you can use a specially formatted file to import that data. Tweakwise uses the [XML](https://www.tutorialspoint.com/xml/index.htm) format to perform this task. This is called the XML feed.

In this guide, we'll build a **seperate products feed** together:

- Basic structure
- Adding items
- Adding attributes to items
- Adding category links to items
- Import the feed

You can view the full example feed [at the bottom of the page](#full-example).

> 💡 Tip
> 
> The recommended method to get your product data into Tweakwise is by generating a feed with products and categories combined. To learn more, go to [Create an XML feed to import your catalog data in Tweakwise](https://docs.tweakwise.com/docs/generate-an-xml-feed).

# Basic structure

Every XML document must have a root element. Our root element is 'tweakwise' and we'll open it with an opening tag `<tweakwise>`. Here's how that looks.

```xml Example
<?xml version="1.0" encoding="utf-8"?>
<tweakwise>
  <items>
    <!-- -->
  </items>
</tweakwise>
```

# Adding items

Now we will add all our items (i.e. products, content or articles).

## Products

For each product we have to write an 'item' element. An item has the following required properties:

[block:parameters]
{
  "data": {
    "h-0": "Property",
    "h-1": "Required",
    "h-2": "Type",
    "h-3": "Max length",
    "h-4": "Description",
    "0-0": "id",
    "0-1": "yes",
    "0-2": "alphanumeric",
    "0-3": "100",
    "0-4": "A <<glossary:unique identifier>>",
    "1-0": "name",
    "1-1": "yes",
    "1-2": "alphanumeric",
    "1-3": "500",
    "1-4": "The item name",
    "2-0": "price",
    "2-1": "yes",
    "2-2": "decimal",
    "2-3": "\\-",
    "2-4": "The item price.",
    "3-0": "stock",
    "3-1": "yes",
    "3-2": "numeric",
    "3-3": "\\-",
    "3-4": "The current available stock.",
    "4-0": "brand",
    "4-1": "no",
    "4-2": "alphanumeric",
    "4-3": "250",
    "4-4": "The item brand",
    "5-0": "groupcode",
    "5-1": "no",
    "5-2": "alphanumeric",
    "5-3": "100",
    "5-4": "Code used to group products related to each other, this field is necessary if the grouping is used for your lister pages.  \nNot supported in Tweakwise JS.",
    "6-0": "image",
    "6-1": "no\\*",
    "6-2": "alphanumeric",
    "6-3": "500",
    "6-4": "the main image <<glossary:URL>>.",
    "7-0": "url",
    "7-1": "no\\*",
    "7-2": "alphanumeric",
    "7-3": "500",
    "7-4": "a <<glossary:URL>> to the item page."
  },
  "cols": 5,
  "rows": 8,
  "align": [
    "left",
    "left",
    "left",
    "left",
    "left"
  ]
}
[/block]


\* In case of Tweakwise JS, these are recommended.

Let's create an XML element for our Tweakwise T-Shirt:

```xml Item XML sample
<item>
  <id>TSH0123</id>
  <name>Tweakwise T-Shirt</name>
  <price>24.99</price>
  <stock>10</stock>
  <brand>Tweakwise</brand>
  <groupcode>SHOE-GROUP1</groupcode>
  <image><![CDATA[https://codesandboxdemostorage.blob.core.windows.net/codesandboxdemostorage/products/tshirt-blauw.jpg]]></image>
  <url><![CDATA[https://3zbfu.csb.app/#twn|?tn_q=tweakwise%20t-shirt%20blue]]></url>
</item>
```
```xml tweakwise-feed.xml
<?xml version="1.0" encoding="utf-8"?>
<tweakwise>
  <categories>
    <category>
      <categoryid>1</categoryid>
      <name>root</name>
      <rank>0</rank>
    </category>
    <category>
      <categoryid>234</categoryid>
      <name>Clothing</name>
      <rank>1</rank>
      <parents>
        <categoryid>1</categoryid>
      </parents>
    </category>
    <category>
      <categoryid>567</categoryid>
      <name>Accessories</name>
      <rank>2</rank>
      <parents>
        <categoryid>1</categoryid>
      </parents>
    </category>
  </categories>
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
    </item>
    
```

## 

# Adding attributes

Of course you'd want to add more information about the item so Tweakwise can use those properties for search. 

[block:parameters]
{
  "data": {
    "h-0": "Property",
    "h-1": "Type",
    "h-2": "Max length",
    "h-3": "Description",
    "0-0": "name",
    "0-1": "alphanumeric",
    "0-2": "100",
    "0-3": "The attribute name.  \n**Note**: this field cannot not contain HTML.",
    "1-0": "value",
    "1-1": "alphanumeric",
    "1-2": "400",
    "1-3": "The attribute value."
  },
  "cols": 4,
  "rows": 2,
  "align": [
    "left",
    "left",
    "left",
    "left"
  ]
}
[/block]


For a T-shirt you probably want the color and size. Let's add them in an attributes element:

```xml Example
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
</item>
```

We added an attributes element containing multiple attribute elements. Each attribute element contains a name and a value.

> 📘 Multiple attribute values
> 
> You can add multi-value attributes in separate <attribute> elements with the same name but different values.
> 
> ```xml
> <attributes>
>   <attribute>
>     <name>Color</name>
>     <value>Blue</value>
>   </attribute>
>   <attribute>
>     <name>Color</name>
>     <value>Red</value>
>   </attribute>
> </attributes>
> ```

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

In **Tweakwise App > Connectivity > Tasks** you should create a new import task with Import type set to **Import items only**.

Make sure this task is executed **after**the **category** import task, using the task chaining option. This is necessary because the product import has a dependency on the category import.

# Good to know

- If you don't have a basic understanding of XML, we recommend reading [XML for the uninitiated](https://support.microsoft.com/en-us/office/xml-for-the-uninitiated-a87d234d-4c2e-4409-9cbc-45e4eb857d44).
- This tutorial will guide you in generating a feed in any programming language or tool, as long as you know how to write text to a file using that language or tool. It will also help you manually create a feed if needed.
- To increase readability, the examples contain different levels of <<glossary:indentation>>>> and newlines. This is not required in your feed. Removing tabs and newlines can make the feed size smaller and have impact on the performance of the import.
- It is best practice to apply [CDATA sections](https://www.tutorialspoint.com/xml/xml_cdata_sections.htm) to all fields containing text. For example, image and url elements usually contain characters like an ampersand (&). To increase readability in this guide we omit this from some elements.