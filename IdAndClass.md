
# Attributes in Gooba

Attributes define properties and behaviors of elements in Gooba, similar to attributes in traditional HTML. Two of the most important attributes are `id` and `className`. These attributes help you apply styles, reference elements, and structure the page.

## 1. **The `id` Attribute**

The `id` attribute uniquely identifies an element in the Gooba document. It is used when you want to specifically target a single element for styling, scripts, or manipulation.
### Example:

	header = CreateElement("h1", id="main-header")
	header.text = "Welcome to Gooba!"

In this example, the `id` attribute is set to `"main-header"`, meaning this `h1` element can now be uniquely targeted.

You can later use this `id` to apply styles or manipulate the element in Gooba or through JavaScript if necessary.

### Styling by `id`:

	style = CreateStyle()
	style.style("#main-header", { 
		"color": "green", 
		"font_size": "24px" 
	})

This style targets the element with `id="main-header"` and applies a green text color and a font size of 24px.

## 2. **The `className` Attribute**

The `className` attribute (corresponding to the HTML `class` attribute) is used to group elements for styling or JavaScript manipulation. Unlike `id`, which must be unique, multiple elements can share the same `className`, allowing you to apply the same styles or behaviors to many elements.

### Example:

	paragraph = CreateElement("p", className="text-paragraph")
	paragraph.text = "This is a paragraph styled with a class."

In this case, the `className` attribute is set to `"text-paragraph"`, allowing you to target this element along with any other elements that share this class name.

### Styling by `className`:

	style = CreateStyle()
	style.style(".text-paragraph", {  
	    "color": "blue",  
	    "line_height": "1.5"  
	})

This style targets all elements with the `className="text-paragraph"` and applies a blue color and line height of 1.5.

## When to Use `id` vs `className`

-   **Use `id`** when you need to target a single, unique element. Since `id` must be unique within a document, it is best used for specific elements like a header, footer, or unique sections.
    
-   **Use `className`** when you need to apply the same styles or behavior to multiple elements. It’s ideal for grouping elements, such as paragraphs, buttons, or any elements that share common styling.

### Example: Using `id` and `className` Together

	header = CreateElement("h1", id="main-header", className="header-title")
	header.text = "Welcome to Gooba!"

	paragraph = CreateElement("p", className="text-paragraph")
	paragraph.text = "This is a paragraph under the header."

	style = CreateStyle()
	style.style("#main-header", {  
	    "color": "green",  
	    "font_size": "24px"  
	})
	style.style(".text-paragraph", {  
	    "color": "blue",  
	    "font_size": "16px"  
	})
	doc.appendHead(style)
	doc.body(header, paragraph)
	doc.build()

In this example:

-   The `h1` element has both an `id` of `"main-header"` and a `className` of `"header-title"`.
-   The `p` element uses the `className` of `"text-paragraph"`.
-   Styles are applied to both elements using their respective `id` and `className`.

----------

[Lets Get Hand On](LetsGetHandOn.md)
[Styling with Gooba](StylingWithGooba.md)