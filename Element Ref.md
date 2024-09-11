



# Elements Reference

This page lists all the elements that Gooba supports. These elements can be used to build UIs with Gooba. The list is grouped by function to help you find what you're looking for. An alphabetical list of all elements is provided in the sidebar for easy navigation.


### Element


| Element Name | Description |
|--|--|
| ``doc = Document() doc.body(elements) doc.build()``| Represents the whole page in Gooba, similar to the `<html>` tag in traditional web development. All other elements must be passed in `doc.body()`. |


## Document Metadata

Metadata provides information about the Gooba page, including styles, scripts, and configurations necessary for rendering the UI.

### Methods

|Methods| Description |
|--|--|
| `doc.appendHead()` | Contains metadata, such as the title of the page, script references, and styles, analogous to the `<head>` tag in web development. |
| `doc.title("Page Title")` | Sets the title for the Gooba page, similar to the `<title>` element in HTML.|



---
Use **CreateElement("ElementName")** to create Elements.

## Content Sectioning

These elements are used to structure the content of your Gooba UI. They help in organizing the page layout and defining sections of content.

### Element

| Element Name | Description |
|--|--|
| header | Represents the header section, typically used for logos, navigation, and introductory content, similar to the `<header>` element. |
|footer | Represents the footer section, often containing copyright information, links, or additional navigation, similar to the `<footer>` element.|
|section | Represents a standalone section within the Gooba page, which doesn't have a more specific semantic element, similar to the `<section>` tag in HTML.|
|main | Represents the dominant content of the body, typically used for the main application logic or content.|


## Heading Elements

Gooba supports heading elements that define different sections of your UI. They correspond to levels of hierarchy in your page's content structure.

### Element
| Element Name | Description |
|--|--|
| h1 | Represents the highest level heading, similar to `<h1>` in HTML. |
|h2 | Represents the second level heading, similar to `<h2>` in HTML.|
|h3 | Represents the third level heading, and so on up to `h6`.|
|p|Represents a paragraph. Paragraphs are usually represented in visual media as blocks of text separated from adjacent blocks by blank lines and/or first-line indentation, but HTML paragraphs can be any structural grouping of related content, such as images or form fields.Similar to `<p>` in HTML.|
|ul|Represents an unordered list of items, typically rendered as a bulleted list.Similar to `<ul>` in HTML.|
|ol|Represents an ordered list of items, typically rendered as a numbered list.Similar to `<ol>` in HTML.|
|li|Represents an item list.Similar to `<li>` in HTML.|

## Builtin Classes
|Class Name| Description |
|--|--|
| Document() | Initializes a new Gooba web page. This is the main entry point for creating a Gooba UI. It sets up the document structure and provides methods to add metadata, content, and other elements to the page. Use `Document()` to start building your UI. Example usage: `doc = Document()` initializes a new document. |
| CreateElement() | Creates a new HTML element with a specified tag name. This class allows you to define and structure the content of your page by creating various HTML elements, such as headers, paragraphs, and divs. You can nest elements within each other to build complex layouts. Example usage: `CreateElement("div")` creates a new `div` element. |
| CreateStyle() | Defines CSS styles to be applied to elements on the page. Use `CreateStyle()` to write CSS rules that control the appearance of your elements, such as colors, fonts, and layouts. Styles can be applied directly to elements or included in the document’s head section. Example usage: `CreateStyle("p { color: blue; }")` adds a style rule for paragraphs. |
| CreateImage() | Embeds an image into the page. This class allows you to specify the source of the image and other attributes such as `alt` text. Use `CreateImage()` to include visual content in your UI. Example usage: `CreateImage("path/to/image.jpg", alt="A descriptive text")` inserts an image with a specified source and alternative text. |
| CreateLink() | Creates a hyperlink to another page or resource. Use `CreateLink()` to define anchor elements that allow users to navigate to different parts of your application or external sites. You can specify the URL and link text. Example usage: `CreateLink("https://example.com", "Visit Example")` creates a link to "[https://example.com](https://example.com)" with the text "Visit Example". |
| CreateForm() | Constructs a form element that can contain input fields, buttons, and other form controls. This class is used to create interactive forms for user input and data submission. You can define form actions, method types, and include various form elements like text fields, checkboxes, and submit buttons. Example usage: `CreateForm(action="/submit")` creates a form with a specified action URL. |


[Style Properties](StyleProperties.md) 