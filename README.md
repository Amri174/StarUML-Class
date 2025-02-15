# StarUML
UML diagrams implemented in StarUML for small scale scenarios.

## Ticket Booking System
Diagram Explanation
The Ticket Booking System consists of three main classes:
Ticket: Represents a train ticket.
Passenger: Represents a passenger booking tickets.
TicketBookingSystem: Manages the overall booking process.


## Library Management System
Diagram Explanation
The Library Management System includes four main classes:
Library: Represents the library itself, including its books and members.
Member: Represents library members who borrow books.
Book: Represents books in the library's collection.
Train (shared): Represents train-related data.

## Access Specifiers Description
- Public Access (+)	Accessible outside the class.
- Private Access (-) Accessible only within the class.

## Syntax 
Each class is represented as follows in UML diagrams:
```
ClassName
-----------------
Features/Attributes
-----------------
Functions/Methods
```
## Class Details

### Ticket
#### Attributes:
- +ticket_id: integer: Unique identifier for each ticket.
- +passenger_name: string: Name of the passenger.
- +train_id: integer: Identifier for the train.
- +departure_station: string: Starting station.
- +departure_time: string: Departure time of the train.
- +arrival_time: string: Arrival time at the destination.
- +fare: integer: Fare amount for the ticket.

#### Methods:
- +book(): void: Books a ticket.
- +cancel(): void: Cancels a ticket.
- +display_ticket(): void: Displays ticket details.

### Passenger
#### Attributes:
- +passenger_id: integer: Unique identifier for a passenger.
- +name: string: Passenger's name.
- +phone_number: double: Passenger's phone number.
- +email: string: Passenger's email address.

#### Methods:
- +book_ticket(): void: Allows a passenger to book a ticket.
- +cancel_ticket(): void: Allows a passenger to cancel a ticket.
- +view_booking_history(): void: Displays the booking history of the passenger.

### TicketBookingSystem
#### Attributes:
- +system_id: string: Identifier for the booking system.
- +available_trains: integer: Number of trains available in the system.

#### Methods:
- +display_all_trains(): void: Displays all available trains in the system.
- +search_trains(): void: Searches for specific trains based on criteria (e.g., destination or time).
- +book_ticket(): void, cancel_ticket(): void, and view_booking_history(): void are similar to those in other classes.

### Library
#### Attributes:
- -name: string: Name of the library (private).
- -address: string: Address of the library (private).
- -books: List<Book>: Collection of books in the library (private).
- -members: List<Member>: List of registered members (private).

#### Methods:
- +addBook(book: Book): void, +removeBook(book: Book): void
- +addMember(member: Member): void, +removeMember(member: Member): void
- +checkoutBook(member: Member, book: Book): void
- +returnBook(member: Member, book: Book): void

### Member 
#### Attributes
- -name: string: The name of the library member. This is private and can only be accessed through getter methods.
- -address: string: The address of the member. This is private.
- -phone: string: The phone number of the member. This is private.
- -booksCheckOut: List<Book>: A list of books currently checked out by the member. This is private.
#### Methods
- +getName(): string: Returns the name of the member.
- +getAddress(): string: Returns the address of the member.
- +getPhone(): string: Returns the phone number of the member.
- +getBooksCheckOut(): List<Book>: Returns a list of books currently checked out by the member.
- +checkoutBook(book: Book): void: Allows a member to borrow a book from the library.
- +returnBook(book: Book): void: Allows a member to return a borrowed book to the library.

### Book
#### Attributes
- -title: string: The title of the book. This is private and can only be accessed through getter methods.
- -author: string: The author of the book. This is private.
- -ISBN: string: The unique identifier for the book (International Standard Book Number). This is private.
- -available: boolean: Indicates whether or not the book is available for borrowing. This is private.

#### Methods
- +getTitle(): string: Returns the title of the book.
- +getAuthor(): string: Returns the author of the book.
- +getISBN(): string: Returns the ISBN number of the book.
- +isAvailable(): boolean: Checks if the book is available for borrowing.

### Train
#### Attributes
- +train_id: integer: A unique identifier for each train.
- +departure_station: string: The station where the train departs from.
- +destination_station: string: The station where the train arrives.
- +departure_time: string: The time when the train departs from its starting station.
- +arrival_time: string: The time when the train arrives at its destination.

#### Methods
- +display_schedule(): void: Displays details about train schedules, including departure and arrival times, and stations.
- +check_availability(): void: Checks if a train has available seats or tickets for booking
