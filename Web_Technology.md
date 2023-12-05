# 1. Use of ``<pre>`` and ``<del>`` tags, Image Maps- map, area, attributes of image area.
### Use of `<pre>` and `<del>` Tags:

#### 1. `<pre>` Tag:
The `<pre>` tag in HTML is used to define preformatted text. The text inside a `<pre>` element is displayed in a fixed-width font (usually Courier), and it preserves both spaces and line breaks. This tag is often used when the formatting of text is important, such as displaying code snippets or poetry.

Example:
```html
<pre>
    This   is   some
    preformatted   text.
</pre>
```

#### 2. `<del>` Tag:
The `<del>` tag is used to represent deleted or removed text within a document. Browsers usually render the text with a strikethrough line. It is commonly used in conjunction with the `<ins>` tag, which represents inserted text, to show changes made to a document.

Example:
```html
<p>This is some <del>deleted</del> text.</p>
```

### Image Maps using `<map>`, `<area>`, and Attributes:

#### 3. Image Maps:
An image map is an HTML construct that allows different regions of an image to be clickable, directing users to different URLs. This is achieved using the `<map>` tag along with `<area>` tags to define clickable areas.

Example:
```html
<img src="example.jpg" alt="Example Image" usemap="#exampleMap">
<map name="exampleMap">
    <area shape="rect" coords="0,0,50,50" href="page1.html" alt="Link 1">
    <area shape="circle" coords="100,100,50" href="page2.html" alt="Link 2">
    <area shape="poly" coords="200,0,250,50,200,100" href="page3.html" alt="Link 3">
</map>
```

#### 4. Attributes of `<area>` Tag:
- **shape:** Specifies the shape of the clickable area. Common values are "rect" for rectangle, "circle" for circle, and "poly" for polygon.
- **coords:** Defines the coordinates of the clickable area. The format depends on the shape. For example, for a rectangle: "x1,y1,x2,y2" and for a circle: "x,y,r".
- **href:** Specifies the URL that the link points to when the area is clicked.
- **alt:** Provides alternative text for the area, similar to the alt attribute in the `<img>` tag.

In the example above, three clickable areas are defined on the image with different shapes and coordinates, each linking to a different page.

This comprehensive explanation should cover the details needed for a 10-mark question on the use of `<pre>` and `<del>` tags, as well as image maps using `<map>` and `<area>` tags with their attributes.
# 2. What are the usages of: hover, active and: focus dynamic pseudo classes?

### Usages of `:hover`, `:active`, and `:focus` Pseudo-classes:

#### 1. `:hover` Pseudo-class:
The `:hover` pseudo-class is used to select and style an element when the user hovers over it with the mouse. It is commonly used to enhance the user experience by providing visual feedback, such as changing the color or background of a link when it is hovered.

Example:
```css
a:hover {
    color: blue;
    text-decoration: underline;
}
```

#### 2. `:active` Pseudo-class:
The `:active` pseudo-class is applied when an element is in the process of being activated, typically when a mouse button is held down while the cursor is over the element. This pseudo-class is often used to provide visual feedback during a click, making interactive elements like buttons or links appear pressed.

Example:
```css
button:active {
    background-color: #ffcc00;
    box-shadow: inset 0 0 5px rgba(0, 0, 0, 0.5);
}
```

#### 3. `:focus` Pseudo-class:
The `:focus` pseudo-class is used to select and style an element when it gains focus, typically through user interaction like tabbing through form fields. It is commonly used to provide a visual indicator for users navigating a webpage via keyboard or assistive technologies.

Example:
```css
input:focus {
    border: 2px solid #4CAF50;
    outline: none; /* Remove default focus outline for better styling */
}
```

### Summary of Usages:
- **`:hover`:**
  - Used for styling an element when the user hovers over it.
  - Enhances the user experience by providing visual feedback.

- **`:active`:**
  - Applied when an element is being activated, usually during a click or touch event.
  - Provides visual feedback to indicate an active state.

- **`:focus`:**
  - Used for styling an element when it gains focus, often through keyboard navigation.
  - Aids in improving accessibility and usability for users navigating with keyboards.

By understanding and effectively using these dynamic pseudo-classes, web developers can create more interactive and user-friendly interfaces, improving the overall user experience on their websites.

