# Styling with Gooba

In Gooba, you have two main ways to style elements:

1.  **Directly Apply Styles to Elements**
2.  **Apply Styles Through Selectors (Class, ID, or Element Name)**

Let's dive into each method.

## 1. Apply Styles Directly to Elements

You can directly set the styles of an element by manipulating its `style` property. This is similar to inline CSS styling in traditional HTML.

Example:

	paragraph = CreateElement("p", className="paragraph")
	paragraph.text = "This is a paragraph with direct styling."
	paragraph.style = {  
	    "color": "blue",  
	    "font_size": "18px"  
	}
In this example, the paragraph text color is set to blue, and the font size is set to 18px.

## 2. Apply Styles Through Selectors

You can use a separate `CreateStyle()` class to define styles using selectors, which can be based on element names, IDs, or class names. This is similar to how CSS is structured with selectors targeting specific elements.

Example:

	paragraph = CreateElement("p", className="paragraph")
	paragraph.text = "This is a paragraph styled using a class selector."

	style = CreateStyle()
	style.style(".paragraph", {  
	    "color": "red",  
	    "font_weight": "bold"
	})

In this example, all elements with the class `"paragraph"` will have their text color set to red and their font weight set to bold.

## Holding or Bundling Styles in Gooba

There are **three ways** to bundle or apply styles in Gooba:
### 1. **Inline Styles**

This method applies styles directly on the element itself. The style is embedded in the element’s attributes, similar to HTML inline CSS.

Example:

	paragraph.style = {  
	    "color": "blue"  
	}

### 2. **Embedded Styles**

Embedded styles apply within a `<style>` tag in the document head. This allows you to define multiple styles for different elements in one place without repeating them for each element.

Example:

	style = CreateStyle()
	style.style(".paragraph", {  
	    "color": "red",  
	    "font_size": "18px"  
	})
	doc.appendHead(style)  # This appends the styles to the document head

### 3. **External Styles**

With external styles, you save the CSS in a separate file (e.g., `styles.css`) and link it in the document head.

Example:

	style = CreateStyle("styles")  # External stylesheet called "styles.css"
	style.style(".paragraph", {  
	    "color": "red",  
	    "font_weight": "bold"  
	})
	doc.appendHead(style)  # Link the external CSS file in the document head

This creates a file named `styles.css` and applies it to the document. All styles inside this file will be linked to the page as external styles.