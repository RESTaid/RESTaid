# RESTaid
Converts JSON to XML and back again. Exposes a set of object manipulation functions to traverse object easily which includes: getting size of object, deep searching object, building sizzle (jquery) like string to preform deep search, storing each last so objects to not have to be passed as parameters either by reference or by this pointer, builds adhoc traversal similar to Windows(r) FindFirstFile and FindNextFile. Works as a script in your favorite browser or in Node.js without any dependancies.

Exported:
    
    Utility Functions:
        ToURIString: Creates a URI string.
        ToURIArray: Creates a URI array. URI arrays are used in all non-ulility functions.
        IsEmpty: Test to make sure object is not empty.
        Copy: Deep copies an object.
    
    Functions:
        ToJSON: Converts <argument> to JSON
        GetKeys: Proforms a search on the <argument> and builds an array with results.
        GetKey: traverses result of GetKeys -OR- finds the first instance of key request
        Size: Gets the count of all branches and leafs within JSON
        Branches: Wrapper to size. Gets the count of all branches [NOT LEAFS]within JSON
        Branch: traverses result of Branches
        Leafs: Wrapper to size. Gets the count of all leafs [NOT BRANCHES] within JSON
        Leaf: traverses result of Leafs [gets all values and returns the URI]
        ToXML: converts the JSON to XML.
        Cache: retreives a copy of the cache created from a function listed above.
   
    Rest Functions: Note: only OData 4.0+ will be impelmented.
        Legs: Builds array of all tables (Functions, Complex Types, Enum, etc too!)
        Leg: traverses result of legs
        Tables: Builds array of entry ("entity") tables
        Table: traverses result of Tables
        Columns: Builds array of all columns
        Column: traverses result of Columns
        Records: Builds array of all records. Use this to get your data.
        Record: traverses result of Records
        Aid: Helps newcomers to REST and OData to preform actions (filter, select, orderby, expand, etc.). Advanced uses will just use Records and Record.
        
