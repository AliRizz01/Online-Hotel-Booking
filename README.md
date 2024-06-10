# Online-Hotel-Booking
My First Semester BS-IT Project
Introduction:
The Hotel Booking System is purposely to allow people to book hotel rooms without any struggles. It is user-friendly with features such as the ability to view which hotels are available or if specific rooms are open for business; the ability to book a room; and the capacity to view previous bookings. The purpose of this system is to ensure that hotel booking is easy and that it takes minimum time. This means that by adopting this system it is easier to access a hotel that suits the user’s needs, and make sure that a room is available during the time they wish to stay; then proceed to book the hotel. Contributing to establishing order when it comes to the booking of rooms in hotels to ensure that everything is in order. There are advantages for users since they can follow their bookings, which is useful on top of everything. In sum, the Hotel Booking System, which has been designed and developed in this work, wants to help people solve the problem of searching the room in a hotel according to customer requirements in an efficient, fast and convenient way.

Objectives:
-> To provide a seamless interface for users to book hotel rooms.
->	To display available hotels and room types in various cities.
->	To store and manage guest information securely.
->	To facilitate the addition of special features like room scenery.
->	To ensure data persistence by saving booking details in a file.

Methodology:
Code Structure
The system is implemented using C++ and consists of various functions to handle different aspects of the booking process:
1. Header Files and Definitions:
->	The necessary header files are included (<iostream>, <string>, <vector>, <cstdlib>, <ctime>, <conio.h>, <fstream>).
->	Color codes for console output are defined for better user experience.
->	Constants for room and scenery prices are defined.
2. Data Structures:
->	Guest: Struct to store guest information.
->	RoomAvailability: Struct to store room availability details.
3. Functions:
->	displaybuilding(): 
The `displaybuilding ()` function in C++ uses `cout` to print an ASCII art representation of a building, forming part of a hotel booking system interface. It first prints blank lines for spacing, then sets the text color to blue, and constructs a building shape with several rows of windows and a central entrance using characters like underscores and pipes. It resets the text color, prints a blue banner with the title "HOTEL BOOKING SYSTEM," and resets the color again, enhancing the console's visual appeal.

->	getRoomAvailability ():
 The `getRoomAvailability () function randomly determines the availability of single and double rooms in a hotel. It first generates a random total number of rooms between 0 and 100. Then, it assigns a random number of these rooms as single rooms. The remaining rooms are designated as double rooms, ensuring that the total number of rooms is accurately divided between single and double room categories.

->	displayAllHotels ():
 The `displayAllHotels () function in C++ iterates through a list of cities, displaying hotels and their room availability for each city. For each city, it initializes an array of hotel names specific to that city, then iterates through these hotels, displaying their names. The function calls getRoomAvailability() to get random room availability for each hotel, displaying the number of available single and double rooms or indicating if booking is full. This provides a comprehensive view of hotel options and their room availability for multiple cities.

->	saveGuestInfo ():
 The saveGuestInfo () function in C++ writes guest information to a file named "guest_info.txt". It appends the guest's details, including CNIC, first and second names, phone number, email, check-in date, stay duration, and number of guests. It also records the number of single and double rooms booked, and the total cost. If scenery is added to the booking, it notes this and calculates the scenery cost based on predefined prices. The function ensures all information is formatted and separated by a line. If the file cannot be opened, it displays an error message in red text.

->	InputGuestInfo ():
The InputGuestInfo () function collects and validates guest information for a hotel booking. It prompts the user to enter details such as CNIC, first name, second name, phone number, email, check-in date, and number of guests. Each input is validated for correct format and type. If an input is invalid, the function prompts the user to re-enter the information. Once all details are correctly entered, it confirms the input and calls the saveGuestInfo() function to save the guest information along with booking details (single rooms, double rooms, total cost, and number of days) to a file..

->	displayBooking():
 The `displayBooking()` function prompts the user to enter their CNIC to view their booking details. It opens the "guest_info.txt" file and searches for a line containing the entered CNIC. If found, it displays the CNIC and the next ten lines of booking details. If the CNIC is not found, it prompts the user to re-enter it. If the file cannot be opened, it displays an error message. This function ensures that users can retrieve their booking information by providing their CNIC.