# 3. cookie in detail

# 4. CSS, what is the meaning of cascading in CSS? Give coding examples of different types of CSS styles?
In CSS, "cascading" refers to the process by which the browser determines which styles to apply to an element when it is affected by multiple style rules. The term "cascading" reflects the order of priority and influence that different style rules have on the final appearance of an element. The cascading process involves a set of rules and mechanisms to resolve conflicts and determine the most specific, applicable styles.

### Specificity and Inheritance:

1. **Specificity:**
   - Specificity is a measure of how specific a selector is in targeting elements. It determines which rule takes precedence when multiple conflicting rules apply to the same element.

   Example:
   ```css
   /* Higher specificity - this style will be applied */
   #specific-element {
       color: red;
   }

   /* Lower specificity - this style will be overridden */
   p {
       color: blue;
   }
   ```

2. **Inheritance:**
   - Inheritance is the process by which certain properties of an element are passed down from its parent to its children. Not all properties are inherited, but those that are will be applied to child elements unless overridden.

   Example:
   ```css
   /* Parent element style */
   div {
       font-family: 'Arial', sans-serif;
   }

   /* Child element inherits font-family from the parent */
   div p {
       /* Inherits 'Arial', sans-serif */
   }
   ```

### Different Types of CSS Styles:

1. **Inline Styles:**
   - Applied directly to an HTML element using the `style` attribute.

   Example:
   ```html
   <p style="color: green; font-size: 16px;">This is a paragraph with inline styles.</p>
   ```

2. **Internal (or Embedded) Styles:**
   - Placed within the `<style>` tag in the `<head>` section of an HTML document.

   Example:
   ```html
   <head>
       <style>
           p {
               color: blue;
               font-size: 18px;
           }
       </style>
   </head>
   <body>
       <p>This is a paragraph with internal styles.</p>
   </body>
   ```

3. **External Styles:**
   - Defined in a separate CSS file and linked to the HTML document.

   Example (style.css):
   ```css
   /* style.css */
   p {
       color: red;
       font-size: 20px;
   }
   ```

   ```html
   <!-- index.html -->
   <head>
       <link rel="stylesheet" type="text/css" href="style.css">
   </head>
   <body>
       <p>This is a paragraph with external styles.</p>
   </body>
   ```

4. **Selector Combinations:**
   - Using combinations of selectors to target specific elements or groups of elements.

   Example:
   ```css
   /* Selects all paragraphs inside a div with class 'container' */
   .container p {
       text-align: center;
   }
   ```

5. **!important Declaration:**
   - Overrides normal cascading rules and gives a style the highest priority.

   Example:
   ```css
   p {
       color: purple !important;
   }
   ```

   Note: The use of `!important` should be minimized, as it can make styles difficult to manage.

Understanding the cascade in CSS is crucial for creating maintainable and predictable stylesheets. It involves considering specificity, inheritance, and the order in which styles are declared and applied to achieve the desired visual presentation on a web page.

# 5. What is the difference between class selector and id selector in CSS?

| Feature                  | Class Selector                            | ID Selector                              |
|--------------------------|-------------------------------------------|-----------------------------------------|
| Syntax                   | Prefixed with a period (`.`)              | Prefixed with a hash/pound (`#`)        |
| Usage                    | Multiple elements can share the same class | Each ID must be unique within the page |
| Example                  | `.example-class { ... }`                  | `#example-id { ... }`                    |
| Specificity             | Lower specificity compared to IDs         | Higher specificity compared to classes |
| Application             | Suitable for styling multiple elements     | Suitable for styling a unique element   |
| JavaScript Interaction  | Can be used multiple times in a document  | Should be unique for each element       |

Explanation:

1. **Syntax:**
   - Class selectors are denoted by a period (`.`) followed by the class name.
   - ID selectors are denoted by a hash/pound (`#`) followed by the ID name.

2. **Usage:**
   - Class selectors can be applied to multiple HTML elements. Multiple elements can share the same class.
   - ID selectors must be unique within the HTML document. Each ID can only be assigned to a single element.

3. **Example:**
   - Class Selector Example: `.highlight-text { color: yellow; }`
   - ID Selector Example: `#header { background-color: blue; }`

