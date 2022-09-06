# [DOM 2022 Build Dynamic Websites JavaScript Part 1](https://www.udemy.com/course/build-interactive-websites-1/)

## Contents

1. Introduction

- DOM
  - [DOM Living Standard](https://dom.spec.whatwg.org/)
    - > "The DOM" is an API for accessing and manipulating documents.
  - [Introduction to the DOM](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction)
- Web APIs
  - [Window](https://developer.mozilla.org/en-US/docs/Web/API/Window) #interface
    - [Window.document](https://developer.mozilla.org/en-US/docs/Web/API/Window/document)
    - [Window.navigator](https://developer.mozilla.org/en-US/docs/Web/API/Window/navigator)
    - [Window.screen](https://developer.mozilla.org/en-US/docs/Web/API/Window/screen)
    - [Window.location](https://developer.mozilla.org/en-US/docs/Web/API/Window/location)
    - [Window.history](https://developer.mozilla.org/en-US/docs/Web/API/Window/history)
    - [Window.console](https://developer.mozilla.org/en-US/docs/Web/API/Window/console)
  - [Document](https://developer.mozilla.org/en-US/docs/Web/API/Document) #interface
    - [Document.head](https://developer.mozilla.org/en-US/docs/Web/API/Document/head) #HTMLHeadElement
    - [Document.body](https://developer.mozilla.org/en-US/docs/Web/API/Document/body) #HTMLBodyElement #or #HTMLFrameSetElement #deprecated #or null
    - [Document.forms](https://developer.mozilla.org/en-US/docs/Web/API/Document/forms) #HTMLCollection
  - [Navigator](https://developer.mozilla.org/en-US/docs/Web/API/Navigator) #interface
  - [Screen](https://developer.mozilla.org/en-US/docs/Web/API/Screen) #interface
  - [Location](https://developer.mozilla.org/en-US/docs/Web/API/Location) #interface
  - [History](https://developer.mozilla.org/en-US/docs/Web/API/History)
  - [console](https://developer.mozilla.org/en-US/docs/Web/API/console)
- Render Tree
  - [Render-tree Construction, Layout, and Paint](https://web.dev/critical-rendering-path-render-tree-construction/)
  - [Populating the page: how browsers work](https://developer.mozilla.org/en-US/docs/Web/Performance/How_browsers_work)
- CSS
  - [Pseudo-elements](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-elements)

2. JavaScript vs DOM

- Web APIs
  - [Document Object Model (DOM)](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model)
  - Window
    - [Window.open()](https://developer.mozilla.org/en-US/docs/Web/API/Window/open)
    - [Window.close()](https://developer.mozilla.org/en-US/docs/Web/API/Window/close)
  - [setTimeout()](https://developer.mozilla.org/en-US/docs/Web/API/setTimeout)

3. Accessing the DOM

- Web APIs
  - Document #interface
    - [Document.getElementById()](https://developer.mozilla.org/en-US/docs/Web/API/Document/getElementById)
      - returns
        - > An `Element` object describing the DOM element object matching the specified ID, or `null` if no matching element was found in the document.
    - [Document.getElementsByClassName()](https://developer.mozilla.org/en-US/docs/Web/API/Document/getElementsByClassName)
      - returns
        - > A live `HTMLCollection` of found elements.
    - [Document.getElementsByTagName()](https://developer.mozilla.org/en-US/docs/Web/API/Document/getElementsByTagName)
      - returns
        - > A live `HTMLCollection` of found elements in the order they appear in the tree.
    - [Document.querySelector()](https://developer.mozilla.org/en-US/docs/Web/API/Document/querySelector)
      - returns
        - > An `Element` object representing the first element in the document that matches the specified set of CSS selectors, or `null` is returned if there are no matches.
    - [Document.querySelectorAll()](https://developer.mozilla.org/en-US/docs/Web/API/Document/querySelectorAll)
      - returns
        - > A non-live `NodeList` containing one `Element` object for each element that matches at least one of the specified selectors or an empty `NodeList` in case of no matches.
  - [Element](https://developer.mozilla.org/en-US/docs/Web/API/Element) #interface
    - [Interface Element](https://dom.spec.whatwg.org/#interface-element)
  - [HTMLCollection](https://developer.mozilla.org/en-US/docs/Web/API/HTMLCollection) #interface
    - [Interface HTMLCollection](https://dom.spec.whatwg.org/#interface-htmlcollection)
  - [NodeList](https://developer.mozilla.org/en-US/docs/Web/API/NodeList) #interface
    - [Interface NodeList](https://dom.spec.whatwg.org/#interface-nodelist)
- HTML
  - [Getting started with HTML](https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Getting_started)
- Emmet
  - [Cheat Sheet](https://docs.emmet.io/cheat-sheet/)

4. Nodes

- Web APIs

  - [Node](https://developer.mozilla.org/en-US/docs/Web/API/Node) #interface

    - [Node.childNodes](https://developer.mozilla.org/en-US/docs/Web/API/Node/childNodes) #read-only
      - > A live `NodeList` containing the children of the node.
    - [Node.nodeType](https://developer.mozilla.org/en-US/docs/Web/API/Node/nodeType) #read-only

      - > Returns an `unsigned short` representing the type of the node. Possible values are:

        | Name                          | Value |
        | :---------------------------- | :---- |
        | `ELEMENT_NODE`                | `1`   |
        | `ATTRIBUTE_NODE`              | `2`   |
        | `TEXT_NODE`                   | `3`   |
        | `CDATA_SECTION_NODE`          | `4`   |
        | `PROCESSING_INSTRUCTION_NODE` | `7`   |
        | `COMMENT_NODE`                | `8`   |
        | `DOCUMENT_NODE`               | `9`   |
        | `DOCUMENT_TYPE_NODE`          | `10`  |
        | `DOCUMENT_FRAGMENT_NODE`      | `11`  |

    - [Node.nodeName](https://developer.mozilla.org/en-US/docs/Web/API/Node/nodeName) #read-only
    - [Node.nodeValue](https://developer.mozilla.org/en-US/docs/Web/API/Node/nodeValue)

5. Traversing the DOM

- Web APIs

  - Node
    - [Node.parentNode](https://developer.mozilla.org/en-US/docs/Web/API/Node/parentNode) #read-only
      - > A `Node` that is the parent of the current node. The parent of an element is an `Element` node, a `Document` node, or a `DocumentFragment` node.
    - [Node.parentElement](https://developer.mozilla.org/en-US/docs/Web/API/Node/parentElement) #read-only
      - > An `Element` that is the parent element of the current node, or `null` if there isn't one.
    - [Node.previousSibling](https://developer.mozilla.org/en-US/docs/Web/API/Node/previousSibling) #read-only
      - > A `Node` representing the previous sibling of the current node, or `null` if there are none.
    - [Node.nextSibling](https://developer.mozilla.org/en-US/docs/Web/API/Node/nextSibling) #read-only
      - > A `Node` representing the next sibling of the current node, or `null` if there are none.
    - [Node.firstChild](https://developer.mozilla.org/en-US/docs/Web/API/Node/firstChild) #read-only
      - > A `Node`, or `null` if there are none.
    - [Node.lastChild](https://developer.mozilla.org/en-US/docs/Web/API/Node/lastChild) #read-only
      - > A `Node` that is the last child of the node, or `null` is there are no child nodes.
    - [Node.hasChildNodes()](https://developer.mozilla.org/en-US/docs/Web/API/Node/hasChildNodes)
      - returns
        - > A `boolean` value that is `true` if the node has child nodes, and `false` otherwise.
    - [Node.childNodes](https://developer.mozilla.org/en-US/docs/Web/API/Node/childNodes) #read-only
      - A live `NodeList` containing the children of the node.
  - Element

    - [Element.previousElementSibling]() #read-only
      - > A `Element` object, or `null`.
    - [Element.nextElementSibling](https://developer.mozilla.org/en-US/docs/Web/API/Element/nextElementSibling) #read-only
      - > A `Element` object, or `null`.
    - [Element.firstElementChild](https://developer.mozilla.org/en-US/docs/Web/API/Element/firstElementChild) #read-only
      - > An `Element` object, or `null`.
    - [Element.lastElementChild](https://developer.mozilla.org/en-US/docs/Web/API/Element/lastElementChild) #read-only
      - > An `Element` object, or `null`.
    - [Element.children](https://developer.mozilla.org/en-US/docs/Web/API/Element/children) #read-only
      - > An `HTMLCollection` which is a live, ordered collection ... If the element has no element children, then children is an empty list with a `length` of 0.

6. Creating, Removing and Cloning DOM Elements

- Web APIs
  - Document
    - [Document.createElement()](https://developer.mozilla.org/en-US/docs/Web/API/Document/createElement)
      - > A new `HTMLElement` is returned if the document is an `HTMLDocument`, which is the most common case. Otherwise a new `Element` is returned.
  - Node
    - [Node.appendChild(aChild)](https://developer.mozilla.org/en-US/docs/Web/API/Node/appendChild)
      - returns
        - > A `Node` that is the appended child (`aChild`), except ...
    - [Node.insertBefore()](https://developer.mozilla.org/en-US/docs/Web/API/Node/insertBefore)
      - > Returns the added child.
    - [Node.replaceChild()](https://developer.mozilla.org/en-US/docs/Web/API/Node/replaceChild)
      - returns
        - > The replaced `Node`.
    - [Node.removeChild()](https://developer.mozilla.org/en-US/docs/Web/API/Node/removeChild)
    - [Node.cloneNode()](https://developer.mozilla.org/en-US/docs/Web/API/Node/cloneNode)
      - returns
        - > The new `Node` cloned.
    - [Node.textContent](https://developer.mozilla.org/en-US/docs/Web/API/Node/textContent)
      - > A string, or `null`.
  - Element
    - [Element.innerHTML](https://developer.mozilla.org/en-US/docs/Web/API/Element/innerHTML)
      - > A string containing the HTML serialization of the element's descendants.
    - [Element.remove()](https://developer.mozilla.org/en-US/docs/Web/API/Element/remove)
  - HTMLElement
    - [HTMLElement.innerText](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/innerText)
      - > A string representing the rendered text content of an element.

7. Where to next

## Known Issues

1. My document and code are different from the official version.