->	displayHotelsInCity ():
The displayHotelsInCity () function displays a list of hotels in a specified city and allows the user to select a hotel to check room availability. It uses predefined arrays of hotel names for various cities. After displaying the hotels, it prompts the user to choose a hotel by number and validates the input. It then calls getRoomAvailability () to fetch and display the number of available single and double rooms for the selected hotel. If no hotels are available for the specified city, it informs the user accordingly. The function ensures users can view and select hotels based on their availability in different cities.

->	bookRooms ():
The bookRooms () function handles the process of booking hotel rooms based on the availability provided. It prompts the user to select and book single and double bedrooms, ensuring the chosen quantity doesn't exceed availability. Users can opt to add scenery to their rooms, calculating the additional cost if chosen. After confirming the booking details, including the number of days of stay, it computes the total cost and adjusts the availability accordingly. Finally, it prompts the user to input guest information and proceeds to save the booking details using InputGuestInfo (). This function facilitates smooth room booking operations while ensuring data integrity and user interaction.

->	cancelBooking (): 
The cancelBooking () function allows users to cancel a hotel booking by specifying their CNIC (Computerized National Identity Card) number. It reads the booking information from a file (`guest_info.txt`), searches for the CNIC in the file, and if found, skips the next 4 lines to remove the corresponding booking details. It then writes all other lines to a temporary file (`temp.txt`). If the booking is found and canceled successfully, it replaces the original `guest_info.txt` file with `temp.txt`. If the CNIC is not found, it informs the user accordingly. Error handling ensures that file operations are managed properly throughout the cancellation process.

System Features
1.	Displaying Hotels and Room Availability:
The system can display hotels in multiple cities (Lahore, Karachi, Peshawar, Multan, Hyderabad, Swat, Rawalpindi, Islamabad). Each hotel is listed with its room availability. 
Room availability in various cities (Lahore, Karachi, etc.) is dynamically simulated using the rand () function, offering users a realistic view of room availability based on single and double room types.
2.	User Interaction:
	Input Validation: Ensures accurate formatting and integrity of CNICs, phone numbers, and dates to maintain data reliability.
	File Handling: Booking details are securely stored in 'guest_info.txt', ensuring persistent data storage and easy retrieval.
3.	Booking Rooms:
Users can book single or double rooms, customize with optional features like room scenery, and calculate costs based on room type and duration of stay.
4.	Storing and Displaying Guest Information:
Guest details such as CNIC, name, contact information, and check-in dates are stored and can be retrieved from the system, ensuring efficient management of reservations.
Validation
The code includes several validation checks for user input:
1. CNIC format: Ensures the CNIC is in the format 00000-0000000-0.
2. Name format: Ensures names contain only alphabetic characters.
3. Phone number format: Ensures the phone number is in the format 0000-0000000.
4. Date format: Ensures the check-in date is in the format DD-MM-YYYY.
5.	Canceling Bookings:
Users can cancel bookings by providing their CNIC, ensuring flexibility in managing reservations and optimizing room availability for other guests.

Conclusion:
A refined system that enjoys a solid consideration in business and management is the Hotel Booking System, programmed in C++. It includes fundamental features like: Browsing through the hotels which are available; Checking whether a particular room is available or not; Booking a hotel and also keeping track of guest’s records. Using proper archival and record keeping principles, the system guarantees that all transactions done within the system and all the guest details are safely kept in the databases for future reference.
It also improves usability through easy to navigate controls to enhance the experience of all users – the guests and the administrative workers. The major goals and objectives include; Data accuracy and retrieval to enhance on the booking process hence the general satisfaction of the end user. The latter element refers to searching through the accommodation list and creating new rooms, or working with bookings – the system offers a clearly structured interface that aims at optimized performance and clarity. With these features, the Hotel Booking System anticipates the actual needs of the hospitality managers while aiming to provide a user experience that goes beyond the simple booking of hotel rooms and their management.