4. **Specificity:**
   - Class selectors have lower specificity compared to ID selectors. In the specificity hierarchy, IDs take precedence over classes.

5. **Application:**
   - Class selectors are suitable for styling multiple elements that share common styles.
   - ID selectors are suitable for styling a specific and unique element on a page.

6. **JavaScript Interaction:**
   - Class selectors can be used multiple times in a document, and JavaScript functions can target elements with a specific class.
   - ID selectors should be unique, and JavaScript functions can directly interact with a specific element using its unique ID.

Understanding the differences between class and ID selectors is important for effective and modular CSS styling in web development.


# 6. XML- Introduction, Tree, Syntax, Elements, Attributes, Validation, Viewing. XHTML, Schema, DTD, XML parser, SAX, DOM
### XML (eXtensible Markup Language):

#### Introduction:
XML, or eXtensible Markup Language, is a markup language designed to store and transport data. It provides a flexible and self-descriptive way to structure information using tags, similar to HTML. XML is platform-independent and widely used in various applications, including data interchange between different systems.

#### Tree Structure:
- XML documents have a hierarchical tree-like structure.
- Consists of an element hierarchy with a root element, parent and child elements, and leaf elements.
- Example:
  ```xml
  <bookstore>
      <book>
          <title>XML for Beginners</title>
          <author>John Doe</author>
      </book>
      <book>
          <title>Advanced XML Techniques</title>
          <author>Jane Smith</author>
      </book>
  </bookstore>
  ```

#### Syntax:
- Tags are enclosed in angle brackets, defining elements.
- Elements can have attributes specified within the start tag.
- Opening and closing tags must match.
- Example:
  ```xml
  <person age="30">John Doe</person>
  ```

#### Elements and Attributes:
- **Elements:** Represent the structure and content of data.
  ```xml
  <elementName>Content</elementName>
  ```

- **Attributes:** Provide additional information about elements.
  ```xml
  <elementName attribute="value">Content</elementName>
  ```

#### Validation:
- **Document Type Definition (DTD):** Defines the structure and the legal elements and attributes of an XML document.
  ```xml
  <!DOCTYPE bookstore [
      <!ELEMENT bookstore (book+)>
      <!ELEMENT book (title, author)>
      <!ELEMENT title (#PCDATA)>
      <!ELEMENT author (#PCDATA)>
  ]>
  ```

- **XML Schema Definition (XSD):** Provides a more powerful and flexible way to define the structure of an XML document.
  ```xml
  <xs:element name="bookstore">
      <xs:complexType>
          <xs:sequence>
              <xs:element name="book" type="bookType" minOccurs="0" maxOccurs="unbounded"/>
          </xs:sequence>
      </xs:complexType>
  </xs:element>
  ```

#### Viewing XML:
- XML documents can be viewed in a web browser, text editor, or specialized XML viewer.
- Browsers may apply XSLT (Extensible Stylesheet Language Transformations) to render XML content more human-readable.

### XHTML (eXtensible HyperText Markup Language):

- A stricter and cleaner version of HTML, adhering to XML syntax rules.
- Designed to be compatible with XML tools and browsers.
- Example:
  ```xml
  <html xmlns="http://www.w3.org/1999/xhtml">
      <head>
          <title>XHTML Example</title>
      </head>
      <body>
          <p>This is a paragraph.</p>
      </body>
  </html>
  ```

### XML Parser:

- **SAX (Simple API for XML):** Parses XML documents sequentially, emitting events as it encounters elements. Suitable for large documents.
  
- **DOM (Document Object Model):** Parses the entire XML document and creates a tree structure in memory. Allows for easy traversal and manipulation of the document.

### Conclusion:

XML is a versatile markup language used for representing structured data. It employs a tree-like structure, defines elements and attributes, supports validation through DTD or XSD, and can be viewed in various tools. XHTML is a stricter version of HTML following XML rules. XML parsers, such as SAX and DOM, provide different approaches to processing XML documents in applications. Understanding XML is essential for data interchange and representation in web development and other domains.
# 7. CGI Scripts- Introduction, Environment Variable, GET and POST Methods

