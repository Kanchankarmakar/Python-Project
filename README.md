# Python-Project

import random

class Movie:
    def __init__(self, title, genre):
        self.title = title
        self.genre = genre

class OTTPlatform:
    def __init__(self):
        self.movies = []
        self.queue = []
    
    def add_movie(self, title, genre):
        movie = Movie(title, genre)
        self.movies.append(movie)
    
    def get_movies_by_genre(self, genre):
        return [movie for movie in self.movies if movie.genre.lower() == genre.lower()]
    
    def get_top_10_movies(self):
        return random.sample(self.movies, min(10, len(self.movies)))
    
    def get_recommended_movies(self):
        return random.sample(self.movies, min(5, len(self.movies)))
    
    def add_to_queue(self, movie):
        self.queue.append(movie)
    
    def view_queue(self):
        return self.queue

def print_menu():
    print("---------- OTT Platform ----------")
    print("1. Show list of movies")
    print("2. Show movies by genre")
    print("3. Show top 10 movies")
    print("4. Show recommended movies")
    print("5. Play a movie")
    print("6. View queue")
    print("7. Exit")
    print("----------------------------------")

def print_movies(movies):
    if not movies:
        print("No movies found.")
        return
    
    print("-------- Movie List --------")
    for movie in movies:
        print(f"{movie.title} ({movie.genre})")
    print("---------------------------")

def get_user_choice(prompt, options):
    choice = input(prompt)
    while choice.lower() not in options:
        print("Invalid choice. Please try again.")
        choice = input(prompt)
    return choice

def main():
    platform = OTTPlatform()

    # Adding movies
    platform.add_movie("Avengers: Endgame", "Action")
    platform.add_movie("The Dark Knight", "Action")
    platform.add_movie("Inception", "Sci-Fi")
    platform.add_movie("Pulp Fiction", "Crime")
    platform.add_movie("The Shawshank Redemption", "Drama")
    platform.add_movie("Fight Club", "Drama")
    platform.add_movie("The Matrix", "Sci-Fi")
    platform.add_movie("The Godfather", "Crime")
    platform.add_movie("Interstellar", "Sci-Fi")
    platform.add_movie("Goodfellas", "Crime")   
    platform.add_movie("The Avengers", "Action")
    platform.add_movie("The Lord of the Rings: The Return of the King", "Fantasy")
    platform.add_movie("Gladiator", "Action")
    platform.add_movie("The Lion King", "Animation")
    platform.add_movie("The Dark Knight Rises", "Action")
    platform.add_movie("Forrest Gump", "Drama")
    platform.add_movie("The Departed", "Crime")
    platform.add_movie("The Prestige", "Thriller")
    platform.add_movie("The Silence of the Lambs", "Thriller")
    platform.add_movie("Titanic", "Romance")
    platform.add_movie("Star Wars: Episode V - The Empire Strikes Back", "Sci-Fi")
    platform.add_movie("Schindler's List", "Drama")
    platform.add_movie("The Green Mile", "Drama")
    platform.add_movie("The Revenant", "Adventure")
    platform.add_movie("The Pianist", "Drama")
    platform.add_movie("The Wolf of Wall Street", "Biography")
    platform.add_movie("Jurassic Park", "Adventure")
    platform.add_movie("The Grand Budapest Hotel", "Comedy")
    platform.add_movie("Avengers: Infinity War", "Action")
    platform.add_movie("Saving Private Ryan", "War")
    platform.add_movie("The Departed", "Crime")
    platform.add_movie("The Shining", "Horror")
    platform.add_movie("The Godfather: Part II", "Crime")
    platform.add_movie("Django Unchained", "Western")
    platform.add_movie("La La Land", "Musical")
    platform.add_movie("Inglourious Basterds", "War")
    platform.add_movie("Casablanca", "Romance")
    platform.add_movie("The Notebook", "Romance")
    platform.add_movie("Jaws", "Thriller")
    platform.add_movie("Gone with the Wind", "Drama")
    platform.add_movie("Black Panther", "Action")
    platform.add_movie("The Social Network", "Drama")
    platform.add_movie("Mad Max: Fury Road", "Action")
    platform.add_movie("The Godfather: Part III", "Crime")
    platform.add_movie("A Clockwork Orange", "Crime")
    platform.add_movie("The Truman Show", "Drama")
    platform.add_movie("Avatar", "Action")
    platform.add_movie("Memento", "Mystery")
    platform.add_movie("No Country for Old Men", "Crime")
    platform.add_movie("The Big Lebowski", "Comedy")
    platform.add_movie("The Sixth Sense", "Thriller")
    platform.add_movie("Raiders of the Lost Ark", "Adventure")
    platform.add_movie("Eternal Sunshine of the Spotless Mind", "Drama")
    platform.add_movie("Blade Runner", "Sci-Fi")
    platform.add_movie("The Great Gatsby", "Drama")
    platform.add_movie("The Princess Bride", "Adventure")
    platform.add_movie("2001: A Space Odyssey", "Sci-Fi")
    platform.add_movie("Back to the Future", "Adventure")
    platform.add_movie("Apocalypse Now", "War")
    platform.add_movie("Citizen Kane", "Mystery")
    platform.add_movie("The Exorcist", "Horror")
    platform.add_movie("The Usual Suspects", "Thriller")
    platform.add_movie("The Terminator", "Sci-Fi")
    platform.add_movie("The Breakfast Club", "Comedy")
    platform.add_movie("Rocky", "Drama")
    platform.add_movie("Good Will Hunting", "Drama")
    platform.add_movie("Scarface", "Crime")
    platform.add_movie("The Avengers: Age of Ultron", "Action")
    platform.add_movie("Alien", "Sci-Fi")
    platform.add_movie("American Beauty", "Drama")
    platform.add_movie("The Hateful Eight", "Crime")
    platform.add_movie("Raging Bull", "Biography")
    platform.add_movie("The Hangover", "Comedy")
    platform.add_movie("The Texas Chainsaw Massacre", "Horror")
    platform.add_movie("The Lion King", "Animation")
    platform.add_movie("Whiplash", "Drama")
    platform.add_movie("Indiana Jones and the Last Crusade", "Adventure")
    platform.add_movie("The Wizard of Oz", "Fantasy")
    platform.add_movie("Blade Runner 2049", "Sci-Fi")
    platform.add_movie("The Godfather: Part III", "Crime")
    platform.add_movie("Inglourious Basterds", "War")
    platform.add_movie("Scarface", "Crime")
    platform.add_movie("American Beauty", "Drama")
    platform.add_movie("The Hangover", "Comedy")
    platform.add_movie("The Texas Chainsaw Massacre", "Horror")
    platform.add_movie("The Lion King", "Animation")
    platform.add_movie("Whiplash", "Drama")
    platform.add_movie("Indiana Jones and the Last Crusade", "Adventure")
    platform.add_movie("The Wizard of Oz", "Fantasy")
    platform.add_movie("Blade Runner 2049", "Sci-Fi")




    while True:
        print_menu()

        choice = get_user_choice("Enter your choice: ", ["1", "2", "3", "4", "5", "6", "7"])
        print()  # Print a blank line for readability
        
        if choice == "1":
            print_movies(platform.movies)
        
        elif choice == "2":
            genre = input("Enter the genre: ").lower()
            movies = platform.get_movies_by_genre(genre)
            print_movies(movies)
        
        elif choice == "3":
            top_movies = platform.get_top_10_movies()
            print_movies(top_movies)
        
        elif choice == "4":
            recommended_movies = platform.get_recommended_movies()
            print_movies(recommended_movies)
        
        elif choice == "5":
            movie_title = input("Enter the movie title: ").lower()
            movie = next((movie for movie in platform.movies if movie.title.lower() == movie_title), None)
            if movie:
                print(f"\n{movie.title} is playing...")
                platform.add_to_queue(movie)
                print("Added to the queue.\n")
            else:
                print("Movie not found!\n")
        
        elif choice == "6":
            queue = platform.view_queue()
            if queue:
                print("Continue watching:")
                print_movies(queue)
            else:
                print("Queue is empty.\n")
        
        elif choice == "7":
            break

    print("Thank you for using the OTT platform!")

