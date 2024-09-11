
## Let’s Get Hands-On with GooBa

### 1. **Understand the Code**

When you open the `main.py` file, you will see a simple script that demonstrates how to create an Web Page using GooBa. Below is the content of the file:

	from GooBa import Document, CreateElement

    # Create a new document
    doc = Document()
    
    # Create an h1 element for the heading
    text = CreateElement("h1")
    text.text = "This is a Heading"
    
    # Create a p element for a paragraph
    p = CreateElement("p")
    p.text = "This is a paragraph."
    
    # Add these elements to the document body
    doc.body(text, p)
    
    # Set the document title
    doc.title("Page Title")
    
    # Build the final HTML document
    doc.build()


### **Code Breakdown:**

1.  **Imports**:
    
    -   The script starts by importing two classes from GooBa: `Document` and `CreateElement`.
    -   `Document` represents the Web Page, while `CreateElement` allows you to create various Elements such as headings, paragraphs, lists, etc.
2.  **Creating the Document**:
    
    -   The `Document()` class is instantiated to create a new Web Page. This `doc` object will hold all the elements and content we will add.
3.  **Creating Elements**:
    
    -   We create two Elements using `CreateElement`:
        -   `h1`: A heading tag created by `CreateElement("h1")`.
        -   `p`: A paragraph tag created by `CreateElement("p")`.
    -   These elements are then assigned text using the `.text` attribute.
4.  **Adding Elements to the Document**:
    
    -   Both the heading (`h1`) and the paragraph (`p`) are added to the document body using the `doc.body()` method.
5.  **Setting the Document Title**:
    
    -   The `doc.title()` method is used to set the title of the document, which will appear in the browser tab when the page is opened.
6.  **Building the Document**:
    
    -   The final step is calling `doc.build()` to generate the actual HTML file. This will typically save an HTML file to an `output` directory.
### 2. **Running the Code**

Once you understand how the code works, it's time to see the output in action.

#### Steps to Execute:

1.  **Run the Script**:
    
    Open your terminal and run the `main.py` file using the following command:

		python main.py

	This will execute the script and generate an HTML file.
    
-   **Locate the Output**:
    
    After running the script, GooBa will generate an HTML file, typically saved in an `output` directory. Open this file in your web browser to see the rendered page.
    
-   **Modifying the Web Page**:
    
    To deepen your understanding, try modifying the code. For example, add more HTML elements like `h2` or `div` and observe how they affect the structure of your document.
    
    Here's an example where we add a subheading (`h2`):
    
		h2 = CreateElement("h2") 
		h2.text = "This is a Subheading" 
		doc.body(text, h2, p)
Run the script again to see the changes!

##  Elements and Their Usages in GooBa

Now, let's dive into some of the core Elements you'll frequently use in GooBa and how you can create and manipulate them.

### 1. **Headings (`h1` to `h6`)**

Headings are an essential part of structuring your Web Page. They define various levels of importance in your content, from `h1` (the highest level) to `h6` (the lowest level).

#### **Usage**: Headings are used to define the structure and importance of content on a webpage.

Here’s how you create headings in GooBa:

	from GooBa import CreateElement 

	# Create h1 element
	heading1 = CreateElement("h1") 
	heading1.text = "Main Heading" 

	# Create h2 element
	heading2 = CreateElement("h2") 
	heading2.text = "Subheading" 

	# Adding the headings to the document body
	doc.body(heading1, heading2)

	# Build the final document
	doc.build()

----------
### 2. **Paragraph (`p`)**

Paragraphs are used to display blocks of text on a webpage. In GooBa, you can create paragraph elements easily.

#### **Usage**: Use paragraphs to represent blocks of text.

Here’s how you can create and add a paragraph:

	from GooBa import CreateElement 

	# Create a paragraph element
	paragraph = CreateElement("p")
	paragraph.text = "This is a paragraph of text."

	# Adding the paragraph to the document body
	doc.body(paragraph)

	# Build the document
	doc.build()

This will render a basic paragraph on the page.

----------
### 3. **A Division (`div`)**

The `div` element is one of the most commonly used elements in Web Page. It acts as a container to group multiple elements together and helps in structuring the layout.