# 8. PERL- Introduction, Variable, Condition, Loop, Array, Implementing data structure, Hash, String, Regular Expression, File handling, I/O handling, chop() and chomp() function.
- **Introduction**: Perl is a general-purpose, high-level, interpreted, and dynamic programming language that was developed for system management and text handling. It is popular for its ability to handle regular expressions and network sockets.
    
- **Variable**: In Perl, variables are used to store values. Perl has three types of variables: scalars, arrays, and hashes.
    
- **Condition**: Perl provides several conditional statements such as if, else, elsif, unless, etc. to execute a block of code based on the result of a condition.
    
- **Loop**: Perl provides several loop statements such as for, foreach, while, do-while, etc. to execute a block of code repeatedly.
    
- **Array**: An array is a collection of variables that are of the same data type. In Perl, arrays are used to store a list of values.
    
- **Implementing data structure**: Perl provides several data structures such as arrays, hashes, and linked lists to store and manipulate data.
    
- **Hash**: A hash is a collection of key-value pairs. In Perl, hashes are used to store and retrieve data using keys.
    
- **String**: A string is a sequence of characters. In Perl, strings are used to store text data.
    
- **Regular Expression**: Regular expressions are used to match patterns in text data. Perl has built-in support for regular expressions.
    
- **File handling**: Perl provides several functions to handle files such as open, close, read, write, etc.
    
- **I/O handling**: Perl provides several functions to handle input and output operations such as print, printf, readline, etc.
    
- **chop() and chomp() function**: The chop() function is used to remove the last character of a string, while the chomp() function is used to remove the newline character from the end of a string.

# 9. Implement the following regular expression in Perl:`` **a*bc.**``

# 10. Write a PERL script to implement an associative array.