if __name__ == "__main__":
    main()






####Explanation
Purpose:
The purpose of this project is to simulate an OTT (Over-The-Top) platform, where users can access and interact with a collection of movies. The program allows users to perform various operations such as viewing a list of movies, searching movies by genre, getting the top 10 movies, getting recommended movies, playing a movie, and managing a viewing queue.

Steps:
1. The program begins by creating an instance of the `OTTPlatform` class, which represents the OTT platform.
2. Movies are added to the platform using the `add_movie` method of the `OTTPlatform` class. The movies are stored in a list.
3. The program then enters a loop where it displays a menu of options and waits for the user's choice.
4. The user can choose from the following options:
   - Option 1: Show list of movies - Displays the entire list of movies available on the platform.
 
   - Option 2: Show movies by genre - Prompts the user to enter a genre and displays all the movies in that genre.

 
 

 
   - Option 3: Show top 10 movies - Displays a randomly selected list of the top 10 movies from the platform's collection.

 

  


 - Option 4: Show recommended movies - Displays a randomly selected list of recommended movies from the platform's collection.

 
   - Option 5: Play a movie - Prompts the user to enter the title of a movie and adds it to the viewing queue if it exists in the platform's collection.

 

 

 
   - Option 6: View queue - Displays the current viewing queue.

 
   - Option 7: Exit - Exits the program.

 
5. The program continues to display the menu and prompt for user input until the user chooses to exit.
6. After the user exits the program, a closing message is displayed.





Running the Program:
To run the program, perform the following steps:
1. Ensure that you have Python installed on your system.
2. Save the provided code in a file with a `.py` extension, for example, `ott_platform.py`.
3. Open a terminal or command prompt and navigate to the directory where the file is saved.
4. Run the program by executing the command: `python ott_platform.py`.
5. The program will start and display the menu. Follow the prompts and enter your choices to interact with the OTT platform.
6. After you are done using the program, choose option 7 to exit.




