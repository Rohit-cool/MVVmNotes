# MVVMNotes
Room + ViewModel + LiveData + RecyclerView (MVVM) - Notes

 build a note taking app, using the Android Architecture Component libraries (Room, ViewModel, LiveData and LifeCycle), a RecyclerView and Java. 
 The data stored in an SQLite database and supports insert, read, update and delete operations. For this we will follow the official recommendations from the "Guide to App Architecture" 
ViewModels store and manage UI related data, they survive configuration changes and can be used seemlessly by the newly created activity.
LiveData is an observable dataholder and it is life-cycle aware, which means it automatically starts and stops updating the UI-controller at the right times in it's lifecycle.
For the backend of our app  use the "Room Persistence Library", which works as a wrapper around SQLite and helps us reduce boilerplate code by making extensive use of Annotations. Instead of creating an SQLiteOpenHelper, we simply turn Java classes into "entities" to create tables, and use "Data Access Objects" (DAO) to query these tables and make operations on them. Room also provides compile time verification for SQL statements, so we run into fewer runtime exceptions, caused by typos and invalid queries.
 also use a "Repository" class that works as another abstraction layer between the ViewModel and the underlying data model.
Together, this whole structure constitues an "MVVM" (Model-View-ViewModel) architecture, which follows the single responsibility and separation of concerns principles.
