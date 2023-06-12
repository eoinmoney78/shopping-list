    Global Variables: The script starts by creating a set of global variables representing various HTML elements on the page. It grabs these elements using their respective IDs (document.getElementById) or tags (document.querySelector). It also sets a variable called isEditMode to false, this will be used to check if the user is currently editing an item.

    displayItems(): This function retrieves the items saved in the local storage and displays them on the webpage. It also checks the state of the User Interface (UI) by calling checkUI().

    onAddItemSubmit(e): This function is the event handler for when the form is submitted. It prevents the form from actually submitting (which would reload the page) using e.preventDefault(). It then gets the value from the input field, validates it, and if it's not an empty string, it adds the item to the DOM and the local storage. Then it clears the input field and checks the UI.

    addItemToDOM(item): This function creates a new li (list item) element, adds the item as its text content, and appends a remove button to it. It then adds this li to the itemList (which is an ul or ol element in the HTML).

    createButton(classes) and createIcon(classes): These functions create a button and an icon with the given CSS classes respectively. The button also has the icon appended to it.

    addItemToStorage(item): This function gets the current list of items from local storage (or an empty array if there are no items), adds the new item to the array, and saves it back to local storage.

    getItemsFromStorage(): This function retrieves the items from the local storage. If there are no items, it returns an empty array.

    onClickItem(e): This function handles the click events on the list items. If the clicked target is a remove button, it removes the item. Otherwise, it switches the form to edit mode for that item.

    setItemToEdit(item): This function switches the form to edit mode for the given item. It changes the submit button text to "Update Item", and pre-fills the input field with the item's text.

    removeItem(item) and removeItemFromStorage(item): These functions remove the item from the DOM and the local storage respectively. They also check the state of the UI.

    clearItems(): This function removes all items from the DOM and the local storage. It also checks the state of the UI.

    filterItems(e): This function hides or shows list items based on the text entered in the filter input field.

    checkUI(): This function hides or shows the clear and filter buttons based on whether there are any items in the list.

    init(): This function sets up the event listeners for the form submit, list item click, clear button click, and filter input field change. It also sets up the initial display of items from local storage and checks the state of the UI.

The init() function is called at the end of the script to kick things off. This script uses event-driven programming, which means it mostly just sits there
