# The past, present and future of local web applications
- HTML5 Storage is based on named key/value pairs. You store data based on a named key, then you can retrieve that data with the same key. 
  - The named key is a string.   
  - The data can be any type supported by JavaScript, including strings, Booleans, integers, or floats. However, the data is actually stored as a string. If you are storing and retrieving anything other than strings, you will need to use functions like parseInt() or parseFloat() to coerce your retrieved data into the expected JavaScript datatype.
  Calling setItem() with a named key that already exists will silently overwrite the previous value. Calling getItem() with a non-existent key will return null rather than throw an exception.
  - Like other JavaScript objects, you can treat the localStorage object as an associative array. Instead of using the getItem() and setItem() methods, you can simply use square brackets.
  - There are also methods for removing the value for a given named key, and clearing the entire storage area (that is, deleting all the keys and values at once).
    - interface Storage {
        deleter void removeItem(in DOMString key);
        void clear();
      };
    Calling removeItem() with a non-existent key will do nothing.
  - Finally, there is a property to get the total number of values in the storage area, and to iterate through all of the keys by index (to get the name of each key).
    - interface Storage {
        readonly attribute unsigned long length;
        getter DOMString key(in unsigned long index);
      };
    If you call key() with an index that is not between 0–(length-1), the function will return null.
- If you want to keep track programmatically of when the storage area changes, you can trap the storage event. The storage event is fired on the window object whenever setItem(), removeItem(), or clear() is called and *actually changes something*. 
- The limitations in current browsers is limited storage, the standard is only 5 megabytes. And also that programmers do not have the ability to request more storage.
- *Data is stored as strings. If you are storing something other than a string, you’ll need to coerce it yourself when you retrieve it.*