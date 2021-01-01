# dataStore
A file-based key-value data store that supports the basic CRD (create, read, and delete) operations. The data store can be exposed as a library to clients that can instantiate a class and work with the data store.
This data store is meant to be used as a local storage for one single process on one laptop.

HOW IT WORKS?

First create a project and add the DataStore dependency, 
then you will be able instantiate and use the DataStore for your project usecase. 
For now the DataStore is available as a jar dependency only. 
it's mentioned in the repo itself , below readME.

Here's an example given below

/**
* Constructor initialize the DataStore with default storage location
*/
DataStore myDataStore = new DataStore();//
*/
DataStore myDataStore = new DataStore(String filePath);//pass file location

1. CREATE 

/**
*
* Method to create an element in the DataStore
*
* @param key
*            The key of the element
* @param value
*            The value of the element
* @return status of the operation
*/
myDataStore.create(String key, JSONObject value);

2. READ

/**
* Method to read an element from the DataStore
*
* @param key
*            The key of the element to read the element
* @return The value as type of JSONObject
*/
myDataStore.read(String key)


3. DELETE

/**
* Method to delete an element from the DataStore
*
* @param key
*            The key of the element to read the element
* @return The status of the delete operation
*/
myDataStore.delete(String key)
