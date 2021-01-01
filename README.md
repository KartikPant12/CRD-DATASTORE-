# CRD-DATASTORE-
Its a file based key-value datastore that supports CRD(create, delete, read) operations. it is meant to be local storage for one process on one laptop. 
How to use DataStore library?
First create a project and add the DataStore dependency, then you will be able instantiate and use the DataStore for your project usecase. 
For now the DataStore is available as a jar dependency only ( MUST DOWNLOAD FROM REPO).

//Constructor initialize the DataStore 
//DataStore myDataStore = new DataStore()
Constructor initialize the DataStore with given storage location
DataStore myDataStore = new DataStore(String filePath);//pass file location

CREATE
* Method to create an element in the DataStore
*
* @param key
*            The key of the element
* @param value
*            The value of the element
* @return status of the operation
myDataStore.create(String key, JSONObject value);
*
* @param key
*            The key of the element
* @param value
*            The value of the element
* @param timeToLive
*            Number of seconds after which the element is destroyed
* @return status of the operation
*/
myDataStore.create(String key, JSONObject value, int timeToLive);


READ
MEthod to read an element from the DataStore
*
* @param key
*            The key of the element to read the element
* @return The value as type of JSONObject
*/
myDataStore.read(String key)


DELETE
* Method to delete an element from the DataStore
*
* @param key
*            The key of the element to read the element
* @return The status of the delete operation
*/
myDataStore.delete(String key)

