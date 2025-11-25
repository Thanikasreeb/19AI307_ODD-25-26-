# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:
Implement a system where a Library contains multiple Book objects. Each Book is created inside the Library. Books can't exist independently (Composition).

<img width="450" height="257" alt="image" src="https://github.com/user-attachments/assets/9e54e40e-298b-48fd-92d6-e86852b8286f" />

## AIM:

To demonstrate composition in Java by creating Book objects that exist only within a Library.

## ALGORITHM :
1.	Start the program.
   
2.	Import the necessary package 'java.util'
   
3.	Instantiate a Library object.

4.Read an integer n representing the number of books to add.

5.For each book (repeat n times):

a. Read the book’s title from input.

b. Read the book’s author from input.

c. Call addBook(title, author) on the Library object, which internally creates Book object and adds it to the library’s collection.

6.Call showBooks() on the Library object to display all books and their details.

7.Close the scanner.

8.End the program.

## PROGRAM:
 ```
/*
Program to implement a Composition Concepts in Java
Developed by: Thanika Sree B
RegisterNumber: 212222100055
*/
```

## SOURCE CODE:
```
import java.util.*;

public class CompositionExample {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Library library = new Library();

        int n = sc.nextInt();
        sc.nextLine();

        for (int i = 0; i < n; i++) {
            String title = sc.nextLine();
            String author = sc.nextLine();
            library.addBook(title, author);
        }

        library.showBooks();
        sc.close();
    }
}

class Book {
    private String title;
    private String author;

    public Book(String title, String author) {
        this.title = title;
        this.author = author;
    }

    public String getDetails() {
        return title + " by " + author;
    }
}

class Library {
    private List<Book> books = new ArrayList<>();

    public void addBook(String title, String author) {
        books.add(new Book(title, author));
    }

    public void showBooks() {
        if (books.isEmpty()) {
            System.out.println("No books in the library.");
        } else {
            System.out.println("Books in Library:");
            for (Book b : books) {
                System.out.println("- " + b.getDetails());
            }
        }
    }
}
```

## OUTPUT:


<img width="835" height="432" alt="image" src="https://github.com/user-attachments/assets/33e7cfef-f48a-424e-81d3-4bb8833856e7" />

## RESULT:
Each Book is instantiated and managed inside the Library, showing a strong lifecycle dependency.


