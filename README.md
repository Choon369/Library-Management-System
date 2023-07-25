# Library-Management-System
editdata(void) :-
This is a simple function which enables the user to edit 
information of books which are already present in the 
system.First of all the screen is cleared by using 
system("cls"), here we have used gotoxy() function which lets 
us to print a message at any position in the screen according 
to our choice. Though we gave to specify the co-ordinates 
where we want to print.The program asks for the book id, to 
find the book from directory. For finding we use fopen, this 
opens the ".dat" file in which data is stored and it also finds 
the specified data as "rb+" command has also been used.A 
file with the DAT file extension is usually a generic data file 
that stores information specific to the applicationit refers to. 
Sometimes you'll find them by themselves but often they're 
with other configuration files like DLL files. Then comes the 
roll of "while" & "if" function to filter the others expect 
specified one. If no Book id matches with the inputed id then 
"No record found" is displayed else the user will be asked to 
enter new "name", "Auhor","quantity", "price", "rackno"."The 
record is modified" message gets displayed after
modification and the user is asked if he wants to modify 
more books, if you enter ‘Y’ it repeats the whole function 
again otherwise 'N' exits the editdata function.
checkid(int t) :-
This function checks weather the book exits in the library or 
not. The function takes input in the variable 't' then 
compares it with the book id, if return 0 then, book exists or 
return 1 if book doesn't exists.
getdata():-
This function asks for data input from the user. This function 
askes for the book id first and it compares it with all the 
book ids already present in the library, if present "The book 
id already exists" else it will ask the user to enter "Book 
name", "Author", "Quantity", "price", "rackno".As the name 
suggests this function only takes input from the user for any 
new entry.
deletebooks () :-
This function is used to delete a record from the file 
fp.Further, fopen function is used to open the existing file 
and then “rb+” is called to open the binary file in read and 
write mode.
Then the rewind function is used to set the file pointer to 
the beginning of the file.
viewbooks () :-
The viewbook function is used to view the list of books and 
other fields and details entered by the user.
It opens the file in reading mode done using the “rb” in the 
file open statement of fp. File fp is then closed and the 
function is returned.
returnfunc(void) :-
This function is actually a loop that just makes the user to 
get back to the main menu by calling the mainmenu function 
until the character given isn’t 13 which is use to only use the 
“enter” button.
AddBooks:-
This function is used to add a book in a specific category and 
then it calls the main menu function where you can enter 
the various details of the book like book-id,bookname,etc.After that it calls the getdata() function which 
writes the whole book information into a binary .dat file 
which is in read and write mode.
Searchbooks():-
This function has two options i.e to search by Book-id or 
Book-name.When you chose one of the options it opens the 
binary file where all the book data is stored and then seeks 
the Book-id or Book-name in the file and returns the 
following data of the books which was later on entered 
during add books.If a book isn’t found while seeking it in the 
file then it show that no book is found.
It calls itself at last to search any another book otherwise it 
goes back to the mainmenu() function.
Password():-
This function allows the user to input password to run the 
application after it is opened. You can’t change the 
password upon running the application.
Issuerecord():-
this function helps to work like the number of books are 
issued or returning or renewing a book or later fine charge 
record etc.
t(void):-
This function gets the current date and time and 
displays in the menu.
Issuebooks():-
Opens a new menu where admin can issue, view , 
search ,and remove issued books .At first ,it checks the 
availability and no . of unissued book . Gets the issued 
date and due date and register the book in student’s 
name. Further one can search and traverse the issued 
books.Also creating a temp folder it help admin to 
remove the issued books. 
