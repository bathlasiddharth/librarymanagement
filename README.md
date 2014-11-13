librarymanagement
=================

Academic Project (CS 6360 Database Design)

This project was developed by Siddharth Bathla as a part of his course CS 6360 Database Design. This is a library management website which will be used by librarians. Various constraints were applied for different library functions like book loans, borrower management etc.


PAGES
1)	Homepage (index.php)
This is the main page of the website. From this page, user can go to different pages to perform various functions (search books, check in/checkout books, add new borrowers and pay/update fines). At the bottom of the page, there is a reset button to load the default data in all the tables.

2)	Search Books (searchbooks.php):
From this page, user can search for books by entering any of these information: Book ID, Title, Author, Branch ID or Branch Name. The user can also checkout any book from the search results directly by entering Card No.

3)	Book Loans (bookloans.php):
From this page, user can check in or check out books by entering book and/or card details.

4)	Check In (checkin.php)
From this page, user can check in books by entering book and/or card details like Card No., Borrower Name, Book ID, Book Name, and Branch ID. After entering the details, user can look for appropriate record of book and borrower details that has to be checked in into library.

5)	Check Out (checkout.php)
From this page, user can checkout a book by entering Card No, Book Id and Branch ID. The user will be prompted with an error message if any information entered is wrong. There are few conditions in the checkout policy: 1) borrower can checkout maximum of 3 books. 2) borrower cannot checkout any book if he has a pending fine to be paid.

6)	Manage Borrowers (addborrowers.php)
From this page, user can add new borrowers into the system. The user should enter First Name, Last Name and Address. Phone no. is an optional field. One person can possess only one card, hence no two records having same first name, last name and address can exist in the system. Card number is auto-generated.

7)	Fines (fines.php)
From this page, user can search for any pending fines on any card number. If there is any pending fine on that card number, then user can pay the fine from the same page. A fine can only be paid if all the books have been returned by that borrower. A borrower has to pay all the fine on his card together. 
On this page, there is another feature of updating the fines. Clicking this button will update the fines table. Fines are charged at $0.25/day

8)	Reset (reset.php)
This is a backend page that deletes all entries from all the tables. This page reads commands stored in sqlcommands folder. This file parses *.sql file and executes each command in that file.

9)	Insert Data (insertdata.php)
This is a backend page that inserts default data into the tables. This page reads commands stored in sqlcommands folder and data stored in data folder. This file parses *.sql file and executes each command in that file.

COMMON FUNCTIONS:
CHECKOUT A BOOK
If you know the book and card details:
1)	Go to Book Loans page
2)	Enter Card No., Book ID and Library Branch ID
3)	Click Checkout to checkout the book
If you don’t know the book and card details:
1)	Go to Book Search page
2)	Enter details that you know
3)	Search for appropriate book to checkout and click corresponding checkout button
4)	Enter Card No.
5)	Click checkout to checkout the book
CHECK IN A BOOK
1)	Go to Book Loans page
2)	Enter book and card details
3)	Click check in button
4)	Confirm book details
5)	Click check in to check in the book
ADD BORROWERS
1)	Go to Manage Borrowers page
2)	Enter borrower details (Phone no. is optional)
3)	Click register to add the borrower
4)	Tell borrower his card no. and ask him to remember it
Pay Fines
1)	Go to Fines page
2)	Enter card no. whose fine has to be paid
3)	Click search to check if borrower has to pay any fine
4)	Confirm amount
5)	Click Pay Fine button to pay the fine
Update fine
1)	Go to Fines page
2)	Click ‘Update Fines’ button on the bottom of the page to update fines

Bonus Features:
1)	A static and fixed menu bar on top of every page to make the website intuitive and user friendly
2)	Apart from separate checkout, user can also checkout a book directly from the book search results page.
3)	When users checkout a book and sees that he already has 3 books checked out, then he can return any of his book from the same page
4)	When user tries to checkout a book that is not available in that particular library, then user gets an option to search book in other libraries
5)	When user tries to checkout a particular book and enters some information wrong, an error is shown to user telling what exactly he has entered wrong
6)	When user search for a book, then checkout button is disabled if there is no available copies of that book in library

 Technical Dependencies
Following technologies are used to build this website:
1)	HTML5
2)	PHP 5
3)	CSS
4)	Bootstrap 3.2.0
5)	JavaScript
6)	MySql