#### **Usage**: Div elements are used to group content, making it easier to apply styles, positioning, and layout properties.

Let’s create a `div` that contains two paragraphs:

	from GooBa import CreateElement 

	# Create two paragraph elements
	paragraph_1 = CreateElement("p") 
	paragraph_1.text = "This is the first paragraph."

	paragraph_2 = CreateElement("p") 
	paragraph_2.text = "This is the second paragraph."

	# Create a div container and append the paragraphs to it
	container = CreateElement("div")
	container.appendChild(paragraph_1, paragraph_2)

	# Add the div container to the document body
	doc.body(container)

	# Build the final document
	doc.build()

This will result in two paragraphs being grouped inside a `<div>` element.

----------
### 4. **Unordered List (`ul`) and List Items (`li`)**

Unordered lists (`ul`) are used to create bullet point lists. Each item in the list is represented by an `li` element.

#### **Usage**: Create bullet point lists to represent collections of items.

Here’s how you can create an unordered list in GooBa:

	from GooBa import CreateElement 

	# Create a ul element (unordered list)
	ul = CreateElement("ul")

	# Create list items and append them to the ul
	li1 = CreateElement("li")
	li1.text = "First item"
	ul.appendChild(li1)

	li2 = CreateElement("li")
	li2.text = "Second item"
	ul.appendChild(li2)

	li3 = CreateElement("li")
	li3.text = "Third item"
	ul.appendChild(li3)

	# Add the unordered list to the document body
	doc.body(ul)

	# Build the final document
	doc.build()

This will render a list with three bullet points.

----------

### 5. **Ordered List (`ol`) and List Items (`li`)**

Ordered lists (`ol`) are used to create numbered lists. Each item in the list is represented by an `li` element, but unlike unordered lists, ordered lists use numbers (1, 2, 3, etc.).

#### **Usage**: Create numbered lists to represent ordered items.

Here’s how you can create an ordered list in GooBa:
	from GooBa import CreateElement

	# Create an ol element (ordered list)
	ol = CreateElement("ol")

	# Create list items and append them to the ol
	li1 = CreateElement("li")
	li1.text = "Step 1: Install GooBa"
	ol.appendChild(li1)

	li2 = CreateElement("li")
	li2.text = "Step 2: Write your first component"
	ol.appendChild(li2)

	li3 = CreateElement("li")
	li3.text = "Step 3: Build your web page"
	ol.appendChild(li3)

	# Add the ordered list to the web page body
	doc.body(ol)

	# Build the final web page
	doc.build()

This will generate a numbered list like:

1.  Step 1: Install GooBa
2.  Step 2: Write your first component
3.  Step 3: Build your web page

----------


### 6. **Putting It All Together**

Now that you know how to create basic elements, let’s combine headings, paragraphs, unordered lists, and ordered lists inside a `<div>` container to build a more complex web page:

	from GooBa import Document, CreateElement

	# Create a new web page
	doc = Document()

	# Create a div container
	container = CreateElement("div")

	# Add a heading
	heading = CreateElement("h1")
	heading.text = "Welcome to My Page"
	container.appendChild(heading)

	# Add a paragraph
	paragraph = CreateElement("p")
	paragraph.text = "This page demonstrates a basic structure using GooBa."
	container.appendChild(paragraph)

	# Create an unordered list
	ul = CreateElement("ul")
	items = ["Learn HTML", "Explore CSS", "Master JavaScript"]

	# Add list items to the ul
	for item in items:
	    li = CreateElement("li")
	    li.text = item
	    ul.appendChild(li)

	# Append the unordered list to the container
	container.appendChild(ul)

	# Create an ordered list
	ol = CreateElement("ol")
	steps = ["Install GooBa", "Write your first component", "Build your web page"]

	# Add list items to the ol
	for step in steps:
	    li = CreateElement("li")
	    li.text = step
	    ol.appendChild(li)

	# Append the ordered list to the container
	container.appendChild(ol)

	# Add the container to the web page body
	doc.body(container)

	# Set the web page title
	doc.title("My GooBa Page")

	# Build the web page
	doc.build()