# 11. JavaScript- Basics, Statements, comments, variable, comparison, condition, switch, loop, break. Object–string, array, Boolean, regular-expression. Function, Errors, Validation.
[[https://www.geeksforgeeks.org/introduction-to-javascript/]]
Single Threaded-> JS is a single threaded which means only one statement is executed at a time.
Interpreter-> Interpreters run through a program line by line and execute each command
# 12. Write a code in java script to find area of a circle. The radius will be input from the keyboard and by clicking on the submit button the area will be displayed on the screen.

# 13. Cookies- Definition of cookies, Create and Store a cookie with example.

Cookie -> A cookie is a piece of data from a website that is stored within a web browser that the website can retrieve at a later time.

Cookies are small pieces of data stored on a user's computer by a web browser while the user is browsing a website. Cookies are used to store information about the user's session, preferences, and other data. They are sent between the web browser and the server to maintain stateful information.
In JavaScript, you can create and store cookies using the `document.cookie` property. Here's a simple example:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Set Cookie Example</title>
</head>
<body>
    <script>
        // Function to set a cookie
        function setCookie(name, value, days) {
            const expires = new Date();
            expires.setTime(expires.getTime() + days * 24 * 60 * 60 * 1000);
            document.cookie = `${name}=${value};expires=${expires.toUTCString()};path=/`;
        }

        // Set a cookie with the name "username" and the value "john_doe" that expires in 1 day
        setCookie("username", "john_doe", 1);

        // Display a message
        alert("Cookie has been set!");
    </script>
</body>
</html>

```
In this example:

- The `setCookie` function is defined to set a cookie with a given name, value, and expiration time in days.
- The `setCookie` function is then called with the parameters "username", "john_doe", and 1 (day).
- The cookie is set using the `document.cookie` property.

# 14. Java Applets- Container Class, Components, Applet Life Cycle, Update method; Parameter passing applet, Applications.

# 15. Client-Server programming In Java- Java Socket, Java RMI and architecture.

# 16. Write a socket program in java to find current time of your PC
  
Certainly! Below is a simple example of a Java socket program to find the current time of your PC. This example uses the `ServerSocket` class to create a server that listens for incoming connections on a specific port and the `Socket` class to handle the communication with the client.

Server (TimeServer.java):
```java
import java.io.IOException;
import java.io.PrintWriter;
import java.net.ServerSocket;
import java.net.Socket;
import java.text.SimpleDateFormat;
import java.util.Date;

public class TimeServer {
    public static void main(String[] args) {
        final int portNumber = 8888;

        try (ServerSocket serverSocket = new ServerSocket(portNumber)) {
            System.out.println("TimeServer is listening on port " + portNumber);

            while (true) {
                Socket clientSocket = serverSocket.accept();
                System.out.println("Connection accepted from " + clientSocket.getInetAddress());

                PrintWriter out = new PrintWriter(clientSocket.getOutputStream(), true);

                // Get the current time and send it to the client
                Date currentTime = new Date();
                SimpleDateFormat dateFormat = new SimpleDateFormat("HH:mm:ss");
                String timeString = dateFormat.format(currentTime);
                out.println("Current time on the server: " + timeString);

                clientSocket.close();
            }
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}
```
Client (TimeClient.java):
```java
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.net.Socket;

public class TimeClient {
    public static void main(String[] args) {
        final String serverAddress = "localhost";
        final int serverPort = 8888;

        try (Socket socket = new Socket(serverAddress, serverPort);
             BufferedReader in = new BufferedReader(new InputStreamReader(socket.getInputStream()))) {

            // Read the current time from the server
            String currentTime = in.readLine();
            System.out.println(currentTime);

        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}

```
Make sure to run the `TimeServer` before running the `TimeClient`. Adjust the server address and port if needed. The `TimeClient` connects to the server and receives the current time from the server.

# 17. Significance of NVT in Telnet, Different types of Operational mode in Telnet

# 18. Distinguish between GET and POST method in HTTP
[[https://www.geeksforgeeks.org/difference-between-http-get-and-post-methods/amp/]]


# 19. Real Time Streaming Protocol, Search Engine, Page Rank Algo.


# 20. Why do we need client side validation when the same can be done at the server side?

Client-side validation and server-side validation serve distinct purposes in web development, and both are important components of a comprehensive validation strategy. Each has its own advantages and considerations. Let's explore the reasons why client-side validation is beneficial, even when server-side validation is in place:

### 1. **User Experience:**
   - **Immediate Feedback:** Client-side validation provides users with immediate feedback as they interact with a form. This enhances the user experience by reducing the time taken to identify and correct errors.

### 2. **Performance:**
   - **Reduced Server Load:** Validating user input on the client side helps offload some of the validation work from the server. This can lead to reduced server load and improved overall application performance.

### 3. **Bandwidth Optimization:**
   - **Minimized Data Transfer:** Client-side validation prevents unnecessary data transfer to the server when users submit a form with invalid data. This can be especially crucial for users with limited bandwidth.

### 4. **Responsiveness:**
   - **Real-time Interaction:** Client-side validation allows real-time interaction without requiring a round-trip to the server. Users can receive instant feedback while filling out a form, creating a more responsive and dynamic interface.

### 5. **Security:**
   - **Front-end Validation for User Convenience:** While server-side validation is crucial for security and should never be bypassed, client-side validation can provide an additional layer of convenience for users. It helps catch common errors before data is sent to the server.

### 6. **Reduced Server-Side Processing:**
   - **Minimized Server Resources:** Client-side validation minimizes the amount of invalid data sent to the server. This reduces the server's need to process and handle invalid data, saving resources for legitimate requests.

### 7. **Enhanced User Interaction:**
   - **Customized Interactivity:** Client-side validation allows developers to implement customized interactive features, such as dynamic error messages, tooltips, or visual cues, improving the overall user interaction.

### 8. **Offline Validation:**
   - **Validations without Server Connectivity:** In scenarios where a user is working offline or has limited connectivity, client-side validation ensures that basic validation checks can still be performed without relying on the server.

### 9. **User Convenience:**
   - **Faster Correction:** Users can correct errors more quickly when they receive immediate feedback on the client side, as opposed to waiting for a server response after form submission.

### 10. **Reduced Server Response Time:**
   - **Quicker Response:** With client-side validation, users experience a quicker response time for simple validation checks, as they don't need to wait for a server round-trip.

While client-side validation provides many benefits, it's essential to note that server-side validation is the primary line of defense for ensuring data integrity and security. Relying solely on client-side validation can expose the application to malicious activities, as client-side scripts can be manipulated or bypassed. Therefore, a well-designed validation strategy includes both client-side and server-side validation to provide a robust and secure user experience.