# Easy to use and fast PHP JSON database.
 
# Documentation
	
 var_dump($database->regex("/[a-zA-Z0-9\-\.\:\+\-\_\#\=\%\~\@]+/")); # Returns Array(...) or if not found null.
	
 var_dump($database->getStringVals()); # Returns Array(...) (All string values.) or if not found null.
	
 var_dump($database->getStringKeys()); # Returns Array(...) (All string keys.) or if not found null.
	
 var_dump($database->getNumericVals()); # Returns Array(...) (All numeric values.) or if not found null.
	
 var_dump($database->getNumericKeys()); # Returns Array(...) (All numeric keys.) or if not found null.
	
 var_dump($database->search("a")); # Returns Array(...) (Searches for the specified parameter in values.) or if not found anything null.
	
 var_dump($database->searchKey("a")); # Returns Array(...) (Searches for the specified parameter in keys.) or if not found anything null.
	
 var_dump($database->hasVal(1)); # Returns true (Checks if the specified parameter is equal to any value.) or if not equal false.
	
 var_dump($database->has(1)); # Returns true (Checks if the specified parameter is equal to any key.) or if not equal false.
	
 var_dump($database->set("key", "val")); # Returns true if successful or error code if an error occurred. (Note: Multiple entries can be made if the $val parameter is  specified as an array.However, for this, the third parameter must be true.) (IMPORTANT NOTE: When sending an array, it may produce unexpected results if you submit a missing key or value! If you don't send a key, a key will be assigned by default. For example 0.)
	
  var_dump($database->delete("key")); # Returns true if successful or error code (If the specified key is not found, it returns false.) if an error occurred.
		
  var_dump($database->get()); # Returns Array(["available"] => 1 ...) (If the parameter is not specified.) or if a parameter is specified and if it not found null.
		
  var_dump($database->update("key", "val")); # Returns true if successful or error code if an error occurred. (Updates a value for the specified key.)
		
  var_dump($database->add("key", "number")); # Returns true if successful (Adds the specified number to the value of the specified key.) or error code (If the       specified key is not found or if the value of the specified key is not a number, it returns false.) if an error occurred.
		
  var_dump($database->subtract("key", "number")); # Returns true if successful (Subtracts the specified number to the value of the specified key.) or error code (If the specified key is not found or if the value of the specified key is not a number, it returns false.) if an error occurred.
		
  var_dump($database->deleteFile()); # Returns true if successful or false if error occurred. (Deletes the called database file.)
		
  var_dump($database->deleteContent()); # Returns true if successful or false if error occurred. (Deletes all database content.)
		
  var_dump($database->order()); # Returns Array(...) or error code (Returns false if there is an error in the sequence.) if an error occurred. (Sorts all database content from A to Z, 0 to 9.)
		
   var_dump($database->reverse()); # Returns Array(...) or error code (Returns false if there is an error in the sequence.) if an error occurred. (Sorts all database content from Z to A, 9 to 0.)
