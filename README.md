   // C++ Program That Uses Structures
   #include <iostream>
   #include <string>
   #include <sstream>
   
   // The <sstream> library allows strings to be converted to streams
   // Stream - used to create, write and read information from files
   
   using namespace std;
  
  struct book_str
    // book_str is a structure type
  { 
    // title and year serve as member types
    string title; 
    int year; 
  } 
    // mine and yours serve as object names
    mine, yours; 
    
  void printbook (book_str book);
  
  int main ()
  {
    string mystr;
    
    // The object name refers back to the member type
    mine.title = "Harry Potter and the Deathly Hallows ";
    mine.year = 2007;
    
    // User input 
    cout << "Enter title: ";
    getline (cin,yours.title);
    cout << "Enter year: ";
    getline (cin,mystr);
    stringstream(mystr) >> yours.year;
    
    cout << "My favorite book is:\n ";
    printbook (mine);
    cout << "And yours is:\n ";
    printbook (yours);
    
  return 0;
  }
  void printbook (book_str book)
  {
    cout << book.title;
    cout << " (" << book.year << ")\n";
  } 

