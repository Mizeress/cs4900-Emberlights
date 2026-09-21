# Logical Model

## Updated Conceptual Model
<img width="705" height="572" alt="Conceptual-model" src="https://github.com/user-attachments/assets/a6681f4e-2a24-4cc4-ab71-2d4fecf85aec" />


## Common Logical Model Terms

### Purpose of a Logical Model

A logical data model describes how the data of an application is organized and how different pieces of data are related to each other. It converts the entities and relationships from the conceptual model into tables, attributes, primary keys, and foreign keys. The logical model focuses on the structure of the data without depending on a specific database management system.

### Primary Key

A primary key is an attribute, or a combination of attributes, that uniquely identifies each record in a table. Primary key values must be unique so that each row of the table can be identified individually.

For example, `SongID` is the primary key of the Song table and `PlaylistID` is the primary key of the Playlist table.

### Foreign Key

A foreign key is an attribute in one table that references the primary key of another table. Foreign keys are used to connect tables and maintain relationships between the data.

For example, `GenreName` in the Song table is a foreign key that references `GenreName` in the Genre table.

### Relationships Between Entities

Relationships describe how entities are connected to each other. Common relationship types include one-to-one (1:1), one-to-many (1:M), and many-to-many (M:M).

In this project, one Genre can be associated with many Songs and many Playlists. Songs and Playlists have a many-to-many relationship because one Song may appear in multiple Playlists and one Playlist may contain multiple Songs.

The many-to-many relationship is resolved in the logical model by using the PlaylistSong table.

### Normalization

Normalization is the process of organizing data into separate related tables in order to reduce duplicate data and improve data consistency.

This logical model separates Songs, Genres, and Playlists into individual tables. The many-to-many relationship between Songs and Playlists is also separated into the PlaylistSong table.

---

## Group Conceptual Model

[Emberlights GitHub Repository](https://github.com/AMcGohan/cs4900-EmberLights-Database/tree/main/conceptual_model)

---

## Logical Model

<img width="967" height="247" alt="logical-model" src="https://github.com/user-attachments/assets/71a48dff-dde4-4d44-a7ab-2f23783fc547" />

---

## Logical Model Description

The **Song** table stores information about songs. Each song is uniquely identified by `SongID`. The table also stores the song name, duration, artist, and album. `GenreName` is included as a foreign key because multiple songs can belong to the same genre.

The **Genre** table stores the different music genres used by the application. `GenreName` is the primary key and uniquely identifies each genre.

The **Playlist** table stores information about playlists. Each playlist is uniquely identified by `PlaylistID`. It also contains the playlist name and creation date. `GenreName` is a foreign key referencing the Genre table because one genre can define multiple playlists.

The relationship between Song and Playlist is many-to-many. A song can appear in multiple playlists, and a playlist can contain multiple songs. A relational database cannot directly represent this many-to-many relationship using a single foreign key.

For this reason, the **PlaylistSong** table is used as an associative table. It contains `PlaylistID` and `SongID` as foreign keys. Together, these two attributes form a composite primary key. This prevents the same song from being added to the same playlist more than once.

The resulting logical model reduces duplicated information, preserves the relationships from the conceptual model, and provides a normalized structure that can later be converted into a physical database model.
