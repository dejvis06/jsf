# JSF Tutorial

### Versions
- **Java EE 8**
- **GlassFish 5**

### Flow Components
XHTML files in this project serve as the primary view technology in JavaServer Faces (JSF). They are used to define the user interface components and the layout of the application.

**Location**: Typically, XHTML files are placed in the `WEB-INF` directory or within a designated `resources` folder. This ensures they are protected and can be accessed through the JSF framework.

The `greeting.xhtml` file is the welcome page of the JSF application, structured with the following main flow elements:

### Namespaces
The `greeting.xhtml` file declares multiple XML namespaces, which are essential for defining JSF tags and ensuring proper functionality:

- **`xmlns="http://www.w3.org/1999/xhtml"`**: Declares the document as an XHTML file.
- **`xmlns:h="http://xmlns.jcp.org/jsf/html"`**: Imports the HTML tag library for JSF, enabling the use of `h:` prefixed tags.
- **`xmlns:f="http://xmlns.jcp.org/jsf/core"`**: Imports the core JSF tag library, enabling `f:` prefixed tags for functions like conversion and validation.

### `<h:body>`

A managed bean in JavaServer Faces (JSF) is a Java bean managed by the JSF framework. It serves as the backend logic for handling requests and managing application state.

In the provided JSF file:

- `#{userNumberBean}` refers to a managed bean named `userNumberBean`. This managed bean is responsible for handling the user's input and managing the state related to the user's number guessing game.

- `#{userNumberBean.minimum}` and `#{userNumberBean.maximum}` are expressions accessing properties of the `userNumberBean` managed bean. These properties likely define the minimum and maximum values for the number guessing game.

- `#{userNumberBean.userNumber}` is an expression binding the value of the `<h:inputText>` component to a property named `userNumber` in the `userNumberBean` managed bean. This allows the entered user number to be stored in the managed bean.

- The `<f:validateLongRange>` component inside the `<h:inputText>` tag validates that the entered number falls within the specified range, which is defined by the `minimum` and `maximum` properties of the `userNumberBean` managed bean.

- Upon clicking the "Submit" button (`<h:commandButton>`), the action defined as "response" is triggered. This action navigates to the page `response.xhtml`

- `<h:message>` displays any validation errors related to the `<h:inputText>` component. It's associated with the input field using the `for` attribute.

The managed bean `userNumberBean` encapsulates the business logic related to the number guessing game, handling user input validation, and managing the game state.
