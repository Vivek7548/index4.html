<!DOCTYPE html>
<html lang="en">

<head>
  <!-- ... (your head content) ... -->
</head>

<body>
  <header id="main-header" class="bg-success text-white p-4 mb-3">
    <div class="container">
      <h1 id="header-title">Item Lister <span style="display:none">123</span></h1>
    </div>
  </header>
  <div class="container">
    <div id="main" class="card card-body">
      <h2 class="title">Add Items</h2>
      <form class="form-inline mb-3">
        <input type="text" class="form-control mr-2">
        <input type="submit" class="btn btn-dark" value="Submit">
      </form>
      <h2 class="title">Items</h2>
      <ul id="items" class="list-group">
        <li class="list-group-item">Item 1</li>
        <li class="list-group-item">Item 2</li>
        <li class="list-group-item">Item 3</li>
        <li class="list-group-item">Item 4</li>
      </ul>
    </div>
  </div>

  <script>
    // Add "Hello" before "Item Lister"
    const headerTitle = document.getElementById("header-title");
    headerTitle.innerText = "Hello " + headerTitle.innerText;

    // Add "Hello" before "Item 1"
    const itemsList = document.getElementById("items");
    const firstItem = itemsList.firstElementChild;
    const helloElement = document.createElement("li");
    helloElement.className = "list-group-item";
    helloElement.innerText = "Hello Item 1";

    // Use DOM manipulation methods
    const parentElement = itemsList.parentElement;
    const lastElementChild = itemsList.lastElementChild;
    const lastChild = itemsList.lastChild;
    itemsList.appendChild(helloElement);
    const firstElementChild = itemsList.firstElementChild;
    const firstChild = itemsList.firstChild;
    const nextSibling = itemsList.nextSibling;
    const nextElementSibling = itemsList.nextElementSibling;
    const previousSibling = itemsList.previousSibling;
    const previousElementSibling = itemsList.previousElementSibling;
    const newElement = document.createElement("div");
    const newTextNode = document.createTextNode("Hello, Text Node!");
    newElement.appendChild(newTextNode);
    itemsList.appendChild(newElement);

    // Set attribute
    newElement.setAttribute("id", "new-element");

    console.log("parentElement: ", parentElement);
    console.log("lastElementChild: ", lastElementChild);
    console.log("lastChild: ", lastChild);
    console.log("firstElementChild: ", firstElementChild);
    console.log("firstChild: ", firstChild);
    console.log("nextSibling: ", nextSibling);
    console.log("nextElementSibling: ", nextElementSibling);
    console.log("previousSibling: ", previousSibling);
    console.log("previousElementSibling: ", previousElementSibling);
  </script>
</body>

</html>
