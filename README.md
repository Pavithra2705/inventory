## Code Explanation

First, the `json` module is imported so that the program can read and write data in JSON format.

Then a dictionary called `new_book` is created. This dictionary stores the details of the new book that needs to be added to the inventory. It contains the title, author, price, and stock availability of the book.

Next, the program opens the file `inventory.json` using a `with` statement in read mode (`"r"`). The `with` statement is used because it automatically closes the file after the operation is completed.

The function `json.load(file)` is used to read the data from the JSON file and convert it into a Python list. This list is stored in a variable called `inventory`.

After that, the program prints the total number of books currently present in the inventory using `len(inventory)`, which counts the number of items in the list.

Then the new book is added to the inventory list using the `append()` function. This updates the list by including the new book at the end.

Next, the file `inventory.json` is opened again using a `with` statement, but this time in write mode (`"w"`). This allows the program to update the file.

The function `json.dump(inventory, file, indent=4)` is used to write the updated inventory list back into the JSON file. The `indent=4` argument is used to format the JSON data so that it is easier to read.

Finally, the program opens the file again in read mode and loads the updated data into a variable called `updated_inventory`.

A `for` loop is used to go through each book in the inventory list. For every book, the program prints the title, author, and price in the required format using an f-string.
