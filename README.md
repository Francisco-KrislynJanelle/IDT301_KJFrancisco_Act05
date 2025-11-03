1. How did you implement CRUD using SQLite?

To implement CRUD with SQLite, I created a database helper class that extends SQLiteOpenHelper. Inside this class, I wrote functions for inserting, reading, updating, and deleting data. When the user creates a note, I use the insert() method to save it in the database. To display notes, I query the database and show the results in a RecyclerView using an adapter. For editing a note, I call the update() method using the note’s ID so only that specific record changes. And for deleting, I use the delete() method and also reference the note ID. This setup allowed the app to manage notes smoothly.

2. What challenges did you face in maintaining data persistence?

One challenge I faced was making sure the data stayed in the app even after closing it. At first, the notes weren’t saving properly because I didn’t manage the database connection correctly. I fixed this by handling the SQLite helper properly and making sure the database was opened and closed at the right time. Another challenge was updating the note list in real time. Sometimes the changes didn’t appear right away, so I used notifyDataSetChanged() to refresh the RecyclerView whenever I added, edited, or deleted a note.

3. How could you improve performance or UI design in future versions?

To improve performance, I plan to use the Room database instead of raw SQLite because Room is easier to maintain and works better with Android components like LiveData. I also want to run database tasks in the background so the app doesn’t lag, especially if there are many notes. For the UI, I would like to use more Material Design elements, add search and filter features for easier note management, and include a dark mode option to make the app more modern and user-friendly.
